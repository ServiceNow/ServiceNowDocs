---
title: Indicators used in the CMDB success advisor for HAM dashboard
description: Indicators enable viewing of high-level metrics that highlight data quality, completeness, and synchronization issues across hardware assets and configuration items \(CIs\).
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use HAM advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Indicators used in the CMDB success advisor for HAM dashboard

Indicators enable viewing of high-level metrics that highlight data quality, completeness, and synchronization issues across hardware assets and configuration items \(CIs\).

## CMDB success advisor for HAM dashboard indicators

-   **Assets created for virtual CIs**

    Total number of virtual CI assets in the Hardware \[alm\_hardware\] table created daily, where the life cycle stage of CI is operational, the asset field is not empty, and the CI is marked as virtual.

-   **Assets missing CI**

    Total number of hardware assets in the Hardware \[alm\_hardware\] table missing a linked CI from the Hardware \[cmdb\_ci\_hardware\] class, measured daily, where the CI is operational, the asset is actively in use, and no CI is linked to the asset.

-   **CI install status vs. asset state matched**

    All CI records from the Hardware \[cmdb\_ci\_hardware\] class where the installation status correctly aligns with the expected asset state, promoting accurate and reliable asset management.

-   **CI install status vs. asset state mismatched**

    All CI records from the Hardware \[cmdb\_ci\_hardware\] class with an installation status that doesn’t align with the expected asset state, resulting in erroneous asset management.

-   **CIs missing asset**

    Total number of CI records from the Hardware \[cmdb\_ci\_hardware\] class missing a linked asset, measured daily, where the life cycle stage of CI is operational and no asset is associated with the CI.

-   **CIs missing assigned to**

    Total number of CI records from the Hardware \[cmdb\_ci\_hardware\] class missing an assigned owner, measured daily, where the CI lacks an assigned owner.

-   **CIs missing location**

    Total number of CI records from the Hardware \[cmdb\_ci\_hardware\] class missing a location, measured daily, where the CI doesn’t have a location assigned.

-   **CIs missing managed by group**

    Total number of CI records from the Hardware \[cmdb\_ci\_hardware\] class missing a managed by group, measured daily, where the CI doesn’t have a managed by group assigned.

-   **CIs missing manufacturer**

    Total number of CI records from the Hardware \[cmdb\_ci\_hardware\] class missing a manufacturer, measured daily, where the CI doesn’t have a manufacturer specified.

-   **CIs missing model ID**

    Total number of CI records from the Hardware \[cmdb\_ci\_hardware\] class missing a model ID, measured daily, where the CI doesn’t have a model ID or model display name specified.

-   **CIs missing model name**

    Total number of CI records from the Hardware \[cmdb\_ci\_hardware\] class missing a model name, measured daily, where the CI doesn’t have a model name specified, with or without a model ID.

-   **CIs missing model number**

    Total number of CI records from the Hardware \[cmdb\_ci\_hardware\] class missing a model number, measured daily, where the CI is not associated with a model ID, or is associated with a model ID that is missing a model number.

-   **CIs missing owner**

    Total number of CI records from the Hardware \[cmdb\_ci\_hardware\] class missing an owner, measured daily, where the CI doesn’t have an owner assigned.

-   **CIs missing serial number**

    Total number of CI records from the Hardware \[cmdb\_ci\_hardware\] class missing a serial number, measured daily, where the CI doesn’t have a serial number assigned.

-   **CIs not updated in last 7 days**

    Total number of CI records from the Hardware \[cmdb\_ci\_hardware\] class not updated in the last seven days, measured daily, where the update timestamp is older than seven days.

-   **CIs not updated in last 14 days**

    Total number of CI records from the Hardware \[cmdb\_ci\_hardware\] class not updated in the last 14 days, measured daily, where the update timestamp is older than 14 days.

-   **CIs not updated in last 30 days**

    Total number of CI records from the Hardware \[cmdb\_ci\_hardware\] class not updated in the last 30 days, measured daily, where the update timestamp is older than 30 days.

-   **CIs not updated in last 60 days**

    Total number of CI records from the Hardware \[cmdb\_ci\_hardware\] class not updated in the last 60 days, measured daily, where the update timestamp is older than 60 days.

-   **CIs not updated in last 90 days**

    Total number of CI records from the Hardware \[cmdb\_ci\_hardware\] class not updated in the last 90 days, measured daily, where the update timestamp is older than 90 days.

-   **Hardware CIs group by**

    Total number of CI records from the Hardware \[cmdb\_ci\_hardware\] class, measured daily and grouped by model category and discovery source.


