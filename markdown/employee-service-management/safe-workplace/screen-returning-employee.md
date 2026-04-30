---
title: Conduct a health screen for entry
description: Use a health screen to verify a person's return requirement status to determine whether the person is able to enter the location.
locale: en-US
release: zurich
product: Safe Workplace
classification: safe-workplace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Employee Health Screening, Safe Workplace, Health and Safety, Employee Service Management]
---

# Conduct a health screen for entry

Use a health screen to verify a person's return requirement status to determine whether the person is able to enter the location.

## Before you begin

Role required: sn\_imt\_monitoring.monitoring\_user

## About this task

Conduct a health screen before people enter a location, such as employees returning to the workplace or students returning to campus. Verify the person's return requirement status on your smartphone, tablet, or computer. Then complete and submit a health screening form to determine whether the person is able to enter the location.

The following procedure includes the steps your organization might use in setting up health screening. Some of the steps might not be applicable to your location.

**Note:** If the ServiceNow® Customer Service Management \(CSM\) application is activated, the health screen can be performed for CSM consumers and contacts. The customer service agent \[sn\_customerservice\_agent\] and consumer service agent \[sn\_customerservice.consumer\_agent\] roles can optionally be given to health screeners so that they can view additional CSM information on the health screening form, but these roles are not required for screening consumers and contacts. For more information about using Customer Service Management with Employee Health Screening, see [Integrate Customer Service Management with Safe Workplace applications](https://www.servicenow.com/docs/access?context=csm-integration-safe-workplace&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

## Procedure

1.  Open the QR code scanning or requirement status page based on the type of device that you're using.

<table id="choicetable_bgv_ws5_r2c"><thead><tr><th align="left" id="d84558e92">

Platform

</th><th align="left" id="d84558e95">

Action

</th></tr></thead><tbody><tr><td id="d84558e101">

**Smartphone or tablet**

</td><td>

From the Now Mobile **Health** screen under the **Health Screening** section, tap **Scan for Entry**.Scan the code that the person presents on their mobile device or on paper. If there is no QR code, enter the user ID in the **User ID** field, for example, `john.smith`.

</td></tr><tr><td id="d84558e131">

**Computer**

</td><td>

Navigate to **Employee Health and Safety Status** &gt; **View Employee and Visitor Status** and select the person.

</td></tr></tbody>
</table>2.  Review the requirement status to verify that the person is cleared to enter.

    **Note:** Requirements are created in the Employee Readiness Core application. For more information, see [Employee Health and Safety Status](../../employee-readiness-core/concept/employee-health-safety-status.md).

    If the status is **Not cleared** and your organization's policy is to deny entry at this check point, provide the person with the next steps to take based on your organization's policy. Then, assist the next person in line.

    ![Health and safety status screen.](../../employee-readiness-core/image/erc-status-screening-links-rnd32.png "Health and Safety Status page")

3.  Perform the health screen.

<table id="choicetable_pjf_l3s_zlb"><thead><tr><th align="left" id="d84558e202">

Platform

</th><th align="left" id="d84558e205">

Action

</th></tr></thead><tbody><tr><td id="d84558e211">

**Smartphone or tablet**

</td><td>

Tap **Health Screen** on the Scan for entry page.

</td></tr><tr><td id="d84558e223">

**Computer**

</td><td>

Navigate to **Employee Health Screening** &gt; **Request Entry**.The screening form opens in a new browser tab.

</td></tr></tbody>
</table>    ![Health screening form](../image/health-screen-person-entry.png)

4.  Take the person's temperature and fill out the screening form.

<table id="table_kgq_qt5_rlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Location

</td><td>

Location of the health screening, such as the address of a workplace or campus.

</td></tr><tr><td>

Person

</td><td>

The person that you're screening.

</td></tr><tr><td>

Account

</td><td>

The account for the contact. This field appears only when the Customer Service Management application is activated and a contact is selected from the **Person** field. You must have the customer service agent role \[sn\_customerservice\_agent\] to view this field.

</td></tr><tr><td>

Suffix

</td><td>

The suffix for the consumer. This field appears only when the Customer Service Management application is activated and a consumer is selected in the **Person** field.

**Note:** You must have the consumer service agent role \[sn\_customerservice.consumer\_agent\] to view this field.

</td></tr><tr><td>

Temperature unit

</td><td>

Temperature unit assigned to this location.

</td></tr><tr><td>

Temperature

</td><td>

The numerical value of the person's temperature.

</td></tr><tr><td>

Personal protective equipment \(PPE\)

</td><td>

Whether the person is wearing PPE. Values are **Yes** or **No**.

</td></tr></tbody>
</table>5.  Tap or click **Submit**.


## Result

You receive a message that indicates whether to allow the person to enter. If the person does not pass the health screening, provide them with the next steps based on your organization's policy.

**Parent Topic:**[Employee Health Screening](../concept/employee-health-screening.md)

