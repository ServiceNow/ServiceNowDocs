---
title: Impact Content release notes
description: Version history for the Impact Content application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-impact-content.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - Impact release notes, ServiceNow Store release notes]
---

# Impact Content release notes

Version history for the Impact Content application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 8.0.5 - June 2026**
    -   What's New Starting June 11th:
        -   Conversations You can now reach your Impact Squad without leaving your instance. Conversations sync in real time between the Store App and the Impact Delivery Instance, so nothing gets lost across channels. Start a conversation, get a response, and pick up right where you left off — your full conversation history carries over automatically. You can message about your account in general or tie conversations directly to specific outcomes, accelerators, or initiatives you're working on.
        -   On-Demand Accelerators Platform Owners no longer need to wait for a Squad member to get started on strategic accelerators. Work through them independently at your own pace, with step-by-step guidance, embedded videos, and live progress tracking built in. Available to Guided+ \(Strategic Value add-on\), Advanced, and Impact Total customers with no concurrency limits. Launching with two accelerators: Staff and Roles Review and AI Governance Maturity Assessment.
        -   Real-Time Prevention Messaging Redesign When the scan engine catches a problem in your code, developers now see a cleaner, easier-to-read breakdown of what needs attention. Issues are organized by severity — Act, Recommend, and Suggest — in a persistent side panel with improved contrast and reduced scrolling. Exception requests appear right next to the relevant finding, and developers get a clear confirmation once something is resolved.
        -   Platform Optimization Add-on A new paid add-on offering that gives all paid Impact customers access to a dedicated catalog of optimization accelerators, backed by hands-on expertise. Impact Total customers on the latest version receive entitlement to the Optimization catalog as part of their existing package.
        -   Parallel Bulk Remediation Processing The Remediation Agent now handles multiple batches at the same time using an event-driven queue, so a large or slow batch no longer holds up everything else. A built-in safeguard automatically clears out any batch that gets stuck for more than six hours, keeping things moving without manual intervention.
        -   Analytics Dashboard You can now click any segment of the donut chart to drill into the findings behind it. The heatmap has been updated to meet accessibility standards, making results easier to read for everyone. Dashboard data now refreshes in near real-time, with status updates so you always know where things stand.
        -   Scan Engine Backend Each flagged finding in an update set now requires its own exception reason, so nothing gets glossed over. A new tooltip on the Level of Finding field explains what Act, Recommend, Suggest, and Review each mean — right in context, without needing to look it up.
        -   7 New Technical Accelerators Seven new accelerators are now available across all Impact packages: AI Data Explorer, AI Control Tower \(AI Lifecycle\), Now Assist in Virtual Agent, ServiceNow Vault, Enterprise Architecture Workspace, Software Asset Management, and ITSM Foundation.
-   **Version 7.1.0 - April 2026**
    1.  Stability fixes
    2.  Localisation fixes
-   **Version 7.0.2 - March 2026**
    -   The Impact Store App: Q1 2026 Australia Release: The Impact Store App brings the full Impact experience directly to your ServiceNow instance—helping you adopt new capabilities faster, maintain a healthy platform, and maximize the value of your ServiceNow investment.
    -   What's New Starting March 12th: Once installed on your instance, you will have access to these powerful new features and enhancements:
        -   Guided Setup Enhancements Onboarding is now simpler and more reliable with updates to accommodate the latest Service Bridge changes, ensuring a streamlined setup experience from day one
        -   Service Bridge Authentication Upgrade Authentication and registration now support Service Bridge version 2.3 with a certificate-based model, eliminating the OAuth-related errors that previously disrupted connectivity between your Impact Delivery Instance and the Impact Store App
        -   Impact Partner Role Customers can now grant selected users from their Partner accounts direct access to the Impact Store App, enabling your partners to seamlessly support and manage Impact on your behalf
        -   On-Demand Diagnostic Scans A new UI action lets you run Full or Delta scans on demand with built-in duplicate prevention, giving you clear visibility and control over when and how your platform health is assessed
        -   Capability Map Homepage Refresh The Capabilities Map is reorganized by product lines and now displays only true applications, making it easier to discover and act on the capabilities you're entitled
-   **Version 6.1.0 - February 2026**
    1.  Stability fixes
    2.  Reporting &amp; Dashboard Enhancements fixes
    3.  Accelerators &amp; Catalog Fixes
    4.  Used the new overload with GlideRecordSecure.addEncodedQuery\(query, boolean\) to explicitly declare intent to enforce Query ACL \(or not\).
    5.  Integrations &amp; UI Updates
-   **Version 6.0.2 - December 2025**
    -   The Impact Store App brings the Impact experience directly to your instances. Impact Store App is designed to support you at every step of your ServiceNow journey—helping you adopt new capabilities faster, maintain a healthy system, and get the most value from their ServiceNow investment.
    -   What's Available Starting December 11th: Once installed on your instance, you will have access to these powerful features:
        -   Platform Health Refresh – A new Scan Engine with Bravium’s Best Practice Engine features integrated enabling you to: Scan your instance against 400+ best practice checks to reduce technical debt, real-time prevention of technical debt, accelerate development with Code Fix AI Agent, and track progress through persona based analytics dashboards.
        -   Enhanced Guided Setup – Platform Health refresh setup steps integrated directly into Guided Setup for a smoother configuration experience.
        -   Learning Recommendations – Get personalized Now Learning course recommendations based on your specific goals and outcomes.
        -   Consumption Report Summary – AI-generated summaries of your consumption reports to help you understand your usage at a glance.
        -   Enhanced Homepage – An improved interface for easier navigation and better user experience.
        -   PAR Management – Editors can now force check in a locked PAR even if it was locked by another user, giving editors more control when needed.
        -   Capability Content for CapMap – AI generated descriptions and helpful resources for each capability will help you with their adoption.
        -   Capability SKU names – Transparent SKU to capability mapping helps you understand which applications you are entitled to.
-   **Version 5.0.3 - August 2025 \(Zurich\)**
    -   New:
        -   Automated registration to seamlessly onboard customers
        -   Introduced Value Reports
        -   Refactoring recommendations to reduce noise
        -   Consumption report for feature parity with IDI
        -   Improvements to Homepage
        -   Adoption functionality for IIP parity with IDI
        -   Impact SPM integration improvements
-   **Version 5.0.2 - August 2025 \(Xanadu and Yokohama\)**
    -   New:
        -   Automated registration to seamlessly onboard customers
        -   Introduced Value Reports
        -   Refactoring recommendations to reduce noise
        -   Consumption report for feature parity with IDI
        -   Improvements to Homepage
        -   Adoption functionality for IIP parity with IDI
        -   Impact SPM integration improvements
-   **Version 4.1.1 - June 2025**

    Minor bug fixes.

-   **Version 4.0.3 - May 2025**
    -   New:
        -   A new page for customers to provide secure, read-only access for squads and experts into their instances to deliver faster, more informed support
        -   Introduced capability details in one full page view
        -   Contextual Accelerators on capability details - helping customers plan smarter and act faster, all in one unified experience
        -   Extended Product Adoption Roadmap Templates for SecOps
        -   Value related terminology updates made to align pre-sales and post sales terminology
        -   Enhanced the experience by allowing customers to easily bookmark accelerators on their catalog
        -   Created a full page for customers to view the details of the accelerator which is linkable and easy to share
    -   Changed: Introduced a new link 'View Squad access to your instance' in the 'Your Impact Squad' widget on the Homepage
-   **Version 3.1.2 - April 2025**

    Minor bug fixes.

-   **Version 3.1.1 - March 2025**
    -   New:
        -   Impact Homepage on customer instance
        -   Introduced new page to view all recommendations
        -   Introduced proactive code check scan and analytics
        -   Updated the existing Data Collection Content Packs to deliver a superior user experience
        -   Opened Product Adoption Roadmap Functionality to our Impact Guided customers
        -   Introduced Product Adoption Roadmap Templates with pre-defined sequence of capabilities for ITSM and ITOM
        -   Introduced content app versioning that allows customers to request the latest version of the Accelerator after upgrading the content app
        -   Enabled customers to seamlessly convert Impact recommendations and free-form initiatives into actionable, trackable SPM/CWM work items.
-   **Version 3.1.1 - March 2025**

    ServiceNow Impact is a customer success product powered by AI and human expertise that helps customers maximize the power of the AI Platform for business transformation. Impact provides customers with the support and expertise they need to get to value fast. This content app contains the Accelerator catalog and will be updated when new Accelerators are released. Global resource table and Learn about impact content would be part of Content app. This app is required for the Main Impact Store Application.


