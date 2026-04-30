---
title: Integrate with Governance, Risk, and Compliance to identify application risks and controls
description: Enterprise Architecture \(formerly Application Portfolio Management\) integrates with Governance, Risk, and Compliance \(GRC\) to help identify and assess risks on business applications.Create an entity with reference to the business application table and its specific application record. Use the entity to scope risk exposure and perform risk assessments on business applications.Attach the entity to a risk and create a risk record. Assess and identify risks that can adversely affect your business applications.The entities are assessed and evaluated for audit engagement. After which the entities that are scoped for audit engagement and validated are associated to an audit.Associate a control to a business application entity that might be at risk. It is mandatory that you set effective control on the business applications to mitigate risks and protect your business. As you upgrade your business applications, you can replace your outdated controls.As an application owner, you can view the risks that a business application is exposed to. Governance, Risk, and Compliance \(GRC\) audits the business application entity and the audited risks and engagements are captured as scripted related lists in the business application form.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Integrate, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Integrate with Governance, Risk, and Compliance to identify application risks and controls

Enterprise Architecture \(formerly Application Portfolio Management\) integrates with Governance, Risk, and Compliance \(GRC\) to help identify and assess risks on business applications.

## Before you begin

Role required: admin

## About this task

Using GRC application, you can analyze the risks associated with assets such as hardware, software, and business application. You can also identify and test controls associated with those risks as well as look at the audits that were conducted on those assets. This analysis helps the application owners to understand the risk of the business application effectively.

The application owner can identify significant risks and compliance issues that the business applications are exposed to, without having to engage an external auditing system and run the applications through the auditing process.

Activate the following plugins to integrate Enterprise Architecture with GRC.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Install the GRC: GRC Profile Dependencies \(com.snc.grc\_profile\_dep\) plugin.

3.  Install the GRC: Vendor Risk Management Dependencies \(com.snc.grc\_vrm\_dep\) plugin.

4.  Install GRC: Policy and Compliance Management Dependencies \(com.snc.grc\_policy\_dep\) plugin.

    This also requires installation of app-compliance from the ServiceNow app store.

    **Note:** The integration also requires certain applications that should be installed from the ServiceNow app store. See [Request apps on the Store](https://www.servicenow.com/docs/access?context=grc-and-store&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US) for instructions to download and activate them.


## What to do next

[Create an entity referencing the business application](apm-grc-integration-identify-risks.md#). Attach the entity to an audit.

**Parent Topic:**[Integrating Enterprise Architecture \(formerly Application Portfolio Management\) with other applications](../concept/apm-integration.md)

## Create an entity for audit referencing business application

Create an entity with reference to the business application table and its specific application record. Use the entity to scope risk exposure and perform risk assessments on business applications.

### Before you begin

Role required: sn\_audit.admin or sn\_audit.manager

### About this task

GRC uses the term, **entity**, instead of profile. An entity can be anything such as a database, server, or a business application that can be audited.

### Procedure

1.  Navigate to **All** &gt; **Audit** &gt; **Scoping** &gt; **All Entities**.

2.  Click **New**.

3.  On the form, fill in the fields.

    For field information, see [Entity Form](../reference/entity-form-fields.md).

4.  Click **Submit**.

    For more information, see:

    -   [Create a profile](https://www.servicenow.com/docs/access?context=create-a-profile&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US).
    -   [Establish profile types, profile classes, and profiles](https://www.servicenow.com/docs/access?context=c_Scoping&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US).

## Associate a risk to the entity

Attach the entity to a risk and create a risk record. Assess and identify risks that can adversely affect your business applications.

### Before you begin

Role required: sn\_risk.admin and sn\_risk.manager

### Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Risk Register** &gt; **All Risks**.

2.  Create a risk in the Risk form.

    See: [Create a risk manually](https://www.servicenow.com/docs/access?context=t_CreateRisk&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US).

    **Note:**

    Relate the risk to the entity in the **Entity** field.


## Add business application entity to an engagement

The entities are assessed and evaluated for audit engagement. After which the entities that are scoped for audit engagement and validated are associated to an audit.

### Before you begin

Role required: sn\_audit.manager or sn\_audit.admin

To add a business application entity to an engagement, you should have created an entity referencing the business application in the **Entity** field of the Entity form. See: [Create an entity for audit referencing business application](apm-grc-integration-identify-risks.md#).

### Procedure

1.  Navigate to **All** &gt; **Audit** &gt; **Engagements** &gt; **All Engagements**.

2.  To add the business application entity to the engagement, click **Add** button in the **Entities** related list.

    **Note:** The engagement must be in **Scope** or **Validate** state.

    See: [Add profiles to an engagement scope](https://www.servicenow.com/docs/access?context=add-profiles-to-engagement-scope&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US).

    When an application profile is attached to an engagement, an engagement record with the associated profile is created in Profile to Engagements \[sn\_audit\_m2m\_profile\_engagement\] table.


## Add a control to the business application entity

Associate a control to a business application entity that might be at risk. It is mandatory that you set effective control on the business applications to mitigate risks and protect your business. As you upgrade your business applications, you can replace your outdated controls.

### Before you begin

Role required: admin

You should have created an entity before associating a control to it. Controls are created in GRC.

### Procedure

1.  To create a control and add an entity to the control, see [Create a control](https://www.servicenow.com/docs/access?context=t_CreateAControl&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US).

    -   The entity that you select from the Controls \[sn\_compliance\_control\] table must be a business application and the entity **Class** of the record must be application.
    -   The control record can be either in the **Draft** or **Retired** state. However, controls in such states are not visible in Enterprise Architecture \(formerly Application Portfolio Management\) to be associated to a business application.

## View Governance, Risk, and Compliance risks and engagements for business application

As an application owner, you can view the risks that a business application is exposed to. Governance, Risk, and Compliance \(GRC\) audits the business application entity and the audited risks and engagements are captured as scripted related lists in the business application form.

### Before you begin

Role required: sn\_apm.apm\_user, sn\_apm.business\_stakeholder\_apm\_user

### Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Application Portfolio** &gt; **All Business Applications**.

2.  Click **GRC Risks** related item.

3.  View the name of the risk statement, its description, the category of risk \(legal, financial, operational, and so on\), inherent impact that indicates the levels of risk, and inherent likelihood that indicates the likelihood of the risk occurring.

    See: [Manage risks, risk statements, and risk frameworks](https://www.servicenow.com/docs/access?context=r_RiskRegister&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)

4.  Click **Engagements** related item.

5.  View the name of the engagement, the user to whom it is assigned, the state in which the engagement is, planned start date on which the activity should begin, its end date, the percentage of engagement completed, and the actual cost of the engagement.

    See: [Manage engagements](https://www.servicenow.com/docs/access?context=c_Engagements&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)

6.  Click **Controls** related item.

7.  View the name of the control, its owner, status of the control whether it is compliant or not, the classification of the control whether it is preventive, corrective, or detective, and the attestation frequency at which the scheduled job runs.

    See: [Manage controls](https://www.servicenow.com/docs/access?context=c_GRCControls&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)

8.  Click display/hide hierarchical lists arrow beside a risk record in the GRC Risks related list to view all the controls that you have associated to the risk of the business application.

    When you associate a control to a risk, the control with its associated risk is created in Risk to Control \[sn\_risk\_m2m\_risk\_control\] table.

    ![Controls associated to risk](../image/RisksToControls.png "Controls associated to a risk")


