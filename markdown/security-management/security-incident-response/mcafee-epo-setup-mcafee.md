---
title: Set up your McAfee ePO console to integrate with Security Incident Response \(SIR\)
description: The following section lists the setup steps that you are required to complete in your McAfee ePO console prior to installing the application from the ServiceNow Store for the integration.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [McAfee ePO integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up your McAfee ePO console to integrate with Security Incident Response \(SIR\)

The following section lists the setup steps that you are required to complete in your McAfee ePO console prior to installing the application from the ServiceNow Store for the integration.

## Before you begin

Role required: McAfee ePO administrator

As a user with the McAfee ePO administrator permission, verify that you have installed the `Servicenow.zip` extension plugin in your McAfee ePO console. This extension plugin is required for the integration. For more information and to obtain the plugin, in your ServiceNow AI Platform instance, navigate to **Knowledge** &gt; **Articles** &gt; **All**. In the Search field, enter, ServiceNow Security Operations Extension for McAfee ePO.

## About this task

The ServiceNow extension plugin connects your ServiceNow AI Platform instance to your McAfee ePO console. This connection allows you to reference the security tags you that create in your McAfee ePO console for the isolate host and initiate malware scan actions to the capability profiles in your ServiceNow AI Platform instance.

The security tags in your McAfee ePO console must match the security tags in the capability records in your ServiceNow AI Platform instance.

The following steps show you how to install the extension plugin, create a security tag in your McAfee ePO console, and assign an action to the tag. For more information about the security tags in the McAfee ePO console, see the [McAfee Product Documentation](https://docs.mcafee.com/bundle?value=225) website.

**Note:** The figures in the following section are from the McAfee ePO console.

## Procedure

1.  If you have not installed the ServiceNow extension plugin on your McAfee ePO console, follow these steps to install it.

    1.  Log in to your McAfee ePO console with your McAfee user name and password.

        ![McAfee ePO console login dialog.](../image/mcafee-extension_install_1.png)

2.  If the page shown in the following figure is not displayed, in the top left of banner of the home page, click the menu icon to display it.

    ![Menu icon McAfee in McAfee ePO.](../image/mcafee-extension-install_3.png)

3.  In the Software section, click the **Extensions** link.

    ![Extensions software option highlighted in McAfee ePO.](../image/mcafee-extension_install_2.png)

4.  On the Extensions page that is displayed, click **Install Extension**.

    ![Install Extension button highlighted in McAfee ePO.](../image/mcafee_extension_install_btn.png)

5.  In the Install Extension dialog, click **Choose File**, navigate to the `Servicenow.zip` file on your system, and click **OK** to download it.

    ![Install Extension dialog in McAfee ePO.](../image/mcafee-extension_install_4.png)

    After the download is completed, the Software Extensions page is displayed with the ServiceNow Extension plugin listed.

    ![Extensions page in McAfee ePO.](../image/mcafee_extension_install_5.png)

    You have successfully installed the ServiceNow plugin Extension on your McAfee ePO console.

6.  If you have not created security tags in McAfee ePO console for the initiate malware scan and isolate host actions, follow these steps.

    1.  Navigate to the home page and click the **Tag Catalog** link.

        ![Tag Catalog highlighted in McAfee ePO.](../image/mcafee_tag_creation_1.png)

    2.  On the Tag Catalog page that is displayed, click **New Tag**.

        ![New Tag button highlighted in McAfee ePO.](../image/mcafee_tag_creation_2.png)

    3.  With the Description step selected in the progress bar that is displayed, enter a name and description for the tag.

        For this example, a tag with a name and description for the Initiate Malware Scan capability is displayed. This tag name is what is matched and referenced in your ServiceNow AI Platform instance.

        ![Description field of the Tag Catalog.](../image/mcafee_tag_creation_3.png)

    4.  To advance to the Criteria step, click **Criteria** in the progress bar.

        The messages that are displayed indicate that no actions are currently assigned to this tag, and that the tag can only be applied manually.

        ![Message displayed that ServiceNow tag is required in McAfee ePO.](../image/mcafee_tag_creation_4.png)

    5.  Click **Evaluation** in the progress bar to continue.

        ![Evaluation tab of Tag Catalog.](../image/mcafee_tag_creation_5.png)

    6.  With the Tag Catalog page of the Evaluation step displayed, leave the settings on this page in their defaults, and, in the progress bar, click **Preview**.

        ![Message displayed that ServiceNow tag is required in McAfee ePO.](../image/mcafee-tag_creation_6.png)

    7.  With the Preview page displayed, in the lower right of the page, click **Save** to save the record.

        The new tag is displayed in the Tag catalog as shown in the following figure.

        ![Tag Catalog with ServiceNow tag for initiate malware scan highlighted in McAfee ePO.](../image/mcafee_tag_creation_7.png)

7.  Create a security tag for the host isolation action by repeating the previous steps.

    After you have created both tags, you are ready to assign actions to the new tags.

8.  To add an action to your new tag, follow these steps.

    1.  Navigate to the home page and in the Policy section, click the **Client Task Assignments** link.

        ![Client Task Assignments highlighted in McAfee ePO.](../image/mcafee_tag_action_1.png)

    2.  In the System Tree page that is displayed, at the bottom of the page, expand the **Actions** menu and select **New Client Task Assignment**.

        ![Choice list expanded with New Client Task Assignment highlighted in McAfee ePO.](../image/mcafee_tag_action_2.5.png)

    3.  On the page that is displayed, navigate to **Endpoint Security Threat Prevention** &gt; **Policy Based On-Demand Scan** &gt; **On-Demand Scan - Full Scan** by selecting the path as shown in the following figure.

        ![System Tree with On-Demand Scan highlighted in McAfee ePO.](../image/mcafee_tag_action_no_tag_assigned.png)

    4.  In the Tags section, under the radio button and next to `Has any of these tags:`, click the **edit** link to edit the criteria for the tag.

        ![Edit link highlighted in System Tree for On-Demand Scan in McAfee ePO.](../image/tag_action_no_tag_assigned1.png)

    5.  In the dialog that is displayed, select the Initiate Malware Scan ServiceNow tag that you created in the preceding steps and click **OK**.

        ![ServiceNow initiate malware scan tag selected and highlighted in McAfee ePO.](../image/mcafee_tag_action_assignment_dialog.png)

        The ServiceNow Initiate Malware Scan tag you created is assigned to the On-Demand Scan action.

    6.  Click **OK**.

        In the Tags section, under the radio button and next to `Has any of these tags:`, the Initiate Malware Scan tag is displayed.

        ![Send this task to only computers which have the following criteria option selected in McAfee ePO.](../image/mcafee_tag_action_tag_selected.png)

    7.  Click **Save**.

        On the System Tree page, the task is displayed on the Assigned Client Tasks list \(tab\).

        ![On-Demand scan highlighted in System Tree in McAfee ePO.](../image/mcafee_tag_action_4.png)

    8.  If you have not assigned an action to the Isolate Host action, repeat the previous steps to assign it.

    You have successfully installed the extension plugin, created security tags, and assigned tasks to your tags. You have completed the setup for the integration in your McAfee ePO console. The next step is to configure a server in your ServiceNow AI Platform instance.


**Parent Topic:**[McAfee ePO integration](../concept/mcaffee-epo-overview-arch.md)

**Previous topic:**[Set up your ServiceNow AI Platform instance for the McAfee ePO integration](../reference/mcaffee-epo-setup-now.md)

**Next topic:**[Install the application and configure a server for the McAfee ePO integration](mcaffe-epo-install.md)

