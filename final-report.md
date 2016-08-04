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

After the research stage, we had a range of pain points of that were ready for further exploration. Solutions were then prototyped at different levels to allow us to start exploring the soundness of the solution, complexity of implementing the solution and any areas that would require further research to properly define the problem to be tackled.

The prototyping stage was spent working with a range of staff within the njc, an iterative approach was taken to all prototypes focusing on regular feedback from stakeholders and regular updates on progress. While the majority of the time was spent working from our Code for Australia offices, regular meetings were scheduled with key stakeholders to update on progress, highlight and address any issues that have arisen and to plan the next steps for each prototype.

## Projects
### Online Pleas
Online pleas progressed the furthest out of all the prototypes, we developed a simple prototype to allow individuals to submit a guilty plea for minor infringements online. The prototype demonstrates how a guilty plea could be lodged online prior to the scheduled court date for non-complex minor offences - typically these offences comprise nearly 50% of MCV’s (Magistrates Court Victoria) case volume.

The prototype was developed to be a simple online form that would allow clients to fill in some simple information about who they are, the offence that they are choosing to plead guilty to and a message to the magistrate. The message to the magistrate might include explaining why you offended, your personal or financial circumstances, and things you would like the magistrate to consider when deciding your sentence. The form also includes declarations from the client acknowledging that they have the option to plead guilty or not guilty to the offences and that the plea is entered voluntarily of their own will. Once the form is completed, a copy is formatted and sent to the registry ready to be processed by the magistrate.

A lot of investigation and changes were required along the way, initially we had hoped clients could simply enter an offence number which would identify their case but because of the different systems used between police and the courts, this could not be easily established. Types of offences that were too complicated or had the potential to slow down progress were removed altogethor. Additionally we spent time understanding how to communicate this service to clients of the court, how the registry could quickly identify the relevant cases and include the right information in the summons.

This prototype is now ready for a pilot test with real world users, the pilot test should be an opportunity to gain feedback and research from real court clients, it should provide further insight in the likelihood of court

Further improvements needed after the pilot include:
* Planning for multiple sites - the current prototype is NJC specific
* Integration with the courts systems to identify upcoming matters that might be eligible
* Workflow for registry staff to simplify identifying potential matters, notifying the clients of the option and updating the court records
* The ability to have a standardised offence number which could be used to identify the matter
* Thorough review of the types of cases that could be included
* User experience research and testing

### Case Triage
One of the strengths of the NJC is the wholistic approach taken to supporting their clients. Client services is mostly composed of staff from various service providers within the City of Yarra, specialising in a vast array of different areas such as drug and alchohol counselling, family violence support, financial and housing support among others. This is particularily showcased in the NJC's approach to family violence matters.

Family violence matters are all heard on the same day, in the week prior to the hearings, staff prepare background information on each of the members in the matter. This allows each of the service providers to not only share any information they might have that could be beneficial to the client, but also for the staff to assess what kind of situation the client is and which services might be appropriate to provide support for the client on the day. This whole process comes in contact with most of the services within the NJC included the legal staff, court registry and most of the service providers. Prior to the matters being heard, all the service providers meet to go through the cases togethor update any new information and decide on which services should be assigned to which clients. Throughout the day staff update each other on the progress of the matters they have been assigned where necessary.

This process is mostly manual with highlighted sheets of paper passed around to communicate a range of information, additionally it is difficult to look back through the history of records for information on the outcomes of a matter and of the different support that was provided from the services, some of the information is recorded on the NJC's case management tool, mostly information about referrals made for a client, but there was a definite gap of information that is not recorded that really captures the full scale of the support the NJC staff provide to their clients.

The case triage dashboard provides an opportunity for all the staff involved in the family violence cases to:

* Assign services to provide support for a client
* Track which services met with a client and what support was offered
* Search a history of all the cases that have been entered and view any relevant outcomes + services provided
* Enter outcomes from a hearing for each case
* Update cases with a legal conflict, allowing the registry to plan which cases might require an alternative legal provider
* Export all the data for quantitative analysis
* Update client information like name and date of birth when not available from the court listing

This prototype was able to give use enough information about how a tool like this could be useful, we could test it within a small group of the NJC service providers without disrutping their day to day work and start to explore where the areas of improvement would be.

The next steps required would be for a proper pilot test to be conducted for at least a month, the pilot would be an opportunity to trial completely replacing the paper process, retaining the paper as a backup and thoroughly testing not only how useful the tool is for all the services included but also delve into any of the edge cases we might have missed.

One of the major limitations of the current prototype is the lack of integration with the courts case system, this proved to be a constant point of blockage during the fellowship so we opted to manually enter the cases each week when they are available. This is a far from ideal solution and adds uneeded overhead to the process, the ideal solution would be a direct feed from the courts system to populate the list of cases for the next week, removing the need for manual entry and reducing the likelihood of errors.

Other areas for further improvement include:

* Integration with other NJC and courts systems to share information
* Expanding the reporting and data available
* User experience testing

### Intranet
This prototype was mostly the result of a series of earlier prototypes around improving internal communications, staff updates and knowledge sharing at the NJC. A large group of the NJC staff are employed by external service providers but they work within the centre for the majority of their week, this results in an environment where different staff have different levels of access to information, tools and software necessary for their day to day work, additionally staff regularly work in the community outside the centre on varying schedules making it difficult to know is currently available in the centre. The prototype provided an opportunity to envision what an intranet for a magistrates court could look like, it provided an opportunity to explore what kind of features could be useful for staff in their day to day work and also help improve the communication and knowledge sharing between the different teams.

We focused on document and information (news, events) management and a central staff listing with , this was one of the key areas of interest.

We were able to develop a working prototype to provide a central location for:

- Managing links to all documents, policies, procedures and forms
- Quick access to contact details for the current duty worker
- Sharing news and upcoming events
- Staff in and out status
- Integrated search across staff contact details, documents, news and events
- An opportunity for staff to provide feedback for improvement

While the prototype worked well enough as a mechanism to gather feedback from the different teams within the NJC to help shape how a tool like this could be used, there was definately room for further improvement and development. This requires more user research, the pain points it currently addressed were really more of the 'obvious' use cases, but there would be more potential for this be something that is embedded deeply into how the NJC shares information and knowledge internally.

Some of the features that were discussed but not implemented included:
* Library of information research staff come across relating to community justice
* Utilising existing tools from MCV for hosting and development of the intranet
* The ability to view previous versions of a document

Particularly the staff in and out board, this could be pursued as a standalone solution to help communicate who is currently at the NJC and who the duty worker for the day is, further work would need to be done to:

* Investigate options for updating your status to reduce friction for users ie email a specific inbox, saving a bookmarklet, webapp
* Sending prompts and reminders for staff to update their status
* Integration with any appointment management tool

## Prototypes
### Electronic access to documents (Prototype)
One of the first areas of exploration was around access to court documents, currently documents such as court dates, summons and intervention orders are printed and either physically handed to clients or sent by mail. We decided to focus on was Personal safety and Family violence intervention orders. These are legal documents with specific terms used to outline the conditions of the order, respondents are expected to understand the terms of the order to ensure they can avoid a breach, and affected members are also required to understand them in the event that a breach does occur and police or other authorities need to be notified.

We wanted to provide a simple, accessible option for clients to have easy access to an up to date copy of this order. In the event of the terms of the order changing, we wanted clients to be able to access the most up to date information whenever they needed it.

A mobile [responsive prototype](http://njc-efv.herokuapp.com) to illustrate how this might work from the clients perspective. We also explored how this might be implemented into a broader project for online family violence intervention orders which the NJC had started to explore. This prototype was well received and will be incorporated into a future project.

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

### Staff in / out (Mockups / prototype)
Staff send emails around each day to notify each other of changes in their work schedule (leaving early, going home sick, working from home), additionally a duty worker is assigned each day to provide frontline assessment of clients, this information is sent around by the staff member assigned to the role. to reduce the number of these emails being sent and keep an  eye on who is around, who is out and who might be on leave. Being the first contact for the any visitor to the centre, the information team are often tasked with tracking down the relevant staff members.

A session was held with staff to dive deeper into what an ideal solution for the NJC might look like, mockups were then produced and a prototype of this was eventually incorporated into the intranet project, along with a general, searchable listing of staff contact details.

### NJC Map (Mockups / research)
The NJC were interested in finding ways to visualise how community justice can work, in particular what has worked within the City of Yarra, focusing on the partnerships between the different service providers in the community and how they have collaborated and contributed to tackling some of the more complex issues in the city. Additionally the map could also prove to be a starting point with service providers the NJC had not previously engaged with, or to help share the knowledge held within the community.

We decided to take the approach of focusing on cases studies in the area, coupled with quantitative data. Mockups were produced over a few iterations to highlight how this might all come togethor.

More research is required to find the kind of case studies and datasets that would be required for this project, the most important step would be to start engaging with local service providers and gauge what information is currently available, or could be pieced togethor to tell a story. Additionally, as this should also be a tool to help 'tell the story' of community justice in the City of Yarra, further research is needed to decide on the appropriate mediums to convey this information. The mockups focused on a web-based interface, but it could be a good opportunity to start exploring other technology such as touchscreen interfaces or augmented reality.

## Final thoguhts
One of the clear challenges for any government organisation taking on year long fellows is the difficulty in being able to pinpoint exactly what the outcomes of the process will be, nonetheless the NJC were committed to exploring how they could find new ways to continue the work they do and also use the opportunity to learn something from the process. This proved to be one of the biggest strengths of the experience as it allowed me to explore the centre, not only as a passive observer but as an active particpant that could provide insights and draw conclusions that come when you're looking from a fresh perspective.

The end result being that we were able to create an environment for the NJC to incubate and explore ideas they had, we could quickly try applying a solution to a pain point and then assess the viability for the solution in-house without having to contract the work needed for a prototype which would have added extra delay and cost.

## Thanks
Special thanks to the following people: Kerry Walker, Gavin Hince, Louise Bassett, Anthony Ket, Cameron Wallace, Pene Knight, Diane Arsic, Damian James, Ann Strunks, Jo Szczpanska, Vanessa Toholka, Andy Johnston, Jacob Lindsay, Alvaro Maz, Dan Groch, Bluebird Espresso, Everyday Coffee and all the other amazing baristas that kept me caffeinated along the way.
