---
title: Creating FSO Case Types
description: If you need a new case type that can't be extended from an existing application, you can create one by extending the FSO Base Case \(sn\_bom\_case\) table.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using case types and service definitions in FSO, Developer resources, Financial Services Operations \(FSO\)]
---

# Creating FSO Case Types

If you need a new case type that can't be extended from an existing application, you can create one by extending the FSO Base Case \(sn\_bom\_case\) table.

Creating a case type involves creating roles, modules, workspaces, and other required entities. For additional information on case types, see Customer Service Case Types.

Here’s a list of questions that you may consider when evaluating whether you must create a case type in FSO. This isn’t an exhaustive list, and you should conduct further analysis based on your individual requirements and use cases.

-   Should you use a service definition instead of a new case type?
-   Does an application exist that you can use for your use case?
-   Which base FSO case type should you extend when creating the case type?
-   Does the service request have different processes across departments, business units, or products?
-   Do the new processes differ from the existing process’s state model?
-   Is there a noticeable attribute difference between different services that must be captured?
-   Does each business unit or team interact with a different set of backend systems to resolve the case?
-   Do the access requirements differ considerably from the existing use case?
-   Must a particular process be improved in the long run using process optimization?
-   Are there future scalability requirements?
-   Change management considerations – if multiple teams are involved, does sharing intake forms and workflows increase the complexity of the change management process?

## Example scenario

When implementing, for example, ACH payment disputes, you may want to create a new case type as it may impact one or more of the following:

-   The process and tasks required to resolve an ACH dispute may be different from card disputes
-   The attributes needed to capture the ACH disputes
-   Different teams processing disputes that have differing access and training requirements

**Parent Topic:**[Using case types and service definitions in FSO](fso-int_guide-work_case_types.md)

