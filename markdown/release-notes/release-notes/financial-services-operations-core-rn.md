---
title: Financial Services Operations Core release notes
description: The ServiceNow Financial Services Operations Core application provides a data model that enables financial institutions to create flexible data structures that meet their business needs. Financial Services Operations Core was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-06"
reading_time_minutes: 2
---

# Financial Services Operations Core release notes

The ServiceNow® Financial Services Operations Core application provides a data model that enables financial institutions to create flexible data structures that meet their business needs. Financial Services Operations Core was enhanced and updated in the Australia release.

## Financial Services Operations Core highlights for the Australia release

The case type selector in Financial Services Operations now uses the predefined Customer Service Management \(CSM\) implementation, replacing the previous FSO-specific override.

See [Case type selector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-case-type-select-modals.md) for more information.

**Important:** Financial Services Operations Core is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Changed in this release

-   **[Case type selector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-case-type-select-modals.md)**

    Filter service definitions using the case type selector in FSO with the predefined CSM implementation. For upgraded instances, existing agent criteria and customer condition data is automatically migrated from the deprecated FSO tables to the CSM tables during upgrade. No manual migration is required.

    To configure agent criteria or customer conditions for the case type selector, use the following CSM tables:

    -   `sn_csm_case_types_service_user_criteria`: for agent criteria
    -   `sn_csm_case_types_service_customer_criteria`: for customer conditions

## Deprecated features

-   The FSO tables `sn_bom_m2m_service_definition_user_criteria` and `sn_bom_m2m_service_definition_customer_condition` are deprecated. If you're on an upgraded instance, you can continue to reference these tables, but they're no longer maintained. Use `sn_csm_case_types_service_user_criteria` and `sn_csm_case_types_service_customer_criteria` instead. For more information, see [FSO Core Banking tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/fso-core-banking-tables.md).
-   The **Show in Interceptor** field \(`show_in_interceptor`\) on the `sn_bom_service_definition` table is deprecated. Use agent criteria in the `sn_csm_case_types_service_user_criteria` table to control which service definitions appear in the case type selector.

    User criteria mappings control the visibility of new service definitions. To hide a service definition, map it to the **No User** user criteria. To make it visible, map it to the **Users with sn\_bom.service\_definition\_read** user criteria. Both user criteria records are predefined in Financial Services Operations Core.

    For more information, see [Components installed with case types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/service-definitions-components.md).


## Activation information

Install Financial Services Operations Core by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Case type selector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-case-type-select-modals.md)**

    Filter service definitions using the FSO case type selector with the CSM implementation, which supports agent criteria and customer conditions for filtering the service definitions displayed when creating a case.


**Parent Topic:**[Financial Services Operations release notes](financial-services-operations-rn-landing.md)

