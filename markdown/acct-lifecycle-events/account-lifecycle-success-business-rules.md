---
title: Customer success management business rules
description: This section includes the Customer Success Management business rules.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 13
breadcrumb: [Reference, Customer Success Management]
---

# Customer success management business rules

This section includes the Customer Success Management business rules.

<table id="table_lnn_4vg_dcc"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Domain - Set Domain

</td><td>

Engagement

</td><td>

Sets the domain information.

</td></tr><tr><td>

Required fields for engagement

</td><td>

Engagement

</td><td>

Validates required fields.

</td></tr><tr><td>

State is closed or canceled

</td><td>

Engagement

</td><td>

Ensures that closure information is populated and object is marked inactive before marking it as closed or canceled.

</td></tr><tr><td>

Engagement is reopened

</td><td>

Engagement

</td><td>

Ensures that closure information is removed and object is marked active before reopening.

</td></tr><tr><td>

Validate account change for engagement

</td><td>

Engagement

</td><td>

Prevent account change if the engagement has objectives, customer plays, internal plays, or risk signals associated with it.

</td></tr><tr><td>

Validate engagement parent

</td><td>

Engagement

</td><td>

Prevent cyclic relationship for the parents in engagement hierarchy.

</td></tr><tr><td>

Validate onboarding for engagement

</td><td>

Engagement

</td><td>

Ensures that the engagement account matches the account of its onboarding case and sets the go live date based on the go live date of its onboarding case.

</td></tr><tr><td>

Domain - Set Domain

</td><td>

Success objective

</td><td>

Sets the domain information.

</td></tr><tr><td>

Required fields for objective

</td><td>

Success objective

</td><td>

Validates required fields

</td></tr><tr><td>

Validate closure for objective

</td><td>

Success objective

</td><td>

Ensures that closure information is populated and object is marked inactive before marking closed/canceled.

</td></tr><tr><td>

Success objective is reopened

</td><td>

Success objective

</td><td>

Ensures that closure information is removed and object is marked active before reopening.

</td></tr><tr><td>

Validate engagement change for objective

</td><td>

Success objective

</td><td>

Prevents engagement change if the objective has outcomes or risk signals associated with it.

</td></tr><tr><td>

Validate planned start and stop

</td><td>

Success objective

</td><td>

Ensures planned stop date isn’t before planned start date.

</td></tr><tr><td>

Domain - Set Domain

</td><td>

Success outcome

</td><td>

Sets the domain information.

</td></tr><tr><td>

Required fields for outcome

</td><td>

Success outcome

</td><td>

Validates required fields.

</td></tr><tr><td>

Validate closure for outcome

</td><td>

Success outcome

</td><td>

Ensures that closure information is populated and object is marked inactive before marking it as closed or canceled.

</td></tr><tr><td>

Success outcome is reopened

</td><td>

Success outcome

</td><td>

Ensures that closure information is removed and object is marked active before reopening.

</td></tr><tr><td>

Validate objective change for outcome

</td><td>

Success outcome

</td><td>

Prevents objective change if the outcome has initiatives or risk signals associated with it.

</td></tr><tr><td>

Validate planned dates

</td><td>

Success outcome

</td><td>

Ensures planned stop date isn’t before planned start date.

</td></tr><tr><td>

Validate tracking method

</td><td>

Success outcome

</td><td>

Validates tracking method to see if the correct reference field for tracking is populated.

</td></tr><tr><td>

Required fields for initiative

</td><td>

Success initiative

</td><td>

Validates required fields.

</td></tr><tr><td>

Validate closure for initiative

</td><td>

Success initiative

</td><td>

Ensures that closure information is populated and object is marked inactive before marking it as closed or canceled.

</td></tr><tr><td>

Success initiative is reopened

</td><td>

Success initiative

</td><td>

Ensures that closure information is removed and object is marked active before reopening.

</td></tr><tr><td>

Validate outcome change for initiative

</td><td>

Success initiative

</td><td>

Prevents outcome change if the initiative has success tasks or risk signals associated with it.

</td></tr><tr><td>

After close or cancel SI

</td><td>

Success initiative

</td><td>

Cancels process automation playbooks associated with initiative if closed or canceled.

</td></tr><tr><td>

Required fields for customer play

</td><td>

Customer play

</td><td>

Validates required fields.

</td></tr><tr><td>

Validate closure for customer play

</td><td>

Customer play

</td><td>

Ensures that closure information is populated and object is marked inactive before marking it as closed or canceled.

</td></tr><tr><td>

Customer play is reopened

</td><td>

Customer play

</td><td>

Ensures that closure information is removed and object is marked active before reopening.

</td></tr><tr><td>

Validate engagement update

</td><td>

Customer play

</td><td>

This prevents the engagement field from changing on the 'Customer Play' record if the 'Customer Play' has success tasks associated with it.

</td></tr><tr><td>

Required fields for touchpoint

</td><td>

Touchpoint

</td><td>

Validates required fields.

</td></tr><tr><td>

Validate closure for touchpoint

</td><td>

Touchpoint

</td><td>

Ensures that closure information is populated and object is marked inactive before marking it as closed or canceled.

</td></tr><tr><td>

Touchpoint is reopened

</td><td>

Touchpoint

</td><td>

Ensures that closure information is removed and object is marked active before reopening.

</td></tr><tr><td>

Validate engagement update

</td><td>

Touchpoint

</td><td>

Prevents engagement change if the touchpoint has success tasks or risk signals associated with it.

</td></tr><tr><td>

Required fields for success task

</td><td>

Success task

</td><td>

Validates required fields.

</td></tr><tr><td>

Validate closure for success task

</td><td>

Success task

</td><td>

Ensures that closure information is populated and object is marked inactive before marking it as closed or canceled.

</td></tr><tr><td>

Success task is reopened

</td><td>

Success task

</td><td>

Ensures that closure information is removed and object is marked active before reopening

</td></tr><tr><td>

Validate parent change for success task

</td><td>

Success task

</td><td>

Prevents parent change if the success task has risk signals associated with it.

</td></tr><tr><td>

Required fields for internal play

</td><td>

Internal play

</td><td>

Validates required fields.

</td></tr><tr><td>

Internal play is closed or canceled

</td><td>

Internal play

</td><td>

Ensures that closure information is populated and object is marked inactive before marking it as closed or canceled.

</td></tr><tr><td>

Reopen internal play

</td><td>

Internal play

</td><td>

Ensures that closure information is removed and object is marked active before reopening.

</td></tr><tr><td>

Parent for internal play must be empty

</td><td>

Internal play

</td><td>

Ensures that parent is empty for all internal plays.

</td></tr><tr><td>

Validate engagement change

</td><td>

Internal play

</td><td>

Prevents engagement change if the internal play has internal play tasks or risk signals associated with it.

</td></tr><tr><td>

Required fields for internal play task

</td><td>

Internal play task

</td><td>

Validates required fields.

</td></tr><tr><td>

Internal play task is closed or canceled

</td><td>

Internal play task

</td><td>

Ensures that closure information is populated and object is marked inactive before marking it as closed or canceled.

</td></tr><tr><td>

Reopen internal play task

</td><td>

Internal play task

</td><td>

Ensures that closure information is removed and object is marked active before reopening.

</td></tr><tr><td>

Validate internal play change

</td><td>

Internal play task

</td><td>

Prevents internal play change if the internal play task has risk signals associated with it.

</td></tr><tr><td>

Domain - Set Domain

</td><td>

Risk signal and issue

</td><td>

Sets the domain information.

</td></tr><tr><td>

Field validation

</td><td>

Risk signal and issue

</td><td>

Validates required fields.

</td></tr><tr><td>

Validate risk signal closure

</td><td>

Risk signal and issue

</td><td>

Ensures that closure information is populated and object is marked inactive before marking it as closed or canceled.

</td></tr><tr><td>

Reopen risk signal

</td><td>

Risk signal and issue

</td><td>

Ensures that closure information is removed and object is marked active before reopening

</td></tr><tr><td>

Avoid duplicate definition record

</td><td>

Definition record

</td><td>

Ensures that no two records share the same title and category.

</td></tr><tr><td>

Domain - Set Domain

</td><td>

Definition record

</td><td>

Sets the domain information.

</td></tr><tr><td>

Set active flag

</td><td>

Definition record

</td><td>

Sets status to active if published, or else inactive.

</td></tr><tr><td>

Avoid duplicate risk signal solution

</td><td>

Risk signal solution relationship

</td><td>

Ensures the no two records share the same solution record.

</td></tr><tr><td>

Avoid duplicate squad member

</td><td>

Squad member

</td><td>

Ensures the no two records share the same user and responsibility

</td></tr><tr><td>

Domain - Set Domain

</td><td>

Squad member

</td><td>

Sets the domain information.

</td></tr><tr><td>

Avoid duplicate engagement to contract relationship

</td><td>

Engagement to contract relationship

</td><td>

Ensures the no two records share the same engagement and contract.

</td></tr><tr><td>

Validate contract account

</td><td>

Engagement to contract relationship

</td><td>

Ensures contract account matches the engagement account.

</td></tr><tr><td>

Contract relationship updated

</td><td>

Engagement to contract relationship

</td><td>

Ensures renewal date for engagement is updated to the date of the earliest non expired contract.

</td></tr><tr><td>

Contract relationship removed

</td><td>

Engagement to contract relationship

</td><td>

Ensures that renewal date for engagement is updated to the date of the earliest non expired contract.

</td></tr><tr><td>

Validate context on publish

</td><td>

Data Source

</td><td>

When publishing a data source, it must have at least one valid context record, which should have at least one context mapper record associated.

</td></tr><tr><td>

Avoid duplicate data source

</td><td>

Data Source

</td><td>

Data source shouldn’t have duplicate source and configurations.

</td></tr><tr><td>

Autopopulate unit of measurement

</td><td>

Data Source

</td><td>

Automatically populated unit of measurement for data source.

</td></tr><tr><td>

Last run/Next run validation

</td><td>

Data Source

</td><td>

Data source last run date shouldn’t come after next run date.

</td></tr><tr><td>

Unique source to context

</td><td>

Context Engine Mapper

</td><td>

Ensure there’s a unique source to context.

</td></tr><tr><td>

Process externally sourced context data

</td><td>

Context Engine Data

</td><td>

When creating a data record for external source, update associated data source date last run field and populate data record's context field.

</td></tr><tr><td>

Validate externally sourced context data

</td><td>

Context Engine Data

</td><td>

Context engine date records with external source should have all required fields.

</td></tr><tr><td>

Unique context according to source

</td><td>

Context

</td><td>

Context record's mappers should be unique.

</td></tr><tr><td>

Abort if duplicate record found

</td><td>

Engagement Risk Definition

</td><td>

Aborts if similar record exists

</td></tr><tr><td>

Abort if invalid template

</td><td>

Engagement Risk Definition

</td><td>

Aborts if risk template set for the risk definition is invalid

</td></tr><tr><td>

Abort if duplicate record found

</td><td>

Risk Threshold Override

</td><td>

Aborts if similar record exists

</td></tr><tr><td>

Abort if no context mapper for risk def

</td><td>

Engagement Risk Definition

</td><td>

Aborts if risk definition is table type and no active mapper exists with the table selected in risk definition as the source and engagement as context

</td></tr><tr><td>

Abort if color or range validation fails

</td><td>

Color Banding

</td><td>

Aborts if duplicate color exists for a record of the same type or max value is lesser than min value or if the given min-max range already overlaps with another existing record of the same type.

</td></tr><tr><td>

Abort if global min-max range is invalid

</td><td>

Color Banding

</td><td>

Aborts if global band has min less than 0 and max greater than 100

</td></tr><tr><td>

Limit \# of global health definition to 1

</td><td>

Engagement Health Definition

</td><td>

Ensures there is at most 1 global health definition in system

</td></tr><tr><td>

Unique engagement health definition

</td><td>

Engagement Health Definition

</td><td>

Ensures that each health definition is unique

</td></tr><tr><td>

Validate sum of health def config weight

</td><td>

Engagement Health Definition

</td><td>

Checks all health definition metric configuration for health definition sums to 100

</td></tr><tr><td>

Abort creation for published health def

</td><td>

Health Metric Configuration

</td><td>

User shouldn’t be able to create health metric configuration for published health definition

</td></tr><tr><td>

Check unique health metric configuration

</td><td>

Health Metric Configuration

</td><td>

Metric configuration for a health definition shouldn’t be duplicate by data source

</td></tr><tr><td>

Update last touchpoint

</td><td>

Touchpoint

</td><td>

Update last\_touchpoint field in engagement table

</td></tr><tr><td>

Update last touchpoint for Delete

</td><td>

Touchpoint

</td><td>

Update last\_touchpoint field in engagement table

</td></tr><tr><td>

Avoid duplicate entitlements

</td><td>

Applicable Entitlement

</td><td>

Aborts if similar record exists

</td></tr><tr><td>

Avoid duplicate sold product

</td><td>

Applicable Sold Product

</td><td>

Aborts if similar record exists

</td></tr><tr><td>

Avoid duplicate customer team

</td><td>

Applicable Customer Team

</td><td>

Aborts if similar record exists

</td></tr><tr><td>

Avoid duplicate account team

</td><td>

Applicable Account Team

</td><td>

Aborts if similar record exists

</td></tr><tr><td>

Create Activity

</td><td>

Create activity for Applicable Account Team \[sn\_acct\_lc\_eng\_m2m\_team\_mem\]

</td><td>

Create record in activity table on insert update delete

</td></tr><tr><td>

Create Activity

</td><td>

Create activity for label \[sn\_meeting\_mgmt\_meeting\_details\]

</td><td>

Create record in activity table on update

</td></tr><tr><td>

Create Activity

</td><td>

Create activity for Risk Signal and Issue \[sn\_acct\_lc\_risk\_signal\_issue\]

</td><td>

Create record in activity table on insert update

</td></tr><tr><td>

Create Activity

</td><td>

Create activity for Escalation \[sn\_customerservice\_escalation\]

</td><td>

Create record in activity table on insert update

</td></tr><tr><td>

Create Activity

</td><td>

Create activity for Success Initiative \[sn\_acct\_lc\_success\_initiative\]

</td><td>

Create record in activity table on update

</td></tr><tr><td>

Create Activity

</td><td>

Create activity for Success Task \[sn\_acct\_lc\_success\_task\]

</td><td>

Create record in activity table on update

</td></tr><tr><td>

Create Activity

</td><td>

Create activity for Touchpoint \[sn\_acct\_lc\_touchpoint\]

</td><td>

Create record in activity table on insert update

</td></tr><tr><td>

Create Activity

</td><td>

Create activity for Applicable Customer Team \[sn\_acct\_lc\_eng\_m2m\_cntct\_rel\]

</td><td>

Create record in activity table on insert update delete

</td></tr><tr><td>

Create Activity for contract

</td><td>

Create activity for Contract \[ast\_contract\]

</td><td>

Create record in activity table on update

</td></tr><tr><td>

Create Activity for Engagement

</td><td>

Create activity for Engagement \[sn\_acct\_lc\_engagement\]

</td><td>

Create record in activity table on update

</td></tr><tr><td>

Create Activity for Success Outcome

</td><td>

Create activity for Success Outcome \[sn\_acct\_lc\_success\_outcome\]

</td><td>

Create record in activity table on update

</td></tr><tr><td>

Sync Progress To State

</td><td>

Sync Progress To State for Implementation Record \[sn\_acct\_lc\_implementation\_record\]

</td><td>

Create or update record in the implementation record table with state or progress fields changing.

</td></tr><tr><td>

Duplicate name in product capability

</td><td>

Product Capability \[sn\_prod\_cap\_core\_prod\_cap\]

</td><td>

Duplicate name check-in Product capability

</td></tr><tr><td>

Prevent Duplicate Product Capability Map

</td><td>

Product Capability Map \[sn\_prod\_cap\_core\_prod\_cap\_map\]

</td><td>

Duplicate check in Product capability map table

</td></tr><tr><td>

Product capability usage validations

</td><td>

Product Capability Usage \[sn\_prod\_cap\_core\_prod\_cap\_usage\]

</td><td>

Validations for capability usage table

</td></tr><tr><td>

Product usage validations

</td><td>

Product Usage \[sn\_prod\_cap\_core\_prod\_usage\]

</td><td>

Validations for product usage table

</td></tr><tr><td>

Set Prod Capability Map Active

</td><td>

Product Capability Map \[sn\_prod\_cap\_core\_prod\_cap\_map\]

</td><td>

Set on state change to mark active = true if state is published, else false.

</td></tr><tr><td>

Set calc metric value in target table

</td><td>

Context Engine Data \[sn\_data\_ctx\_engine\_data\]

</td><td>

Whenever an entry is added or updated in the Context Engine Data table for a calculated data source, and if that data source has a target table and target field defined, the corresponding rows in the target table - where the target query field matches the context record - will have the data context engine value set in the target field.

</td></tr><tr><td>

Abort adding future data

</td><td>

Context Engine Data \[sn\_data\_ctx\_engine\_data\]

</td><td>

Aborts if the record added to Data Context Engine has a start or end date after current time

</td></tr><tr><td>

Validate circular reference

</td><td>

Segment \[sn\_data\_ctx\_engine\_brkdwn\_seg\]

</td><td>

Aborts the publish operation and reverts the segment to draft if it introduces a circular reference: That is, if the segment configuration includes a data source that already depends on the current data source associated with the segment. This circular reference check is necessary to ensure that all data sources maintain a valid execution order.

</td></tr><tr><td>

Validate context on publish

</td><td>

Data Source \[sn\_data\_ctx\_engine\_src\]

</td><td>

Validates all contexts are active and have active mappers on publish. In case of calculated metrics, validate if at least 1 active context exists with same table as breakdown table.

</td></tr><tr><td>

Unique source to context

</td><td>

Context Engine Mapper \[sn\_data\_ctx\_engine\_map\]

</td><td>

For global mappers: Ensure only one mapper exists for each combination of a given source and resolving context table.

 For metric-based mappers: Ensure that the same metric or data source does not appear in multiple mappers for the same source and resolving context table pair.

</td></tr><tr><td>

Validate breakdown segments on publish

</td><td>

Data Source \[sn\_data\_ctx\_engine\_src\]

</td><td>

On publishing calculated data source, ensure that at least one segment is present and all segments are published

</td></tr><tr><td>

Validate sum of seg config weight

</td><td>

Segment \[sn\_data\_ctx\_engine\_brkdwn\_seg\]

</td><td>

On publishing segment, ensure that weight of all segment configurations add to 100

</td></tr><tr><td>

Avoid duplicate breakdown segment

</td><td>

Segment \[sn\_data\_ctx\_engine\_brkdwn\_seg\]

</td><td>

Ensure duplicate segment for the same data source isn’t present for the same name, rank, or conditions

</td></tr><tr><td>

Abort if visualization validation fails

</td><td>

DCE Visualization \[sn\_data\_ctx\_engine\_visualization\]

</td><td>

Abort if another visualization record exists with the same data source, resolving context and conditions

</td></tr><tr><td>

Unique context according to source

</td><td>

Context \[sn\_data\_ctx\_engine\_ctx\]

</td><td>

Abort if another context with the same table exists for the given data source

</td></tr><tr><td>

Unique set of metrics according to breakdown seg

</td><td>

Segment Configuration \[sn\_data\_ctx\_engine\_seg\_conf\]

</td><td>

Abort if another segment configuration exists for the given segment with the same data source

</td></tr><tr><td>

Abort ctx creation for non draft src

</td><td>

Context \[sn\_data\_ctx\_engine\_ctx\]

</td><td>

Enable creating context for data source in draft state only

</td></tr><tr><td>

Abort seg conf creation if non draft seg

</td><td>

Segment Configuration \[sn\_data\_ctx\_engine\_seg\_conf\]

</td><td>

Enable creating segment configuration for segment in draft state only

</td></tr><tr><td>

Abort creating seg for non draft source

</td><td>

Segment \[sn\_data\_ctx\_engine\_brkdwn\_seg\]

</td><td>

Enable creating segment for data source in draft state only

</td></tr><tr><td>

Move data source to draft

</td><td>

Segment \[sn\_data\_ctx\_engine\_brkdwn\_seg\]

</td><td>

As soon as a segment is moved to draft, if its data source isn’t draft, move it to draft as well

</td></tr><tr><td>

Abort if invalid Visualization M2M

</td><td>

DCE Visualization M2M \[sn\_data\_ctx\_engine\_visualization\_m2m\]

</td><td>

Validates given visualization\_m2m item record

</td></tr><tr><td>

Abort if insight item validation fails

</td><td>

DCE Insight Item \[sn\_data\_ctx\_engine\_insight\_item\]

</td><td>

Validates given insight item record

</td></tr><tr><td>

Abort if insight validation fails

</td><td>

DCE Insight \[sn\_data\_ctx\_engine\_insight\]

</td><td>

Validates given insight record

</td></tr><tr><td>

Create Usage based on Appl Sold Prod

</td><td>

Applicable Sold Product \[sn\_acct\_lc\_eng\_m2m\_sp\]

</td><td>

Trigger:​

 A record is added or modified in the Applicable Sold Products table.​

 Actions:​ Create Product Usage Record. If a Product Usage record doesn’t exist for the sold product, create it.​Create Product Usage records for all child products \(across all hierarchy levels\).​For each usage record, update the Total Child Product Count \(reflecting only immediate children\).​

 Associate Capabilities:​For each usage record:​Check the Product Capability Map using the sold product's product model.​If capability records exist, create corresponding Capability Usage records.​Update the Total Capability Count.​ Don’t include related capabilities—only direct capabilities are considered.​

</td></tr><tr><td>

Add Capability usage for new Cap Map

</td><td>

Product Capability Map \[sn\_prod\_cap\_core\_prod\_cap\_map\]

</td><td>

Trigger:​

 A new active record is added to the Product Capability Map.​

 Actions:​ Identify all sold products with a matching product model.​For each matching product:​Create Capability Usage records, update the Total Capabilities in Use count on the corresponding Product Usage record

</td></tr><tr><td>

Update usage on setting adoption score

</td><td>

Product Usage \[sn\_prod\_cap\_core\_prod\_usage\]

</td><td>

Set Activation status of the given sold product and all its parent sold products in its hierarchy to 'In Use' and update Usage plan to 'Activated' if Usage plan isn’t set

</td></tr><tr><td>

Update usage on setting adoption score

</td><td>

Product Capability Usage \[sn\_prod\_cap\_core\_prod\_cap\_usage\]

</td><td>

Set Activation status of the given capability usage record, its sold product and all its parent sold products in its hierarchy to 'In Use' and update Usage plan to 'Activated' if Usage plan isn’t set

</td></tr><tr><td>

Update renewal finalized on

</td><td>

Update renewal finalized on field value on Contract table when Substate changes to Renewal Approved or Renewal Rejected. To capture the date when it is approved or rejected.

</td><td>

This helps to determine the won/loss of a contract and at what month of the year for Renewal Tab won/loss visualization graphical plot.

</td></tr></tbody>
</table>**Parent Topic:**[Customer Success Management reference](account-lifecycle-reference.md)

