---
title: Policy status aggregation in a multi-product release
description: In a multi-product release, the policy run status of releases for all primary and included products are rolled up to the policy status of the main release.
locale: en-US
release: zurich
product: Digital Product Release
classification: digital-product-release
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Digital Product Release, IT Service Management]
---

# Policy status aggregation in a multi-product release

In a multi-product release, the policy run status of releases for all primary and included products are rolled up to the policy status of the main release.

## Example of a policy status aggregation

Consider a release with a primary product or service and three related products. Each phase has policies mapped to it. You can run policies on the current phase from the main release or from an included product release.

**Note:** Removing a policy from an in-progress phase triggers automatic re-evaluation of the remaining policies. The aggregated policy status for the phase is recalculated based on the remaining policies.

The following table shows how the aggregated status is calculated from the status of each release.

|Status for primary product or service|Status for Included product 1|Status for Included product 2|Status for Included product 3|Aggregated status on the main release|
|-------------------------------------|-----------------------------|-----------------------------|-----------------------------|-------------------------------------|
|Not run|Not run|Not run|Not run|**Not run**|
|Not run|Non-compliant|Non-compliant|Non-compliant|**Not run**|
|Not run|Compliant|Compliant|Compliant|**Not run**|
|Non-compliant|Compliant|Compliant|Compliant|**Non-compliant**|
|Compliant|Compliant|Compliant|Compliant|**Compliant**|
|Compliant|Compliant|Compliant|Compliant with exception|**Compliant with exception**|

**Parent Topic:**[Digital Product Release reference](../concept/dpr-reference.md)

