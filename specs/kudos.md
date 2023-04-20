# Spec for a future "Kudos" widget
This community-driven spec is a collaborative community-led effort to create a functional specification for a widget to be developed. The goal is to bring clarity and alignment to the deliverables for developers to deliver a functional widget that meets the requirements.

# Overview
<!-- Describe the widget in one sentence. -->
This widget will allow any verified human to give any NEARSocial/Discovery account a Kudo.

## Document Status 
<!-- What is the current status of this document? Inception / draft / community consultation / Locked: RFP ongoing / Locked: RFP awarded  -->
This document is currently in "Locked" status. A prototype exists and @starpause will finalize the spec and ux design.

## Other potential names for this widget:
- High Five
- Props

## Challenge
<!-- List the challenge(s) being solved by this widget -->
The goal of this widget is to foster and improve recognition and celebrations of individuals, nodes, projects, workgroups or collectives for their contribution to NEAR. 

This will server as a fundemental MVP for Reputation and Badges and create a general widget that can be forked and used for many use cases

## Scope
<!-- Define the scope and potential phases of the widget -->
Finalize the features and UX for launch, complete integrations to IamHuman and SBT standard.

## Requirements
<!-- What are the Minimal Viable Requirements (MV)  the widget should meet to be considered complete? -->
- Tag any BOS/NEARSocial/Discovery account
- Notify the account of the Kudo via the Notifications API
- Upvote a Kudo
- Comment on a Kudo
- Show all comments
- Integration with IamHuman
- Send account SBT Badge for each Kudo

## Phases
<!-- Do the project have multiple phases? Identify a high-level summary of each phase. -->
- Finalize UX design add a table view
- Integrate with IamHuman
- Integrate with SBT Standard

# Use Cases
<!-- Identify and list the collectives that will use this widget and what each one will specifically do. -->
Any account registered on BOS/NEARSocial/Discovery will be able to use the widget to send Kudos

## Actors
<!-- List all collections that will use the widget. -->
Individual Accounts

## Actions
<!-- List the actions each collective will take individually. -->
- Send Kudo
- UpVote
- Comment
- Share

## Actor/Action Matrix
<!-- Describe which action is done by which actors. Feel free to use a table format or provide your own graphics. A "swimlane process chart" often works well here. -->

|         | Action 1  | Action 2 | Action 3 | action 4 |
| ------- | --------  | -------- | -------- | -------- |
| Actor 1 | Send Kudo | Upvote   | Comment  |  Share   |




# Tech Spec
## Functions
<!-- What functions and functionalities should the widget have -->
- isHuman
- mintSBT

## Process Flows
<!-- Describe the process flows -->
REPLACE THIS TEXT

## Screens
<!-- Describe the layout and content of the various screens within the widget -->
REPLACE THIS TEXT

## Dependent Widgets
<!-- Does the widget interact with other widgets? -->
##### Main
[Kudos.Styles](https://near.social/#/neardigitalcollective.near/widget/Kudos.Styles)

[Common.Compose](https://near.social/#/neardigitalcollective.near/widget/Common.Compose)
[Kudos](https://near.social/#/neardigitalcollective.near/widget/Kudos)
[kudoBox](https://near.social/#/neardigitalcollective.near/widget/kudoBox)
[FollowButton](https://near.social/#/neardigitalcollective.near/widget/FollowButton)
[MainPage.Post.Header](https://near.social/#/neardigitalcollective.near/widget/MainPage.Post.Header)
[MainPage.Post](https://near.social/#/neardigitalcollective.near/widget/MainPage.Post)
[showCommentsButton](https://near.social/#/neardigitalcollective.near/widget/showCommentsButton)

# Audit
<!-- Identify if this widget needs an audit. Does it store sensitive information, transfer tokens, or have a middleware layer? Consult the Security Workgroup if needed. -->

