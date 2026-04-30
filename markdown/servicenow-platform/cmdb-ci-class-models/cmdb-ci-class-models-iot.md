---
title: Internet of Things \(IoT\) extension classes
description: The CMDB CI Class Models store app adds or updates classes for the Internet of Things \(IoT\).
locale: en-US
release: yokohama
product: CMDB CI Class Models
classification: cmdb-ci-class-models
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [CMDB CI Class Models, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Internet of Things \(IoT\) extension classes

The CMDB CI Class Models store app adds or updates classes for the Internet of Things \(IoT\).

The CMDB CI Class Models app adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and, if applicable, dependent relationships. You can use the added classes just like any other CMDB class. Applications such as Discovery and Service Mapping Patterns can use the class extensions to populate CIs and discover technologies and software.

See the [full release notes for all CMDB CI Class Models](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/it-operations-management/store-rn-itom-cmdb-class-models.html?emcs_t=S2h8ZW1haWx8Ym9hcmRfc3Vic2NyaXB0aW9ufE1FMlVTSFREVDc3S0hTfDMzNDcxMjV8U1VCU0NSSVBUSU9OU3xoSw).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Internet of Things \(IoT\)

IoT is a system of interrelated computing devices, mechanical and digital machines, objects, animals or people that are provided with unique identifiers and the ability to transfer data over a network without requiring human-to-human or human-to-computer interaction. The classes added in this release, extend the Data Model to provide a foundation for the representation of IoT CI classes. This foundation underpins workflows for Enterprise Asset Management \(EAM\), Governance Risk Compliance \(GRC\), Component Supply Management \(CSM\), and Field Service Management \(FSM\) surrounding the management of IoT devices and the transport vehicles that some reside in.

![IoT extension classes integrated with the CMDB class hierarchy.](../image/cmdb_iot_diagram.png "IoT extension classes integrated with the CMDB class hierarchy")

## Classes

This section lists the classes that the CMDB CI Class Models store app adds or updates. For the list of classes in the base system, including classes that this app might extend, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

CMDB CI Class Models: Release 1.6.0 adds the following classes for IoT.

<table id="table_x53_n4v_phb"><thead><tr><th>

Class

</th><th>

Extends

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Transport Type\[cmdb\_ci\_transport\]

</td><td>

cmdb\_ci

</td><td>

Types of transportation that contain interconnected technology.

</td></tr><tr><td>

Converged Infrastructure\[cmdb\_ci\_converged\_infra\]

</td><td>

cmdb\_ci\_hardware

</td><td>

Devices that serve both computing and networking functions.

</td></tr><tr><td>

IoT Device\[cmdb\_ci\_IoT\]

</td><td>

cmdb\_ci\_hardware

</td><td>

Parent table that contains Internet of Things device types.

</td></tr><tr><td>

Aircraft\[cmdb\_ci\_aircraft\]

</td><td>

Transport Type\[cmdb\_ci\_transport\]

</td><td>

A transportation method that utilizes air or space as its primary pathway. For example, airplanes and helicopters.

</td></tr><tr><td>

Ship\[cmdb\_ci\_ship\]

</td><td>

Transport Type\[cmdb\_ci\_transport\]

</td><td>

A transportation method that utilizes water as its primary pathway. For example, ships.

</td></tr><tr><td>

Train\[cmdb\_ci\_train\]

</td><td>

Transport Type\[cmdb\_ci\_transport\]

</td><td>

A transportation method that utilizes rails as its primary pathway. For example, Amtrak.

</td></tr><tr><td>

Vehicle\[cmdb\_ci\_vehicle\]

</td><td>

Transport Type\[cmdb\_ci\_transport\]

</td><td>

A transportation method that utilizes wheels or tracks as its method of movement. For example, cars, trucks, bulldozers.

</td></tr><tr><td>

IoT Gateway\[cmdb\_ci\_IoT\_gateway\]

</td><td>

Converged Infrastructure\[cmdb\_ci\_converged\_infra\]

</td><td>

A device that provides the following services:-   Forwards packets between LAN and WAN on the IP layer.
-   Performs application layer functions between IoT nodes and other entities.
-   Enables local, short-range communication between IoT devices.

</td></tr><tr><td>

Security Device\[cmdb\_ci\_security\]

</td><td>

IoT Device\[cmdb\_ci\_IoT\]

</td><td>

Connected device that serves a security function such as badge readers.

</td></tr><tr><td>

Single Board Computing\[cmdb\_ci\_sbc\]

</td><td>

IoT Device\[cmdb\_ci\_IoT\]

</td><td>

Single Board Computing device such as a Raspberry Pi.

</td></tr><tr><td>

Display Device\[cmdb\_ci\_display\]

</td><td>

IoT Device\[cmdb\_ci\_IoT\]

</td><td>

Connected device that displays images.

</td></tr><tr><td>

Imaging Device\[cmdb\_ci\_imaging\]

</td><td>

IoT Device\[cmdb\_ci\_IoT\]

</td><td>

Connected device that captures images.

</td></tr><tr><td>

Medical Device\[cmdb\_ci\_medical\]

</td><td>

IoT Device\[cmdb\_ci\_IoT\]

</td><td>

Connected device that serves a Medical Care function such as a nurse call unit.

</td></tr><tr><td>

Manufacturing Device\[cmdb\_ci\_manufacturing\]

</td><td>

IoT Device\[cmdb\_ci\_IoT\]

</td><td>

Connected device that helps a manufacturing process.

</td></tr><tr><td>

Multimedia Device\[cmdb\_ci\_multimedia\]

</td><td>

IoT Device\[cmdb\_ci\_IoT\]

</td><td>

A connected device that helps the generation or delivery of media content.

</td></tr><tr><td>

Payment Device\[cmdb\_ci\_payment\]

</td><td>

IoT Device\[cmdb\_ci\_IoT\]

</td><td>

Connected device that allows for purchasing goods or services.

</td></tr><tr><td>

Drone\[cmdb\_ci\_drone\]

</td><td>

IoT Device\[cmdb\_ci\_IoT\]

</td><td>

Unmanned connected device with mobility.

</td></tr><tr><td>

Wearable Technology\[cmdb\_ci\_wearable\]

</td><td>

IoT Device\[cmdb\_ci\_IoT\]

</td><td>

Connected device that is worn by an entity such as a smart watch.

</td></tr><tr><td>

Smart Television \[cmdb\_ci\_stv\]

</td><td>

Display Device\[cmdb\_ci\_display\]

</td><td>

A television that is network connected and can run applications.

</td></tr><tr><td>

IP Camera \[cmdb\_ci\_ip\_camera\]

</td><td>

Imaging Device\[cmdb\_ci\_imaging\]

</td><td>

A camera that is network connected.

</td></tr><tr><td>

Patient Monitoring\[cmdb\_ci\_med\_patient\_monitoring\]

</td><td>

Medical Device\[cmdb\_ci\_medical\]

</td><td>

Monitors and tracks various physiological parameters of a patient. Monitors heart rate, blood pressure, oxygen levels, respiratory rate, and so on.

</td></tr><tr><td>

Surgical Instrument \[cmdb\_ci\_med\_surgical\_instrument\]

</td><td>

Medical Device\[cmdb\_ci\_medical\]

</td><td>

Devices used during surgical interventions. Life support tools and tools to assist surgeons in precise and controlled maneuvers.

</td></tr><tr><td>

Lab Equipment\[cmd\_ci\_med\_lab\_equipment\]

</td><td>

Medical Device\[cmdb\_ci\_medical\]

</td><td>

Specialized tools, apparatus, and instruments used in scientific research, experiments, and analyses.

</td></tr><tr><td>

Patient Implant\[cmdb\_ci\_med\_patient\_implant\]

</td><td>

Medical Device\[cmdb\_ci\_medical\]

</td><td>

Medical devices or tissues that are surgically placed inside a patient's body.

</td></tr><tr><td>

Clinical Device\[cmdb\_ci\_med\_clinical\_device\]

</td><td>

Medical Device\[cmdb\_ci\_medical\]

</td><td>

Devices used in a clinical setting for overall management, medical staff, and patient aid.

</td></tr><tr><td>

Diagnostic Imaging\[cmd\_ci\_med\_diagnostic\_imaging\]

</td><td>

Medical Device\[cmdb\_ci\_medical\]

</td><td>

Specialized equipment used in medicine to visualize the internal structures of the body.

</td></tr><tr><td>

Therapeutic Device\[cmdb\_ci\_med\_therapeutic\_device\]

</td><td>

Medical Device\[cmdb\_ci\_medical\]

</td><td>

Specialized tools designed to aid in the treatment, rehabilitation, or management of health conditions. Can range from orthopedic supports to cardiac implants and neurostimulation devices.

</td></tr><tr><td>

Process Logic Controller \[cmdb\_ci\_plc\]

</td><td>

Manufacturing Device\[cmdb\_ci\_manufacturing\]

</td><td>

A logic controller that is network connected which is used in manufacturing. For example, devices made by Siemens and Allen Bradley.

</td></tr><tr><td>

Human Machine Interface\[cmdb\_ci\_hmi\]

</td><td>

Manufacturing Device\[cmdb\_ci\_manufacturing\]

</td><td>

An HMI that is network connected which is used in manufacturing. For example, devices made by Siemens and Allen Bradley.

</td></tr><tr><td>

Game Console \[cmdb\_ci\_game\_console\]

</td><td>

Multimedia Device\[cmdb\_ci\_multimedia\]

</td><td>

A device that is network connected which is used to play games or stream media. For example, an Xbox or Playstation.

</td></tr><tr><td>

Media Player \[cmdb\_ci\_media\_player\]

</td><td>

Multimedia Device\[cmdb\_ci\_multimedia\]

</td><td>

A device that is network connected which is used to play digital media content. For example, Amazon Fire TV.

</td></tr><tr><td>

Display Monitor Control \[cmdb\_ci\_monitor\_control\]

</td><td>

Multimedia Device\[cmdb\_ci\_multimedia\]

</td><td>

A device that is network connected that controls the display of media on a monitor. For example, a Crestron Media Controller.

</td></tr><tr><td>

Point of Sale Device \[cmdb\_ci\_pos\]

</td><td>

Payment Device\[cmdb\_ci\_payment\]

</td><td>

A device that is network connected which is used in the purchase of goods or services. For example, a credit card reader.

</td></tr></tbody>
</table>**Related topics**  


[CMDB schema model](c_ConfigurationManagementDatabase.md)

