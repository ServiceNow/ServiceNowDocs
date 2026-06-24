---
title: Embed a playbook in ServiceNow mobile
description: Embed a playbook in ServiceNow mobile by creating a screen in Mobile App Builder.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/embed-playbook-mobile.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure a playbook for ServiceNow mobile, Design Playbook Experience, Playbooks, Workflow Studio, Build workflows]
---

# Embed a playbook in ServiceNow mobile

Embed a playbook in ServiceNow® mobile by creating a screen in Mobile App Builder.

## Before you begin

Role required: admin

If you haven't configured your playbook for ServiceNow® mobile in UI Builder yet, see [Configure a playbook for ServiceNow mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/configure-playbook-mobile.md).

## Procedure

1.  Create a playbook screen
2.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

3.  Search for and select the scope of the application that you want to create a screen for.

    \[Omitted image "mobile-app-builder-landing.png"\] Alt text: The Mobile App Builder landing page

4.  Navigate to **Screens**.

    \[Omitted image "mobile-app-builder-screens.png"\] Alt text: Navigating to Screens

5.  To create new screen, select **New**.

6.  In the **Create a screen** modal, select **Mobile Web**.

    \[Omitted image "create-screen-mobile-web.png"\] Alt text: Create a screen modal

    The form for a new mobile web screen appears.

    \[Omitted image "new-mobile-web-screen.png"\] Alt text: Form for a new mobile web screen

7.  Give your mobile web screen a name and description.

8.  Choose an icon for your mobile web screen.

9.  Under **Screen Settings**, enter the URL of your mobile playbook.

    \[Omitted image "create-screen-mobile-web-form.png"\] Alt text: Properties for the mobile web screen

    **Important:** The **web\_controller\_spinner=on** parameter is important to include for proper loading behavior on mobile.

    /now/playbook-mobile/playbook/interaction/-1/params/view/stages​​​​​​​?web\_controller\_spinner=on

10. If you have any roles you want to limit this screen to, or any other configurations you would like to learn more about, see .

11. **Save** the screen.

    Your mobile web screen is configured for your playbook.

12. Configure the Mobile Agent
13. Navigate back to the scope level by selecting the home icon \(\[Omitted image "home-icon-app-scope.png"\] Alt text: Home icon that brings you back to the scope level\).

14. Select **Mobile app configs**.

    \[Omitted image "nav-to-mobile-agent.png"\] Alt text: Navigating to the Mobile Agent

15. Select **Mobile Agent**.

16. In the banner message at the top, select **Edit in original scope**.

    \[Omitted image "edit-original-scope.png"\] Alt text: Edit in original scope banner message

17. In the component tree, select the **Launcher screen** component.

18. 
## Result

Your playbook is now embedded in ServiceNow® mobile.

