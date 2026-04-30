---
title: YouTube Spoke
description: Manage your videos, channels, subscriptions, and playlists in YouTube account, and access analytics and statistics from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# YouTube Spoke

Manage your videos, channels, subscriptions, and playlists in YouTube account, and access analytics and statistics from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

YouTube spoke v1.0.5 is the latest version.

## Supported versions

This spoke was built for these YouTube versions, but may be compatible with later versions.

-   Reporting API version v1
-   Data API version v3
-   Analytics API version v2

## YouTube spoke requirements

The YouTube spoke requires a custom app that you create in Google Cloud Platform.

## Spoke dependencies

If you’re having trouble installing the app, confirm that these dependent plugins are installed:

-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The YouTube spoke provides actions to automate YouTube tasks when events occur in the ServiceNow AI Platform. Available actions include:

<table id="table_u1p_kh2_hfb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="6">

Analytics

</td><td>

Audience Retention Statistics

</td><td>

Retrieves information about the audience retention statistics.

</td></tr><tr><td>

Basic Statistics

</td><td>

Retrieves information about the basic statistics.

</td></tr><tr><td>

Demographics

</td><td>

Retrieves information about the demographics. That is, details about the age, gender, and geographical location of your audience.

</td></tr><tr><td>

Device/OS Statistics

</td><td>

Retrieves information about the devices from which your audience accesses your content.

</td></tr><tr><td>

Get Country Codes \(Metadata\)

</td><td>

Retrieves details of countries and their ISO codes.**Note:** This action is a metadata action.

</td></tr><tr><td>

Traffic Source Statistics

</td><td>

Retrieves information about the various traffic sources.

</td></tr><tr><td rowspan="2">

Captions

</td><td>

Delete Caption

</td><td>

Deletes captions on a video.

</td></tr><tr><td>

Look up Captions

</td><td>

Retrieves information about the captions on a video.

</td></tr><tr><td rowspan="4">

Comments

</td><td>

Delete Comment

</td><td>

Delete the specified comment on a video.

</td></tr><tr><td>

Look up Comments

</td><td>

Retrieves details about the top-level comments in a comment thread.

</td></tr><tr><td>

Post Comment

</td><td>

Posts a top-level comment on a video.

</td></tr><tr><td>

Reply to Comment

</td><td>

Posts a reply to a top-level comment on a video.

</td></tr><tr><td rowspan="6">

Groups

</td><td>

Create Groups

</td><td>

Creates a group for videos, channels, or playlists.

</td></tr><tr><td>

Delete Group

</td><td>

Deletes the specified group.

</td></tr><tr><td>

Delete Group Item

</td><td>

Deletes the specified group item.

</td></tr><tr><td>

Insert Item into Group

</td><td>

Inserts an item in the specified group.

</td></tr><tr><td>

Look up Group-Items

</td><td>

Retrieves information about all items in a group.

</td></tr><tr><td>

Look up Groups

</td><td>

Retrieves information about the specified groups.

</td></tr><tr><td rowspan="4">

Playlist

</td><td>

Create Playlist

</td><td>

Creates a playlist in your YouTube account.

</td></tr><tr><td>

Delete Playlist

</td><td>

Deletes a playlist from your YouTube account.

</td></tr><tr><td>

Delete Playlist Item

</td><td>

Deletes the specified playlist item.

</td></tr><tr><td>

Insert into Playlist

</td><td>

Inserts an item in the specified playlist.

</td></tr><tr><td rowspan="4">

Reports

</td><td>

Create Report Job

</td><td>

Creates a report job in YouTube account. YouTube generates the requested report within 24 hours.

</td></tr><tr><td>

Get Report Types Choice \(Metadata\)

</td><td>

Retrieves information about the Report Types list.

</td></tr><tr><td>

Look up Reports

</td><td>

Retrieves information about the reports generated for a job.

</td></tr><tr><td>

View Report

</td><td>

Retrieves data in a report in CSV format.

</td></tr><tr><td rowspan="3">

Subscriptions

</td><td>

Look up Subscriptions

</td><td>

Retrieves information about the specified subscriptions.

</td></tr><tr><td>

Subscribe Channel

</td><td>

Subscribes to the required channel.

</td></tr><tr><td>

Unsubscribe Channel

</td><td>

Unsubscribes to the required channel.

</td></tr><tr><td rowspan="8">

Video

</td><td>

Delete Video

</td><td>

Deletes an uploaded video.

</td></tr><tr><td>

Look up Video

</td><td>

Retrieves information about the specified video.

</td></tr><tr><td>

Look up Videos

</td><td>

Retrieves information about the specified multiple videos.

</td></tr><tr><td>

Rate/Unrate Video

</td><td>

Likes or dislikes the specified video. Also, remove the previous rating for a video.

</td></tr><tr><td>

Search

</td><td>

Searches for the required video, channel, or playlist.

</td></tr><tr><td>

Set Thumbnail to Video

</td><td>

Sets a thumbnail image for an uploaded video.

</td></tr><tr><td>

Set Video Metadata

</td><td>

Sets the metadata of a video.

</td></tr><tr><td>

Upload Video

</td><td>

Uploads a video to your channel in YouTube.

</td></tr></tbody>
</table>## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the YouTube spoke](../task/youtube-setup.md#).

