---
title: Assessments and Surveys release notes
description: The ServiceNow Assessments and Surveys application enables you to create, send, and collect responses for surveys. Assessments and Surveys was enhanced and updated in the Xanadu release
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-01-29"
reading_time_minutes: 1
---

# Assessments and Surveys release notes

The ServiceNow® Assessments and Surveys application enables you to create, send, and collect responses for surveys. Assessments and Surveys was enhanced and updated in the Xanadu release

## Assessments and Surveys highlights for the Xanadu release

-   View the user responses only for active questions.

See [Exploring Assessments and Surveys](https://www.servicenow.com/docs/access?context=assessments-and-surveys&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for more information.

## Important information for upgrading Assessments and Surveys to Xanadu

Update the Automated Test Framework \(ATF\) tests, if you're upgrading to Xanadu from any version prior to Utah. In the Utah release, all the buttons on the assessments or surveys cards have been removed. To run ATF tests successfully, the Click the Take Survey button step must be replaced with the Click the Survey card step for all tests that have this step.

## New in the Xanadu release

-   **[Improved Survey Response Behavior](https://www.servicenow.com/docs/access?context=c_SurveyResults&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    To ensure consistency between the platform and portal, user responses to inactive survey questions are no longer viewable. Previously:

    -   On the platform, while taking the survey/assessment, both active and inactive questions were visible.
    -   On the portal, only active questions were visible.
    This update aligns platform and portal behavior. Only responses to active survey questions are accessible through the View User Response button on the assessment instance form, even if the user had answered them while the question was active. However, the responses will still be retained in the respective tables \(the response data will not be deleted from the instance\). On the response form, only active questions will be displayed

-   **[Quick start tests for Assessments and Surveys](https://www.servicenow.com/docs/access?context=quick-start-tests-survey&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    After upgrades and deployments of new applications or integrations, run quick start tests to verify that Assessments and Surveys works as expected. If you customized Assessments and Surveys, copy the quick start tests and configure them for your customizations.

    For more information, see [Quick start tests for Assessments and Surveys](https://www.servicenow.com/docs/access?context=quick-start-tests-survey&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).


## Activation information

Assessments and Surveys is a ServiceNow AI Platform feature that is active by default.

## Related ServiceNow applications and features

-   **[Employee Center](https://www.servicenow.com/docs/access?context=employee-center-landing-page&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

    After an assessment is assigned to users, the assigned assessment appears on the ServiceNow® Employee Center, where users can take the assessment.

-   **[Now Mobile app](https://www.servicenow.com/docs/access?context=now-mobile-app&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US)**

    Use the ServiceNow® Now Mobile app to take an assessment that is assigned to you.


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](now-platform-capabilities-rn-landing.md)

