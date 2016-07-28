# Code for Australia - NJC Fellowship
## Summary
My year as a fellow has been nothing short of interesting, I've enjoyed having the opportunity to work with the Neighbourhood Justice Centre, exploring what community justice means and how it can be realised.

I decided to apply for the fellowship because I was looking for a change in my career. I wanted an opportunity to bring all the skills and knowledge that I had learned through studying, working at universities, freelancing for small businesses and startups togethor to work on meaningful work that could have an impact on everyday citizens lives, help government deliver solutions for its citizens that meets their needs and reduce the frustration of dealing with government services.

The fellowship has given me the opportunity to work with a diverse range of people passionate about the work they do for the community, it's given me the chance to apply my technical and analytical skills in a domain outside my understanding and also explore a variety of projects.

## Research
During my research period, my time was spent trying to get a better understanding of who the NJC are and what they do. I spent roughly 60 days working at the NJC getting involved in the day to day by:
- Shadowing staff across all different areas of the NJC in their work
- Observing the different types of court cases seen at the NJC
- Attending meetings both on-site and in the community with staff members and sitting in on appointments with clients
- And by asking lots and lots of questions

What I wanted to understand from this was:
- their context - why they exist, what do they do, who do they work with and how do they do this
- their constraints - technical, resourcing and administrative constraints
- their pain points - this included the pain points that I observed, processes I noticed could be improved by some simple technology and issues staff were telling me about
- previous solutions and upcoming projects - what were some of the solutions that had been previously tried to alleviate some of the pain points, I didnt want to recreate solutions that had already been tried and tested.

### Research outputs
THIS SHOULD ALL BE IN A SINGLE DRIVE FOLDER
* [Draft plan](https://docs.google.com/a/codeforaustralia.org/document/d/1P_RL06H0FK-DSSnlRjlFwCoUDheLsRlkTo4IQcy_Yuw/edit?usp=drive_web)
* [Possible questions](https://docs.google.com/a/codeforaustralia.org/document/d/1ZNwN5d7I5YODZn-roO8UyTWh7uK_YU4aAlQ17S3033Y/edit?usp=drive_web)
* [Trello - Shadowing Tasks](https://trello.com/b/JQkz4SSo/tasks)
* [Trello - Ideas](https://trello.com/b/rqGrXZI8/ideas)
* [Trello - Context/Tools/Data](https://trello.com/b/iJQVp70E/context-data-locale-software-skills)
* [Possible problems](https://docs.google.com/document/d/1K-nJ_UJ8YjQeK-etNyQqE7aUMF3-wO6b2XAS-PLz4MY/edit)
* [Workshop plan - Oct 27](https://docs.google.com/document/d/1GVY_11MLdnIImb4xaVj1pCfcSnyGIhNPRicqkRgJAnM/edit)
* [Problem list - Workshop Oct, 27](https://docs.google.com/a/codeforaustralia.org/document/d/1ei3nhEUEDj4k-WtX5gTj3YNGtrXzSNulDdSV5334toY/edit?usp=drive_web)
* [Solutions list - Workshop with Client services Dec, 1](https://docs.google.com/document/d/1m9j1RvoM6uUL240SAy8ZJxCVToBS1tU5zeEmYHhzRmk/edit)
* Link to research report
* Link to public blog posts

## Prototypes
After the research stage, we had a range of pain points of various sizes that were ready for further exploration. Solutions were then prototyped at different levels to allow us to start exploring:
- Soundness of the solution
- Complexiity of implementing the solution
-


### Electronic access to documents
Digitising and providing the option of online access to family violence and personal safety orders, and other court documents to NJC clients.
* Clients are given a paper copy of their court documents (in person or via mail)
* The NJC would like to give clients the option of online access to their documents to be able to access them at any time such as when an incident occurs and you need to convey the terms of your order to the police.
* Focusing on Family violence intervention and Personal safety orders (FVIO/PSO)

Created a mobile [responsive prototype](http://njc-efv.herokuapp.com)

### Calendar of appointments
Providing online access to a list of your upcoming appointments (with social workers) at the NJC and for court dates. Clients turn up for appointments, sometimes they don't have an appointment scheduled, the details have changed or they have the wrong date, the information team usually are the first contact and must call / email / search around to verify the meeting. Clients check in with the court registry when they arrive for their court date, social workers routinely check with the registry to see who has attended for the day.

* Provide a calendar of appointments for the information team to verify clients have an appointment with person X
* Access to the details of upcoming appointments and court dates
* Clients check-in when they arrive at the NJC - allow social workers to see who has attended, clients have a record that they attended
* Ability to reschedule appointments if you need to
* New appointment requests sent to your account and you can accept / propose a new time

Mockups produced:
* Mocking [interface for clients](https://app.moqups.com/ekigbo/ShWGM4yt7q/view/page/a0056ded4)
* [Mocking interface](https://app.moqups.com/ekigbo/ShWGM4yt7q/view/page/a298c2517) for list of appointments, who has attended and creating a new appointment

I recommend keeping an eye on the work being done by DTO on an [appointment booking tool for citizenship](https://github.com/AusDTO/citizenship-appointment-client).

### In / Out board
Staff send emails around each day to notify each other of changes in their work schedule (leaving early, going home sick, working from home), there is also a duty worker assigned each day. This is also sent around as an email. The information team have been trialling [inoutboard](https://www.inoutboard.com/) to reduce the number of these emails being sent and keep an eye on who is around, who is out and who might be on leave.

#### Status: Early progress
* Ran a session with client services staff to understand why they werent using in/out board + what could improve it
* Mocking a possible alternative to test
  - [See who is in / out](https://app.moqups.com/ekigbo/5ZBPPdq0mn/edit/page/ae4e92ceb)
  - [Update my in / out](https://app.moqups.com/ekigbo/5ZBPPdq0mn/edit/page/a6650e232)
  - [Set up a schedule for my regular hours](https://app.moqups.com/ekigbo/5ZBPPdq0mn/edit/page/acb56e560)
  - Integrate into the [NJC Intranet](#njc-intranet)

### NJC Website
The NJC are rebuilding their website, we are hoping to tie in some community engagement activities into the process to show how you can involve your clients and community in government projects.

More user research required

#### Status: Early progress
* [Pausefest session](/docs/pausefest-session) on card sorting current NJC website content

### NJC Map
The NJC want to show how community justice can work, and the work that has been done in the City of Yarra. The focus will be on the partnerships between different social agencies and how they collaborate.

Further validation of the idea required

#### Status: Early progress
* [Mocked prototype](https://app.moqups.com/ekigbo/5ZBPPdq0mn/view/page/a1c9a6a86)
* Next steps:
  - Gather sample data
  - Produce working demo - demo around to get other agencies on board to contribute data

## Events
* Links to slides and presentations
* Observations Session
* Workshop with staff??
* Card Sorting - website
* Pausefest
* Prototype feedback
* Hackathons - govjam, red cross, budgethack

## Recommendations
### Online Pleas
* This is ready for a pilot test
* Integration with courtlink and other systems to:
  - Provide functionality for clients to check if their case is eligible
  - Provide administration flow to properly action pleas that are requested
// ADD POTENTIAL FEATURES FROM TRELLO

### Case Triage
* this is ready for a pilot test
* pilot should focus on using the tool as the first point of interaction for staff, with paper as a backup
* Automatic case population from courtlink
* Pilot should be at 1 - 3 months
* Should eventually be part of a wider ecosystem of digital tools, linking into other systems that staff use
* Expand the reporting and data insights
// ADD POTENTIAL FEATURES FROM TRELLO

### Intranet
* document versioning
* This requires more user research, the pain points it currently addressed were more of the 'obvious' use cases, but there would be more potential for this to truly help with information / knowledge sharing
* What are the use cases for other courts?
* Any NJC website update should start to incorporate an intranet aspect as well
* Staff In/Out - this could probably be pursued as a standalone platform, focused on managing who is currently at the NJC
  - Investigate modes of updating your status to reduce friction for users, email a specific inbox, bookmarklets, webapp?
  - prompts and reminders for staff to update their status
// ADD POTENTIAL FEATURES FROM TRELLO

## Final thoguhts
One of the clear challenges for any government organisation taking on year long fellows is the difficulty in being able to pinpoint exactly what the outcomes of the process will be, nonetheless the NJC were committed to exploring how they could find new ways to continue the work they do and also use the opportunity to learn something from the process. This proved to be one of the biggest strengths of the experience as it allowed me to explore the centre, not only as a passive observer but as an active particpant that could provide insights and draw conclusions that come when you're looking from a fresh perspective.

## Thanks
Special thanks to the following people: Kerry Walker, Gavin Hince, Louise Bassett, Anthony Ket, Cameron Wallace, Pene Knight, Diane Arsic, Damian James, Ann Strunks, Jo Szczpanska, Vanessa Toholka, Andy Johnston, Jacob Lindsay, Alvaro Maz, Dan Groch, Bluebird Espresso, Everyday Coffee and all the other amazing baristas that kept me caffeinated along the way.

## Useful links
