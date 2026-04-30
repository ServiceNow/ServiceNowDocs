---
title: Tutorial part 9: Create an app workspace
description: Add a workspace to your app for volunteer admins to use. While managing and configuring workspaces may traditionally be a complex and time-consuming task, the integration of Workspace Builder within ServiceNow Studio makes it a much simpler and more streamlined process.
locale: en-US
release: yokohama
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ServiceNow Studio tutorial, Exploring ServiceNow Studio, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# Tutorial part 9: Create an app workspace

Add a workspace to your app for volunteer admins to use. While managing and configuring workspaces may traditionally be a complex and time-consuming task, the integration of Workspace Builder within ServiceNow Studio makes it a much simpler and more streamlined process.

## Before you begin

Role required: admin or delegated\_developer

## Procedure

1.  From the We Volunteer app dashboard, select **Create** &gt; **File**.

2.  Enter **We Volunteer** in the Application field.

3.  Under the User Interface category, select **Workspace**.

4.  Select **Continue**.

5.  Select **Begin**.

6.  Verify that the information you see matches the following:

    -   Name: We volunteer
    -   Description: Can be blank
    -   URL: we-volunteer \(/now/we-volunteer\)
    -   Roles: x\_snc\_we\_volunteer.event\_reg.admin, x\_snc\_we\_volunteer.event\_reg.attendee, and x\_snc\_we\_volunteer.event\_reg.organizer
7.  Select **Continue**.

8.  Verify that the Primary table is **Event** and secondary tables are **Attendee** and **Volunteer Survey Response**.

    You can type the tables into the fields, but make sure the table names begin with x\_snc\_we\_volunteer\_.

9.  Select **Continue**.

10. Select **Edit**.

11. Explore more about Workspace Builder or select **Don't show me this again**.

12. Select **Get Started**.

13. Select **List**.

14. Under Event, select **Add filtered list** and add the following information:

    -   Name: Upcoming Events
    -   Table: Event
15. Select **Add**.

16. On the right side under Configurations, select **Apply Conditions**.

17. Enter the following condition to filter the records: `Starts at or after Today`.

18. Select **Apply filter**.

19. Select **Save**.

20. Select **Home**.

21. Select **Add a tab**.

22. Select the pencil icon and enter: `Volunteer Survey Response`.

23. Select **Add new element**, and select **Data visualization**.

24. Select **Saved visualization**.

25. Select the **Filter by name or description** text input box.

26. Enter `We Volunteer` and select **Search**.

27. Select the check box next to Name to select all the reports.

28. Select **Add to Dashboard**.

29. Select **Save**.


## Result

Congratulations! You have completed the lab and created the We Volunteer app in ServiceNow Studio.

**Parent Topic:**[ServiceNow Studio tutorial](../concept/lab-sns-lab-guide.md)

