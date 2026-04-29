---
title: Manage update set for Now Assist for Setup
description: Upload a batch update set to promote validated configuration changes from a non-production instance to production in a single, controlled deployment, ensuring consistency and reducing manual errors.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Administer, Now Assist for Setup, Get started, Administer the ServiceNow AI Platform]
---

# Manage update set for Now Assist for Setup

Upload a batch update set to promote validated configuration changes from a non-production instance to production in a single, controlled deployment, ensuring consistency and reducing manual errors.

## Before you begin

Before performing this task you must request for the entitlement for Now Assist for Setup and install it.

**Note:** Request for the entitlement and installation of Now Assist for Setup is the first step to experience automatic product installations and implementation of default configurations on your ServiceNow instance.

The following conditions should be met:

-   Preset and manual configurations are completed and verified in the non-production instance.
-   The batch update set is packaged in the non-production instance, and the XML file is downloaded.
-   The production instance version is compatible with the source non-production instance.

The following task is performed on a production instance only after the above conditions are met:

Upload a batch update set in Now Assist for Setup 

Role required: admin

## Procedure

1.  Navigate to your Admin Home page on your instance.

    The system dynamically renders application and plugin cards based on your admin entitlement status.

2.  Select **View product overview** for AI-native IT Service Management product family card to start the setup process.

    The Product Hub page for AI-native IT Service Management shows up.

3.  Select **Upload batch** under Option 2 - Coming from another ServiceNow instance? option.

    The Upload your batch update set as XML file modal shows up.

4.  Select +Add file in the modal to upload the batch file and select **Continue**.

    The Update set ready modal shows up with "Upload successful with no conflicts detected" message.

    **Note:** This message is visible only if the batch file doesn't have any errors.

    When the batch file contains errors, the "Your update set has conflicts that need attention" message shows up.

5.  Select **Preview** in the Update set ready modal.

    You can also select Open KB article if you want to view the KB article about uploading batch file.

    The Retrieved Update Set form shows up on a new tab.

6.  Select **Commit Update Set Batch** in the form.

    **Note:** The **Commit Update Set Batch** option is visible only when there is no error in the batch file. You are required to resolve the errors in the batch file before selecting **Commit Update Set Batch**.

    The Commit Update Set Batch modal gets displayed showing the progress of the batch file being committed.

    If the commit operation fails, an error message is shown stating the failure. Review the commit status and any error details presented and navigate back to the Product Hub page. The Product Hub page provides a See Logs link to the commit logs, with details of the specific reasons for any commit failures.

    **Note:** Resolve all commit log errors before retrying to upload the update set xml file again. Ensure the non-production and production instances are running compatible versions.

7.  Select Preview Problems for Batch related list to review the errors in the update set batch file.

    **Note:** This step is applicable only when there are errors in the update set batch file.

    The list of errors shows up under the Preview Problems for Batch related list.

8.  Select any of the available actions to resolve the errors.

    **Note:** This step is applicable only if there are any errors in the update set batch file. You are then required to resolve the errors in the batch file and then proceed with the **Commit Update Set Batch** option. The **Commit Update Set Batch** option appears once the errors are resolved in the batch file.

9.  Navigate back to the Product Hub page to see the progress.

10. Once the update set commit completes, you can either select **Upload another update set** or **Configure** depending on the requirement.

    If you want to upload another batch file, select **Upload another update set**. You can also select **Configure** if you are done uploading the update set batch file and wants to proceed with the configuration process.


## Result

These steps complete the successful uploading and committing of the update set batch file.

**Parent Topic:**[Administer Now Assist for Setup](../concept/ia-administer.md)

