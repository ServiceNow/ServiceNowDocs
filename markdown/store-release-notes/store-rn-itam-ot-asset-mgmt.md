---
title: OT Asset Management release notes
description: Version history for the OT Asset Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itam-ot-asset-mgmt.html
release: store
topic_type: reference
last_updated: "2025-12-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - IT Asset Management release notes, ServiceNow Store release notes]
---

# OT Asset Management release notes

Version history for the OT Asset Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.2.0 - December 2025**
    -   Fixed:
        -   Demo data has been removed.
        -   Files were transferred from the OTAM App to the EAM App to enable firmware support in additional workflows if required.
-   **Version 2.1.2 - September 2025**

    Fixed: The issue is with displaying the Firmware installations and Knowledge-related lists on the Firmware model form.

-   **Version 2.1.1 - June 2025**
    -   Fixed:
        -   The missing opt-in capability for Custom Firmware CPE mapping feature in the Enterprise Asset Management Content Service to improve the firmware normalization process.
        -   Added an Exclude from Content Service toggle on the Custom Firmware CPE mapping form, allowing you to prevent selected transactions from being shared with the Content Service.
-   **Version 2.1.0 - February 2025**
    -   New:
        -   Firmware Model Discovery: Capture and track the installed firmware model and version during discovery.
        -   Firmware Install Management: Track firmware installations on OT and hardware assets.
        -   Firmware Normalization: Normalize discovered firmware models against a content library curated by ServiceNow and map to CPE vulnerability published data.
        -   Hardware Asset Integration: Manage hardware class assets that are part of the OT network throughout their lifecycle using the same workspace and workflows used to manage OT and OE assets. Workflows include Request, Refresh, Stock Order, Single and Multi-asset Onboarding, Repair, RMA, Maintenance Plan, and Disposal.
        -   MAC Addresses: MAC addresses are tracked on asset records during asset receiving and onboarding. They are also synced with configuration items \(CIs\) and related network adapters.
-   **Version 1.1.0 - August 2024**
    -   -   New:
    -   Added new roles
        -   sn\_otam.ot\_asset\_manager
            -   Full access to OT Asset Workspace, Mobile Agent App, all EAM features including all EAM workflows and tasks, and creating models and assets limited to the respective classes.
        -   sn\_otam.ot\_asset\_technician
            -   Limited access to OT Asset Workspace and Mobile Agent App. Ability to work on select EAM workflows and tasks limited to the respective model and asset classes
    -   Subscription Units Based licensing based on resource categories.
-   **Version 1.0.0 - May 2024**

    Operational Technology \(OT\) Asset Management is a specialized offering within our suite of Enterprise Asset Management \(EAM\) solutions, tailored specifically for the management of Operational Technology \(OT\) and Operational Equipment \(OE\) assets. With OT Asset Management, users can expect a comprehensive approach to managing the end-to-end lifecycle of their OT and OE assets.


