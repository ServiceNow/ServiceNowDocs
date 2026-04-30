---
title: Setting up Proactive Engagement
description: Setting up Proactive Engagement enhances the issue resolution capabilities of the organisation to help employees resolve their digital experience issues.
locale: en-US
release: yokohama
product: Proactive Engagement
classification: proactive-engagement
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Proactive Engagement, Proactive Engagement, Digital End-User Experience, IT Service Management]
---

# Setting up Proactive Engagement

Setting up Proactive Engagement enhances the issue resolution capabilities of the organisation to help employees resolve their digital experience issues.

## Before you begin

**Note:** Proactive Engagement integrates with ServiceNow DEX to proactively detect the digital experience issues.

-   Activate the Glide Virtual Agent plugin \(Id: com .glide.cs.chatbot\).
-   Install the ServiceNow Proactive Engagement application from the ServiceNow® Store.
-   Activate the Remedial actions framework plugin to use remedial actions as a resolution type.
-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do).
-   Review the Proactive Engagement application listing in the ServiceNow® Store for information on dependencies, licensing or subscription requirements, and release compatibility.

**Note:**

-   To view the Virtual Agent notifications:

    -   Set the system property **com.glide.cs.notification\_newuser\_webclient** to **True**.
    -   Navigate to **sys\_cs\_live\_agent\_setup.do?sys\_id=f0acbc4c5f091300e6333654de7313c8** and **enable** the notifications for all users.
-   To ensure no additional Virtual Agent conversations are triggered when an active conversation with the Virtual Agent:
    -   Enable the system property **sn\_pren.continue\_engagement\_if\_user\_is\_in\_active\_VA\_conversation** to ensure that no new Virtual Agent conversations are triggered when there's already an active conversation with Virtual Agent.

        When you are in an active conversation with the virtual agent, if a new conversation is triggered, an alert is created and an experience issue is created. Enabling this system property ensures to close the experience issue to **close\_skipped** state. All the close\_skipped experience issues will be triggered again if the issue still persists after 72 hrs.


Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Proactive Engagement application \(com.snc.proactive\_engagement\) using the filter criteria and search bar.

    **Note:** You can search for the application by its name or ID. If you cannot find the application, you must request it from the ServiceNow® Store. In the list next to the **Install**, the available versions are displayed.

3.  Select a version from the list and select **Install**.

    **Note:** Any dependencies that are installed along with the application are also listed.

4.  If you are prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


**Parent Topic:**[Configuring Proactive Engagement](configuring-proactive-engagement.md)

