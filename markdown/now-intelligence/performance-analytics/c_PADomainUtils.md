---
title: PADomainUtils - Global
description: The PADomainUtils API enables you to copy Performance Analytics records between different domains on the same instance.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Domain separation and Performance Analytics, Configure Performance Analytics advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# PADomainUtils- Global

The PADomainUtils API enables you to copy Performance Analytics records between different domains on the same instance.

Use this API in server scripts to copy Performance Analytics records such as indicators, breakdowns, and dashboards, to different domains. This API enables you to create a Performance Analytics record in one domain and copy that record to any number of additional domains.

**Note:** This API cannot copy records into the Global domain.

**Warning:** When configuration records are moved to another domain, scores will not be accessible.

To use PADomainUtils, you must satisfy these requirements:

-   Performance Analytics must be enabled.
-   The user running the script must have the admin role.
-   The instance must use domain separation.
-   The script must be run from the global domain.
-   When moving or copying records, the source and target domains must be different.

-   **[PADomainUtils - PADomainUtils\(\)](../reference/r_PADU-PADomainUtils.md)**  
Instantiates a new PADomainUtils object to move or copy Performance Analytics records from the global domain.
-   **[PADomainUtils - PADomainUtils\(String domainFrom\)](../reference/r_PADU-PADomainUtils_String.md)**  
Instantiates a new PADomainUtils object to move or copy Performance Analytics records from the specified domain.
-   **[PADomainUtils - setFoundation\(Boolean foundation\)](../reference/r_PADU-setFoundation_boolean.md)**  
Use this method to move or copy only foundational records in a hybrid domain configuration.
-   **[PADomainUtils - setOverrides\(Boolean overrides\)](../reference/r_PADU-setOverrides_boolean.md)**  
Use this method before copying records to set the sys\_override value of the new record to the original parent record.
-   **[PADomainUtils - copy\(String runAs\)](../reference/r_PADU-copy_String.md)**  
Copies Performance Analytics records to a different domain.
-   **[PADomainUtils - copyJob\(String paJob, String runAs\)](../reference/r_PADU-copyJob_String_String.md)**  
Copies a Performance Analytics scheduled data collection job record to another domain.
-   **[PADomainUtils - copyDashboard\(String dashboardId, String runAs\)](../reference/PADU-copyDashboard_S_S.md)**  
Copy a dashboard to another domain.
-   **[PADomainUtils - move\(String runAs\)](../reference/r_PADU-move_String.md)**  
Moves Performance Analytics records to a different domain.
-   **[PADomainUtils - isWriteable\(String table, String id\)](../reference/r_PADU-isWriteable_String_String.md)**  
Evaluate if you can write to a specific record identified by table and sys\_id.

**Parent Topic:**[Domain separation and Performance Analytics](../../../../../use/performance-analytics/concept/c_PAWithDomainSeparation.md)

