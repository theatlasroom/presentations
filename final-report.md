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

## Prototyping activities
After the research stage, we had a range of pain points of that were ready for further exploration. Solutions were then prototyped at different levels to allow us to start exploring the soundness of the solution, complexiity of implementing the solution and any areas that would require further research to properly define the problem to be tackled.

### Electronic access to documents (Prototype)
Digitising and providing the option of online access to family violence and personal safety orders, and other court documents to NJC clients.
* Clients are given a paper copy of their court documents (in person or via mail)
* The NJC would like to give clients the option of online access to their documents to be able to access them at any time such as when an incident occurs and you need to convey the terms of your order to the police.
* Focusing on Family violence intervention and Personal safety orders (FVIO/PSO)

We created a mobile [responsive prototype](http://njc-efv.herokuapp.com) to illustrate how this might work and fit within the NJCs broader project on a online family violence intervention order. This prototype was well received and will be rolled out into a future project.

### Staff in / out (Mockups / prototype)
Staff send emails around each day to notify each other of changes in their work schedule (leaving early, going home sick, working from home), additionally a duty worker is assigned each day to provide frontline assessment of clients, this information is sent around by the staff member assigned to the role. to reduce the number of these emails being sent and keep an  eye on who is around, who is out and who might be on leave. Being the first contact for the any visitor to the centre, the information team are often tasked with tracking down the relevant staff members.

A session was


### Calendar of appointments (Mockups / additional research)
We saw a good opportunity for providing online access to a list of upcoming appointments, both for NJC clients and staff. Clients turn up for appointments, sometimes they don't have an appointment scheduled, the details have changed or they have the wrong date, the information team usually are the first contact and must call / email / search around to verify the meeting. Clients check in with the court registry when they arrive for their court date, social workers routinely check with the registry to see who has attended for the day.

* Provide a calendar of appointments for the information team to verify clients have an appointment with a staff member
* Access to the details of upcoming appointments and court dates
* Clients check-in when they arrive at the NJC - allow client services staff to see who has attended
* Clients have a record that they attended
* Ability to reschedule appointments if you need to
* New appointment requests sent to clients with and option to accept / propose a new time that might be more appropriate

Mockups and a process map were produced after some additional user interviews to better understand how this solution might look and how it could be integrated into the work the NJC staff.

Additionally it would be useful to keep an eye on the work being done by DTO on an [appointment booking tool for citizenship](https://github.com/AusDTO/citizenship-appointment-client).

### NJC Website (Additional research)
The NJC had begun exploring what a new website might look like for them, so we spent some time conducting some additional research to help prepare for this project. Some preliminary work had been conducted on a possible Information Architecture, so we decided to explore what it might mean to try and test that with a wider audience.

We held a workshop at the [2016 Pausefest](www.codeforaustralia.org/blog/pausefest-2016-re-building-a-government-website) conference with participants so we could try to possibly:

* Identify some areas that might be missing from the current website and IA
* Generate a possible IA from the NJCs current content
* Protosketch ideal solutions for a NJC service or a new website

The results of this session along with an internal session held with staff for the same IA and a deeper look at some analytics data provided some new perspectives and possible ideas for the new NJC website which will be continued by the NJC.

### NJC Map (Mockups)
The NJC were interested in finding ways to visualise how community justice can work, in particular what has worked within the City of Yarra, focusing on the partnerships between the different service providers in the community and how they have collaborated around challenges in the community.

Further validation of the idea required

* [Mocked prototype](https://app.moqups.com/ekigbo/5ZBPPdq0mn/view/page/a1c9a6a86)
* Next steps:
  - Gather sample data
  - Produce working demo - demo around to get other agencies on board to contribute data


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
