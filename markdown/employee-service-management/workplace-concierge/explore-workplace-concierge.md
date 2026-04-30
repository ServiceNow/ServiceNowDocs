---
title: Explore Workplace Concierge
description: The Workplace Concierge application is a Workplace Service Delivery application designed to provide employees with real-time insights to optimize their workplace experience.
locale: en-US
release: yokohama
product: Workplace Concierge
classification: workplace-concierge
topic_type: concept
last_updated: "2025-04-28"
reading_time_minutes: 3
breadcrumb: [Workplace Concierge, Workplace Service Delivery, Employee Service Management]
---

# Explore Workplace Concierge

The Workplace Concierge application is a Workplace Service Delivery application designed to provide employees with real-time insights to optimize their workplace experience.

The Workplace Concierge application helps employees plan their on-site presence, improve in-person interactions using team collaboration, and set a routine to indicate the days that they plan to be in the office. The Concierge experience, that is, the Employee Presence module is available in the Workplace Service Portal, Employee Center, and also on the Now Mobile app.

## Presence dashboard

The Presence dashboard can be used to view and optimize employee presence in the workplace. Employees can create exceptions to update their in-office days without changing their routine and create reservations on the days that they’re planning to visit the office. Facility managers can use data from the dashboard to plan office space that supports the company's work needs.

The dashboard contains a calendar section with a personalized week view that displays the following information:

-   Employee routine
-   Routine exceptions
-   Routine exceptions at an alternate location
-   Collaborators planning to be in the office
-   Calendar insights about collaborators and reservations on a specific day
-   Personal insights that inform employees about being in office

![Presence dashboard showing the Insights and calendar sections.](../images/workplaceConcei-EmpPresForm.png "Presence dashboard")

**Note:**

-   Dashboard insights are generated after a set interval, which can be configured by the admin.
-   Calendar insights are generated when you open the dashboard and are updated every 30 minutes.

## Employee presence routine

The Workplace Concierge application enables employees to set their expected presence in the office. An employee can set the days of a week that they’re present at the office. An employee can also add their colleagues, managers, or stakeholders as collaborators to make them aware of their expected in-office presence during the week. By adding collaborators, employees can coordinate their in-office presence for better interaction, planning a meeting, or socializing.

![Add routines window showing the in-office days set, added collaborators, and privacy settings.](../images/workplaceConcei-EmpPres.png)

With the help of collaboration, employees can add each other as collaborators to be aware of each other's expected in-office days. They can plan their routines based on their work progress, meetings, plannings, and more. At any time, an employee can modify their in-office routine or set an exception for better interaction with the collaborators, boosting in-person interactions and performance.

An employee can set their in-office days using the Workplace Service Portal, the Employee Center, and also the Now Mobile app.

![Setting the employee presence routine using the Now Mobile app.](../images/workplaceConcei-EmpPresMobile.png)

As an admin using the Employee Presence module in the Workplace Concierge application, you can perform the following:

-   Make updates at any time, if necessary.
-   View the collaborators added for an employee. You can view the details of the employee to whom the collaborator is added.
-   View routine-related details such as the routine start and end date. At any time, only one employee routine is active. So, when an employee updates their routine, a record is created and the old record becomes invalid and is generated with an end date.
-   View routine exceptions raised by employees.
-   Add or remove sections displayed on the Presence dashboard.
-   Set the first day of the week in the calendar section using the **glide.ui.date\_picker.first\_day\_of\_week** system property.
-   Apply the filter on collaborators using the **sn\_wsd\_concierge.collaborators\_filter** system property. Based on the filter, the collaborators are displayed to employees while adding a collaborator. For more information about setting the property, see [Properties installed with Workplace Concierge](../reference/properties-installed-with-workplace-concierge.md).
-   Create insights for employees, which are personalized and displayed on the Presence dashboard and the calendar section. For more information, see [Create custom insights using Proactive Prompts](../task/create-insights-proactive-prompts.md).
-   Configure the changing the Signal Configuration schedule to update interval of dashboard insights.

## Workplace reservation suggestions

Workplace Concierge and Workplace Core administrators can configure workplace suggestions while suggesting a space to an employee for reservation. For more information, see [Configure workplace space suggestions for employees](configure-workplace-suggestions.md).

The employee can set their workplace schedule and in-office preferences in Workplace Service Delivery for Mobile. When suggesting a space to an employee using the Workplace Service Delivery for Mobile, application uses these preferences. For more information see, [Manage workplace schedule and in-office presence using Workplace Service Delivery for Mobile](../../wsd-for-mobile/concept/workplace-preference-schedule.md).

