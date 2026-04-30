---
title: Configure the HR case form for an HR service
description: Configure the fields that appear on the HR case form for an HR service.Examples on how to configure the HR case form for an HR service.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Configure an HR service, HR service configuration, HR services, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Configure the HR case form for an HR service

Configure the fields that appear on the HR case form for an HR service.

## Before you begin

Role required: sn\_hr\_core.admin

## About this task

This is the form that displays after an HR case is created. Configuration of the HR case form is a two-part process. First, you add or remove the additional fields on the HR service form. Second, you configure the HR case form for the HR Center of Excellence \(COE\) that the HR service is categorized under.

## Procedure

1.  Add or remove the fields in the **HR Service Additional Information** related list.

    1.  Navigate to **HR Administration** &gt; **HR Services** &gt; **HR Service Configuration**.

    2.  Open the HR service.

    3.  In the **HR Service Additional Information** related list, fill in the fields as appropriate.

<table id="table_zv3_rxh_nfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service table fields

</td><td>

Click the lock icon to view the list of available fields from the HR Center of Excellence \(COE\) that the HR service is categorized under. Select the fields you want to appear on the HR case form for the HR service. For example, the 401\(k\) retirement plan enrollment inquiry HR service includes the **Benefit plan** field.**Note:** If you added a custom column to an HR COE table, you must create a UI policy action \(**Visible** field is set to **False**\) to hide it from other HR services that use that HR COE table. For example, if you add a custom column to the HR Payroll Case \[sn\_hr\_core\_case\_payroll\] table, it appears in all HR services related to this table. The custom column appears even after you add it for a specific HR service. For more information, see [UI policies](https://www.servicenow.com/docs/access?context=t_CreateAUIPolicy&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Subject person related lists

</td><td>

Click the lock icon to search for a subject person related list you want to appear on the HR case form for the HR service. For example, the 401\(k\) retirement plan enrollment inquiry HR service includes the **Retirement Benefits for Subject Person** related list.

</td></tr></tbody>
</table>    4.  Click **Update**.

2.  Configure the HR case form for the HR Center of Excellence \(COE\) that the HR service is categorized under.

    1.  Navigate to **HR Case Management** &gt; **All HR Cases**, and open an HR case that is part of the same COE as the HR service.

    2.  In the HR case form header, click the menu icon and navigate to **Configure** &gt; **Form Layout**.

    3.  Move the fields that you added to the HR service form to the **Selected** column.

    4.  Click **Save**.


**Parent Topic:**[Configure an HR service](configure-hr-service.md)

## HR case form configuration examples

Examples on how to configure the HR case form for an HR service.

### Additional fields for 401\(k\) HR case forms

You are part of an enterprise HR organization using the HR Service Delivery application. You have several HR services related to 401\(k\) retirement benefits, and you want to add several additional fields to the HR case form, specifically the benefit plan and the list of retirement benefits for the subject person. This way, HR agents can have access to that information when working on that case type. Configuration of the HR case form for an HR service is a two-part process:

First, you need to add the fields and/or related lists you want to appear on the HR case form for that HR service in the **HR Service Additional Information** related list.

![In the HR Service Additional Information related list, provide the additional fields you want to add to the HR case form.](../image/hr-service-additional-information-field.png)

Second, you need to configure the HR case form for the COE that the HR service is categorized under. For the 401\(k\) retirement plan enrollment inquiry HR service, that COE is HR Total Rewards. Open any HR case for the HR Total Rewards COE. In the HR case form header, click the hamburger icon and navigate to **Configure** &gt; **Form Layout**. Make sure the additional fields are included under the Selected column.

![Configure any HR case form for the COE that the HR service is categorized under.](../image/configure-hr-case-form-for-coe.png)

Once the configuration is complete, HR agents that are working on a 401\(k\) case will see the additional fields you added to the HR case form. This enables the HR agent to use the additional information as they work on the HR case.

![And here is how the HR case form fields appear.](../image/hr-case-form-part-1.png)

![And here is how the HR case form related list appears.](../image/hr-case-form-part-2.png)

### Requesting an e-signature for an HR document template

You are configuring an HR service to request electronic signatures for HR document templates using [HR e-signature](../concept/hr-e-signature.md). Unlike managed documents or knowledge articles, the HR document template that the signatory will sign is selected on the HR case form. Therefore, you need to add the **PDF Template** field to the HR case form for your HR service. This way, HR agents can select the HR document template that they want the employee to sign when creating that case type.

First, on the HR service form, under the **HR Service Additional Information** related list, add the **PDF Template** field.

![Add the PDF Template field to the HR service.](../image/hr-case-form-config-e-signature-1.png)

Second, create an HR case or open an existing case that is part of the COE that your HR service is categorized under. On the HR case form header, click the menu icon and navigate to **Configure** &gt; **Form Layout**. Make sure that the **PDF Template** field is included under the Selected column.

![On the HR case form, add the PDF Template field.](../image/hr-case-form-config-e-signature-2.png)

Now, when an HR agent requests an electronic signature for an HR document template, the **PDF Template** field will appear on the HR case form for that HR service. This enables the HR agent to select an HR document template, preview it, and generate it so that the employee can then electronically sign the document.

![HR agents can then select an HR document template for the signatory to sign on the HR case form.](../image/hr-case-form-config-e-signature-3.png)

