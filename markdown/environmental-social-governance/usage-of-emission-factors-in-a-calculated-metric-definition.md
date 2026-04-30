---
title: Usage of emission factors in a calculated metric definition
description: When using an emission factor in a calculated metric definition \(CMD\), follow the specified guidelines to confirm accurate results.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Usage of emission factors in a calculated metric definition

When using an emission factor in a calculated metric definition \(CMD\), follow the specified guidelines to confirm accurate results.

1.  Date alignment:

    -   The start and end dates of your metric data must fall within the date range specified by the emission factor location.
    -   If your metric data start and end dates aren’t within this range, the calculation defaults to a value of 0.
2.  Location matching:

    -   The location associated with your metric data must match the location specified for the emission factor.
    -   If these locations don’t match, the system checks the parent location of the metric data. If the parent location matches an emission factor location, that emission factor value is used in the calculation.
    -   If the location matches but doesn’t fall within the valid date range of the emission factor location, the parent hierarchy of the location isn’t checked for calculations.
3.  Updating emission factor for older CMD's:

    -   Older emission factors does not have a recalculate button, making it challenging to update linked CMDs when emission factor values changes. While newly created CMDs offer a recalculate option when emission factors are updated, existing CMDs don't have this capability. To address this limitation, refer to [Enable recalculation for historical CMDs](https://support.servicenow.com/kb?sys_kb_id=53f0493293922e5cd9743f986cba10a0&id=kb_article_view) to update older CMDs and enable the recalculate button, ensuring they reflect the latest emission factor values.
    -   When you update an emission factor value and recalculate it, the system automatically reruns the calculations when a scheduled job automatically recalculates the data. This recalculation applies to the relevant dates within the emission factor's validity period. This confirms that CMD metrics data and CMD data are always up to date with the latest calculations, providing more accurate and reliable insights.

By verifying both the date and location alignment, you can accurately build your formulas for calculations.

**Parent Topic:**[Exploring Operational Sustainability Management \(formerly ESG Management\)](esg-new-explore.md)

