---
title: Docker Spoke
description: Lookup Docker data from your ServiceNow instance. Automate changes in the Docker engine when an event occurs in ServiceNow.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-03"
reading_time_minutes: 4
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Docker Spoke

Lookup Docker data from your ServiceNow instance. Automate changes in the Docker engine when an event occurs in ServiceNow.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Docker spoke v2.3.4 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Supported versions

Community Edition version 18.09.0.

## Spoke actions

The Docker spoke provides actions to automate Docker tasks when events occur in ServiceNow. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Images Management|Create An Image|Creates an image in the Docker instance.|
|List Images|Lists images from the Docker instance.|
|Remove An Image|Removes an image from the Docker instance.|
|Search Images|Searches for images on Docker Hub.|
|Services Management|Create A Service|Creates a service in the Docker instance. Services are tasks run on a swarm.|
|Delete A Service|Deletes a service from the Docker instance.|
|Inspect A Service|Returns detailed information about a service in the Docker instance.|
|Update A Service|Updates a service to the swarm on the docker instance.|
|List Services|Returns a list of services from the Docker instance.|
|Containers Management|Create A Container|Creates a container in the Docker instance.|
|Inspect A Container|Inspects a container in the Docker instance.|
|Kill A Container|Kills a container in the Docker instance.|
|List Containers|Lists containers in the Docker instance.|
|Pause A Container|Suspends all processes in a container on the Docker instance.|
|Remove A Container|Removes a container from the Docker instance.|
|Rename A Container|Renames a container in the Docker instance.|
|Restart A Container|Restarts a container in the Docker instance.|
|Start A Container|Starts a container in the Docker instance.|
|Stop A Container|Stop a container in the Docker instance.|
|Unpause A Container|Unpauses a container in the Docker instance.|
|Update A Container|Updates a container in the Docker instance with the provided values.|
|Wait for A Container|Blocks all processes until a container stops, then returns the exit code for the container on the Docker instance.|
|Executions Management|Create An Exec Instance|Creates an exec instance in Docker, through which you can run a new command in a running container. To execute a command in a container, create and start an exec instance.|
|Inspect An Exec Instance|Inspects an exec instance in Docker.|
|Start An Exec Instance|Starts an exec instance in Docker, through which you can run a new command in a running container.|
|Networks Management|Create A Network|Creates a network on the Docker instance.|
|Inspect A Network|Returns detailed information about a network in the Docker instance.|
|List Networks|Returns a list of networks from the Docker instance.|
|Remove A Network|Removes a network from the Docker instance.|
|Volumes Management|Create A Volume|Creates a volume in Docker.|
|Inspect A Volume|Returns detailed information about a volume in Docker.|
|List Volumes|Returns a list of volumes from Docker.|
|Remove A Volume|Removes a volume from the Docker instance.|
|Swarm Management|Delete A Node|Deletes a node from the Docker instance.|
|Initialize A New Swarm|Initializes a new Docker swarm. A swarm is a group of machines running Docker joined into a cluster.|
|Inspect Swarm|Returns detailed information about a Docker swarm.|
|Join An Existing Swarm|Joins a node to a swarm as a manager or worker node based on the Docker token.|
|Leave A Swarm|Removes a Docker instance from a swarm.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

This spoke uses the Docker alias record to authorize actions. To use the spoke connection alias, create an associated Connection record. This spoke does not require a credential record. For information about setting up the spoke, see [Configure a connection for Docker spoke](../task/setup-docker-spoke.md#).

## MID Server requirements

These actions use REST calls that can run either on an instance or, optionally, through a MID Server. Use the connection record associated with the Docker alias to configure where actions run and, if needed, specify MID Server selection attributes. For more information, see [MID server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

