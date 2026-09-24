---
title: Validating product offerings before publishing
description: Extended life cycle states add validation stages before publication, so you can assemble and review catalog hierarchies without publishing unfinished records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/extended-product-lifecycle-states.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [Specifications and product offerings, Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Validating product offerings before publishing

Extended life cycle states add validation stages before publication, so you can assemble and review catalog hierarchies without publishing unfinished records.

Enable the optional In Test and Staged states to validate product offerings and product, service, or resource specifications before publication. These states provide clear checkpoints between authoring and release.

By default, records move directly from Draft to Published. With extended states enabled, records move through Draft, In Test, Staged, and Published.

## Building product hierarchies with unpublished components

Without a validation stage, an offering under review can't be added as a child of another offering until it is published. This limitation can force admins to publish individual components before a bundle is complete.

Extended states let a product offering include child offerings that are in Draft, In Test, Staged, or Published. You can assemble and refine a bundle from work-in-progress components without publishing each component first.

The following table provides more information about these states.

|States|Purpose|Editing behavior|
|------|-------|----------------|
|Draft|Author and update the record.|The record and its child lists are editable.|
|In Test|Validate the record before release.|The record and its child lists are read-only. Return the record to Draft to make changes.|
|Staged|Prepare the validated record for publication.|The record and its child lists are read-only. A rejected approval anywhere in the hierarchy blocks the move to Staged.|
|Published|Make the record available according to its configured dates and visibility.|Published visibility applies unless prepublication visibility is enabled.|
|Retired|Remove the record from active use.|Staged records can be Retired directly without publishing it. A retired record can't be reverted to any active state.|

Product offerings in the In Test and Staged states can also be referenced in the price lists, cost books, price adjustments, and context variables.

## Referencing records in compatible life cycle states

Product offerings and specifications can be organized into hierarchies in which a parent record references one or more child records. For example, a bundle offering can reference child product offerings, and a product offering can reference an underlying product specification.

The life cycle state of the parent determines which child records it can reference. These rules help prevent a parent record from advancing toward publication while its dependencies are still incomplete or haven’t reached an appropriate state.

For example, before an offering can move from In Test to Staged, each referenced child must already be Staged or Published. If a child is still Draft or In Test, the parent can’t move to Staged. Move the child to a compatible state, and then retry the transition.

The state of a record determines the states of the records that it can reference.

|Parent record state|Allowed states for referenced records|
|-------------------|-------------------------------------|
|Draft|Draft, In Test, Staged, or Published|
|In Test|In Test, Staged, or Published|
|Staged|Staged or Published|
|Published|Published|

## Enabling extended life cycle states

Product offerings and specifications use two related system properties as listed in the following table. Both properties are off by default, so the existing Draft-to-Published behavior remains unchanged until a product catalog admin enables the properties.

|System property|What it controls|Default|
|---------------|----------------|-------|
|sn\_prd\_pm.enable\_extended\_product\_lifecycle|Adds the In Test and Staged states between Draft and Published.|false|
|sn\_prd\_pm.enable\_product\_lifecycle\_prepublish\_visibility|Makes In Test and Staged records visible to catalog consumers. Takes effect only when extended life cycle states are enabled.|false|

For more information, see [Enable extended life cycle states for product offerings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/enable-extended-lifecycle-states.md).

Keep extended product life cycle statuses turned off if your organization wants to continue using the existing Draft-to-Published process. Enabling the feature is optional and doesn’t change existing catalog behavior until a product catalog admin turns it on.

## Controlling prepublication availability

Enable prepublication visibility in an instance where the catalog teams need to test pre-release catalog records. When extended life cycle statuses and prepublication visibility are enabled, In Test and Staged records can appear in catalog listings and reference fields. They can also be used to validate quote, order, pricing, configuration, and portal flows before the records are published.

**Note:** If the **sn\_prd\_pm.enable\_product\_lifecycle\_prepublish\_visibility** property is turned off, only published offerings appear to catalog consumers. This property has no effect unless extended life cycle states are also enabled. The **sn\_prd\_pm.enable\_product\_lifecycle\_prepublish\_visibility** is turned off in production environments by default.

## Example: Build a bundle from work-in-progress offerings

A product catalog admin is building a bundle from several child offerings that aren’t ready for publication. In a test or preproduction instance, the admin moves the child offerings to In Test and adds them to the bundle without publishing them. The implementation team can then validate the bundle structure and use the pre-release offerings in supported quote and order transaction flows.

If testing identifies an issue, the admin moves the affected offering back to Draft, makes the required changes, and returns the offering to In Test for further validation. After the bundle and its child offerings pass validation, the admin moves each eligible record to Staged and then to Published.

This process enables the team to validate the complete bundle before release, without publishing unfinished offerings or creating unnecessary revisions.

## Moving records through the extended life cycle

1.  In the Draft state, create and update a record and its child lists.
2.  Move the record to In Test when it is ready for validation. The record and its child lists become read-only.
3.  Return the record to Draft if you need to make changes.
4.  Resolve rejected approvals anywhere in the hierarchy before moving the record to Staged.
5.  Move the validated record from Staged to Published when it is ready for release.
6.  Retire a record when it's no longer in active use.

For more information, see [36e0738cf8938e71ff603b1a07014fedcf33c1e8.dita](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/move-offering-spec-states.md).

-   **[Enable extended life cycle states for product offerings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/enable-extended-lifecycle-states.md)**  
Turn on the In Test and Staged life cycle states for product offerings and product, service, and resource specifications, and optionally preview pre-publish records before they're published.
-   **[Validate product offerings and specifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/move-offering-spec-states.md)**  
Move a product offering or specification through the In Test and Staged statuses to validate it before you publish it.

**Parent Topic:**[Setting up specifications and product offerings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/order-mgt-product-catalog.md)

**Related topics**  


[Product Catalog Management properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/product-catalog-management-properties.md)

[creating-publishing-new-versions-product-offerings]

