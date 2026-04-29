---
title: Domain separation in Live Feed
description: This is an overview of domain separation and Live Feed. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Live Feed
classification: live-feed
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Live Feed reference, Live Feed Core UI, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Domain separation in Live Feed

This is an overview of domain separation and Live Feed. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Overview

**Support: Level 2**



Parent and child domains define the Live Feed content that can be viewed and shared with other users.

-   A user in a parent domain can see users and content within their domain and within all child domains that are lower in the domain hierarchy.
-   A user in a child domain can see users and content within their domain but cannot see the parent domain or other child domains at the same level in the domain hierarchy.

## Enable domain separation for Live Feed

Domain separation for the Live Feed application is available starting with the Eureka release. For users upgrading to Eureka, a sys\_domain column is added to existing live feed-related database tables. For existing database records, the value of the sys\_domain field is set to empty \(global\). This allows the domain separation feature to work with existing Live Feed records.

## Show or hide the Live Feed application for a domain

The administrator can Live Feed visibility for a domain. This includes:

-   Displaying Live Feed in the application navigator.
-   Following a document feed for a record.
-   Viewing Live Feed from a record.

## Use Live Feed with domain separation

All of the Live Feed features are available to users within a domain and work the same way, with some exceptions to visibility.

-   Posting and sharing content
    -   Users in a child domain can interact with other users in the same domain. This includes posting and replying to messages, deleting messages, attaching files and links, and rating content.
    -   Users in a parent domain can interact with other users in the same domain and with users in any child domains. Messages that are added to child threads by parent users are given the visibility of the child domain, not the parent domain.
-   Viewing content
    -   Users in a child domain can view content that resides within their domain. This includes filtering by feed, sorting, searching, and viewing older messages.
    -   Users in a parent domain can view content that resides within their domain and within any child domains.
    -   My Feed shows messages, teams, and hashtags based on the user's domain. Showing another user's feed only shows posts visible in the current user's domain.
-   Using hashtags
    -   Hashtags are separated by domain. Users in a child domain can use all of the hashtag functions within their domain. This includes tagging messages, viewing available hashtags, changing hashtag names, and searching and filtering by hashtag.
    -   Users in a parent domain can use all of the hashtag functions within their domain and can see hashtags in any child domains.
-   Using teams
    -   Teams are separated across domains. Users in a child domain can join and follow teams within their domain, and can invite other users within their domain to join teams.
    -   Users in a parent domain can join and follow teams that belong to their domain or to any child domains.
-   Exceptions to teams
    -   New teams are created in the user's domain. However, if the team has a record associated with it, the team is created in record's domain.
    -   New threads in an existing team are created in the domain of the existing team.
    -   When a user is creating a new team from a document, if the document domain is not empty or global, the team domain needs to be changed to be the document's domain.
    -   For a document-generated team, when the domain of the document changes, the domain of all related Live Feed records changes as well.
-   Subscribing to email notifications

    Users can subscribe to email notifications from users and teams within their domain only.


**Parent Topic:**[Live Feed reference](live-feed-reference.md)

**Related topics**  


[Live Feed security and table access](r_LiveFeedTableAccessRules.md)

[Limit Live Feed access by role](../task/t_LimitLiveFeedAccessByRole.md)

[Manage Live Feed message content](../task/t_ManageLiveFeedMessageContent.md)

[Live Feed team security](r_LiveFeedTeamSecurity.md)

[Restrict hashtag renaming](r_RestrictHashtagRenaming.md)

[Domain separation](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=australia&pubname=australia-platform-security&ft:locale=en-US)

