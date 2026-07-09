---
title: Product Capability Core release notes
description: Version history for the Product Capability Core application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-telecom-product-capability-core.html
release: store
topic_type: reference
last_updated: "2026-07-09"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - Technology Provider Service Management release notes, ServiceNow Store release notes]
---

# Product Capability Core release notes

Version history for the Product Capability Core application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.1.2 - July 2026 \(Zurich\)**
    -   Product Use Case — Two new tables ship in this release: Base Use Case \(the extensible foundation, with complexity, owner, process flow, and a Draft → Published → Retired lifecycle\) and Supported Use Case \(extends Base with industry and audience type\). Use Cases can be mapped to capabilities and product models via a Use Case Map, with the capability picker automatically filtered to only show capabilities active for the selected product model. State transitions — Publish, Return to Draft, Retire, Cancel — are available as UI actions in both the classic form and the workspace. Write and delete access is locked to Draft state, preventing mutations on published or retired records.Use Case Solution Map — The Use Case Solution Map relationship is surfaced as a related list on the Supported Use Case form, with a dedicated Delete action for removing individual map entries. A Business Rule guards the map to block inserts, updates, and deletes whenever the parent Use Case is not in Draft.
    -   Access control — Full ACL coverage added for all new tables \(Base Use Case, Supported Use Case, Use Case Map\) and expanded across existing tables \(Product Capability, Capability Relationship Map, Product Usage\), all scoped to the existing read/write/admin roles. Fields that must not be edited post-publish \(number, state, active\) are marked strict read-only, with N-2 compatibility ensured through the read\_only\_option plugin dependency.
    -   Fluent SDK migration — The repo is now built on the Fluent SDK framework, with all existing and new artifacts represented as typed TypeScript/JavaScript source. This aligns the project with the standard platform development toolchain for testing, linting, and CI.
-   **Version 2.2.2 - July 2026 \(Australia\)**
    -   Product Use Case — Two new tables ship in this release: Base Use Case \(the extensible foundation, with complexity, owner, process flow, and a Draft → Published → Retired lifecycle\) and Supported Use Case \(extends Base with industry and audience type\). Use Cases can be mapped to capabilities and product models via a Use Case Map, with the capability picker automatically filtered to only show capabilities active for the selected product model. State transitions — Publish, Return to Draft, Retire, Cancel — are available as UI actions in both the classic form and the workspace. Write and delete access is locked to Draft state, preventing mutations on published or retired records.Use Case Solution Map — The Use Case Solution Map relationship is surfaced as a related list on the Supported Use Case form, with a dedicated Delete action for removing individual map entries. A Business Rule guards the map to block inserts, updates, and deletes whenever the parent Use Case is not in Draft.
    -   Access control — Full ACL coverage added for all new tables \(Base Use Case, Supported Use Case, Use Case Map\) and expanded across existing tables \(Product Capability, Capability Relationship Map, Product Usage\), all scoped to the existing read/write/admin roles. Fields that must not be edited post-publish \(number, state, active\) are marked strict read-only, with N-2 compatibility ensured through the read\_only\_option plugin dependency.
    -   Fluent SDK migration — The repo is now built on the Fluent SDK framework, with all existing and new artifacts represented as typed TypeScript/JavaScript source. This aligns the project with the standard platform development toolchain for testing, linting, and CI.
-   **Version 2.0.2 - July 2026 \(Yokohama\)**
    -   This release introduces the Product Use Case data model — letting teams define, publish, and retire use cases across industries and audiences, and map them to product capabilities. The app is also migrated to the Fluent SDK framework.
    -   Product Use Case — Two new tables ship in this release: Base Use Case \(the extensible foundation, with complexity, owner, process flow, and a Draft → Published → Retired lifecycle\) and Supported Use Case \(extends Base with industry and audience type\). Use Cases can be mapped to capabilities and product models via a Use Case Map, with the capability picker automatically filtered to only show capabilities active for the selected product model. State transitions — Publish, Return to Draft, Retire, Cancel — are available as UI actions in both the classic form and the workspace. Write and delete access is locked to Draft state, preventing mutations on published or retired records.Use Case Solution Map — The Use Case Solution Map relationship is surfaced as a related list on the Supported Use Case form, with a dedicated Delete action for removing individual map entries. A Business Rule guards the map to block inserts, updates, and deletes whenever the parent Use Case is not in Draft.
    -   Access control — Full ACL coverage added for all new tables \(Base Use Case, Supported Use Case, Use Case Map\) and expanded across existing tables \(Product Capability, Capability Relationship Map, Product Usage\), all scoped to the existing read/write/admin roles. Fields that must not be edited post-publish \(number, state, active\) are marked strict read-only, with N-2 compatibility ensured through the read\_only\_option plugin dependency.
    -   Fluent SDK migration — The repo is now built on the Fluent SDK framework, with all existing and new artifacts represented as typed TypeScript/JavaScript source. This aligns the project with the standard platform development toolchain for testing, linting, and CI.
-   **Version 1.7.6 - June 2026 \(Australia\)**
    -   No new features are being released in this version. This release focuses on platform compliance, security hardening, and quality improvements to keep the application current with the latest platform standards.
        -   Platform compliance — Updates to meet platform-wide security directives including default-deny agentic AI ACLs, cross-scope access enforcement, and CSRF protection on public APIs.
        -   Security &amp; ACL hardening — Embedded query ACLs directly into product source code, eliminating the need for customers to re-run audits after install or upgrade.
        -   Platform readiness — Java 21 compile support and related framework upgrades to stay current with the underlying platform.
        -   Accessibility — WCAG 2.2 AA + 400% zoom/reflow support — Now meets the accessibility bar for this release.
-   **Version 1.7.4 - June 2026 \(Zurich\)**
    -   -   No new features are being released in this version. This release focuses on platform compliance, security hardening, and quality improvements to keep the application current with the latest platform standards.

    Platform compliance — Updates to meet platform-wide security directives including default-deny agentic AI ACLs, cross-scope access enforcement, and CSRF protection on public APIs.

-   Security &amp; ACL hardening — Embedded query ACLs directly into product source code, eliminating the need for customers to re-run audits after install or upgrade.
-   Platform readiness — Java 21 compile support and related framework upgrades to stay current with the underlying platform.
-   Accessibility — WCAG 2.2 AA + 400% zoom/reflow support — Now meets the accessibility bar for this release.
-   **Version 1.7.2 - June 2026 \(Yokohama\)**
    -   No new features are being released in this version. This release focuses on platform compliance, security hardening, and quality improvements to keep the application current with the latest platform standards.
        -   Platform compliance — Updates to meet platform-wide security directives including default-deny agentic AI ACLs, cross-scope access enforcement, and CSRF protection on public APIs.
        -   Security &amp; ACL hardening — Embedded query ACLs directly into product source code, eliminating the need for customers to re-run audits after install or upgrade.
        -   Platform readiness — Java 21 compile support and related framework upgrades to stay current with the underlying platform.
        -   Accessibility — WCAG 2.2 AA + 400% zoom/reflow support — Now meets the accessibility bar for this release.
-   **Version 1.6.6 - March 2026 \(Australia\)**

    This release does not include any updates for this application.

-   **Version 1.6.4 - March 2026 \(Zurich\)**

    This release does not include any updates for this application.

-   **Version 1.6.2 - March 2026 \(Yokohama\)**

    This release does not include any updates for this application.

-   **Version 1.2.7 - September 2025 \(Zurich\)**

    Make this a license free plugin

-   **Version 1.2.6 - September 2025 \(Yokohama\)**

    Make this plugin license free

-   **Version 1.2.0 - August 2025**
    -   Product Capability Core introduces Product Capabilities tied to Product Models inside the ServiceNow platform.
    -   This helps organizations to clearly define functions or outcomes a product is designed to deliver. By representing what a product can do, it enables the organization to articulate value for users or customers and is typically used to guide development, measure adoption, and align with business outcomes.
    -   Use Case 1: Fine-Grained Capabilities within a Product​
        -   Description: Enables direct association of detailed capabilities with a specific product, while also allowing secondary capabilities to be linked under a primary capability associated with that product.​
    -   Use Case 2: Capabilities Spanning Multiple
        -   Products​ Description: Supports capabilities that are shared across multiple products, along with secondary​ capabilities that can belong to various primary capabilities, demonstrating the m:n relationship.​

**Parent Topic:**[ServiceNow Store - Technology Provider Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-tech-highlights.md)

