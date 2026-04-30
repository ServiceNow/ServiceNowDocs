---
title: Calculated Risk Score
description: Risk lookup table is to get the risk value corresponding to the success probability value and impact value.
locale: en-US
release: zurich
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Change Management, IT Service Management]
---

# Calculated Risk Score

Risk lookup table is to get the risk value corresponding to the success probability value and impact value.

sn\_chg\_probability\_risk\_lookup table is used to fetch the data to calculate the risk value of the change request.

By default, there are nine records with all the possible mappings for Impact and Success Probability along with their corresponding risk values.

Change manager can add new records and delete existing records in the table. The Check impact and probability combination business rule validates the duplicate mapping entries.

Navigate to **All** &gt; **Change** &gt; **Administration** &gt; **Calculated Risk Score**.

All the risk calculating engines calculate their corresponding risk value, the system picks the highest risk and defines the risk for the Change. You can modify the Risk values irrespective of the values defined for Impact and Success probability.

You can view the success probability definition that has set the success probability on the change request by accessing the sn\_chg\_probability\_details table. This table can be accessed by the users who has read access to the change requests.

On the change request form, in the **Related Links**, click **Calculate risk**. The risk engines calculate the risk for the Change. Click the icon against the **Risk** field to view the risk set for the Change.

Click the icon against **Calculated Risk Score** to find which type of success probability definition is responsible to set the risk for the change. There are three types of calculated risk score:

-   Calculated \(Impact + Success Probability\)
-   Calculated \(Impact + Change Success Score\)
-   Calculated \(Impact + Change Model Success\)
-   Not set: When the risk is not evaluated

**Note:**

Risk lookup supports domain separation. The **sn\_chg\_probability\_risk\_lookup** table is process separated when you install the domain separation plugin.

**Parent Topic:**[Reference section for Change Management](reference-change-management.md)

