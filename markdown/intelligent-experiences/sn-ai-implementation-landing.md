---
title: ServiceNow AI implementation
description: Getting ready to implement Now Assist is more than just installing plugins—it’s about laying the groundwork for a seamless, intelligent experience across your workflows. Whether you're enabling conversational catalogs, automating content generation, or enhancing user interactions, a few key steps will ensure your data is ready, your applications are prepared, and your organization's AI policy is in alignment with your implementation.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-10-14"
reading_time_minutes: 4
breadcrumb: [Enable AI experiences]
---

# ServiceNow AI implementation

Getting ready to implement Now Assist is more than just installing plugins—it’s about laying the groundwork for a seamless, intelligent experience across your workflows. Whether you're enabling conversational catalogs, automating content generation, or enhancing user interactions, a few key steps will ensure your data is ready, your applications are prepared, and your organization's AI policy is in alignment with your implementation.

## Get started

<table id="table_vhh_f41_zgc" class="nav-card presentation"><tbody><tr><td>

[Now Assist overview![](../../../reuse/icons/brand-icons/bus-explore.svg)Learn about the applications and features that make up the Now Assist experience.](sn-ai-impl-overview-tools.md)

</td><td>

[AI governance![](../../../reuse/icons/brand-icons/bus-business-management.svg)Learn about the importance of AI governance to ensure responsible use, regulatory compliance, and alignment with enterprise goals.](sn-ai-impl-governance.md)

</td><td>

[Data readiness![](../../../reuse/icons/brand-icons/bus-database.svg)Learn how to prepare your instance data for Now Assist.](sn-ai-impl-data-readiness.md)

</td></tr><tr><td>

[Application readiness![](../../../reuse/icons/brand-icons/bus-management-console.svg)Ensure that your instance is ready to take advantage of Now Assist by preparing Platform applications.](sn-ai-impl-app-readiness.md)

</td><td>

[Resolve common issues![](../../../reuse/icons/brand-icons/bus-root-cause-issue-resolution.svg)Address issues or gaps in your Now Assist configuration.](../../now-assist-admin/reference/now-assist-install-config-checklist.md)

</td><td>

 

</td></tr></tbody>
</table>Additional implementation information is available on [Now Create](https://learning.servicenow.com/nowcreate).

For additional Now Assist resources, see [Additional resources for AI products and solutions](../../general/reference/ai-additional-resources.md).

**Important:**

-   Not all model providers are available for customers with in-country SKUs, and some Now Assist products/features are currently unavailable for in-country customers. For more information, see the [KB1584492](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1584492) article in the Now Support Knowledge Base. Be sure to check for model provider availability updates in future releases.
-   Some Now Assist products/features are currently unavailable for customers in the FedRAMP, NSC DOD IL5, or Australia IRAP-Protected data centers, self-hosted customers, or in other restricted environments. For more information, see the [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854) article in the Now Support Knowledge Base. Be sure to check for availability updates in future releases.
-   Some Now Assist products/features are currently available only for customers in some regions. Be sure to check for availability updates in future releases.
-   Some AI products and skills are not available in Regulated Markets. For more information, see [KB2593939: Regulated Markets AI Products/Skills Not Available](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=e8d7cc82475aba90b7832920326d4362). Be sure to check for availability updates in future releases.

## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

## Data processing

This application requires data to be transferred from ServiceNow customers' individual instances to a centralized ServiceNow environment, which may be located in a different data center region from the one where your instance is, and potentially to a third-party cloud provider, such as Microsoft Azure. This data is handled per ServiceNow's internal policies and procedures, including our policies available through our [CORE Compliance Portal](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0564067).

## Data collection

ServiceNow collects and uses the inputs, outputs, and edits to outputs of this application to develop and improve ServiceNow technologies including ServiceNow models and AI products. Customers can opt out of future data collection at any time, as described in the [Now Assist Opt-Out page](../../now-assist-admin/task/opt-out-of-data-sharing-for-now-assist.md).

