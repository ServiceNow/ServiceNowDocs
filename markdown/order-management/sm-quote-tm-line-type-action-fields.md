---
title: Line type and line action fields for subscriptions
description: Line type and line action fields are system-provided fields in Quote Experience that define the type of change and the action required for subscription amendments and renewals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sm-quote-tm-line-type-action-fields.html
release: brazil
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 4
breadcrumb: [Quote Experience configuration for subscriptions, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Line type and line action fields for subscriptions

Line type and line action fields are system-provided fields in Quote Experience that define the type of change and the action required for subscription amendments and renewals.

## Line type and line action

Line type and line action fields vary depending on the amendment or renewal use case. Subscription amendment and renewal workflows set the line type and line action fields, and the system populates the corresponding transaction fields in Quote Experience.

The line type field indicates the nature of the change being made to a quote line. The line action field indicates the operation being performed.

## Quantity changes

The following table summarizes the line type and line action field settings for quantity changes.

|Use case|Line type/Line action|Description|
|--------|---------------------|-----------|
|Upsell quantity: active line|
|Original line|No Change/No Change|No changes on the existing line. Additional quantity handled on the new split line.|
|Split line|Amend/Add|Creation of a new line to carry the additional quantity from the effective date forward.|
|Downsell quantity: active line|
|Original line|Cancel/Change|Active line closed off at the effective date \(end date set\). A split line carries the reduced quantity forward.|
|Split line|Amend/Add|New line segment to represent the modified \(lower\) quantity from the effective date.|
|Downsell quantity: future-dated line|
|Original line|Amend/Change|Amendment not a cancellation of the original line since the line had not yet started. Creation of a split line depends on whether the effective date equals the start date.|
|Split line \(if any\)|Amend/Add|Creation of a new line segment if the effective date is between the start date and the end date of the future-dated line.|
|Quantity to 0: early termination|
|Original line|Cancel/Change|Reduction of quantity to 0 equivalent to removing the product. End date set to the day before the effective date. No split line.|

## Product modifications

The following table summarizes the line type and line action field settings for adding, removing, and swapping products. It also includes product characteristic changes.

|Use case|Line type/Line action|Description|
|--------|---------------------|-----------|
|Product additions or removals|
|Add product: amendment quote|
|New line|Upsell/Add|Addition of a new product to an existing subscription. Quote type set to Amend/Renew and line type set to Upsell to distinguish from a new sale.|
|Remove product: active line|
|Original line|Cancel/Change|Ending of the product at the effective end date and the setting of the end date set accordingly. No split line due to no ongoing amendment version.|
|Remove product: future-dated line|
|Original line|Amend/Change|Setting of the line type to Amend and an update to the end date because the future line has not yet started. No split line needed.|
|Full product swap|
|Original product line|Cancel/Change|Termination of the original product at the effective date.|
|New product line|Amend/Add|Addition of a replacement product as a new amended line.|
|Partial product swap|
|Original: Original line|Cancel/Change|Reduction of the original product quantity to 0 and termination of the original product quantity for the swapped portion.|
|Original: Split line|Amend/Add|Split line for remaining quantity of the original product carried forward.|
|New product line|Amend/Add|Addition of a new product as part of the swap. Setting of the line type to Amend and not Upsell because of the downsell action.|
|Characteristic changes|
|Original line|Cancel/Change|Closing of the original line and creation of a line with the updated product characteristic whenever a product characteristic changes.|
|Split line|Amend/Add|Creation of a split line to carry the same product with the updated characteristic from the effective date.|

## Date changes

The following table summarizes the line type and line action field settings for date changes, including an early end date and an end date extension.

|Use case|Line type/Line action|Description|
|--------|---------------------|-----------|
|Early termination or early end date|
|Original line|Cancel/Change|Movement of the end date to an earlier date and cancellation of the line at the new end date. No split line needed.|
|End date extension|
|Original line|Amend/Change|Extension of the end date with the existing line amended. No termination or split line needed.|

## Renewals

The following table summarizes the line type and line action field settings for various renewal scenarios.

|Use case|Line type/Line action|Description|
|--------|---------------------|-----------|
|Quantity change|
|Renewed line|Renew/Add|Renewal of line as is.|
|Quantity set to 0 on line|Cancel/Disconnect|Removal of product from renewal when reducing the quantity to 0 or swapping the product. Cancellation of line.|
|Date change|
|Renewed line|Renew/Add|Renewal of line as is.|
|Characteristic change|
|Renewed line|Renew/Add|Renewal of line as is.|
|Product addition|
|New product line|New/Add|Addition of product to the renewal.|
|Product removal|
|Original product line|Cancel/Disconnect|Removal of the product from the renewal and the cancellation of the line at the renewal effective date.|
|Product swap|
|Original product line|Cancel/Disconnect|Cancellation of the original product as part of the swap.|
|New product line|New/Add|Addition of the replacement product as New, not Amend.|

## Quote and unmodified line changes

The following table summarizes the line type and line action field settings for new quotes and unmodified lines.

|Use case|Line type/Line action|Description|
|--------|---------------------|-----------|
|New quote|
|New product line|New/Add|Addition of a product from a catalog, resulting in a quote type of New and a line type of New.|
|No change|
|Unmodified line|No Change/No Change|No action required if there are no modifications to the line.|

