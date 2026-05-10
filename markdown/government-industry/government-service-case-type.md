---
title: Public Sector Digital Services case types
description: You can use a public service case, which is based on the Government Service case type, to extend the customer service case from the Customer Service Management application. By using a case type, you can define the processes and data that are needed to resolve your public service requests.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Case Management, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Public Sector Digital Services case types

You can use a public service case, which is based on the Government Service case type, to extend the customer service case from the Customer Service Management application. By using a case type, you can define the processes and data that are needed to resolve your public service requests.

## Overview of a case type

A case type represents the processes and data needed to resolve a specific type of constituent request. For example, within Public Sector, government service agents can use case types for different constituent needs such as requests for information, requests for maintenance, social benefits application processing, or managing licenses and permits. You can associate record producers with a certain type of case so that when you submit that record producer through the portal, it creates a case of the correct type. In addition to using service definitions, you can use the case types feature to create and configure the different types of government service cases that your agency handles. For more information on service definitions, see [Service definitions for Public Sector Digital Services](psds-service-definitions.md).

The base Government Service case type is called a public service case, and is an extension of the Customer Service case type from the Customer Service Management application. Each Public Sector Digital Services playbook application comes with its own case type \(for example, Information Request Playbook has an Information Request case type that comes by default, which is an extension of the base Government Service case type\). The Information Request case type can be extended further if your specific use case goes beyond what it offers.

As an administrator, you can extend from existing base case types that are provided in applications out-of-the-box to create additional case types for various government services that your agency offers, or you can create and configure an entirely new case type that extends the Case table, in order to implement specific case application types, and enabling you to take advantage of prebuilt roles, business rules, and other business logic.

Creating a new case type can include creating a new table that is an extension of an existing case, or creating an entirely new case type. Typically this involves creating new roles, modules, workspaces, and other required entities. For additional information on case types, see [Customer Service Case Types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-service-case-types.md)

All Public Sector Digital Services applications have a base case type table. Use the base case type table when adding a new case type for that application. For example, if you need a new case type in License and Permit Playbook, extend the License and Permit Base Case table, which is itself an extension of the Government Service base case table and was created to capture more specific information related only to a License and Permit case. However, if there is need for a new case type for which there is no base application in PSDS that works, extend the base PSDS case \[sn\_govservice\_case\] table.For more information on the base tables installed with each Public Sector Digital Services application, see [Public Sector Digital Services Data Model](public-sector-digital-services-data-model.md).

You can use both case types and service definitions to define the data and processes that are needed to resolve a government service request. For more information on service definitions in Public Sector Digital Services, see [Service definitions for Public Sector Digital Services](psds-service-definitions.md)

When you are evaluating whether you need to create a new case type in Public Sector Digital Services, you should consider the following:

-   Should I use a service definition instead of a new case type?
-   Does an application already exist that I can use for my use case?
-   Which base PSDS case type should I extend when creating the new case type?

## Case type tasks for administrators

You can configure a case type by creating a table for the new case type that extends the government service base case table. Then, you can set up a series of processes and components for that case type.

-   To get an overview of this process, see the Government Service Case Types Guided Setup.
-   For more details on how to configure case types using Guided Setup, see [Configuring customer service case types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-csm-case-types.md).

An agent can then use this custom case type to create a case to resolve a constituent or business request. .

## Government Service Case Types plugin

The Customer Service Case Types plugin \(com.snc.csm\_case\_types\) is activated when you enable the Public Sector Digital Services Core plugin \(sn\_gsm\).

Activating this plugin adds the Case Types module to the application navigator. You can use this module to create and manage case types, as well as extend the Government Service base case type.

For more information on the plugins that are installed with the Public Sector Digital Services Core application, see [Components and Roles installed with Public Sector Digital Services Core](../reference/installed-with-public-sector-digital-services-core.md).

## Case Types Guided Setup

Activating the Customer Service Case Types plugin adds the Case Types section to the Public Sector Digital Services Core Guided Setup.

Navigate to **All** &gt; **Constituent Service** &gt; **Administration** &gt; **Guided Setup** and use the tasks in this section to create and configure a case type.

You can configure several different processes and components for a Government Service case type by using guided setup, including the roles, access control lists \(ACLs\), notifications, actions, and record producers.

To create and configure a case type, do the following tasks.

-   Create a table for the new case type that extends the base Case table \(sn\_gsm\_government\_service\_case\).
-   Configure the UI actions, UI policies, and client scripts for the new case type.
-   Configure the views and view rules, roles and access controls \(ACLs\), business rules, and more for the new case type.
-   Set up the processes for the case type, including the record producers, state flows, and special handling notes.
-   Create a case type definition record for the new case type and add it to the Case Type table \(sn\_case\_type\).
-   Configure the Get Case Types flow and modify the conditions that determine the visibility for a case type.

For more information on using Guided Setup for Public Sector Digital Services, see [Configure Public Sector Digital Services Core foundational data using guided setup](configure-psds-foundation-data.md#).

## Government Service case type applications

The following table lists the applications available from the ServiceNow Store that use the Government Service case type and its extensions.

<table id="table_iay_abl_kbz"><thead><tr><th>

Application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Grants Management\(sn\_gsm\_grnt\_mgmt\)

</td><td>

Provides an end-to-end workflow for handling applications for grants submitted by public sector end users.

</td></tr><tr><td>

Social Benefits Playbook\(sn\_gsm\_soc\_bnfts\)

</td><td>

Provides an end-to-end workflow for handling applications for one or more social benefit programs submitted by public sector end users.

</td></tr><tr><td>

License and Permit Playbook\(sn\_gsm\_license\_permit\)

</td><td>

Playbook that provides step-by-step guidance through the life cycle of license or permit request case. This playbook uses the license and permit request case type to capture the details of a request for new license.

</td></tr><tr><td>

Information Request Playbook\(sn\_gsm\_info\_req\)

</td><td>

Playbook that provides step-by-step guidance through the life cycle of an information request case. This playbook uses the information request case type to capture the details of a requests for various types of federal, state, and local public records that fall outside of nine exemptions.

</td></tr><tr><td>

Service Request Playbook \(sn\_gsm\_srvc\_req\)

</td><td>

Playbook that provides step-by-step guidance through the life cycle of a service request case. This playbook uses the service request case type to capture the details of the requests for the various types of community maintenance. For more information, see [Life cycle of a Public Service case](../reference/government-service-case-states.md). The Service Request case table \[sn\_gsm\_service\_request\_case\] is installed with Service Request Playbook.

</td></tr></tbody>
</table>Review the [Service Request Playbook](https://store.servicenow.com/sn_appstore_store.do#!/store/application/7aade7bb87a0d51056f84089cebb35ff), [Information Request Playbook](https://store.servicenow.com/sn_appstore_store.do#!/store/application/bd7902882cd29510f877ae4a7a748ca3), [License and Permit Playbook](https://store.servicenow.com/sn_appstore_store.do#!/store/application/50f57c9d93d4f950e3e7b0627cba1045), [Social Benefits playbook](https://store.servicenow.com/sn_appstore_store.do#!/store/application/1490efb5c3fbf5509fad2abdc0013133/1.1.1?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%25253Bgenerative_ai%25253Bsnow_solution%26q%3Dsocial%2520benefits&sl=sh), or [Grants Management](https://store.servicenow.com/store/app/b687d2b01bd52a50396216db234bcbf3) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

## Public Service case stages

The government service case type moves through the stages that are listed in the following table.

|Stage|Description|
|-----|-----------|
|Intake|Default stage for a new case.|
|Review|Stage when the state is updated from Draft to Open because the case is assigned and has been accepted by the agent named in the **Assigned to** field.|
|Process|Stage when the state is updated from Open to Work In Progress.|
|Decision|Stage when the state is updated from Work In Progress to Resolved.|

## Public Service Case states

The government case type moves through the states that are listed in the following table. For more information, see [Life cycle of a Public Service case](../reference/government-service-case-states.md).

|State|Description|
|-----|-----------|
|Draft|Default state for a new case.|
|New|Case that moves from Draft to New when the user selects **Submit**.|
|Open|Case that moves from New to Open when it’s assigned and has been accepted by the agent in the **Assigned to** field.|
|Work in Progress|Case that moves from Open to Work in Progress when the agent selects **Start Work**.|
|Awaiting Info|Case that moves from Work in Progress to Awaiting Info when the agent selects **Request Info**.|
|Resolved|Case that moves to the Resolved state when the agent selects **Propose Solution**.|
|Closed|Case that moves to the Closed state when the requester selects **Accept Solution** or **Close Case**.|
|Cancelled|Case that is moved to the Cancelled state. This can happen through automatic timeout, or if the requester selects **Cancel**.|

