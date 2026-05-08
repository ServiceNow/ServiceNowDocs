---
title: Event Management tag based alert clustering tag form
description: The form for creating or modifying a tag based alert clustering tag displays detailed information about the tag.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Event Management reference, Event Management, ITOM AIOps, IT Operations Management]
---

# Event Management tag based alert clustering tag form

The form for creating or modifying a tag based alert clustering tag displays detailed information about the tag.

<table id="table_r1k_rvh_3rb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the clustering tag. Defaults to a description of the configured tag \(such as, **Exact match on Alert Field "metric name"**\).The default name is visible only after saving the tag.

 Tag names must be unique.

</td></tr><tr><td>

Customized name

</td><td>

Select the check box to customize the value in the **Name** field.

</td></tr><tr><td>

Domain

</td><td>

The domain in which the current record was created. Read-only.

</td></tr><tr><td>

Description

</td><td>

Enter an optional description of the tag.

</td></tr><tr><td>

Source

</td><td>

Select the source from which to choose the field to be matched.-   **Alert field**
-   **Alert additional info**
-   **Alert CI**
-   **Alert CI key**
-   **Alert tags**

 If you select **Alert additional info**, choose an **Additional Info Key** instead of a field. **Alert additional info** is a field on alert containing the key value pair in Jason format and we can use a specific key.

**Alert CI key**: Create CMDB key values to cluster alerts based on CMDB Key Values \[cmdb\_key\_value\] table. Key values provide an additional method for determining commonalities between alert CIs.

</td></tr><tr><td>

Selected field

</td><td>

Indicate the field that has to match between alerts for the alerts to be included in a group.Appears when you select **Alert Field** or **Alert CI** in the **Source** field.

If you select **Alert CI** in the **Source** field, you need to select a CMDB key. A CMDB key is assigned to the CI of the alert.

</td></tr><tr><td>

Key

</td><td>

Indicate the Key that has to match between alerts for the alerts to be included in a group.Appears when you select **Alert additional info** in the **Source** field, or appears when you select **Alert tags** in the **Source** field.

 When **Alert additional info** is selected, enter the name of one of the fields in the additional info field.

 When **Alert tags** is selected, enter the name of the relevant alert tag.

</td></tr><tr><td>

CMDB key

</td><td>

Indicate the CMDB key to match for the alerts to be included in a group.Appears when you select **Alert CI Key** in the **Source** field.

</td></tr><tr><td>

Match method

</td><td>

Select the type of match required for the alerts to be included in a group.-   **Exact**: Indicates that the field value must be an exact match for the alert to be included in a group.

For example, you can configure an alert clustering tag indicating that the alert's **Metric name** field must be an exact match to form a group. When invoking that tag, all alerts with identical values in the **Metric name** field are included in the same group.

-   **Fuzzy**: Indicates that the field value needs to be an approximate match \(depending on the value configured in the **Similarity** field\) for the alert to be included in a group.
-   **Pattern**: Indicates that the field value needs to follow the pattern in the **Pattern** field. For correct syntax and usage examples, see Pattern matching.

</td></tr><tr><td>

Similarity

</td><td>

Specify the similarity percentage that must be met by the alerts to be included in a group. For example, entering 50 indicates that at least 50 percent of the indicated value must appear in the alert for the alert to be included in the group. Appears only when **Fuzzy** is selected as the **Match Method** value.

 Default value = 90

</td></tr></tbody>
</table>**Parent Topic:**[Event Management reference](event-management-reference.md)

