---
title: Information objects
description: Information objects are a part of the information portfolio management capability in the Application Portfolio Management application.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Associate risks, citations, policies, and controls with a risk identification record, Application risk assessment using Advanced Risk Assessment, Integrate, Risk Management, Governance, Risk, and Compliance]
---

# Information objects

Information objects are a part of the information portfolio management capability in the Application Portfolio Management application.

An information object is a configuration item that displays information in an organized form. The purpose of the information object is to logically describe the type of data that is exchanged between the application and the database. After information objects are created, they are mapped to business applications. For a given business application, the information objects determine if information can be created, updated, deleted, or read in that business application. This ability allows application owners to efficiently manage information. From an information security management perspective, this ability enables the risk and compliance function to define the right level of controls that must be applied.

The following figure shows an example of information objects. There are two applications: Workday and Now HR. Both applications store employee information. Employee information is an information object. The Now HR application can only read employee information, while the Workday application has more permissions. The risks and controls that apply to the applications are similar. However, Workday not only reads, but also creates, updates, and deletes the employee information. This means that the risks associated with Workday are higher, and so the controls applied to Workday are more stringent.

![Information objects.](../image/information-objects.png "Example of information objects")

**Parent Topic:**[Associate risks, citations, policies, and controls with a risk identification record](../task/associate-risks-pols-citations-risk-idenfn.md)

