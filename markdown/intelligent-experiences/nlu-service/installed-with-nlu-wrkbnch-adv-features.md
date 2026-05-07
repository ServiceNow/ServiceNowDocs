---
title: Components installed with NLU Workbench - Advanced Features
description: Several types of components are installed with activation of the com.snc.nlu.workbench.advanced plugin, including tables.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Install NLU Workbench - Advanced Features, NLU Workbench - Advanced Features, Natural Language Understanding, Enable AI experiences]
---

# Components installed with NLU Workbench - Advanced Features

Several types of components are installed with activation of the com.snc.nlu.workbench.advanced plugin, including tables.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

NLU Performance Ignored Clusters\[nlu\_performance\_ignored\_clusters\]

</td><td>

Contains information on the ignored cluster. Filled when user clicks **Ignore**.

</td></tr><tr><td>

NLU Batch Test Result\[nlu\_batch\_test\_result\]

</td><td>

Contains the parsed results of a batch test including each utterance and predicted intent.

</td></tr><tr><td>

NLU Conflict Execution\[nlu\_conflict\_execution\]

</td><td>

Stores the information related to each execution of a conflict analysis run for a given definition.

</td></tr><tr><td>

NLU Batch Test Run Definition\[nlu\_batch\_test\_run\_definition\]

</td><td>

Contains base information related to the batch test execution.

</td></tr><tr><td>

NLU Batch Test Run Execution\[nlu\_batch\_test\_run\_execution\]

</td><td>

Contains information related to each execution of the batch test.

</td></tr><tr><td>

NLU Conflict Result\[nlu\_conflict\_result\]

</td><td>

Stores the complete results of a conflict analysis execution.

</td></tr><tr><td>

NLU Batch Test Utterance\[nlu\_batch\_test\_utterance\]

</td><td>

Contains the utterances used for a test set. Populated by the import set.

</td></tr><tr><td>

NLU Batch Test Set\[nlu\_batch\_test\_set\]

</td><td>

Includes the information for the batch test. Referenced by the utterance record and run definition.

</td></tr><tr><td>

NLU Performance Utterance Trace \[nlu\_performance\_utterance\_trace\]

</td><td>

Contains the information on the utterances added to an intent.

</td></tr><tr><td>

NLU Conflict Definition\[nlu\_conflict\_definition\]

</td><td>

Contains the details of the NLU model or pair of models used for the conflict.

</td></tr><tr><td>

NLU Model Analysis Definition\[nlu\_analysis\_definition\]

</td><td>

Supports IAR model tuning in NLU Workbench.

</td></tr><tr><td>

NLU Model Analysis Execution\[nlu\_analysis\_execution\]

</td><td>

Stores records for each instance of IAR model tuning in NLU Workbench.

</td></tr><tr><td>

ML Label User Feedback\[ml\_label\_user\_feedback\]

</td><td>

Stores utterances that are marked Needs review.

</td></tr></tbody>
</table>## Role installed

<table id="table_ft5_3xh_qyb"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

NLU Feedback Admin

 \[nlu\_feedback\_admin\]

</td><td>

Data labelling \(NLU feedback\) Admin role - to manage data labelling across models also ability to optimize models

</td></tr></tbody>
</table>