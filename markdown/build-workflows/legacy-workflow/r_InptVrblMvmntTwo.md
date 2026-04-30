---
title: Input variable movement use case - two input variables
description: An existing workflow already contains two input variables.You can verify the variables that are included in a specific workflow.
locale: en-US
release: xanadu
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Input variable movement, Workflow administration, Classic Workflow, Build workflows]
---

# Input variable movement use case - two input variables

An existing workflow already contains two input variables.

1.  User A checks out the workflow.
2.  User A adds two input variables.

    ServiceNow adds to the current update set one customer update record for each new variable.

    The current workflow now has 4 input variables: the two that were present prior to check out and the two new ones.

3.  User A publishes the workflow.

    There are now three related customer update records: two for new variables, and one for the published workflow. The XML payload of the new workflow version now includes all input variable database entries. So while the two original input variables do not have individual customer update records, all four variables are migrated to the local instance with the payload of the newly published workflow version.

4.  Verify variables included in a specific workflow.
5.  User A completes the update set.
6.  Adding Input Variables - Success

    User A migrates and commits the update set to a local instance where the original workflow version had previously been committed.

    -   The two existing input variables are already present because of the earlier version.
    -   The system adds the two new input variables when the user commits the update set.
    -   The system preserves the two legacy input variables on the instance receiving the update set. The update set does not overwrite these variables.
    -   The new published workflow version uses all four variables.
    -   The user tests the new workflow version and it runs as expected.

**Parent Topic:**[Input variable movement](../concept/c_InputVariableMovement.md)

## Verify variables included in a specific workflow

You can verify the variables that are included in a specific workflow.

### Procedure

1.  Navigate to **All** &gt; **System Update Sets** &gt; **Local Update Sets**.

2.  Select the active update set.

3.  Select the customer update entry for the workflow.

4.  View the **XML Payload**.

5.  Search for the name of one of the columns or search for var\_dictionary.

    There is one var\_dictionary entry for each input variable.


