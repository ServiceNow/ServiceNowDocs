---
title: Use Predictive Intelligence for Legal Service Delivery
description: Use the Predictive Intelligence solution to predict and auto populate or view the suggestions for sub-category and assignment group.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/employee-service-management/legal-service-delivery/lsd-pi-use-legal-request.html
release: xanadu
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use Predictive Intelligence for Legal Service Delivery, Predictive intelligence for Legal Service Delivery, Integration of Legal Service Delivery with ServiceNow applications, Legal Service Delivery, Employee Service Management]
---

# Use Predictive Intelligence for Legal Service Delivery

Use the Predictive Intelligence solution to predict and auto populate or view the suggestions for sub-category and assignment group.

## Before you begin

Role required: sn\_lg\_ops.legal\_fulfiller

## About this task

-   Ensure you have installed and configured the Predictive Intelligence for Legal Service Delivery plugin \(sn\_lg\_pi\). For more information, see [Configure Predictive Intelligence for Legal Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/legal-service-delivery/lsd-PI-configure-landing.md)
-   Ensure the solution definitions are trained on your ServiceNow instance.
-   When a legal request is submitted, the Predictive Intelligence feature predicts values for the subcategory and assignment group based on solution definitions.
-   Under the following conditions, the values are predicted again.

    -   When the short description or description is modified, the subcategory is predicted again.
    -   When short description, description or subcategory is modified, the assignment group is predicted again.
    The conditions under which the values are predicted again are defined in the business rules. For more information, see [Solution definitions and business rules for Predictive Intelligence for Legal Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/legal-service-delivery/lsd-pi-solution-defn-br.md)


## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  Click the list icon \(\[Omitted image "checklist-icon.png"\] Alt text: List icon\).

3.  In the **Lists** tab, open a General Legal Request or Ethics Complaints by selecting an option under **Legal Requests**.

    -   Predictions for Subcategory and Assignment group are available.
    -   Fields with high confidence predictions are automatically updated with the predicted value.
    -   Fields with medium and low confidence predictions are not automatically updated but the values are shown as suggestions.
    -   The Activity stream is also updated with the predicted values. You can customize the activity stream to display additional fields. For more information, see [Configure fields to be displayed in Activity stream](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/legal-service-delivery/lsd-configure-activity-stream.md).

**Parent Topic:**[Use Predictive Intelligence for Legal Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/legal-service-delivery/lsd-PI-use-landing.md)

