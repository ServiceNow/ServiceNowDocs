---
title: Embed a playbook in ServiceNow mobile
description: Embed a playbook in ServiceNow mobile by creating a screen in Mobile App Builder.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-11-24"
reading_time_minutes: 1
breadcrumb: [Configure a playbook for ServiceNow mobile, Designing playbooks, Use, Workflow Studio, Build workflows]
---

# Embed a playbook in ServiceNow mobile

Embed a playbook in ServiceNow® mobile by creating a screen in Mobile App Builder.

## Before you begin

Role required: admin

If you haven't configured your playbook for ServiceNow® mobile in UI Builder yet, see [Configure a playbook for ServiceNow mobile](configure-playbook-mobile.md).

## Procedure

1.  Create a playbook screen
2.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

3.  Search for and select the scope of the application that you want to create a screen for.

    ![image.mobile-app-builder-landing]

4.  Navigate to **Screens**.

    ![image.mobile-app-builder-screens]

5.  To create new screen, select **New**.

6.  In the **Create a screen** modal, select **Mobile Web**.

    ![image.create-screen-mobile-web]

    The form for a new mobile web screen appears.

    ![image.new-mobile-web-screen]

7.  Give your mobile web screen a name and description.

8.  Choose an icon for your mobile web screen.

9.  Under **Screen Settings**, enter the URL of your mobile playbook.

    ![image.create-screen-mobile-web-form]

    **Important:** The **web\_controller\_spinner=on** parameter is important to include for proper loading behavior on mobile.

    /now/playbook-mobile/playbook/interaction/-1/params/view/stages​​​​​​​?web\_controller\_spinner=on

10. If you have any roles you want to limit this screen to, or any other configurations you would like to learn more about, see [Configure a mobile web screen](https://www.servicenow.com/docs/access?context=sg-configure-url-screen&version=zurich&pubname=zurich-mobile&ft:locale=en-US).

11. **Save** the screen.

    Your mobile web screen is configured for your playbook.

12. Configure the Mobile Agent
13. Navigate back to the scope level by selecting the home icon \(![image.home-icon-app-scope]\).

14. Select **Mobile app configs**.

    ![image.nav-to-mobile-agent]

15. Select **Mobile Agent**.

16. In the banner message at the top, select **Edit in original scope**.

    ![image.edit-original-scope]

17. In the component tree, select the **Launcher screen** component.

18. 
## Result

Your playbook is now embedded in ServiceNow® mobile.

**Parent Topic:**[Configure a playbook for ServiceNow mobile](configure-playbook-mobile.md)

