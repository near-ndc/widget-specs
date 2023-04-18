# Spec for a future "Nominate" widget
This community-driven spec is a collaborative community-led effort to create a functional specification for a widget to be developed. The goal is to bring clarity and alignment to the deliverables for developers to deliver a functional widget that meets the requirements.

# Overview
<!-- Describe the widget in one sentence. -->
The Nominate widget will probably be a fork of the "Kudos" and/or "Upvote" widgets on Near Social, and will allow users who have been validated as real humans to either nominate themselves or nominate other humans for upcoming elections. 

## Document Status 
<!-- What is the current status of this document? Inception / draft / community consultation / Locked: RFP ongoing / Locked: RFP awarded  -->
This document is currently in inception / early draft stage. We're looking for people who are interested in helping draft this spec.

## Other potential names for this widget:
<!-- Propose simple and clean names for the widget. -->
Nominate
Candidacy
NDC Candidates

## Challenge
<!-- List the challenge(s) being solved by this widget -->
1. The voting contract is currently being built to let the community to vote on who will be their elected representatives. This voting UI assumes that there is a list of condidates to vote on. This widget is intended to help originate the list of candidates.
2. There are not yet any defined criteria for who gets to be a candidate nor how the candidacy process will work. This widget, and the discussion we will have as a community while drafting the spec for the widget, will help clarify the conditions and will help guide future candidates through the process. This document makes no assumptions on criteria to qualify, other than that candidates should be verified human.
3. Does a person have to announce their candidacy on-chain by nominating themselves prior to others being able to nominate them? Or can anyone nominate anyone, regardless of if they have announced their candidacy. The design in this document assumes the latter, but adds a requirement to self-nominate before becoming a full blown candidate that users can vote into office. The reason for this is that we don't want to enable wasting a vote on someone who hasn't confirmed that they would be interesting in taking the seat if elected.
4. Feedback interface from the voting contract can be conteplated for a v2: 1) update candidate status from running to elected or defeated, 2) differentiate between incumbents and challengers.
5. Should the Nominate widget only support NDC's official Council Roles, or should any DAO be able to leverage the functionality? This becomes a challenge with the whitelist of admins being able to curate the Council Roles, while at the same time allowing the general public to create their own Council Roles without oversight.

## Scope
<!-- Define the scope and potential phases of the widget -->


## Requirements
<!-- What are the Minimal Viable Requirements (MV)  the widget should meet to be considered complete? -->
- only accounts which have been validated by i-am-humans are allowed to interact with the widget
- any human can nominate themselves, and can only nominate themselves to one position (house) at a time
- any human can nominate any other human (TBD: Does the nominee have to already be self-nominated first)
- differentiate between incumbents and challengers
- support the three NDC houses by default, but also support public candidacy and election to any other DAO

## Phases
<!-- Do the project have multiple phases? Identify a high-level summary of each phase. -->
- First design and build the predecessor widgets: Kudos and/or Upvote. Becase giving a nomination to someone is largely similar (technically) to giving them Kudos or to upvoting their self-nomination.
- Fork the predecessors and rename from Kudos / Upvote to Nominate
  - Add the human-gating functionality. Only i-am-human-verified accounts should be able to interact with this widget.
  - Ensure that the widget can produce a harmonized list of candidates for each NDC vote 
- Add any other features to support the nomination process, such as
  - Support for candidate to introduce themselves and their platform
  - Links to their socials and contact info
  - Meet the candidate: Upcoming AMA events and recordings of past events

# Use Cases
<!-- Identify and list the collectives that will use this widget and what each one will specifically do. -->
- DAO Admins: Will open up election slots for candidates to nominate themselves or others towards. E.g. House of Merit will open up 10 new slots for election within a month, and specify that only candidates with three nominations or more will be eligible to be voted upon.
- NDC Candidates: Will nominate themselves to one of three default NDC slot, and will enter information about themselves and their campaign platform.
- Candidates to other DAOs: Will nominate themselves to a non-NDC DAO council position, and will enter information about themselves and their campaign platform.
- Friends of candidates: Will nominate their preferred Candidates to a slot, or give their support to a self-nominated candidate.
- Voters: Will vote on those candidates that have passed the minimum threshold of Nominations

## Actors
<!-- List all collections that will use the widget. -->
Admins
- A user is an admin if they have been added to the admin whitelist by another admin
- Admins can create and modify Council Roles, to which people can then be nominated
- Admins can add or remove other fellow admins

Non-human Users
- A user is anyone with acess to near.social that is either not logged in, or is logged in but has not been verified by i-am-human
- These actors have view-only access to the widget, they have no ability to nominate or otherwise affect the state

Nominators
- A Nominator is any user who is logged into near.social and has been verified by i-am-human
- Nominators have access to the base feature of the app: They can nominate themselves or others, and they can withdraw their nominations.

Nominees
- Nominees are a subset of nominators who have also received a nomination
- Nominees have the added ability of viewing the nominations that they have received

## Actions
<!-- List the actions each collective will take individually. -->
Common actions within this widget include
- Nominate someone (or self)
- Withdraw nomination
- Create or Deprecate Council Role
- Pause or Unpause Council Role
- Modify Council Role
- Increment the Congress Counter for a Council Role

## Actor/Action Matrix
<!-- Describe which action is done by which actors. Feel free to use a table format or provide your own graphics. A "swimlane process chart" often works well here. -->
REPLACE THIS TEXT

|                                         | Admins   | Nominators | Nominees | Non-human Users |
| -------                                 | -------- | -------- | -------- | -------- |
| Nominate someone                        |  Yes        |  Yes        |  Yes        |  No         |
| Withdraw nomination                     |  Yes        |  Yes        |  Yes        |  No         |
| Create or Deprecate Council Role        |  Yes        |  No         |  No         |  No         |
| Pause or Unpause Council Role           |  Yes        |  No         |  No         |  No         |
| Modify Council Role                     |  Yes        |  No         |  No         |  No         |
| Increment Congress Counter              |  Yes        |  No         |  No         |  No         |



# Tech Spec
## Functions
<!-- What functions and functionalities should the widget have -->
REPLACE THIS TEXT

## Process Flows
<!-- Describe the process flows -->
REPLACE THIS TEXT

## Screens
<!-- Describe the layout and content of the various screens within the widget -->
The Nomination widget will have three screens. Two of these will be visible to all users, while the admin screen will only be available to whitelisted users.

### Admin Screen
Any account that's been whitelisted will have access to the Admin screen, which will have the following main functions:

1. Create new Council Role 
   - For example when a new Grassroots DAO has been recognized, they may want to create a Council Role for their DAO, to which people can be nominated.
   - When creating a new Council Role there are two input fields required: 1) Council Role name (string), and 2) Minimum required nominations (integer), which defaults to 3 but can be changed
   - The Congress Counter (integer) will default to 1 for a new Council Role
2. Modify a role: Change minimum required count of nominations for the Council Role
3. Modify a role: Change name of the Council Role
4. Increment the Congress Counter for the Council Role
   - Immediately after an election to one Congress has been made, then the Congress Counter should be incremented
   - The previous Congress becomes locked. All nominations for that Congress are archived
   - A new Congress is opened up, with a blank slate (there are zero nominations yet for the new Congress)
5. Pause / Unpause / Deprecate the Council Role
   - Once an election have been held for a Congress, there may be a need to wait for a while until opening nominations for the next Congress. 
   - When a DAO ceases to exist, then the corresponding Council Role should be deprecated
6. Add new admins
   - Only accounts that have been verified by i-am-human are allowed to be added
7. Remove a current admin
   - If there is only one admin remaining then the Remove Admin function should be disabled (we need at least one admin)

### Nomination Screen
This is the default view when first opening the app. Users can nominate themselves or other users to the various currently open Council Roles. A Council Role is open after it has been created and it's status is not Paused nor Deprecated. 

Requirements:
- Only accounts that have been verified by i-am-human can nominate other accounts
- Only accounts that have been verified by i-am-human and can be nominated

This screen will show a nomination dialog with three key inputs
  - Select who to nominate
  - Select which role I'm nominating this person to
    - Note: When listing the Council Roles, only currently active roles should be shown
  - Description of why I'm nominating this person

After pressing nominate then the app will check that the nominated account is indeed verified by i-am-human before saving the nomination.

The screen also shows a listing of all accounts that the logged in user has nominated to the various Council Roles
   - Option to withdraw nominations if the Council Role is still open
   - This listing includes both current and past Council Roles, where an account might have been nominated several times, either to different roles and/or to different Congress Counters

### Nominee Screen
This screen is for the user to check what roles they have been nominated to, and to analyze the current state of nominations across all roles.

The first list on this screen shows all nominations that the logged in user has received for currently open roles.

The second list on this screen shows all nominations for all roles
  - prepopulated with only currently acive roles
  - allows the user to filter the list by clicking on a role to see only active nominations that pertain to that role
  - once a role has been selected, the user can also select any of the previous Congress Counters for that role, to see the archived nominations.

## Dependent Widgets
<!-- Does the widget interact with other widgets? -->

### Inbound Dependencies
This widget depends on the registry contract (registry.i-am-human.near) within the i-am-human ecosystem of SBTs. Prior to enabling each nomination action we need to ensure that the logged in user account is a verified human account. And prior to finalizeing a nomination we need to ensure that the nominee is also a verified human account.

### Outbound Dependencies
The NDC Voting contract / widget in return depends on this Nomination widget. The list of electable candidates shown in the Voting widget will be generated by querying this Nomination widget. All accounts that have equal to or more nominations than the required minimum for a role, and for which the nominee has also self-nominated to the same role, will be added to the list of electable candidates.

# Audit
<!-- Identify if this widget needs an audit. Does it store sensitive information, transfer tokens, or have a middleware layer? Consult the Security Workgroup if needed. -->
REPLACE THIS TEXT
