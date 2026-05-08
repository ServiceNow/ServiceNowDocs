---
title: HR profile editable field configuration
description: An option in Human Resources Configuration provides a list of HR profile fields that can be enabled for edit. Understand the difference between how the personal and the employment information fields are updated in the HR profile based on this configuration.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [HR Profile, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# HR profile editable field configuration

An option in Human Resources Configuration provides a list of HR profile fields that can be enabled for edit. Understand the difference between how the personal and the employment information fields are updated in the HR profile based on this configuration.

Typically, organizations allow employees to update certain personal information, but not sensitive and employment information. HR agents or managers change this information. For example, employees can change their home address and personal email address, but the manager must update the position when the employee is promoted.

**Note:** Use the configurable allow list to add fields that users can modify themselves. This allow list is a system property and accessed by going to **All** &gt; **HR Administration** &gt; **Properties**. The list of user editable fields appears as comma separated list. The property name is **sn\_hr\_core.hr\_profile\_editable\_fields**.

For more information about adding or modifying HR profiles, see [Add or modify an HR profile](../task/t_CreateOrModifyAUserProfile.md)

The **HR profile fields that users or managers can edit without HR approval include &lt;number of fields&gt;** option in Human Resources Configuration provides the list of editable HR profile fields. The following list of fields indicates which of the configurable fields contain personal and which contain sensitive and employment information.

<table id="table_zdf_4n3_hdb"><thead><tr><th>

Personal information fields

</th><th>

Sensitive and employment information fields

</th></tr></thead><tbody><tr><td>

-   Home address
-   Home city
-   Home country
-   Home phone
-   Home state/province
-   Home zip/postal
-   Middle name
-   Personal email
-   Personal mobile phone
-   Prefix
-   Work email
-   Work mobile
-   Work phone

</td><td>

-   Date of birth
-   Department
-   Employee number
-   Employment end date
-   Employment start date
-   Employment type
-   Ethnicity
-   First name
-   Gender
-   Last name
-   Location
-   Location type
-   Manager
-   Nationality
-   Notice period
-   Place of birth
-   Position
-   Probation end date
-   Probation period
-   Time type

</td></tr></tbody>
</table>In the configuration option field list, all the personal information fields are enabled for edit by default. All employees can open their HR profile from the HRSM Portal and update these fields. If you do not want to allow employees to update one or more of these fields, disable editing by clearing the check box in the configurable list. For example, you do not want employees updating their work email address or phone number.

ACLs control the HR profile personal information fields, which can be modified for more controlled access.

You must have the **sn\_hr\_core.secure\_info\_reader** role to view the Social Security field on an HR profile. This role is contained in the **sn\_hr\_core.manager** role.

The employment information fields that you enable for edit allows a manager to update the field. However, the manager cannot open an employee HR profile. The manager must submit an employee information change request with the updated information. When the request to change the editable fields is submitted, the HR Employee Change Workflow takes the following actions.

-   Opens an HR case.
-   Updates the employee HR profile.
-   Closes the HR case.

To update any HR profile fields that are not editable, employees or their managers submit an employee information change request. An HR case is created and the HR Employee Change Workflow is started. The workflow requires that the change request is approved. When it is approved, the fields are updated and the HR case is closed.

## At a Glance panel in Agent Workspace for HR Service Delivery

The fields that appear on the **At a Glance** panel in Agent Workspace for HR Service Delivery are dependent on what fields appear in an HR profile.

**Note:** Fields with no data on the HR profile do not appear in the **At a Glance** panel.

If you want additional fields to appear on the **At a Glance** panel, see Configuring the form layout.

**Parent Topic:**[HR Profile](c_HRProfileRecords.md)

**Related topics**  


[HR Profile](c_HRProfileRecords.md)

