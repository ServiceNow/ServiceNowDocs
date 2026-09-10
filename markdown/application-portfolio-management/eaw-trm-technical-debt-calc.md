---
title: Technical debt calculation
description: Technical debt records identify products used in business applications that are not approved in the TRM or that use unapproved versions. View technical debt records to understand conformance gaps and plan remediation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-trm-technical-debt-calc.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exploring the Technology Reference Model in Enterprise Architecture Workspace, Exploring Technology Portfolio view, Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Technical debt calculation

Technical debt records identify products used in business applications that are not approved in the TRM or that use unapproved versions. View technical debt records to understand conformance gaps and plan remediation.

## Prerequisites

To view technical debt records, you need the Technology Lifecycle Management \(sn\_apm\_tpm\) Store application and the SAM Foundation \(com.snc.sams\) plugin.

## Configurable conditions

You can select which conditions the scheduled job uses to create technical debt records. At least one condition must remain selected. For configuration steps, see [Configure technical debt settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-configure-tech-debt.md).

## Technical debt levels

The system creates technical debt records at two levels when specific conditions are met. Level 2 checks occur only when the **sn\_apm\_trm.is\_product\_life\_cycle\_tech\_debt\_enabled** property is set to `true`.

**Level 1 conditions**

The system creates a Level 1 technical debt record when either of the following conditions is true:

-   A product is associated with a business application but is not part of the TRM product list.
-   A product is associated with a business application and is part of the TRM product list, but the Production phase is not approved.

**Level 2 conditions**

The system creates a Level 2 technical debt record when either of the following conditions is true:

-   A product is associated with a business application, is part of the TRM product list, has an approved Production phase, but has no associated TRM product lifecycles.
-   A product meets the criteria in the following cases.

**Case 1: Full version is not empty**

When the full version field in the Software Discovery Model \[cmdb\_sam\_sw\_discovery\_model\] table is not empty, the system creates a technical debt record. This occurs if no TRM product lifecycle meets all of the following criteria:

-   The TRM phase is approved for production.
-   The TRM product phase is approved for production.
-   The version matches the full version or wildcard pattern in the Software Discovery Model \[cmdb\_sam\_sw\_discovery\_model\] table.
-   The current date falls between the phase start date and phase end date.

**Case 2: Full version is empty**

When the full version field in the Software Discovery Model \[cmdb\_sam\_sw\_discovery\_model\] table is empty, the system creates a technical debt record. This occurs if no TRM product lifecycle meets all of the following criteria:

-   The TRM phase is approved for production.
-   The TRM product phase is approved for production.
-   The version matches \(exact or wildcard\) the version in the Software Discovery Model \[cmdb\_sam\_sw\_discovery\_model\] table.
-   The edition matches the edition in the Software Discovery Model \[cmdb\_sam\_sw\_discovery\_model\] table.
-   The current date falls between the phase start date and phase end date.

## Edition-specific technical debt

A Level 2 technical debt record can be created from a TRM product lifecycle that is defined by both version and edition. The technical debt record captures the edition along with the version. The edition is part of the record identity. A debt for version X, edition A is a separate record from a debt for version X, edition B.

**Parent Topic:**[Exploring the Technology Reference Model in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-managing-the-technology-portfolio.md)

**Related topics**  


[Technical debt settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-setup-tech-debt.md)

[TRM technical debt states and transitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-trm-technical-debt-states.md)

[Governing TRM product fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-trm-governing-fields.md)

