---
title: ITOM Infra Services Workspace release notes
description: Version history for the ServiceNow ITOM Infra Services Workspace application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-infra-services-ws.html
release: store
topic_type: reference
last_updated: "2026-07-09"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# ITOM Infra Services Workspace release notes

Version history for the ServiceNow® ITOM Infra Services Workspace application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 2.0.3 - July 2026**
    -   New MID Server Onboarding Experience: New onboarding page in the ITOM Infra Services Workspace provides guidance through initial MID Server setup. The previous downloads page can be accessed via "mid\_server\_download\_ui.do" if required.
    -   Command Line Installer for Windows and Linux \(for JWT Authentication\)
        -   The workspace now offers an automated command line installer that pre-configures your instance name, authentication, proxy, and other settings during installation.
        -   The service account that will run on the MID Server needs to be specified on the MID Server host during installation.
        -   Applications and capabilities must be assigned after the MID Server comes online and validates
    -   Private Key JWT Authentication
        -   Each MID Server gets authenticates with a unique certificate that automatically rotates every 45 days
        -   Migration from basic authentication to private key JWT can be done from the Auth-type migration tab on the MID Admin Workspace
        -   New MIDs can be setup to authenticate with JWTs through the above command line installer or manually via registration key in ITOM Infrastructure Services Workspace
        -   Currently available for standard cloud and on-prem instances. Regulated cloud and on-prem instances are not yet supported.
-   **Version 1.0.2 - June 2026**
    -   Updates to ACC Admin Workspace:
        -   Agent Diagnostics page - When ACC agents encounter issues in the field, administrators currently have limited visibility into agent health from the ServiceNow instance. This page allows customers to run diagnostic tests from the agent record in the ACC Admin Workspace and gather suggestions for remediation.
        -   Agent Onboarding page - Deploying new ACC agents can be challenging due to the number of available configuration options.  This page guides customers through proper ACC agent deployment.
-   **Version 1.0.0 - December 2025**

    The ServiceNow ITOM infrastructure Services Workspace provides platform owners and IT Operations teams with a single, unified interface to manage and monitor MID Servers, Agent Client Collectors, and related components. It streamlines troubleshooting, assists with configuration, and grants visibility into these deployments. This workspace helps admins reduce downtime and lower operational overhead, so that critical services like Discovery, Integration Hub, Service Mapping, and Orchestration stay up and running. Enhanced with Now Assist for ITOM \(MID Guardian skill\) to provide advanced AI-driven troubleshooting and remediation.


**Parent Topic:**[ServiceNow Store - IT Operations Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itom.md)

