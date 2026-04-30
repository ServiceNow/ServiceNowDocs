---
title: Export and import an Agent Client Collector policy
description: You can move a single or multiple Agent Client Collector policies from one ServiceNow instance to another by exporting the policy and then importing it into the target instance. Only published policies can be exported.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create a new Agent Client Collector policy, Working with checks and policies, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Export and import an Agent Client Collector policy

You can move a single or multiple Agent Client Collector policies from one ServiceNow instance to another by exporting the policy and then importing it into the target instance. Only published policies can be exported.

## Before you begin

Ensure that you published the policies you want to export on the source instance.

**Note:** When working in a domain separated environment, imported policies are moved from the source instance domain to the identical domain on the target instance. Therefore, you must ensure that you have defined the same domains on the target instance as you have on the source instance, either by cloning the source instance or by exporting and importing domains from the source to the target instance.

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Policies**.

2.  Select the check box of the published policies you want to export.

3.  In the **Actions on selected rows...** list underneath the list of policies, select **Export policies**.

    A confirmation dialog box appears.

4.  Click **Yes**.

    The selected policies are exported as an update set file in XML format, which is downloaded to your browser. The generated update set has the following name convention: `AccPolicyExport <Current Date and Time>`. For example, `AccPolicyExport 2020-08-11 15:35:05`.

5.  Import the policy to the target instance.

    1.  Navigate to **System Update Sets** &gt; **Retrieved Update Sets**.

        The **Retrieved Update Sets** page appears.

    2.  Right-click on one of the table headers and select **Import XML**.

        The **Import XML** page appears.

        ![Import XML page](../image/ACC-Import-XML.png)

    3.  Click the **Choose File** button and select the previously downloaded update set to import.

    4.  Click **Upload**.

        **Note:** When the exported content is in a scope, the imported update set appears on the **Retrieved Update Sets** page as multiple records. The **Global** scope record is the parent, and the other records appear with the Global record as their parent update set. Only the Global update set record can initiate the import process.

    5.  Select the **Global** update set.

    6.  On the **Retrieved Update Sets** page, click **Preview Update Set Batch** to verify whether there are any conflicts with existing policies on the target instance.

        Resolve any conflicts, as needed.

    7.  If no conflicts exist, click **Commit Update Set Batch** to validate and commit the update set.

    8.  Navigate to **Agent Client Collector** &gt; **Policies** and verify that the imported policies appear on the Policies list.

        The imported policies are synchronized with the relevant MID Servers on the target instance and are ready for immediate use.

    **Note:** The import process overrides any existing policies on the target instance and sets the imported policies to **Published**. However, draft copies of policies created on the target instance are not modified. Therefore, delete draft records of the imported policies after completing the import process, as these records are not synchronized with the published policies on the target instance.


