---
title: Script includes installed with Operational Resilience
description: When you download the Operational Resilience application, several Script includes are added to your instance.
locale: en-US
release: xanadu
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reference, Operational Resilience, Governance, Risk, and Compliance]
---

# Script includes installed with Operational Resilience

When you download the Operational Resilience application, several Script includes are added to your instance.

## Script includes and other references installed

<table id="table_v4x_dcz_z2c"><thead><tr><th>

Script Name

</th><th>

Description

</th><th>

Process step used

</th></tr></thead><tbody><tr><td>

Add to related area after insert

</td><td>

Script include

</td><td>

 

</td></tr><tr><td>

Build scratchpad values

</td><td>

Script include

</td><td>

 

</td></tr><tr><td>

Cancel vulnerability notification

</td><td>

Script include

</td><td>

 

</td></tr><tr><td>

Delete relevant records after deletion

</td><td>

Script include

</td><td>

 

</td></tr><tr><td>

Update relevant records after update

</td><td>

Script include

</td><td>

 

</td></tr><tr><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Show Opres tables only upon loading

</td><td>

Client script

</td><td>

Load options for the source field on operational vulnerability

</td></tr><tr><td>

Hide activity journal in workspace

</td><td>

Client script

</td><td>

Hide activity journal on operational vulnerability

</td></tr><tr><td>

Validate due date

</td><td>

Client script

</td><td>

Validate due date when submitting operational vulnerability

</td></tr><tr><td>

Disable attachments if inactive

</td><td>

Client script

</td><td>

Disable attachments if inactive when loading the operational vulnerability

</td></tr><tr><td>

Synch source to source table

</td><td>

Client script

</td><td>

Change the source table, when the source is changed on operational vulnerability

</td></tr><tr><td>

Hide or show related lists

</td><td>

Client script

</td><td>

Hide or show related lists in terms of the installation of the integrated apps.

</td></tr><tr><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Make type read-only for operational vulnerability

</td><td>

Catalog UI Policy

</td><td>

 

</td></tr><tr><td>

Validate date of occurrence

</td><td>

Catalog Client script

</td><td>

 

</td></tr><tr><td>

Show/Hide fields when source changes

</td><td>

Catalog Client script

</td><td>

 

</td></tr><tr><td>

Validate date of discovery

</td><td>

Catalog Client script

</td><td>

 

</td></tr><tr><td>

Show Opres tables only upon loading

</td><td>

Catalog Client script

</td><td>

 

</td></tr><tr><td>

Synch source to source table

</td><td>

Catalog Client script

</td><td>

 

</td></tr><tr><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

VulnerabilityUtils

 VulnerabilityUtilsBase

</td><td>

Script include

</td><td>

Used for the operational vulnerability.

</td></tr><tr><td>

OperationalResilienceEntitiesLists

 OperationalResilienceEntitiesListsBase

</td><td>

Script include

</td><td>

Used for the roll up of the red flags, CSDM, and dependencies.

</td></tr><tr><td>

OpResLogger

</td><td>

Script include

</td><td>

Used for logging.

</td></tr><tr><td>

OperationalResilienceComputation

OperationalResilienceComputationBase

​

</td><td>

Script include

</td><td>

Contains the utility functions that are being used to fetch the data from different places in Operational Resilience and also to fetch all the issues that are related to a business service's entity or configuration item \(CI\). Used for updating the CSDM, dependencies, and their red flags.

</td></tr><tr><td>

OperResBusinessServiceUtil

 OperResBusinessServiceUtilBase

</td><td>

Script include

</td><td>

Contains the utility functions for the related lists in the business service form.​ Utility classes used for service and business service.

</td></tr><tr><td>

OpResAssessmentUtils

 OpResAssessmentUtilsBase

</td><td>

Script include

</td><td>

Used for importance and impact duration assessment.

</td></tr><tr><td>

OpResRedFlags

 OpResRedFlagsBase

</td><td>

Script include

</td><td>

Used to calculate red flags.

</td></tr><tr><td>

OperResUtils

 OperResUtilsBase

</td><td>

Script include

</td><td>

Utility class used for Operational Resilience.

</td></tr><tr><td>

OperationalResilienceConstants

</td><td>

Script include

</td><td>

Contains the constants that are required in different places in the application.​ Used to define constants.

</td></tr><tr><td>

OperationalResilienceAjax​

</td><td>

Script include

</td><td>

Client callable script include that handles the interaction between the client side and the service side​. AJAX utilities for Operational Resilience.

</td></tr><tr><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

sn\_oper\_res.businessservice\_dependencies

</td><td>

Event

</td><td>

Event to trigger the updating of business service dependencies

</td></tr><tr><td>

sn\_oper\_res.businessprocess\_dependencies

</td><td>

Event

</td><td>

Event to trigger the updating of business process dependencies

</td></tr><tr><td>

sn\_oper\_res.serviceoffering\_dependencies

</td><td>

Event

</td><td>

Event to trigger the updating of service offering dependencies

</td></tr><tr><td>

sn\_oper\_res.compliance\_comp\_job\_err

</td><td>

Event

</td><td>

Event to trigger the logging.

</td></tr><tr><td>

sn\_oper\_res.set\_entity\_type\_pillar

</td><td>

Event

</td><td>

Event to trigger adding pillar to the entities.

</td></tr><tr><td>

sn\_oper\_res.set\_child\_service\_pillar

</td><td>

Event

</td><td>

Event to add pillar to the child service

</td></tr><tr><td>

sn\_oper\_res.remove\_child\_service\_pillar

</td><td>

Event

</td><td>

Event to remove pillar from the child service

</td></tr><tr><td>

sn\_oper\_res.set\_entity\_pillar

</td><td>

Event

</td><td>

Event to add pillar to single entity

</td></tr><tr><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Fetch business service dependencies

</td><td>

Event script action

</td><td>

Updating of business service dependencies

</td></tr><tr><td>

Fetch service offering dependencies

</td><td>

Event script action

</td><td>

Updating of service offering dependencies

</td></tr><tr><td>

Fetch business process dependencies

</td><td>

Event script action

</td><td>

Updating of business process dependencies

</td></tr><tr><td>

Compliance job error handler

</td><td>

Event script action

</td><td>

Logging an error if the scheduled job throws exception.

</td></tr><tr><td>

Set pillar for entities in entity type

</td><td>

Event script action

</td><td>

Adding the pillar of the entity type to its entities.

</td></tr><tr><td>

Set service pillar for child services

</td><td>

Event script action

</td><td>

Adding service pillar from the child services.

 \(Only used for the service\)

</td></tr><tr><td>

Remove service pillar for child services

</td><td>

Event script action

</td><td>

Removing service pillar from the child services.

 \(Only used for the service\)

</td></tr><tr><td>

Set pillar for entity

</td><td>

Event script action

</td><td>

Adding the pillar for single entity

</td></tr></tbody>
</table>