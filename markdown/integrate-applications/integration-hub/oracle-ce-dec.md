---
title: Oracle Compute Engine Spoke
description: Manage images and instance in the Oracle Compute Engine account from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Oracle Compute Engine Spoke

Manage images and instance in the Oracle Compute Engine account from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Oracle Compute Engine v1.0.4 is the latest version.

## Supported versions

This spoke was built for Oracle Compute Engine API version 20160918, but may be compatible with later versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   [Oracle Cloud IAM Spoke](oracle-iam.md)
-   [Oracle Object Storage Management Spoke](object-storage-mngmt-dec.md)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Oracle Compute Engine spoke provides actions to automate Oracle Compute Engine tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Custom Image Management|Change Image Compartment|Moves an Image into a different compartment within the same tenancy.|
|Create Image|Creates a custom image in the specified compartment.|
|Delete Image|Deletes the specified custom image.|
|Export Image|Exports the specified image to the Oracle Cloud Infrastructure Object Storage service.|
|Get Image|Retrieves a specified custom image.|
|Look up Images|Retrieves a list of available images in the specified compartment.|
|Update Image|Updates details of the specified custom image.|
|Image Shape Compatibility Management|Add Image Shape Compatibility|Adds a shape to the compatible shapes list for the image.|
|Delete Image Shape Compatibility|Deletes an image shape compatibility entry.|
|Get Image Shape Compatibility|Retrieves a specified image shape compatibility entry.|
|Look up Image Shape Compatibilities|Retrieves a list of all the compatible shapes for the specified image.|
|Instance Configuration Management|Change Instance Configuration Compartment|Moves an Instance Configuration into a different compartment within the same tenancy.|
|Create Instance Configuration|Creates an instance configuration.|
|Delete Instance Configuration|Deletes the specified instance configuration.|
|Get Instance Configuration|Gets the specified instance configuration.|
|Look up Instance Configurations|Retrieves a list of instance configurations in the specified compartment.|
|Update Instance Configuration|Updates details of the specified instance configuration.|
|Instance Management|Change Instance Compartment|Moves an Instance into a different compartment within the same tenancy.|
|Create Instance|Creates an instance.|
|Delete Instance|Deletes a specified instance.|
|Get Instance|Retrieves information about the specified instance.|
|Instance Action|Performs a specified power action on an instance.|
|Look up Instances|Retrieves a list of instances in the specified compartment.|
|Update Instance|Updates details of the specified instance.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the Oracle Compute Engine spoke](../task/oracle-ce-setup-dec.md).

