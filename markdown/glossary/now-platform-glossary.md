---
title: ServiceNow AI Platform glossary
description: Learn about the terms and concepts related to the ServiceNow AI Platform.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 27
keywords: [glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms]
---

# ServiceNow AI Platform glossary

Learn about the terms and concepts related to the ServiceNow AI Platform.

## A

Glossary terms are grouped alphabetically.

### Accordion

Gives users the ability to reveal and hide relevant sections of content in collapsible categories.

**Note:** This component is only available for use in code and will not appear in UI Builder.

### account

An account is a supported external customer. An account can be a customer account, a partner account, or both.

### account hierarchy

An account hierarchy represents the legal entity structure of the accounts and their relationships, the account's customers, assets, and service entitlements.

### action

Actions in UI Builder are specifically activity on a page or within a page component. Events and event handlers are used to add actions. For example, add a button component to a page and then add an event handler to apply an action for the button, such as opening a web page.

### activities

Reusable set of instructions that are designed for an automation on the Design surface of RPA Desktop Design Studio.

### agent-intiated

A chat that the agent starts.

### Agentic system

An agentic system is a type of software or AI that perceives its environment, makes decisions that are based on that perception, and takes actions to achieve specific goals, often with minimal human intervention. An agentic system can learn, adapt, and operate independently to solve problems or perform tasks.

### alert

Custom notifications that are sent to a user or a group. These notifications are generated for robots, schedules, process jobs, and other RPA Hub related tables.

### AMB channel

The Asynchronous Message Bus \(AMB\) channel is utilized to notify unattended robots, when a change is made to bot processes in RPA Hub. Consequently, all the robots subscribed to the designated channel receive a notification. For example, when Start Process is initiated from RPA Hub, a message is sent to the selected robot via an AMB channel, then the robot receives the message to start the automation process.

### app shell

App shells are the static elements of a web experience \(for example, the header, footer, and menu navigation\) that stays with the end user as they navigate throughout the experience. App shells are primarily used and supported in Workspace and Portal experiences.

### Application template

Provides predefined data, experience, logic and automation, and security to support a certain use case. For example, the Travel Request template provides application content for submitting and approving employee travel requests.

For more information on the available templates, see [Available templates](https://www.servicenow.com/docs/access?context=template-library&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

### assignment workbench

A feature, part of case routing, that uses configurable criteria, such as skills and availability, to evaluate the agents in a selected group and provide an overall ranking of how well they can handle certain cases. Managers can view these results and click one button to assign a task.

### asynchronous chat

This feature in Engagement Messenger empowers support agents and end users to engage in conversations at their own pace, without the constraint of being online simultaneously. Through notifications, the user is notified about the new messages received.

### Attachment Framework

A set of REST APIs that enable uploading or downloading attachments to or from a ServiceNow instance. This helps in publishing and downloading automation packages that are built in RPA Desktop Design Studio to the ServiceNow instance \(RPA Hub\) that run on attended or unattended robots.

### Attended Robot

Software agent that is installed on a Windows machine and executes attended automations.

### automated breakdown

Automated breakdowns are based on a breakdown source, which is a set of records from a table. The breakdown maps these records, known as breakdown elements, with fields on tables that indicators collect scores from. Scores collected from mapped tables can then be grouped and filtered based on the values in the mapped fields and the breakdown elements.

### automated indicator

An automated indicator uses an indicator source as its data set. The indicator source specifies a table or database view, conditions for filtering records from that source, and the frequency at which you expect to display the data. The indicator applies an aggregator and optional conditions to this data. The indicator also specifies a data collection job and any breakdowns to apply.

**Related topics**  


[indicator \(KPI\)](now-platform-glossary.md#)

[database view](now-platform-glossary.md#)

### automation

Robotic Process Automation \(RPA\) is a software technology that makes it easy to build, deploy, and manage robots that emulate human actions interacting with digital systems and software.

## B

Glossary terms are grouped alphabetically.

### binding

See data binding.

### bot process

A predefined sequence of actions that a robot follows to accomplish a specific task or achieve a particular goal in RPA Hub. You can assign and schedule a package that will be executed by the software agent. You can add other details that pertain to the bot process, such as business applications, credential groups, process robot credentials, process parameters, attended users, or groups.

### bot process configuration

A record that contains the bot process settings. The bot process configuration record is mapped to a bot process record in RPA Hub. It is a one to one mapping.

### bot response

The type of response that the virtual agent \(bot\) gives to the customer. For example: a card response displays information from a record with rich content such as a video or image.

### breakdown

A grouping or a filter of indicator scores that is based on a qualitative attribute such as Priority, Category, or Assignment Group.

**Related topics**  


[breakdown element](now-platform-glossary.md#)

[indicator \(KPI\)](now-platform-glossary.md#)

### breakdown element

The values for a breakdown. For example, the Priority breakdown may have the elements Critical, High, and Low.

**Related topics**  


[breakdown](now-platform-glossary.md#)

### breakdown mapping

A breakdown mapping specifies the relationships between breakdowns and indicator sources. A breakdown mapping references either a field on the indicator source or a script that queries the indicator source.

### breakdown source

A set of records from a table or database view that constitute the unique values, or breakdown elements, of a breakdown source. Can be a bucket group. Multiple breakdowns can use the same breakdown source.

**Related topics**  


[breakdown](now-platform-glossary.md#)

[breakdown element](now-platform-glossary.md#)

[bucket group](now-platform-glossary.md#)

### breakpoint

Option in RPA Desktop Design Studio that you set to stop or pause the automation execution for debugging purposes.

### bucket group

Gathers continuous data into discrete groups when there is no table field that can serve as breakdown elements. For example, a bucket group might take differences between timestamps and divide them up into hourly periods.

### business location

The business location enables you to model internal and external organizational structures to support customers and provide agents the right level of visibility into customer data.

## C

Glossary terms are grouped alphabetically.

### Callback

Users can request an immediate callback or schedule a voice or video callback from an agent during a chat on Virtual Agent or Engagement Messenger. Additionally, users can easily reschedule or cancel their callback requests.

### candidate case

A case created by a customer service agent to flag an issue that may be a wider problem impacting multiple customers. An agent can create a major case candidate by promoting an existing customer service case with a reported issue, or creating a major case candidate directly.

### case

A record that is used to track and manage a specific customer issue, request, or incident. It is commonly used in resolving issues through customer support and helpdesk systems.

### case routing

A feature that uses matching rules and assignment rules to identify cases with specific case attributes and route them to the best-equipped customer service agent. Part of Engagement Messenger.

### case synchronization

A major issue management system property that allows for user-specified fields from the major case to be synchronized with each of the associated child cases.

### case task

Tasks created for additional work that needs to be completed as part of resolving a customer service case, stored in the Case Task \[sn\_customerservice\_task\] table. Frequently assigned to users such as middle or back office agents.

### child case

Cases that are associated with a major case, created one-to-one for each business account \(B2B\) or consumer \(B2C\) impacted by the major case issue. It contains customer-specific information for each customer affected by the major case issue.

### classification

In Document Intelligence, the process of categorizing documents and document pages based on their type.

### client script

Client-side JavaScript that interact with components and client state parameters on a page. Client scripts are mapped to events as event handlers in UI Builder.

### client state parameter

Page variables that are defined for a page to store a piece of data \(a client state\) only for that page. For example, create three client state parameters to store the input needed to create a record and specify when to refresh the list. Page variables can be updated using client scripts and events to make a page dynamic.

### component \(UI Builder\)

Use the UI Builder library of components to build pages. Components have an interface that an end user can view and interact with. Components can talk to each other through events and properties. Commonly used components include Heading, Image, List, Form, and Button.

### component

Reusable blocks that are used for designing automations and to abstract functionality in RPA Desktop Design Studio.

### component id

Used to reference a component when adding a script or binding data to the component. A component ID is automatically created \(based on the component label\) when you add a component to a page, but the component ID can be edited.

### component preset

Use to apply predefined configuration values and event mappings to components. Presets apply prebuilt configurations to component properties and events handlers. Presets are only available for certain components.

### component properties

Available in the Configuration panel and used to configure a component. Each component has unique properties. Component properties are specified within each tab on the Configuration panel: Config, Style, and Event. Some components have presets available. Use the component presets to set component properties automatically.

### confidence score

A numerical value assigned to a recommendation by Document Intelligence indicating its certainty about the extracted information. The higher the score, the more reliable the recommendation.

### Configurable Cards

Option to add a custom card to the Engagement Messenger homescreen. Using Configurable Cards, admins can display the following custom features as a card:

-   Portal pages or catalog items
-   Links to external website
-   Data from any table

### connector

Connector that connects to various data sources and tools to create automation in RPA Desktop Design Studio.

### contract

A contract contains customer-specific information like the tenure of the contract, contract line details, and the net and covered products. They also hold the after-sales service information that the customers are eligible to receive.

### contributing indicator

An indicator that is used in the formula of a formula indicator. A contributing indicator can be an automated or a formula indicator.

### controller

A type of data resource that includes data and event logic and enables component presets. Controllers are added automatically when using a page template. There are two types of controllers:

-   Data controllers contain data resources and can be manually added to a page
-   UI controllers are added to pages when using page templates and can't be added manually. Creating controllers isn't supported currently.

### conversational integration

A chat with a virtual agent that engages the customer in a friendly way that simulates a normal human conversation. This conversation takes place in a 3rd party application such as Facebook or Google messenger.

### customer

A customer is an account or a contact. In business-to-business \(B2B\) scenarios, a customer is typically an account, while in business-to-consumer \(B2C\) scenarios, a customer is typically a consumer.

### customer access management

Customer access management supports multiple related parties in handling cases, sold products, and install bases by providing them with varying levels of access. For more information about Customer Access Management, see [Configure customer access management](https://www.servicenow.com/docs/access?context=configuring-cam&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US).

## D

Glossary terms are grouped alphabetically.

### Data

Information that is stored in your application. For example, employee phone numbers or office locations. You configure application data using tables.

### data binding

The process of associating data with a UI element that displays the information.

### data collector, data collection job

A scheduled job that collects data from one or more indicator sources to produce indicator scores.

### data resource

A dynamic, reusable way of defining what data to fetch for a page's components.

### data snapshots

An alternative architecture for indicators. This architecture uses a change data capture \(CDC\) process, which captures data changes from configurable tables that are optimized for generating scores and time series at run-time. Data snapshots avoid the need for breakdown matrices, allowing unlimited breakdowns.

### database view

A database view defines table joins for reporting purposes.

For example, a database view can join the Incident table to the Metric Definition table. This view can be used for an indicator source.

### decision tree

A guided flow to troubleshoot an issue and provide a solution. A decision tree is a multi-step process that includes a series of questions, answers, and a guidance for users to follow.

### Decision Tree Builder

A no-code visual tool, which provides a diagrammatic canvas for configuring nodes and their paths in a troubleshooting process.

### Deployment request

Ticket to track the review of submitted applications. From the deployment request form, a reviewer can deploy the application to different environments, accept or reject an application, and send feedback to a developer.

### Desktop In Desktop

Option in Attended Robot where you can work simultaneously while the robot runs an automation in the background. You can create multiple sessions on your machine.

### document class

A field used to apply a category or label to a document and to pages within a document in Document Intelligence.

For example, for an identity document use case, the classes might be passport, driver’s license, birth certificate, and the like.

### document task

A document processing activity in Document Intelligence. It includes the information that you want to extract from the document or documents.

## E

Glossary terms are grouped alphabetically.

### Engagement Messenger

Engagement Messenger is a messenger-like pop-up that can be embedded on any third-party web application to interact with ServiceNow® features, such as Case Management, Knowledge, Virtual Agent, Live Agent chat, and AI Search. It enables customers to use self-service to find the information or services that they need from third-party web applications that are outside of the ServiceNow environment.

### entitlement

An entitlement defines the type of support that a customer receives after a product is purchased.

### entity view action mapper

Also known as EVAM. Standardizes the format for displaying data in cards and lists.

### Environment

Instance that you use for the developing, testing, or launching an application. To set up App Engine Studio, you must define environments in each of the instances that you're using as environments.

### event \(UI Builder\)

Action a user takes \(such as selecting a button\) or an occurrence that happens on a page. Most UI Builder components, pages, and data resources have default-associated events. Use event handlers with the events to add additional actions to pages.

### event handler

An action performed when an event occurs.

### event mapping

The process of identifying an event handler to run when an event occurs.

### Experience

Graphical interface that your users interact with. For example, you can create a portal where users find information, submit requests, or complete business tasks. For more information on the available application experiences, see [Add an application experience](https://www.servicenow.com/docs/access?context=add-experience&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

### execution logs

Logs that are captured when an automation is executed by either an attended or an unattended robot. These logs help in understanding the errors and the end-to-end logging of automation execution. For more information, see .

### external user

Users who are external to your organization, such as third parties, contractors, or external agents. External users are not employees of your organization. You can define external users to have availability to access your instance, but without access to all the capabilities allocated to internal users.

### extraction

In Document Intelligence, the process of identifying relevant information in a document and using it as a basis for the AI to recommend a field value.

## F

Glossary terms are grouped alphabetically.

### field

A single piece of information to extract from a document in Document Intelligence. For example, the date on a document.

Fields are sometimes called keys or attributes.

### field group

A group of fields that belong together in Document Intelligence. Field groups are used to extract information from lists and tables.

For example, a group named "item" contains description, quantity, and unit price fields from a purchase order.

### field recommendation

A value that is recommended for a field on a record. Field recommendations are auto-filled or shown as messages underneath the fields.

### field value

The final output of the Document Intelligence application. The output contains the values for the specified fields that were extracted for a given document task.

### formula indicator

Produces a computed indicator score from one or more other indicators. Besides indicator scores, the formula can include calculations such as the gap between an indicator score and the indicator target.

## G

Glossary terms are grouped alphabetically.

### GraphQL services

A web query language optimized for client-side development to request the exact data they need. It provides a flexible and efficient way to interact with an API. Graph QL services refer to the APIs that utilize the GraphQL query language to retrieve and manipulate data for bot processes. RPA Desktop Design Studio, Unattended Robot, and Attended Robot applications use GraphQL services from RPA Hub.

### guidance

An action that users can take or information that they can share in Recommended Actions.

## H

Glossary terms are grouped alphabetically.

### HashCode

Unique, auto-generated alphanumeric value of a published package version.

### Heartbeat

Every 30 seconds, the ServiceNow unattended robot that runs on a robot machine posts a collection of heartbeat messages.

## I

Glossary terms are grouped alphabetically.

### indicator \(KPI\)

A performance measurement taken at regular intervals of a business service, an activity, or organizational behavior. These performance measurements result in a series of indicator scores over time. Businesses track these scores to measure current conditions and to forecast trends.

### indicator score

The value of an indicator for a specific collection period. For automated indicators, this value is calculated in a data collection job. For formula indicators, this value is calculated by performing operations on multiple automated indicators.

### indicator source

Defines sets of records from a ServiceNow table or database view that have a common characteristic, for example, that the Priority field value is critical. Indicators use indicator sources to calculate scores. Indicator scores are KPI values. Indicator sources specify a table, filtering conditions, and the frequency for collecting data.

### install base characteristics

The install base characteristics provide information about the service requirements for timely maintenance services of an install base item.

### install base management

The install base management helps track the products and services that are purchased by a customer along with the detailed configuration for each installed item.

### installed products

An installed product creates an association between sold products and install base items and provides information about where the sold product instance is deployed.

### interactive features

Responses that the virtual agent \(bot\) sends to customers which give the customer an option to interact. For example, a time picker gives the customer time slots to choose from when making an appointment.

### Internal User

Users who are internal to your organization, such as managers, agents, and other employees.

## J

Glossary terms are grouped alphabetically.

### Java keystore

A repository of security certificates – either authorization certificates or public key certificates – plus corresponding private keys.

### JSON Web Token \(JWT\)

A compact and self-contained way to securely transmit information between parties as a JSON object.

## K

Glossary terms are grouped alphabetically.

## L

Glossary terms are grouped alphabetically.

### Logic and automation

Business automated application processes. You define logic and automation using flows. A flow includes a sequence of actions and a trigger. You can use a flow template or create a flow from scratch.

Automate all the work in your application by adding logic and automation. For example, you can build a flow that sends a notification to the admin when someone makes a request.

Logic and automation

## M

Glossary terms are grouped alphabetically.

### macroponent

Core data structure that drives UI Builder pages. Fields contain JSON that builds the page.

### major case

A case that contains information about a specific issue that impacts multiple customers, like a system-wide outage. It is not associated with any accounts, contacts, or consumers; customer-specific information resides in the associated child cases. Major cases are also called parent cases.

### manual breakdown

In a manual breakdown, you define the breakdown elements and the indicator scores for each element manually instead of using records from a breakdown source.

### manual indicator

Manual indicators are not associated with an indicator source. Scores for manual indicators are not generated automatically by a data collection job. Instead, populate these indicators by adding scores to the scoresheet manually.

### matching rule

A rule that captures cases with specific case attributes that meet the matching rule criteria and routes them to the best-equipped customer service agent.

### modal

User experience window that overlays another content window and takes control of the user experience.

## N

Glossary terms are grouped alphabetically.

### natural language understanding \(NLU\)

A capability that enables the system to learn and respond to human-expressed intent. By entering natural language examples into the system, you help it understand word meanings and contexts so it can infer user or system actions.

### now code editor

A rich-text editor that supports CSS, HTML, JavaScript, XML, and JSON. Use Now Code Editor to change UI configuration, data resource configuration, styles, events, client-side scripts, and server-side scripts in Next Experience UI Builder components.

## O

Glossary terms are grouped alphabetically.

### order

An order is a confirmed request for the delivery of goods and services at specified terms. Alternatively, it's a quotation that is accepted by a customer.

## P

Glossary terms are grouped alphabetically.

### package

A package refers to a set of workflows, scripts, configurations, and dependencies that are designed to automate specific tasks or processes. These packages can be published or imported onto the RPA platforms to quickly deploy automation solutions.

Packages are used to encapsulate functionalities, libraries, or applications, making it simpler for developers or RPA administrators to deploy software components.

### package version

Package version that is a number that identifies the set of components uploaded in a package.

After a package is created, the RPA developer publishes an automation from RPA Desktop Design Studio. This process results in a new package version.

### page

Collection of column layouts, columns, and components. Create or customize multiple UI Builder pages for workspace and portal experiences.

### page collection

Group of pages that can be reused in experiences within tabs or modals.

### parent case

A case that contains information about a specific issue that impacts multiple customers, like a system-wide outage. It is not associated with any accounts, contacts, or consumers; customer-specific information resides in the associated child cases. Parent cases are also called major cases.

### Pipeline

Configuration for deploying an application to different environments.

### popover

A page overlay that enables users to continue using the rest of the page. Popovers can be configured just like UI Builder pages with text, components, images, fields, and menu items.

### port

Part of the component, categorized into Data ports and Control ports in RPA Desktop Design Studio.

### Portal Banner widget

This widget showcases announcements, highlights new products or features, and communicates important information on the portal page.

### Portal Browse Taxonomy widget

This widget displays hierarchical taxonomy topics, providing users with a seamless navigation experience to access knowledge articles and catalog items through the widget navigation pane.

### Portal Catalog Quick Links widget

This widget displays catalog items based on specific filter criteria. It enables admins to add an image, icon, name, and description on each card.

### Portal FAQ widget

This widget displays a curated list of frequently asked questions \(FAQs\) from a selected knowledge table on the portal. This feature empowers users to find answers to their queries without having to reach out to customer support or navigate through multiple knowledge article pages. Additionally, this widget provides the flexibility to filter the FAQs using options available in the main navigation.

### post case review

A document written after the case has been closed captures details about a resolved case, including a summary of the issue, affected assets, root cause, resolution, and any preventive measures.

### process job

Execution of a bot process by a robot in RPA Hub.

### process parameter

Variable that is used within a bot process in RPA Hub.

### product model

A product model is a specific version or configuration of a product. Product models provide customer service agents and customers with a common understanding of the products that are being used.

### product offer

A product offer represents entities that can be ordered from the catalog. An offer includes pricing information and add-on services like warranties, service contracts, maintenance contracts, or entitlements.

### proxy contact

The proxy contacts are employees within a company who are not fulfillers or do not have other CSM-specific roles. This role enables employees to create cases for customer accounts and contacts, and also allows them to be proxy case contacts on behalf of customers.

## Q

Glossary terms are grouped alphabetically.

### queue

Repository that can hold a number of work items in RPA Hub. Work items can store multiple types of data, such as transaction information, customer details, or information from a document.

Queues are used in automations to distribute transactional data or the workload among different robots.

### quote

A quote is a formal offer for products or services that are proposed to a customer at specific prices and payment terms.

## R

Glossary terms are grouped alphabetically.

### recommendation

In Document Intelligence, a bit of text found on a document. The recommendation includes information about its location in the document, meaning the page of a document and the particular location on that page.

The recommendations that the AI provides are sorted based on how likely the AI believes a given recommendation to be the correct value for the current field.

### repeater

In UI Builder, a repeater is a component that acts as a basic loop that repeats the data you provide in multiple components. Repeaters use an array or an array of objects. Repeaters bind values to a data array property. For example, \[\{"task": "A"\},\{"task": "B"\}\], repeats the content inside it two times.

### requester

A consumer or a customer contact who interacts with a virtual agent or live agent through a chat.

### resource generator

A configuration that provides resources such as a knowledge article, a set of cases, or a field value that you can use in providing recommendations in Recommended Actions.

### robot

A software agent that runs a bot process \(automation\). Robots are designed to interact with software applications, data sources, and user interfaces like a human operator would, but in a more efficient, accurate, and consistent manner.

### robot file

The automation file that is created when you use RPA Desktop Design Studio for designing an automation workflow. This robot file contains the automation logic for the robot to execute.

### RPA Desktop Design Studio

Windows native application that is used by RPA developers to design or configure automation workflows.

### RPA plugin

Software component that adds a specific feature for an interaction with third-party applications such as Microsoft Office 365, Google Chrome, Windows, and so on.

### RPA plugins app \(RPA plugin bundle\)

The Robotic Process Automation \(RPA\) Plugin Bundle is the application responsible for building automations. The RPA Plugin Bundle contains metadata of Windows library files that are consumed by RPA Desktop Design Studio, Unattended Robot, and Attended Robot applications. These plugins extend the capability of the RPA product. For instance, RPA Chrome Plugin enables RPA application to automate tasks on the Google Chrome browser. Similarly, the RPA Excel plugin enables the RPA applications to interact with Excel files and many more. Along with Integration Hub, RPA Plugins Bundle is part of Workflow Data Fabric for a complete integration and automation solution for ServiceNow.

## S

Glossary terms are grouped alphabetically.

### schedule

In RPA Hub, a schedule is associated to an unattended bot process to enable users to execute jobs in a planned manner at regular intervals. More than one schedule can be associated with one bot process.

### Security

Roles and access controls to limit who can use your application.

### Service Level Agreement \(SLA\)

An agreement that specifies the time within which service must be provided. SLA definitions are configured to include the necessary information to create and progress SLAs for customer service cases.

### Service Level Agreement \(SLA\) definition

A definition that includes the timings, conditions, workflows, and other information required to create and progress task Service Level Agreements \(SLAs\), enabling you to use an SLA system for your organization's tasks.

### Service Model Foundation

A foundational data model framework that customers can use to create structured and flexible data models to represent their business needs. For more information about the Service Model Foundation overview, see [Service Model Foundation overview](https://www.servicenow.com/docs/access?context=csm-industry-data-model&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US).

### shared parameter

Global variables or configurable items that are stored in one place. These variables are used across bot processes.

### skill

Pre-built automation and plug-and-play integration for your complex business processes.

### snapshot

A list of table records \(sys\_ids\) that are collected at the time that the indicator scores for those records are collected.

### special handling notes

Notes, created with the Special Handling Notes application, that bring important information about individual records to the user's attention, and can be assigned a status, a priority, and an expiration date. Special handling notes can be displayed in different ways: in an embedded list or a related list on a record form or in a pop-up window that displays when you access a form.

## T

Glossary terms are grouped alphabetically.

### target

Future hoped-for indicator scores that represent goals your organization wants to achieve. A target can be global or can be personal to one user.

### threshold

The user-defined top or bottom limit of the normal range of scores for an indicator. You can set up an alert to inform you when a threshold is breached and how, such as when a score reaches an all-time high or low.

## U

Glossary terms are grouped alphabetically.

### UI Builder \(UIB\)

A WYSIWYG web user interface builder. UI Builder enables developers to build new pages or customize existing pages for Agent Workspace and portals using Now Experience UI Framework components.

### Unattended Robot

Software agent that is installed on a Windows machine and executes unattended automations.

### unstructured document

A document that mainly contains free-form textual information and does not conform to a specific format or structure.

### use case

A use case is a set of configurations used to define the structure of a type of document that you want to process. It’s made up of the use case record and its related fields, field groups, integrations, flows, and all the related machine learning \(ML\) models. The use case also includes the mode for how the extraction should occur.

### user input control

The format of the response choice given to the user, for example, “Static Choice” where a user chooses from a predefined list.

## V

Glossary terms are grouped alphabetically.

### variant

Version of a UI Builder page with access controlled by role or condition. Create variants of pages to target experiences for different audiences. For example, create a home page for agents and a variant for managers at the same URL. Alternatively, create a page variant that users see under different conditions.

### Virtual Agent

Virtual Agent is an AI-powered conversational chatbot that provides instant resolution to common requests, increases customer satisfaction, and keep agents focused on more important issues.

## W

Glossary terms are grouped alphabetically.

### webhook

An HTTP-based callback function that allows lightweight, event-driven communication between two application programming interfaces \(APIs\).

### widget instance options

These options enable admins to modify the data, presentation, and behavior of the widget. Each instance of the widget can be configured to look and behave differently.

### work item

Store multiple types of data, such as transaction information, customer details, or information from a document.

