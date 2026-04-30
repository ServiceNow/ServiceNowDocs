---
title: Defining a control's requirements at the level of control objective
description: You can break down a control at a more granular level as requirements when you generate the control at the control objective level.
locale: en-US
release: yokohama
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Implementing controls and assessment objectives in CAM, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Defining a control's requirements at the level of control objective

You can break down a control at a more granular level as requirements when you generate the control at the control objective level.

Defining control requirements helps:

-   Security Control Assessor \(SCA\): To assess each requirement of the control individually if there are different aspects to the control testing.
-   Authorization official \(AO\), Information System Security Officer \(ISSO\) and Information System Security Manager \(ISSM\): To understand the requirement that failed, which lead to the non-compliance of the control, instead of evaluating the failure of the control as a whole.
-   Attestation respondent identified for a control: To respond at the control requirements level, which is at a more granular level, rather than the control level.

As a CAM user you can break down the controls to control requirements, manage the requirements more efficiently, attest them individually, and have the package authorized. You can also define the requirements and create them at the control objective level when controls are generated.

For details, see [Control requirement details in the CAM view of Control objective and Control forms](../reference/cam-cr-control-form.md).

## Creating NIST content from control objective description as control requirements

The base system ships the control requirements generated from the NIST 800-53 revision 5 control objectives to CAM users. The **Description** field of the Control objective form lists the requirements broken down as sub-points with sub-numbers. The Reference of the control objective is clubbed with each sub-number or the clause in the **Description** field and referenced as a **Requirement number** in the Control objective requirement. For example, if the Control objective reference is IR-9, and the description of the control objective starts with a sub-number \(a.\), then the two are clubbed together to generate the first control objective requirement as IR-9.a, with further sub-numbers added to it if available. Therefore, if there are about seven sub-descriptions, then seven control requirements are generated.

![Control requirement number.](../image/cam-nist-number.png)

