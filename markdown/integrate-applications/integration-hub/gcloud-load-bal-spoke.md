---
title: Google Cloud Load Balancer Spoke
description: Manage load balancing of your external or internal Virtual Private Cloud \(VPC\) network from ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Google Cloud Load Balancer Spoke

Manage load balancing of your external or internal Virtual Private Cloud \(VPC\) network from ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Google Cloud Load Balancer spoke v1.0.1 is the latest version.

## Supported versions

This spoke was built for Google Cloud Load Balancer v1, but may be compatible with later versions.

## Spoke requirements

Google Cloud Platform \(GCP\) account with access to Google Compute Engine and Google Virtual Private Network.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   Complex Object \(com.glide.cobject\)
-   Google Compute Engine spoke \(sn\_gcompute\_spoke\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke subflows

The Google Cloud Load Balancer Spoke provides subflows to automate Google Cloud Load Balancer tasks when events occurs in your ServiceNow instance. Available subflows include:

|Categotry|Action|Description|
|---------|------|-----------|
|HTTPS Load Balancer Management|Create HTTPS Load Balancer For A New Backend Service|Creates a HTTPS load balancer for a new backend service in the specified project.|
|Create HTTPS Load Balancer For An Existing Backend Service|Creates a HTTPS load balancer for an existing backend service in the specified project.|
|Delete HTTPS Load Balancer|Deletes the components of the specified load balancer.|
|Look up Components Of HTTPS Load Balancer|Retrieves a list of names of all the components associated with a HTTPS load balancer.|
|HTTP Load Balancer Management|Create A HTTP Load Balancer For A New Backend Service|Creates a HTTP load balancer for a new backend service in the specified project.|
|Create HTTP Load Balancer For An Existing Backend service|Creates a HTTP load balancer for an existing backend service in the specified project.|
|Delete HTTP Load Balancer|Deletes the components of a HTTP load balancer.|
|Look up Components Of HTTP Load Balancer|Retrieves a list of names of all the components associated with a HTTP load balancer.|

## Spoke actions

The Google Cloud Load Balancer Spoke provides actions to automate Google Cloud Load Balancer tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Backend Service Management|Create Backend Service|Creates a backend service.|
|Delete Backend Service|Deletes the specified backend service|
|Get Backend Service|Retrieves the details of the specified backend service.|
|Get Health Of Backend Service|Retrieves the health details of the specified backend service.|
|Look up Backend Services|Retrieves a list of all backend services.|
|Update Backend Service|Updates the details of the specified backend service.|
|Global Address Management|Create A Global Address|Creates a global address.|
|Delete A Global Address|Deletes the specified global address.|
|Get Global Address|Retrieves the details of all the global addresses.|
|Look up Global Addresses|Retrieves a list of all global addresses.|
|Global Forwarding Rule Management|Create Global Forwarding Rule|Creates a global forwarding rule.|
|Delete Global Forwarding Rule|Deletes the specified global forwarding rule.|
|Get Global Forwarding Rule|Retrieves the details of a global forwarding rule.|
|Look up Global Forwarding Rules|Retrieves a list of all global forwarding rules.|
|Set Target For Global Forwarding Rule|Assigns target information to the specified global forwarding rule.|
|HTTP Health Check Management|Create A HTTP Health Check|Creates a HTTP health check.|
|Delete A HTTP Health Check|Deletes the specified HTTP health check.|
|Get HTTP Health Check|Retrieves the details of the specified HTTP health check.|
|Look up HTTP Health Checks|Retrieves a list of all HTTP health checks.|
|Update A HTTP Health Check|Updates the details of the specified HTTP health check.|
|HTTP Load Balancer Management|Get Resource Name|Retrieves the name of the resource from a resource URL.|
|HTTPS Health Check Management|Create A HTTPS Health Check|Creates a HTTPS health check.|
|Delete A HTTPS Health Check|Deletes the specified HTTPS health check.|
|Get HTTPS Health Check|Retrieves the details of the specified HTTPS health check.|
|Look up HTTPS Health Checks|Retrieves a list of HTTPS health checks.|
|Update A HTTPS Health Check|Updates the details of the specified HTTPS health check.|
|Instance Group Manager Management|Create An Instance Group Manager|Creates an instance group manager.|
|Create Instance In Instance Manager Group|Creates an instance in the specified instance group manager.|
|Delete An Instance Group Manager|Deletes the specified instance group manager.|
|Get Instance Group Manager|Retrieves the details of a specified instance group manager.|
|Look up Instance Group Managers|Retrieves a list of managed instance groups.|
|Look up Managed Instances In An Instance Group Manager|Retrieves a list of managed instances in a specified managed instance group.|
|Resize An Instance Group Manager|Resizes the number of instances in a specified instance group manager.|
|Update Instance Template Of An Instance Group Manager|Assigns the details of instance template to the specified instance group manager.|
|Target HTTP Proxy Management|Create Target HTTP Proxy|Creates a target HTTP proxy.|
|Delete Target HTTP Proxy|Deletes the specified target HTTP proxy.|
|Get Target HTTP Proxy|Retrieves the details of the specified target HTTP proxy.|
|Look up Target HTTP Proxies|Retrieves a list of all target HTTP proxies.|
|Update URL Map Of Target HTTP Proxy|Assigns the URL map information to the specified target HTTP proxy.|
|Target HTTPS Proxy Management|Create Target HTTPS Proxy|Creates a target HTTPS proxy.|
|Delete Target HTTPS Proxy|Deletes the specified target HTTPS proxy.|
|Get Target HTTPS Proxy|Retrieves the details of the specified target HTTPS proxy.|
|Look up Target HTTPS Proxies|Retrieves a list of the target HTTPS proxies.|
|Set SSL Certificates To Target HTTPS Proxy|Assigns SSL certificates to the specified target HTTPS proxy.|
|Set URL Map To Target HTTPS Proxy|Assigns URL map information to the specified target HTTPS proxy.|
|URL Map Management|Create URL Map|Creates a URL map.|
|Delete URL Map|Deletes the specified URL map.|
|Get URL Map|Retrieves the details of the specified URL map.|
|Look up URL Maps|Retrieves the details of all URL maps.|
|Update URL Map|Updates the details of the URL map.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the Google Cloud Load Balancer Spoke](../task/setup-gcloud-load-bal.md#).

