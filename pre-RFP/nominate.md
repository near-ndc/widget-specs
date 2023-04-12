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
2. There are not yet any defined criteria for who gets to be a candidate nor how the candidacy process will work. This widget, and the discussion we will have as a community while drafting the spec for the widget, will help clarify the conditions and will help guide future candidates through the process.

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
REPLACE THIS TEXT

## Actions
<!-- List the actions each collective will take individually. -->
REPLACE THIS TEXT

## Actor/Action Matrix
<!-- Describe which action is done by which actors. Feel free to use a table format or provide your own graphics. A "swimlane process chart" often works well here. -->
REPLACE THIS TEXT

|         | Action 1 | Action 2 | Action 3 | action 4 |
| ------- | -------- | -------- | -------- | -------- |
| Actor 1 |          |          |          |          |
| Actor 2 |          |          |          |          |
| Actor 3 |          |          |          |          |
| Actor 4 |          |          |          |          |



# Tech Spec
## Functions
<!-- What functions and functionalities should the widget have -->
REPLACE THIS TEXT

## Process Flows
<!-- Describe the process flows -->
REPLACE THIS TEXT

## Screens
<!-- Describe the layout and content of the various screens within the widget -->
REPLACE THIS TEXT

## Dependent Widgets
<!-- Does the widget interact with other widgets? -->
REPLACE THIS TEXT

# Audit
<!-- Identify if this widget needs an audit. Does it store sensitive information, transfer tokens, or have a middleware layer? Consult the Security Workgroup if needed. -->
REPLACE THIS TEXT
