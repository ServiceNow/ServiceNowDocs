---
title: Data preservation on cloning target instances
description: You can use data preservers to protect data on the target instance from being overwritten. If you have custom applications, you must also manually preserve unpublished application content.Data preservers maintain specified data on a target instance.If you want a clone target instance to keep its existing SAML integration, you must edit the Core Instance Properties data preserver to include the SAML properties.Manually preserve a copy of each application and customization that you currently have in development before you can clone the application version to the target \(development\) instance.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [Request a clone, System clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Data preservation on cloning target instances

You can use data preservers to protect data on the target instance from being overwritten. If you have custom applications, you must also manually preserve unpublished application content.

## Data preservers

Sometimes, it is necessary to preserve some data on an instance targeted for cloning. For example, if the target is a MID Server, you must not overwrite the MID Server \[ecc\_agent\] table. Preserved data is stored on the target instance before cloning begins and is restored on the target instance after cloning.

**Warning:** You must define data preservers on the source instance. Defining them on the target instance does not preserve the data.

Data preservers typically preserve system settings and themes, such as:

-   Instance-specific authentication settings
-   Bookmark \[sys\_ui\_bookmark\]
-   Recent Selection \[sys\_ui\_recent\_selection\]
-   User Preference \[sys\_user\_preference\]

**Note:** A clone does not support preserving data from a database view.

Do not use data preservers to transfer large sets of data, such as user groups. If you must preserve table data, such as users, groups, and roles, consider exporting the records to a file and importing them after cloning.

## Data preservers for Multi-SSO

The system automatically creates the necessary data preservers for cloning when you activate Multiple Provider Single Sign-On integration.

<table><thead><tr><th>

Name

</th><th>

Table

</th><th>

Conditions

</th></tr></thead><tbody><tr><td>

Certificate

</td><td>

X.509 Certificates \[sys\_certificate\]

</td><td>

None

</td></tr><tr><td>

Core Instance Properties

</td><td>

System Property \[sys\_properties\]

</td><td>

-   \[OR\] \[Name\] \[is one of\] \[glide.authenticate.external, glide.authenticate.external.logout\_redirect\]
-   \[OR\] \[Name\] \[starts with\] \[com.snc.integration.saml\_esig\]
-   \[OR\] \[Name\] \[is one of\] \[glide.smtp.port, glide.smtp.auth, glide.smtp.encryption\]
-   \[OR\] \[Name\] \[starts with\] \[glide.authenticate.multisso\]
-   \[OR\] \[Name\] \[is\] \[glide.authenticate.sso.redirect.idp\]

 **Note:** The properties **glide.smtp.port**, **glide.smtp.auth**, and **glide.smtp.encryption** are deprecated.

</td></tr><tr><td>

Digest Properties

</td><td>

Digest Properties \[digest\_properties\]

</td><td>

None

</td></tr><tr><td>

Identity Providers

</td><td>

Identity Providers \[sso\_properties\]

</td><td>

None

</td></tr><tr><td>

SAML2 Update1 Properties

</td><td>

SAML2 Update1 Properties \[saml2\_update1\_properties\]

</td><td>

None

</td></tr></tbody>
</table>**Note:** Although you can modify these data preservers, it is good practice not to. The Digest Properties \[digest\_properties\], Identity Providers \[sso\_properties\], and SAML2 Update1 Properties \[saml2\_update1\_properties\] tables are required for multiple source, single sign-on \(SSO\) to function properly. If multiple source, single sign-on is disabled on the target instance, you can safely remove all three data preservers. Remove them at the same time, as the system terminates the clone with an error message when you attempt to clone with one or two of these tables being preserved.

## Data preservers for SAML

Preserving SAML SSO-related settings can prevent the target instance from using the wrong issuer and audience parameters when making authentication requests to your IdP. To preserve SAML settings, create data preservers for the following tables:

-   System Property \[sys\_properties\]: to preserve SAML properties.
-   X.509 Certificates \[sys\_certificate\]: to preserve SAML certificates.
-   User \[sys\_user\]: to preserve SAML users.

You also need to preserve [properties](data-preservation.md#) and users that are involved in SAML.

## Preservation of unpublished applications

You cannot use data preservers to save unpublished applications. Instead, application developers must choose how they want to [preserve unpublished applications](data-preservation.md#).

The cloning process does not preserve version differences for applications in development. Instead, the system clone only copies the application version installed on the source instance onto the target instance. If the target instance had a development version of the same application, the application will be editable after the clone, but it will be at whatever version was installed on the source instance. If the application was missing from the source instance, the cloning process deletes the application from the target instance.

## Create a data preserver

Data preservers maintain specified data on a target instance.

### Before you begin

Role required: clone\_admin or admin

### About this task

Sometimes, preserving certain data on a target instance is desirable. For example, when using a MID Server, you can avoid overwriting the MID Server \[ecc\_agent\] table. Preserved data is stored in a dynamically generated list on the target instance before the clone and restored on the target instance after the clone is complete. You define data preservers on the source instance.

Data preservers are primarily intended to preserve system settings and themes, such as instance-specific authentication settings. Do not use data preservers to transfer large sets of data, such as user groups. If you must preserve table data such as users, groups, and roles, consider exporting the records to a file and importing it after the clone is complete.

Consider whether to preserve the data in the following tables.

-   Bookmark \[sys\_ui\_bookmark\]
-   Recent Selection \[sys\_ui\_recent\_selection\]
-   User Preference \[sys\_user\_preference\]

If you set a data preserver on a table where the source instance has more records than the target instance, the data preserved on the target instance also includes the additional records from the source instance.

For example, assume that the data preserver is already in place.

-   In the source instance, the sys\_temp table contains 100 records.
-   In the target instance, the sys\_temp table contains 20 records.

After the clone, the sys\_temp table in the target instance contains 100 records.

-   The 20 records in the target sys\_temp table are preserved successfully \(per the data preserver specification\). These records were part of the 100 records in the source sys\_temp table.
-   The source sys\_temp table brings over the remaining 80 records to the target sys\_temp table.

To resolve this issue and to preserve only the records in the target table, [create an exclude table record](../task/t_ExcludeATableFromCloning.md) for the target table, in addition to setting the data preserver on the source table.

**Important:** Configure preservers on the source instance.

### Procedure

1.  On the source instance, navigate to **System Clone** &gt; **Preserve Data**.

2.  Click **New**.

3.  Enter the table label as the **Name**, for example, User Preference for the \[sys\_user\_preference\] table.

    The data preserver must have a table name or it cannot be submitted.

4.  Select the **Table** to be preserved.

    The data preserver must have a table selected or it cannot be submitted.

5.  Select the **Theme** check box if the data being preserved is a UI property.

6.  Define the data to be preserved using the [Condition Builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) .

    You can use conditions to define particular records you want to preserve during a clone. For example, to only preserve particular system properties, you can add conditions for each property name you want to preserve.

    **Note:** The condition to match regular expressions \[match regex\] is no longer supported.

    ![Data preserver with conditions](../image/DataPreserver2.png)

    **Warning:** If the clone from backup fails for some reason, the clone process fails over to the legacy clone engine. The legacy clone engine cannot preserve data from extended tables, relationships, hierarchies between tables, and dot-walked queries. You may want to reschedule a system clone or manually transfer data in such cases.

7.  Click **Submit**.

    If you want to delete the data preserver later, make sure not to modify or delete the following data preserver records:

    -   Core Instance Properties
    -   Semaphores
    -   Email Accounts
    **Note:** DB views cannot be preserved.

    Preservers cannot be empty, and users will not be able to submit the clone if preservers are empty.


## Preserve SAML properties

If you want a clone target instance to keep its existing SAML integration, you must edit the **Core Instance Properties** data preserver to include the SAML properties.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Clone** &gt; **Preserve Data**.

2.  Select **Core Instance Properties**.

3.  Add the following **Conditions**.

    -   **\[OR\] \[Name\] \[is one of\] \[glide.authenticate.external, glide.authenticate.external.logout\_redirect, glide.authenticate.failed\_requirement\_redirect\]**
    -   **\[OR\] \[Name\] \[starts with\] \[glide.authenticate.sso.saml2\]**
    -   **\[OR\] \[Name\] \[starts with\] \[com.snc.integration.saml\_esig\]**
    ![SAML system property preservation](../image/DataPreserverSAML.png)

    **Note:** Ensure the **Theme** check box is cleared so these properties are preserved regardless of whether you preserve the instance theme.

4.  Click **Update**.


## Preserve applications and customizations in development during a system clone

Manually preserve a copy of each application and customization that you currently have in development before you can clone the application version to the target \(development\) instance.

### Before you begin

Ensure that you have write access to the application record.

Ensure that you have access to a source control repository.

Role required: admin

### About this task

The cloning process does not preserve version differences for applications and app customizations in development. Instead, the system clones only the copies of the application and app customization versions that are installed on the source instance onto the target instance. If the target instance had a development version of the same application, the application is editable after the clone, but is at the version that was installed on the source instance. If the application was missing from the source instance, the cloning process deletes the application from the target instance.

### Procedure

1.  To preserve the application on the clone target instance, do one of these actions:

<table id="table_icq_cv1_4y"><thead><tr><th>

Application version state

</th><th>

Action to take

</th></tr></thead><tbody><tr><td>

The application version on the clone target instance is different than the source instance version.

</td><td rowspan="2">

Export each application from the clone target instance. The choices include:-   Link each application to a source control repository.

**Note:** If the application is already linked to a source control repository, commit the latest version to it.

-   Publish each application to an update set.


</td></tr><tr><td>

The application is available only on the clone target instance.

</td></tr><tr><td>

The application version on the clone target instance is the same as the source instance.

</td><td>

None. The system clone process copies this application version onto the target instance during the clone.

</td></tr></tbody>
</table>2.  Request a system clone of the source instance to the target instance.

    For example, clone your production instance over your development instance.

3.  After the clone process finishes, log in to the clone target instance.

4.  **Note:** If source control is linked, then post clone, the platform will automatically retrieve applications and customized applications. If this is disabled via `glide.source_control.post_clone_import_enabled` you will need to manually retrieve by doing the following.

    If you saved each application to a source control repository, use one of these actions to retrieve them from the source control repository:

    **Note:** For what to expect after application customization post clone, see [Results post cloning for application customizations](https://www.servicenow.com/docs/access?context=what-to-expect-post-clone-for-app-customization&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

    |Application installation state|Action to take on clone target|
    |------------------------------|------------------------------|
    |The application and customization were previously installed on the source instance.|Apply remote changes from the source control repository.|
    |The application was never installed on the source instance.|Delete the repository configuration \(sys\_repo\_config\) and import the customization from the source control repository.|

    |Field|Description|
    |-----|-----------|
    |glide.source\_control.post\_clone\_import\_enabled|To disable the apply remote changes automation, set to **False**. The default is **True**.|
    |glide.source\_control.post\_clone\_import\_delay\_time\_sec|To provide a delay time, which will delay processing of the queue, provide a value. The default is zero.|
    |glide.source\_control.post\_clone\_import\_pause\_refresh\_time\_sec|To provide an interval in which the refresh repository job will not run, provide a value. The default is three hours \(10800\).|

5.  If you saved each application to an update set, do one of these actions to retrieve them from the update set:

<table id="table_oyk_l51_4y"><thead><tr><th>

Application installation state

</th><th>

Action to take on clone target

</th></tr></thead><tbody><tr><td>

The application was previously installed on the source instance.

</td><td>

1.  Delete the application version that was cloned from the source instance.
2.  Load the update set that contains the current application version.


</td></tr><tr><td>

The application was never installed on the source instance.

</td><td>

Load the update set that contains the current application version.

</td></tr></tbody>
</table>
### Result

The applications previously in development are available for further development on the clone target instance.

### Preserve the Marketing Events application

Let's say that your company previously created version 1.0 of a custom application called Marketing Events. You have already published version 1.0 of the Marketing Events application to the application repository and installed it on your production instance.

Over time, users have submitted enhancement requests for the application, and you decide to develop version 2.0 of the Marketing Events application on a non-production instance to address these requests. As development nears completion, you want to update your non-production instance to the latest copy of production for some comprehensive testing.

Because you previously used a source control integration to develop version 1.0 of the Marketing Events application, you have already linked the Marketing Events application to a source control repository. You commit version 2.0 of the Marketing Events application to the source control repository.

You schedule a clone of the production instance over the development instance. After completion, you log in to the development instance and see that it has version 1.0 of the Marketing Events application, because that was the version installed on the source instance.

Because the application was already installed on the source instance, you apply the remote changes from the source control repository to receive the latest application version. The development instance now has version 2.0 of the Marketing Events application and is available for further development and testing.

