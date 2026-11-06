---
title: Set up Proactive Engagement
description: Set up Proactive Engagement to help employees proactively resolve their digital experience issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/setting-up-proactive-engagement.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure, Digital End-User Experience, IT Operations Management]
---

# Set up Proactive Engagement

Set up Proactive Engagement to help employees proactively resolve their digital experience issues.

## Before you begin

**Note:** Proactive Engagement integrates with ServiceNow DEX to proactively detect the digital experience issues.

-   The Glide Virtual Agent plugin \(com.glide.cs.chatbot\) must be active.
-   Install the ServiceNow Proactive Engagement application from the ServiceNow® Store.
-   To use remedial actions as a resolution type, the Remedial actions framework plugin must be active.
-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do).
-   Review the Proactive Engagement application listing in the ServiceNow® Store for information on dependencies, licensing or subscription requirements, and release compatibility.

**Note:**

-   To view the Virtual Agent notifications:

    -   Set the system property **com.glide.cs.notification\_newuser\_webclient** to **True**.
    -   Navigate to `sys_cs_live_agent_setup.do?sys_id=f0acbc4c5f091300e6333654de7313c8` and turn on the notifications for all users.
-   To avoid triggering additional Virtual Agent conversations during an active Virtual Agent conversation:
    -   Turn on the system property **sn\_pren.continue\_engagement\_if\_user\_is\_in\_active\_VA\_conversation** so that no new Virtual Agent conversations are triggered when a conversation with Virtual Agent is already active.

        When you are in an active conversation with the virtual agent, if a new conversation is triggered, an alert is created and an experience issue is created. Turning on this system property closes the experience issue in the **close\_skipped** state. All close\_skipped experience issues are triggered again if the issue persists after 72 hours.


Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Proactive Engagement application \(com.snc.proactive\_engagement\) using the filter criteria and search bar.

    **Note:** You can search for the application by its name or ID. If you cannot find the application, you must request it from the ServiceNow® Store. The available versions appear in the list next to the **Install** button.

3.  Select a version from the list and select **Install**.

    **Note:** Any dependencies that are installed along with the application are also listed.

4.  If you are prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


