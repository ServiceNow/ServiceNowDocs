---
title: ServiceNow Studio Navigator panel taxonomy
description: Learn more about each metadata file type and its corresponding primary table in the File categories tab of the ServiceNow Studio Navigator panel.
locale: en-US
release: australia
product: ServiceNow Studio
classification: servicenow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 35
breadcrumb: [Reference, ServiceNow Studio, Developing your application, Building applications]
---

# ServiceNow Studio Navigator panel taxonomy

Learn more about each metadata file type and its corresponding primary table in the File categories tab of the ServiceNow Studio Navigator panel.

**Note:** Any additional extensions of the sys\_metadata table are automatically included in the Navigator panel in the appropriate section.

For each file category, see the file types that you can create and their corresponding primary table. For more information about navigating to a file's primary table, see [Navigate directly to a table in ServiceNow Studio](../task/qs-navigate-directly-to-table.md).

Metadata-specific admin roles are existing roles on the ServiceNow AI Platform that provide developers with admin access to a specific metadata type. For example, a script include admin allows a developer to create, read, update, or delete any script include on the ServiceNow AI Platform and perform development on script includes in ServiceNow Studio. For more information, see [ServiceNow Studio personas and roles](../concept/sn-studio-personas-roles.md).

## AI files

AI files provide ways to use generative AI to enhance user productivity and efficiency through conversation and proactive experiences.

**Important:** AI options in the ServiceNow Studio file taxonomy are only available if the AI components have been installed and configured.

<table id="table_jsx_hzn_gfc"><thead><tr><th>

File type

</th><th>

Description

</th><th>

Primary table

</th><th>

Primary editing experience

</th></tr></thead><tbody><tr><td>

Agentic Workflow

</td><td>

An agentic workflow is a business problem that you want to solve. In AI Agent Studio, you must define an agentic workflow and connect it with an AI agent to get a resolution plan.

 For more information, see [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

</td><td>

sn\_aia\_usecase

</td><td>

AI Agent Studio

</td></tr><tr><td>

AI Agent

</td><td>

AI Agents are entities that mimic human-like intelligence by using large language models \(LLMs\). AI agents can perform tasks that range from simple automated responses to complex problem solving. By using AI agents, you can reduce the workloads of your live agents and help increase their productivity.

 For more information, see [Create an AI agent](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

</td><td>

sn\_aia\_agent

</td><td>

AI Agent Studio

</td></tr><tr><td>

Skill

</td><td>

Skills are user-defined AI capabilities tailored to meet specific business needs. Custom skills are created using Now Assist Skill Kit, which allows for a user to define input data, prompts, LLM providers and deployment areas for custom skills.

 For more information, see [Create a skill](https://www.servicenow.com/docs/access?context=create-new-skill&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

</td><td>

sn\_nowassist\_skill\_config

</td><td>

UI16

</td></tr></tbody>
</table>## Automation files

Automations provide ways to manage recurring tasks efficiently, with fewer steps, reducing human input and effort. For example, you can configure an email notification to be sent automatically when a record is approved. Create automations to streamline and simplify how you work by adding automations to an app, such as actions, flows, and other automatic tasks.

<table id="table_zws_dv2_ddc"><thead><tr><th>

File type

</th><th>

Description

</th><th>

Primary table

</th><th>

Primary editing experience

</th></tr></thead><tbody><tr><td>

Action

</td><td>

Actions automate a repeatable task or operation within a flow as a sequence of related steps. Actions run a sequence of steps to complete the task, and pass data to the flow as outputs.

 For more information, see [Exploring actions](https://www.servicenow.com/docs/access?context=exploring-actions&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

</td><td>

sys\_hub\_action\_type\_definition

</td><td>

Workflow Studio

</td></tr><tr><td>

Activity definition

</td><td>

Activity definitions describe how the activities in your playbook get the data that they need when your playbook runs. Each activity definition contains some basic configuration details, as well as an automation plan and activity experience.

 For more information, see [Activity definitions](https://www.servicenow.com/docs/access?context=activity-definitions&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

</td><td>

sys\_pd\_activity\_definition

</td><td>

UI16

</td></tr><tr><td>

Connection &amp; Credential Aliases

</td><td>

A Connection and Credential alias defines an alias that labels a credential or connection record, enabling an app to connect to another system or component.

 For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td><td>

sys\_alias

</td><td>

UI16

</td></tr><tr><td>

Data stream

</td><td>

A data stream is a reusable action that processes a stream of response data within a flow. For example, you can create a data stream action to import a large quantity of employee data from a third-party HR site.

 For more information, see [Data Stream actions and pagination](https://www.servicenow.com/docs/access?context=data-stream-actions&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

</td><td>

sys\_hub\_action\_type\_definition

</td><td>

Workflow Studio

</td></tr><tr><td>

Decision table

</td><td>

Decision tables decouple decision logic from your code by creating and maintaining decision rules. Decision tables provide a single point where you can create, view, and modify decisions.

 For more information, see [Exploring Decision Tables](https://www.servicenow.com/docs/access?context=decision-designer-overview&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

</td><td>

sys\_decision

</td><td>

Workflow Studio

</td></tr><tr><td>

Email Template

</td><td>

Email templates enable administrators to create reusable content for the subject line and message body of email notifications. Admins can add rich text and other items, such as images, to email templates.

 For more information, see [Email templates](https://www.servicenow.com/docs/access?context=c_EmailTemplates&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td><td>

sysevent\_email\_template

</td><td>

UI16

</td></tr><tr><td>

External trigger

</td><td>

External triggers are reusable triggers that respond to external events through webhooks. When an event occurs in the configured third-party application that meets the specified conditions, the trigger is activated.For more information, see [Create a saved external trigger](https://www.servicenow.com/docs/access?context=create-saved-external-trigger&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

</td><td>

sys\_ih\_external\_trigger\_definition

</td><td>

UI16

</td></tr><tr><td>

Flow

</td><td>

Flows are automated processes that consist of a trigger and a sequence of reusable actions and flow logic. The trigger specifies when to run the flow. The actions perform a sequence of operations on your data. For example, the Visual Task Boards \(VTB\) Sample Flow creates and assigns a VTB card whenever a priority 1 incident is created.

 For more information, see [Exploring flows](https://www.servicenow.com/docs/access?context=exploring-flows&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

</td><td>

sys\_hub\_flow

</td><td>

Workflow Studio

</td></tr><tr><td>

Notification

</td><td>

Notifications alert users when a record changes. For example, you could get a push notification when a request is rejected.

 For more information, see [System notifications](https://www.servicenow.com/docs/access?context=system-notifications-landing&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td><td>

sysevent\_email\_action

</td><td>

UI16

</td></tr><tr><td>

Playbook

</td><td>

Playbooks are sets of automated activities that occur based on a trigger. For example, you can create a playbook for your app to send an email when a request is approved.

 For more information, see [Building your first playbook](https://www.servicenow.com/docs/access?context=getting-started-processes&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

</td><td>

sys\_pd\_process\_definition

</td><td>

Workflow Studio

</td></tr><tr><td>

Subflow

</td><td>

Subflows are processes that consist of a sequence of reusable actions and flow logic, data inputs, and outputs. In contrast to flows, subflows don’t have a trigger but instead run when called from a playbook, flow, another subflow, or a script.

 For more information, see [Exploring subflows](https://www.servicenow.com/docs/access?context=exploring-subflows&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

</td><td>

sys\_hub\_flow

</td><td>

Workflow Studio

</td></tr><tr><td>

Trigger

</td><td>

Triggers contain the start conditions for your automation. You can create separate triggers for each flow or create a reusable saved trigger that you can use in multiple flows.For more information, see [Building triggers](https://www.servicenow.com/docs/access?context=building-triggers&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

</td><td>

sys\_hub\_trigger\_template

</td><td>

Workflow Studio

</td></tr></tbody>
</table>## Client development files

Client development files define operations that occur based on actions you can take when working with an app built in ServiceNow Studio.

<table id="table_it4_jw2_ddc"><thead><tr><th>

File type

</th><th>

Description

</th><th>

Primary table

</th><th>

Primary editing experience

</th></tr></thead><tbody><tr><td>

Assignment Data Lookup

</td><td>

Use assignment data lookups to assign a record automatically using Data Lookup and Record Matching. For example, you can automatically set a value in the assigned\_to and assignment\_group fields for a record when a set of conditions occurs, such as assigning approvals to a group of managers for users below a certain level.

 For more information, see [Defining assignment rules](https://www.servicenow.com/docs/access?context=c_DefineAssignmentRules&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td><td>

dl\_u\_assignment

</td><td>

UI16

</td></tr><tr><td>

Client Extension Instance

</td><td>

Use a client extension integration to a registered instance of a client extension point that links a UI script with a client extension point. The UI script is included on pages that invoke the client extension point.

 For more information, see [Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=australia&pubname=australia-api-reference&ft:locale=en-US).

</td><td>

sys\_client\_extension\_instance

</td><td>

UI16

</td></tr><tr><td>

Client Extension Point

</td><td>

Client extension points extend the functionality of an application without altering the original application code. Extension points can help prevent your custom code interactions from breaking, which often occurs after an upgrade if you directly embed the custom code into the application code.

 For more information, see [Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=australia&pubname=australia-api-reference&ft:locale=en-US).

</td><td>

sys\_client\_extension\_point

</td><td>

UI16

</td></tr><tr><td>

Client Script

</td><td>

Client scripts enable apps on the ServiceNow AI Platform to run JavaScript on the client \(web browser\) when client-based events occur. For example, it could run when a form loads, after form submission, or when a field changes value.

 For more information, see [Client scripts](https://www.servicenow.com/docs/access?context=client-scripts&version=australia&pubname=australia-api-reference&ft:locale=en-US).

</td><td>

sys\_script\_client

</td><td>

UI16

</td></tr><tr><td>

Data Lookup Definitions

</td><td>

Data lookup definitions are no-code solutions that enable you get attributes from a record on the same table. For example, you can create a data lookup definition to populate an email field automatically when you enter your name.

 For more information, see [Create a catalog lookup definition](https://www.servicenow.com/docs/access?context=t_CreatACatDataLookupDefRec&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td><td>

dl\_definition

</td><td>

UI16

</td></tr><tr><td>

Priority Data Lookup

</td><td>

Priority data lookups enable you to define the impact and urgency of an incident to calculate how it should be prioritized.

 For more information, see [Define priority lookup rules](https://www.servicenow.com/docs/access?context=def-prio-lookup-rules&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

</td><td>

dl\_u\_priority

</td><td>

UI16

</td></tr><tr><td>

UI Extension Instance

</td><td>

Use a UI extension instance to create a registered instance of a UI extension point that links a UI macro with a UI extension point. The macro can be called whenever the UI extension point is invoked.

 For more information, see [Creating and adding a UI extension point](https://www.servicenow.com/docs/access?context=impl-ui-ext-pts-base-code&version=australia&pubname=australia-api-reference&ft:locale=en-US).

</td><td>

sys\_ui\_extension\_instance

</td><td>

UI16

</td></tr><tr><td>

UI Extension Point

</td><td>

UI extension points enable you to add custom content to a UI page without having to modify the page directly. You must first create the UI extension points, and then add them to the UI macros in the base application code.

 For more information, see [Using UI extension points in server-side UI macros](https://www.servicenow.com/docs/access?context=ui-extension-points&version=australia&pubname=australia-api-reference&ft:locale=en-US).

</td><td>

sys\_ui\_extension\_point

</td><td>

UI16

</td></tr><tr><td>

UI Policy

</td><td>

UI policies dynamically change the behavior of information on a form and control custom process flows for tasks. For example, you can use UI policies to make the number field on a form read only, make the short description field required, and hide other fields.

 For more information, see [Using UI policies](https://www.servicenow.com/docs/access?context=t_CreateAUIPolicy&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td><td>

sys\_ui\_policy

</td><td>

UI16

</td></tr><tr><td>

UI Script

</td><td>

UI scripts provide a way to package client-side JavaScript into a reusable form, similar to how script includes store server-side JavaScript.

 For more information, see [UI scripts](https://www.servicenow.com/docs/access?context=c_UIScripts&version=australia&pubname=australia-api-reference&ft:locale=en-US).

</td><td>

sys\_ui\_script

</td><td>

UI16

</td></tr></tbody>
</table>## Content files

Content files define ways to provide users and systems with information by referring to knowledge articles and other forms of communication. For example, content files can reference knowledge articles, static blocks of text, or external web-based content. Use content files to provide information to apps you're building in ServiceNow Studio.

<table id="table_qkg_rx2_ddc"><thead><tr><th>

File type

</th><th>

Description

</th><th>

Primary table

</th><th>

Primary editing experience

</th></tr></thead><tbody><tr><td>

Audio

</td><td>

Use audio files to upload sounds and recordings that your app can use on the ServiceNow AI Platform.

 For more information, see [Manage audio files](https://www.servicenow.com/docs/access?context=t_UploadAnAudioFile&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td><td>

db\_audio

</td><td>

UI16

</td></tr><tr><td>

Detailed content

</td><td>

Use a detailed content block to display the content of an existing document, such as an incident, knowledge article, or service management request.

 For more information, see [Configure a detailed content block](https://www.servicenow.com/docs/access?context=t_DetailedContentBlock&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td><td>

content\_block\_detail

</td><td>

UI16

</td></tr><tr><td>

Dynamic content

</td><td>

Dynamic content uses scripting or pulls information from the ServiceNow AI Platform into an app. For example, use dynamic content to create a job posting, where the postings are stored in knowledge articles and displayed in the app with a dynamic block.

 For more information, see [Configure dynamic blocks](https://www.servicenow.com/docs/access?context=t_CreateADynamicBlock&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td><td>

content\_block\_programmatic

</td><td>

UI16

</td></tr><tr><td>

iFrames

</td><td>

Use iFrames to embed a URL on a page within a frame. You can embed external pages or render ServiceNow content.

 For more information, see [Configure iFrames](https://www.servicenow.com/docs/access?context=t_IFrame&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td><td>

content\_block\_iframe

</td><td>

UI16

</td></tr><tr><td>

Images

</td><td>

Upload and store images on the ServiceNow AI Platform to be used in apps and forms. You can then reference images from HTML fields by appending the name of the image to the URL of the instance.

 For more information, see [Storing images in the database](https://www.servicenow.com/docs/access?context=c_StoringImagesInTheDatabase&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td><td>

db\_image

</td><td>

UI16

</td></tr><tr><td>

Static content

</td><td>

Use static blocks for text that doesn’t change. For example, use a static block for a site footer with only the company or organization name.

 For more information, see [Configure a static HTML block](https://www.servicenow.com/docs/access?context=t_StaticHTMLBlock&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td><td>

content\_block\_static

</td><td>

UI16

</td></tr></tbody>
</table>## Data files

Data files enable you to use information stored in or referenced by an application in apps built in ServiceNow Studio. Data is the foundation of any app. You can start with a table, or upload spreadsheets and PDFs to get data into the ServiceNow AI Platform for apps to consume.

<table id="table_sb3_bbf_ddc"><thead><tr><th>

File type

</th><th>

Description

</th><th>

Primary table

</th><th>

Primary editing experience

</th></tr></thead><tbody><tr><td>

Form

</td><td>

A form is a content page that displays fields and values for a single record from a database table.

 For more information, see [Forms in Table Builder](../../../administer/form-builder/concept/form-view-configuration.md).

</td><td>

sys\_ui\_form

</td><td>

Form Builder

</td></tr><tr><td>

Form section

</td><td>

Use sections to design the layout of a form. For example, you can have one column or two.

 For more information, see [Customize your form layout in Table Builder](../../../administer/form-builder/task/customize-form-layout.md).

</td><td>

sys\_ui\_section

</td><td>

Form Builder

</td></tr><tr><td>

Many to Many Definition

</td><td>

Use a many to many task to define relationships between different tasks. You can implement one-to-one, one-to-many, and many-to-many relationships. For example, users and roles are a many-to-many relationship because a user can have multiple roles, and multiple users can have any given role.

 For more information, see [Creating many-to-many task relations](https://www.servicenow.com/docs/access?context=c_ManyToManyTaskRelations&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td><td>

sys\_m2m

</td><td>

UI16

</td></tr><tr><td>

Relationship

</td><td>

Use relationships to define how tables interact with each other. You can create relationships between tables by extending tables, referencing records in another table, creating many-to-many relationships, and joining tables in a database view.

 For more information, see [Table relationships](https://www.servicenow.com/docs/access?context=table-relationships&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td><td>

sys\_relationship

</td><td>

UI16

</td></tr><tr><td>

Table

</td><td>

Tables are the foundation of how the ServiceNow AI Platform stores data. When you view a table as a list, each row is a record, and each column is a field from the record. For example, the Incident table has a record for every customer interaction, or incident.

 For more information, see [ServiceNow AI Platform tables and data](https://www.servicenow.com/docs/access?context=tables-fields-and-forms&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and [Table Builder](../../../administer/form-builder/concept/tb-landing-page.md).

 Preferred table admins can configure preferred tables for Table Builder. For more information, see [ServiceNow Studio personas and roles](../concept/sn-studio-personas-roles.md).

</td><td>

sys\_db\_object

</td><td>

Table Builder

</td></tr><tr><td>

Table Column

</td><td>

A table column represents a field from a record. For example, a user record might have a column for first name and a separate column for family name.

 For more information, see [Table properties in Table Builder](../../../administer/form-builder/reference/table-parameters.md).

</td><td>

sys\_dictionary

</td><td>

UI16

</td></tr></tbody>
</table>## Inbound integration files

Inbound integrations enable you to get information and data onto the ServiceNow AI Platform from another system or source. Inbound integrations enable seamless data flow into ServiceNow from external systems, facilitating efficient communication and integration between systems.

<table id="table_wfy_ycf_ddc"><thead><tr><th>

File type

</th><th>

Description

</th><th>

Primary table

</th><th>

Primary editing experience

</th></tr></thead><tbody><tr><td>

Data Import

</td><td>

Use data imports to view the all the records that are being processed for an import job and also the import jobs that are awaiting approvals.

 For more information, see [Importing data using import sets](https://www.servicenow.com/docs/access?context=c_ImportDataUsingImportSets&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) and [Integration Hub - Import](https://www.servicenow.com/docs/access?context=integrationhub-imports&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

</td><td>

sn\_ihub\_integration\_instance

</td><td>

Integration Hub

</td></tr><tr><td>

Data Source

</td><td>

A data source specifies how and where to get the data you want to import.

 For more information, see [Data sources](https://www.servicenow.com/docs/access?context=c_DataSources&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) and [Configure a data source](https://www.servicenow.com/docs/access?context=configure-data-source&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

</td><td>

sys\_data\_source

</td><td>

UI16

</td></tr><tr><td>

Scheduled Data Import

</td><td>

Scheduled data imports specify to import data from data sources using import sets. Transform maps are applied to the imported data before writing the data to the target table.

 For more information, see [Run or schedule a data import](https://www.servicenow.com/docs/access?context=run-schedule-data-imports&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

</td><td>

scheduled\_import\_set

</td><td>

UI16

</td></tr><tr><td>

Scheduled Data Import

</td><td>

Scheduled data imports specify to import data from data sources. Transform maps are applied to the imported data before writing the data to the target table.

 For more information, see [Run or schedule a data import](https://www.servicenow.com/docs/access?context=run-schedule-data-imports&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

</td><td>

scheduled\_data\_import

</td><td>

UI16

</td></tr><tr><td>

Scripted REST API

</td><td>

Use scripted REST APIs to build custom web service APIs for your application. You can define service endpoints, query parameters, and headers for a scripted REST API, as well as scripts to manage the request and response.

 For more information, see [Scripted REST APIs](https://www.servicenow.com/docs/access?context=c_CustomWebServices&version=australia&pubname=australia-api-reference&ft:locale=en-US).

</td><td>

sys\_ws\_definition

</td><td>

UI16

</td></tr><tr><td>

Scripted Web Service

</td><td>

Scripted web services enable developers to create their own APIs on the ServiceNow AI Platform. Third-party applications use scripted web services to access records in ServiceNow tables.

 For more information, see [Web services](https://www.servicenow.com/docs/access?context=r_AvailableWebServices&version=australia&pubname=australia-api-reference&ft:locale=en-US).

</td><td>

sys\_web\_service

</td><td>

UI16

</td></tr><tr><td>

Table Transform Map

</td><td>

Transform maps contain a set of field maps that determine the relationships between fields in an import set and fields in an existing ServiceNow table, such as Incident \[incident\] or User \[sys\_user\]. After creating a transform map, you can reuse it to map data from another import set to the same table.

 For more information, see [Transform maps](https://www.servicenow.com/docs/access?context=c_CreatingNewTransformMaps&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

</td><td>

sys\_transform\_map

</td><td>

UI16

</td></tr></tbody>
</table>## Outbound integration files

Outbound integrations enable you to work with data that comes from the ServiceNow AI Platform and is sent to an external system or source.

<table id="table_zjf_y5k_ddc"><thead><tr><th>

File type

</th><th>

Description

</th><th>

Primary table

</th><th>

Primary editing experience

</th></tr></thead><tbody><tr><td>

Export Definition

</td><td>

Export definitions determine the data to include in an export set.

 For more information, see [Create an export definition](https://www.servicenow.com/docs/access?context=t_CreateAnExportDefinition&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

</td><td>

sys\_export\_definition

</td><td>

UI16

</td></tr><tr><td>

Export Set

</td><td>

Export sets define the data to export, as well as the export target to use when exporting data. For example, you can push data from an instance to an external file.

 For more information, see [Create an export set](https://www.servicenow.com/docs/access?context=t_CreateAnExportSet&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

</td><td>

sys\_export\_set

</td><td>

UI16

</td></tr><tr><td>

Export Target

</td><td>

Export targets specify the target file on a MID Server to which the export set data will be written.

 For more information, see [Create an export target](https://www.servicenow.com/docs/access?context=t_CreateAnExportTarget&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

</td><td>

sys\_export\_target

</td><td>

UI16

</td></tr><tr><td>

REST Message

</td><td>

A REST message is a record that stores details on how to interact with an external web service through REST. Use REST messages to send requests to a REST web service endpoint by creating a REST message record.

 For more information, see [Create a REST message](https://www.servicenow.com/docs/access?context=t_ConfiguringARESTMessage&version=australia&pubname=australia-api-reference&ft:locale=en-US).

</td><td>

sys\_rest\_message

</td><td>

UI16

</td></tr><tr><td>

Scheduled Data Export

</td><td>

Scheduled data exports specify a schedule when export sets will be run. A single export can be scheduled or regular intervals can be scheduled with support for including only delta records.

 For more information, see [Schedule an export](https://www.servicenow.com/docs/access?context=t_ScheduleAnExport&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

</td><td>

scheduled\_data\_export

</td><td>

UI16

</td></tr><tr><td>

SOAP Message

</td><td>

A SOAP message is a record that stores details on how to interact with an external web service through SOAP. SOAP messages define the remote endpoint, web services description language \(WSDL\), and authentication settings.

 For more information, see [SOAP message](https://www.servicenow.com/docs/access?context=c_SOAPMessage&version=australia&pubname=australia-api-reference&ft:locale=en-US).

</td><td>

sys\_soap\_message

</td><td>

UI16

</td></tr></tbody>
</table>## MID Server files

Work with management, instrumentation, and discovery \(MID\) Server files to facilitate communication and data movement between a single ServiceNow instance and external applications, data sources, and services.

<table id="table_dph_wxk_ddc"><thead><tr><th>

File type

</th><th>

Description

</th><th>

Primary table

</th><th>

Primary editing experience

</th></tr></thead><tbody><tr><td>

MID Server Application

</td><td>

The ServiceNow MID Server is a Java application that runs as a Windows service or UNIX daemon on a server in your local network.

 For more information, see [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td><td>

ecc\_agent\_application

</td><td>

UI16

</td></tr><tr><td>

MID Server Capability Value Test

</td><td>

MID Server capabilities define the specific functions of a MID Server within an IP address range. The capability value can be empty, a single value, or a \* \(wildcard\). You can use value tests to create capabilities that find devices using values without requiring exact string matching.

 For more information, see [MID Server capabilities](https://www.servicenow.com/docs/access?context=mid-server-capabilities&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

</td><td>

ecc\_agent\_capability\_value\_test

</td><td>

UI16

</td></tr><tr><td>

MID Server IP Range

</td><td>

Use MID Server to specify an IP range or the specific IP address of a target.

 For more information, see [Configure an IP address range for the MID Server](https://www.servicenow.com/docs/access?context=t_ConfigureMIDIPRange&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td><td>

ecc\_agent\_ip\_range

</td><td>

UI16

</td></tr><tr><td>

MID Server Property

</td><td>

Use MID Server properties to define the behavior of one or more MID Servers.

 For more information, see [MID Server properties](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td><td>

ecc\_agent\_property

</td><td>

UI16

</td></tr><tr><td>

MID Server Script File

</td><td>

Use a MID Server script file to synchronize to a connected MID Server.

 For more information, see [Attach a script file to a file synchronized MID Server](https://www.servicenow.com/docs/access?context=mid-server-script-attach&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td><td>

ecc\_agent\_script\_file

</td><td>

UI16

</td></tr><tr><td>

MID Server Script Include

</td><td>

Use MID Server script includes to make REST calls to cloud providers.

 For more information, see [CAPI classes in MID Server script includes](https://www.servicenow.com/docs/access?context=mid-server-script-includes&version=australia&pubname=australia-it-operations-management&ft:locale=en-US).

</td><td>

ecc\_agent\_script\_include

</td><td>

UI16

</td></tr></tbody>
</table>## Mobile files

Mobile App Builder is a configuration tool to build and manage screens and records that make up workflows within ServiceNow mobile apps. The organizational layout and navigation options in the Mobile App Builder facilitate a faster and more intuitive creation of ServiceNow mobile applications. Mobile Card Builder files enable you to edit the cards and templates used in applications for iOS and Android.

<table id="table_lly_xcl_ddc"><thead><tr><th>

File type

</th><th>

Description

</th><th>

Primary table

</th><th>

Primary editing experience

</th></tr></thead><tbody><tr><td>

Analytics preview

</td><td>

Analytics previews display previews of data visualization charts and single score reports in your launcher screen’s analytics section. Analytics previews enable you to verify that your data is tailored for mobile use and communicates the appropriate information for users.

 For more information, see [Create a mobile analytics preview](https://www.servicenow.com/docs/access?context=sg-mobile-dashboard-preview&version=australia&pubname=australia-mobile&ft:locale=en-US).

</td><td>

sys\_sg\_chart

</td><td>

Mobile App Builder

</td></tr><tr><td>

Calendar screen

</td><td>

Calendar screens display a calendar interface and records associated with the selected date. You can use a calendar screen to display dates that are relevant to application records. For example, you can display when tasks are due or when important events take place.

 For more information, see [Calendar screen](https://www.servicenow.com/docs/access?context=calendar-screen&version=australia&pubname=australia-mobile&ft:locale=en-US).

</td><td>

sys\_sg\_calendar\_screen

</td><td>

Mobile App Builder

</td></tr><tr><td>

Card

</td><td>

Cards are predetermined layouts that can show visuals, text, and data in mobile applications. You can define card elements and specify how elements are arranged within a card.

 For more information, see [Cards and icons](https://www.servicenow.com/docs/access?context=sg-cards-and-icons&version=australia&pubname=australia-mobile&ft:locale=en-US).

</td><td>

sys\_sg\_view\_config

</td><td>

Mobile Card Builder

</td></tr><tr><td>

Card template

</td><td>

Card templates are preconfigured layouts or frameworks that determine how information is displayed in mobile application cards. You can use the existing Mobile Card Builder card templates or create your own templates.

 For more information, see [Create a card template with Mobile Card Builder](https://www.servicenow.com/docs/access?context=mcb-create-template&version=australia&pubname=australia-mobile&ft:locale=en-US).

</td><td>

sys\_sg\_view\_template

</td><td>

Mobile Card Builder

</td></tr><tr><td>

Chart screen

</td><td>

Chart screens display data visualizations created in the Analytics Overview and are displayed in the analytics section of your launcher screen. Adding data visualizations helps you identify trends and turning points through indicator scores and visual representation.

 For more information, see [Chart screen](https://www.servicenow.com/docs/access?context=chart-screen&version=australia&pubname=australia-mobile&ft:locale=en-US).

</td><td>

sys\_sg\_chart\_screen

</td><td>

Mobile App Builder

</td></tr><tr><td>

Custom Map Screen

</td><td>

Custom map screens enable you to create maps that display content for specific records.

 For more information, see [Configure a map screen](https://www.servicenow.com/docs/access?context=sg-configure-map-screen&version=australia&pubname=australia-mobile&ft:locale=en-US).

</td><td>

sys\_sg\_custom\_map\_screen

</td><td>

Mobile App Builder

</td></tr><tr><td>

Function

</td><td>

Functions determine what actions users can perform in your mobile application. For example, you can create a navigation function that enables users to open a record from a list, or move from an employee user profile screen to a manager user profile screen.

 For more information, see [Mobile functions](https://www.servicenow.com/docs/access?context=sg-studio-mobile-button-types&version=australia&pubname=australia-mobile&ft:locale=en-US).

</td><td>

sys\_sg\_button

</td><td>

Mobile App Builder

</td></tr><tr><td>

Input form screen

</td><td>

Input form screens provide interfaces for users to enter information in mobile applications. For example, you can use input form screens to create or edit records, complete surveys, or any other situation where your users must enter information.

 For more information, see [Input form screen](https://www.servicenow.com/docs/access?context=parameter-input-screen&version=australia&pubname=australia-mobile&ft:locale=en-US).

</td><td>

sys\_sg\_parameter\_screen

</td><td>

Mobile App Builder

</td></tr><tr><td>

Launcher screen

</td><td>

Launcher screens serve as landing pages or home pages. Using a launcher screen, you can access screens in various formats, search, perform quick actions, and find user information.

 For more information, see [Launcher screens](https://www.servicenow.com/docs/access?context=sg-mobile-applet-launcher&version=australia&pubname=australia-mobile&ft:locale=en-US).

</td><td>

sys\_sg\_applet\_launcher

</td><td>

Mobile App Builder

</td></tr><tr><td>

List screen

</td><td>

List screens display a list of records. Records in list screens appear in a card format, showing a limited selection of the information for the record.

 For more information, see [List screen](https://www.servicenow.com/docs/access?context=list-screen&version=australia&pubname=australia-mobile&ft:locale=en-US).

</td><td>

sys\_sg\_list\_screen

</td><td>

Mobile App Builder

</td></tr><tr><td>

Map screen

</td><td>

Map screens display a map with locations that are associated with the records in a data item. For example, map screens can show your users where their assets are located, or which job locations they must travel to.

 For more information, see [Map screen](https://www.servicenow.com/docs/access?context=map-screen&version=australia&pubname=australia-mobile&ft:locale=en-US).

</td><td>

sys\_sg\_map\_screen

</td><td>

Mobile App Builder

</td></tr><tr><td>

Mobile app config

</td><td>

Mobile app configs enable you to create customized mobile experiences for the Now Mobile app and Mobile Agent app.

 For more information, see [Configuring the Mobile Platform](https://www.servicenow.com/docs/access?context=config-mobile-platform-landing&version=australia&pubname=australia-mobile&ft:locale=en-US).

</td><td>

sys\_sg\_native\_client

</td><td>

Mobile App Builder

</td></tr><tr><td>

Mobile web screen

</td><td>

Mobile web screens open an external URL or a relative URL within your instance.

 For more information, see [Mobile web screen](https://www.servicenow.com/docs/access?context=url-screen&version=australia&pubname=australia-mobile&ft:locale=en-US).

</td><td>

sys\_sg\_browser\_screen

</td><td>

Mobile App Builder

</td></tr><tr><td>

Record screen

</td><td>

Record screens display content for a specific single record. You can configure functions on record screens to enable users to make edits and perform actions.

 For more information, see [Record screen](https://www.servicenow.com/docs/access?context=form-screen&version=australia&pubname=australia-mobile&ft:locale=en-US).

</td><td>

sys\_sg\_form\_screen

</td><td>

Mobile App Builder

</td></tr></tbody>
</table>## Natural Language Understanding \(NLU\) files

Natural Language Understanding \(NLU\) is a model that enables a computer to interpret, analyze, and derive meaning from human language. By creating NLU files, you build and train your application's NLU model to help it recognize user input, or utterances, and determine the corresponding user or system actions.

<table id="table_zbg_bsm_ddc"><thead><tr><th>

File type

</th><th>

Description

</th><th>

Primary table

</th><th>

Primary editing experience

</th></tr></thead><tbody><tr><td>

NLU Model

</td><td>

A Natural Language Understanding \(NLU\) model is the collection of utterance examples and their associated intents and entities that an application uses as a reference to infer intents and entities in a new utterance.

 For more information, see [Natural Language Understanding](https://www.servicenow.com/docs/access?context=nlu-landing&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

</td><td>

sys\_nlu\_model

</td><td>

UI16

</td></tr></tbody>
</table>## Properties files

Properties files are configurable parameters that enable you to change the behavior of an application without hard-coding the values directly into scripts.

<table id="table_zmh_xbs_ddc"><thead><tr><th>

File type

</th><th>

Description

</th><th>

Primary table

</th><th>

Primary editing experience

</th></tr></thead><tbody><tr><td>

Message

</td><td>

Messages are the text values used in informational messages, confirmation messages, error messages, and other types of system messages in your application.

 For more information, see [Message table](https://www.servicenow.com/docs/access?context=r_MessageTable&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td><td>

sys\_ui\_message

</td><td>

UI16

</td></tr><tr><td>

System Property

</td><td>

A system property is a way to store important values for an application, like settings or configurations, that you might need in different scripts. Instead of writing these values directly into the script \(hard-coding\), you can store them as system properties. Creating system properties enables you to update and edit properties in one place, without having to change each script that references the values manually.

 For more information, see [What are application properties?](https://developer.servicenow.com/dev.do#!/learn/learning-plans/xanadu/new_to_servicenow/app_store_learnv2_automatingapps_xanadu_what_are_application_properties) and [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td><td>

sys\_properties

</td><td>

UI16

</td></tr><tr><td>

System Property Category

</td><td>

A system property category creates the page layout for an application's system properties. The system property category page contains all the application properties in a single location.

 For more information, see [Create a system property category](https://developer.servicenow.com/dev.do#!/learn/learning-plans/xanadu/new_to_servicenow/app_store_learnv2_automatingapps_xanadu_create_a_system_property_category).

</td><td>

sys\_properties\_category

</td><td>

UI16

</td></tr></tbody>
</table>## Reporting files

Reporting files enable you to create and distribute reports that show the current state of instance data, such as the number of open incidents of each priority.

<table id="table_v1m_scs_ddc"><thead><tr><th>

File type

</th><th>

Description

</th><th>

Primary table

</th><th>

Primary editing experience

</th></tr></thead><tbody><tr><td>

Chart Colors

</td><td>

Chart colors assign a consistent color to a grouping or stacking value in reports and dashboards. The color stays the same across reports regardless of the order of the values.

 For more information, see [Chart colors](https://www.servicenow.com/docs/access?context=c_ChartColors&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

</td><td>

sys\_report\_chart\_color

</td><td>

UI16

</td></tr><tr><td>

Color Definition

</td><td>

Color definitions enable you to maintain consistency in the platform's look and feel by applying defined colors to various UI components, such as buttons, backgrounds, text, and other elements.

 For more information, see [Define system colors for analytics](https://www.servicenow.com/docs/access?context=t_DefiningSystemColors&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

</td><td>

sys\_report\_color

</td><td>

UI16

</td></tr><tr><td>

Dashboard

</td><td>

Dashboards enable you to display performance analytics, reporting, and other widgets on a single screen. You can use dashboards to create a story with data that you can share with other users.

 For more information, see [Create and use dashboards](https://www.servicenow.com/docs/access?context=create-and-edit-dashboards&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

</td><td>

pa\_dashboards

</td><td>

Dashboard Builder

</td></tr><tr><td>

Metric Definition

</td><td>

A metric measures and evaluates the effectiveness of an application process. For example, a metric could measure the effectiveness of the incident resolution process by calculating how long it takes to resolve an incident. You can define metrics and create reports and dashboards using your metrics definitions.

 For more information, see [Metrics](https://www.servicenow.com/docs/access?context=c_MetricDefinitionSupport&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and [Define a metric](https://www.servicenow.com/docs/access?context=create-metric&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td><td>

metric\_definition

</td><td>

UI16

</td></tr><tr><td>

Range

</td><td>

Ranges are defined data intervals that are used in bar and pie charts to segment the data into logical groups. For example, you might create a range to see how many tasks were completed well within the service level agreement \(SLA\) and how many tasks elapsed during the SLA.

 For more information, see [Report ranges](https://www.servicenow.com/docs/access?context=c_ReportRanges&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

</td><td>

sys\_report\_range

</td><td>

UI16

</td></tr><tr><td>

Report

</td><td>

Reports are tools used to display data visually, enabling you to gain insights, track performance, and make data-driven decisions. For example, you can create and distribute reports that show the current state of instance data, such as the number of open incidents of each priority.

 For more information, see [Exploring reporting](https://www.servicenow.com/docs/access?context=exploring-reporting&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

</td><td>

sys\_report

</td><td>

UI16

</td></tr><tr><td>

Scheduled Email of Report

</td><td>

Scheduled emails of reports enable you to generate and distribute scheduled reports via email.

 For more information, see [Schedule emails of Core UI reports](https://www.servicenow.com/docs/access?context=t_ScheduleAReport&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

</td><td>

sysauto\_report

</td><td>

UI16

</td></tr></tbody>
</table>## Schedules files

Schedules can help you manage the entire life cycle of your application, from setting up maintenance schedules to defining durations and risks for operations.

<table id="table_nnz_pfs_ddc"><thead><tr><th>

File type

</th><th>

Description

</th><th>

Primary table

</th><th>

Primary editing experience

</th></tr></thead><tbody><tr><td>

Blackout Schedule

</td><td>

A blackout schedule is a time during which certain activities, such as changes or updates, are restricted to avoid disruptions. You can set up blackout schedules to confirm that critical business operations remain unaffected during high-impact or sensitive times, such as holidays, end-of-quarter financial processing, or other key business events.

 For more information, see [Create blackout and maintenance schedules in Change Management](https://www.servicenow.com/docs/access?context=t_CreateBlkoutMaintSched&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

</td><td>

cmn\_schedule\_blackout

</td><td>

UI16

</td></tr><tr><td>

Maintenance Schedule

</td><td>

A maintenance schedule is a time during which planned maintenance activities, such as changes and updates, should take place. Maintenance schedules usually occur during low-impact times to minimize disruptions to business operations.

 For more information, see [Create blackout and maintenance schedules in Change Management](https://www.servicenow.com/docs/access?context=t_CreateBlkoutMaintSched&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

</td><td>

cmn\_schedule\_maintenance

</td><td>

UI16

</td></tr><tr><td>

Relative Duration

</td><td>

Relative durations are a duration type available in ServiceNow Studio that you can select when defining service level agreements \(SLAs\). Relative durations enable you to calculate how much time you have to work on an SLA by defining the amount of time to wait. For example, you can define a relative duration as three business days by 4pm.

 For more information, see [Define a relative duration](https://www.servicenow.com/docs/access?context=t_DefineARelativeDuration&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and [Use a relative duration](https://www.servicenow.com/docs/access?context=t_UseARelativeDuration&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td><td>

cmn\_relative\_duration

</td><td>

UI16

</td></tr><tr><td>

Risk Conditions

</td><td>

A risk condition is a set of rules or criteria that evaluate the potential risks associated with scheduling activities, such as changes, updates, or maintenance tasks. You can define risk conditions and run risk calculations using The Best Practice - Change Risk Calculator.

 For more information, see [Add or modify risk and impact conditions](https://www.servicenow.com/docs/access?context=define-risk-and-impact-conditions&version=australia&pubname=australia-it-service-management&ft:locale=en-US) and [Risk conditions and calculation](https://www.servicenow.com/docs/access?context=change-risk-assess-detect-conflict&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

</td><td>

risk\_conditions

</td><td>

UI16

</td></tr><tr><td>

Schedule

</td><td>

Schedules are rules that include or exclude time for various actions or tasks.

 For more information, see [Schedules](https://www.servicenow.com/docs/access?context=c_UseSchedules&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and [Define a schedule](https://www.servicenow.com/docs/access?context=t_DefineASchedule&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td><td>

cmn\_schedule

</td><td>

UI16

</td></tr></tbody>
</table>## Security files

Security files enable you to control who has access to application data and help prevent accidental modification or deletion of data.

<table id="table_p1l_pjs_ddc"><thead><tr><th>

File type

</th><th>

Description

</th><th>

Primary table

</th><th>

Primary editing experience

</th></tr></thead><tbody><tr><td>

Access Control

</td><td>

Access control, or access control lists \(ACLs\), restrict access to data by requiring users to pass a set of requirements before they can interact with application content.

 For more information, see [Explore Access Control Lists](https://www.servicenow.com/docs/access?context=exploring-access-control-list&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td><td>

sys\_security\_acl

</td><td>

UI16

</td></tr><tr><td>

Public Pages

</td><td>

Public pages enable users to see the application content without logging in.

 For more information, see [Make UI pages public or private](https://www.servicenow.com/docs/access?context=t_MakeAPagePublic&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td><td>

sys\_public

</td><td>

UI16

</td></tr><tr><td>

Role

</td><td>

Roles determine what application access is granted to which users.

 For more information, see [Managing roles](https://www.servicenow.com/docs/access?context=ua-creating-roles&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and [Determine What Roles to Create](https://developer.servicenow.com/dev.do#!/learn/courses/vancouver/app_store_learnv2_aescreateappfromscratch_vancouver_create_an_app_from_scratch_with_app_engine_studio/app_store_learnv2_aescreateappfromscratch_vancouver_secure_apps_and_data/app_store_learnv2_aescreateappfromscratch_vancouver_determining_what_roles_to_create).

</td><td>

sys\_user\_role

</td><td>

UI16

</td></tr></tbody>
</table>## Server development files

Server development files manage back-end processes in ServiceNow Studio to verify that data is handled appropriately and securely.

<table id="table_dnf_rks_ddc"><thead><tr><th>

File type

</th><th>

Description

</th><th>

Primary table

</th><th>

Primary editing experience

</th></tr></thead><tbody><tr><td>

Business Rule

</td><td>

A business rule is a server-side script that runs when a record is displayed, inserted, updated, or deleted, or when a table is queried. You can establish server-side conditions to determine when a business rule script should run and what record operations the business rule applies to.

 For more information, see [Classic Business rules](https://www.servicenow.com/docs/access?context=c_BusinessRules&version=australia&pubname=australia-api-reference&ft:locale=en-US).

</td><td>

sys\_script

</td><td>

UI16

</td></tr><tr><td>

Data Policy

</td><td>

Data policies enable you to enforce data consistency by setting mandatory and read-only states for fields. Data policies are similar to UI policies, but UI policies only apply to data entered on a form through the standard browser. Data policies can apply rules to all data entered into the system, including data brought in through import sets or web services and data entered through the mobile UI.

 For more information, see [Data policy](https://www.servicenow.com/docs/access?context=c_DataPolicy&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td><td>

sys\_data\_policy2

</td><td>

UI16

</td></tr><tr><td>

Event Registration

</td><td>

Events are special records that the system uses to log when certain conditions occur and to take some kind of action in response to the conditions. By registering an event, you can define properties about the event and associate the event with the business rule that fires the event.

 For more information, see [Register an event](https://www.servicenow.com/docs/access?context=t_RegisterAnEvent&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

</td><td>

sysevent\_register

</td><td>

UI16

</td></tr><tr><td>

Extension Instance

</td><td>

An extension instance is a registered instance of a scripted extension point that links a script include with a scripted extension point. When you want to define custom logic or methods without affecting your original code, you may consider using an extension instance. An extension instance enables you to encapsulate specific logic and functions, making it easier for you to manage, update, and debug your code.

 For more information, see [Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=australia&pubname=australia-api-reference&ft:locale=en-US).

</td><td>

sys\_extension\_instance

</td><td>

UI16

</td></tr><tr><td>

Extension Point

</td><td>

An extension point designates where custom script logic can be incorporated into your code, so that you can integrate customizations and new features without altering the existing code for your application. Data or objects returned by an extension point must conform to requirements that are specified by the application creator.

 For more information, see [Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=australia&pubname=australia-api-reference&ft:locale=en-US).

</td><td>

sys\_extension\_point

</td><td>

UI16

</td></tr><tr><td>

Fix Script

</td><td>

Fix scripts are server-side JavaScript that run after a custom application is installed or upgraded. You can include fix scripts to make changes that are necessary for the data integrity or product stability of an application.

 For more information, see [Fix scripts](../../applications/concept/c_FixScripts.md) and [Create a fix script](../../applications/task/t_CreateFixScripts.md).

</td><td>

sys\_script\_fix

</td><td>

UI16

</td></tr><tr><td>

Scheduled Script Execution

</td><td>

Scheduled script executions, also known as scheduled jobs, are automated, server-side script logic that execute at a specific time or on a recurring basis. Use scheduled script executions when application processes require script logic to be executed based on a time schedule.

 For more information, see [What is a Scheduled Script Execution?](https://developer.servicenow.com/dev.do#!/learn/courses/washingtondc/app_store_learnv2_automatingapps_washingtondc_automating_application_logic/app_store_learnv2_automatingapps_washingtondc_scheduled_script_executions_and_events/app_store_learnv2_automatingapps_washingtondc_what_is_a_scheduled_script_execution) and [Creating a Scheduled Script Execution](https://developer.servicenow.com/dev.do#!/learn/courses/washingtondc/app_store_learnv2_automatingapps_washingtondc_automating_application_logic/app_store_learnv2_automatingapps_washingtondc_scheduled_script_executions_and_events/app_store_learnv2_automatingapps_washingtondc_creating_a_scheduled_script_execution).

</td><td>

sysauto\_script

</td><td>

UI16

</td></tr><tr><td>

Script Action

</td><td>

A script action is server-side JavaScript that is executed when a particular event is generated.

 For more information, see [Script actions](https://www.servicenow.com/docs/access?context=r_ScriptActions&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

</td><td>

sysevent\_script\_action

</td><td>

UI16

</td></tr><tr><td>

Script Include

</td><td>

Script includes are reusable, server-side JavaScript that define a function or class and execute only when explicitly called.

 For more information, see [Script includes](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=australia&pubname=australia-api-reference&ft:locale=en-US) and [Script Includes](https://developer.servicenow.com/dev.do#!/learn/courses/washingtondc/app_store_learnv2_scripting_washingtondc_scripting_in_servicenow/app_store_learnv2_scripting_washingtondc_server_side_scripting/app_store_learnv2_scripting_washingtondc_script_includes).

</td><td>

sys\_script\_include

</td><td>

UI16

</td></tr><tr><td>

UI Action

</td><td>

UI actions are configurations that define the behavior of buttons, links, or context menu items in your application, specifying how they interact with the server-side database.

 For more information, see [Defining UI actions](https://www.servicenow.com/docs/access?context=c_UIActions&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and [Create a UI action](https://www.servicenow.com/docs/access?context=t_EditingAUIAction&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td><td>

sys\_ui\_action

</td><td>

UI16

</td></tr></tbody>
</table>## UI Builder files

UI Builder files enable you to build pages for workspaces generated in ServiceNow Studio, or custom web experiences using Next Experience Components and custom web components.

<table id="table_dnv_3wx_j3c"><thead><tr><th>

File type

</th><th>

Description

</th><th>

Primary table

</th><th>

Primary editing experience

</th></tr></thead><tbody><tr><td>

Components

</td><td>

Components are used in the UI Builder to build pages. Components have an interface that an end user can view and interact with. Components can talk to each other through events and properties. Commonly used components include Heading, Image, List, Form, and Button.For more information, see [Customize UI Builder pages using components](../../../administer/ui-builder/concept/work-components.md).

</td><td>

sys\_ux\_macroponent

</td><td>

UI16

</td></tr><tr><td>

Controllers

</td><td>

Controllers are a type of data resource that includes data and event logic and enables component presets. Controllers are added automatically when using a page template. There are two types of controllers:

-   Data controllers contain data resources and can be manually added to a page.
-   UI controllers are added to pages when using page templates and can't be added manually.

For more information, see [Bind data to UI Builder pages using controllers \(advanced feature\)](../../../administer/ui-builder/concept/controllers.md#).

</td><td>

sys\_ux\_controller

</td><td>

UI16

</td></tr><tr><td>

Experiences

</td><td>

Experiences are a collection of web pages for users to interact with an application.For more information, see [Create an experience for UI Builder](../../../administer/ui-builder/task/create-experience.md).

</td><td>

sys\_ux\_page\_registry

</td><td>

UI16

</td></tr><tr><td>

Page collections

</td><td>

Page collections are groups of pages that can be reused in experiences within tabs or modals.For more information, see [Page collections](../../../administer/ui-builder/concept/page-collections.md).

</td><td>

sys\_ux\_extension\_point

</td><td>

UI16

</td></tr><tr><td>

UI interactions

</td><td>

UI interactions are reusable flows that combine UI elements and logic into a single unit that you can trigger from component events in UI Builder. They help you avoid repeating the same wiring across multiple pages and make your designs easier to maintain.For more information, see [UI interactions](../../../administer/ui-builder/concept/uib-ui-interactions.md).

</td><td>

sys\_ui\_interaction

</td><td>

UI16

</td></tr></tbody>
</table>## User interface files

User interface files define layouts for pages, modules, and tools that users interact with. Some examples of user interface files include catalog items, guided tours, and themes.

<table id="table_fzd_fms_ddc"><thead><tr><th>

File type

</th><th>

Description

</th><th>

Primary table

</th><th>

Primary editing experience

</th></tr></thead><tbody><tr><td>

Application Menu

</td><td>

An application menu is a grouping of modules as they appear in the application navigator \(UI16\) or **All** menu \(Next Experience\). You can refer to an Application menu as simply an application.

 For more information, see [Enable or disable an application menu or module](https://www.servicenow.com/docs/access?context=t_EnDisableAppMenuOrMod&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td><td>

sys\_app\_application

</td><td>

UI16

</td></tr><tr><td>

Assessment Metric

</td><td>

In the Assessments application, a metric is a trait or value used to evaluate assessable records.

 For more information, see [Assessment metrics](https://www.servicenow.com/docs/access?context=c_AssessmentMetrics&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td><td>

asmt\_metric

</td><td>

Survey Designer

</td></tr><tr><td>

Catalog

</td><td>

A catalog is a section of the Service Catalog where users can order items and services. A catalog is like a portal where your users can request catalog items such as service and product offerings. For example, a hardware catalog may have items to request a new keyboard or a new mouse device.

 For more information, see [Exploring Service Catalog](https://www.servicenow.com/docs/access?context=exploring-service-catalog&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td><td>

sc\_catalog

</td><td>

Catalog Builder

</td></tr><tr><td>

Catalog Item

</td><td>

A catalog item is essentially a form that describes a good or service you can order in the service catalog. For example, if you're requesting time off using a catalog item, you may enter your name and requested dates off on the form.

 For more information, see [Service Catalog items](https://www.servicenow.com/docs/access?context=c_IntroductionToCatalogItems&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td><td>

sc\_cat\_item

</td><td>

UI16

</td></tr><tr><td>

Context Menu

</td><td>

The context menu for a form provides controls for a list or form based on the table and user access rights.

 For more information, see [Form context menu](https://www.servicenow.com/docs/access?context=c_FormContextMenu&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td><td>

sys\_ui\_context\_menu

</td><td>

UI16

</td></tr><tr><td>

Embedded Help

</td><td>

Embedded Help provides targeted help content to a user in a UI page, based on their role. Some embedded help content comes with the base instance. Your organization can add or replace embedded help content.

 For more information, see [Embedded Help](https://www.servicenow.com/docs/access?context=embedded-help&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td><td>

sys\_embedded\_help\_content

</td><td>

UI16

</td></tr><tr><td>

Embedded Help Qualifier

</td><td>

An Embedded Help qualifier is an identifier that helps a ServiceNow instance identify the correct Embedded Help topic when there could be more than one topic for a UI page.

 For more information, see [Use qualifiers in Embedded Help](https://www.servicenow.com/docs/access?context=embedded-help-qualifiers&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td><td>

sys\_embedded\_help\_qualifier

</td><td>

UI16

</td></tr><tr><td>

Guided Tour

</td><td>

Guided Tours contain a series of interactive steps that help users complete online tasks within their browser window to help train and onboard users working in a ServiceNow app.

 For more information, see [Guided Tours](https://www.servicenow.com/docs/access?context=guided-tours&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td><td>

sys\_embedded\_tour\_guide

</td><td>

UI16

</td></tr><tr><td>

List

</td><td>

Lists display a set of records from a table, and can be filtered to refine the contents. For example, you can filter the Task list to show only Unassigned tasks. Each row in a list is a record, and each column is a field from the record.

 For more information, see [Lists in the classic environment](https://www.servicenow.com/docs/access?context=c_UseLists&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) and [ServiceNow AI Platform® list administration](https://www.servicenow.com/docs/access?context=p_ListAdministration&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td><td>

sys\_ui\_list

</td><td>

UI16

</td></tr><tr><td>

List Control

</td><td>

List controls are settings that specify which features are available on a list, such as the **New** and **Edit** buttons.

 For more information, see [Configure list controls](https://www.servicenow.com/docs/access?context=t_ConfigureListControls&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td><td>

sys\_ui\_list\_control

</td><td>

UI16

</td></tr><tr><td>

Map Page

</td><td>

Map pages display ServiceNow data graphically on a Google map page based on location data that you provide.

 For more information, see [Map pages](https://www.servicenow.com/docs/access?context=c_MapPages&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td><td>

cmn\_map\_page

</td><td>

UI16

</td></tr><tr><td>

Module

</td><td>

A module is any link in the application navigator \(UI16\) or **All** menu \(Next Experience\) that opens a page in the content frame or in a separate tab or window.

 For more information, see [Modules](https://developer.servicenow.com/dev.do#!/learn/courses/xanadu/app_store_learnv2_buildneedit_xanadu_build_the_needit_application/app_store_learnv2_buildneedit_xanadu_create_the_needit_application_and_application_files/app_store_learnv2_buildneedit_xanadu_modules) on the Developer Site.

</td><td>

sys\_app\_module

</td><td>

UI16

</td></tr><tr><td>

Portal

</td><td>

Portals provide users with access to the services, information, and resources they need to get their work done quickly and efficiently. Work with portals in UI Builder.

 For more information, see [Configure UI Builder portal experiences](../../../administer/ui-builder/concept/ui-builder-portal-settings.md).

</td><td>

sys\_ux\_page\_registry

</td><td>

UI Builder

</td></tr><tr><td>

Record Producer

</td><td>

Record producers are catalog items that enable users to create task-based records, such as incident records, from the service catalog.

 For more information, see [Record Producer](https://www.servicenow.com/docs/access?context=c_RecordProducer&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td><td>

sc\_cat\_item\_producer

</td><td>

Catalog Builder - Record producer

</td></tr><tr><td>

Related List

</td><td>

Related lists appear on forms and show records in tables that have relationships to the current record.

 For more information, see [Related lists](https://www.servicenow.com/docs/access?context=c_RelatedLists&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td><td>

sys\_ui\_related\_list

</td><td>

UI16

</td></tr><tr><td>

Schedule Page

</td><td>

A schedule page is a record that contains a collection of scripts that enable custom generation of a calendar or timeline display.

 For more information, see [Schedule Pages](https://www.servicenow.com/docs/access?context=c_SchedulePages&version=australia&pubname=australia-api-reference&ft:locale=en-US).

</td><td>

cmn\_schedule\_page

</td><td>

UI16

</td></tr><tr><td>

Service Portal

</td><td>

Service Portal enables you to build a mobile-friendly self-service portal experience for your employees or customers.

 For more information, see [Service Portal](https://www.servicenow.com/docs/access?context=c_ServicePortal&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td><td>

sp\_portal

</td><td>

Service Portal

</td></tr><tr><td>

Style

</td><td>

Styles define properties such as font size, border, and alignment for text that appears in your app.

 For more information, see [Create a Next Experience style](https://www.servicenow.com/docs/access?context=create-next-experience-style&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) and [Style - Scoped, Global](https://www.servicenow.com/docs/access?context=StyleBothAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US).

</td><td>

sys\_ui\_style

</td><td>

UI16

</td></tr><tr><td>

Template

</td><td>

Templates enable administrators to create reusable content. For example, an email template could have a reusable subject line and message body for email notifications. Form templates simplify the process of submitting new records by populating fields automatically.

 For more information, see [Email templates](https://www.servicenow.com/docs/access?context=c_EmailTemplates&version=australia&pubname=australia-platform-administration&ft:locale=en-US), [Using form templates](https://www.servicenow.com/docs/access?context=c_Templates&version=australia&pubname=australia-platform-administration&ft:locale=en-US), and [Page templates](https://www.servicenow.com/docs/access?context=r_PageTemplates&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td><td>

sys\_template

</td><td>

UI16

</td></tr><tr><td>

Theme

</td><td>

Themes enable you to tailor the visual experience for your users, helping to update the look and feel to be more like your brand.

 For more information, see [Working with themes in Next Experience](https://www.servicenow.com/docs/access?context=next-experience-theming&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td><td>

sys\_ui\_theme

</td><td>

UI16

</td></tr><tr><td>

Timeline Page

</td><td>

Use timeline pages to track any activity bounded by two dates, such as change request start and end dates, or incident open and close dates.

 For more information, see [Timeline pages](https://www.servicenow.com/docs/access?context=c_TimelinePages&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td><td>

cmn\_timeline\_page

</td><td>

UI16

</td></tr><tr><td>

View Rule

</td><td>

Use view rules to force a specified view when users access a page or application.

 For more information, see [Create a view rule](https://www.servicenow.com/docs/access?context=t_CreateAViewRule&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td><td>

sysrule\_view

</td><td>

UI16

</td></tr><tr><td>

Workspace

</td><td>

Workspaces are spaces that provide agents and managers with tools to help answer customer questions and resolve customer problems. Workspaces are primarily used for request and fulfillment processes, such as a service desk to manage tickets.

 For more information, see [Configurable Workspace UI](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) and [Workspace Builder](../../workspace-builder/concept/workspace-builder-landing.md).

</td><td>

sys\_ux\_page\_registry

</td><td>

Workspace Builder

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow Studio reference](../concept/servicenow-studio-reference.md)

