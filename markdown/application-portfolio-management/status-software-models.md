---
title: Status of the Software models
description: An application owner can run the software model suggestions engine to fetch software models. These models can be related to an application service instead of mapping them manually. Every application service displays the status after they are mapped.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Enterprise Architecture \(formerly Application Portfolio Management\) reference, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Status of the Software models

An application owner can run the software model suggestions engine to fetch software models. These models can be related to an application service instead of mapping them manually. Every application service displays the status after they are mapped.

## Status of the Software models

|First run of the job|Second run of the job|Conditions of association|New status of the software model|
|--------------------|---------------------|-------------------------|--------------------------------|
|Found|Found|Yes|**Associated**: Associates the selected software model to the application service. The status is prefixed with a green bubble. In the subsequent run of the job, these software models are still in Associated state. You may choose to dissociate the software model if it has been removed or uninstalled from the hardware on which the application service runs.|
|Found|Found|No|**Ignored**: If no action is taken on the software models in the prior run of the job, then they are identified as **Ignored** \(prefixed with a gray bubble\) in the current run of the status.|
|Not found|Found|Not applicable|**New**: The software models that are identified in the first run of the job, and those software models that have been added after the last run but before the current run are marked with status **New** prefixed with a yellow bubble. You can associate or dissociate such software models.|
|Found|Not found|Yes|**Delete**: You can delete a software model that is in Associated, Ignored, or New status. This action deletes the software model from the list of the retrieved software models, which is Retrieved Software Models \[sn\_apm\_service\_software\_model\_suggestion\] table but not from the Application Service Software Model \[sn\_apm\_tpm\_service\_software\_model\] table.|
|Found|Not found|No|Delete|

**Parent Topic:**[Enterprise Architecture \(formerly Application Portfolio Management\) reference](apm-reference.md)

**Related topics**  


[Associate suggested technology models to an application service](../task/associate-application-service-software-models.md)

