---
title: Topic form
description: Use the topic form to create topics for the new or cloned taxonomy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/topic-form.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Employee Center reference, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Topic form

Use the topic form to create topics for the new or cloned taxonomy.

<table id="table_yvq_hs3_sqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the topic.**Note:** For better topic discovery and search results, avoid special character **/** and ensure you re-index the content after topic name edits.

Ensure that the topic table changes are manually reindexed for their corresponding indexed sources, see [Create and associate topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/create-topics-for-taxonomy.md).

</td></tr><tr><td>

Taxonomy

</td><td>

Taxonomy with which you want to associate the topic. For example, Employee Center Pro or Employee Center Pro Kiosk.

</td></tr><tr><td>

Template

</td><td>

Name of the topic template.Available options are **emp\_taxonomy\_topic** \(for EC portal\) and **eck\_taxonomy\_topic** \(for kiosk\).

</td></tr><tr><td>

Parent topic

</td><td>

Parent topic with which you want to associate this topic. Leave this field blank if the topic you’re creating is the parent topic.**Note:** When you clone or move a topic, the associated guided self-service also is cloned or moved accordingly.

</td></tr><tr><td>

Application

</td><td>

This field is set to Employee Center by default.

</td></tr><tr><td>

Active

</td><td>

Option to make the topic available for use.

</td></tr><tr><td>

Apply template to child topics

</td><td>

Option to apply the parent topic template on the child topics.

</td></tr><tr><td>

Order

</td><td>

Order in which you want the topic to appear.

</td></tr><tr><td>

Description

</td><td>

Brief description of the topic.

</td></tr><tr><td>

Icon

</td><td>

Icon that you want to display for the topic. Click the **Click to add** option to browse and select an image you want to set as the topic icon. Supported file types include .jpg, .png, .bmp, .gif, .jpeg, .ico, and .svg.The recommended size for icons is:

-   Topic icon: 56 x 56px
-   Sub-topic icon: 28 x28px

Use the default icons that align with the EC theme such as Coral.

</td></tr><tr><td>

Banner Image

</td><td>

Banner that you want to display for the topic. Click **Click to add...** to browse and select an image you want to set as the topic banner. Supported file types include .jpg, .png, .bmp, .gif, .jpeg, .ico, and .svg.The recommended size for banners is:

-   Home page banner: 1440 x 400px
-   Topic page: 1258 x 300px

</td></tr><tr><td>

Topic manager

</td><td>

Names of the topic managers with access to the topic.

</td></tr><tr><td>

Topic contributor

</td><td>

Names of the topic contributors with access to the topic.

</td></tr><tr><td>

Enable user criteria check

</td><td>

When you opt in, you can select the user criteria for the topic visibility. Enable user criteria check to determine visibility of current topic and its child topics in navigation and popular topics widget. The criteria set also applies to child topics. Criteria in connected content still govern content visibility on topic pages.**Note:** When you have a lot of topics, ensure you set up user criteria for your topics.

Default: Disable

For more information, see [Enable user criteria for topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/enable-user-criteria-topics.md).

</td></tr><tr><td>

Available For

</td><td>

User group for whom the topic is visible. Ensure you specify the user criteria to make topics available for specific users and user groups.**Note:** When you do not specify any values for both **Available For** and **Not Available For**, the topics do not appear.

This field is available when the **Enable user criteria check** is selected.

</td></tr><tr><td>

Not Available For

</td><td>

User group for whom the topic isn’t visible. Ensure you specify the user criteria to make topics unavailable for specific users and user groups.**Note:** When you do not specify any values for both **Available For** and **Not Available For**, the topics do not appear.

This field is available when the **Enable user criteria check** is selected.

</td></tr></tbody>
</table>**Parent Topic:**[Employee Center reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/emp-center-reference.md)

**Related topics**  


[Activity Configuration form]()

[Activity Configuration Detail form]()

[Approvals experience reference]()

[Connected Content form]()

[Default Employee Profile Header Configuration record]()

[Employee Center widgets]()

[Employee Profile form]()

[Employee Profile Header Configuration form]()

[Employee Profile portal configuration form]()

[Employee Profile upgrade scenarios]()

[Enhanced Requests Experience forms]()

[External Link form]()

[Featured Content form]()

[Footer form]()

[Footer Menus form]()

[Guided Self-Service reference]()

[Menu Item form]()

[Overview section form]()

[Portal notification configuration form]()

[Portal notification content form]()

[Trigger conditions form]()

[Quick Link form]()

[Tab widget mapping form]()

[Taxonomy form]()

[User Criteria form]()

[User Criteria output]()

[Schedule appointment form]()

[Location Consent form]()

[Website configuration form]()

[Create and associate topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/create-topics-for-taxonomy.md)

