---
title: License Report form
description: Description of the fields on the License Report form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/license-report-form.html
release: zurich
product: IT Operations Management
classification: it-operations-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ITOM/OT SU Licensing Reference, ITOM/OT SU Licensing and subscriptions, IT Operations Management]
---

# License Report form

Description of the fields on the License Report form.

<table id="table_txl_kbm_szb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CI Category

</td><td>

Grouping of Configuration Items \(CIs\) in each application based on shared characteristics or attributes. For the list of supported CI categories, including 2026 Packaging SKUs, see [Subscriptions for Operational Technology Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/otm-license-module.md)

</td></tr><tr><td>

Domain

</td><td>

Domain to which the CI belongs.

</td></tr><tr><td>

Total Count

</td><td>

Average of 90 daily counts of CIs categorized by CI types, within each ITOM application.

 **Note:** The total count adheres to the above definition only if the **Aggregated** condition in the filter is set as **true**. When the **Aggregated** condition is set as **false**, the total count represents the daily count for a specific application and category on that day.

</td></tr><tr><td>

Subscription Unit Ratio

</td><td>

Number of CIs, in a specific category that need a subscription, that are counted as one Subscription Unit. SU ratio is determined by your customer contract.

</td></tr><tr><td>

Total Subscription Units Consumed

</td><td>

Total number of subscription units consumed by ITOM applications within a specific timeframe.

 The licensing module calculates this number by using the subscription units ratio with the count of CIs in each CI category.

</td></tr><tr><td>

Sum

</td><td>

Total consumption of subscription units by the application and all ITOM applications.

 Appears highlighted under Total Subscription Units Consumed.

</td></tr></tbody>
</table>**Note:** To estimate the predicted usage under 2026 Packaging SKUs, see [Generate CI consumption predictions for 2026 Container Packaging SKU migration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/generate-ci-consumption-predictions.md)

**Parent Topic:**[ITOM/OT SU Licensing Reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/itom-su-licensing-reference.md)

