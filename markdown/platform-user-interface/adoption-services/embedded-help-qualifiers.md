---
title: Use qualifiers in Embedded Help
description: The embedded help administrator can use qualifiers to customize content for a common page in the instance.
locale: en-US
release: xanadu
product: Adoption Services
classification: adoption-services
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Embedded Help planning, Configuring Embedded Help, Embedded Help, In-product help, Adoption services, Configure user experiences]
---

# Use qualifiers in Embedded Help

The embedded help administrator can use qualifiers to customize content for a common page in the instance.

## Before you begin

Role required: embedded\_help\_admin

## About this task

The `home.do` page is opened for every Homepage module and for many Dashboard modules. The specified query parameters in the URL define which homepage to open.

Imagine that your organization wants to provide specific instructions for the SLA homepage. You can write custom embedded help content and use a qualifier to accomplish that goal. Create the qualifier, and then associate it with custom embedded help content that you write.

## Procedure

1.  To get the information for the qualifier, open the module in a new browser window and copy the query parameter.

    Notice that the query parameter uses underscores between words instead of hyphens or dashes.

    ![Shows a query parameter in URL and the module link type](../image/query-parameter.png)

    You can also select the query parameter from the **Arguments** field on the module link type. To see the module link type, click the pencil icon beside the module in the application navigator, and then click the **Link Type** tab.

2.  Navigate to **Embedded Help** &gt; **Help Qualifiers**, and then click **New**.

3.  Complete the form.

<table id="table_vqb_b52_p1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Path

</td><td>

Enter the page to display the embedded help content. Do not include `.do`. For example, for the SLA homepage, enter `home`.

</td></tr><tr><td>

Query params

</td><td>

Enter the query parameters or the link argument using the format `id=query_parameters`.

 **Warning:** If the query parameter contains more than one word, use underscores between words instead of hyphens or dashes. If you use hyphens or dashes, the system uses only the first word in the parameter and ignores the rest.

</td></tr><tr><td>

Fragment

</td><td>

Enter the `#<string>` at the end of the URL.This is rarely found in the URL of a page in the instance. If you want custom help for a page that ends with `#<string>`, place it into this field.

**Note:** The proven practice is to include at least a query parameter. If you do not, the custom help appears for every `home.do` page. You can use either the query parameter, the fragment, or both.

</td></tr><tr><td>

Qualifier

</td><td>

Enter the qualifier to use, for example `sla_homepage`. Record the qualifier to use in the embedded help content record.

 **Warning:** If the query parameter contains more than one word, use underscores between words instead of hyphens or dashes. If you use hyphens or dashes, the system uses only the first word in the parameter and ignores the rest.

</td></tr></tbody>
</table>4.  Click **Submit**.

5.  Follow the steps in [Add custom Embedded Help content](add-custom-help-topic.md) to create the content, and include the following information.

    -   **Name** and **Page**: The page you created the qualifier for, for example, **home**.
    -   **Qualifier**: The qualifier you entered, for example **sla\_homepage**.
    **Note:** You can also copy an existing embedded help topic and enter the qualifier in the copied record.

6.  Test the qualifier by opening the page you added the content for, and then opening the help panel.

    **Note:** If you added a role to the embedded help content, ensure that you are logged in as a user with the role, or impersonate a user with that role.


**Parent Topic:**[Embedded Help planning](../concept/embedded-help-planning.md)

