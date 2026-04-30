---
title: Plugins or applications installed with ITOM Cloud Accelerate
description: Tables that list the plugins or applications that are installed with ITOM Cloud Accelerate applications. When you update your application, any newly required application dependencies are installed.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [ITOM Cloud Accelerate reference, ITOM Cloud Accelerate, IT Operations Management]
---

# Plugins or applications installed with ITOM Cloud Accelerate

Tables that list the plugins or applications that are installed with ITOM Cloud Accelerate applications. When you update your application, any newly required application dependencies are installed.

## Cloud Services Catalog

The CSC Content Pack plugin \(sn\_itom\_csc\_cp\) provides the required predefined content for the Cloud Services Catalog application. This content includes governance policies and actions to deliver an end-to-end governed deployment workflow.

|Plugin or application name|Description|
|--------------------------|-----------|
|Cloud Provisioning and Governance: Terraform Connector \(sn\_cmp\_terraform\)|Integrates Terraform Open Source, Terraform Enterprise, and Terraform Cloud with ITOM Cloud Provisioning and Governance \(CPG\), enabling you to provision and manage services in multiple clouds like AWS, Azure, GCP, and VMware. The Terraform templates are codified as cloud template catalogs that you can use to provision cloud resources.|
|Cloud Discovery Workspace \(sn\_cloud\_ops\_ws\)|Offers a comprehensive solution to manage the cloud operations of your organization.|
|Cloud Provisioning and Governance \(com.snc.cloud.mgmt\)|Provides a single interface to access cloud resources, publish cloud offerings to a catalog, and manage the use of those resources.|
|Guided Setup \(sn\_ads\_setup\)|Enables you to step through the initial configuration of any product or application that provides a Guided Setup module. Guided Setup assists you with planning the roll-out of a product and performing the basic configuration necessary to go live.|
|ITOM/OT SU Licensing \(sn\_itom\_licensing\)|Calculates and displays how many subscriptions for ITOM applications your organization purchases and consumes.|

|Plugin or application name|Description|
|--------------------------|-----------|
|Cloud Services Catalog \(sn\_itom\_csc\)|Provides a simplified interface to automate cloud management and access cloud resources. The application enables you to publish cloud offerings to a catalog and manage the usage and life cycle of those resources.|
|ServiceNow IntegrationHub Action Step - SSH \(com.glide.hub.action\_step.ssh\)|The SSH step executes SSH commands on an external \*nix system through a ServiceNow® MID Server. The step also stores scripts and commands for the \*nix systems.|
|Agent Client Collector Framework \(sn\_agent\)|Manages Agent Client Collector on the ServiceNow instance and the MID Server.|
|CCG Content Pack \(sn\_itom\_ccg\_cp\)|Provides optional predefined content for the Cloud Configuration Governance application such as policies, resource collectors, configuration collectors, and remediation actions.|
|Flow Designer Action Step - Email \(com.glide.hub.action\_step.email\)|Provides the Send Email step to send an email to specified users or groups as an action in a flow.|

## Cloud Migration Assessment

|Plugin or application name|Description|
|--------------------------|-----------|
|ITOM/OT SU Licensing \(sn\_itom\_licensing\)|Calculates and displays how many subscriptions for ITOM applications your organization purchases and consumes.|
|Discovery \(com.snc.discovery\)|Finds applications and devices on your network, and then updates the CMDB with the information it finds.|
|Cloud Migration Base \(com.sn\_cloud\_mig\_base\)|A base plugin to support the Cloud Migration Assessment application.|

## Cloud Configuration Governance

The CCG Content Pack plugin \(sn\_itom\_ccg\_cp\) provides optional predefined content for the Cloud Configuration Governance application such as policies, resource collectors, configuration collectors, and remediation actions.

|Plugin or application name|Description|
|--------------------------|-----------|
|Cloud Action Library \(sn\_itom\_cal\)|Provides predefined actions and sublows to enable interaction with the cloud resources of your organization. ServiceNow® ITOM Cloud Accelerate features such as Cloud Configuration Governance use these actions to operate.|

|Plugin or application name|Description|
|--------------------------|-----------|
|Cloud Configuration Governance \(sn\_itom\_ccg\)|Checks the configuration settings of cloud resources in your organization against a set of policies to identify violations. After the violation is identified, you can use remediation workflows to mitigate them.|

## Cloud Action Library

|Plugin or application name|Description|
|--------------------------|-----------|
|ITOM/OT SU Licensing \(sn\_itom\_licensing\)|Calculates and displays how many subscriptions for ITOM applications your organization purchases and consumes.|
|Flow Designer Action Step - Payload Builder \(com.glide.hub.action\_step.payload\)|Enable action designers to easily create name-value pairs in JSON and XML payloads using dynamic data.|
|ServiceNow IntegrationHub Action Step - Get Connection Info \(com.glide.hub.action\_step.get\_connection\_info\)|Provides the connection and credential details from another step, such as a representational state transfer \(REST\) step, to other steps in your action.|
|ServiceNow IntegrationHub Action Step - XML Parser \(com.glide.hub.action\_step.xmlparser\)|Enables the XML parser action step in Workflow Studio.|
|ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)|Enables execution of IntegrationHub actions and flows.|
|Cloud Provisioning and Governance Core \(com.snc.cloud.core\)|Contains resource blocks and cloud Application Programming Interface \(cloud API\) mappings related to Cloud API-based discovery and events processed by either response mapping or calling patterns.|
|Flow Designer Action Step - Script on MID \(com.glide.hub.action\_step.script\_mid\)|Provides an action step to execute custom JavaScript within a reusable action on a MID Server.|
|ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)|Enables the REST action step in Workflow Studio.|
|ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)|Send REST, SOAP, or JDBC requests from Workflow Studio to APIs that return a stream of response data larger than 10 MB, or that return paginated results. Parse stream data into a series of complex object outputs and use the data pills in other actions in a flow.|

**Related topics**  


[Plugins or applications installed with ITOM Visibility](../../it-operations-management/reference/plugin-app-itom-visibility.md)

[Plugins or applications installed with ITOM Health](../../it-operations-management/reference/plugin-app-itom-health.md)

[Plugins activated with ITOM Optimization](../../it-operations-management/reference/plugin-itom-optimization.md)

[Applications installed with Now Assist for ITOM](../../now-assist-itom/reference/app-now-assist-itom.md)

