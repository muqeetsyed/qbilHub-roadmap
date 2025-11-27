# Project Roadmap (One-Page Overview)

## STEP 1 — Initial R&D
- **THE GAME PLAN**
- The initial R&D will include the feasibility study of the Qbil Hub. Before going technical, we will need to check the main requirements. What the stakeholders are expecting and if all the requirements are clear. That will start with a simple POC for visualization. The POC is entirely to gain a gist of the main requirements and to make sure developers and stakeholders are aligned towards a single goal. Also we should make sure the POC takes minimum possible time. The POC will be a part of R&D for a change as it will help us to actually how the stuff will paint out.
- In parallel the heart of Qbil hub will be explored. The heart being the mapping of data across customers. The nature of data is very much peculiar. The customers dont use the same terminology for indetifying main root data elements. One of the main challenges is the product map. The products are identified across different customer pairs in a very different way. For example betweem FF and MWH we tracked some contracts and we came across the fact that they track orders/products using unloading reference on orderlines. These and other customer specific trends need to be identified and taken into account.
- The R&D also needs to take into account other root data elements. This includes packaging, pallet types, payment conditions, delivery conditions and rest.
- The R&D is very extensive as we have to make sure we check the way trade is done across our customers.

- **TECHNIQUES TO BE UTILIZED**
- The techniques that we can explore for this include [MUQEET FILL THIS IN PLEASE]

- **TIME ESTIMATES**
- For the R&D of whole project the estimate will be round about 350 - 400 hours.
- The POC implementation will be a 2 week job - ~10 days
- For the rest of process the time estimation is in the individual phases below. Please note all the estimations are subject to change on the basis of the R&D done, especially for the mapping step.


## Step 2 — Documentation and R&D result publlishing
- This is ofcourse a parallel process, that will run alongside with the R&D. The whole of the R&D will be documented to make sure we can revisit any decision/step and iterate/improve accordingly.
- Ours is an agile process, so the R&D wont be a black box process. There will be regular meetings with Kashif to make sure we keep him aligned with the progress and make timely alterations if necessary.
- **Techniques** - All the R&D related documents will either go to the ADR section or will be records accordingly in the qbil hub code base, so that everyone can check and reflect on it.
- **Time frame** - This will be a one week process. To publish the R&D results and have thorough discussions with the core team and the management team to get the main results from the R&D to lay the initial foundation of the HUB.

## Step 3 — Technical descisions
- This step will be entirely dedicated to the technical decisions and discussions. After the R&D when we are wll aware of what we need, next step will be te decide tools, technologies and techniques to achieve this. The technical decisions will be taken keeping all the phases in mind and a technical map will be prepared to make sure we see all the possible paths and challenges that lay before us for implementing the HUB and choose the technologies accordingly.
- **Techniques** - Some of the initial technologies/techniques that we had listed as below. [MUQEET FILL THIS IN PLEASE]
- **Time frame** - This will be a two week process. This step could include exploring some technologies to check if it fits in for our needs and this can increase the frame by a day or two.

## Step 4 - Cross team requirement check
- One we have decided the technologies, it will be clear if we need any assistance from other teams/team members.
- Depending on the need we can communicate with the respective teams and make plans accordingly.
- This phase will also include creating initial technical document to present to other teams to make sure they are in line with the HUB.
- **Time frame** - This will be a one week process.

## Step 5 - Start of the fight
- Once done with all the non-coding things, the implementation will begin. Lets walk through this phase by phase

#### Phase 1 — Admin Hub Connectivity & Basic Document Transmission
- **What we understood about the phase** - This phase is centered around email interface in qbil trade. In this phase following implementations are to be carried out
    1. An admin panel will be created in QT from where admin from one tenant will send a connection request to another tenant. The admin of the other tenant will use the same admin panel from QT to accept/reject the request. Once accepted, the connection will be set up and now documents can be exchanged between tenants using the existing email UI of QT. If the request is rejected, the sender admin will be notified in the admin panel about the rejection.
    2. The document sending and reception capabilities will be implemented. The documents will only be sent and received by the admins. In additions they can view the PDF previews of the documents sent/received.
- **R&D:** Basic requirement gathering for the phase. The R&D will be done already, this phase is just to get a gist and gather all the stuff up for the phase. This will take a week.
- **Discussions and planning:** Non technical discussions and plan out the tickets that  will be created for implemented this thing and plan the sprint break up accordingly. This will take about a week
- **Prototype:** A working prototype of basic admin UI for hub setup + simulated transmission. The prototype will be kept simple and will be discussed with Arshan and Kashif to finalize a UI and take fine care of the UX. This will be a 2-3 week process as there can be iterations. The prototype creation is an important step to be able to know what we are going to get at the end of the phase and to figure out any UI/UX level constraints that can arise over time and delay the actual implementation process.
- **Technical planning** - Planning out the main work flow technically. The technical discussions will ofcourse be already taken and finalized, but there is still some stuff that will be done here. This will include inner details of implementation and will be done within the team exclusively. External help will be taken as and when needed. This will be a one week process.
- **Implementation:** The main game finally begins where we will be implementing the phase. Small tickets will be created to make sure the implementation is tested along with the development. The first phase will take some time to setup the initial boilerplate. This can cause the time needed for this phase to be more that the other ones. The time estimate for this will heavily rely on the technology selected and the architecture chosen. But from the overview it looks like that a rough estimate of 4-5 months will be needed for the first phase. Please note the implementation will also include writing tests at each and every step and testing each path of execution properly.
- **Refinement:** Code cleanup, reliability improvements, security hardening . This will be a final step in the implementation and can take a couple of weeks.
- **Time frame** - A total of about 6-7 months will be taken for implementing the phase 1 fully.


#### Phase 2 — User Notifications & Document Reception
- **What we understood about the phase** - In this phase a user permission system will be setup where an admin can control who can access the HUB and what will be the access levels. Also document transmission will now be between users too where the user with document send capabilities will be ale to specify the receivers for the documents. Depending upon the receivers chosen a notification system will be setup to notify users about document received and other activities performed on the document. The notifications will make sure the sender and receiver will be informed about any change to the document on either side. Also a login system needs to be setup in this phase.
- **R&D:** Same as phase 1.
- **Discussions and planning:** Same as phase 1
- **Prototype:** Same as phase 1
- **Technical planning** - Same as phase 1
- **Implementation:** Small tickets will be created to make sure the implementation is tested along with the development. The time estimate for this will heavily rely on the technology selected and the architecture chosen. But from the overview it looks like that a rough estimate of 5-6 months will be needed for this phase. Please note the implementation will also include writing tests at each and every step and testing each path of execution properly.
- **Refinement:** Code cleanup, reliability improvements, security hardening . This will be a final step in the implementation and can take a one month.
- **Time frame** - A total of about 7-8 months will be taken for implementing the phase 2 fully. The time frame is more as this phase will take the code work outside of Qbil Trade. In short, this phase will mark the start of the UIs of Qbil Hub. The Hub inbox will also take shape in this phase.


## Phase 3 — Intelligent Mapping System (Learning Enabled)
- **What we understood about the phase** - Once the document is received, Qbil Hub will match the details from the sender's contract and gather matching data from the receiver's side and present a side by side split view to the user and also highlight unmatched fields. At this step the user will choose/enter the unmatched values and we will store the values to use for future matching. In addition if any matched data is changed by the user, the change should also be saved and if repeated by the user for more than let's say 3 times, then the system should learn and automatically update the mapping and use the same value in future.
- **R&D:** Same as phase 1. But this can take a couple of weeks.
- **Discussions and planning:** Same as phase 1
- **Prototype:** Same as phase 1.
- **Technical planning** - Same as phase 1
- **Implementation:** The main game finally begins where we will be implementing the phase. Small tickets will be created to make sure the implementation is tested along with the development. The first phase will take some tiem to setup the initial boilerplate. This can cause the time needed for this phase to be more that the other ones. The time estimate for this will heavily rely on the technology selected and the architecture chosen. But from the overview it looks like that a rough estimate of 7-8 months will be needed for the first phase. Please note the implementation will also include writing tests at each and every step and testing each path of execution properly.
- **Refinement:** Same as phase 2.
- **Time frame** - A total of about 8-9 months will be taken for implementing the phase 3 fully.----------------------------------->>>>>>

## Phase 4 — Algorithm Refinement & Advanced Features
- **What we understood about the phase** - Let users explore the Hub and provide feedback. In addition to implementing user feedback, we will also need to perfect the matching algo and try to improve and test it on some real world data sets. This has to be an iterative process.
- **Discussions and planning:** Non technical discussions and plan out the tickets that  will be created for implemented this thing and plan the sprint break up accordingly. Time taken will depend om the feedback cycle and amount of work needed
- **Technical planning** - Planning out the main work flow technically. The technical discussions will ofcourse be already taken and finalized, but there is still some stuff that will be done here. This will include inner details of implementation and will be done within the team exclusively. External help will be taken as and when needed. Time taken will depend om the feedback cycle and amount of work needed
- **Implementation:** The main game finally begins where we will be implementing the phase. Small tickets will be created to make sure the implementation is tested along with the development. The time estimate for this will heavily rely on the technology selected and the architecture chosen. But from the overview it looks like that a rough estimate of 2-3 months will be needed for the HUB tp start working smoothly and meet up our and user expectations. Please note the implementation will also include writing tests at each and every step and testing each path of execution properly.
- **Refinement:** Code cleanup, reliability improvements, security hardening.
- **Time frame** - Time taken for this phase will depend entirely on the amount of user feedback and our own improvements. Not feasible to get an estimation for this phase.
