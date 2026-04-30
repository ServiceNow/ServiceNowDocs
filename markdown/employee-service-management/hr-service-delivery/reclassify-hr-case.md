---
title: Transfer an HR case
description: You can create and use methods to reclassify or transfer an opened HR case from one HR service to another. Oftentimes an HR case opens as a General Benefits Inquiry. After investigating, you can transfer it to the applicable HR service.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Use HR Case Management, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Transfer an HR case

You can create and use methods to reclassify or transfer an opened HR case from one HR service to another. Oftentimes an HR case opens as a General Benefits Inquiry. After investigating, you can transfer it to the applicable HR service.

The base system includes two scenarios that agents can use when transferring HR cases from one service to another: Reclassify and Standard.

<table id="table_tkd_4fy_hgc"><thead><tr><th>

Functionality

</th><th>

Reclassify

</th><th>

Standard

</th></tr></thead><tbody><tr><td>

HR case number

</td><td>

Does not changeThe system closes the original case, creates a new one with the same number, and changes the number in the original case. This ensures that the subject person continues to see the same case number.

</td><td>

ChangesThe system closes the original case and creates a new case. The subject person sees a different case number.

</td></tr><tr><td>

Links

</td><td>

Redirect to the new case

</td><td>

Do not redirect from the original case to the new case

</td></tr><tr><td>

Notification emails

</td><td>

Not sent

</td><td>

Sent to the subject person with closed and transferred case information

</td></tr></tbody>
</table>The following apply to both Reclassify and Standard transfer scenarios:

-   Fields from the current case are copied and moved to the new case.

    **Note:** The sn\_hr\_core.transfer\_case.ignored\_fields sys property can be set with fields that are not copied in an HR case transfer.

-   Work notes copy from original case to new case.
-   Attachments are copied and moved from the current case to the new case.
-   Previous interaction records from the current case are copied and moved to the new case.

The sn\_hr\_core.reclassify\_default\_transfer sys property determines the default method to use after upgrade. For more information, see [HR properties](../task/t_HRProperties.md).

You can configure additional transfer case scenarios by following these steps: [Configure HR transfer case](../task/config-hr-transfer-case.md).

-   **[Configure HR transfer case](../task/config-hr-transfer-case.md)**  
The base system provides examples of HR transfer case configuration types. You can also create your own.
-   **[Move an HR case from one HR service to another](../task/TransferHRCase.md)**  
You can reclassify an HR case that you originally create under one HR service but want to move it under a different HR service.

**Parent Topic:**[Use HR Case Management](c_HRCaseManagement.md)

