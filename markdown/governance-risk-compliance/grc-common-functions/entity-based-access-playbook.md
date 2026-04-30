---
title: Entity based record access update utility
description: The entity based record access update utility is a guided assistance, designed to simplify the application of enabling or disabling access restrictions across large volumes of records.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Entity Based Access, Common GRC features, Governance, Risk, and Compliance]
---

# Entity based record access update utility

The entity based record access update utility is a guided assistance, designed to simplify the application of enabling or disabling access restrictions across large volumes of records.

The guided assistance provides a user-friendly, step-by-step interface that enables authorized users to configure and execute bulk updates in a consistent and auditable manner. It supports dynamic scoping, conditional filtering, and real-time feedback, promoting a controlled and transparent update process. This utility helps scale access management efforts efficiently. It improves overall operational efficiency and strengthens governance.

The bulk record access update process follows a four-step process, designed for clarity and control:

1.  Scope entities – In this step, you select the entities, entity classes, or entity types whose associated records are impacted by the utility. Entities can include individuals, departments, processes, systems, or applications. This step helps ensure that the update is focused on the selected entities' related records.
2.  Scope related record types – You define the selected entities' related records. Record types can include risks, controls, or any other scoped tables that support entity-based access. This granular scoping helps prevent unintended updates and help apply entity-based access restrictions in a phased manner. You can define conditions optionally to narrow the scope further. The entity scoped in the previous step acts as a primary filter, and you can add more filters.
3.  Preview record counts \(optional\) – Before execution, you’re presented with a summary preview of your selections. This step includes the selected record types and their secondary information with impacted record counts. The system prompts you to review and confirm the potential impact based on scope. You can set access using the enable or disable access restrictions buttons.
4.  View results – See the result of the entity-based record access update with a count of the records updated.

After confirmation, the system executes the update job in a controlled and asynchronous manner. You can see the results after the job execution is completed. You can see the log data specific to the configuration record.

The update states the system supports are as follows:

-   Update queued – The update is actively being processed.
-   Completed – The update is successfully applied to all selected records.
-   Failed – The update couldn’t be executed due to configuration issues or system errors. You can see a **Retry** button in this state so that you can trigger the update again.

The following image shows the entity-based record access update utility screen:

![Guided-experience for entity-based record access update utility.](../image/entity-based-record-access-update-utility.png "Entity based record access update utility guided assistance")

**Parent Topic:**[Entity Based Access](entity-based-access.md)

