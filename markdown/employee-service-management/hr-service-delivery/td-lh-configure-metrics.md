---
title: Configure metrics for employee engagement
description: Use the Leader Hub Metric Configurations table to configure metrics for employee engagement with certain applications in the Talent Development suite. The configurable options are applicable to the metrics that appear in the Growth engagement widget and the employee cards on the Org talent page.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Install and configure, Leader Hub, HR Service Delivery, Employee Service Management]
---

# Configure metrics for employee engagement

Use the Leader Hub Metric Configurations table to configure metrics for employee engagement with certain applications in the Talent Development suite. The configurable options are applicable to the metrics that appear in the Growth engagement widget and the employee cards on the Org talent page.

## Before you begin

Role required: admin \[sn\_egd\_lh.admin\]

## Procedure

1.  Navigate to **All** &gt; **Leader Hub** &gt; **Leader Hub Metric Configuration**.

2.  Select a record in the list to revise an existing configuration or select **New** to create a configuration.

3.  Specify the name of the application for which you're creating metrics in the **Name** field.

    **Tip:** Refer to the options in the **Metric** field to determine the application for which you want to create metrics.

4.  Make your employee engagement metric available to leaders by selecting the check box associated with the **Active** field.

5.  Indicate the sequential order in which your employee engagement metric appears by entering a numeric value in the **Order** field.

    **Tip:** The employee engagement metric you configure for the application you specify in the **Metric** field appears in the Growth engagement widget in the following order: from lowest **Order** field value to highest.

6.  Add an image for the employee engagement metric that you create by selecting the **Lookup using list** icon in the **Icon** field.

7.  Select an application from the drop-down list associated with the **Metric** field that matches the application you specified in the **Name** field.

8.  Select an option from the drop-down list associated with the **Metric Calculation Base** field to specify the base for the metric calculation.

    |Option|Description|
    |------|-----------|
    |**Employees Count**|Metrics for employee engagement are calculated based on the number of employees using the application you specify in the **Metric** field.|
    |**Managers Count**|Metrics for employee engagement are calculated based on the number of managers using the application you specify in the **Metric** field.|
    |**ICs Count**|Metrics for employee engagement are calculated based on the number of individual contributors using the application you specify in the **Metric** field.|

9.  Enter a description in the **Description** field to describe the metric you're configuring for the application you specified in the **Metric** field.

    |Application|Description|
    |-----------|-----------|
    |**Aspirations**|of &lt;personnel&gt; have active aspirations|
    |**Growth Plans**|of &lt;personnel&gt; have active growth plans|
    |**Conversations**|of &lt;personnel&gt; have had conversations|
    |**Learning**|of &lt;personnel&gt; have completed courses|
    |**Mentoring**|of &lt;personnel&gt; are involved in mentorships|

    **Tip:** `<personnel>` represents the role that you specified in the **Metric Calculation Base** field \(i.e., employee, manager, or individual contributor\). The description you enter appears underneath the percentage that is calculated for the employee engagement metric you create. Using the description provided for the Aspirations app, the Growth engagement widget displays the following message: `<percentage>` of `<personnel>` have active aspirations.

10. Enter alternate text in the **Tooltip** field to provide further details about the employee engagement metric you're configuring.

    **Tip:** Use the tooltip to display text about the calculation for the metric you're configuring. For example, if you're configuring metrics for the Aspirations app, and metrics are calculated based on the number of employees with a minimum of one aspiration that is in progress, enter `Employees with at least one-in-progress aspiration` in the **Tooltip** field. This text appears when you hover your cursor over the icon appended at the end of the description.

11. Enter `now/leader-hub-analytics/<UIB page>` in the **Analytics URL** field.

    **Tip:** &lt;UIB page&gt; represents the name of the user interface builder \(UIB\) page. The name of the application for which you're configuring metrics is the UIB page name by default. For example, if you're configuring metrics for the Aspirations app and you're using the default UIB page, enter `now/leader-hub-analytics/aspirations`.

12. Select the check box associated with the **Enable on Talent Visibility** field to make your employee engagement metric visible on the Org talent page when you view a card that contains information about an employee.

13. Use the **Domain** field to specify the domain in which your metric configuration data is available.


## Result

The employee engagement metric that you configured appears in the Growth engagement widget. The Growth engagement widget appears on the At a glance page.

**Parent Topic:**[Installing and configuring Leader Hub](../concept/td-lh-install-config.md)

