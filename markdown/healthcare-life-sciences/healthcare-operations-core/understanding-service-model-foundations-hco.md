---
title: Understanding Service Model Foundation in Healthcare Operations
description: Understand how the Service Model Foundation \(SMF\) tables relate to each other so that you configure cases, locations, and bulk imports correctly for Healthcare Operations Core.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/healthcare-operations-core/understanding-service-model-foundations-hco.html
release: australia
product: Healthcare Operations Core
classification: healthcare-operations-core
topic_type: concept
last_updated: "2026-07-24"
reading_time_minutes: 6
breadcrumb: [Organizations and locations overview, Configure, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Understanding Service Model Foundation in Healthcare Operations

Understand how the Service Model Foundation \(SMF\) tables relate to each other so that you configure cases, locations, and bulk imports correctly for Healthcare Operations Core.

## The Service Model Foundation data model

Healthcare Operations Core is built on the Service Model Foundation \(SMF\) framework, the same platform framework used across industries such as banking, retail, and manufacturing. For the platform-wide overview of these tables, see [Service Model Foundation overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-industry-data-model.md).

The SMF location tables form an extension hierarchy. From parent to child:

-   **Organization Core** \[sn\_customer\_service\_organization\] is the base table in the hierarchy.
-   **Business Organization** \[sn\_csm\_business\_location\] is an extension of Organization Core.
-   **Internal Organization** \[sn\_csm\_business\_location\_internal\] and **External Organization** \[sn\_csm\_business\_location\_external\] are both extensions of Business Organization.

\[Omitted image "smf-data-model.png"\] Alt text: ERD diagram showing the Service Model Foundation data model, from the case table through Organization Core, Business Organization, Internal Organization, External Organization, healthcare organization, and common location.

For the complete field-level reference for these tables, see [Service Model Foundation tables and plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-data-model-tables.md).

**Note:**

These tables were previously labeled **Service Organization**, **Business Location**, **Internal Business Location**, and **External Business Location**. Only the display name changed—the table names \(`sn_customer_service_organization`, `sn_csm_business_location`, `sn_csm_business_location_internal`, `sn_csm_business_location_external`\) and the Business Location plugin itself are unchanged. If you see the older names in existing configuration steps, integrations, or an instance that hasn't picked up the rename yet, they refer to the same tables. For the complete list of renamed entities and field labels, see [Service Model Foundation renamed Entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/renamed-entities.md).

Two additional tables relate to this hierarchy by reference rather than by extension:

-   The **common location** \[cmn\_location\] table is referenced from Organization Core through a location reference field. It stores the physical address of a record.
-   The **healthcare organization** \[sn\_hcls\_organization\] table has a one-to-one, bidirectional relationship with Business Organization.

**Important:**

The primary record for a location is Internal Organization or External Organization—not the healthcare organization.

Because the documentation and configuration steps focus heavily on the healthcare organization table, it's commonly mistaken for the primary record. In reality, Internal Organization and External Organization are the tables that are considered the requesting organization or location—not the healthcare organization.

The healthcare organization is like a profile: a one-to-one repository of healthcare-specific fields and information about its linked Internal or External Organization record. It's against best practice to add healthcare-specific information directly to the Business Organization tables. That information belongs on the healthcare organization record. For more information, see [Setting up healthcare locations and healthcare organizations]().

## Internal Organization and External Organization

Whether a location is internal or external depends on its relationship to the organization that owns the ServiceNow instance.

-   **Internal Organization** records are internal to your organization. For example, the hospital that owns the ServiceNow instance, the units within that hospital, or the individual floors and rooms within the hospital.
-   **External Organization** records are external to your organization, such as those for private practices or healthcare affiliates that consume your healthcare services. For example, an affiliate might log into your organization's Epic environment through Epic Community Connect. To report EMR issues requires an External Organization record in ServiceNow, along with the corresponding membership setup.

## Service organization fields on cases

The Healthcare Operations case \[sn\_hco\_case\] form has two service organization fields. Configure them correctly to preserve out-of-box case visibility. For the platform-wide pattern this is based on, including the shared-visibility model and how CSM and ITSM divide the work, see [CSM and ITSM integration models for Service Model Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-and-itsm-integration-models-for-smf.md).

-   **Requesting service org**

    Represents the organization that needs support \(the requester\). This out-of-box field is used in every SMF implementation and drives shared case visibility. If the requesting service org isn't populated on the case, none of the shared visibility works.

-   **Supporting service org**

    Represents the organization that's fulfilling the case \(the fulfiller\). This field isn't used in every implementation.


**Note:**

A common configuration error is displaying the healthcare organization on the case form. Display the Internal or External Organization record through the out-of-box requesting service org field instead. Because the healthcare organization is only a profile, showing it on the case doesn't establish the visibility that the requesting service org field provides.

## Common locations and Business Organization

The common location \[cmn\_location\] table represents the physical address of a record and is used across the ServiceNow platform. Because several tables contain *location* in their name, it's commonly assumed that one table extends another, but they don't. Organization Core holds a reference field to the common location record.

For healthcare use cases, configure the healthcare location \[sn\_hcls\_location\] table rather than customizing the common location table directly. The healthcare location is a profile for an individual location—a repository of fields and information that aren't available on the common location table. For more information, see [Setting up healthcare locations and healthcare organizations]().

## Importing location data

When you bulk import location data, a business rule on Organization Core creates a new common location record whenever address fields are added and the common location reference field is empty. If multiple units at the same hospital share a single physical address and you import address details on each Business Organization record, this business rule creates duplicate common location records—one for every Internal or External Organization record that you import.

To avoid duplicates, look up and reuse existing common location records instead of letting the business rule create new ones. Reusing existing records also matters for customers migrating from ServiceNow IT Service Management, who likely already have common location records—and incidents related to them—that should be reused.

Use the following process to import location data:

1.  Load or confirm the addresses in the common location \[cmn\_location\] table. If the customer already has address records, such as from an existing ITSM deployment, no action is needed in this step. Otherwise, import the addresses into the common location table first.
2.  Create a single import set and transform map at the healthcare organization \[sn\_hcls\_organization\] table. Include a custom choice column in the import spreadsheet that indicates whether each row is internal or external.
3.  Use an onBefore transform script to create the correct Internal Organization or External Organization record. Based on the internal or external value, the script creates the linked Internal Organization or External Organization record. This approach produces one import set that creates records across the appropriate tables, so the customer manages only a single import set.
4.  In the same script, look up an existing common location record for the address and reference it from the Internal Organization or External Organization record, copying the address data up to the Business Organization record. Only when no matching common location record exists should you add the address details and allow a new common location record to be created.

**Tip:**

Don't add address fields directly to an Internal Organization or External Organization record when a matching common location record already exists if you haven't populated the common location yet. Doing so triggers the business rule that creates duplicate common location records.

For a worked example that applies this data model to a hospital system, see .

