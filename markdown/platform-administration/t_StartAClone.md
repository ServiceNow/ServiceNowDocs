---
title: Request a clone
description: Request a clone to copy data from a production instance to a non-production instance or to copy data between non-production instances.Request a clone to copy data from a production instance to a non-production instance or to copy data between non-production instances.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-09-12"
reading_time_minutes: 5
breadcrumb: [Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Request a clone

Request a clone to copy data from a production instance to a non-production instance or to copy data between non-production instances.

## Before you begin

Role required: `clone_admin` on the source instance; `clone_admin` and `soap` on the target instance.

## Procedure

1.  Navigate to **All** &gt; **Clone Admin Console** &gt; **Request Clone**.

2.  On the form, fill in the fields.

<table id="table_ujp_cdf_gxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source instance

</td><td>

The original database where data is copied from.

</td></tr><tr><td>

Target instance

</td><td>

The new location where the data is copied to.**Note:** You can add an instance or select an existing instance without leaving the page.

</td></tr><tr><td>

Clone Profile

</td><td>

Apply a clone profile that you created previously. All exclusions, preservers, and scripts you added to the profile are applied to the clone request.

 If clone profile is left empty the system will pull in all available preservers, exclusions and cleanup scripts

 **Note:** If **default** is checked on the clone profile, the clone request loads this profile every time you open the clone request page.

</td></tr><tr><td>

Lock settings at the time of clone request

</td><td>

If you use a clone profile, this option locks the settings and options at the time of the clone request. Any subsequent changes to the clone profile, regardless of when the clone runs, don’t affect the clone request.

</td></tr><tr><td>

Clone Scheduled Start time

</td><td>

The start time to begin cloning your instance. See [Schedule recurring clones \(legacy\)](schedule-cloning.md).

</td></tr><tr><td>

-   Email updates about this clone
-   External email address


</td><td>

The email or emails to be notified of the clone process and clone completion.

</td></tr></tbody>
</table>3.  Select the hyperlinked number under each item in the definitions section to review your exclusions, preservers, and cleanup scripts.

4.  Select the options to configure for your clone.

    **Note:** For information on all available options see [Clone options](../reference/clone-options.md). For information on general guidelines to expedite your clone request see [General guidelines for optimizing your clone duration](../reference/clone-duration-optimization.md).

5.  Select **Continue**.

6.  Review your clone request summary and select **Confirm and Submit Clone Request**.


## Request a clone \(legacy\)

Request a clone to copy data from a production instance to a non-production instance or to copy data between non-production instances.

### Before you begin

Role required: clone\_admin

Starting with the Australia release, clone requests are no longer deployed, enhanced, or supported on the legacy page. Requests that are initiated via the legacy page `clone_instance.do` don't show up on the new clone console home page. However, they can still be found on the legacy clone history page `clone_instance_list.do`.

**Note:**

Configure your target instance before requesting your clone. See [Register target instance \(legacy\)](t_CreateACloneTarget.md).

Configure a clone profile. See [Create a custom clone profile](configure-clone-profile.md).

For self-hosted customer instances that use an Oracle database, see [https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB0563847](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0563847).

### About this task

The ServiceNow AI Platform uses data from the most recent, daily backup of the source instance when cloning. Backups that are used for cloning are a maximum of 36 hours old. The initial preparation begins, including selecting the latest backup to use, only at the date and time processing is scheduled to start.

### Procedure

1.  Log in to the instance that you want to clone.

    This instance becomes the source instance of the clone request.

2.  Configure a [Register target instance \(legacy\)](t_CreateACloneTarget.md) record for each target instance that you want to receive clone data.

3.  Verify the list of tables that are excluded from cloning and [add or remove tables to exclude](t_ExcludeATableFromCloning.md) from the target instance.

4.  Verify the list of tables and system properties that you want saved on the target instance with the following.

5.  Navigate to **Instance clone** &gt; **Request Clone**.

6.  Specify a predefined clone profile.

    A clone profile stores target and clone options. The clone profile automatically populates your clone request with your selected profile settings. See [clone profiles for clone requests](../reference/system-profile-clone.md).

7.  In the **Target instance** field, select the target instance that you want to receive the cloned data.

    Create a separate clone request for each target instance that you want to receive clone data.

8.  In the **Clone Scheduled Start Time** field, select the time that you want the cloning to start.

    You can schedule multiple clone requests for the same source instance. For example, create a clone request to copy data to non-production instance A and another clone request to copy data to non-production instance B. The scheduling engine determines whether multiple clone requests against the same source instance can occur simultaneously or whether they must occur sequentially. If your source instance is large, see clone chaining on [Exploring Instance Clone](../concept/exploring-instance-clone.md#).

    The system verifies the scheduled start time and either accepts the date-time value that you selected or suggests an available date-time value. The validation process helps prevent scheduling conflicts with other automations using the same target instance.

9.  In the **Email upon completion** field, enter your email address so that you can receive alerts after the cloning finishes, is canceled, or has an error.

10. Select the **Options** arrowhead so that it turns downward.

11. Fill in your options.

12. Select **Submit**.

    If there are no issues with the clone request, the system displays the Authenticate Target modal.

13. Enter the user name and password for an administrator account on the target instance and then select **Authenticate**.

14. Review the clone settings and select **OK**.

    An email is sent to the supplied address after the clone finishes, is canceled, or has an error.


### What to do next

-   [Schedule recurring clones](schedule-cloning.md).
-   [Cancel your clone request](cancel-clone-cac.md#).
-   [View the clone history](t_ViewCloneHistory.md) of completed clones.

