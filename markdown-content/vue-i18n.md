# Vue i18n

## A brief tour

<footer><small>16 July, 2019</small></footer>

<!-- Slide -->

## Hello

- Hi I'm Ezekiel, I currently work as a FE engineer at GitLab and have been there for ~6months
- I grew up in Newcastle, lived and worked in melbourne for quite a while and have been living in sydney for the last year. So im local-ish
- I obviously love programming, also making music 🎵 playing football ⚽ and learning about langauges and cultures

<!-- Slide -->

## Overview

- I'll be talking about internationalization (aka i18n) tonight, because i think its an area that's rarely touched on and quite possibly easily skipped in a lot of products, which is a shame since theres some really useful tooling around to support i18n efforts.
- While i'll talk broadly about a few topics, i'll be mostly focussing on one aspect of i18n which is translation
- I didnt want to only talk about vue-i18n, instead i thought it might be good to dive a little deeper and talk about some of what libraries like vue-i18n help you achieve and why they are so useful. So this wont be a strictly vue talk and that will make sense why, but ill definately touch on some of the tools available in the vue world
- So i'll cover a few topics
  - What is i18n & l10n
  - How we do i18n at GitLab
  - Tools available for vue

<!-- Slide -->

## Gitlab

- So the short summary if you havent come across GitLab, we are building a single application for the entire DevOps lifecycle.
  - ??More product stuff??
- We are a 100% remote company, so yes everyone works from home or whatever location suits them, currently with something like ~<some-number> members of staff across <some-number> countries around the world
  - Most importantly, we also have ~<some-number> pets.
  - Heres our pets page, theres some real cuties on there
- Currently and for the foreseeable future, our FE stack is in a period of transition

  - At heart of our product is a rails monolith, making use of haml for a lot of the views and templates
  - As time progressed,

- So being remote and spread across the world, you can imagine internationalization is a pretty big deal for us
  - ??While English is the working language of the company, its not necessarily the first language of everyone. This is true not just for us, but also many other product companies.??

<!-- Slide -->

## What is internationalization (i18n)

- i18n is really the process of developing a service or product that can be easily localized (adapted to different audiences).
  - For example:
    - Ensuring designs have enough space to accommodate strings in other languages / character sets
    - Developing layouts for right to left text
    - Ensuring strings in your program are easily translateable to other languages
- Localization (l10n) is about implementing your i18n process for a specific audience, this can include things like
  - translation into the relevant language(s)
  - time and date formatting appropriate for a locale
  - converting between timezones
  - correctly setting text direction
- Implementing an i18n process helps ensure youre delivering high quality products, that can be adapted to different audiences and provide each audience with the same experience you intend

<!-- Slide -->

## Translation

- general steps involved
  - Firstly, you need to mark all the strings within your application you would like to translate
    - GNU gettext is a common library used for this
    - The `gettext()` function call is often aliased to `_()`, which, no doubt can be a little confusing at first for js devs used to underscore/lodash
  - Once you've marked all your strings, you will need to create a dictionary of strings, this is used to generate the translation files for the languages you want to support
    - one example is .pot file, this is a po template file
    - show example of .pot file
  - Translate your strings (surprise surprise) based on the dictionary keys (lots of third party services for this)
    - show translated .po
  - Detect (or allow your user to specify) their locale
  - Load the relevant translation file for the selected locale, replacing all the keys in your application their translated text

<!-- Slide -->

## An example

- In the vue world, we have a useful library, called, surprise surprise vue-i18n
  - Explain the rules it provides
- Also provides some other useful helpers
  - ??Uses json formatted messages??
  - Locale setting
  - setup
  - Pluralization
  - Interpolation
  - Ensuring all your strings are up to date is one of the challenges
    - At gitlab we have some tools to help with this
    - We have some rules in our CI pipelines to detect marked strings that arent in the .pot
    - But with the added challenge that we have strings in numerous places, ruby files, haml templates, js, vue files and need to ensure these are always marked for translation
    - Something my team has been working on recently was some various linting tools to assist with identifying translateable strings in our codebase
    - Specifically i worked on one for .vue files, diving into the <template>, ill demo this later

<!-- Slide -->

## Example project

- Demo of vue-i18n
- I've been extending it with rules for detecting strings
  - Demo

<!-- Slide -->

## Final takeaways

- i18n and l10n arent as big and scary as you might think
- There are a few steps involved in the process but also lots of tools available so id suggest consider baking it in as early as possible to your product or website if you would like to reach a wider audience
- I'll be sticking around so feel free to ask me any questions about i18n, GitLab, working remotely or whatever else
- Why is it called i18n? - 18 characters between the i and the n in internationalization :)

## Ideas

- What i'll talk about + me

  - Just want to give a brief overview on internationalization, why its important and how to get started in your vue apps
  - I feel like this something that's often overlooked

  <!-- - I started SoftEng at Newcastle and switched to comp sci because it's a year shorter and I could skip the final year project (Trollface) - not even kidding
  - My first role after uni had communication in it which ironically was a poor communication of the role when I wanted to move on. -->

  - I used to call myself a full stack engineer,
  - Then started calling myself a front end developer
  - Then somewhere along the line I gave up and I just settle for what's currently on my twitter. - I'm not trying to be obtuse, but i just find these arbitrary labels a bit weird /rant.
  - So I'm currently a frontend engineer at gitlab 🤷‍♂️
  - What does FE look like?

    - all the things

      - rails: we go it
      - haml: we got it
      - es6: we got it
      - vuejs: we got
      - did you say jquery? yeah we got it

    - what does my day look like

      - 45% failed pipelines
      - 35% rspec tests
      - 10% js
      - 5% coffee related things
      - 5% laughing at markdalgleish's memes

- What is i18n

  - overview
  - Why i18n is important
    - Broader audience for your users, allowing users to use your tools and products in the language they are most comfortable with
    - Relatively easy to bolt-on to existing apps
  - general steps involved
    - High level, you create a dictionary of strings and reference the strings from the relevant language file in your app
    - Markup all strings in your code base
      - These will be used as keys mapped to a translation file
    - Generate translation file or template
      - Translate your strings based on the keys (lots of third party services for this)
    - Detect the user's language preference
    - Load the appropriate translation file for their language
  - Challenges / Considerations
    - Interpolation
      - v-html
      - escaping / xss
    - Pluralization
    - UI / design
      - For example: English strings will likely be a lot shorter than their international equivalents, so you need to leave some space in your UI to allow for this. This can break your UI if you're design for specific widths / sizes

- How do we do this at GL?

  - Why we needed to automate this
    - We have strings in various places of the codebase: ruby, haml, js, vue
  - Focus on externalization
    - Generate the AST
    - Look for valid string nodes
    - Autofix easy ones, warn tricky ones
  - Maybe do some rough stats on GL commits + vue files etc to illustrate scale

- How can you do this in your vue app

  - Show example app? - codesandbox?
  - vue-i18n

    - features
      - available rules
      - namespaces
      - pluralization
      - interpolation
    - config?
      - json format?
    - eslint-vue-i18n??

  - locale detection
  - language switcher
  - i18n plugin to get users language from browser?
  - vue-i18n:
  - playground?

## TODO build a slides webapp + i18n?

## Links

- [eslint plugin vue i18n](https://github.com/kazupon/eslint-plugin-vue-i18n)
- [GL: eslint plugin vue i18n](https://gitlab.com/ekigbo/eslint-plugin-vue-i18n)
- [mdn - gettext](https://developer.mozilla.org/en-US/docs/Mozilla/Localization/gettext)
- [Internationalization at GitLab](https://docs.gitlab.com/ee/development/i18n/externalization.html)
- [gettext plural forms](https://www.gnu.org/software/gettext/manual/html_node/Translating-plural-forms.html)
- [Transifex](https://www.transifex.com/)?
- [i18next](https://www.i18next.com/)
- [vue-i18next]()
- [vue-i18n]()
- [vue-i18n-starter](https://github.com/dobromir-hristov/vue-i18n-starter)
- [W3c - Text size in translation](https://www.w3.org/International/articles/article-text-size)
- [Wikipedia - Internationalization / Localization](https://en.wikipedia.org/wiki/Internationalization_and_localization)
- [localeplanet](http://www.localeplanet.com/)
