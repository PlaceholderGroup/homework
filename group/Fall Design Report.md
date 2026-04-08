# Fall Design Report
A comprehensive report of the progress made and assignments completed for CS 5001.

**Table of Contents**
1. [Team names](#team-names) (include Advisor) and [Project Abstract](#abstract) (limit of 400 ascii chars)
2. [Project Description](#project-description) (Assignment #2)
3. User Stories and Design Diagrams (Assignment #4)
    - [User Stories](/group/User_Stories.md#user-stories)
    - [Design Diagrams](/group/User_Stories.md#design-diagrams): Level 0, Level 1 and Level 2
    - [Description of the Diagrams](/group/User_Stories.md#design-diagrams): including conventions and a brief description of the purpose of each component.
4. Project Tasks and Timeline (Assignment #5-6)
    - [Task List](/group/Milestones%2C%20Timeline%2C%20and%20Effort%20Matrix.md#milestones)
    - [Timeline](/group/Milestones%2C%20Timeline%2C%20and%20Effort%20Matrix.md#timeline)
    - [Effort Matrix](/group/Milestones%2C%20Timeline%2C%20and%20Effort%20Matrix.md#effort-matrix)
5. [ABET Concerns Essay](/group/Project%20Constraints%20Essay.md) (Assignment #7)
6. [PPT Slideshow (includes ABET Concerns)](#ppt-slideshow) (Assignment #8)
7. [Self-Assessment Essays](#self-assessment-essays) (Assignment #3)
8. [Professional Biographies](#professional-biographies) (Assignment #1)
9. [Budget](#budget)
10. [Appendix](#appendix)

## Team Names
**Advisor**:
- Dr. Jillian Aurisano

**Team Members**:
- Anne Ning
- Jack Detrick
- Jonah Carter
- Kevin Long

## Abstract
A cross-platform mobile app that makes it dead-simple to share the correct contact info with the correct people. Allows for both granular control over the details shared with each person and pre-saved profiles to make any type of contact sharing a breeze! Utilizing technologies like NFC, RFID, and QR codes our focus is on making the experience frictionless for both the sharer and the receiver.

## Project Description
A cross-platform mobile app that makes it *dead-simple* to share the correct contact info with the correct people *every time*. Our app will allow granular control over the details shared with each person and come with pre-saved profiles to make business, personal, and any other category of contact information sharing a breeze!

Our focus is on making the experience as frictionless for both the sharer and the receiver as possible. We plan to utilize technologies like NFC, RFID, and QR codes to offer a sharing experience that works in all situations, regardless of internet connection, or the busyness of the environment with intelligent fallbacks depending on the surroundings.

## PPT Slideshow
- [Slides](https://docs.google.com/presentation/d/1QuAuR-Rzw4278_MuOEcm_G7NuQxXVfcbX-eU6XOwzng/edit?usp=sharing)
- [Video](https://uc.mediaspace.kaltura.com/media/t/1_k1c30a46)

## Self-Assessment Essays
- [Anne Ning](/individual/anne/assessment.md)
- [Jack Detrick](/individual/jack/Individual%20Capstone%20Assessment.pdf)
- [Jonah Carter]()
- [Kevin Long](/individual/kevin/assessment.md)

## Professional Biographies
- [Anne Ning](/indiviudal/anne/bio.md)
- [Jack Detrick](/indiviudal/jack/bio.md)
- [Jonah Carter](/indiviudal/Jonah/JonahCarter%20-%20ProfesionalBio.md)
- [Kevin Long](/indiviudal/kevin/bio.md)

## Budget
As of 2025/11/24 we have not had any project related expenses.

## Appendix
So far this semester we have been focused on planning and the assignments for the course itself. We have all dedicated quite a bit of time to each of these activities. Much of the previous sections represent a lot of the work we have done on the assignments. In this section we will provide a brief overview/outline of the project status and the other work we have done that is not reflected in the required assignments.

### Research

Much of our time spent this semester has been focused on conducting the necessary research and preparation to position us well to complete the code and final design portion next semester.

We have been individually researching different components of the project within our own focus areas as well as making sure we are familiar and knowledgeable with the technologies and tech stack we will be utilizing.

In no specific order we have researched:

- Existing solutions  
  - Is there anything out there that does the same/similar things?  
  - Where do similar solutions fail?  
  - How can we learn from and improve upon them?  
- RFID and NFC  
  - How does each work?  
  - What compatibility exists for each on both Android and iOS?  
  - What compatibility exists *between* Android and iOS?  
  - How about support for passive vs. active RFID?  
  - How much information can NFC cards store?  
- QR Codes  
  - QR code generation.  
  - Embedding vCards in QR codes.  
- vCard format  
  - What fields exist?  
  - Will we have to extend it?  
- Tech stack  
  - Cross platform framework or native iOS and Android apps?  
  - Flutter vs. React Native?  
    - Does each have support for all the RFID and/or NFC access we will need?  
    - Which are people more familiar/comfortable with?  
  - None of us have a Mac. How can we build/compile an iOS app?  
- Backend  
  - Do we need a backend?  
  - What features would necessitate a backend?  
  - What technologies/functionalities would we need from a backend?  
  - Express vs. Flask  
  - Postgres  
  - Redis  
  - Costs associated with running a backend?

### Design

We have recently begun sketching designs for our frontend. Since we are so heavily focused on making the experience as seamless and easy for our users as possible we felt it was important to start thinking about how the user will interact with our app as soon as possible in the process. We now have a decent understanding of what is technically possible and thus before we get too bogged down/limited by how it makes the most technical sense to implement something we want to instead think about how it makes the most sense from a user’s perspective for the app to work and build and implement our functionality around this.

Obviously we are still limited by what is possible, but the benefit of thinking about this now in the process is that we are now aware of what is possible, but don’t yet have a definite model of the exact way it works. Thus we can still keep the focus on how the user would expect/want it to work and design based off of that, not with the burden of additional self-imposed technical limitations.

Everyone from the frontend team is currently working on their own individual sketches over the upcoming Thanksgiving break, and when we return we will convene to discuss and take the best of all our ideas and combine it into one intuitive and well thought out design.

### Meeting Notes

We have not been very good about keeping meeting minutes or extensive notes. Below is a summary of some of our most recent meeting(s).

Meeting Notes (Summarized):  
Initial Concept:  
Central server that “gatekeeps” all requests for information/sharing of contact info. Server/backend would consist of node.js and express.js with postgreSQL for the database engine.   
Initial testing/hello\_world example: [https://github.com/PlaceholderGroup/Placeholder\_Work/tree/Jack's-Branch/testing](https://github.com/PlaceholderGroup/Placeholder_Work/tree/Jack's-Branch/testing)

Meeting (11/24/2025):  
Reworking initial thoughts for the central server. We want to have each app hold its own database of contact info instead of relying on a single server/database.  
Issues with one server:

* If there’s difficulty connecting to the internet (such as a job fair or trade show) the app would lose its “snappiness” when sharing contact info. i.e. if someone has a slow connection they can’t access the contact info right away.  
* The server would have to limit how long a request would be able to exist before being accepted or denied (to prevent overloading).   
* Depending on how many requests are sent out at one time, throttling could occur. (bottlenecking)

Solutions provided by app-based storage:

* Since the connection is peer-to-peer, there won’t be any issues with receiving the contact info upon a share request.  
* There would be no inherent need to limit the number of requests as each exchange of information happens only at a point of contact.  
* No throttling as we would limit it to one exchange at a time. (can’t really tap more than one phone together at a time) 
