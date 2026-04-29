---
title: Preserve applications and customizations in development during a system clone
description: Manually preserve a copy of each application and customization that you currently have in development before you can clone the application version to the target \(development\) instance.
locale: en-US
release: australia
product: Application Repository \(Self-Hosted\)
classification: application-repository-self-hosted
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage customizations to applications, ServiceNow application repository, Application sharing, Administer your apps, Deploying applications, Building applications]
---

# Preserve applications and customizations in development during a system clone

Manually preserve a copy of each application and customization that you currently have in development before you can clone the application version to the target \(development\) instance.

## Before you begin

Ensure that you have write access to the application record.

Ensure that you have access to a source control repository.

Role required: admin

## About this task

The cloning process does not preserve version differences for applications and app customizations in development. Instead, the system clones only the copies of the application and app customization versions that are installed on the source instance onto the target instance. If the target instance had a development version of the same application, the application is editable after the clone, but is at the version that was installed on the source instance. If the application was missing from the source instance, the cloning process deletes the application from the target instance.

## Procedure

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

    **Note:** For what to expect after application customization post clone, see [Results post cloning for application customizations](../reference/what-to-expect-post-clone-for-app-customization.md).

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
## Result

The applications previously in development are available for further development on the clone target instance.

## Preserve the Marketing Events application

Let's say that your company previously created version 1.0 of a custom application called Marketing Events. You have already published version 1.0 of the Marketing Events application to the application repository and installed it on your production instance.

Over time, users have submitted enhancement requests for the application, and you decide to develop version 2.0 of the Marketing Events application on a non-production instance to address these requests. As development nears completion, you want to update your non-production instance to the latest copy of production for some comprehensive testing.

Because you previously used a source control integration to develop version 1.0 of the Marketing Events application, you have already linked the Marketing Events application to a source control repository. You commit version 2.0 of the Marketing Events application to the source control repository.

You schedule a clone of the production instance over the development instance. After completion, you log in to the development instance and see that it has version 1.0 of the Marketing Events application, because that was the version installed on the source instance.

Because the application was already installed on the source instance, you apply the remote changes from the source control repository to receive the latest application version. The development instance now has version 2.0 of the Marketing Events application and is available for further development and testing.

