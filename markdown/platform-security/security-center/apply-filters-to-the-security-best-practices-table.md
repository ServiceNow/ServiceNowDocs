---
title: Filter the security best practices table
description: Apply filters to return more relevant results for your security best practices.Save the filters that you build on the security best practices table so that you can reapply them the next time you log in to your instance.Reapply a filter that you saved to the security best practices table so that you don't have to rebuild its conditions after you log out.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/security-center/apply-filters-to-the-security-best-practices-table.html
release: brazil
product: Security Center
classification: security-center
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Security Best Practices, Security posture console, Security Center, Platform Security]
---

# Filter the security best practices table

Apply filters to return more relevant results for your security best practices.

## Before you begin

Role required: admin

## Procedure

1.  Access Security Best Practices Manager by selecting **All** on your ServiceNow instance and entering `best practice`.

2.  Navigate to the Best Practices table and select the kebab menu of the field to filter, or the one with three vertical dots \[Omitted image "ellipsis-vertical-fill-24.svg"\] Alt text:.

<table id="choicetable_k12_2fy_cbc"><thead><tr><th align="left" id="d180073e75">

Fields

</th><th align="left" id="d180073e78">

Filter

</th></tr></thead><tbody><tr><td id="d180073e84">

**Name**

</td><td>

Combine a conditional operator with a string of text to return security best practices that match the name you entered.

</td></tr><tr><td id="d180073e93">

**Maturity level**

</td><td>

Apply a filter to return security best practices that match one or more of the following maturity levels:

 -   Build a foundation
-   Enhance the experience
-   Optimize the functionality
-   Add advanced features


</td></tr><tr><td id="d180073e120">

**Status**

</td><td>

Apply a filter to return security best practices that match one or more of the following statuses:

 -   Empty
-   Open
-   In progress
-   Completed


</td></tr><tr><td id="d180073e147">

**Priority**

</td><td>

Apply a filter to return security best practices that match the following priorities:

 -   Empty
-   Immediate
-   Later
-   Not applicable


</td></tr><tr><td id="d180073e175">

**Goals**

</td><td>

Apply a filter to return security best practices that match one or more of the following goals:

 -   Address initial security configurations
-   Keep instances up to date
-   Manage access controls
-   Monitoring logs
-   Protect with encryption
-   Secure emails
 **Note**: Advanced filters are applied for goals by default. To modify them, select **Make changes** &gt; **Advanced view** &gt; **Select field goals** and then build the rest of the conditions and select **Update**.

</td></tr><tr><td id="d180073e229">

**First introduced**

</td><td>

Combine a conditional operator with a string of text to return best practices that were first introduced with the version you entered.

</td></tr><tr><td id="d180073e238">

**Changed**

</td><td>

Combine a conditional operator with a string of text to return security best practices that changed in the version you entered.

</td></tr><tr><td id="d180073e247">

**Removed**

</td><td>

Combine a conditional operator with a string of text to return security best practices that were removed in the version you entered.

</td></tr></tbody>
</table>
**Parent Topic:**[Security Best Practices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/security-center/security-best-practices-manager.md)

## Save a filter for future use

Save the filters that you build on the security best practices table so that you can reapply them the next time you log in to your instance.

### Before you begin

Role required: none

### About this task

After you create filters in the security best practices table, you can save them for use the next time you authenticate into your instance. For more flexibility in the types of filters you can create, apply an advanced filter.

### Procedure

1.  Select the Show filter panel icon \[Omitted image "filter-outline-24.svg"\] Alt text:.

2.  In the Filter dialog panel, scroll down and select **Advanced view**.

3.  Build a filter by adding conditions that contain a field, operator, and values.

4.  Select **Save filter**

5.  Enter a name in the **Filter name** field.

6.  Select a permission.

7.  Select **Save**.

8.  Select **Update** to apply the saved filter to the security best practices table.


## Use a saved filter

Reapply a filter that you saved to the security best practices table so that you don't have to rebuild its conditions after you log out.

### Before you begin

Role required: none

### About this task

After you log out of your instance your filters are reset to the default settings. The following steps show how to retrieve a saved filter so that you can reapply it on the security best practices table.

### Procedure

1.  Select the Show filter panel icon \[Omitted image "filter-outline-24.svg"\] Alt text:.

2.  In the Filter dialog box, scroll down and select **Advanced view**.

3.  Select **Use existing filter**, and then select a saved filter from the drop-down list.

4.  Select **Update** to apply the saved filter.


