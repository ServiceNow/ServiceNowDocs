---
title: Submit your app for approval and publishing
description: Start the process of getting the application you built in App Engine Studio \(AES\) published by submitting it for administrator review.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/app-engine-studio/submit-for-approval.html
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Publish your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Submit your app for approval and publishing

Start the process of getting the application you built in App Engine Studio \(AES\) published by submitting it for administrator review.

## Before you begin

Role required: delegated developer with permissions \(**Submit for deployment**, **Publish to app repo**, or **Publish to app store**, depending on the desired action\)

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  From the app home, select **Submit**.

4.  On the dialog box that appears, review the submission details and then select **Submit**.


## What to do next

The administrator reviews the submitted application and checks for potential issues. You can check the status of your application from the application home in App Engine Studio.

\[Omitted image "pending-approval-status.png"\] Alt text: Status is "Pending Approval"

After a reviewer begins testing the application, the status changes to `In Validation`.

\[Omitted image "in-validation-status.png"\] Alt text: Status is "In Validation"

An administrator may provide you with test accounts for different roles in your application. Log in with each of these accounts to check that the application works as expected.

If the reviewer rejects the application, the status changes to `Rejected`. You may also receive an email that includes the reviewer's comments. Use the feedback to improve your application, and then submit the application again.

\[Omitted image "rejected-status.png"\] Alt text: Status is "Rejected"

If the application passes testing, the administrator publishes the application and the status changes to `Published`. The administrator on-boards the team that requested the application. For example, if you specified a certain security role for the application, the administrator assigns that role to the relevant users.

\[Omitted image "published-status.png"\] Alt text: Status is "Published"

**Parent Topic:**[Publish your app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-studio/publish-your-app.md)

**Related topics**  


[Delegate developers using AES](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-studio/aes-app-dev-workflow.md)

