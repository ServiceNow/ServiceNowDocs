---
title: Configure
description: Configure Dynamic Guidance to be available in the Help Center and Now Assist panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/adoption-services/configure.html
release: australia
product: Adoption Services
classification: adoption-services
topic_type: task
last_updated: "2026-03-20"
reading_time_minutes: 1
breadcrumb: [Dynamic Guidance, Adoption services, Configure user experiences]
---

# Configure

Configure Dynamic Guidance to be available in the Help Center and Now Assist panel.

## Before you begin

Role required: sn\_dyn\_guidance\_admin and sn\_nowassist\_admin.nsa\_admin

**Note:**

-   By default, Dynamic Guidance as a skill is active for applicable users but not accessible. The admin \(with role sn\_dyn\_guidance\_admin\) must assign sn\_dyn\_guidance\_user role to users who can access Dynamic Guidance.
-   When sn\_dyn\_guidance\_user role is assigned, it also includes the genai\_admin role.

**Note:** The genai\_admin role does not grant administrative privileges.


.

Follow these steps to enable Dynamic Guidance on Help Center and Now Assist panel:

## Procedure

1.  Log in to the relevant instance.

2.  Navigate to **ServiceNow Otto Admin**.

3.  Select **Platform** &gt; **Knowledge** under ServiceNow Otto Skills.

4.  Search for **Dynamic guidance** and select **Activate skills**.

    -   Dynamic Guidance gets enabled on Help Center.
    -   External Content Connectors\(XCC\) ServiceNow Docs plugin is automatically installed as a dependency. This verifies that the XCC infrastructure for documentation search is available.

## What to do next

-   Configure external content connectors to integrate with Dynamic Guidance. See [External content connector in Dynamic Guidance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/adoption-services/external-content-connector-in-dynamic-guidance.md).
-   Link Dynamic Guidance to additional documentation sources. See [Adding custom sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/adoption-services/adding-custom-sources.md).

