# Spec for a future "Regional Communities" widget
This community-driven spec is a collaborative community-led effort to create a functional specification for a widget to be developed. The goal is to bring clarity and alignment to the deliverables for developers to deliver a functional widget that meets the requirements.

# Overview
<!-- Describe the widget in one sentence. -->
This widget will help users find, join and interact with communities that are in their region and aligned with their interest. It also provides a natural way of growing all the regional communities within NEAR.

## Document Status 
<!-- What is the current status of this document? Inception / draft / community consultation / Locked: RFP ongoing / Locked: RFP awarded  -->
This document is a very early draft. Looking for community input to make it a better and more fully documented draft.

## Other potential names for this widget:
<!-- Propose simple and clean names for the widget. -->
My Communities
My Community
Regional Community
Regional Communities
Community Finder

## Challenge
<!-- List the challenge(s) being solved by this widget -->
It's currently really easy to create a new community on near.social. All you have to do is create a new account with your community name and start promoing it. But this unstructured approach comes with a lot of challenges:
- If you want to start a new community you have to start from scratch, and you have to build your own membership base from scratch.
- If you're simply looking for a community to join, it's not easy to find one in the unstrucctured mess
- There is competition by default". If two or more communities were formed with the same or similar scope, then they are bound to try and attract member following from the same community base, potential members who werent interested in the choice from the beginning but just wanted to find their one "home"

Most communities form around some intersection of geography, language and vertical constellation / interest. But they are not getting any help in finding their place in these dimensions. Similarly, new users looking for a community to join have a hard time finding the right community in the right intersection.

There is no natural evoution provided for communities that grow "too large" or too diverse. If they want to split then the only option is to create a new  sibling- or child-community, again from scratch. Similarly, there is no natural way of merging two communities without having to agree to delete one (with all it's history) and ask the members each to manually move to the new community.

## Scope
<!-- Define the scope and potential phases of the widget -->
All geographies
All languages
All verticals
Users interested in joining, forming or managing communities of likeminded

Typical resons to come together in a community:
- Networking
- Learning from each other, discussing
- Support and help each other
- Find new friends, build meaningful relationship

What is NOT within the scope of regional communities? Groups that are not bulding lasting relationships, groups where the only purpose is to facilitate one-time or temporary transactions.
- Buy and sell groups
- Job listing / job search
- Gig economy

## Requirements
<!-- What are the Minimal Viable Requirements (MV)  the widget should meet to be considered complete? -->
- Built on BOS / Alpha / Near.social
- Can have a single admin owner or a DAO as an owner
- Members can post messages within community
- Messages posted in communities that I follow will show up in my stream
- Supports all three dimensions
   - Geography as a hierarchy (each community has one geography, and has a parent with a higher level geography)
   - Language as a flat list, single-select
   - Constealltion as tags, multi-select

## Phases
<!-- Do the project have multiple phases? Identify a high-level summary of each phase. -->
REPLACE THIS TEXT

# Use Cases
<!-- Identify and list the collectives that will use this widget and what each one will specifically do. -->

## Actors
<!-- List all collections that will use the widget. -->
REPLACE THIS TEXT

## Actions
<!-- List the actions each collective will take individually. -->

### Find and Join a Community
Finding a community aligned with my interests should be very easy. It's a core concept of this widget and serves to get people into open and collaborative communities rather than creating competing factions.

Searching for communities should be possible through a few different ways
- Search by map. Zoom into a map and update the list of available communities accordingly
- Seach-as-you-type.
   - Search by fuzzy search of geographies. Start typing in a city, country or region and all available options are shown. 
   - Search by fuzzy search of constellations. Start typing in a constellation and all available options are shown.
- Select you language, which updates the available communities. Default language is English.
- Any combination of the above will further narrow the search


### Approve a new Community member
Approvind a new community member could be as simple as a "follow back" by the owner of the community or someone who has been given the keys to control the community account. 

It is recommended that only human-verified accounts be allowed to become members, as a minimum requirement.

A drawback of this approach is that there is no vote. Any single admin can follow or unfollow, which may be too arbitrary for some communities. Another drawback is that the "follow" feature would no longer be available to use for its originally intended purpose. A more structured approach to membership may have to be contemplated. Optins include:
- user follows the Community and automatically becomes a member as long as some criteria are filled (e.g. is human verified and accepts the code of conduct) => Preferred
- user applies for membership, followed by a majority vote to approve the application
- membership is open to anyone without approval
- membership is open to anyone, with the restriction that they can be a full member of one and only one community

This author recommends a combination, whereby there are four types of membership:
1. Home Membership - each user can define their one and only "home" membership = the community that is most closely aligned with them. This can be done without approval from the community
2. Hangaroud Membership - any user can be a hangaround. This feature is similar to a standard "follow" and should be the default membership for most communities.
3. Core Member - the user has been approved in some way (by community vote or admin vote) to be a core member of the community. This option should not be a default option, but could be a possibility to enable for some communities that desire this option.
4. Admin Member - the user has admin rights for the group

It is this authors recommendation that commuinties be open for anyone to join and that applications are "accepted by default". If limitations are desired then it's better to use the "silence the member" feature than to go to "accepted pending approval" which signals a closed or restricted society.

### Split a Community
Instead of creating a Community from scratch, splitting an existing Community into two should be the default way of creating new communities. This is a core feature of the Community widget design.

When splitting a community, the following choices should be taken:
- Along which dimension do you want the split to occur: Geography, Language, or Constellation?
  - If splitting along Geography then ask if it's a sibling-split of child-split. Example of the former: Sweden splits into Sweden + Norway. Example of the latter: Sweden splits into Sweden + Stockholm
  - If splitting along Language then simply ask which other language the new community should serve
  - If splitting along Constellations and there is already a constellation picked, then simply ask what constellation the new Community should serve and it will be a sibling. If splitting along Constellations and there was no prior constellation picked, then ask which Constellations the new Community wishes to serve and it will be a child.
  - The user requesting the split will also be the first leader of the new community by default

After splitting the community, then each member should be given a choice as to which of the resulting communities they wish to belong to, or if they wish to be a member of both.

### Merge two Communities
We don't anticipate this to happen often, but it could be the case that two communities have shrinking membership and would like to merge to increase the total membership in one Community.

A merge proposal should be approved by majority vote in both communities before it is allowed to happen.

It's not easy to design rules for how the merge should be executed, based on the complexity of possible permutations of the pre-merge Communities. It seems plausible that merge power should not be given to regular users but could be given as an admin power to a dev / superuser. The alternative would be that merging not be supported, in which case the community will manually have to move from and abandon one community in favor of the other.

### Ban a user from a Community
Banning is a strong power and should be used very restrictively. We suggest milder and more human forms of restricting users that are not following the code of conduct for a community. 
- Issue a warning for breach of code of conduct
- Temporarily silence the user for a day
- Temporarily silence the user for a week
- Silence the user until un-silenced (perhaps after taking some corrective action)
- Banning the user with chance of reapplying
- Banning the user with chance of reapplying (permanently)

It is this author's opinion that silencing the user is a much preferred method over banning them. Silencing allows the user to keep following the activitiy of the community and still feel like they belong there. It creates less animosity and makes the world a nicer place. Consider not implementing the banning feature.

These measures can be designed such that each increasing level of banning must be preceeded by the milder forms before it can be implemented. E.g. must silence the user for a day before can silence them for a week.

### Manage a Community
Communities should be open and welcoming, not closed for elite members only. We should design them such that members have as much powers as possible, and that admins are given as few god-like options as possible.

One way to achieve decentralized leadership is to give admin powers to the community by majority vote, where any member can propose a vote and any member can vote on them, and where the proposal is automatically executed following a majority vote. 
- Consider making it a requirement that communities are owned and managed by an Astro-DAO with a minimum of 5 council members, rather than an individual owner.
- Consider forking the relevant parts of the Sputnik DAO codebase into this widget, to manage the Community by vote.

### Create a new Community
The widget design should inherently discourage users from creating new communities. Instead, users should be encouraged to...
- Find an existing community to join that fits their interest
- Find an existing community with approximate match, and suggest them to increase their scope to include their interest
- Find an existing community to join, and suggest they split out a child- or sibling communit that fits their interest

By taking the above actions, the following benefits would be realized:
- We discourage creating overlapping communities unneccessarily
- The new communities come with a default following and get a default parent or sibling
- Less need to start from scratch finding members, as a seed membership would come along from the preceeding community
- Create an audit trail of community growth
- Natural evolution and growth of the various dimeensions (geography, vertical, etc)

If the developers decide anyways to give an option to create a new community from scratch, then the following should be required actions:
- Select a geographical area that the community covers, selecting from a list of already existing areas, preferably from a hierarchy of existing areas (global-continent-country-region-municipality-city)
- Select which one language the community will be using
- Select which vertical constellation the community will be focused on (multiselect, optional). If no constellation is selected then the geographical area covered should be very small (i.e. country or below)
- The creator of the community becomes the default Council member by default

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
