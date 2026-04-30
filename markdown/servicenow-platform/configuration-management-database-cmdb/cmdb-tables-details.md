---
title: CMDB tables descriptions
description: List of tables in the CMDB in a base system with its name, label, and a description of the type of information that is stored in the table.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 32
breadcrumb: [Explore, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB tables descriptions

List of tables in the CMDB in a base system with its name, label, and a description of the type of information that is stored in the table.

You can extend tables in a base system by installing a CMDB CI Class Models store app which adds class models that support specific technologies. These extensions include class definitions, identification rules, identifier entries, and dependent relationships if applicable. A CMDB CI Class Models store app can also modify the label of a base class. For more information, see [CMDB CI Class Models](../concept/cmdb-ci-class-models.md).

Class descriptions are integrated into the CI Class Manager and appear in the **Description** field on the Basic Info page for a class. For more information about viewing class descriptions, see [View and edit class definitions and metadata](../task/t_ViewTableDefinitions.md).

<table id="table_jjn_xvp_33b"><thead><tr><th>

Table name

</th><th>

Label \(display name\)

</th><th>

Table description

</th></tr></thead><tbody><tr><td>

cmdb\_ci

</td><td>

Configuration Item

</td><td>

Base configuration item \(CI\) table.

</td></tr><tr><td>

cmdb\_ci\_acc

</td><td>

Accessory

</td><td>

Accessories for phones, computers, and so on.

</td></tr><tr><td>

cmdb\_ci\_ad\_controller

</td><td>

Active Directory Domain Controller

</td><td>

Microsoft Active Directory domain controller.

</td></tr><tr><td>

cmdb\_ci\_ad\_domain

</td><td>

AD Domain

</td><td>

Microsoft Active Directory domain.

</td></tr><tr><td>

cmdb\_ci\_aix\_server

</td><td>

AIX Server

</td><td>

Server running the AIX operating system.

</td></tr><tr><td>

cmdb\_ci\_alias

</td><td>

Alias

</td><td>

Pseudonym for data locations, virtual email addresses, pointers, and so on.

</td></tr><tr><td>

cmdb\_ci\_apache\_web\_server

</td><td>

Apache Web Server

</td><td>

Server hosting Apache web server software.

</td></tr><tr><td>

cmdb\_ci\_appl

</td><td>

Application

</td><td>

Application, which is a collection of files and data that deliver a service and manage business processes.

</td></tr><tr><td>

cmdb\_ci\_appl\_now\_app

</td><td>

ServiceNow Application

</td><td>

CIs that Event Management generates for various components such as Impact calculator, which is used to bind alerts that are later shown in maps. Used internally by self-health when monitoring internal health checks for key components such as connector instance status and MID Server status.

 Parent class for all ServiceNow applications.

</td></tr><tr><td>

cmdb\_ci\_application\_cluster

</td><td>

Application Cluster

</td><td>

Logical group of servers with clustering software installed on each of the servers in the group so that the group acts like a single system.

</td></tr><tr><td>

cmdb\_ci\_application\_server\_resource

</td><td>

Application Server Resource

</td><td>

Parent class for application servers such as Coldfusion application server.

</td></tr><tr><td>

cmdb\_ci\_app\_server

</td><td>

Application Server

</td><td>

A base table for logical CIs, which indicate the primary function of a physical or virtual server such as a Tomcat server or a WebSphere server.

</td></tr><tr><td>

cmdb\_ci\_app\_server\_composer

</td><td>

Composer

</td><td>

Server hosting IBM WebSphere Multichannel Bank Transformation Toolkit.

</td></tr><tr><td>

cmdb\_ci\_app\_server\_datapower

</td><td>

Data Power

</td><td>

Server hosting IBM DataPower Gateway Secure software.

</td></tr><tr><td>

cmdb\_ci\_app\_server\_domino

</td><td>

Domino

</td><td>

Server hosting IBM Domino software.

</td></tr><tr><td>

cmdb\_ci\_app\_server\_hp\_ucmdb

</td><td>

HP uCMDB

</td><td>

Server hosting HP uCMDB software.

</td></tr><tr><td>

cmdb\_ci\_app\_server\_java

</td><td>

JavaServer

</td><td>

Server hosting Java applications.

</td></tr><tr><td>

cmdb\_ci\_app\_server\_jb\_module

</td><td>

delivery Controler

</td><td>

Server hosting an inner module of JBoss application \(deployed application\).

</td></tr><tr><td>

cmdb\_ci\_app\_server\_jboss

</td><td>

JBoss

</td><td>

Server hosting a JBoss Application Server \(JBoss AS\), which is a cross-platform Java application server, open-source developed by the JBoss software company.

</td></tr><tr><td>

cmdb\_ci\_app\_server\_jrun

</td><td>

Jrun

</td><td>

Server hosting JRun applications.

</td></tr><tr><td>

cmdb\_ci\_app\_server\_jrun\_war

</td><td>

Jrun WAR

</td><td>

Server hosting the inner module of a JRun application \(deployed application\).

</td></tr><tr><td>

cmdb\_ci\_app\_server\_ora\_ess

</td><td>

Oracle Essbase Server

</td><td>

Server hosting Oracle Essbase software.

</td></tr><tr><td>

cmdb\_ci\_app\_server\_ora\_ias

</td><td>

Oracle iAS

</td><td>

Server hosting Oracle internet Application Server.

</td></tr><tr><td>

cmdb\_ci\_app\_server\_ora\_ias\_m

</td><td>

Oracle iAS Web module

</td><td>

Server hosting the inner module of the Oracle iAS application \(deployed application\).

</td></tr><tr><td>

cmdb\_ci\_app\_server\_remedy

</td><td>

Remedy HSServer

</td><td>

Server hosting Remedy HSSServer application.

</td></tr><tr><td>

cmdb\_ci\_app\_server\_tomcat

</td><td>

Tomcat

</td><td>

Server hosting Apache Tomcat software.

</td></tr><tr><td>

cmdb\_ci\_app\_server\_tomcat\_war

</td><td>

Tomcat WAR

</td><td>

Server hosting inner module of Apache Tomcat application \(deployed application\).

</td></tr><tr><td>

cmdb\_ci\_app\_server\_vendavo

</td><td>

Vendavo Application Server

</td><td>

Server hosting Vendavo Application Server software.

</td></tr><tr><td>

cmdb\_ci\_app\_server\_weblogic

</td><td>

BEA Weblogic

</td><td>

Server hosting Oracle WebLogic Server.

</td></tr><tr><td>

cmdb\_ci\_app\_server\_webseal

</td><td>

Webseal

</td><td>

Server hosting IBM Tivoli Access Manager solution.

</td></tr><tr><td>

cmdb\_ci\_app\_server\_websphere

</td><td>

IBM Websphere

</td><td>

Server hosting IBM WebSphere software.

</td></tr><tr><td>

cmdb\_ci\_app\_server\_wl\_module

</td><td>

WeblogicModule

</td><td>

Server hosting inner module of WebLogic.

</td></tr><tr><td>

cmdb\_ci\_app\_server\_ws\_ear

</td><td>

Websphere EAR

</td><td>

Server hosting inner module of IBM WebSphere software.

</td></tr><tr><td>

cmdb\_ci\_app\_server\_ws\_odr

</td><td>

Websphere ODR LB

</td><td>

Server hosting WebSphere ODR LB application.

</td></tr><tr><td>

cmdb\_ci\_appl\_active\_directory

</td><td>

Active Directory Service

</td><td>

Inner software module of AD Domain application.

</td></tr><tr><td>

cmdb\_ci\_appl\_biztalk

</td><td>

BizTalk

</td><td>

Microsoft BizTalk Server software.

</td></tr><tr><td>

cmdb\_ci\_appl\_biztalk\_orch

</td><td>

BizTalk Orchestration

</td><td>

Inner module of Microsoft Biztalk Server software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ca

</td><td>

CA Enterprise Communicator

</td><td>

CA Enterprise Communicator software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ca\_dir\_server

</td><td>

CA eTrust Directory Server

</td><td>

CA eTrust Directory Server software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ca\_ent\_man

</td><td>

CA Introscope Enterprise Manager

</td><td>

CA introscope Enterprise Manager software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ca\_id\_man

</td><td>

CA Identity Manager Provisioning Server

</td><td>

CA Identity Manager Server software.

</td></tr><tr><td>

cmdb\_ci\_appl\_cisco\_call\_man

</td><td>

Cisco CallManager

</td><td>

Cisco CallManager \(Cisco Unified Communications Manager\) software.

</td></tr><tr><td>

cmdb\_ci\_appl\_cisco\_fibre

</td><td>

Cisco Fibre InterConnect

</td><td>

Cisco Fibre InterConnect software.

</td></tr><tr><td>

cmdb\_ci\_appl\_citrix\_app

</td><td>

Citrix Application Icon

</td><td>

Inner module of Citrix software.

</td></tr><tr><td>

cmdb\_ci\_appl\_citrix\_collector

</td><td>

Citrix Collector

</td><td>

Citrix Collector software.

</td></tr><tr><td>

cmdb\_ci\_appl\_citrix\_xenapp

</td><td>

Citrix XenAPP or Presentation Server

</td><td>

Citrix XenApp software.

</td></tr><tr><td>

cmdb\_ci\_appl\_connectit

</td><td>

Connect-It Service

</td><td>

Connect-It software.

</td></tr><tr><td>

cmdb\_ci\_appl\_controlm

</td><td>

Control-M

</td><td>

Control-M software.

</td></tr><tr><td>

cmdb\_ci\_appl\_delivery\_controler

</td><td>

Delivery Controler

</td><td>

Application delivery controller software.

</td></tr><tr><td>

cmdb\_ci\_appl\_doc\_brava\_proc

</td><td>

Documentum Brava Job Processor

</td><td>

Brava \(EMC Documentum\) job processor software.

</td></tr><tr><td>

cmdb\_ci\_appl\_doc\_brava\_server

</td><td>

Documentum Brava License Server

</td><td>

Brava \(EMC Documentum\) License Server software.

</td></tr><tr><td>

cmdb\_ci\_appl\_doc\_docbase

</td><td>

Documentum DocBase

</td><td>

Documentum Docbase software.

</td></tr><tr><td>

cmdb\_ci\_appl\_doc\_docbroker

</td><td>

Documentum Broker

</td><td>

Documentum Docbase broker software.

</td></tr><tr><td>

cmdb\_ci\_appl\_dot\_net

</td><td>

.NET Application

</td><td>

Microsoft .NET application software.

</td></tr><tr><td>

cmdb\_ci\_appl\_fastsearch

</td><td>

Fast Search

</td><td>

Microsoft FAST Search software \(for the SharePoint collaboration platform\).

</td></tr><tr><td>

cmdb\_ci\_appl\_generic

</td><td>

Generic Application

</td><td>

Generic application, which is identified by the system when there is an endpoint with an open port in listen mode and there is no pattern for it.

</td></tr><tr><td>

cmdb\_ci\_appl\_glassfish

</td><td>

GlassFish

</td><td>

Oracle GlassFish Server software.

</td></tr><tr><td>

cmdb\_ci\_appl\_glassfish\_war

</td><td>

GlassFish WAR

</td><td>

Inner module of GlassFish application \(deployed application\).

</td></tr><tr><td>

cmdb\_ci\_appl\_groundwork

</td><td>

Groundwork

</td><td>

Groundwork \(open source\) monitoring software.

</td></tr><tr><td>

cmdb\_ci\_appl\_hp\_index

</td><td>

HP SM Index Server

</td><td>

HP Service Manager Index Server software.

</td></tr><tr><td>

cmdb\_ci\_appl\_hp\_operations

</td><td>

HP Operations Manager

</td><td>

HP Operations Manager software.

</td></tr><tr><td>

cmdb\_ci\_appl\_hp\_qc

</td><td>

HP Quality Center

</td><td>

HP Quality Center software.

</td></tr><tr><td>

cmdb\_ci\_appl\_hp\_service

</td><td>

HP Service Manager

</td><td>

HP Service Manager software.

</td></tr><tr><td>

cmdb\_ci\_appl\_hp\_sm\_kb

</td><td>

HP SM KnowledgeBase

</td><td>

HP Service Manager KnowledgeBase software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ibm\_cics

</td><td>

IBM CICS

</td><td>

IBM CICS Transaction Server software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ibm\_ctg

</td><td>

IBM CTG

</td><td>

IBM CICS Transaction Gateway software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ibm\_wmb

</td><td>

IBM WebSphere Message Broker

</td><td>

IBM WebSphere Message Broker software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ibm\_wmb\_listener

</td><td>

IBM WMB Http Listener

</td><td>

IBM WebSphere HTTP Listener software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ibm\_wmq

</td><td>

IBM MQ Manager \(Formerly IBM WebSphere MQ\)

</td><td>

IBM MQ software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ibm\_wmq\_queue

</td><td>

IBM MQ Queue \(Formerly IBM WebSphere MQ Queue\)

</td><td>

Inner module of IBM MQ software.

</td></tr><tr><td>

cmdb\_ci\_appl\_itam

</td><td>

ITAM Asset Center

</td><td>

HP Asset Center software.

</td></tr><tr><td>

cmdb\_ci\_appl\_mongo\_config\_serv

</td><td>

Mongo Config Server

</td><td>

Mongo Configuration Server software.

</td></tr><tr><td>

cmdb\_ci\_appl\_mongos

</td><td>

Mongos Server

</td><td>

MongoDB server software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ms\_dynamic\_crm

</td><td>

Dynamic CRM Component

</td><td>

Microsoft Dynamic CRM software.

</td></tr><tr><td>

cmdb\_ci\_appl\_msmq

</td><td>

MSMQ

</td><td>

Microsoft Message Queuing \(MSMQ\) software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ora\_conc

</td><td>

Oracle Concurrent Server

</td><td>

Oracle Concurrent Server software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ora\_disc

</td><td>

Oracle Discoverer Engine

</td><td>

Oracle Discoverer software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ora\_disc\_ui

</td><td>

Oracle Discoverer UI

</td><td>

Oracle Discoverer UI module software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ora\_ebs

</td><td>

Oracle ESB

</td><td>

Oracle Enterprise Service Bus software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ora\_forms

</td><td>

Oracle Forms Engine

</td><td>

Oracle Forms software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ora\_forms\_ui

</td><td>

Oracle Forms UI

</td><td>

Oracle Forms UI software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ora\_fs

</td><td>

Oracle Fulfillment Server

</td><td>

Oracle Fulfillment Server software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ora\_http

</td><td>

Oracle HTTP Server

</td><td>

Oracle HTTP Server software \(web tier of Oracle Fusion middleware\).

</td></tr><tr><td>

cmdb\_ci\_appl\_ora\_jms\_queue

</td><td>

Oracle Weblogic JMS Queue

</td><td>

Oracle WebLogic JMS software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ora\_metric\_client

</td><td>

Oracle Metric Client

</td><td>

Oracle Metric client software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ora\_metric\_svr

</td><td>

Oracle Metric Server

</td><td>

Oracle Metric server software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ora\_notif\_svr

</td><td>

Oracle Notification Server

</td><td>

Oracle Notification Server \(ONS\) software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ora\_oacore

</td><td>

Oracle OACORE Server

</td><td>

Oracle OACORE server software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ora\_oafm

</td><td>

Oracle OAFM Server

</td><td>

Oracle OAFM server software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ora\_pm

</td><td>

Oracle Process Manager

</td><td>

Oracle BPEL Process Manager server software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ora\_queue

</td><td>

Advanced Queue Queue

</td><td>

Oracle Advanced Queuing software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ora\_report

</td><td>

Oracle Report Server

</td><td>

The Oracle Report Server software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ora\_tns

</td><td>

Oracle App TNS Service

</td><td>

Oracle Application Express \(TNS\) listener software.

</td></tr><tr><td>

cmdb\_ci\_appl\_ora\_tnslsnr

</td><td>

Oracle TNS Listener Engine

</td><td>

Oracle Application Express software.

</td></tr><tr><td>

cmdb\_ci\_appl\_peoplesoft

</td><td>

Peoplesoft Application Server

</td><td>

Peoplesoft Application Server software.

</td></tr><tr><td>

cmdb\_ci\_appl\_rabbitmq

</td><td>

RabbitMQ

</td><td>

RabbitMQ \(open source\) software.

</td></tr><tr><td>

cmdb\_ci\_appl\_rabbitmq\_cluster

</td><td>

RabbitMQ Cluster

</td><td>

RabbitMQ Cluster \(open source\) software.

</td></tr><tr><td>

cmdb\_ci\_appl\_sap\_ascs

</td><td>

SAP ASCS Application

</td><td>

SAP ASCS software.

</td></tr><tr><td>

cmdb\_ci\_appl\_sap\_bo

</td><td>

SAP Business Objects CMS Server

</td><td>

SAP Business Objects CMS server software.

</td></tr><tr><td>

cmdb\_ci\_appl\_sap\_bo\_scheduler

</td><td>

SAP BO BOXIScheduleRouter

</td><td>

SAP BO BOXIScheduleRouter software.

</td></tr><tr><td>

cmdb\_ci\_appl\_sap\_bus\_obj

</td><td>

SAP Business Objects

</td><td>

SAP bushiness Object application.

</td></tr><tr><td>

cmdb\_ci\_appl\_sap\_ci

</td><td>

SAP CI Application

</td><td>

The SAP Central Instance software.

</td></tr><tr><td>

cmdb\_ci\_appl\_sap\_di

</td><td>

SAP DI Application

</td><td>

Oracle Development Infrastructure \(DI\) software.

</td></tr><tr><td>

cmdb\_ci\_appl\_sap\_ers

</td><td>

SAP ERS Application

</td><td>

Oracle Evaluated Receipt Settlement \(ERS\) software.

</td></tr><tr><td>

cmdb\_ci\_appl\_sap\_hana\_db

</td><td>

SAP Hana Db

</td><td>

SAP HANA software.

</td></tr><tr><td>

cmdb\_ci\_appl\_sap\_jc

</td><td>

SAP JC Application

</td><td>

SAP JC \(java application\) software.

</td></tr><tr><td>

cmdb\_ci\_appl\_sap\_scs

</td><td>

SAP SCS Application

</td><td>

SAP SCS \(central services\) software.

</td></tr><tr><td>

cmdb\_ci\_appl\_sendmail

</td><td>

Sendmail

</td><td>

Sendmail \(open source\) software.

</td></tr><tr><td>

cmdb\_ci\_appl\_sharepoint

</td><td>

SharePoint

</td><td>

Microsoft SharePoint software.

</td></tr><tr><td>

cmdb\_ci\_appl\_sp\_service

</td><td>

SharePoint Service

</td><td>

Microsoft Windows Sharepoint Services \(WSS\) software.

</td></tr><tr><td>

cmdb\_ci\_appl\_tibco\_hawk

</td><td>

Tibco Hawk

</td><td>

TIBCO Hawk software.

</td></tr><tr><td>

cmdb\_ci\_appl\_tibco\_matrix

</td><td>

ActiveMatrix Business Works

</td><td>

TIBCO ActiveMatrix BusinessWorks software.

</td></tr><tr><td>

cmdb\_ci\_appl\_tibco\_matrix\_proc

</td><td>

ActiveMatrix Business Works Process

</td><td>

TIBCO ActiveMatrix BusinessWorks Process software.

</td></tr><tr><td>

cmdb\_ci\_appl\_tibco\_message

</td><td>

Tibco Enterprise Message Service

</td><td>

TIBCO Enterprise Message Service software.

</td></tr><tr><td>

cmdb\_ci\_appl\_tibco\_queue

</td><td>

EMS Queue

</td><td>

Tibco EMS \(Enterprise Message Service\) Queues software.

</td></tr><tr><td>

cmdb\_ci\_appl\_tuxedo

</td><td>

Tuxedo

</td><td>

Tuxedo software \(middleware transactions for UNIX, Extended for Distributed Operations\).

</td></tr><tr><td>

cmdb\_ci\_appl\_tuxedo\_portal

</td><td>

Tuxedo Portal

</td><td>

Tuxedo portal software.

</td></tr><tr><td>

cmdb\_ci\_appl\_vign\_content\_svr

</td><td>

Vignette Content Management Server

</td><td>

Vignette \(Open Text Corp\) Content Management Server software.

</td></tr><tr><td>

cmdb\_ci\_appl\_vignette\_search

</td><td>

Vignette Search Starter

</td><td>

Vignette \(Open Text Corp\) Search Server software.

</td></tr><tr><td>

cmdb\_ci\_appl\_vignette\_server

</td><td>

Vignette Server

</td><td>

Vignette \(Open Text Corp\) Server software.

</td></tr><tr><td>

cmdb\_ci\_appl\_weblogic\_jms

</td><td>

Weblogic JMS Server

</td><td>

WebLogic JMS software.

</td></tr><tr><td>

cmdb\_ci\_appl\_weblogic\_lb

</td><td>

Weblogic LB

</td><td>

WebLogic Server load balancer software.

</td></tr><tr><td>

cmdb\_ci\_appl\_weblogicmodule

</td><td>

Weblogic Module Server

</td><td>

WebLogic Server software.

</td></tr><tr><td>

cmdb\_ci\_appl\_websphere\_portal

</td><td>

Websphere Portal

</td><td>

WebSphere Portal software.

</td></tr><tr><td>

cmdb\_ci\_appl\_wmb

</td><td>

WMB Flow

</td><td>

WebSphere Message Broker software.

</td></tr><tr><td>

cmdb\_ci\_application\_cluster

</td><td>

Application Cluster

</td><td>

Logical cluster of application-tier servers.

</td></tr><tr><td>

cmdb\_ci\_application\_software

</td><td>

Application Software

</td><td>

Computer program designed to perform a group of coordinated functions, tasks, or activities for the benefit of the user.

 An extension of the Software table, providing installed software information \(not a running process\).

</td></tr><tr><td>

cmdb\_ci\_ats\_power\_eq

</td><td>

Automatic Transfer Switch

</td><td>

Electrical power switch that switches a load between two sources.

</td></tr><tr><td>

cmdb\_ci\_availability\_set

</td><td>

Availability Set

</td><td>

Logical grouping of virtual machines running on Microsoft Azure platform.

</td></tr><tr><td>

cmdb\_ci\_base\_rpa\_process

</td><td>

Base Bot Process

</td><td>

Business reason, process type, and schedule.

</td></tr><tr><td>

cmdb\_ci\_base\_rpa\_robot

</td><td>

Base Robot

</td><td>

Machine where robot is running, state, and type.

</td></tr><tr><td>

cmdb\_ci\_batch\_job

</td><td>

Batch Job

</td><td>

A computer program or set of programs processed in batch mode.

</td></tr><tr><td>

cmdb\_ci\_aws\_datacenter

</td><td>

AWS datacenter

</td><td>

Logical representation of an Amazon Web Services datacenter.

</td></tr><tr><td>

cmdb\_ci\_azure\_datacenter

</td><td>

Azure datacener

</td><td>

Logical representation of a Microsoft Azure datacenter.

</td></tr><tr><td>

cmdb\_ci\_business\_app

</td><td>

Business Application

</td><td>

All business applications.

</td></tr><tr><td>

cmdb\_ci\_business\_process

</td><td>

Business Process

</td><td>

A process that is owned and carried out by the business and contributes to the delivery of a product or business service to a business customer.

</td></tr><tr><td>

cmdb\_ci\_chassis\_server

</td><td>

Server Chassis

</td><td>

A metal structure that is used to house or physically assemble servers in various different form factors.

</td></tr><tr><td>

cmdb\_ci\_cim\_profile

</td><td>

CIM Profiles

</td><td>

CIM Profiles \(UML\).

</td></tr><tr><td>

cmdb\_ci\_cim\_server

</td><td>

CIM Server

</td><td>

Server hosting CIM profiles.

</td></tr><tr><td>

cmdb\_ci\_circuit

</td><td>

Circuit

</td><td>

Electrical circuits information.

</td></tr><tr><td>

cmdb\_ci\_cloud\_database

</td><td>

Cloud Database

</td><td>

Database which runs on a cloud computing platform.

</td></tr><tr><td>

cmdb\_ci\_cloud\_ip\_address

</td><td>

Cloud IP Address

</td><td>

Web server which runs on a cloud computing platform.

</td></tr><tr><td>

cmdb\_ci\_cluster

</td><td>

Cluster

</td><td>

Logical group of computing resources bound together by software to function as one logical computing resource.

</td></tr><tr><td>

cmdb\_ci\_cluster\_node

</td><td>

Cluster Node

</td><td>

Single computing resource which is logically/operationally bound into a cluster.

</td></tr><tr><td>

cmdb\_ci\_cluster\_resource

</td><td>

Cluster Resource

</td><td>

System object that is a set or grouping of cluster resources that are used to manage events that occur in a clustered environment.

</td></tr><tr><td>

cmdb\_ci\_cluster\_vip

</td><td>

Cluster Virtual IP

</td><td>

Cluster VIP information.

</td></tr><tr><td>

cmdb\_ci\_cmp\_price\_product\_base

</td><td>

Cloud Product Price Base

</td><td>

Used to calculate the approximate monthly cost of running a stack built on Virtual Servers in cloud environment:

-   Cloud Price Base: Common price base to store pricing info of all the resources of all the supported clouds.
-   Cloud Price Product Base: Base table to store the common attributes of all the pricing resources.
-   VM Instance Price: Specific table that extends the Cloud Price Product base to store the VM specific product info of all the supported clouds.

 Parent class for cloud product prices such as VM instance price.

</td></tr><tr><td>

cmdb\_ci\_cmp\_resource

</td><td>

Cloud Resource

</td><td>

Generic cloud resources.

</td></tr><tr><td>

cmdb\_ci\_comm

</td><td>

Communication Device

</td><td>

Communication devices information. A choice list containing devices such as cellphone, phone, conference phone, and Wi-Fi.

</td></tr><tr><td>

cmdb\_ci\_computer

</td><td>

Computer

</td><td>

An extension of the Hardware table, capturing computer properties.

</td></tr><tr><td>

cmdb\_ci\_computer\_room

</td><td>

Computer Room

</td><td>

Logical representation of a computer room.

</td></tr><tr><td>

cmdb\_ci\_config\_automation\_server

</td><td>

Management Server

</td><td>

Dev Ops tools such as Chef and Puppet, that are used to manage server configurations.

 Parent class for application management servers.

</td></tr><tr><td>

cmdb\_ci\_config\_file

</td><td>

Configuration file

</td><td>

Configuration files which establish the parameters and initial settings for some computer programs.

</td></tr><tr><td>

cmdb\_ci\_crac

</td><td>

Computer Room AC

</td><td>

Air conditioning units used to cool data centers.

</td></tr><tr><td>

cmdb\_ci\_csu\_dsu\_network

</td><td>

CSU/DSU

</td><td>

Digital-interface device used to connect networking equipment to a digital circuit.

</td></tr><tr><td>

cmdb\_ci\_database

</td><td>

Database

</td><td>

Organized collection of data such as the set of files where data is stored, the reason for a database, and the metadata about the data.

</td></tr><tr><td>

cmdb\_ci\_datacenter

</td><td>

Data Center

</td><td>

Facility used to house computer systems and associated components, such as telecommunications and storage systems. It generally includes redundant or backup power supplies, redundant data communications connections, environmental controls \(such as air conditioning and fire suppression\), and various security devices.

</td></tr><tr><td>

cmdb\_ci\_datapower\_server

</td><td>

Data Power Hosting Server

</td><td>

Server running IBM DataPower Gateway software.

</td></tr><tr><td>

cmdb\_ci\_datastore

</td><td>

Datastore

</td><td>

Datastores are like file systems, abstracting the physical storage and providing a model for storing files. The child class represents the VMware specific Datastore.

 Parent class for VMWare datastore object types such as vCenter Datastores.

</td></tr><tr><td>

cmdb\_ci\_db\_catalog

</td><td>

Database Catalog

</td><td>

Metadata which defines database objects such as base tables, views \(virtual tables\), synonyms, value ranges, indexes, users, and user groups, for a specific database instance.

</td></tr><tr><td>

cmdb\_ci\_db\_db2\_catalog

</td><td>

DB2 Catalog

</td><td>

Database catalog for DB2 database.

</td></tr><tr><td>

cmdb\_ci\_db\_db2\_instance

</td><td>

DB2 Instance

</td><td>

Instance of a DB2 database.

</td></tr><tr><td>

cmdb\_ci\_db\_hbase\_instance

</td><td>

HBase Instance

</td><td>

Instance of an HBase database.

</td></tr><tr><td>

cmdb\_ci\_db\_instance

</td><td>

Database Instance

</td><td>

Software and memory used to manipulate data in a database.

</td></tr><tr><td>

cmdb\_ci\_db\_mongodb\_instance

</td><td>

MongoDB Instance

</td><td>

Instance of a MongoDB database.

</td></tr><tr><td>

cmdb\_ci\_db\_mssql\_analysis

</td><td>

SQL Server Analysis Services

</td><td>

Microsoft SQL Server Analysis Services software.

</td></tr><tr><td>

cmdb\_ci\_db\_mssql\_catalog

</td><td>

MSFT SQL Catalog

</td><td>

Database catalog for a specific instance of a Microsoft SQL database.

</td></tr><tr><td>

cmdb\_ci\_db\_mssql\_instance

</td><td>

MSFT SQL Instance

</td><td>

Microsoft SQL instance.

</td></tr><tr><td>

cmdb\_ci\_db\_mssql\_int\_job

</td><td>

SQL Server Integration Services Job

</td><td>

Scheduled job to run a SQL Server Integration Service package.

</td></tr><tr><td>

cmdb\_ci\_db\_mssql\_integration

</td><td>

SQL Server Integration Services

</td><td>

MSQL Server Integration Services software.

</td></tr><tr><td>

cmdb\_ci\_db\_mssql\_reporting

</td><td>

SQL Server Reporting Services

</td><td>

SQL Server software used for server-based reporting generation.

</td></tr><tr><td>

cmdb\_ci\_db\_mysql\_catalog

</td><td>

MySQL Catalog

</td><td>

Database catalog for a specific instance of a MySQL database.

</td></tr><tr><td>

cmdb\_ci\_db\_mysql\_clustermgnode

</td><td>

MySQLClusterMGMNode

</td><td>

MySQL primary administrative interface to a running cluster.

</td></tr><tr><td>

cmdb\_ci\_db\_mysql\_clusternode

</td><td>

MySQLClusterDataNode

</td><td>

Summary table used in the \[ndbd\] or \[ndbd default\] sections of a config.ini file for configuring MySQL Cluster data nodes.

</td></tr><tr><td>

cmdb\_ci\_db\_mysql\_instance

</td><td>

MySQL Instance

</td><td>

Instance of a MySQL database.

</td></tr><tr><td>

cmdb\_ci\_db\_ora\_catalog

</td><td>

Oracle Catalog

</td><td>

Database catalog for a specific instance of an Oracle database.

</td></tr><tr><td>

cmdb\_ci\_db\_ora\_instance

</td><td>

Oracle Instance

</td><td>

Instance of an Oracle database.

</td></tr><tr><td>

cmdb\_ci\_db\_ora\_listener

</td><td>

Oracle Database Listener

</td><td>

Process that runs on an Oracle Database Server.

</td></tr><tr><td>

cmdb\_ci\_db\_postgresql\_instance

</td><td>

PostgreSQL Instance

</td><td>

Instance of a PostgreSQL database.

</td></tr><tr><td>

cmdb\_ci\_db\_syb\_catalog

</td><td>

Sybase Catalog

</td><td>

Database catalog for a specific instance of a Sybase database.

</td></tr><tr><td>

cmdb\_ci\_db\_syb\_instance

</td><td>

Sybase Instance

</td><td>

Instance of a Sybase database.

</td></tr><tr><td>

cmdb\_ci\_desktop\_software

</td><td>

Desktop Software

</td><td>

Software used on desktops and laptops.

</td></tr><tr><td>

cmdb\_ci\_dir\_policy\_server

</td><td>

Policy Server

</td><td>

Policy server, which provides a security component of a policy-based network that provides authorization services and facilitates tracking and control of files.

</td></tr><tr><td>

cmdb\_ci\_dir\_site\_minder\_server

</td><td>

Site Minder

</td><td>

Server running SiteMinder software.

</td></tr><tr><td>

cmdb\_ci\_directory\_ad\_forest

</td><td>

AD Forest

</td><td>

Active Directory forest.

</td></tr><tr><td>

cmdb\_ci\_directory\_ha

</td><td>

HA Proxy

</td><td>

HAProxy software.

</td></tr><tr><td>

cmdb\_ci\_directory\_iifp

</td><td>

IIFP

</td><td>

Identity Identification Feature Pack \(Active Directory\) software.

</td></tr><tr><td>

cmdb\_ci\_directory\_ldap

</td><td>

LDAP DB

</td><td>

LDAP \(Lightweight Directory Access Protocol\) database software.

</td></tr><tr><td>

cmdb\_ci\_directory\_server

</td><td>

Directory Server

</td><td>

Server running LDAP software.

</td></tr><tr><td>

cmdb\_ci\_disk

</td><td>

Disk

</td><td>

General category of data storage mechanisms.

</td></tr><tr><td>

cmdb\_ci\_disk\_partition

</td><td>

Disk Partition

</td><td>

Sections of a disk separated so that information in each section can be managed separately.

</td></tr><tr><td>

cmdb\_ci\_display\_hardware

</td><td>

Display Hardware

</td><td>

Hardware used to display information in visual form.

</td></tr><tr><td>

cmdb\_ci\_dns\_alias

</td><td>

DNS Alias

</td><td>

Synonym for the host used to resolve DNS addresses.

</td></tr><tr><td>

cmdb\_ci\_dns\_name

</td><td>

DNS Name

</td><td>

Primary DNS names.

</td></tr><tr><td>

cmdb\_ci\_docker

</td><td>

Docker Container

</td><td>

Docker containers \(a runtime instance of a docker image\).

</td></tr><tr><td>

cmdb\_ci\_docker\_engine

</td><td>

Docker Engine

</td><td>

Docker software for running and managing Docker containers.

</td></tr><tr><td>

cmdb\_ci\_docker\_image

</td><td>

Docker Image

</td><td>

Docker images. Ordered collection of root filesystem changes and the corresponding execution parameters for use within a container runtime.

</td></tr><tr><td>

cmdb\_ci\_docker\_image\_tag

</td><td>

Docker Image Tag

</td><td>

Docker tag, which is a label applied to a Docker image in a repository.

</td></tr><tr><td>

cmdb\_ci\_docker\_local\_image

</td><td>

Docker Local Image

</td><td>

Locally managed Docker image.

</td></tr><tr><td>

cmdb\_ci\_drs\_vm\_config

</td><td>

DRS VM Config

</td><td>

Distributed Resource Scheduler \(DRS\) behavior for the VMs in the vCenter that override the cluster behavior.

</td></tr><tr><td>

cmdb\_ci\_ec2\_instance

</td><td>

EC2 Virtual Machine Instance

</td><td>

Virtual machine running in the Amazon Elastic Compute Cloud \(EC2\) platform.

</td></tr><tr><td>

cmdb\_ci\_email\_server

</td><td>

Email Server

</td><td>

Server running email software.

</td></tr><tr><td>

cmdb\_ci\_email\_server\_jes

</td><td>

JES

</td><td>

Server running JES software \(multi-featured hybrid MTA/MDA server\).

</td></tr><tr><td>

cmdb\_ci\_endpoint

</td><td>

Endpoint

</td><td>

Endpoint, which represents the entry point to a service, a process, or a queue or topic destination in service-oriented architecture.

</td></tr><tr><td>

cmdb\_ci\_environment

</td><td>

Environment

</td><td>

Logical grouping of hardware and software used to develop, test, and deliver computing services. For example: development, test, quality assurance, and production.

</td></tr><tr><td>

cmdb\_ci\_esx\_resource\_pool

</td><td>

ESX Resource Pool

</td><td>

VMware set of physical resources.

</td></tr><tr><td>

cmdb\_ci\_esx\_server

</td><td>

ESX Server

</td><td>

Physical ESX server running the VMware ESXi operating system.

</td></tr><tr><td>

cmdb\_ci\_exchange\_backend

</td><td>

ExchangeBackEndServer

</td><td>

Server running Exchange software.

</td></tr><tr><td>

cmdb\_ci\_exchange\_cas

</td><td>

Exchange Client Access Server

</td><td>

Server running Exchange software providing client access services.

</td></tr><tr><td>

cmdb\_ci\_exchange\_edge\_transport\_server

</td><td>

Exchange Edge Transport Server

</td><td>

Server running Exchange Edge Transport software.

</td></tr><tr><td>

cmdb\_ci\_exchange\_frontend

</td><td>

ExchangeFrontEndServer

</td><td>

Server running Exchange software.

</td></tr><tr><td>

cmdb\_ci\_exchange\_hub

</td><td>

ExchangeHub

</td><td>

Server running Exchange Hub software.

</td></tr><tr><td>

cmdb\_ci\_exchange\_hub\_transport\_server

</td><td>

Exchange Hub Transport Server

</td><td>

Server running Exchange Hub software providing transport services.

</td></tr><tr><td>

cmdb\_ci\_exchange\_mailbox

</td><td>

Exchange MailBox

</td><td>

Exchange email account.

</td></tr><tr><td>

cmdb\_ci\_exchange\_mailbox\_server

</td><td>

Exchange Mailbox Server

</td><td>

Server running Exchange software providing client access services.

</td></tr><tr><td>

cmdb\_ci\_exchange\_service\_component

</td><td>

Exchange Service Component

</td><td>

Exchange Service Component software.

</td></tr><tr><td>

cmdb\_ci\_facility\_hardware

</td><td>

Facility Hardware

</td><td>

Base class for hardware used to facilities services such as electric, water, sewer, air, and security.

</td></tr><tr><td>

cmdb\_ci\_fc\_disk

</td><td>

Fibre Channel Disk

</td><td>

Base table for fibre channel disk.

</td></tr><tr><td>

cmdb\_ci\_fc\_export

</td><td>

Fibre Channel Export

</td><td>

Storage volume exported by a storage server via Fibre Channel protocol.

</td></tr><tr><td>

cmdb\_ci\_fc\_port

</td><td>

Fibre Channel Port

</td><td>

Fibre Channel port on a storage server, FC switch, or on a host's HBA.

</td></tr><tr><td>

cmdb\_ci\_fddi\_network

</td><td>

FDDI Cards

</td><td>

Fiber Distributed Data Interface cards.

</td></tr><tr><td>

cmdb\_ci\_file\_system

</td><td>

File System

</td><td>

File system information for a server, capturing details such as mount point, capacity, and type of file system.

</td></tr><tr><td>

cmdb\_ci\_file\_system\_nfs

</td><td>

NFS File system

</td><td>

Extension of File System, which provides NFS file system information.

</td></tr><tr><td>

cmdb\_ci\_file\_system\_smb

</td><td>

SMB File system

</td><td>

Extension of File System, which provides SMB file system information.

</td></tr><tr><td>

cmdb\_ci\_firewall\_network

</td><td>

Firewall Hardware

</td><td>

Firewall hardware.

</td></tr><tr><td>

cmdb\_ci\_ftp\_server

</td><td>

FTP Server

</td><td>

Server providing FTP services.

</td></tr><tr><td>

cmdb\_ci\_fuel\_tank

</td><td>

Fuel Tank

</td><td>

Fuel tank.

</td></tr><tr><td>

cmdb\_ci\_generator\_power\_eq

</td><td>

Power Generator

</td><td>

Power generator.

</td></tr><tr><td>

cmdb\_ci\_group

</td><td>

Group

</td><td>

Logical group of CIs.

</td></tr><tr><td>

cmdb\_ci\_hardware

</td><td>

Hardware

</td><td>

Base class for hardware.

</td></tr><tr><td>

cmdb\_ci\_host\_cluster

</td><td>

Host Cluster

</td><td>

Cloud agnostic way of representing a group of hosts as a cluster. The child class represents VMware vCenter Cluster specific details.

 Parent class for VMWare host cluster object types such as vCenter Clusters.

</td></tr><tr><td>

cmdb\_ci\_hpux\_server

</td><td>

HPUX Server

</td><td>

Server running HPUX software.

</td></tr><tr><td>

cmdb\_ci\_hub\_network

</td><td>

Hub Hardware

</td><td>

Physical network hub.

</td></tr><tr><td>

cmdb\_ci\_hvac

</td><td>

HVAC Equipment

</td><td>

Heating, ventilation, and air conditioning equipment.

</td></tr><tr><td>

cmdb\_ci\_hyper\_v\_cluster

</td><td>

Hyper-V Cluster

</td><td>

Cluster of the Hyper-V servers.

</td></tr><tr><td>

cmdb\_ci\_hyper\_v\_instance

</td><td>

Hyper-V Virtual Machine Instance

</td><td>

Hyper-V virtual machine instance. This table extends the generic Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] table.

</td></tr><tr><td>

cmdb\_ci\_hyper\_v\_network

</td><td>

Hyper-V Virtual Network

</td><td>

Hyper-V virtual network.

</td></tr><tr><td>

cmdb\_ci\_hyper\_v\_object

</td><td>

Hyper-V Object

</td><td>

Base class for all Hyper-V objects.

</td></tr><tr><td>

cmdb\_ci\_hyper\_v\_resource\_pool

</td><td>

Hyper-V Resource Pool

</td><td>

Hyper-V resource pool.

</td></tr><tr><td>

cmdb\_ci\_hyper\_v\_rpool\_comp

</td><td>

Hyper-V Resource Pool Component

</td><td>

Resource pool component belonging to resource pool.

</td></tr><tr><td>

cmdb\_ci\_hyper\_v\_server

</td><td>

Hyper-V Server

</td><td>

Server running Hyper-V software.

</td></tr><tr><td>

cmdb\_ci\_ids\_network

</td><td>

Intrusion Detection System

</td><td>

Security intrusion detection systems.

</td></tr><tr><td>

cmdb\_ci\_iisdirectory

</td><td>

IIS Virtual Directory

</td><td>

Virtual Directory in IIS Manager.

</td></tr><tr><td>

cmdb\_ci\_imaging\_hardware

</td><td>

Imaging Hardware

</td><td>

Hardware used to create electronic/physical images.

</td></tr><tr><td>

cmdb\_ci\_inetinfo

</td><td>

Inetinfo service

</td><td>

Inetinfo service of IIS application.

</td></tr><tr><td>

cmdb\_ci\_inf\_software

</td><td>

Infrastructure Software

</td><td>

Base class for enterprise software or programs specifically designed to help business organizations perform basic tasks such as workforce support, business transactions and internal services, and processes.

</td></tr><tr><td>

cmdb\_ci\_information\_object

</td><td>

Information Object

</td><td>

Types of information that a business application or any other entity handles.

 For example: 'Employee Salary Data', Employee Personal Data', and 'Sales Data'.

 For more information, see [CSDM implementation stage — Fly](../../csdm-implementation/concept/csdm-implement-fly-stage.md) and [Enterprise Architecture \(formerly Application Portfolio Management\) and CSDM tables - Legacy](https://www.servicenow.com/docs/access?context=apm-use-case&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).

</td></tr><tr><td>

cmdb\_ci\_installed\_bundles

</td><td>

Installed Bundles

</td><td>

Extension of the Virtual Machine Object \[cmdb\_ci\_vm\_object\] table, which represents bundles of installed software.

</td></tr><tr><td>

cmdb\_ci\_infra\_service

</td><td>

Infrastructure Service

</td><td>

IT services which support providing computing infrastructure.

</td></tr><tr><td>

cmdb\_ci\_infra\_service\_ldap

</td><td>

LDAP Service

</td><td>

Running LDAP service.

</td></tr><tr><td>

cmdb\_ci\_ip\_address

</td><td>

IP Address

</td><td>

IP address.

</td></tr><tr><td>

cmdb\_ci\_ip\_device

</td><td>

IP Device

</td><td>

Base class for devices with an IP address.

</td></tr><tr><td>

cmdb\_ci\_ip\_firewall

</td><td>

IP Firewall

</td><td>

Firewall hardware.

</td></tr><tr><td>

cmdb\_ci\_ip\_network

</td><td>

IP Network

</td><td>

IP network information capturing details such as subnet, router, and router\_interface\_type.

</td></tr><tr><td>

cmdb\_ci\_ip\_phone

</td><td>

IP Phone

</td><td>

IP-enabled \(VOIP\) phone.

</td></tr><tr><td>

cmdb\_ci\_ip\_router

</td><td>

IP Router

</td><td>

Specialization of the Network Gear \[cmdb\_ci\_netgear\] table.

</td></tr><tr><td>

cmdb\_ci\_ip\_server

</td><td>

IP Server

</td><td>

Server hardware.

</td></tr><tr><td>

cmdb\_ci\_ip\_service

</td><td>

IP Service Instance

</td><td>

Base table for IP services running on a server such as Unix daemon or Windows service.

</td></tr><tr><td>

cmdb\_ci\_ip\_switch

</td><td>

IP Switch

</td><td>

Specialization of the Network Gear \[cmdb\_ci\_netgear\] table.

</td></tr><tr><td>

cmdb\_ci\_iplanet\_web\_server

</td><td>

Iplanet Web Server

</td><td>

Server running Oracle iPlanet Web Server \(OiWS\) software.

</td></tr><tr><td>

cmdb\_ci\_isam\_server

</td><td>

ISAM Server

</td><td>

Server running ISAM software.

</td></tr><tr><td>

cmdb\_ci\_iscsi\_disk

</td><td>

iSCSI Disk

</td><td>

Host mount of an iSCSI disk.

</td></tr><tr><td>

cmdb\_ci\_iscsi\_export

</td><td>

iSCSI Export

</td><td>

Storage volume exported by a storage server via iSCSI.

</td></tr><tr><td>

cmdb\_ci\_kubernetes\_component

</td><td>

Kubernetes Component

</td><td>

Kubernetes cluster, ingress, namespace, node, pod, service, volume, and workload. Also represents open shift build conf, deployment conf, docker images repository, group, images, stream, project, route, and user.

 Parent class for Kubernetes components such as Pods and Clusters.

</td></tr><tr><td>

cmdb\_ci\_kvm

</td><td>

KVM

</td><td>

Hypervisor that manages kernel-based virtual machines \(KVMs\).

</td></tr><tr><td>

cmdb\_ci\_kvm\_network

</td><td>

Network

</td><td>

KVM Virtual network.

</td></tr><tr><td>

cmdb\_ci\_kvm\_object

</td><td>

KVM Object

</td><td>

Base object for all KVM objects.

</td></tr><tr><td>

cmdb\_ci\_kvm\_storage\_pool

</td><td>

Storage Pool

</td><td>

KVM storage pool.

</td></tr><tr><td>

cmdb\_ci\_kvm\_storage\_volume

</td><td>

Storage Volume

</td><td>

KVM storage volume.

</td></tr><tr><td>

cmdb\_ci\_kvm\_vm\_instance

</td><td>

KVM Virtual Machine Instance

</td><td>

Virtual machine instance running on a KVM hypervisor.

</td></tr><tr><td>

cmdb\_ci\_lb

</td><td>

Load Balancer

</td><td>

Server functioning as a load balancer.

</td></tr><tr><td>

cmdb\_ci\_lb\_a10

</td><td>

A10 Load Balancer

</td><td>

Server functioning as an A10 load balancer.

</td></tr><tr><td>

cmdb\_ci\_lb\_ace

</td><td>

ACE

</td><td>

Server functioning as an ACE load balancer.

</td></tr><tr><td>

cmdb\_ci\_lb\_alteon

</td><td>

Alteon

</td><td>

Server functioning as an Alteon load balancer.

</td></tr><tr><td>

cmdb\_ci\_lb\_appl

</td><td>

Load Balancer Application

</td><td>

Application that provides load balancing functionality.

</td></tr><tr><td>

cmdb\_ci\_lb\_backend\_server

</td><td>

LB Backend Server

</td><td>

Server functioning as a backend load balancer.

</td></tr><tr><td>

cmdb\_ci\_lb\_bigip

</td><td>

F5 BIG-IP

</td><td>

Server functioning as an F5 BIG-IP load balancer.

</td></tr><tr><td>

cmdb\_ci\_lb\_cisco\_csm

</td><td>

Cisco CSM

</td><td>

Server functioning as a Cisco CSM load balancer.

</td></tr><tr><td>

cmdb\_ci\_lb\_cisco\_css

</td><td>

Cisco CSS

</td><td>

Server functioning as a Cisco CSS load balancer.

</td></tr><tr><td>

cmdb\_ci\_lb\_f5\_gtm

</td><td>

F5 BigIP GTM

</td><td>

Server functioning as an F5 BigIP GTM load balancer.

</td></tr><tr><td>

cmdb\_ci\_lb\_f5\_ltm

</td><td>

F5 BigIP LTM

</td><td>

Server functioning as an F5 BigIP LTM load balancer.

</td></tr><tr><td>

cmdb\_ci\_lb\_haproxy

</td><td>

HAProxy Load Balancer

</td><td>

Server functioning as an HA Proxy load balancer.

</td></tr><tr><td>

cmdb\_ci\_lb\_isa

</td><td>

ISA Server

</td><td>

Server functioning as an ISA load balancer.

</td></tr><tr><td>

cmdb\_ci\_lb\_modjk

</td><td>

Modjk Load Balancer

</td><td>

Server functioning as a Cisco CSM load balancer.

</td></tr><tr><td>

cmdb\_ci\_lb\_modproxy

</td><td>

ModProxy Load Balancer

</td><td>

Server functioning as a ModProxy load balancer.

</td></tr><tr><td>

cmdb\_ci\_lb\_netscaler

</td><td>

Citrix Netscaler

</td><td>

Server functioning as a Citrix Netscaler load balancer.

</td></tr><tr><td>

cmdb\_ci\_lb\_network

</td><td>

Network Load Balancer

</td><td>

Server performing network load balancing.

</td></tr><tr><td>

cmdb\_ci\_lb\_nginx

</td><td>

Nginx Load Balancer

</td><td>

Server functioning as an Nginx load balancer.

</td></tr><tr><td>

cmdb\_ci\_lb\_pool

</td><td>

Load Balancer Pool

</td><td>

Collection of host-to-port mappings to be balanced.

</td></tr><tr><td>

cmdb\_ci\_lb\_pool\_member

</td><td>

Load Balancer Pool Member

</td><td>

Host-to-port mapping of a request to be balanced.

</td></tr><tr><td>

cmdb\_ci\_lb\_radware

</td><td>

Radware Load Balancer

</td><td>

Server functioning as a Radware load balancer.

</td></tr><tr><td>

cmdb\_ci\_lb\_service

</td><td>

Load Balancer Service

</td><td>

Virtual service that the device balances by forwarding requests to members within a pool.

</td></tr><tr><td>

cmdb\_ci\_lb\_template

</td><td>

Load Balancer Template

</td><td>

Load balancer template which contains load balancer-related configuration settings for a specific type of network traffic.

</td></tr><tr><td>

cmdb\_ci\_lif

</td><td>

LIF

</td><td>

Logical interface.

</td></tr><tr><td>

cmdb\_ci\_lb\_vlan

</td><td>

Load Balancer VLAN

</td><td>

Virtual LAN segment.

</td></tr><tr><td>

cmdb\_ci\_linux\_server

</td><td>

Linux Server

</td><td>

Server running Linux software.

</td></tr><tr><td>

cmdb\_ci\_logical\_datacenter

</td><td>

Logical Datacenter

</td><td>

VMware vCenter logical datacenter.

</td></tr><tr><td>

cmdb\_ci\_lpar

</td><td>

Logical Partition

</td><td>

Logical partition, commonly called an LPAR, is a subset of a computer's hardware resources, virtualized as a separate computer.

</td></tr><tr><td>

cmdb\_ci\_lvm\_pool

</td><td>

LVM Pool

</td><td>

Linux Volume Manager storage pool.

</td></tr><tr><td>

cmdb\_ci\_lvm\_pool\_member

</td><td>

LVM Pool Member

</td><td>

Linux Volume Manager storage pool member.

</td></tr><tr><td>

cmdb\_ci\_mainframe

</td><td>

IBM Mainframe

</td><td>

IBM large-scale computer system.

</td></tr><tr><td>

cmdb\_ci\_mainframe\_hardware

</td><td>

Mainframe Hardware

</td><td>

The hardware components of a large-scale computer system.

</td></tr><tr><td>

cmdb\_ci\_mainframe\_lpar

</td><td>

IBM Mainframe LPAR

</td><td>

Logical partition, which is commonly called an LPAR, and is a subset of a mainframes computer's hardware resources, virtualized as a separate computer.

</td></tr><tr><td>

cmdb\_ci\_memory\_module

</td><td>

Memory Module

</td><td>

Circuit board that provides for memory storage.

</td></tr><tr><td>

cmdb\_ci\_mfp\_printer

</td><td>

Multi-function Printer

</td><td>

Physical device with scan, copy, and fax capabilities.

</td></tr><tr><td>

cmdb\_ci\_microsoft\_iis\_web\_server

</td><td>

Microsoft iis Web Server

</td><td>

Server running Internet Information Services \(IIS\) for Windows software.

</td></tr><tr><td>

cmdb\_ci\_modem\_network

</td><td>

Modem Hardware

</td><td>

Physical modem hardware.

</td></tr><tr><td>

cmdb\_ci\_mpio\_pool

</td><td>

Multipath IO Pool

</td><td>

Multipath IO pool, representing multiple redundant paths to storage.

</td></tr><tr><td>

cmdb\_ci\_mpio\_pool\_group

</td><td>

Multipath IO Pool Group

</td><td>

Group of multipath IO pools.

</td></tr><tr><td>

cmdb\_ci\_mpio\_pool\_path

</td><td>

Multipath IO Pool Path

</td><td>

Single path in an MPIO pool.

</td></tr><tr><td>

cmdb\_ci\_msd

</td><td>

Mass Storage Device

</td><td>

Physical storage device.

</td></tr><tr><td>

cmdb\_ci\_nas\_file\_system

</td><td>

NAS File System

</td><td>

Extension of the File System \[cmdb\_ci\_file\_system\] table, representing network attached storage.

</td></tr><tr><td>

cmdb\_ci\_nat\_gateway

</td><td>

NAT Gateway

</td><td>

Functionality for NAT gateway.

</td></tr><tr><td>

cmdb\_ci\_netapp\_cdot

</td><td>

NetApp CDOT

</td><td>

Functionality of NetApp Clustered Data OnTap operating system

</td></tr><tr><td>

cmdb\_ci\_netapp\_datacenter

</td><td>

NetApp Datacenter

</td><td>

NetApp logical datacenter.

</td></tr><tr><td>

cmdb\_ci\_netapp\_svm

</td><td>

NetApp SVM

</td><td>

NetApp Storage Virtual Machine.

</td></tr><tr><td>

cmdb\_ci\_netapp\_volume

</td><td>

NetApp Volume

</td><td>

NetApp FlexVol storage volume.

</td></tr><tr><td>

cmdb\_ci\_net\_app\_server

</td><td>

Network Appliance Hardware

</td><td>

Server configured to perform as a networking appliance.

</td></tr><tr><td>

cmdb\_ci\_netgear

</td><td>

Network Gear

</td><td>

Extension of the Hardware table, that captures network equipment such as router, switch, hub, gateway, and bridge.

</td></tr><tr><td>

cmdb\_ci\_netware\_server

</td><td>

Netware Server

</td><td>

Server running NetWare software.

</td></tr><tr><td>

cmdb\_ci\_network

</td><td>

Cloud Network

</td><td>

VMware vCenter cloud network.

</td></tr><tr><td>

cmdb\_ci\_network \_acl

</td><td>

Network ACL

</td><td>

Network access control list \(ACL\).

</td></tr><tr><td>

cmdb\_ci\_network\_acl\_rule

</td><td>

Network ACL Rule

</td><td>

Rule used to control networking access rights.

</td></tr><tr><td>

cmdb\_ci\_network\_adapter

</td><td>

Network Adapter

</td><td>

Network adapter hardware.

</td></tr><tr><td>

cmdb\_ci\_network\_policy\_group

</td><td>

Network Policy Group

</td><td>

Group policy consumed by Active Directory services.

</td></tr><tr><td>

cmdb\_ci\_network\_template

</td><td>

Network Template

</td><td>

OpenStack file used to configure a network.

</td></tr><tr><td>

cmdb\_ci\_nic

</td><td>

Cloud Mgmt Network Interface

</td><td>

Virtual network adapter.

</td></tr><tr><td>

cmdb\_ci\_nginx\_web\_server

</td><td>

Nginx Web Server

</td><td>

Server running Nginx software.

</td></tr><tr><td>

cmdb\_ci\_openstack\_datacenter

</td><td>

OpenStack Datacenter

</td><td>

OpenStack logical datacenter.

</td></tr><tr><td>

cmdb\_ci\_optical\_transport

 \(Installed with the com.snc.cmdb.telecom.category plugin\)

</td><td>

Fiber Optic Equipment

</td><td>

Fiber optics which are used for long-distance and high-performance data networking. Fiber optics are commonly used in telecommunication services such as internet, television, and telephones.

 Child class of Transport Hardware and parent class for telecom fiber optic equipment such as optical multiplexers and terminal equipment.

</td></tr><tr><td>

cmdb\_ci\_oslv\_container

</td><td>

Operating-system-level Virtualization Container

</td><td>

Containers \(a runtime instance of a docker image\).

</td></tr><tr><td>

cmdb\_ci\_oslv\_engine

</td><td>

Operating-system-level Virtualization Engine

</td><td>

Software for running and managing containers.

</td></tr><tr><td>

cmdb\_ci\_oslv\_image

</td><td>

Operating-system-level Virtualization Image

</td><td>

Container images. Ordered collection of root filesystem changes and the corresponding execution parameters for use within a container runtime.

</td></tr><tr><td>

cmdb\_ci\_oslv\_image\_tag

</td><td>

Operating-system-level Virtualization Image Tag

</td><td>

Container tag, which is a label applied to a container image in a repository.

</td></tr><tr><td>

cmdb\_ci\_oslv\_local\_image

</td><td>

Operating-system-level Virtualization Local Image

</td><td>

Locally managed container image.

</td></tr><tr><td>

cmdb\_ci\_osx\_server

</td><td>

OS/X Server

</td><td>

Server running OS/X operating system.

</td></tr><tr><td>

cmdb\_ci\_os\_template

</td><td>

Image

</td><td>

Software files used to create a new instance of a compute resource such as server, desktop, virtual machine, and virtual router.

</td></tr><tr><td>

cmdb\_ci\_outofband\_device

</td><td>

Out-of-Band Device

</td><td>

Hardware used to perform out-of-band management.

</td></tr><tr><td>

cmdb\_ci\_patches

</td><td>

Patch

</td><td>

Patch software to fix or improve a computer program or its supporting data.

</td></tr><tr><td>

cmdb\_ci\_pc\_hardware

</td><td>

Personal Computer

</td><td>

Multi-purpose electronic computer whose size, capabilities, and price make it feasible for individual use.

</td></tr><tr><td>

cmdb\_ci\_pcf\_component

</td><td>

CloudFoundry Component

</td><td>

Cloud Foundry provides a highly efficient, modern model for cloud native application delivery on top of Kubernetes. Component represents application, domain, organization, quota, routes, service, service plan, space, and space instances.

 Parent class for price base of cloud products such as virtual machines.

</td></tr><tr><td>

cmdb\_ci\_pdu

</td><td>

PDU

</td><td>

Power distribution unit \(PDU\).

</td></tr><tr><td>

cmdb\_ci\_pdu\_outlet

</td><td>

Outlet

</td><td>

Single outlet of a PDU.

</td></tr><tr><td>

cmdb\_ci\_peripheral

</td><td>

Computer Peripheral

</td><td>

Various computer peripherals such as monitor, docking station, KVM switch, projector, scanner, keyboard, mouse, and UPS.

</td></tr><tr><td>

cmdb\_ci\_personal\_printer

</td><td>

Personal Printer

</td><td>

Printer whose size,capabilities and price make it feasible for individual use.

</td></tr><tr><td>

cmdb\_ci\_plotter

</td><td>

Plotter

</td><td>

Printer with capabilities to print large vector graphic images.

</td></tr><tr><td>

cmdb\_ci\_power\_eq

</td><td>

Power Equipment

</td><td>

Hardware used to manage electrical power.

</td></tr><tr><td>

cmdb\_ci\_port

</td><td>

Port

</td><td>

Interface between a computer and other electronic devices.

</td></tr><tr><td>

cmdb\_ci\_port\_group

</td><td>

Port Group

</td><td>

Group of ports on a virtual switch.

</td></tr><tr><td>

cmdb\_ci\_print\_queue

</td><td>

Puppet Primary

</td><td>

Print queue, which is a list of printer output jobs held in a reserved memory area, including the most current status of all active and pending print jobs.

</td></tr><tr><td>

cmdb\_ci\_printer

</td><td>

Printer

</td><td>

Physical device which makes a persistent human-readable representation of graphics or text on paper or similar physical media.

</td></tr><tr><td>

cmdb\_ci\_printing\_hardware

</td><td>

Printing Hardware

</td><td>

Physical device which makes a persistent human-readable representation of graphics or text on paper or similar physical media.

</td></tr><tr><td>

cmdb\_ci\_puppet\_master

</td><td>

 

</td><td>

Server running PuppetMaster application.

</td></tr><tr><td>

cmdb\_ci\_qtree

</td><td>

Qtree

</td><td>

Qtree file system.

</td></tr><tr><td>

cmdb\_ci\_qualifier

</td><td>

Qualifier

</td><td>

Relation qualifier CIs which contain important information about CI relationships.

 In a relation qualifier, you can annotate arbitrary unique information about the relationship between two CIs. You can define multiple qualifiers for a single relationship, resulting in a qualifier chain. However, there can be only a single qualifier chain for a specific relationship type between two CIs.

 Parent class for the various relation qualifier types such as EntryPoint Markers and Boundary Connections.

</td></tr><tr><td>

cmdb\_ci\_rack

</td><td>

Rack

</td><td>

Datacenter racks containing details such as rack units, rack units in use, and power consumption.

</td></tr><tr><td>

cmdb\_ci\_raid

</td><td>

RAID

</td><td>

Storage pool using RAID mechanisms to ensure data integrity.

</td></tr><tr><td>

cmdb\_ci\_raid\_member

</td><td>

RAID Member

</td><td>

Member of storage pool using RAID mechanisms.

</td></tr><tr><td>

cmdb\_ci\_resource\_group

</td><td>

Resource Group

</td><td>

Resource pool is a logical abstraction for flexible management of resources.

</td></tr><tr><td>

cmdb\_ci\_sa\_scaling\_pol\_base

</td><td>

Scaling Policy

</td><td>

Parent class for virtual machines scaling policy options such as simple and dynamic.

</td></tr><tr><td>

cmdb\_ci\_san

</td><td>

Storage Area Network

</td><td>

Network which provides access to block level storage.

</td></tr><tr><td>

cmdb\_ci\_san\_connection

</td><td>

SAN Connection

</td><td>

Connection in a SAN network.

</td></tr><tr><td>

cmdb\_ci\_san\_disk

</td><td>

SAN Disk

</td><td>

Base table for the iSCSI Disk \[cmdb\_ci\_iscsi\_disk\] and the Fibre Channel Disk \[cmdb\_ci\_fc\_disk\] tables.

</td></tr><tr><td>

cmdb\_ci\_san\_endpoint

</td><td>

SAN Endpoint

</td><td>

One end of a SAN connection.

</td></tr><tr><td>

cmdb\_ci\_san\_export

</td><td>

SAN Export

</td><td>

Base table for the iSCSI Export \[cmdb\_ci\_iscsi\_export\] and the Fibre Channel Export \[cmdb\_ci\_fc\_export\] tables.

</td></tr><tr><td>

cmdb\_ci\_san\_fabric

</td><td>

SAN Fabric

</td><td>

Hardware that connects workstations and servers to storage devices in a SAN. Referred to as a "fabric."

</td></tr><tr><td>

cmdb\_ci\_san\_zone

</td><td>

SAN Zone

</td><td>

Subset of SAN storage that certain users are restricted to.

</td></tr><tr><td>

cmdb\_ci\_san\_zone\_alias

</td><td>

SAN Zone Alias

</td><td>

Collection of SAN zone members.

</td></tr><tr><td>

cmdb\_ci\_san\_zone\_alias\_member

</td><td>

SAN Zone Alias Member

</td><td>

M2m relationship between SAN zone aliases and SAN zone members.

</td></tr><tr><td>

cmdb\_ci\_san\_zone\_member

</td><td>

SAN Zone Member

</td><td>

Ports and devices in a SAN zone.

</td></tr><tr><td>

cmdb\_ci\_san\_zone\_set

</td><td>

SAN Zone Set

</td><td>

Collection of SAN zones.

</td></tr><tr><td>

cmdb\_ci\_scanner

</td><td>

Scanner

</td><td>

Hardware used to create digital images of paper documents.

</td></tr><tr><td>

cmdb\_ci\_server

</td><td>

Server

</td><td>

Base class for all types of servers.

</td></tr><tr><td>

cmdb\_ci\_server\_snapshot

</td><td>

Server Snapshot

</td><td>

Server snapshot, which is the state of a system at a particular point in time.

</td></tr><tr><td>

cmdb\_ci\_service

</td><td>

Service

</td><td>

IT Service that directly supports a Business Process \(ITIL\).

</td></tr><tr><td>

cmdb\_ci\_service\_auto

</td><td>

Service Instance

</td><td>

Services that can be monitored by the system, which in the base system, includes only application services. If Service Mapping is activated, there can also be records for dynamic CI groups. If Event Management is activated, there can be records for alert groups.

</td></tr><tr><td>

cmdb\_ci\_service\_business

</td><td>

Business Service

</td><td>

Business services are published to business users and typically underpin one or more business capabilities. Business services are often orderable by business users.

</td></tr><tr><td>

cmdb\_ci\_service\_discovered

</td><td>

Mapped Application Service

</td><td>

Application services, created by the Manual service population method. For each application service, there is a container CI record that models the application service.

</td></tr><tr><td>

cmdb\_ci\_service\_technical

</td><td>

Technology Management Service \(formerly Technical Service\)

</td><td>

Technology management services are published to service owners and typically underpin one or more business services. A technology management service may have an operational view made up of one or more technical management offerings.

</td></tr><tr><td>

cmdb\_ci\_solaris\_instance

</td><td>

Solaris Virtual Machine Instance

</td><td>

Virtual machine instance running Solaris software.

</td></tr><tr><td>

cmdb\_ci\_solaris\_server

</td><td>

Solaris Server

</td><td>

Physical server running Solaris software.

</td></tr><tr><td>

cmdb\_ci\_spkg

</td><td>

Software

</td><td>

Software package information containing details such as version, install count, license count, package name, and key \(when SAM enabled\).

</td></tr><tr><td>

cmdb\_ci\_storage\_controller

</td><td>

Storage Controller

</td><td>

Logical device that controls a storage volume or Fibre Channel port.

</td></tr><tr><td>

cmdb\_ci\_storage\_device

</td><td>

Storage Device

</td><td>

Base table for block storage devices such as DAS, SAN, and NAS.

</td></tr><tr><td>

cmdb\_ci\_storage\_disk

</td><td>

Storage Disk

</td><td>

Disk installed in a storage server.

</td></tr><tr><td>

cmdb\_ci\_storage\_export

</td><td>

Storage Export

</td><td>

Base table for the SAN Export \[cmdb\_ci\_san\_export\] table.

</td></tr><tr><td>

cmdb\_ci\_storage\_fileshare

</td><td>

Storage File Share

</td><td>

NAS file system on a storage server \(an exported file system\).

</td></tr><tr><td>

cmdb\_ci\_storage\_hba

</td><td>

Storage HBA

</td><td>

Host bust adapter for Fibre Channel. The physical device that provides Fibre Channel ports.

</td></tr><tr><td>

cmdb\_ci\_storage\_pool

</td><td>

Storage Pool

</td><td>

Logical collection of storage.

</td></tr><tr><td>

cmdb\_ci\_storage\_pool\_member

</td><td>

Storage Pool Member

</td><td>

Logical volume in a storage pool.

</td></tr><tr><td>

cmdb\_ci\_storage\_switch

</td><td>

Storage Switch

</td><td>

Fibre Channel switch.

</td></tr><tr><td>

cmdb\_ci\_storage\_volume

</td><td>

Storage Volume

</td><td>

Volume on a storage server.

</td></tr><tr><td>

cmdb\_ci\_storage\_vol\_snapshot

</td><td>

Storage Volume Snapshot

</td><td>

Server snapshot is the state of a system at a particular point in time.

</td></tr><tr><td>

cmdb\_ci\_subnet

</td><td>

Cloud Mgmt Subnet

</td><td>

Part of a larger network.

</td></tr><tr><td>

cmdb\_ci\_sun\_dir\_proxy\_server

</td><td>

Sun Directory Proxy Server

</td><td>

Server running Sun ONE Directory Proxy Server software.

</td></tr><tr><td>

cmdb\_ci\_sun\_ldap\_dir\_server

</td><td>

Sun LDAP Server

</td><td>

Server running Sun ONE Directory Server \(LDAP\) software.

</td></tr><tr><td>

cmdb\_ci\_surge\_power\_eq

</td><td>

Surger Protection Equipment

</td><td>

Power equipment used to prevent power surges.

</td></tr><tr><td>

cmdb\_ci\_tape\_server

</td><td>

Server Tape Unit

</td><td>

Hardware for using magnetic tape storage.

</td></tr><tr><td>

cmdb\_ci\_tomcat\_connector

</td><td>

Tomcat Connector

</td><td>

Software which provides web server plugins to connect web servers with Tomcat and other backends.

</td></tr><tr><td>

cmdb\_ci\_tower\_eq

</td><td>

Tower Equipment

</td><td>

Parent class for facility towers and tower equipment such as lights and beacons.

</td></tr><tr><td>

cmdb\_ci\_translation\_rule

</td><td>

NAT

</td><td>

Rules to allow router to remap one network address to another.

</td></tr><tr><td>

cmdb\_ci\_transport\_hardware

</td><td>

Transport Hardware

</td><td>

Telecommunication hardware used for digital communication and related hardware such as telecommunication racks, servers to connect port to LAN, relays, channel banks, and network circuit switch.

 Parent class for telecom transport hardware such as multiplexers and fiber optic equipment.

</td></tr><tr><td>

cmdb\_ci\_ucs\_blade

</td><td>

Cisco UCS Blade

</td><td>

Physical Cisco UCS Blade server hardware.

</td></tr><tr><td>

cmdb\_ci\_ucs\_chassis

</td><td>

Cisco UCS Chassis

</td><td>

Physical Cisco UCS chassis hardware used to hold Cisco UCS Blade server hardware.

</td></tr><tr><td>

cmdb\_ci\_ucs\_equipment

</td><td>

Cisco UCS Equipment

</td><td>

Cisco Unified Computing System \(UCS\) products.

</td></tr><tr><td>

cmdb\_ci\_unix\_cluster

</td><td>

UNIX Cluster

</td><td>

Set of computers clustered together to present a single Unix server resource.

</td></tr><tr><td>

cmdb\_ci\_unix\_daemon

</td><td>

UNIX Daemon

</td><td>

Long running Unix background process used to answer requests for services.

</td></tr><tr><td>

cmdb\_ci\_unix\_server

</td><td>

UNIX Server

</td><td>

Server running Unix software.

</td></tr><tr><td>

cmdb\_ci\_ups

</td><td>

UPS

</td><td>

Uninterrupted Power Supply devices, where devices are traditional UPS devices.

</td></tr><tr><td>

cmdb\_ci\_ups\_alarm

</td><td>

UPS Alarm

</td><td>

Uninterrupted Power Supply alarm.

</td></tr><tr><td>

cmdb\_ci\_ups\_bypass

</td><td>

UPS Bypass

</td><td>

Uninterrupted Power Supply bypass.

</td></tr><tr><td>

cmdb\_ci\_ups\_input

</td><td>

UPS Input

</td><td>

Electrical input to an Uninterrupted Power Supply device.

</td></tr><tr><td>

cmdb\_ci\_ups\_output

</td><td>

UPS Output

</td><td>

Electrical output from an Uninterrupted Power Supply device.

</td></tr><tr><td>

cmdb\_ci\_ups\_power\_eq

</td><td>

Uninterruptible Power Supply

</td><td>

Uninterrupted Power Supply devices, where devices are any non-traditional UPS devices that manage electrical power.

</td></tr><tr><td>

cmdb\_ci\_vcenter

</td><td>

VMware vCenter Instance

</td><td>

Installed instance of VMware VCenter software.

</td></tr><tr><td>

cmdb\_ci\_vcenter\_cluster

</td><td>

VMware vCenter Cluster

</td><td>

Set of servers that work together while running VMware VCenter software.

</td></tr><tr><td>

cmdb\_ci\_vcenter\_cluster\_drs\_rule

</td><td>

VMWare vCenter Cluster DRS Rule

</td><td>

vCenter specific table which stores Distributed Resource Scheduler \(DRS\) basic rule information. Stores the affinity rule specifying that the members of a selected virtual machine DRS group can or must run on the members of a specific host DRS group.

 Populated by the [vCenter API ClusterRuleInfo\(vim.cluster.RuleInfo\)](https://code.vmware.com/apis/196/vsphere#/doc/vim.cluster.RuleInfo.html).

</td></tr><tr><td>

cmdb\_ci\_vcenter\_datacenter

</td><td>

VMware vCenter Datacenter

</td><td>

VMware VCenter data center objects.

</td></tr><tr><td>

cmdb\_ci\_vcenter\_datastore

</td><td>

VMware vCenter Datastore

</td><td>

VMware VCenter datastore objects containing details such as capacity, freespace, filesystem, and type.

</td></tr><tr><td>

cmdb\_ci\_vcenter\_datastore\_disk

</td><td>

Datastore Disk

</td><td>

Individual VMware VCenter datastore disk.

</td></tr><tr><td>

cmdb\_ci\_vcenter\_folder

</td><td>

VMware vCenter Folder

</td><td>

VCenter folders, which can be used to group objects of the same type for easier management.

</td></tr><tr><td>

cmdb\_ci\_vcenter\_network

</td><td>

VMware vCenter Network

</td><td>

VMWare vCenter virtual network.

</td></tr><tr><td>

cmdb\_ci\_vcenter\_object

</td><td>

VMware vCenter Object

</td><td>

Base class for most VMware VCenter objects.

</td></tr><tr><td>

cmdb\_ci\_vcenter\_server\_obj

</td><td>

VMware vCenter Server Object

</td><td>

VMware hypervisor.

</td></tr><tr><td>

cmdb\_ci\_veritas\_disk

</td><td>

Veritas Disk

</td><td>

Physical disk that is controlled by Veritas Volume Manager.

</td></tr><tr><td>

cmdb\_ci\_veritas\_disk\_group

</td><td>

Veritas Disk Group

</td><td>

Collection of disks in Veritas Volume Manager.

</td></tr><tr><td>

cmdb\_ci\_veritas\_plex

</td><td>

Veritas Plex

</td><td>

Logical partition in Veritas Volume Manager.

</td></tr><tr><td>

cmdb\_ci\_veritas\_subdisk

</td><td>

Veritas Subdisk

</td><td>

Partition of a Veritas\_disk.

</td></tr><tr><td>

cmdb\_ci\_veritas\_volume

</td><td>

Veritas Volume

</td><td>

Aggregation of plexes.

</td></tr><tr><td>

cmdb\_ci\_virtualization\_server

</td><td>

Virtualization Server

</td><td>

Base table used by the ESX Server \[cmdb\_ci\_esx\_server\] table.

</td></tr><tr><td>

cmdb\_ci\_virtual\_desktop

</td><td>

Virtual Desktop

</td><td>

User's desktop environment \(such as icons, wallpaper, windows, folders, toolbars, and widgets\) is stored remotely on a server.

</td></tr><tr><td>

cmdb\_ci\_virtual\_pvt\_gateway

</td><td>

Virtual Private Gateway

</td><td>

Two VPN endpoints for automatic failover.

</td></tr><tr><td>

cmdb\_ci\_vm

</td><td>

Virtual Machine HyperVisor

</td><td>

Hypevisor software.

</td></tr><tr><td>

cmdb\_ci\_vm\_instance

</td><td>

Virtual Machine Instance

</td><td>

Generic virtual machines information.

</td></tr><tr><td>

cmdb\_ci\_vm\_object

</td><td>

Virtual Machine Object

</td><td>

Base class for all VM objects. Parent for all objects such as Hyper-V object and KVM object.

</td></tr><tr><td>

cmdb\_ci\_vm\_parallels

</td><td>

Parallels

</td><td>

Instance of Parallels software.

</td></tr><tr><td>

cmdb\_ci\_vm\_template

</td><td>

Virtual Machine Template

</td><td>

Template, which is a main copy of a virtual machine that can be used to create many clones. Base table for all VM templates.

</td></tr><tr><td>

cmdb\_ci\_vm\_user\_credentials

</td><td>

VM User Credentials

</td><td>

Credentials, which are used to authenticate access rights and permissions.

</td></tr><tr><td>

cmdb\_ci\_vm\_vmware

</td><td>

VMware

</td><td>

**Note:** No longer used.

VMWare specialization of the Virtual Machine table.

</td></tr><tr><td>

cmdb\_ci\_vm\_zones

</td><td>

Zones

</td><td>

Partitioned virtual OS environment working in a Solaris operating system space.

</td></tr><tr><td>

cmdb\_ci\_voice\_hardware

 \(Installed with the com.snc.cmdb.telecom.category plugin\)

</td><td>

Voice System Hardware

</td><td>

Telecommunication systems that represent telephone systems, telephone exchanges, and voice mail.

 Parent class for telecom voice system hardware such as voicemail and private branch exchanges.

</td></tr><tr><td>

cmdb\_ci\_volume\_template

</td><td>

Volume Template

</td><td>

Set of rules that specify one or more capabilities of a storage volume \(storage selection and layout rules\).

</td></tr><tr><td>

cmdb\_ci\_vmware\_instance

</td><td>

VMware Virtual Machine Instance

</td><td>

VMware VM instance on VMware hypervisor.

</td></tr><tr><td>

cmdb\_ci\_vmware\_template

</td><td>

VMware Virtual Machine Template

</td><td>

Main copy of a VMware virtual machine that can be used to create many clones.

</td></tr><tr><td>

cmdb\_ci\_vpc

</td><td>

Virtual Private Cloud

</td><td>

On-demand configurable pool of shared computing resources allocated within a public cloud environment.

</td></tr><tr><td>

cmdb\_ci\_vpn

</td><td>

Virtual Private Network

</td><td>

Private network configured to run across a public network.

</td></tr><tr><td>

cmdb\_ci\_vpn\_connection

</td><td>

VPN Connection

</td><td>

Secure connection to another network over the Internet.

</td></tr><tr><td>

cmdb\_ci\_vserver\_peer

</td><td>

Vserver Peer

</td><td>

Extends the Virtual Machine Object \[cmdb\_ci\_vm\_object\] table. Peer relationship between the Vservers \(NetApp\).

</td></tr><tr><td>

cmdb\_ci\_wap\_network

</td><td>

Wireless Access Point

</td><td>

Networking hardware device that allows a Wi-Fi compliant device to connect to a wired network.

</td></tr><tr><td>

cmdb\_ci\_web\_application

</td><td>

Web Application

</td><td>

Client–server software application in which the client \(or user interface\) runs in a web browser.

</td></tr><tr><td>

cmdb\_ci\_web\_domino

</td><td>

Lotus Domino HTTP Server

</td><td>

Server running IBM Notes software \(formerly Lotus Notes/IBM Domino\).

</td></tr><tr><td>

cmdb\_ci\_web\_server

</td><td>

Web Server

</td><td>

Computer system that processes requests via HTTP from the World Wide Web.

</td></tr><tr><td>

cmdb\_ci\_web\_service

</td><td>

Web Service

</td><td>

Service offered by an electronic device to another electronic device, communicating with each other via the World Wide Web.

</td></tr><tr><td>

cmdb\_ci\_web\_site

</td><td>

Web Site

</td><td>

A collection of related web pages.

</td></tr><tr><td>

cmdb\_ci\_websphere\_cell

</td><td>

Websphere Cell

</td><td>

A logical grouping of IBM Websphere nodes \(each of which runs one or more application servers\) that are centrally managed.

</td></tr><tr><td>

cmdb\_ci\_win\_cluster

</td><td>

Windows Cluster

</td><td>

A single \(virtual\) server composed of one or more physical Windows Servers.

</td></tr><tr><td>

cmdb\_ci\_win\_cluster\_node

</td><td>

Windows Cluster Node

</td><td>

A physical member of the Windows Cluster application.

</td></tr><tr><td>

cmdb\_ci\_win\_cluster\_resource

</td><td>

Windows Cluster Resource

</td><td>

A logical or physical entity managed by the Windows Cluster application.

</td></tr><tr><td>

cmdb\_ci\_win\_domain\_controller

</td><td>

Windows Domain Controller

</td><td>

A server that responds to security authentication requests within a Windows Server domain.

</td></tr><tr><td>

cmdb\_ci\_win\_server

</td><td>

Windows Server

</td><td>

A server running Microsoft Windows Server operating system.

</td></tr><tr><td>

cmdb\_ci\_windows\_service

</td><td>

Windows Service

</td><td>

A Windows computer program that operates in the background.

</td></tr><tr><td>

cmdb\_ci\_zone

</td><td>

Data Center Zone

</td><td>

A specified portion of a data center facility.

</td></tr></tbody>
</table>## Service tables

In the CMDB, child tables of the Service \[cmdb\_ci\_service\] table store information about services, including application services.

<table id="table_kp1_gj2_2r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Business criticality

</td><td>

The importance of this service to the business. This field can be used to determine disaster recovery strategies for this service. Default options are: -   1 - most critical
-   2 - somewhat critical
-   3 - less critical
-   4 - not critical

</td></tr><tr><td>

SLA

</td><td>

A reference to the Agreement \[sla\] table.

</td></tr><tr><td>

Service classification

</td><td>

Designates the type of the service. -   Application Service \(For more information, see [Application services](../concept/application-services.md)\)
-   Technical Service \(For more information, see [Application services](../concept/application-services.md) and [Use the Dynamic CI Group method to populate application services](../task/populate-app-service-dynamic-group.md)\)
-   Service Offering \(For more information, see [Service Portfolio Management service offerings](https://www.servicenow.com/docs/access?context=SPM2-service-offerings&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)\)
-   Shared Service \(For more information, see IT shared services\)
-   Billable Service \(To represents a service that is billed, or that is cost managed\)

</td></tr><tr><td>

Used for

</td><td>

Designates how this service is used. Default options are: -   Production
-   Staging
-   QA
-   Test
-   Development
-   Demonstration
-   Training
-   Disaster Recovery

</td></tr><tr><td>

Users supported

</td><td>

The users that this service supports. A reference to the Group \[sys\_users\_group\] table.

</td></tr><tr><td>

Version

</td><td>

Use this field for your own versioning processes.

</td></tr></tbody>
</table>## Service Configuration Item Association table

The Service Configuration Item Association table \[svc\_ci\_assoc\] binds an application service and a CI to track which CIs are part of each application service.

|Field|Description|
|-----|-----------|
|Configuration Item Id|A reference to the Configuration Item \[cmdb\_ci\] table.|
|Service Id|A reference to the Service \[cmdb\_ci\_service\] table.|

