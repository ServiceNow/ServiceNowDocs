---
title: Surge Modal Redirect
description: Handle high concurrency events on the employee portal home page by showing a pop-up modal if there's a live company event.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/ec\_home\_surge\_modal\_redirect.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-09-04"
reading_time_minutes: 2
breadcrumb: [Company events, Creating employee communications, Manage, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Surge Modal Redirect

Handle high concurrency events on the employee portal home page by showing a pop-up modal if there's a live company event.

## Before you begin

-   Role required:
    -   sn\_cd.content\_admin
    -   sn\_cd.content\_manager

## About this task

A redirect is implemented on the Employee Center Pro home page when a company event has been activated on the portal and meets or exceeds the surge traffic threshold for that event. This is intended to direct users to the relevant company event.

The surge modal redirect improves performance by providing a modal that intercepts the portal home page early to prevent calls before other widgets and mega menu items are loaded.

**Note:** This feature works when there’s a live **Company Events** scheduled.

## Procedure

1.  Navigate to **Content Publishing****Advanced****Properties**

2.  Event modal property must be toggled on by selecting **Yes**.

3.  \[Omitted image "ce-surge-modal-property.png"\] Alt text: Select Yes to display the event modal on homepage

    **Note:** For **customized portal themes**, the surge modal is not displayed unless the same UI script on m2m\_sp\_theme\_js\_include is added. **Out of the box themes** already have the UI script.

4.  For creating **Company event** see, [Create a company event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/create-company-event.md)

5.  **Note:** Content Admin is required to create a company event.

6.  Search for scheduled job **Precompute Audience for Company Events** and check the **Precomputed Audiences** table.

7.  \[Omitted image "ce-precomputed-audiences.png"\] Alt text: Lists the content, domain and user for precomputed audiences

    **Note:** A scheduled job runs every night to check for company events that are going live in the next 30 hours and populates the audience group with users who have permission to see the event.

    **Note:** For customized themes, check that it has the UI script in **m2m\_sp\_theme\_js\_include**. Check that the employee center header widget used in the portal has the updated server script storing data.

8.  The modal intercept populates a message with a confirmation to select **Yes, go to event**or **No** for not proceeding to the live event, and continue to access to the home page.

9.  \[Omitted image "ce-surge-modal-notif.png"\] Alt text: Allows you to select Yes, or No for proceeding to live event

    **Note:** The surge modal intercepts the employee portal home page before the usual widgets and navigation menu load. If you choose not to see the modal, it 's not shown again unless you log out or use in a different browser.

10. Live event details or home page will be redirected depending on what option you chose.

    If **Yes, go to event** is chosen, you proceed to live event details page. If **No** is chosen, you continue to the home page.


**Parent Topic:**[Company events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/ec-company-events.md)

