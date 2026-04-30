---
title: Upgrade Accounts Payable Operations
description: Upgrade Accounts Payable Operations from any version to the latest version.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Components installed with Accounts Payable Invoice Processing, Install Accounts Payable Invoice Processing, Configuring Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Upgrade Accounts Payable Operations

Upgrade Accounts Payable Operations from any version to the latest version.

## Before you begin

Role required: admin

## Procedure

1.  When you upgrade Accounts Payable Operations from any version to the latest version, follow the steps mentioned in [Configuring the invoice ingestion flows using Accounts Payable Operations integration with Document Intelligence](../concept/config-apo-docintel-integration.md) with the latest use case- **DO NOT USE- Invoice Processing Vx** SYS DI Task Definition.

    X refers to the latest version.

2.  [Create a copy of the default Invoice Processing use case](create-use-case-copy.md).

3.  [Configure the newly created DocIntel Extract Values Flow](configure-extract-values-flow.md).

4.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

5.  To copy and configure the invoice attachment DI processing flow, perform the following steps:

    1.  Search and use the existing flow that was copied from [Copy and configure the Invoice attachment DI processing flow](copy-di-processing-flow.md).

    2.  Open **Flows**.

    3.  Under ACTIONS, do the following:

        -   Select **Process Attachment using DI** to expand it.
        -   In the **SYS DI Task Definition \[Use Case\]** field, select the copy of the use case that was created using the **Duplicate use case** icon \(![Duplicate icon](../image/duplicate-di-usecase.png)\). For more information on copying use case, refer [Create a copy of the default Invoice Processing use case](create-use-case-copy.md).
    4.  Select **Save**.

    5.  Select **Activate**.

6.  To copy and configure the DI STP failed flow, perform the following steps:

    1.  Search and use the selected flow from DI STP failed flow.

    2.  Under **TRIGGER**, in the **Condition** field, ensure that you select the copy of the use case that was created in Global scope.

        For more information on copying use case, refer [Create a copy of the default Invoice Processing use case](create-use-case-copy.md).

    3.  Select **Save**.

    4.  Select **Activate**.


