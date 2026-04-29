---
title: Robotic Process Automation \(RPA\) Hub glossary
description: Learn about the terms and concepts that are unique to Robotic Process Automation \(RPA\) Hub.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms]
breadcrumb: [Reference, RPA Hub, Workflow Data Fabric]
---

# Robotic Process Automation \(RPA\) Hub glossary

Learn about the terms and concepts that are unique to Robotic Process Automation \(RPA\) Hub.

**Parent Topic:**[RPA Hub reference](rpa-hub-reference.md)

## A

Glossary terms are grouped alphabetically.

### activities

Reusable set of instructions that are designed for an automation on the Design surface of RPA Desktop Design Studio.

### alert

Custom notifications that are sent to a user or a group. These notifications are generated for robots, schedules, process jobs, and other RPA Hub related tables.

### AMB channel

The Asynchronous Message Bus \(AMB\) channel is utilized to notify unattended robots, when a change is made to bot processes in RPA Hub. Consequently, all the robots subscribed to the designated channel receive a notification. For example, when Start Process is initiated from RPA Hub, a message is sent to the selected robot via an AMB channel, then the robot receives the message to start the automation process.

### Attachment Framework

A set of REST APIs that enable uploading or downloading attachments to or from a ServiceNow instance. This helps in publishing and downloading automation packages that are built in RPA Desktop Design Studio to the ServiceNow instance \(RPA Hub\) that run on attended or unattended robots.

### Attended Robot

Software agent that is installed on a Windows machine and executes attended automations.

### automation

Robotic Process Automation \(RPA\) is a software technology that makes it easy to build, deploy, and manage robots that emulate human actions interacting with digital systems and software.

## B

Glossary terms are grouped alphabetically.

### bot process

A predefined sequence of actions that a robot follows to accomplish a specific task or achieve a particular goal in RPA Hub. You can assign and schedule a package that will be executed by the software agent. You can add other details that pertain to the bot process, such as business applications, credential groups, process robot credentials, process parameters, attended users, or groups.

### bot process configuration

A record that contains the bot process settings. The bot process configuration record is mapped to a bot process record in RPA Hub. It is a one to one mapping.

### breakpoint

Option in RPA Desktop Design Studio that you set to stop or pause the automation execution for debugging purposes.

## C

Glossary terms are grouped alphabetically.

### component

Reusable blocks that are used for designing automations and to abstract functionality in RPA Desktop Design Studio.

### connector

Connector that connects to various data sources and tools to create automation in RPA Desktop Design Studio.

## D

Glossary terms are grouped alphabetically.

### Desktop In Desktop

Option in Attended Robot where you can work simultaneously while the robot runs an automation in the background. You can create multiple sessions on your machine.

## E

Glossary terms are grouped alphabetically.

### execution logs

Logs that are captured when an automation is executed by either an attended or an unattended robot. These logs help in understanding the errors and the end-to-end logging of automation execution. For more information, see [Bot Process form in RPA Hub](../task/select-botprocess.md#).

## G

Glossary terms are grouped alphabetically.

### GraphQL services

A web query language optimized for client-side development to request the exact data they need. It provides a flexible and efficient way to interact with an API. Graph QL services refer to the APIs that utilize the GraphQL query language to retrieve and manipulate data for bot processes. RPA Desktop Design Studio, Unattended Robot, and Attended Robot applications use GraphQL services from RPA Hub.

## H

Glossary terms are grouped alphabetically.

### HashCode

Unique, auto-generated alphanumeric value of a published package version.

### Heartbeat

Every 30 seconds, the ServiceNow unattended robot that runs on a robot machine posts a collection of heartbeat messages.

### High density robot

High density robots leverage the Remote Desktop Services to execute multiple automations simultaneously in separate user sessions on the same Windows Server machine.

## P

Glossary terms are grouped alphabetically.

### package

A package refers to a set of workflows, scripts, configurations, and dependencies that are designed to automate specific tasks or processes. These packages can be published or imported onto the RPA platforms to quickly deploy automation solutions.

Packages are used to encapsulate functionalities, libraries, or applications, making it simpler for developers or RPA administrators to deploy software components.

### package version

Package version that is a number that identifies the set of components uploaded in a package.

After a package is created, the RPA developer publishes an automation from RPA Desktop Design Studio. This process results in a new package version.

### port

Part of the component, categorized into Data ports and Control ports in RPA Desktop Design Studio.

### process job

Execution of a bot process by a robot in RPA Hub.

### process parameter

Variable that is used within a bot process in RPA Hub.

## Q

Glossary terms are grouped alphabetically.

### queue

Repository that can hold a number of work items in RPA Hub. Work items can store multiple types of data, such as transaction information, customer details, or information from a document.

Queues are used in automations to distribute transactional data or the workload among different robots.

## R

Glossary terms are grouped alphabetically.

### robot

A software agent that runs a bot process \(automation\). Robots are designed to interact with software applications, data sources, and user interfaces like a human operator would, but in a more efficient, accurate, and consistent manner.

### robot file

The automation file that is created when you use RPA Desktop Design Studio for designing an automation workflow. This robot file contains the automation logic for the robot to execute.

### RPA bot generation skill

Now Assist for RPA Hub skill that uses generative AI for creating automations, activities, and extending automation logic.

### RPA Desktop Design Studio

Windows native application that is used by RPA developers to design or configure automation workflows.

### RPA plugin

Software component that adds a specific feature for an interaction with third-party applications such as Microsoft Office 365, Google Chrome, Windows, and so on.

### RPA plugins app \(RPA plugin bundle\)

The Robotic Process Automation \(RPA\) Plugin Bundle is the application responsible for building automations. The RPA Plugin Bundle contains metadata of Windows library files that are consumed by RPA Desktop Design Studio, Unattended Robot, and Attended Robot applications. These plugins extend the capability of the RPA product. For instance, RPA Chrome Plugin enables RPA application to automate tasks on the Google Chrome browser. Similarly, the RPA Excel plugin enables the RPA applications to interact with Excel files and many more. Along with Integration Hub, RPA Plugins Bundle is part of Workflow Data Fabric for a complete integration and automation solution for ServiceNow.

## S

Glossary terms are grouped alphabetically.

### schedule

A schedule that is associated to an unattended bot process to enable users to execute jobs in a planned manner at regular intervals. More than one schedule can be associated with one bot process.

### shared parameter

A global variable or configurable item that is stored in one place. These variables are used across bot processes.

### skill

A pre-built automation and plug-and-play integration for your complex business processes.

## U

Glossary terms are grouped alphabetically.

### Unattended Robot

A software agent that is installed on a Windows machine and executes unattended automations.

## W

Glossary terms are grouped alphabetically.

### work item

Store multiple types of data, such as transaction information, customer details, or information from a document.

