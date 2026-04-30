---
title: Service Owner Workspace Service Offering survey
description: Subscribers can rate their experience with service offerings via the Service Portfolio Management Premium Service Offering survey. This feedback provides portfolio managers and service owners with valuable information to improve service offering performance and subscriber satisfaction.
locale: en-US
release: xanadu
product: Service Owner Workspace
classification: service-owner-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Service Owner Workspace, Service Owner Workspace, IT Service Management]
---

# Service Owner Workspace Service Offering survey

Subscribers can rate their experience with service offerings via the Service Portfolio Management Premium Service Offering survey. This feedback provides portfolio managers and service owners with valuable information to improve service offering performance and subscriber satisfaction.

**Important:** As of the San Diego release, Service Owner Workspace is in a planned deprecation. New customers can't find or activate Service Owner Workspace. ServiceNow® continues to support existing customers with Service Owner Workspace. For information on the product replacement and the deprecation process, see [Service Owner Workspace](SPM2-premium.md).

<table id="table_e2x_rbr_nkb"><tbody><tr><td>

![Navigate](../image/SOWUseBanner2.png "Navigate")

</td></tr></tbody>
</table>In the base system, a predefined SPM Service Offering Survey is available. Surveys are sent for operational and retiring service offerings only. Portfolio admins \[portfolio\_admin\] can edit the survey and service editors \[service\_editor\] can configure the associated trigger conditions.

You must have the admin or portfolio\_admin role to modify the SPM Service Offering Survey. To view the survey, navigate to **Survey** &gt; **View Surveys**.

The SPM Service Offering Survey is triggered randomly for 10% of service offering subscribers. Only subscribers who have not been polled within the previous three-month time period can receive a survey. Subscribers receive an email with the survey link. The service offering name is displayed and the survey inquires how satisfied the subscriber is with the service or service offering. Subscribers use radio buttons to rate satisfaction on a 1 through 5 scale, with 1 being not satisfied and 5 being very satisfied.

You are encouraged to modify the survey to better match your organizations needs.

Two system properties determine the percentage of subscribers to receive the survey and how often a subscriber is polled.

-   **sn\_spm.csat.survey\_probability**: Default value is 10% of subscribers are randomly polled.
-   **sn\_spm.csat.survey\_period**: Default value is 90 days. The system does not send a survey to a subscriber who has been polled within the previous 90 days.

Service owners can use the Service Offering form to define how often to send a CSAT survey. The**CSAT survey frequency** field offers the following frequency choices:

-   **Never** \(default\)
-   **Daily**
-   **Weekly**
-   **Monthly**

Service owners can view the last time a survey was sent for an offering in the **CSAT survey last sent** field on the Service Offering form.

Portfolio managers and service owners can review responses and view vendor CSAT weight in Service Owner Workspace.

For more detailed information about working with surveys, trigger conditions, and survey questions, see [Surveys](https://www.servicenow.com/docs/access?context=r_SurveyManagementLandingPage&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

