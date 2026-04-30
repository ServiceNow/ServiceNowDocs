---
title: Events related to the Listening Posts surveys on User Experience Analytics dashboard
description: The User Experience Analytics dashboard displays events to understand the users behavior when interacting with the Listening Posts survey widgets.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [User Experience for HR Service Delivery, Integration of HR Service Delivery with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# Events related to the Listening Posts surveys on User Experience Analytics dashboard

The User Experience Analytics dashboard displays events to understand the users behavior when interacting with the Listening Posts survey widgets.

You can evaluate the successful and unsuccessful attempts of an employee related to the Listening Posts My survey and Take survey widgets by viewing two related events on the User Experience Analytics dashboard: Successful submissions at survey response and Unsuccessful attempts at survey response. For example, understanding the average time taken by an employee to respond to a survey, or view the number of resignations in the survey process could help you evaluate how to improve the design of future surveys or indicate whether more encouragement is needed to increase employee participation.

## Successful submissions at survey response

On Listening Posts survey widgets, the Successful submissions event indicates that the users have attempted the survey and were able submit it without any difficulty. The following image shows the dashboard charts that display employee interactions on the widgets as actions on the associated properties.

![User Experience Analytics dashboard - Successful submission.](../image/lp-analytics-appsee-succ-submit.png "User Experience Analytics dashboard")

-   Distribution of time spent.

    The percentage of average time spent by an employee either on the My survey widget or the Take survey widget. The time spent data is grouped in time durations of &lt;30 seconds, &gt;30 seconds, or &gt;60 seconds.

-   Submissions with flow change.

    **Note:** This metric applies only to the My survey widget.

    A flow change is any alteration to the natural course of a flow, for example, the user navigating backward rather than proceeding forward. This chart displays the percentage of flow change by user's who Navigated forward or Navigated back when taking the survey.

-   Submissions with comments across widgets.

    The percentage of submissions with comments across the Listening Posts My survey and Take survey widgets.

-   Submissions across surveys.

    The percentage of successful submissions across various surveys. For example, the sample image shows the percentage of submissions distributed across PS1 and PS2 surveys.

-   Distribution of submissions across widgets \(My Survey &amp; Take survey\).

    The percentage of successful submissions distributed across the Listening Posts My survey and Take survey widgets.


**Note:** On the dashboard, the Channels, Applications, Page Id, and Instance Id charts are default properties that are not custom-defined for the Listening Posts widgets.

## Unsuccessful attempts at survey response

On Listening Posts survey widgets, the Unsuccessful attempts event indicates that the users have attempted the survey but were not able complete it or submit it. The following image shows the dashboard charts that display employee interactions on the widgets as actions on the associated properties.

![User Experience Analytics dashboard - Unsuccessful attempts.](../image/lp-analytics-appsee-unsucc-attempt.png "User Experience Analytics dashboard")

An attempt is defined by the actions performed in any of the following three properties: Distribution of time spent, Attempts to rate, and Attempts to comment.

-   Distribution of time spent \(on either of the widgets\).

    The percentage of average time spent by an employee. The time spent can be either on the My survey or Take survey widget. The time spent data is grouped in time durations of &gt;10 seconds, &gt;60 seconds, or &gt;120 seconds.

-   Attempts to rate.

    The percentage of unsuccessful attempts to rate a survey. True indicates that the employee clicked on a rating but did not submit it and False means the employee clicked on the rating and submitted it.

-   Attempts to comment.

    The percentage of unsuccessful attempts to comment by clicking the comments box on the widget. True indicates that the employee typed the comment but did not submit it and False means employee typed the comment and submitted it.

-   Attempts across surveys.

    The percentage of unsuccessful attempts across various surveys. For example, the sample image shows the percentage of attempts distributed across PS1 and PS2 surveys.

-   Distribution of attempts across widgets \(My survey &amp; Take survey\).

    The percentage of unsuccessful attempts distributed across the Listening Posts My survey and Take survey widgets.


**Parent Topic:**[User Experience for HR Service Delivery](user-exp-hrser.md)

