# Vue i18n

### A brief summary

<footer><small>16 July, 2019</small></footer>

<!-- Slide -->

### Hello

- I'm Ezekiel
- FE @ GitLab
- New(ish) to Vue

<!-- Notes -->

- Hi I'm Ezekiel, I currently work as a FE engineer at GitLab and have been there for ~6months
- I obviously love programming, also making music 🎵 playing football ⚽ and learning about langauges, different cultures and history
- Prior to joining GitLab I mostly worked with React and before that angular 1.5, you know, the good one
- But I've enjoyed the transistion to vue because of its flexibility,its not overly complex and the great community and wide range of libraries and resources available to help

<!-- Slide -->

### GitLab

- Single application for software development, incl: Source code management, project management, CI, CD, Security (SAST and DAST) and metrics on your running applications

<!-- Notes -->

- So the short summary if you havent come across GitLab, we are building a single application for the entire software development lifecycle.
  - What does that mean? Well it means we have solutions for source code management, code review, project management, CI, package management
  - Additionally we have both a SAAS offering or you can run our tools on your infrastructure
- Currently and for the foreseeable future, our FE stack is in a period of transition

  - At the heart of our product is a rails monolith, with a lot of our views originally written in haml
  - Over time the codebase has become more dynamic, making greater use of JS and we eventually settled on vuejs as our path forward

<!-- Slide -->

![Remote company](./images/vue-i18n/remote.png) <!-- .element height="67.5%" width="67.5%" -->

- 100% Remote, that's correct! REMOTE!
- We work in the open
- ~750 staff across 55 countries

<!-- Notes -->

- We are a 100% remote company, so yes everyone works from home or whatever location suits them, currently with something like ~750 members of staff across 55 countries around the world

- So being remote and spread across the world, you can imagine internationalization is a pretty big deal for us
  - While English is the working language of the company, its not necessarily the first language of everyone. This is true not just for us, but also many other product companies.

<!-- Slide -->

### PETS!!!!

![Odin](./images/vue-i18n/odin-the-destroyer.png) <!-- .element height="67.5%" width="67.5%" -->

<!-- Notes -->

- Most importantly, we also have ~170 pets.
- Heres our pets page, theres some real cuties on there

<!-- Slide -->

### ...and cool swag

![Swag](./images/vue-i18n/socks.webp) <!-- .element height="67.5%" width="67.5%" -->

<!-- Notes -->

- GL socks
- You'll often see gitlabbers out in the wild in different shades of purple and orange

<!-- Slide -->

### Overview

- What is internationalization (i18n)?
- Localization (l10n)
- Translation
- Vue-i18n

<!-- Notes -->

- I'll be talking about internationalization (aka i18n) tonight, because i think its an area that's rarely touched on and quite possibly easily skipped in a lot of products, which is a shame since theres some really useful tooling around to support i18n efforts.
- While i'll talk broadly about a few topics, i'll be mostly focussing on one aspect of i18n which is translation
- I didnt want to only talk about vue-i18n, instead i thought it might be good to dive a little deeper and talk about some of what libraries like vue-i18n help you achieve and why they are so useful. So this wont be a strictly vue talk and that will make sense why, but ill definately touch on some of the tools available in the vue world
- Hopefully by the end, you'll have some intuition about i18n and l10n

<!-- Slide -->

### I18n - what is it?

> Developing a service or product that can be easily localized

<!-- Notes -->

- i18n is really the process of developing a service or product that can be easily localized (adapted to different audiences).
  - For example:
    - Ensuring designs have enough space to accommodate strings in other languages / character sets
      - For example: Quite often English strings end up shorter than their international equivalents, so you need to ensure your UI can grow to accommodate additional characters. This can break your UI if you're design for specific widths / sizes
    - Developing custom layouts for right to left text
    - Ensuring strings in your program are easily translatable to other languages

<!-- Slide -->

### Localization (l10n)

![Herbs vs Erbs](./images/vue-i18n/erbs.gif)

> Implementation of i18n processes for a particular audience

<!-- Notes -->

- Localization (l10n) is about implementing your i18n process for a specific audience, this can include things like
  - swapping z's for s's
  - translation into the relevant language(s)
  - time and date formatting appropriate for a locale
  - converting between timezones
  - correctly setting text direction
- Implementing an i18n process helps ensure youre delivering high quality products, that can be adapted to different audiences and provide each audience with the same experience you intend

<!-- Slide -->

### Translation

- Mark translatable strings
- Create a translation file for each language
- Translate the strings (duh)
- Detect your user's language preference and load the relevant translation file

<!-- Notes -->

In general, there are a few steps involved in translating,

- Mark translatable strings
- Create a translation file for each language
- Translate the strings (duh)
- Detect your user's language preference and load the relevant translation file

<!-- Slide -->

### Translation - gettext

```javascript
gettext("This is an awesome text string that should be translated");
```

```javascript
__("This is a convention for translatable text");
__("Hello people!");
```

<!-- Notes -->

- Firstly, you need to mark all the strings within your application you would like to translate
  - GNU gettext is a common library used for this
  - The `gettext()` function call is often aliased to `_()`, which, no doubt can be a little confusing at first for js devs used to underscore/lodash

<!-- Slide -->

### Translation - json

```json
{
  "greeting": "Hallo Leute!",
  "synthsMessage": "Habe aber {count} synthesizers 🎹🎵",
  ...
}

```

<!-- Notes -->

- Once you've marked all your strings, you will need to create a dictionary of strings, this is used to generate the translation files for the languages you want to support
  - You will usually execute an externalization function to extract all your `gettext` marked strings
- This is an example of a json format dictionary

<!-- Slide -->

### Translation - .pot

```
...
"Language-Team: LANGUAGE <LL@li.org>\n"
"Language: \n"
...
"Plural-Forms: nplurals=INTEGER; plural=EXPRESSION;\n"

msgid "Please sign in."
msgstr ""

msgid "%d cat,"
msgid_plural "%d cats,"
msgstr[0] ""
msgstr[1] ""
```

<!-- Notes -->

- One of the other common formats is the .pot file, or .po template
- The .pot template shows the relevant string keys and also gives information on the type of pluralization rules supported
- Ensuring all your strings are up to date is one of the challenges
  - At gitlab we have some tools to help with this
  - We have some rules in our CI pipelines to detect marked strings that arent in the .pot
  - But with the added challenge that we have strings in numerous places, ruby files, haml templates, js, vue files and need to ensure these are always marked for translation
  - Something my team has been working on recently was some various linting tools to assist with identifying translatable strings in our codebase
  - Specifically i worked on one for .vue files, to detect strings that should be marked

<!-- Slide -->

### Translation - translated pot

```
...
"Language-Team: German\n"
"Language: de_DE\n"
...
"Plural-Forms: nplurals=2; plural=(n != 1);\n"
...
"PO-Revision-Date: 2019-06-14 20:03\n"

msgid "Please sign in."
msgstr "Bitte melde dich an."

msgid "%d cat,"
msgid_plural "%d cats,"
msgstr[0] "%d Katze,"
msgstr[1] "%d Katzen,"
```

<!-- Notes -->

- Translate your strings (surprise surprise) based on the dictionary keys (lots of third party services for this)

<!-- Slide -->

### Translation - translate

![Translated app](./images/vue-i18n/translated.png) <!-- .element height="67.5%" width="67.5%"  border="none"-->

<!-- Notes -->

- Detect (or allow your user to specify) their locale
- Load the relevant translation file for the selected locale, replacing all the keys in your application their translated text

<!-- Slide -->

### What about vue? - Step 1

> npm install vue-i18n --save

![Coffee time](./images/vue-i18n/goals.gif)

<!-- Notes -->

- In the vue world, we have a useful plugin, called, surprise surprise vue-i18n
- You can install this plugin and be off to a great start
- Additionally we also have `eslint-plugin-vue-i18n` which provides some extra eslint rules to help with i18n such as checking for unused keys, or keys missing from your message files. It also looks like they recently added support for bare string detection, warning when you have strings that should be marked for translation.

<!-- Slide -->

### Cool plugin m8!

```json
const messages = {
  en: {
    message: {
      hello: '{msg} world'
    }
  }
}
```

```html
...
<div id="app">
  <p>{{ $n(100, 'currency') }}</p>
  <p>{{ $n(100, 'currency', 'ja-JP') }}</p>
</div>

...
<!-- output -->
<div id="app">
  <p>$100.00</p>
  <p>￥100</p>
</div>
...
```

<!-- Notes -->

- This plugin, while not complete, does covers a lot of the relevant parts of i18n for vue apps and can be a great place to kick off
  - It supports JSON tranlsated messages
  - Datetime localization
  - Number format localization

<!-- Slide -->

### What about vue? - Step 2:

![Coffee time](./images/vue-i18n/coffee-time.gif)

<!-- Slide -->

### But wait... there's more

![But wait, theres more](./images/vue-i18n/theres-more.gif)

Locale setting, Pluralization, Interpolation & Lazy loading translations

<!-- Notes -->

- Also provides some other useful helpers
  - Locale setting - locale can be specified dynamically and switched at will
  - Pluralization - out of the box support for specifying how to pluralize you content, allowing you to set different text based on a variable
  - Interpolation - allowing you to mix html into your translations
  - Lazy loading translations - very useful once the strings in your application start to grow. Loading all the translations at once isnt very efficientg

<!-- Slide -->

### Example project

https://gitlab.com/ekigbo/say-hello

<!-- Notes -->

- Demo of vue-i18n
- I've been extending it with rules for detecting strings
  - Demo

<!-- Slide -->

### Final takeaways

```javascript
console.log('i' + 'nternationalizatio'.length + 'n')
=> i18n

console.log('l' + 'ocalizatio'.length + 'n')
=> l10n
```

> Follow me <strong>@theatlasroom</strong>

<!-- Notes -->

- i18n and l10n arent as big and scary as you might think
- There are a few steps involved in the process but also lots of tools available so id suggest consider baking it in as early as possible to your product or website if you would like to reach a wider audience
- I'll be sticking around so feel free to ask me any questions about i18n, GitLab, working remotely or whatever else

### Links

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
