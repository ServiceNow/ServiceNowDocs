---
title: Set up your McAfee ePO console to integrate with Security Incident Response \(SIR\)
description: The following section lists the setup steps that you're required to complete in your McAfee ePO console before installing the application from the ServiceNow Store for the integration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-incident-response/mcafee-epo-setup-mcafee.html
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [McAfee ePO integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up your McAfee ePO console to integrate with Security Incident Response \(SIR\)

The following section lists the setup steps that you're required to complete in your McAfee ePO console before installing the application from the ServiceNow Store for the integration.

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

        \[Omitted image "mcafee-extension\_install\_1.png"\] Alt text: McAfee ePO console login dialog.

2.  If the page shown in the following figure is not displayed, in the top left of banner of the home page, select the menu icon to display it.

    \[Omitted image "mcafee-extension-install\_3.png"\] Alt text: Menu icon McAfee in McAfee ePO.

3.  In the Software section, select the **Extensions** link.

    \[Omitted image "mcafee-extension\_install\_2.png"\] Alt text: Extensions software option highlighted in McAfee ePO.

4.  On the Extensions page that is displayed, select **Install Extension**.

    \[Omitted image "mcafee\_extension\_install\_btn.png"\] Alt text: Install Extension button highlighted in McAfee ePO.

5.  In the Install Extension dialog, select **Choose File**, navigate to the `Servicenow.zip` file on your system, and select **OK** to download it.

    \[Omitted image "mcafee-extension\_install\_4.png"\] Alt text: Install Extension dialog in McAfee ePO.

    After the download is completed, the Software Extensions page is displayed with the ServiceNow Extension plugin listed.

    \[Omitted image "mcafee\_extension\_install\_5.png"\] Alt text: Extensions page in McAfee ePO.

    You have successfully installed the ServiceNow plugin Extension on your McAfee ePO console.

6.  If you have not created security tags in McAfee ePO console for the initiate malware scan and isolate host actions, follow these steps.

    1.  Navigate to the home page and select the **Tag Catalog** link.

        \[Omitted image "mcafee\_tag\_creation\_1.png"\] Alt text: Tag Catalog highlighted in McAfee ePO.

    2.  On the Tag Catalog page that is displayed, select **New Tag**.

        \[Omitted image "mcafee\_tag\_creation\_2.png"\] Alt text: New Tag button highlighted in McAfee ePO.

    3.  With the Description step selected in the progress bar that is displayed, enter a name and description for the tag.

        For this example, a tag with a name and description for the Initiate Malware Scan capability is displayed. This tag name is what is matched and referenced in your ServiceNow AI Platform instance.

        \[Omitted image "mcafee\_tag\_creation\_3.png"\] Alt text: Description field of the Tag Catalog.

    4.  To advance to the Criteria step, select **Criteria** in the progress bar.

        The messages that are displayed indicate that no actions are currently assigned to this tag, and that the tag can only be applied manually.

        \[Omitted image "mcafee\_tag\_creation\_4.png"\] Alt text: Message displayed that ServiceNow tag is required in McAfee ePO.

    5.  Select **Evaluation** in the progress bar to continue.

        \[Omitted image "mcafee\_tag\_creation\_5.png"\] Alt text: Evaluation tab of Tag Catalog.

    6.  With the Tag Catalog page of the Evaluation step displayed, leave the settings on this page in their defaults, and, in the progress bar, select **Preview**.

        \[Omitted image "mcafee-tag\_creation\_6.png"\] Alt text: Message displayed that ServiceNow tag is required in McAfee ePO.

    7.  With the Preview page displayed, in the lower right of the page, select **Save** to save the record.

        The new tag is displayed in the Tag catalog as shown in the following figure.

        \[Omitted image "mcafee\_tag\_creation\_7.png"\] Alt text: Tag Catalog with ServiceNow tag for initiate malware scan highlighted in McAfee ePO.

7.  Create a security tag for the host isolation action by repeating the previous steps.

    After you have created both tags, you are ready to assign actions to the new tags.

8.  To add an action to your new tag, follow these steps.

    1.  Navigate to the home page and in the Policy section, select the **Client Task Assignments** link.

        \[Omitted image "mcafee\_tag\_action\_1.png"\] Alt text: Client Task Assignments highlighted in McAfee ePO.

    2.  In the System Tree page that is displayed, at the bottom of the page, expand the **Actions** menu and select **New Client Task Assignment**.

        \[Omitted image "mcafee\_tag\_action\_2.5.png"\] Alt text: Choice list expanded with New Client Task Assignment highlighted in McAfee ePO.

    3.  On the page that is displayed, navigate to **Endpoint Security Threat Prevention** &gt; **Policy Based On-Demand Scan** &gt; **On-Demand Scan - Full Scan** by selecting the path as shown in the following figure.

        \[Omitted image "mcafee\_tag\_action\_no\_tag\_assigned.png"\] Alt text: System Tree with On-Demand Scan highlighted in McAfee ePO.

    4.  In the Tags section, under the radio button and next to `Has any of these tags:`, select the **edit** link to edit the criteria for the tag.

        \[Omitted image "tag\_action\_no\_tag\_assigned1.png"\] Alt text: Edit link highlighted in System Tree for On-Demand Scan in McAfee ePO.

    5.  In the dialog that is displayed, select the Initiate Malware Scan ServiceNow tag that you created in the preceding steps and select **OK**.

        \[Omitted image "mcafee\_tag\_action\_assignment\_dialog.png"\] Alt text: ServiceNow initiate malware scan tag selected and highlighted in McAfee ePO.

        The ServiceNow Initiate Malware Scan tag you created is assigned to the On-Demand Scan action.

    6.  Select **OK**.

        In the Tags section, under the radio button and next to `Has any of these tags:`, the Initiate Malware Scan tag is displayed.

        \[Omitted image "mcafee\_tag\_action\_tag\_selected.png"\] Alt text: Send this task to only computers which have the following criteria option selected in McAfee ePO.

    7.  Select **Save**.

        On the System Tree page, the task is displayed on the Assigned Client Tasks list \(tab\).

        \[Omitted image "mcafee\_tag\_action\_4.png"\] Alt text: On-Demand scan highlighted in System Tree in McAfee ePO.

    8.  If you have not assigned an action to the Isolate Host action, repeat the previous steps to assign it.

    You have successfully installed the extension plugin, created security tags, and assigned tasks to your tags. You have completed the setup for the integration in your McAfee ePO console. The next step is to configure a server in your ServiceNow AI Platform instance.


**Parent Topic:**[McAfee ePO integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/mcaffee-epo-overview-arch.md)

**Previous topic:**[Set up your ServiceNow AI Platform instance for the McAfee ePO integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/mcaffee-epo-setup-now.md)

**Next topic:**[Install the application and configure a server for the McAfee ePO integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/mcaffe-epo-install.md)

