---
title: Impact release notes
description: ServiceNow Impact is built on the ServiceNow AI Platform and combines customized service with a digital interface to provide tailored recommendations and guidance. Impact Store App was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
---

# Impact release notes

ServiceNow® Impact is built on the ServiceNow AI Platform and combines customized service with a digital interface to provide tailored recommendations and guidance. Impact Store App was enhanced and updated in the Australia release.

## Impact highlights for the Australia release

-   Version 8.0.0
    -   Identify problematic lines and receive proposed solutions by engaging an AI analysis panel with the [Fix code in real-time with Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/code-fix-ai-agent-scan-engine.md) feature.
    -   Submit exception requests directly from Recommend-level findings in [Now Assist for Platform Health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/impact-health-agent.md).
    -   Get a high-level estimate of your Impact app storage usage so you can proactively plan your storage management.
    -   Discover, filter, launch, and complete accelerators independently and also download a self-served 90-day action plan with On-demand accelerators.
    -   Manage Impact accounts with the dedicated partner role support where partners can manage Impact on behalf of customers without manual intervention.
-   Version 7.0.0:
    -   Streamline the Impact Store Application configuration with the updated Impact guided setup.
    -   Proactively identify, prioritize, and resolve technical debt with the Impact Health Agent, a collection of AI-native tools embedded within the Impact Platform Health experience.
    -   Provide access to partners with the impact\_partner\_role.
    -   View true applications capabilities organized by product lines.

See [Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/impact-landing-page.md) for more information.

**Important:** Impact is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Impact to Australia

The Impact Store Application configuration requires a sequence of tasks in a unified registration process. See [Configure the Impact Store Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configuring-impact-platform.md).

## New in the Australia release

-   **[Now Assist for Platform Health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/impact-health-agent.md)**

    Version 8.0.0

    -   Access summarized findings in one line grouped by findings level. Use the statistical and sys property scan types to view scan results in a statistical section.
    -   Create exceptions directly from Recommend-level findings and view approved exceptions which are required for every Recommend-level finding. Previously, the logic confirmed only that at least one approved exception existed, leaving a gap when multiple findings were present.
    Version 7.0.0

    -   Proactively identify, prioritize, and resolve technical debt by using the collection of AI-native tools embedded within the Impact Platform Health experience.
    -   Track and resolve issues in developer code throughout the end-to-end workflow by reviewing and applying AI-recommended fixes through the [Now Assist for Platform Health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/impact-health-agent.md), which provides AI-generated code fixes for leading practice violations.
-   **[New Accelerators in the Australia Release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/new-accelerators-australia-release.md)**

    Version 8.0.0

    -   Explore AI data, learn AI governance, and improve Virtual Agent performance.
    -   Configure ServiceNow Vault, optimize HR and service management, and build skills for the EA Workspace.
    -   Evaluate and improve the performance of your platform teams and assess their AI governance with On-demand accelerators.
    -   Sustain ServiceNow platform adoption and business value using OCM accelerators that offer structured coaching in alignment with the OCM Readiness framework.
    -   Enhance platform capabilities and drive product adoption through focused engagements including Capability Design and Capability Configuration with Optimization Accelerators.
    Version 7.0.0

    -   Accelerate your Impact Platform health, Data privacy, Walk-up experience, Digital product release, Modern change management, Major incident management, CSDM for service operations, and Integration hub by using technical accelerators.
    -   Improve your change readiness by using the OCM: Preparing for change and adopt AI governance impact strategy accelerators.
    -   Assess your CSDM maturity, improve CSDM Data modeling, and accelerate your portal’s user experience with the help of usage insights and virtual agent experience design provided by the architecture accelerators.
-   **[On-demand accelerators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/on-demand-accelerators.md)**
    -   Provide Self-service capabilities with improved session persistence, an entitlement-aware catalog, and a downloadable 90-day action plan.
    -   Access engagement-type filtering, progress tracking, questionnaire persistence, and self-serve directly within the catalog.
-   **[Impact Conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/impact-conversations_store.md)**

    Collaborate with your Impact squad through organized, category-based conversations where you can ask questions, get expert guidance, and share files without leaving yourServiceNow instance.

-   **[Alert card to capture long pending jobs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/io-long-pending-job-alert-card.md)**

    Get timely notifications of pending jobs based on their lateness duration and act on them to reduce the risk of downstream failures and SLA misses. The Long Pending Jobs alert card identifies jobs that breach predefined lateness thresholds.

-   **[Configure IO alert notifications for a ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/io-receive-notification-customer-conf-webhook.md)**

    Receive timely notifications on failures in customer-configured webhook integrations caused by invalid URLs or credentials that go unnoticed until runtime.

    -   All URLs are now validated before integrations.
    -   Daily system notifications are indicated by a bell icon and through email notifications.
    -   Alert Console alerts provide real-time visibility.
-   **[Roles installed with Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/impact-roles.md)**

    Grant selected users with partner accounts access to the Impact Store Application through the new **Impact Partner** role. Users assigned with the partner role can efficiently manage Impact for their customers. You can view the users added as partners on the Impact homepage.

-   **[Manage Capabilities Maps for the Impact Store Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/manage-capability-maps.md)**

    Version 7.0.0: The Capabilities Map homepage now shows true application capabilities organized by product line.


## UI changes

-   **[Optimization Accelerators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/optimization-accelerators.md)**

    Optimization accelerators catalog displays across dashboards, catalog filter and navigation, accelerator creation flows, and accelerator detail views inline with the other accelerator catalogs

    Flash cards now reflect the Optimization accelerator catalog category, and dashboards include platform optimization usage and consumption metrics.

-   **[Track Platform Health trends](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/scan-engine-diagnostic-dashboards.md)**

    Open the Real-time Messaging panel directly alongside the development workspace; a slide-in side panel that stays visible until dismissed. Findings are organized into tabs by severity level, each showing a total count, and ordered by impact to the instance.

    Hover over the Level of Finding field in the findings table and definition records now displays a tooltip explaining Act, Recommend, Suggest, and Review.

    Select and open a filtered back-end list view for donut chart segments.

-   **[Fix code in real-time with Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/code-fix-ai-agent-scan-engine.md)**

    Dashboard data refresh timing and status jobs trigger at the enhanced time frame and frequency for near real-time data. The dashboard also displays status messaging about job progress and any delays.


-   **[Capabilities maps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/capabilities-map.md)**

    Recommended capabilities has been renamed Squad-prioritized capabilities.


## Changed in this release

-   **[Run Impact Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/guided-setup-impact-in-app.md)**

    The Impact Guided Setup provides a more efficient, streamlined way for you to configure the Impact Store Application. For information about how to upgrade, see [Configure the Impact Store Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configuring-impact-platform.md).


## Removed in this release

On-demand value report and Value potential accelerators have been removed.

## Activation information

-   **[Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/impact-landing-page.md)**

    For information on package entitlement and features activation, see .

    For details on configuring Impact and its features, see [Configuring Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configuring-impact.md).


## Plugin information

-   **Plugins planned for deprecation**

    The following plugins are planned for deprecation in a future release.

    Impact Health \(com.sn\_impact\_health\): Planned for deprecation in a future release. For this functionality, install the [Now Assist for Platform Health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/impact-health-agent.md) Scan Engine application.


## Related ServiceNow applications and features

-   **[Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/admin-center-intro.md) [Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/ham-landing-page.md)**

    Admin Center provides a central hub for platform owners and admins to access platform capabilities, discover new applications, and get intelligent, actionable insights.

-   **[Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/r_ITBusinessManagement.md)**

    Strategic Portfolio Management \(SPM\) enables digital transformation by helping you plan, deliver, and track value across different methodologies.

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Now Assist uses generative AI to enhance productivity and efficiency through conversation and proactive experiences.


**Parent Topic:**[Features and changes by product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/new-features-changes.md)

