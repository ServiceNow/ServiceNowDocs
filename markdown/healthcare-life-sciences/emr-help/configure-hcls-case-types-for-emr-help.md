---
title: Configure healthcare case types for EMR Help
description: Configure healthcare case types for EMR Help to fulfill service requests made from the EMR Help portal.
locale: en-US
release: zurich
product: EMR Help
classification: emr-help
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configure healthcare case types for EMR Help

Configure healthcare case types for EMR Help to fulfill service requests made from the EMR Help portal.

The base healthcare case type \[sn\_hcls\_case\] is an abstract case type, which provides a foundation to extend from when building your own healthcare case types.

EMR Help provides a default record producer and request definition built on this base case type as an example of how you might configure your own.

You must configure your own healthcare case type to fulfill records created against the abstract case type. For more information on the abstract Healthcare case type, see [Healthcare case table](../reference/hcls-case-table.md).

The following steps walk you through creating a case type and modifying the default record producer and request definition to support it.

## Configuration requirements

-   A ServiceNow administrator
-   EMR Help
-   Healthcare and Life Sciences Service Management Core

