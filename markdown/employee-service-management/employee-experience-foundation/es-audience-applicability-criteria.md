---
title: User criteria form and reference
description: Reference information for configuring audience applicability criteria used in multi-theme functionality and other platform features.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/es-audience-applicability-criteria.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2026-06-04"
reading_time_minutes: 1
keywords: [audience criteria, user criteria, applicability, targeting]
breadcrumb: [Configure multi-theme, Employee Slate for Now Assist, Configuration flow, Employee Slate, Unified Employee Experience, Employee Service Management]
---

# User criteria form and reference

Reference information for configuring audience applicability criteria used in multi-theme functionality and other platform features.

## User Criteria form fields

The User Criteria form contains fields for defining user access criteria and restrictions. For more information, see [Configure additional themes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/es-configure-multi-theme.md).

|Field|Description|
|-----|-----------|
|**Name**|Descriptive name for the user criteria record. This field is required.|
|**Application**|Application scope for the user criteria. Defaults to Global.|
|**Short Description**|Brief description of the user criteria purpose and scope.|
|**Active**|When selected, the user criteria record is active and enforced. When cleared, the criteria are inactive.|
|**Users**|Specific users included in the criteria. Select the reference icon to choose users or the list icon to view selected users.|
|**Companies**|Companies included in the criteria. Select the reference icon to choose companies.|
|**Groups**|User groups included in the criteria. Select the reference icon to choose groups.|
|**Locations**|Locations included in the criteria. Select the reference icon to choose locations.|
|**Roles**|User roles included in the criteria. Select the reference icon to choose roles.|
|**Departments**|Departments included in the criteria. Select the reference icon to choose departments.|
|**Advanced**|When selected, enables advanced criteria configuration options.|
|**Match All**|When selected, users must match all specified criteria. When cleared, users must match any of the specified criteria.|

## Criteria structure

Audience applicability criteria define which users receive specific themes, configurations, or features. The system uses a platform construct that wraps user criteria functionality to provide inclusion and exclusion capabilities.

|Criteria Type|Description|Use Cases|
|-------------|-----------|---------|
|User roles|Target users based on assigned roles and permissions|Admin-specific themes, role-based branding|
|Departments|Target users based on organizational department|Department-specific branding, divisional themes|
|Geographic location|Target users based on physical or regional location|Regional branding, location-specific themes|
|User groups|Target users based on group membership|Team-specific themes, project-based branding|
|Custom attributes|Target users based on custom user profile fields|Business unit themes, specialized configurations|
|Time zones|Target users based on time zone settings|Regional themes, time-based configurations|
|Domains|Target users based on domain separation|Multi-tenant environments, domain-specific branding|

