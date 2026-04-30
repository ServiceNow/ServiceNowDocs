---
title: New features and products in Xanadu
description: Cumulative release notes summary on new Xanadu features and products.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2026-04-08"
reading_time_minutes: 254
breadcrumb: [Release notes summaries for Xanadu features, Release notes for upgrading from Washington DC, Learn about the Xanadu release, Xanadu release notes]
---

# New features and products in Xanadu

Cumulative release notes summary on new Xanadu features and products.

New products were introduced in Xanadu, and additional features were added to existing  products.

<table id="rn-summary-new-features-tables" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Search

</td><td>

-   **\([Xanadu Patch 9](../quality/xanadu-patch-9.md)\) Improve semantic search with third-party embedding models**

Use custom and third-party embedding models supported by the AI Search RAG application to generate more accurate and relevant semantic search results.


-   **\([Xanadu Patch 3](../quality/xanadu-patch-3.md)\) [Knowledge block content indexing](https://www.servicenow.com/docs/access?context=index-single-source-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

When you index knowledge articles for search, AI Search now includes content from knowledge blocks to improve search recall.

-   **[NLQ Genius Results support searching for multiple CMDB tables](https://www.servicenow.com/docs/access?context=genius-result-nlq-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

When your search includes terms that could match multiple CMDB tables, NLQ Genius Result answers display a drop-down list of potential CMDB table matches for each affected term. Use these drop-down lists to select the CMDB tables that you want to surface information for.

-   **[Middle dot support for Japanese](https://www.servicenow.com/docs/access?context=international-language-support-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Increase search precision for Japanese phrases that include nakaguro \(中黒, middle dot\) characters. When indexing Japanese text or searching in Japanese, AI Search preserves individual terms separated by a nakaguro instead of merging them into a single term.


</td></tr><tr><td>

AIOps LEAP

</td><td>

-   **[Incident clustering and comprehensive summaries](https://www.servicenow.com/docs/access?context=aiops-leap-features&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

AIOps LEAP smartly categorizes IT incidents based on short descriptions and assignment groups. It uses historical data to get a deeper understanding of issues and summarizes them into actionable resolutions. AIOps LEAP consolidates information from different incidents to help with decision making and serves as a repository of knowledge.

-   **[Group incidents to create automation opportunities](https://www.servicenow.com/docs/access?context=aiops-leap-features&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

AIOps LEAP uses the ServiceNow® GAF \(Group Action Framework\) plugin to organize and group incidents based on specific parameters. These groups are clusters or automation opportunities. They are created by analyzing incident data such as work notes and resolution notes. AIOps LEAP uses these automation opportunities to generate resolution steps to help solve similar future incidents.

-   **[Automation recommendations and playbook generation](https://www.servicenow.com/docs/access?context=aiops-leap-features&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

AIOps LEAP identifies frequent issues and offers automation recommendations to address them. It streamlines and optimizes operational processes by creating actionable playbooks based on historical data and resolution workflows. Additionally, it builds a knowledge base by documenting workflows and solutions through detailed resolution steps, enabling further analysis, learning, and continuous improvement. These resolution steps can be shared across teams to facilitate collaboration and enhance operational efficiency, even without formal playbook creation. Thus, automated playbook generation is a valuable output of the AIOps LEAP platform.


-   **[Enhanced opportunities page](https://www.servicenow.com/docs/access?context=aiops-leap-features&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Enhancements &amp; Design changes to load all opportunities and enable to select all cards.


</td></tr><tr><td>

API

</td><td>

<table id="table_tcd_5v3_wqb"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[CMDBQBScopedScriptableAPI - Scoped](https://www.servicenow.com/docs/access?context=CMDBQBScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   createReport\(\)
-   deleteQuery\(\)
-   getSavedQueryExecutionDetails\(\)
-   saveQuery\(\)
-   updateQuery\(\)

</td></tr><tr><td>

[HistoryWalker - Scoped, Global](https://www.servicenow.com/docs/access?context=HistoryWalkerScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

walkTo\(checkpoint\)

</td></tr><tr><td>

[NumberFormatter - Scoped, Global](https://www.servicenow.com/docs/access?context=NumberFormatterBoth&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   parseWithLocale\(\)
-   parseWithSeparators\(\)

</td></tr><tr><td>

[PDAutomationProvider - Scoped, Global](https://www.servicenow.com/docs/access?context=PDAutomationProviderBothAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   activateProcess\(\)
-   deactivateProcess\(\)
-   duplicateProcess\(\)

</td></tr><tr><td>

[PDFGenerationAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=PDFGenerationAPIBothAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

redact\(\)

</td></tr><tr><td>

[PersonalAuthAPI - Scoped](https://www.servicenow.com/docs/access?context=PersonalAuthAPIScoped&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   PersonalAuthAPI\(\)
-   getInitiatorURL\(\)
-   isTokenValid\(\)
-   revokeToken\(\)

</td></tr><tr><td>

[PlaybookExperience - Scoped](https://www.servicenow.com/docs/access?context=PlaybookExperienceScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

restartPlaybook\(\)

</td></tr></tbody>
</table><table id="table_lc5_sqn_xwb"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[CMDBQueryBuilderAPI - Global](https://www.servicenow.com/docs/access?context=CMDBQueryBuilderAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   createReport\(\)
-   deleteQuery\(\)
-   saveQuery\(\)
-   updateQuery\(\)

</td></tr><tr><td>

[DynamicSchemaAPI - Global](https://www.servicenow.com/docs/access?context=DynamicSchemaAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   clearDynamicCategoryCache\(\)
-   clearDynamicChoiceSetCache\(\)
-   clearDynamicAttributeGroupCache\(\)
-   clearDynamicAttributeGroupCacheItem\(\)
-   clearDynamicCategoryCacheItem\(\)
-   clearDynamicChoiceSetItem\(\)
-   get\(\)

</td></tr><tr><td>

[GlideAggregate - Global](https://www.servicenow.com/docs/access?context=c_GlideAggregateAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   getDynamicAttributeValue\(\) - two signatures
-   getDynamicAttributeDisplayValue\(\) - two signatures

</td></tr><tr><td>

[GlideDate - Global](https://www.servicenow.com/docs/access?context=GlideDateAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

parseDate\(\)

</td></tr><tr><td>

[GlideDynamicAttributeStore - Global](https://www.servicenow.com/docs/access?context=GlideDynamicAttStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   clear\(\)
-   getDisplayValue\(\)
-   getValue\(\)
-   setDisplayValue\(\)
-   setDynamicAttributeDisplayValue\(\)
-   setDynamicAttributeValue\(\)
-   setDynamicAttributeValues\(\)
-   setValue\(\)
-   toString\(\)

</td></tr><tr><td>

[GlideElementDynamicAttributeStore - Global](https://www.servicenow.com/docs/access?context=GlideElementDynamicAttStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   getDynamicAttribute\(\)
-   getDynamicAttributeDisplayValue\(\)
-   getDynamicAttributeValue\(\)
-   setDynamicAttributeValue\(\)
-   setDynamicAttributeValues\(\)
-   setDynamicAttributeDisplayValue\(\)
-   setDynamicAttributeDisplayValues\(\)

</td></tr><tr><td>

[GlideRecord - Global](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   getDynamicAttribute\(\) - two signatures
-   getDynamicAttributeValue\(\) - two signatures
-   getDynamicAttributeDisplayValue\(\) - two signatures
-   setDynamicAttributeValue\(\) - two signatures
-   setDynamicAttributeDisplayValue\(\) - two signatures
-   setDynamicAttributeValues\(\)

</td></tr><tr><td>

[HistoryWalker - Scoped, Global](https://www.servicenow.com/docs/access?context=HistoryWalkerScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

walkTo\(checkpoint\)

</td></tr><tr><td>

[NumberFormatter - Scoped, Global](https://www.servicenow.com/docs/access?context=NumberFormatterBoth&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   parseWithLocale\(\)
-   parseWithSeparators\(\)

</td></tr><tr><td>

[PDFGenerationAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=PDFGenerationAPIBothAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

redact\(\)

</td></tr></tbody>
</table><table id="table_g2w_k5d_mbc"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[m\_form - Client](https://www.servicenow.com/docs/access?context=m_formClientAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   addErrorMessage\(\)
-   addInfoMessage\(\)
-   getValue\(\)
-   setAffectedInputs\(\)
-   setValue\(\)

</td></tr><tr><td>

[MobileScriptIncludeCaller - Client](https://www.servicenow.com/docs/access?context=MobileScriptInclCallerClientAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   MobileScriptIncludeCaller\(\)
-   addParam\(\)
-   call\(\)

</td></tr></tbody>
</table>

</td></tr><tr><td>

Accounts Payable Operations

</td><td>

-   **[Tolerance Rules and Variances for invoices](https://www.servicenow.com/docs/access?context=tolerance-rules-and-variance&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**
    -   The **tax tolerance** rule, which defines the variance limit set on the tax amount variance in an invoice.
    -   The **under tax amount** variance exception, which is raised when the supplier-provided tax amount is less than the system-calculated tax amount.
    -   The**over tax amount** variance exception, which is raised when the supplier-provided tax amount is greater than the system-calculated tax amount.
-   **[Playbook for updating the invoice primary data](https://www.servicenow.com/docs/access?context=playbooks&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**
    -   Add tax lines to invoice lines through a playbook activity.
    -   Apply the new tax lines to single or multiple invoice lines.
-   **[Tax calculations](https://www.servicenow.com/docs/access?context=tax-calculations-in-apo&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

As a tax owner or tax manager, add tax lines and tax codes.


-   ****

The Invoice cost allocation feature allocates invoice costs across various business functions, which increases the accuracy of financial reporting, and informs strategic decision-making.

In the cost center-based approval rule for invoices, costs can be allocated to multiple cost centers, enabling cost center owners to approve the invoice only for the amount allocated to their cost center.

-   ****

The ServiceNow® Now Assist for APO application guides APO fulfillers to generate a case summary and quickly understand the case context by using the case summarization skill.


</td></tr><tr><td>

Advanced AI Search Management Tools

</td><td>

-   **[AI Search Analytics dashboard](https://www.servicenow.com/docs/access?context=ai-search-analytics-dashboard&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

The **Search application** interactive filter now supports the Mobile Platform search application.


</td></tr><tr><td>

Advanced Risk

</td><td>

-   **[Create multidimensional entities](https://www.servicenow.com/docs/access?context=create-composite-entity-ws&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Create multidimensional entities by combining two or more entities from different entity classes using the Composite Entity Management application. You can create multidimensional entity classes with a composite entity structure, such as Company \| Department \| Business Process. After defining the composite entity class, you can create composite entity that operates as a standalone entity. This feature enables you to manage risk and compliance workflows at the composite entity level, providing visibility into the combined risk and compliance posture.

**Note:** Composite entity classes can be created in both the classic UI and the Risk Workspace. The creation of composite entities is supported only in Risk Workspace.

-   **[Assess multiple risks and controls simultaneously](https://www.servicenow.com/docs/access?context=risk-assessment-project&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Create a risk assessment project to perform bulk assessments on multiple risks and controls, enabling assessors to evaluate them in a single project. This approach reduces time and effort, confirms consistency across multiple assessments, and provides a more comprehensive view of risks and controls within the same project. You can scope multiple risks related to the assessable entity within the project and perform assessments.

**Note:** Assessment of multiple risks and controls is supported only in Risk Workspace.

-   **[Addition of new roles](https://www.servicenow.com/docs/access?context=risk-assessment-project&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

The following roles related to risk assessment project were added:

    -   Risk assessment project reader \[sn\_risk\_advanced.risk\_asmt\_project\_reader\]: Provides read only access to the risk assessment projects.
    -   Risk assessment project user \[sn\_risk\_advanced.risk\_asmt\_project\_user\]: Provides the ability to create risk assessment projects and update or delete only the projects created by the user.
    -   Risk assessment project manager \[sn\_risk\_advanced.risk\_asmt\_project\_manager\]: Provides the ability to create, update, and delete any risk assessment projects.
-   **[Enhanced risk response workflow](https://www.servicenow.com/docs/access?context=workflow-of-risk-response-task&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Streamline your risk response workflow with the following enhancements:

    -   Use a uniform workflow for all types of risk response tasks. A standardized workflow for risk response tasks enhances the management of all types of risk response tasks, promotes consistency, and reduces the need for customization.
    -   Configure multiple levels of approvals for the risk response tasks using the approval configurator. By default, a single level of approval is enabled for all types of risk response tasks, where the risk owner can approve the tasks. These approvals can be configured based on requirements.
    -   Reject a risk response task and move it to the work in progress state without closing it. This feature helps the risk response task owner to modify the response strategy if the approver is unsatisfied with the response.
    -   Create action items with an independent workflow and link them to the risk response tasks when they are in the Draft or Work in progress state.

**Note:** You can create risk response action items for all types of risk responses except for Risk acceptance tasks.

    -   Copy risk response plans from the previous risk assessment to the current risk assessment while reassessing.
    -   Link an open risk response task from the previous assessment to the current risk assessment while reassessing. You can also edit or remove an existing risk response task.
-   **[Issue linking with risk assessments](https://www.servicenow.com/docs/access?context=perform-ara-workspace&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Streamline your risk assessments with the following enhancements:

    -   Enable the issue linking option on the Risk Assessment Methodology \(RAM\) form to create an issue or link an existing open issue with the risk assessment.
    -   View issue details from the configurable issue card available on the risk assessment.
    -   Identify newly created issues from existing linked issues with a visual differentiator on the issue card.
    -   Edit or remove issues.
-   **[Enhanced risk event task workflow](https://www.servicenow.com/docs/access?context=manage-risk-events&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Streamline your risk event workflow with the following enhancements:

    -   Use a uniform and enhanced workflow for the risk event tasks. A standardized workflow enhances the management of risk event tasks.
    -   Configure multiple levels of approvals for the risk event tasks using the approval configurator.
    -   Reject a risk event task and move it to the work in progress state without closing it. This feature helps the risk event task owner to modify the risk event if the approver is unsatisfied.
-   **[Improved user experience for risk identification questionnaire using Smart Assessment Engine](https://www.servicenow.com/docs/access?context=configure-risk-identification-form&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Respond to the risk identification questionnaires from the [Assessment Workspace](https://www.servicenow.com/docs/access?context=sae-asmnt-workspace&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US) with an interactive and intuitive user experience. Risk admin can select between classic and smart assessment questionnaire in the risk identification configuration without making it a forced behavior. You can migrate an existing risk identification template to the Smart Assessment Engine application. You can also create risk identification templates in the [Assessment Workspace](https://www.servicenow.com/docs/access?context=sae-asmnt-workspace&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US).

**Note:** Only published assessment templates with a Risk Identification category are available for selection on the Risk Identification Configuration form.

-   **[Configuring currency conversion dates](https://www.servicenow.com/docs/access?context=advanced-risk-properties&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Define currency conversion dates for the risk event entries in the system properties. This feature enhances the accuracy of net loss calculations by enabling you to select specific dates for currency conversion rather than relying solely on the date of impact. You can select a currency conversion date at the system property level from the following options:

    -   Risk event entry date
    -   First loss entry date
    -   Last loss entry date
    -   First recovery entry date
    -   Last recovery entry date
    -   Custom date
**Note:** You can also override the defined currency conversion dates in the risk response template configuration. These changes apply to both new and ongoing risk event workflows.

-   **[Reopen closed risk events](https://www.servicenow.com/docs/access?context=reopen-a-risk-event&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Reopen closed risk events to update existing risk events with new discoveries, losses, or relevant information without creating new risk events. This feature saves time and effort, offering flexibility and boosting efficiency in managing risk events. You can reopen a risk event individually or in bulk.

-   **Miscellaneous enhancements and improvements**

Streamline your processes with the following enhancements:

    -   Notify the risk assessor with a notification email when a risk assessment is approved or rejected.
    -   Define a specific group as the respondent type in the Feedback Integration Configuration form when the target record doesn't have a user or group. For more information, see [Configure a feedback integration](https://www.servicenow.com/docs/access?context=configure-feedback-integration&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US).
    -   Configure a single currency mode for advanced risk assessments. This feature displays all financial values in the selected single currency, confirming consistency and clarity in all fields. For more information, see [Single-currency mode](https://www.servicenow.com/docs/access?context=single-currency-mode&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
    -   View the completion date of the most recent risk identification in the new field **Last completed date**, added to the Risk Identification form. For more information, see [Set up risk identification integration](https://www.servicenow.com/docs/access?context=configure-risk-identification-form&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US).

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

-   **[External routing overview](https://www.servicenow.com/docs/access?context=awa-external-routing-overview&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Use the updated Admin UI to enable the integration of Advanced Work Assignment with third-party contact-center-as-a-service \(CCaaS\) providers with the External Routing functionality.

-   **[Migrating Advanced Work Assignment Dashboards](https://www.servicenow.com/docs/access?context=awa-dashboards-migration&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Migrate the AWA dashboards - Interactions, Messaging, Task, and Operations dashboards - to Next Experience.

-   **[Define external routing test implementation](https://www.servicenow.com/docs/access?context=define-extrnl-routng-plugin&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Defined the External Routing Test Tools plugin \(com.glide.awa.external.test\_tools\) with a simplified external-routing-provider ATF-based sample implementation to receive and process REST calls about external events.

Align the payloads generated by the demo data for the sample implementation to process and use the ATF-based tool to verify any modified components.


</td></tr><tr><td>

Agent Chat

</td><td>

-   **[Using Agent Chat](https://www.servicenow.com/docs/access?context=ci-agent-chat-using&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Trigger Now Assist while interacting with users in Agent Chat to generate a recommended response. You can edit the recommended response or have Now Assist shorten or lengthen it.

-   **[Using Agent Chat](https://www.servicenow.com/docs/access?context=ci-agent-chat-using&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Agent Chat supports multiple languages in chat summarizations.

Configure when and to whom chat summarization is available by specifying channels and roles in the Now Assist Admin console.


</td></tr><tr><td>

Agent Client Collector

</td><td>

-   **[Load the allow list only from a configuration file](https://www.servicenow.com/docs/access?context=acc-yml-options&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Enhance system security by loading the allow list from the file specified in the **allow-list** parameter of the configuration file while ignoring the allow lists that are bundled with the plugins.

-   **[Configure agent log level from the instance](https://www.servicenow.com/docs/access?context=set-agent-log-level&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Configure the agent log level from the ServiceNow instance without having to access the `acc.yml` configuration file.

-   **[Ensure secure agent connections](https://www.servicenow.com/docs/access?context=add-certificate-trust-store&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Ensure that your agent connections are secure by adding a self-signed certificate to your operating system's truststore, which verifies that the certificate is authentic.

-   **[Update existing assets](https://www.servicenow.com/docs/access?context=agent-plugins-remove&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Update your Agent Client Collector \(ACC\) plugins to the latest version by removing your existing plugins before reinstalling.

-   **[Use expanded Linux and Windows checks](https://www.servicenow.com/docs/access?context=linux-checks-policies&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Enable enhanced check functionality by using the expanded Linux and Windows checks provided with the system.

-   **[Upgrade Agent Client Collector for Kubernetes – Visibility Informers remotely](https://www.servicenow.com/docs/access?context=cnov-informer-upgrade-remote&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Starting in version 3.6.3, upgrade Informer pods in Kubernetes clusters remotely from the ServiceNow instance to avoid dependence on your Kubernetes admin.

-   **[Override Informer parameters from the Instance](https://www.servicenow.com/docs/access?context=cnov-params-override&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Starting in version 3.6.3, control CNO for Visibility Informer execution parameters from the ServiceNow instance to avoid dependence on your Kubernetes admin.

-   **[Store Instance credentials in Microsoft Azure Vault when Informer uses Azure Kubernetes Service \(AKS\)](https://www.servicenow.com/docs/access?context=cnov-deploy-prepare&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Starting in version 3.6.3, if your organization uses AKS, you can store the secret in the Microsoft Azure Vault. The Informer then pulls the ServiceNow credentials for accessing your instance from the Azure Vault.

-   **[Enable Informer to connect to the instance using OAuth2.0 authorization](https://www.servicenow.com/docs/access?context=cnov-deploy-prepare&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Starting in version 3.6.3, the Informer can use OAuth2.0 authorization to connect to the ServiceNow instance for enhanced security.

-   **[Enable expanded processing for the MID server on Network Interface Controllers \(NICs\) during keepalive operation](https://www.servicenow.com/docs/access?context=acc-yml-options&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Starting in version 3.6.3, benefit from enhanced stability when running a keepalive operation by using the enhanced MID Server capability to configure the number of Network Interface Controllers \(NICs\) that can be monitored by a keepalive operation.

-   **[Upgrade Agent Client Collector manually on a macOS system](https://www.servicenow.com/docs/access?context=acc-macos-upgrade-manual&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Starting in version 3.6.3, run the consolidated upgrade procedure manually for the Agent Client Collector in a macOS environment.

-   **[Configure the Dynatrace connector instance](https://www.servicenow.com/docs/access?context=configure-dynatrace-connector&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Starting in version 3.6.3, Event Management supports collecting raw metric data collection using the Dynatrace metric connector

-   **[Consolidate agent errors](https://www.servicenow.com/docs/access?context=view-agent-errors&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Starting in version 4.1.0, view errors for all agents on the Agent Error Messages page. Additionally, you can view errors per individual agent by selecting the agent and selecting the **ACC Error Messages** tab .

-   **[Use Linux commands to enable additional system capabilities beyond your permission level](https://www.servicenow.com/docs/access?context=acc-installation&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Starting in version 4.1.0, use Linux commands to grant enhanced permissions, which are enabled once the installation `.exe` file is executed. These enhanced capabilities are provided securely, ensuring that there is no security risk to your environment.

-   **[Use the new Windows event check for enhanced event details](https://www.servicenow.com/docs/access?context=windows-checks-policies&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Starting in version 3.12.0, use the new Windows event check to collect and filter Windows event logs.

-   **[Use the network port check to determine port availability](https://www.servicenow.com/docs/access?context=network-port-checks-policies&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Starting in version 3.12.0, use the Network port check to create events for all ports of a specified host address, which indicates whether each port is available or in use.

-   **[Enjoy multi-architecture support for docker image](https://www.servicenow.com/docs/access?context=cnov-deploy-prepare&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Starting in version 3.9.0 \(Informer version 2.3.0\), the docker image supports both arm64 and amd64 architectures. Upgrading from the previous image to the new one will not cause any disruptions. However, the new image requires more storage space in your image repository than the previous one.

-   **[Change the Informer's extensibility settings from the instance](https://www.servicenow.com/docs/access?context=cnov-params-override&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Starting in version 3.9.0 \(Informer version 2.3.0\), update the Informer's extensibility configuration directly from the Instance using the **Additional resources ConfigMap** parameter. By providing a JSON map with keys such as `resources`, `mappings`, and `mappings_oob`, you can instruct Cloud Native Operations for Visibility to retrieve additional information. If one of these keys exists and the system finds a change, it patches the ConfigMap and restarts the Informer.

-   **[View the OpenShift version in the Cluster version field on the Kubernetes Cluster CI](https://www.servicenow.com/docs/access?context=cnov-deploy-install&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Starting in version 3.9.0 \(Informer version 2.3.0\), see the OpenShift version and the Kubernetes Cluster version in one place. OpenShift operates on top of Kubernetes, so there's an OpenShift version and a Kubernetes Cluster version. By installing the Informer with the **--set openShift=true** flag, the system adds the OpenShift version number to the **cluster\_version** field on the Kubernetes Cluster CI in addition to the Kubernetes Cluster version.


</td></tr><tr><td>

Agent Workspace for HR Case Management

</td><td>

-   **[Create a case in Agent Workspace for HR Case Management](https://www.servicenow.com/docs/access?context=agent-ws-configurable-hr-create-case&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

HR agents can minimize case transfers and improve efficiency by viewing HR service descriptions populated in the HR service configuration by HR admins during case creation.

-   **[Lists in Agent Workspace for HR Case Management](https://www.servicenow.com/docs/access?context=hr-agent-ws-lists&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

View recently updated cases using the **Recently updated** tab in the Lists view in Agent Workspace for HR Case Management.

-   **[Using a Response template in an HR case or HR task record](https://www.servicenow.com/docs/access?context=hr-agent-ws-using-response-template&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Enable agents to quickly respond to HR tasks by using response templates as reusable messages that you can copy and paste into the comments or work notes for an HR task.

-   **[Resolve HR cases using guided decision trees in Agent Workspace for HR Case Management](https://www.servicenow.com/docs/access?context=guided-decision-tree-aws&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Expedite HR services by creating decision trees that agents can use to triage employee cases.

-   **[Add personal notes](https://www.servicenow.com/docs/access?context=add-pn-aws&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Upload attachments in personal notes that support the claim in Employee Relations cases for an assigned agent.


</td></tr><tr><td>

Agent experience for CSM

</td><td>

-   **[Quick start tests for Customer Service Management](https://www.servicenow.com/docs/access?context=quick-start-tests-csm&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Customer Service Management works as expected. If you customized Customer Service Management, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

App Engine Studio

</td><td>

-   **[Add users to one or more user groups](https://www.servicenow.com/docs/access?context=manage-intake-application-requests&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

When viewing an intake request in AEMC, add a user to one or more AES and Creator Studio user groups.

-   **[Manage user groups for Application Intake](https://www.servicenow.com/docs/access?context=manage-app-intake-user-groups&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Manage which AES and Creator Studio user groups are active in your instance by updating records on the User Groups Permission Types \[sn\_app\_intake\_permission\_type\] table.

-   **[Test AEMC on a non-production instance](https://www.servicenow.com/docs/access?context=test-aemc-non-production-instance&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Test AEMC on a non-production instance to ensure everything works as expected before moving to your production instance.

-   **Open applications in ServiceNow Studio**

As of Xanadu Store Release 2, open an application in ServiceNow Studio directly from a banner link in App Engine Studio to explore the more advanced application development environment ServiceNow Studio offers.


</td></tr><tr><td>

Application Vulnerability Response

</td><td>

-   **[Customize the calculation of Age and Age closed parameters of a application vulnerable item](https://www.servicenow.com/docs/access?context=avm-vul-items-fields&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, the Age and Age Closed durations of am Application Vulnerable item can be configured to be calculated from the date in the Created, Opened, or First Found fields.

-   **Open the search results in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-change-app-scope-search&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) or [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-change-app-scope-search&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) rather than the Classic UI**

Starting with v24.0.6 of Vulnerability Response, automatically open your search results in the Vulnerability Manager Workspace or IT Remediation Workspace rather than the Classic UI, by adjusting the application scope in the unified navigation bar to Vulnerability Manager Workspace or IT Remediation Workspace respectively. These application scopes are available to you based on your assigned role.

-   **[Vulnerability Manager Workspace access to the sn\_vul.app\_read\_all role](https://www.servicenow.com/docs/access?context=installed-with-avm&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, as a user with the sn\_vul.app\_read\_all role, you can view the application vulnerable items in the Vulnerability Manager Workspace.

-   **[IT Remediation Workspace access to the sn\_vul.app\_read\_assigned role](https://www.servicenow.com/docs/access?context=installed-with-avm&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, as a user with the sn\_vul.app\_read\_assigned role, you can view the application vulnerable items assigned to you and your assignment groups in the IT Remediation Workspace and remediate them.

-   **Navigate to the List page in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) or [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) by selecting the links from the All menu**

Starting with v24.0.6 of Vulnerability Response, when you enable the 'sn\_vul\_cmn\_ws.navigate\_to\_workspace' system property, selecting predefined filter links in the Application Vulnerability Response module from the 'All' menu will automatically open these links in the List page in the Vulnerability Manager Workspace or IT Remediation Workspace based on your role.

-   **Hide the record count on the lists in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) and [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, you can hide the record count on the lists in the List page in the Vulnerability Manager Workspace and IT Remediation Workspace, by adding the table names to the **glide.ui.list.seismic.omit.count** system property.

-   **[Enable automatic refresh for the Home page dashboard in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-home-page-create-filter&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, when creating and editing filters in the Application Vulnerabilities tab on the Home page of the Vulnerability Manager Workspace, you can configure the widgets to refresh automatically. Otherwise, you can manually refresh the widgets by selecting the **Refresh** button on the Application Vulnerabilities tab.

-   **[Re-evaluating remediation properties for all records in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-reevaluate-remediation-parameters&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, you can evaluate the remediation properties for all the Application Vulnerable Items from the Application Vulnerable Items list by selecting the **All items** in the **Record selection** field of the Re-evaluate remediation properties modal in the Vulnerability Manager Workspace.

-   **New Properties module**

Starting with v24.0.6 of Application Vulnerability Response, a new **Properties** module has been added to the navigation menu under the **Administration** section. This module enables direct modification of the values, offering a user-friendly method to manage and update system properties directly from the interface.

-   **[View, classify, and assign software license information you upload with your SBOM files](https://www.servicenow.com/docs/access?context=vr-sbom-license-overview&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Use the License administration module in the SBOM Workspace to help you determine your over-all license compliance and risk exposure to the open-source and vendor-supplied software components you use in your application development.

    -   View all the licenses that are used in your organization in the License administration module.
    -   Classify existing licenses as: "Permitted", "Restricted", "Banned", or "Unclassified", and create new licenses.
    -   For unassigned or missing licenses, you can manually assign licenses to components used by your applications.
-   **[Closed application vulnerable items in the SBOM Workspace reopen automatically](https://www.servicenow.com/docs/access?context=vr-sbom-config-sbom-response&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

A **Closed** application vulnerable item \(AVIT\) for a component with an associated vulnerability is reopened automatically and visible in the SBOM Workspace if the following conditions are met:

    -   The Reopen AVITs if detected \(sn\_sbom\_resp.reopen\_avits\_if\_detected\) system property is activated. This system property is activated by default.
    -   The AVIT with the associated vulnerability is detected again by a third-party integration's vulnerability scans or the component with the vulnerability is part of a subsequent SBOM upload.
    -   The substate of the **Closed** AVIT is not one of the following: **Mitigation Control in Place**, **Not Affected**, or **False Positive**. AVITs with these substates are not reopened by the system property.
Deactivate the system property only if you do not want **Closed** AVITs to reopen automatically.

-   **[Reevaluate the remediation properties for application vulnerable items in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-reevaluate-remediation-parameters&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Select the application vulnerable items conditionally for reevaluating the following remediation properties in the Vulnerability Manager Workspace:

    -   Assignments
    -   Remediation tasks
    -   Remediation target date
    -   Exceptions \(Vulnerability Response v24.0.6\)
    -   Risk score
-   **[Software Bill of Materials enhancements for CycloneDX SBOM files](https://www.servicenow.com/docs/access?context=vr-sbom-exploring&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

The following enhancements were made to support SBOM files in CycloneDX format:

Import additional information in CycloneDX SBOM files with the \(**sn\_sbom\_core.collect\_properties**\) property. This property is deactivated by default. Activate the property to import information that is generally not supported. Any information imported from these properties is uploaded to the SBOM Component Property \[sn\_sbom\_comp\_property\] table for the following:

    -   Uploaded SBOM files
    -   Metadata
    -   Individual vulnerabilities
    -   Components
View imported component data for declared and concluded licenses for SBOM files in versions 1.4 and later of CycloneDX in two new license fields:

    -   **Declared**
    -   **Concluded**
SBOM parsing support is enhanced for the following CycloneDX versions and component types:

    -   Version 1.5: Platform, Data, Device driver, Machine Learning model
    -   Version 1.6: Cryptographic
-   **[Enhancements to SBOM Response for PaCE](https://www.servicenow.com/docs/access?context=vr-sbom-exploring&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

The Policy as Code Engine \(PaCE\) application is available for SBOM Response.

    -   Determine if components are stale or abandoned with the **Run PaCE policies for SBOM Response** scheduled job. The scheduled job is deactivated by default.
    -   View components that are identified as stale or abandoned as `Non-compliant` in the PaCE interface that is available in the SBOM Workspace.
-   **[Upload SBOM files to the ServiceNow AI Platform® from your GitHub repositories](https://www.servicenow.com/docs/access?context=vr-sbom-exploring&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Determine if SBOM files generated in your CI/CD \(continuous integration and continuous delivery/deployment\) pipelines have been successfully queued in your ServiceNow AI Platform instance.

    -   Protect your environments from potentially harmful components during software development cycles with GitHub Actions that you initiate from your GitHub environment.
    -   Obtain any required GitHub Actions for SBOM upload in the GitHub Marketplace.
-   **[Enhancements to Bill of Materials records for the Veracode Vulnerability Integration](https://www.servicenow.com/docs/access?context=veracode-vuln-integration&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

**Veracode** is mapped to the **Source** field for records in the Bill of Materials \[sn\_sbom\_doc\] table for the Veracode SBOM files that you upload.

-   **[Remediation Task Rules for Container Vulnerability Response](https://www.servicenow.com/docs/access?context=remediate-cvr&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Define and group container vulnerable items automatically based on the remediation task rules.

-   **[GitHub Secrets Scanning](https://www.servicenow.com/docs/access?context=github-vuln-integration&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Ingest secrets detected in your organization’s code along with the application security testing results, enabling ease of accessibility for developers to mitigate these results.

-   **[Enhanced processing performance of scheduled job](https://www.servicenow.com/docs/access?context=installed-with-avm&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

The **Rollup application vulnerable item values to vulnerability and group** scheduled job is enhanced to create background jobs with multithreading capabilities. This upgrade involves segmenting the job into several smaller child jobs, which are executed either in parallel or concurrently. This modification enables processing of multiple records simultaneously, thus significantly speeding up the overall task.

-   **[Quick Start Tests](https://www.servicenow.com/docs/access?context=available-quick-start-tests&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US) for Application Vulnerability Response**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Application Vulnerability Response works as expected. If you customized Application Vulnerability Response, copy the quick start tests and configure them for your customizations.

-   **Set the Veracode integration to update SCA findings**

You can select the scan that takes precedence for the final updates for SCA findings data imported from Veracode. On the Veracode configuration page, ‘Default’ is the set value until you change it. You must select the Include SCA findings check box and choose one from the list:

    -   Agent – the agent scan results make the final updates to SCA finding
    -   Upload – the upload scan results make the final updates to SCA finding
    -   Default – the last scan processed, either the agent or upload scan, makes the final updates to SCA findings
**Note:** If you do not select the Include SCA findings check box on the configuration page, the scan you selected from the list is not used, and the last scan that is processed makes the final updates.

-   **Add and delete support for applications in Veracode imported from the ServiceNow AI Platform**

Set the value for the \[sn-vul-veracode.app-mark-unseen-apps-inactive\] system property to ‘true’ to prevent errors if the Platform requests applications already deleted by Veracode. If this property is set to ‘true’ \(activated\), the successful import of the Application List Integration marks any unseen applications in the Platform as ‘inactive’.

-   **[Application Penetration testing enhancements](https://www.servicenow.com/docs/access?context=pen_test_workspace_avr&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

New workspace that permits you to use the penetration testing workflow in the Next Experience UI. Alignment of penetration testing for mobile application security with the recognized standards of the Mobile Application Security Verification Standard \(MASVS\) via a questionnaire in the penetration testing workflow.


</td></tr><tr><td>

Assessments and Surveys

</td><td>

-   **[Improved Survey Response Behavior](https://www.servicenow.com/docs/access?context=c_SurveyResults&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

To ensure consistency between the platform and portal, user responses to inactive survey questions are no longer viewable. Previously:

    -   On the platform, while taking the survey/assessment, both active and inactive questions were visible.
    -   On the portal, only active questions were visible.
This update aligns platform and portal behavior. Only responses to active survey questions are accessible through the View User Response button on the assessment instance form, even if the user had answered them while the question was active. However, the responses will still be retained in the respective tables \(the response data will not be deleted from the instance\). On the response form, only active questions will be displayed

-   **[Quick start tests for Assessments and Surveys](https://www.servicenow.com/docs/access?context=quick-start-tests-survey&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Assessments and Surveys works as expected. If you customized Assessments and Surveys, copy the quick start tests and configure them for your customizations.

For more information, see [Quick start tests for Assessments and Surveys](https://www.servicenow.com/docs/access?context=quick-start-tests-survey&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).


</td></tr><tr><td>

Audit Management

</td><td>

-   **[Generate an audit report for an engagement using Microsoft Word template](https://www.servicenow.com/docs/access?context=generate-audit-report&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Use the Audit Workspace to generate audit reports for an engagement using Microsoft Word template to collaborate with your auditors in an effortless and user-friendly manner. You can manage the generated report as a cloud file either on cloud \(Microsoft SharePoint\) or as a sys\_attachment that is attached to the engagement record.

-   **[Cloud document management](https://www.servicenow.com/docs/access?context=manage-cloud-docs-using-onedrive-int&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Upload documents from your local computer as cloud files and link them to any record in ServiceNow. You can upload files to a predefined folder path and location.

-   **[User role enhancements in Audit Management](https://www.servicenow.com/docs/access?context=r_InstallWAudit&version=xanadu&pubname=xanadu-governance-risk-compliance&section=r_RolesInstallWAudit&ft:locale=en-US)**

The following roles have been added:

    -   Use the Audit approver \(sn\_audit.approver\) role to approve an engagement and audit plan. Anyone with this role can be a part of an approver list. This role is also classified as a lite operator role.
    -   Use the Audit reader \(sn\_audit.reader\) role to view the audit-related entities, such as engagements, plans, observations, and audit tasks. Anyone with this role has exclusive read access to all the entities in the Audit Management application. This role is also classified as a lite operator role.

</td></tr><tr><td>

Benchmarks

</td><td>

-   **[Benchmark KPIs](https://www.servicenow.com/docs/access?context=c_BenchKPIConfig&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

The new Self-solved using AI search QnA and Self-solved using Proactive Engagement for DeX KPIs added to the self-solved deflections are benchmarked for all the cohorts. These new contributing indicators help organizations track the self-solved deflection.


</td></tr><tr><td>

Business Continuity Management

</td><td>

-   **[Create a business impact analysis](https://www.servicenow.com/docs/access?context=create-bia-in-uib-ws&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Analyze the business impact of an asset's dependencies by using the latest updates from the most recent Business Impact Analysis \(BIA\) record. You can also determine the recovery time frame and data backup needs for the asset.

-   **[Create a business continuity plan](https://www.servicenow.com/docs/access?context=create-bcp-plan-in-uib-ws&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Access the Business Impact Analysis \(BIA\) record from the BIA column in the plan asset form. This column has been updated from a document ID type to a reference type so that you can update the BIA information and navigate to the plan record.

Identify the assets that are affected when a primary scope is operationally down by marking an asset as a primary scope and identifying its related assets. This way, you get a clear view of the relationships between assets.

-   **[Add asset and scope to the BCP](https://www.servicenow.com/docs/access?context=add-asset-plan-scope-for-bcp-uib-ws&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Identify the discrepancies between the primary and related assets by using the hierarchical view in the plan record. This way, you can address the gaps in the Recovery Time Objective \(RTO\), Recovery Point Objective \(RPO\), or Recovery Tier \(RT\) values.

-   **[Dependency Configuration records](https://www.servicenow.com/docs/access?context=dependency-config-modules&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Access up-to-date information on the dependencies that are related to the BIA, plans, or events. You can analyze how these dependencies affect your business.

-   **[Add recovery tasks](https://www.servicenow.com/docs/access?context=add-a-recovery-task&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Calculate the time that it takes to recover each event asset by tagging the assets to the recovery tasks.

-   **[Create New Recovery task form](https://www.servicenow.com/docs/access?context=create-new-recovery-task-form&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Preview the execution order of the recovery tasks by their dependencies during an exercise or an actual event. You can identify any cyclic dependencies in the recovery tasks that might trigger error notifications and stop further actions on that recovery task. You can also record the estimated time that is required for a recovery task directly on the recovery task form.

-   **[Create an exercise](https://www.servicenow.com/docs/access?context=start-exercise-event-in-uib-ws&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Assess the time and effort for an activated plan and the recovery of the impacted assets. You can track the status of an open activated plan and monitor the progress during an actual event.

-   **[Format PDF templates for BIAs, BCPs, and events](https://www.servicenow.com/docs/access?context=update-pdf-format-for-bia-bcp-event&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Improve the content in PDFs of BIAs, plans, and events by implementing a new layout:

    -   Arrange the various event tasks in a table format.
    -   Include the details of the asset owner and the description from the Business Impact Analysis.
    -   Display a table that outlines the dependencies of the plan assets.
    -   Mark the date of the PDF creation on the front page.

</td></tr><tr><td>

Case and Knowledge Management

</td><td>

-   **[Guided setup for HR Service Delivery](https://www.servicenow.com/docs/access?context=guided-set-up-hr&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Run the guided setup for each domain within HR Service Delivery. Prior to the Xanadu release, you could run the guided setup at the global domain only.

-   **Workflow to Workflow Studio migration**

Because of the enhanced features in Workflow Studio, the HR Service Activities, HR Case User Acceptance, HR Case Approval subflows have been migrated from Workflow to Workflow Studio. As an HR administrator, you can configure the **sn\_hr\_core.deprecated\_workflows** system property to decide whether to run a legacy workflow or corresponding flow in Workflow Studio.

-   **Zero Trust Access \(ZTA\) for HR Service Delivery**

Enable an administrator to configure in-time access with the dynamic role relegation feature. Based on different criteria such as the IP address, location, device, or time, the administrator can craft policies to permit only a certain subset of the user's original roles in the session.


</td></tr><tr><td>

Case management for CSM

</td><td>

-   **[Playbooks](https://www.servicenow.com/docs/access?context=customer-service-case-playbooks&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Use updated playbook templates in UI Builder that incorporate generative AI feature parity and Agent Experience modernization features such as the modeless dialogs, activity stream, lookup cards, and related items.

-   **[Order Operations Case Management](https://www.servicenow.com/docs/access?context=csm-case-mgmt-order-ops&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Use the Order Operations Case Management application \(com.sn\_order\_case\) to create order cases that reference multiple line items, including orders and order lines. Agents can use these cases to process order-related services such as order changes, inquiries, and disputes.

-   **[Case lines and workflows](https://www.servicenow.com/docs/access?context=csm-case-mgmt-case-lines&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Use the Case lines and workflows application \(com.sn\_case\_line\) to reference multiple line items on a case record, including orders or order lines, invoices or invoices lines, contracts, and sold products.

-   **[Quick start tests for Customer Service Management](https://www.servicenow.com/docs/access?context=quick-start-tests-csm&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Customer Service Management works as expected. If you customized Customer Service Management, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Clone Admin Console

</td><td>

-   **[Target instance modal](https://www.servicenow.com/docs/access?context=clone-ui-request-clone&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Request a clone to copy the data from a production instance to a non-production instance or to copy the data between non-production instances. You can request a clone without leaving the form by using the **add an instance** option in the **clone request target instance** field.

-   **[Using the same backup from another clone](https://www.servicenow.com/docs/access?context=Clone-UI&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Use the backup from another clone when you're selecting a backup option for a faster backup process. If the backup no longer exists, it triggers an on-demand backup instead.

-   **[Clone storage](https://www.servicenow.com/docs/access?context=Clone-UI&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Legacy clones and new clones are stored separately. Clones that you request via the Clone Admin Console are stored on a new table and displayed within the new console.  Legacy clones aren't shown in the Clone Admin Console. Clones that you initiate via the legacy Request Clone page are stored on the legacy Clone History table.


</td></tr><tr><td>

Cloud Cost Management 8.0.0

</td><td>

-   **[Troubleshoot billing issues in Cloud Cost Management implementation](https://www.servicenow.com/docs/access?context=compare-metricbase-spend&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Compare MetricBase \(Clotho\) data with your Spend data for Amazon Web Services \(AWS\), Azure, and Google Cloud Platform \(GCP\) to diagnose and troubleshoot Cloud Cost Management billing issues. You can also download the comparison data as a CSV file to analyze any mismatch in the cost values from both of the sources.

-   **[Gain insights into your spend of AI resources](https://www.servicenow.com/docs/access?context=spend-anaytics&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

View the total spend details for your AI services under the Machine Learning service category in your current billing download for AWS, Azure, and GCP. You can also filter your results by cloud category, tag category, and tag values.

-   **[Manage high transaction volume efficiently by installing the Cloud Cost Management Infra Stack application](https://www.servicenow.com/docs/access?context=ccm-infra-stack&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Process and download billing files quickly with improved data download speed by installing the Cloud Cost Management Infra Stack application in addition to Cloud Cost Management version 8.1.


</td></tr><tr><td>

Collaborative Work Management

</td><td>

-   **[Templates in CWM for Boards and Docs](https://www.servicenow.com/docs/access?context=templates-in-cwm-for-spaces-boards-and-docs&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

With templates in CWM, you get a predefined format for Boards and Docs, which you can use as-is or customize to suit your workflow. You can use templates for new Boards and Docs or apply them to existing ones. You can also save an existing Board or Doc in its current format as templates.

Template Center provides a centralized space where you can manage all templates for Boards and Docs.

-   **[Board views in CWM](https://www.servicenow.com/docs/access?context=board-views-in-cwm&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Create and customize Board display preferences such as column display and order, sorting, and filters based on the audience and purpose.

    -   Save Board display preferences as personal or shared views.
    -   Create shared views for the team so that all the team members consuming the data have the same experience.
    -   Create multiple views for the same Board so that you can display data in a way that is fit for your audience.
    -   Quickly switch between views to avoid manually updating display preferences each time the audience is changed.
    -   Update the view preferences anytime to adapt to changing processes.
-   **[Export a CWM Board to CSV or Microsoft Excel](https://www.servicenow.com/docs/access?context=export-a-board-in-cwm-to-csv-or-excel&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Extract data of the tasks on a CWM Board into a CSV or Microsoft Excel file so that you can use it to obtain insights, share with stakeholders, and prepare for analysis or presentations.

The exported CSV or Excel file doesn't retain the hierarchy of the CWM tasks from the List view.

-   **[Export a Doc in CWM to a PDF file](https://www.servicenow.com/docs/access?context=export-a-doc-in-cwm-to-a-pdf-file&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Export pages of CWM Docs as PDF files so that you can share documentation across emails to multiple teams or to stakeholders who don’t have access to CWM.

-   **[My Work in CWM](https://www.servicenow.com/docs/access?context=my-work-in-cwm&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Manage all your assigned work such as CWM tasks, project tasks, RIDAC items, Agile stories, and demand tasks from a consolidated dashboard view with My Work.

    -   Track overall progress on all work that's assigned to you and quickly identify tasks that are high priority or overdue using different widgets and visualizations in the **Overview** tab.
    -   View all assigned tasks in a list view from the **List** tab. From this view, you can also navigate to the source item. If a Risk is assigned to you, you can navigate directly to the relevant RIDAC page in Project Workspace for more details.
    -   Filter the dashboard to show only specific tasks or from a specific date range.
-   **[Duplicate a Board in CWM](https://www.servicenow.com/docs/access?context=duplicate-board-in-cwm&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Save time by duplicating an existing Board to copy all the task and collaborator details without having to copy the information manually.

    -   The copied Board is added to the same Space as the original Board.
    -   The states of all the copied tasks are reset to default in the Board.
    -   Any custom columns in the original Board are copied to the new Board.
-   **[Duplicate a Doc in CWM](https://www.servicenow.com/docs/access?context=duplicate-doc-in-cwm&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Save time by duplicating an existing Doc to copy all its pages and content without having to copy the information manually. The copied Doc is added to the same Space as the original Doc.

-   **[Add People column users in Board automations](https://www.servicenow.com/docs/access?context=implementing-automations-in-collaborative-work-management&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Board automations to notify and send an email can now include users and groups from the columns of the CWM task. For example, you can create an automation to notify the task assignee whenever a task priority is updated. The users are dynamically picked from the **Assigned to** column of the task. Similarly, a custom column of the type **People** can be used to create such automation.


</td></tr><tr><td>

Common Governance, Risk, and Compliance feature

</td><td>

-   **[Management method in issue grouping](https://www.servicenow.com/docs/access?context=issue-grouping-in-workspaces&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Group and manage issues from a parent issue, or manage child issues independently using the group issue management method. When you select the Management method as **Manage parent**, the child issues inherit the values of the **State**, **Response**, and **Explanation** fields from the parent issue. When **Manage child** is selected, the child issue maintains its own **State**, **Response**, and **Explanation** fields individually.

As a part of this feature, the following two new fields were added on the issue record in the Issue grouping section:

    -   **Group level**: Identifies whether an issue is a child, parent, or a standalone issue.
    -   **Management method**: Indicates whether the issue is managed from a parent issue or as an individual child issue.
-   **[Confidentiality and inheritance enhancements in issue grouping](https://www.servicenow.com/docs/access?context=confidential-records&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Streamline the issue grouping process with the following enhancements:

    -   Add confidential child issues only under a confidential parent issue.
    -   Add nonconfidential child issues under a confidential or nonconfidential parent issue.
    -   Change a confidential parent issue to nonconfidential. This action will remove all confidential child issues under the parent issue, making them standalone issues after you save the record.

**Note:** When you change a nonconfidential child issue to confidential, which is under a nonconfidential parent issue, this action removes the child issue from the nonconfidential parent issue. The child issue becomes a standalone issue and no longer linked to the parent issue.

-   **[GRC Licensing Overview dashboard](https://www.servicenow.com/docs/access?context=grc-licensing-summary-dashboard&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Use the self-service GRC Licensing Overview dashboard to track license usage trends and next month's projected usage based on role allocation. You can see the monthly aggregated counts of license consumption across different product families including Integrated Risk Management, Business Continuity Management, and Privacy Management. The following infrastructure enhancements were made:

    -   Expanded the unique user usage table capacity from 9 months to 12 months.
    -   License consumption details are archived for five years.
    -   Aggregated monthly counts of license usage are stored.
-   **[Introducing GRC Employee role](https://www.servicenow.com/docs/access?context=grc-common-roles&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Install the new GRC Employee User application and assign the GRC Employee role to your employees. The users with the GRC Employee role can perform the following activities from the Employee Center:

    -   Read and acknowledge organizational policies.
    -   Report risk events and issues.
    -   Request policy exceptions.
    -   Report a compliance case to the Compliance team.
    -   Raise inquiries and requests to the Compliance team.
**Note:** This update is only applicable to customers who are entitled to and have installed the GRC Employee User application. For more details, review the entitlement on the subscription dashboard or contact ServiceNow.

-   **[Lite operator role enhancements](https://www.servicenow.com/docs/access?context=grc-common-roles&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

The sn\_audit.reader and sn\_audit.approver roles were added as Lite Operator roles. These new roles are available to all customers.

The following Operator roles are reclassified as Lite Operator roles when GRC Employee User application and GRC Business User Lite applications are installed:

    -   sn\_grc.business\_user
    -   sn\_risk\_advanced.ara\_assessor
    -   sn\_irm\_cont\_auth.authorization\_official
    -   sn\_irm\_cont\_auth.reader
    -   sn\_irm\_cont\_auth.executive\_read
**Note:** This reclassification is only applicable to customers who are entitled to and have installed the GRC Employee User application. For more details, review the entitlement on the subscription dashboard or contact ServiceNow.

-   **[Entity filter deletion or modification warning](https://www.servicenow.com/docs/access?context=what-is-an-entity-filter&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Avoid the unintended consequences of deleting or modifying an entity filter with a warning message. This message includes an impact analysis of the affected entity, risk, and control records.

-   **[Document designer integration](https://www.servicenow.com/docs/access?context=configuring-audit-word-based-templates&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

You can update and add content using Microsoft 365 for ServiceNow Reporting now integrated with the Document designer application to insert data and reports into a Microsoft Word document.

-   **[Role attribution to licensing mapping tab](https://www.servicenow.com/docs/access?context=grc-licensing-summary-dashboard&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Use the Role attribution to licensing mapping tab on the GRC Licensing Overview dashboard to understand how licensing applies to roles and users. This tab helps you with the following:

    -   Identify the license treatment for all the default GRC roles.
    -   Determine the license treatment of a specific user based on their assigned roles.
    -   Determine the license treatment for a specific combination of roles.
-   **[Map stakeholders in entity](https://www.servicenow.com/docs/access?context=entities-in-risk-ws&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Use the Stakeholders related list in the entity form to define stakeholders with customizable roles relevant to single and composite entities. This feature enables effective team involvement in risk assessments and risk assessment projects. You can add persona, group, and users in the stakeholder list.


</td></tr><tr><td>

Compliance Case Management

</td><td>

-   **[Regulatory Agency Library](https://www.servicenow.com/docs/access?context=regulatory-agency-library-rcm&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Establish a centralized library of agencies for identifying the relevant regulatory authorities that are responsible for overseeing particular industries or sectors within each jurisdiction. The centralized library consolidates all the regulatory communications via emails and implements the notification rules for the data privacy or security breaches for the reported compliance cases.

-   **[Auto-calculate future dates](https://www.servicenow.com/docs/access?context=auto-calculate-future-dates&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Set up future auto-calculations to track your compliance cases or requests.


</td></tr><tr><td>

Configuration Compliance

</td><td>

-   **[Identify Wiz Resource Types for import](https://www.servicenow.com/docs/access?context=wiz-assets-resources-tab&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Identify the Resource Types \(assets\) reported by Wiz in your environment on the Wiz Integration Resource Type configuration page in your ServiceNow AI Platform instance that you want to import.

The Resource Types that you select apply to all the primary Wiz vulnerability and compliance integrations except the Wiz Container Vulnerability Integration.

-   **[Wiz Backfill Integrations](https://www.servicenow.com/docs/access?context=wiz-backfill&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Retrieve and process data stored on the Wiz Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table for missing assets that were not processed by the primary compliance integrations with specialized Wiz Backfill Integrations.

    -   Test Results Backfill Integration
    -   Host Test Results Backfill Integration
    -   Issues Backfill Integration
The Wiz Backfill Integrations are activated by default.

-   **[Wiz Host Test Result Vulnerability Integration](https://www.servicenow.com/docs/access?context=wiz-host-test-result-tab-filters&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Import test results associated with the resource type, `VIRTUAL MACHINE` with the Wiz Host Test Result Vulnerability Integration. This integration is activated by default.

-   **[New Properties module](https://www.servicenow.com/docs/access?context=installed-with-config-compliance&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v15.1 of Configuration Compliance, a new **Properties** module has been added to the navigation menu under the **Administration** section. This module enables direct modification of the values, offering a user-friendly method to manage and update system properties directly from the interface.

-   **[Customize the calculation of Age and Age closed durations of a test result](https://www.servicenow.com/docs/access?context=view-vuln-config-compl-test-results&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v15.1 of Configuration Compliance, the Age and Age Closed durations of a test result can be configured to be calculated from the date in the Created, Opened, or First Found fields.

-   **[Associating a Qualys Test with its Test Group](https://www.servicenow.com/docs/access?context=Qualys-cc-Integration&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

You can associate a Qualys Test with its Test Group by enabling the **sn\_vulc.add\_policy\_as\_key** system property. This helps you to identify the Test Group to which a Test Result belongs to and differentiate Test records with the same Test id that are associated with different Test Groups.

-   **[Calculate the remediation target date of a remediation task with respect to the Last Opened date](https://www.servicenow.com/docs/access?context=cc-remed-target-rules&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v15.1 of Configuration Compliance, you can customize the calculation of the remediation target date of a remediation task to be calculated with respect to the Last Opened date.

-   **Open the search results in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-change-app-scope-search&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) or [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-change-app-scope-search&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) rather than the Classic UI**

Starting with v24.0.6 of Vulnerability Response, automatically open your search results in the Vulnerability Manager Workspace or IT Remediation Workspace rather than the Classic UI, by adjusting the application scope in the unified navigation bar to Vulnerability Manager Workspace or IT Remediation Workspace respectively. These application scopes are available to you based on your assigned role.

-   **[Vulnerability Manager Workspace access to the sn\_vulc.read role](https://www.servicenow.com/docs/access?context=installed-with-config-compliance&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, as a user with the sn\_vulc.read role, you can view the test results in the Vulnerability Manager Workspace.

-   **Navigate to the List page in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) or [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) by selecting the links from the All menu**

Starting with v24.0.6 of Vulnerability Response, when you enable the 'sn\_vul\_cmn\_ws.navigate\_to\_workspace' system property, selecting predefined filter links in the Configuration Compliance module from the 'All' menu will automatically open these links in the List page in the Vulnerability Manager Workspace or IT Remediation Workspace based on your role.

-   **Hide the record count on the lists in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) and [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, you can hide the record count on the lists in the List page of the Vulnerability Manager Workspace and IT Remediation Workspace by adding the table names to the **glide.ui.list.seismic.omit.count** system property.

-   **[Enable automatic refresh for the Home page dashboard in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-home-page-create-filter&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, when creating and editing filters on the Configuration Test Results tab on the Home page of the Vulnerability Manager Workspace, you can configure the widgets to refresh automatically. Otherwise, you can manually refresh the widgets by selecting the **Refresh** button on the Configuration Test Results tab.

-   **[Re-evaluating remediation properties for all records in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-reevaluate-remediation-parameters&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, you can evaluate the remediation properties for all the test results from the Configuration Test Results list by selecting the **All items** in the **Record selection** field of the Re-evaluate remediation properties modal in the Vulnerability Manager Workspace.

-   **[Re-evaluate remediation properties for test results in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-reevaluate-remediation-parameters&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Select the test results conditionally for reevaluating the following remediation properties in Vulnerability Manager Workspace:

    -   Assignments
    -   Remediation tasks
    -   Remediation target date
    -   Exceptions \(Vulnerability Response v24.0.6\)
    -   Risk score
-   **[Using bulk edit for test results in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-bulk-edit-overview&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Perform the following tasks on multiple test results simultaneously or a remediation task in Vulnerability Manager Workspace:

    -   [Assign test results to an assignment group for remediation](https://www.servicenow.com/docs/access?context=vmws-bulk-edit-assign&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US).
    -   [Request an exception in bulk](https://www.servicenow.com/docs/access?context=vmws-bulk-edit-request-exception&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US).
    -   [Mark test results as false positive in bulk](https://www.servicenow.com/docs/access?context=vmws-bulk-edit-request-false-positive&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US).
-   **[Populating additional information for the test results](https://www.servicenow.com/docs/access?context=view-vuln-config-compl-test-results&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

The Age, Age closed, Closed date, Active, and Last open date columns have been added in the test results table.

The test results that aren’t in the Closed state are marked as true in the **Active** field. The **Active** field replaces the **Result** and **State** fields in the filter conditions of the default-saved filters across the All menu, Configuration Compliance Overview, Unified, Cybersecurity Executive, and Health dashboards.

-   **[CI compliance and test results compliance on a Test Group in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

View the percentage of CI compliance and test results compliance on a Test Group in Vulnerability Manager Workspace.

-   **[Enabling or disabling the test results import for a Qualys test group in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=enable-disable-imports-qualys&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Enable or disable the import of test results for a Qualys test group in Vulnerability Manager Workspace.

-   **[Updating Rollup weights section in the roll up calculators](https://www.servicenow.com/docs/access?context=v11create-rollup-calc&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Other than the script format, an alternative approach of adding the weights in the Rollup Weights section for the rollup calculators has been introduced.

-   **[Percentage test result compliance in the Discovered Items table](https://www.servicenow.com/docs/access?context=discovered-items-fields&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

The percentage of test results compliance of a CI is populated in the % Test Results Compliance column of the Discovered Item. To populate this value in the % Test Results Compliance column, set `calcTRComplianceForCI` to `true` in the **Update remediation metrics** scheduled job.

-   **[Quick Start Tests for Configuration Compliance](https://www.servicenow.com/docs/access?context=available-quick-start-tests&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Configuration Compliance works as expected. If you customized Configuration Compliance, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

-   **[CMDB Workspace v7.6](https://www.servicenow.com/docs/access?context=cmdb-workspace&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US):**
    -   Access a centralized location with a comprehensive view of CI details by using the new CI form in CMDB Workspace. The form shows the attributes \(key attributes are highlighted on a Summary page\), tags, resources, activities, relationships, related services, health state, performance indicators, and CMDB 360 data that is associated with the CI. While viewing, you can also modify many of those CI details. For information about all the details on a CI form, see [Manage CI details in CI Form](https://www.servicenow.com/docs/access?context=ci-form-cmdb-workspace&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
    -   Access the Data Certification dashboard in CMDB Workspace. The Data Certification dashboard provides the insights about the data certification activities and progress, policies and tasks, reports about certification instances, charts that show the aging certification tasks, and group and individual workloads. For more information, see [Data Certification Dashboard](https://www.servicenow.com/docs/access?context=data-cert-dashboard-workspace&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
    -   [Create or manage a shared preset](https://www.servicenow.com/docs/access?context=unified-map-manage-shared-preset&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US). Save Unified Map filter settings as shared presets that any user on the team can access. This task requires the sn\_cmdb\_admin, sm\_admin, or admin role.
    -   [Access Unified Map from the main navigation panel](https://www.servicenow.com/docs/access?context=cmdb-workspace-unified-map&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US). Access Unified Map from the main navigation panel by navigating to **All** &gt; **CMDB Workspace** &gt; **Unified Map**.
    -   Archival and destroy processes of certification policy related records, are now separated from those processes for records of all other policy types. This separation facilitates the extension of the retention period of certification policy records, as follows:
        -   The table cleanup rule for table CMDB Data Management Policy Executions \[cmdb\_data\_management\_policy\_execution\], which is stored in the Auto Flushes \[sys\_auto\_flush\] table, now excludes certification policy execution records from recurring cleanups.

Retaining certification policy execution records instead of deleting them after 7 days is useful in situations where those records are needed for audits and are also useful for the Data Certification Dashboard, which is populated by these records.

        -   The Archive CMDB Data Management Tasks archive rule, that applied to all CMDB Data Manager policy execution records, now excludes certification policy records. At each archive run, this archive rule is configured to also automatically archive its related records in table CMDB Data Management Certification Task To Document \[sn\_cmdb\_ws\_dm\_certification\_task\_to\_document\] \(Archive Related Records\).
        -   The archive rule, Archive Certification Instances, is added to specifically archive certification policy execution records from the CMDB Data Management Policy Execution \[cmdb\_data\_management\_policy\_execution\] table. This new archive rule is configured to archive certification policy execution records 2 years after creation, and to destroy those records 7 years after they are archived.
        -   The archive rule, Archive Certification tasks, is added to specifically archive certification task records from the CMDB Data Management Task \[cmdb\_data\_management\_task table\].
        -   The archival of related records in table CMDB Data Management Certification Task To Document \[sn\_cmdb\_ws\_dm\_certification\_task\_to\_document\] is now moved as an Archive Related Records entry from the Archive CMDB Data Management Tasks archive rule to the new Archive Certification tasks archive rule.
-   **[CMDB Health Dashboard](https://www.servicenow.com/docs/access?context=c_MonitorCMDBHealth&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

The CMDB Health Dashboard is now built using UI Builder components and is fully integrated into the CMDB Workspace. When you select either of its views, it opens in CMDB Workspace. The CMDB Health Dashboard has a modernized look and feel of the Next Experience user interface

CI health is now reported on CI forms within the CI Health tile in CMDB Workspace.

-   **[CSDM and the CMDB Data Foundations Dashboards](https://www.servicenow.com/docs/access?context=csdm-cmdb-foundations-dashboards&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Starting with version 4.0, the CSDM and the CMDB Data Foundations Dashboards store app is built using UI Builder components. You can also now access the CSDM Data Foundations Dashboard from Management tools in the Management view in CMDB Workspace.

-   **[CMDB Integrations Dashboard in the Next Experience user interface](https://www.servicenow.com/docs/access?context=cmdb-integ-dashboard&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

The CMDB Integrations Dashboard has a modernized look and feel with the Next Experience user interface. Starting with Xanadu release, the CMDB Integrations Dashboard is automatically migrated to the Next Experience user interface. For more information on the Next Experience user interface, see [Next Experience UI](https://www.servicenow.com/docs/access?context=next-experience-landing-page&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

-   ****

The ServiceNow® Now Assist for CMDB application brings generative AI to CMDB. The Now Assist for CMDB application provides the following skills:

    -   CI summarization: Shows CI details such as discovery and class, and tallies of records that are related to the CI such as incidents, alerts, and security vulnerabilities, directly on CI forms.
    -   Manage duplicate CIs: Guides you step-by-step through the process of reviewing de-duplication tasks, and then creating and running de-duplication templates to remediate tasks that you choose. As you respond to choices presented by the manage duplicate CIs skill, you receive clear guidance for what should be your next step in the remediation process. This skill also provides root cause analysis to help you prevent future generation of duplicate CIs.
-   ****

The ServiceNow® Now Assist for Service Graph Connectors \(SGC\) application brings in generative AI capabilities to resolve issues within Service Graph Connectors. The Now Assist for SGC application provides the Service Graph Connector diagnosis skill. This skill enables you to troubleshoot issues in a failed import set associated with a Service Graph Connector.

-   **[Quick start tests for CMDB](https://www.servicenow.com/docs/access?context=quick-start-tests-cmdb&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that CMDB works as expected. If you customized CMDB, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Container Vulnerability Response

</td><td>

-   **[New Properties module](https://www.servicenow.com/docs/access?context=installed-with-cvr-data&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v2.11.3 of Container Vulnerability Response, a new **Properties** module has been added to the navigation menu under the **Administration** section. This module enables direct modification of the values, offering a user-friendly method to manage and update system properties directly from the interface.

-   **[Create auto-close rules for Container Vulnerability Response](https://www.servicenow.com/docs/access?context=cvr-create-auto-close-rules&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v2.11.3 of Container Vulnerability Response, define auto-close rules with advanced conditions to automatically close older or stale CVITs based on defined filter criteria on container vulnerabilities.

-   **[Customize the calculation of Age and Age closed parameters of a container vulnerable item](https://www.servicenow.com/docs/access?context=container-vul-items-fields&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v2.11.3 of Container Vulnerability Response, the Age and Age Closed durations of a Container Vulnerable Item can be configured to be calculated from the date in the Created, Opened, or First Found fields.

-   **Open the search results in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-change-app-scope-search&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) or [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-change-app-scope-search&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) rather than the Classic UI**

Starting with v24.0.6 of Vulnerability Response, automatically open your search results in the Vulnerability Manager Workspace or IT Remediation Workspace rather than the Classic UI, by adjusting the application scope in the unified navigation bar to Vulnerability Manager Workspace or IT Remediation Workspace respectively. These application scopes are available to you based on your assigned role.

-   **[Vulnerability Manager Workspace access to the sn\_vul\_container.read\_all role](https://www.servicenow.com/docs/access?context=installed-with-cvr-data&version=xanadu&pubname=xanadu-security-management&section=roles-installed-cvr&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, as a user with the sn\_vul\_container.read\_all role, you can view the container vulnerable items in the Vulnerability Manager Workspace.

-   **[IT Remediation Workspace access to the sn\_vul\_container.read\_assigned role](https://www.servicenow.com/docs/access?context=installed-with-cvr-data&version=xanadu&pubname=xanadu-security-management&section=roles-installed-cvr&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, as a user with the sn\_vul\_container.read\_assigned role, you can view the container vulnerable items assigned to you and your assignment groups in the IT Remediation Workspace and remediate them.

-   **Navigate to the List page in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) or [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) by selecting the links from the All menu**

Starting with v24.0.6 of Vulnerability Response, when you enable the 'sn\_vul\_cmn\_ws.navigate\_to\_workspace' system property, selecting predefined filter links in the Container Vulnerability Response module from the 'All' menu will automatically open these links in the List page in the Vulnerability Manager Workspace or IT Remediation Workspace based on your role.

-   **Hide the record count on the lists in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) and [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, you can hide the record count on the lists in the List page of the Vulnerability Manager Workspace and IT Remediation Workspace, by adding the table names to the **glide.ui.list.seismic.omit.count** system property.

-   **[Enable automatic refresh for the Home page dashboard in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-home-page-create-filter&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, when creating and editing filters on the Container Vulnerabilities tab on the Home page of the Vulnerability Manager Workspace, you can configure the widgets to automatically refresh. Otherwise, you can manually refresh the widgets by selecting the **Refresh** button on the Container Vulnerabilities tab.

-   **[Re-evaluating remediation properties for all records in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-reevaluate-remediation-parameters&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, you can evaluate the remediation properties for all the Container Vulnerable Items from the Container Vulnerable Items list by selecting the **All items** in the **Record selection** field of the Re-evaluate remediation properties modal in the Vulnerability Manager Workspace.

-   **[Re-evaluate the remediation properties for container vulnerable items in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-reevaluate-remediation-parameters&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Select the container vulnerable items conditionally for reevaluating the following remediation properties in Vulnerability Manager Workspace:

    -   Assignments
    -   Remediation tasks
    -   Remediation target date
    -   Exceptions \(Vulnerability Response v24.0.6\)
    -   Risk score
-   **[Enhanced processing performance of scheduled job](https://www.servicenow.com/docs/access?context=installed-with-cvr-data&version=xanadu&pubname=xanadu-security-management&section=scheduled-jobs-installed-cvr&ft:locale=en-US)**

The **Rollup container vulnerable item values to vulnerability and group** scheduled job is enhanced to create background jobs with multithreading capabilities. This upgrade involves segmenting the job into several smaller child jobs, which are executed either in parallel or concurrently. This modification enables processing of multiple records simultaneously, thus significantly speeding up the overall task.

-   **[for Container Vulnerability Response](https://www.servicenow.com/docs/access?context=quick-start-tests&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Container Vulnerability Response works as expected. If you customized Container Vulnerability Response, copy the quick start tests and configure them for your customizations.

-   **[Vulnerability Response Prisma Registry Integration](https://www.servicenow.com/docs/access?context=pcc-integration&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Now you can ingest the static image findings obtained from the Prisma registry scan into the ServiceNow Container Vulnerability Response.


</td></tr><tr><td>

Continuous Authorization and Monitoring

</td><td>

-   **[CAM Workspace](https://www.servicenow.com/docs/access?context=cam-ws-home-page&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Use the CAM Workspace for an end-to-end user experience. The Home page, overview pages of authorization boundary and authorization package, unified tasks page, and the dashboards help you capture information and give you a better insight into the data that aids in decision making.

CAM Workspace includes exclusive features with which you can:

    -   Add related control objectives.
    -   View controls by family for a control objective and report based on families for NIST 800-53.
    -   Add attachments to assessment procedures and document notes.
    -   View all Plan of Actions and Milestones \(POA&amp;M\) in a single pane.
-   **[CAM supports the OSCAL format to export control-related information](https://www.servicenow.com/docs/access?context=oscal-support-cam&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Export SSP files in the OSCAL format based on various models such as SSP, Profile, Catalog, and Catalog overlay. The generated report is compatible to share the information with other systems. CAM supports the National Institute of Standards and Technology \(NIST\) recommended OSCAL format to provide control-based information in machine-readable formats.

-   **[CAM ATO artifacts](https://www.servicenow.com/docs/access?context=generate-ato-artifacts-cam-ws&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Generate ATO artifacts from an authorization package in Microsoft Word format for the following reports:

    -   SSP
    -   Security Assessment Report \(SAR\)
    -   POA&amp;M
-   **[Enhancements in CAM user roles](https://www.servicenow.com/docs/access?context=assign-cam-roles&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

The existing user roles in CAM application have been enhanced with the following privileges:

    -   Use the Information Owner \(sn\_irm\_cont\_auth.information\_owner\) role to view and update the information types of an authorization package.
    -   Use the Audit reader \(sn\_audit.reader\) lite role to view audit-related entities, such as engagements.
    -   Create and manage issues as a system user.

</td></tr><tr><td>

Core ServiceNow AI Platform

</td><td>

-   **[Dynamic schema for storing attributes](https://www.servicenow.com/docs/access?context=dynamic-schema&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Create and store structured groups of attributes and their values in a dynamic attribute store field.

-   **[Use ECMAScript 2021 \(ES12\) features in any server-side script](https://www.servicenow.com/docs/access?context=set-es12-mode-scripts&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)**

Use the latest JavaScript features supported with ECMAScript 2021 \(ES12\) mode in individual scripts in applications that use ES5 Standards mode or Compatibility mode. From a script’s record, select **Turn on ECMAScript 2021 \(ES12\) mode**.

-   **[Automated jobs scheduling and manual scaling of jobs](https://www.servicenow.com/docs/access?context=auto-job-scheduling&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Starting with the Xanadu release, you can opt for automated job scheduling using queue registration. Select a queue in the new event form. As an admin, you can also manually define the number of jobs running at a queue level by scaling it either up or down as required in the Queue Details form.

-   **[Migrate existing sys event applications to Message Processing Framework](https://www.servicenow.com/docs/access?context=auto-job-scheduling&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Migrate your existing sys event queues to Message Processing Framework. You can also roll back a queue back to its previous configurations.

-   **[Geo point functions](https://www.servicenow.com/docs/access?context=platform-support-functions&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Convert longitude and latitude columns to a geo point field. Convert a geo point field or any valid numeric values or columns into longitude and latitude columns or values.

-   **[System Events and Scheduled Jobs enhancements](https://www.servicenow.com/docs/access?context=track-events&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Try the new **Active Jobs** tile in the System Events dashboard that states the number of jobs associated for a queue in processing framework. You can also review the details of the completed jobs by using the new **Stuck Jobs** and **Permanent Error Jobs** tiles on the Scheduled Jobs dashboard.


</td></tr><tr><td>

Creator Studio

</td><td>

-   **[Associate a topic with a form](https://www.servicenow.com/docs/access?context=creator-studio-edit-form-settings&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

You can now add a topic to the settings for a form, enabling users to browse forms by their related topics.

-   **[Dynamic behavior for forms](https://www.servicenow.com/docs/access?context=creator-studio-dynamic-behavior&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

As of Creator Studio version 26.2.1, you can add dynamic updates to forms and their questions based on how users answer questions. For example, you can define a question to appear based on the answer to another question. See the Accessibility section of these release notes for accessibility details.

-   **[Define custom activities for use in automations](https://www.servicenow.com/docs/access?context=creator-studio-add-automation&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

As of Creator Studio version 26.2.1, administrators can define custom activities on the ServiceNow AI Platform to use in automations when building apps in Creator Studio.

-   **[Interact with sample records within Creator Studio](https://www.servicenow.com/docs/access?context=creator-studio-preview-record&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

As of Creator Studio version 26.2.1, app creators can now see how records generated by Creator Studio apps will appear by previewing and interacting with a sample record on the **Form submissions** tab. Selecting a record in the app's workspace opens it in a new tab within the app in Creator Studio.

-   **[Use questions as process triggers](https://www.servicenow.com/docs/access?context=creator-studio-add-trigger-automation&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

You can now select one of the published questions from the app's form as a trigger for its process. For example, if a user selects "blue" as the reply about their favorite color on the app's form, you can specify "blue" as the trigger for an automated process.

-   **[New send email activity in automations](https://www.servicenow.com/docs/access?context=creator-studio-add-activities-automation&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

When you create a process, you can now have your app's automation automatically send an email when specified conditions are met.

-   **[Add curated questions to a form using question sets](https://www.servicenow.com/docs/access?context=creator-studio-edit-form&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

When creating forms, developers can now select from preconfigured question sets, enabling them to select curated questions without worrying about the details. Admins create question sets on the ServiceNow AI Platform, and question sets can't be edited in Creator Studio.


</td></tr><tr><td>

Customer Contracts and Entitlements

</td><td>

-   **[Enhancements in service contracts and entitlements workflow](https://www.servicenow.com/docs/access?context=cont-ent-workflows-csm&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Track covered products directly through the contract records, facilitating changes and visibility of what is covered​. Covered products refer to specific products or order line items included in a service contract. These items are linked to the contract to define what is covered for service or maintenance. Agents in Order Management can select the products to be covered by a contract when the order is captured for the contract offering.


-   **[Create single contracts](https://www.servicenow.com/docs/access?context=create-cont-ent-workflows-csm&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Create a single contract from a single order with multiple contract offerings. Add multiple contract offerings from an order to an existing contract.


-   **[Create quotes for contract renewal or modification](https://www.servicenow.com/docs/access?context=create-cont-ent-workflows-csm&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Create a quote or an order while renewing or modifying a service contract, service contract line, or an entitlement.


</td></tr><tr><td>

Customer Success Management

</td><td>

-   **[Account onboarding playbook](https://www.servicenow.com/docs/access?context=account-lifecycle-playbook-overview&version=xanadu&pubname=xanadu-acct-lifecycle-events&ft:locale=en-US)**

Manage your account onboarding with the Account Lifecycle Events playbook, which contains activity definitions for onboarding workflows that include key details such as onboarding status and progress, and shares clear instructions on when tasks should be delivered to various stakeholders.

-   **[Account onboarding home page](https://www.servicenow.com/docs/access?context=account-lifecycle-events-onboarding-landing&version=xanadu&pubname=xanadu-acct-lifecycle-events&ft:locale=en-US)**

Monitor onboarding cases assigned to you, including case tasks, data capture tasks, and associated risks.

-   **[Data import and validation](https://www.servicenow.com/docs/access?context=account-lifecycle-import-flow&version=xanadu&pubname=xanadu-acct-lifecycle-events&ft:locale=en-US)**
    -   Upload and process multiple files to the staging table simultaneously.
    -   Use the Data Import Builder to configure data sources and transform maps for importing data.
    -   Perform field and record level data validations in the Data Validation Assist table. Additionally, 8 pre-configured field level validations are also available with the base system.
-   **[Recommended actions for account onboarding](https://www.servicenow.com/docs/access?context=account-lifecycle-events-recommend-action&version=xanadu&pubname=xanadu-acct-lifecycle-events&ft:locale=en-US)**

Provide guidance and recommended actions to the user based on the context of the current record so agents can take appropriate actions as required. Additionally, agents can use guided decision trees to navigate and troubleshoot the onboarding process.

-   **[View account onboarding cases in the Consumer Service Portal](https://www.servicenow.com/docs/access?context=account-lifecycle-view-csm-portal&version=xanadu&pubname=xanadu-acct-lifecycle-events&ft:locale=en-US)**

View Account Lifecycle Events onboarding case records or case task records on the CSM portal to see details of the Account Lifecycle Events onboarding journey.

-   **[Improve adoption and reduce attrition with Customer Success](https://www.servicenow.com/docs/access?context=account-lifecycle-events-customer-success-about&version=xanadu&pubname=xanadu-acct-lifecycle-events&ft:locale=en-US)**

Use the Customer Success feature to engage with your customers, mitigate risks by running success plays, and identify opportunities for expansion and renewals.

    -   Monitor your success portfolio on the Success landing page. View the status of your current engagements, upcoming renewals, and new engagements.
    -   View engagement details including success initiatives, success blueprint, and monitor your success cases.
    -   Create success plays and success blueprints to define manual or automated activities using the workflow launcher.

</td></tr><tr><td>

Data Management

</td><td>

-   **[Data Management policies](https://www.servicenow.com/docs/access?context=data-management-policies&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Access a holistic view of the data management rules that you configured for a table.

-   **[Support for multiple archive rules on one table](https://www.servicenow.com/docs/access?context=c_ArchiveData&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Create multiple archive rules for a single table using a data management policy.

-   **[Table cleaner performance improvements](https://www.servicenow.com/docs/access?context=table-cleaner&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Automatically delete older records more efficiently using the table cleaner.

-   **[Data Management usage dashboard](https://www.servicenow.com/docs/access?context=viewing-data-usage&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

View a summary of storage consumption on your instance and monitor the top 10 tables consuming the most data on your instance.


</td></tr><tr><td>

Data Privacy

</td><td>

-   **[Child job execution](https://www.servicenow.com/docs/access?context=dps-create-anonymization-policies&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

Run child parallel jobs to optimize the duration of your job executions.

-   **[Encrypt with column level encryption \(CLE\)](https://www.servicenow.com/docs/access?context=data-classification&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

As a security admin, view whether the discovery field is encrypted or can be encrypted.


</td></tr><tr><td>

Data management for CSM

</td><td>

-   **[Unified user - employee as a consumer](https://www.servicenow.com/docs/access?context=features-supp-and-unsupp-by-unified-consumer&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Update the additional features and workflows, such as the case types Order Management, and Field Service Management integration, to support the unified consumer \(sn\_customerservice.unified\_consumer\) role.

-   **[Inter-organization support](https://www.servicenow.com/docs/access?context=setup-bus-loc-serviced-by-bus-loc&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Enable your agents to get visibility into the business locations that they support so that they can resolve issues efficiently. You can provide the agents that are assigned to the fulfilling service organization with access to the cases, install base items, sold products, and member details of all the requesting service organizations that they’re assisting.

-   **[External business location as a fulfiller](https://www.servicenow.com/docs/access?context=industry-data-model-cases&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Enable external business locations such as partners, external agencies, and franchises to fulfill customer cases with store-related issues.

-   **[Associating assignment groups with a business location](https://www.servicenow.com/docs/access?context=setting-up-assignment-groups&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Associate groups with an internal or external business location through a one-to-many \(1:M\) relationship, which means that one or more assignment groups can be associated with a business location.

-   **[Install Base hierarchy visualization](https://www.servicenow.com/docs/access?context=install_base_hierarchy_visualisation&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

View the entire hierarchy of an install base item by using the **Install Base hierarchy** tab on the CSM Configurable Workspace. You can expand the multiple nodes of the hierarchy and create cases for the install base item.


</td></tr><tr><td>

Decision tables in Workflow Studio

</td><td>

-   **[Create a decision table in a flow](https://www.servicenow.com/docs/access?context=create-decision-table-flow&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Create a decision table directly in your flow to add decisions quickly using the flow's inputs.

-   **[Create a decision table in a subflow](https://www.servicenow.com/docs/access?context=create-decision-table-subflow&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Create a decision table directly in your subflow to add decisions quickly using the flow or subflow's inputs.

-   **[Create a decision table in a Playbook](https://www.servicenow.com/docs/access?context=make-decision-first-match-activity&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Add a decision table directly in a Playbook to manage complex business logic using the **Make a Decision - First Match** activity. Add inputs from the playbook and manage other actions based on the results of your decision tables.

-   **[Rank and reorder decision table rows](https://www.servicenow.com/docs/access?context=modify-decision-table-rules&version=xanadu&pubname=xanadu-build-workflows&section=reorder-decision-row&ft:locale=en-US)**

Determine or change the sequence in which your decision rules are evaluated by reordering the rows in a decision table. Type a new value in the **Rank** column to easily change decision row order.


</td></tr><tr><td>

DevOps Change Velocity

</td><td>

-   **[Change Management in SOW Admin Center](https://www.servicenow.com/docs/access?context=manage-admin-console-sow-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Configure Change Management features from the Service Operations Workspace Admin Center to increase change efficiency, accelerate change approvals, drive data-driven risk analysis, and leverage DevOps data for change automation.

-   **[OAuth 2.0 authentication for Azure DevOps \(ADO\)](https://www.servicenow.com/docs/access?context=set-up-azure-devops-oauth-2-0-credential&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Use OAuth 2.0 authentication to connect your Azure DevOps tool with DevOps Change Velocity ensuring a more secure authentication method.

-   **[OAuth 2.0 authentication for Jira Cloud](https://www.servicenow.com/docs/access?context=create-jira-tool-dev-ops&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Use OAuth 2.0 authentication to connect your Jira Cloud tool with DevOps Change Velocity ensuring a more secure authentication method.

-   **[Bitbucket Cloud tool integration with ServiceNow](https://www.servicenow.com/docs/access?context=bitbucket-integration-dev-ops&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Integrate the Bitbucket Cloud coding tool with DevOps Change Velocity to connect, discover, import, and process real-time repository events in DevOps Change Velocity.

-   **[DevOps Change Workspace UI for simplified creation of custom tool integration with planning, coding and orchestration capabilities](https://www.servicenow.com/docs/access?context=create-a-tool-integration-from-the-devops-change-workspace&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Integrate a new custom tool across planning, coding and orchestration capabilities with basic know-how of ServiceNow using an intuitive DevOps Change Workspace UI. It offers easy navigation to the ServiceNow Platform for defining transformer or adapter rules, or integrate the ability to do so within the Workspace wherever applicable, and embeds necessary documentation links and tooltips to support self-service.

-   **[Import based evidence collection](https://www.servicenow.com/docs/access?context=import-based-evidence-collection-for-orchestration-capability&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Improve instance efficiency by skipping step-level pipeline processing for accelerated change management and evidence collection for GitHub Actions and Azure DevOps \(ADO\) orchestration tools.


</td></tr><tr><td>

Digital End-User Experience

</td><td>

-   **[DEX Insights](https://www.servicenow.com/docs/access?context=dex-workspace-insights-tab&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

See a complete picture of your device performance, user interactions, and network health with DEX data. DEX Insights provide a simplified view with clear insights so you can identify issues and remedies before they slow you down.

-   **[Integration with ServiceNow Proactive Engagement](https://www.servicenow.com/docs/access?context=add-alert-action&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Keep things running smoothly and avoid interruptions. DEX integration with ServiceNow Proactive Engagement helps make managing your digital experience smoother. It monitors your devices and apps, sends you alerts about potential problems, and guides you through fixing them.

-   **[Desktop Assistant with Now Assist](https://www.servicenow.com/docs/access?context=chat-using-now-assist&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Troubleshoot and solve problems independently with Desktop Assistant, which gives you direct access to generative AI on a user-friendly interface.

-   **[Actions and Actions Library](https://www.servicenow.com/docs/access?context=view-actions-in-actions-library&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Automate and streamline issue resolution within digital experience environments using the Actions and Actions Library in DEX. You can use prebuilt solutions and set up automated actions to resolve issues on your own efficiently.


</td></tr><tr><td>

Digital Portfolio Management

</td><td>

-   **[Use the Admin Center in Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-admin-center&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Use the DPM Admin Center guided walk-through to set up your DPM Workspace. The Admin Center guides you to identify data in your instance that’s ready to view in DPM. Use the provided suggestions to set up and configure the DPM Workspace for that instance. For example, if planning data isn’t used in the instance, then the DPM Admin Center guides you on how to hide the Plan tab. The DPM Admin Center also provides links to appropriate tables to create or edit services, applications, and portfolios. Here are more tasks a DPM administrator can do with the DPM Admin Center.

    -   Use workflows to identify and set up solutions \(services, service offerings, business applications, and application services\). The guided walk-through includes insights into each solution's data readiness for DPM.
    -   Access the settings pages to configure the DPM Workspace using the provided system properties.
    -   Configure solution page headers and the General info section of the Info tab.
    -   Map KPI groups to solutions to view metrics in the DPM Workspace.
    -   Use links to helpful resources.
    -   Refer to common question links to aid implementation.
    -   Follow the prompts for more setup tasks.
-   **[View relationship maps in Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-view-relationship-map&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Use the ServiceNow platform Unified Map to see a more holistic and comprehensive view of your service and application relationships. The Unified Map replaces the custom DPM relationship map, but you still access the Unified Map in the context of the DPM Workspace. For more information on the platform map, see [Unified Map](https://www.servicenow.com/docs/access?context=cmdb-workspace-unified-map&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

-   **[Update KPIs in Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-kpi-descriptions&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**
    -   Update the description of a KPI indicator that's provided by the base system. The KPI indicators on solution records come from Performance Analytics \(PA\). In the DPM Workspace, you can select a tooltip on a solution indicator card to see a description that clarifies the indicator data. Even though the descriptions come with the base system, administrators can update the descriptions to accommodate the organization.
    -   With the June 2024 release and after, the **KPI latest score** system property is set to true for new and zBoot customers.
-   **[Work with Needs attention panels in Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-needs-attn-panels&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**
    -   Added problem \(PRB\) records to the Needs attention attributes so that you can identify problems on the following solutions.
        -   Services and service offerings. Problems are related to the service offering via the service offering record on the form, impacted services related list, and on the affected CIs related list. Problems are then rolled up to the parent service and should be deduplicated at the parent service level.
        -   Business applications. Problems are related to the application service via the configuration item field on the form. Problems are then rolled up from the application service to the business application and should be deduplicated at the parent service level.
        -   Application services. Problems are related to the application service via the configuration item field on the form.
    -   Updated the team logic in the DPM Contacts tab for each solution. When you select the Contacts icon \(![Contacts icon.](../../product/digital-portfolio-management/image/contacts.png)\) next to the Needs attention panel, the Teams tab includes multiple teams that support the record. The multiple team assignment is an existing platform feature that was added to Service Portfolio Management so the teams can be viewed in the DPM Workspace. For more information on the platform feature, see [Teams related list](https://www.servicenow.com/docs/access?context=teams-related-list&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Dispute Content Pack for US Regulations

</td><td>

-   **[Configurable SLA Definitions for Reg E and Reg Z](https://www.servicenow.com/docs/access?context=using-the-dispute-content-pack-for-us-regulation&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

Configure SLA definitions for Reg E and Reg Z to enable dispute agents to manage cases efficiently and enable managers to monitor progress and take timely actions.

-   **[Enhancements to dispute manager and dispute agent landing pages](https://www.servicenow.com/docs/access?context=exploring-dispute-content-pack-for-us-regulation&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

Modified the existing tabs **Debit card disputes cases** and **Credit card cases under incorrect billing** with **SLA breached** and **SLA at risk** on both the disputes manager and dispute agent landing pages.


</td></tr><tr><td>

Dispute Rules Content Pack for Mastercard

</td><td>

-   **[Decision tables](https://www.servicenow.com/docs/access?context=decision-designer-overview&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Streamline dispute processing by validating Mastercard transaction details and questionnaire answers against the eligibility rules in the decision tables that are included in this application.


</td></tr><tr><td>

Document Intelligence

</td><td>

-   **[Improved security for the document and visual insights AI agent](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Enable access control lists \(ACLs\) to improve the security for the document and visual insights AI agent. ACLs provide you with the capability to run AI agents and agentic workflow executions either as a dynamic user or an AI user.

The document and visual insights AI agent and its skills are classified as a worker or helper agent. A worker can act as an AI user with different privileges than the human user. A helper only has the privileges of a human user.


-   **[Document and visual insights AI agent](https://www.servicenow.com/docs/access?context=document-and-visual-insights-ai-agent&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Use an AI agent to help process tasks that analyze and extract data from documents and images.

-   **[Full automation for document data extraction](https://www.servicenow.com/docs/access?context=data-extraction-modes-now-assist-document-intelligence&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Automatically extract document data and process the document task without agent review.

-   **[Document chat in Virtual Agent](https://www.servicenow.com/docs/access?context=upload-documents-na-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Integrate Now Assist for Virtual Agent with Now Assist in Document Intelligence to enable chat responses based on document content.

-   **[Attachment summarization in ITSM](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-skill&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

View the summaries of attachments with the record summary in ITSM.


-   **[Now Assist in Document Intelligence](https://www.servicenow.com/docs/access?context=docintel-nowassist-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Use Now Assist in Document Intelligence to extract information from contract documents with generative AI.


-   **[Draw tool enhancements](https://www.servicenow.com/docs/access?context=use-draw-mode-to-extract-fields&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Extract the data from single fields by using the draw tool to select a document area and extract the information.

-   **[Data normalization](https://www.servicenow.com/docs/access?context=data-normalization&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Standardize the data extracted from documents with the following improvements:

    -   Determine a default interpretation of the ambiguous values for the date and number fields.
    -   Create a Reference field type to match the extracted field values with the fields in a referenced table record.
-   **[Dashboards in the Admin experience](https://www.servicenow.com/docs/access?context=monitoring-document-intelligence-performance&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Monitor the overall performance of Document Intelligence in the Document Intelligence monitoring dashboard. You can monitor the performance at the use case level in the use case performance dashboard.

-   **[Document classification integration workflow](https://www.servicenow.com/docs/access?context=configure-integration-setup&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Integrate document classification use cases with a custom application or workflow.


</td></tr><tr><td>

Document Services

</td><td>

-   **[Document Management integration with external content provider](https://www.servicenow.com/docs/access?context=integration-external-content-providers&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Collaborate on documents in Microsoft OneDrive, Microsoft SharePoint, or Google Drive.

-   **[Redaction of sensitive data](https://www.servicenow.com/docs/access?context=data-redaction-documents&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Redact sensitive information within a document for configurable workspaces.


</td></tr><tr><td>

Document Templates

</td><td>

-   **[Signing date in PDF](https://www.servicenow.com/docs/access?context=edit-pdf-mappings&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Record the date automatically when a participant signs a document. When the **Use signing date** option is selected, the date appears on the PDF document within the field that you specify in the **Field name** field on the PDF template mapping record. This capability is available for the ServiceNow signing type only.


</td></tr><tr><td>

Dynamic Translation

</td><td>

-   **[Exclusion Framework in Dynamic Translation](https://www.servicenow.com/docs/access?context=dyn-translation-exclusion-framework&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Exclusion Framework enables you to prevent machine translation of certain words and terms. You can specify words, such as official product names, that you want to shield from the translation process. You can also input regex to prevent translation of patterns such as sys ids.

-   **[The flows used by default Translator Configurations are upgraded to v4](https://www.servicenow.com/docs/access?context=migrate-v4-dynamic-translation&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

With the Xanadu Patch 3 release, the flows used by default translator configurations are automatically upgraded to v4. If you want to use v4 flows and APIs with customized translator configurations, you must migrate them manually. The previous v3 is still supported.


</td></tr><tr><td>

ERP Semantic Mining

</td><td>

-   **[Candidate result snapshot](https://www.servicenow.com/docs/access?context=erpcm-view-work-with-candidate-details&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Better ensure that the results of the mining process can be used to develop customization on development instance by exporting and importing ERP scan results using the snapshot option.

-   **[Implement re-triggering of the ERP Mining](https://www.servicenow.com/docs/access?context=ecm-and-erp-integration&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Improve candidate scoring after the creation of new custom ERP Models by re-triggering the AI/ML execution for ERP-CM on demand.


-   **[Score improvement metric for recommendations](https://www.servicenow.com/docs/access?context=erpcm-candidate-recommendations-field-descriptions&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

View the possible score improvement in the overall potential for a candidate if a specific recommendation is implemented.


</td></tr><tr><td>

Employee Center

</td><td>

-   **[Accelerate news article creation with reusable articles](https://www.servicenow.com/docs/access?context=ec-content-templates&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Create news articles faster and more efficiently by leveraging prebuilt reusable articles within content templates. Reusable articles offer a predefined content layout into which content authors can input text and images.

-   **[Content engagement](https://www.servicenow.com/docs/access?context=ec-content-engagement&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Gather feedback on content:

    -   Employees can engage with news articles by selecting a reaction icon, leaving a comment, or sharing the article.
    -   Managers can view metrics for employee engagement with an article such as the number of views, shares, and reactions.
-   **[Employee Center Pro Kiosk](https://www.servicenow.com/docs/access?context=deskless-kiosk-overview&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Empower deskless workers with simplified access to important information related to their job through a kiosk that provides self-serve opportunities such as:

    -   Access shift and time-off details.
    -   Get queries answered with the help of AI Search.
    -   Track the status of requests.
    -   Provide enhanced Employee Center Pro kiosks that can highlight targeted communication and self-service content.
    -   Leverage guided help links that make the kiosk environment accommodative and easy to navigate.
-   **[Guided Self-Service in Employee Center](https://www.servicenow.com/docs/access?context=gss-guided-self-service-overview&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Provide employees with an intuitive, visual, Q&amp;A-based experience for self-serving on highly used complex topics such as time off balance through GSS.

-   **[Content operations dashboard](https://www.servicenow.com/docs/access?context=ec-content-operations&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

View engagement metrics for published content, manage the content publishing calendar, handle incoming content requests, and review the ownership for pages and widgets through the Content Operations dashboard.

-   **[Content Analytics support for Content Publishing](https://www.servicenow.com/docs/access?context=content-library-overview-dashboard&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

View data visualizations of performance metrics for content published to the portal or the Now Mobile app using a publish plan or content schedule. Access metrics such as the most-clicked content, most-clicked notifications, number of user interactions by content, and task status.

-   **[Enhanced copy-paste options in Rich Content Editor](https://www.servicenow.com/docs/access?context=ec-rich-content-text&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Copy and paste formatted content into the Rich Content Editor while retaining the original source formatting or paste the content as plain text that matches the formatting of the destination text box.

-   **[Integrated service and experience feedback in Now Mobile®](https://www.servicenow.com/docs/access?context=ex-service-mobile&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Access feedback functionality more easily through the Experience and Service feedback functionality in Now® Mobile.

-   **[Create rich content from portal widgets](https://www.servicenow.com/docs/access?context=ec-create-content-widgets&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Create or edit content directly from the Employee Center portal pages.

-   **[Hide parameters in the Rich Content Editor](https://www.servicenow.com/docs/access?context=configure-content-rendering-parameter&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Content administrators can configure content rendering parameters for hosted videos to be hidden in the Rich Content Editor so these parameters can't be modified by users.

-   **[New campaign demo data for Content Experiences](https://www.servicenow.com/docs/access?context=ecpro-campaigns&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Access example campaigns to better understand campaign structuring, explore sample bundle trigger configurations, and discover possible use cases.

-   **[Quick start tests for Employee Center](https://www.servicenow.com/docs/access?context=quick-start-tests-employee-center&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Employee Center works as expected. If you customized Employee Center, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Employee Relations

</td><td>

-   **[Create an allegation record for HR Service Delivery Employee Relations in the legacy UI or Agent Workspace](https://www.servicenow.com/docs/access?context=hr-er-create-allegation&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

For single-subject Employee Relations cases, the **Subject of Allegation** field in relevant case tabs is automatically filled in with the subject's name.

-   **[Create an HR Service Delivery Employee Relations case using the legacy UI](https://www.servicenow.com/docs/access?context=create-hr-employee-relations&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US), [Create an HR Service Delivery Employee Relations case using Agent Workspace](https://www.servicenow.com/docs/access?context=create-hr-er-ws&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US), [Anonymously report discrimination](https://www.servicenow.com/docs/access?context=arc-report-discrimination&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Create cases specifically related to discrimination using Core UI case creation HR Service Delivery Agent Workspace for HR Case Management, or the Anonymous Report Center portal.


</td></tr><tr><td>

Encryption Key Management

</td><td>

-   **[New plugin available for Code Signing roles and administrative features](https://www.servicenow.com/docs/access?context=cs-role-landing&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

Activate the plugin to access the new roles and administration features. The new plugin creates signature migration jobs, new code signing roles, and a new code signing administration page.


</td></tr><tr><td>

Enterprise Architecture \(formerly Application Portfolio Management\)

</td><td>

-   **[Exploring Enterprise Modeling and Visualization in the EA Workspace](https://www.servicenow.com/docs/access?context=eaw-modeling&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

Use the Enterprise Modeling and Visualization functionality in Enterprise Architecture Workspace to create diagrams for your applications hierarchy. You can associate the diagrams with architectural artifacts and plan the future state modeling of your IT with alignment to the business. Creating modeling diagrams can you help your stakeholders to understand the complexities of the organization. Perform the following tasks using the Enterprise Modeling and Visualization:

    -   Create and update modeling diagrams using the General, Enterprise Architecture, and ArchiMate shapes.
    -   Create diagrams from the Business Application view using the Create diagram menu option.
    -   Create diagrams for Business hierarchy map and Business capability maps from the Enterprise Modeling and Visualization page.
    -   Apply colors to business capability shapes in the capability hierarchy map.
    -   Add related records to a shape. Add CI relationship or Reference type relationship.
    -   Synchronize shapes, relationships, and entire diagrams to the repository.
    -   Select an architectural category while creating a diagram.
    -   Share your diagrams with the other users or groups and define their access levels for the diagram.
    -   Leverage a workflow to get approval for the diagrams, and to enable committing the diagram to the database.
    -   Configure access for Enterprise Modeling and Visualization menu items for roles, users, and groups.
    -   Initiate modeling in the Enterprise Modeling and Visualization directly from any Unified map.
-   **[Technology Portfolio](https://www.servicenow.com/docs/access?context=eaw-technology-portfolio-view&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

The Technology Portfolio section has been restructured and new features have been added. The section now contains the following pages:

    -   TRM catalog
    -   Technical debt
    -   TPM lifecycles
    -   TPM risk
    -   Technology portfolio audit
-   **[Digital integration and interface enhancements](https://www.servicenow.com/docs/access?context=eaw-create-digital-interface&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**
    -   View Information Objects and SDLC Components associated with a digital integration or digital interface.
    -   View Credentials assigned to a digital interface, digital integration, and business application.
    -   Set the Provider company instead of Provider business application, for a Provider digital interface in a digital integration.
-   **[Portfolio section enhancements](https://www.servicenow.com/docs/access?context=portfolio-list-view&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

The Portfolio section has been restructured and new modules and features have been added. The following is the new structure:

    -   Business Architecture
        -   Business Units
        -   Departments
        -   Goals
        -   Value Streams
        -   Value Stream Stages
        -   Business Capabilities
        -   Business Processes
        -   Demands
    -   Application Portfolio
        -   Business Applications
        -   Application Services
        -   Digital Integrations
        -   Digital Interfaces
    -   Information Portfolio
        -   Data Domains
        -   Information Objects
        -   Architectural Artifacts
        -   Architectural Artifact Versions
        -   Diagrams
    -   My Entities
        -   My Business Capabilities
        -   My Business Processes
        -   My Business Applications
        -   My Application Services
        -   My Information objects
        -   My Architectural Artifacts
        -   My Technology Reference Model Products
        -   My Digital Integrations
        -   My Digital Interfaces
-   **[Setup section enhancements](https://www.servicenow.com/docs/access?context=eaw-setup&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

The configuration for Enterprise Modeling and Visualization is the following:

    -   Shape Libraries
    -   Modeling menu options
    -   Entities
    -   Relationships
The **TPM logs** details are now available in the Setup section.

-   **[Connect a digital interface with the CMDB API in the EA Workspace](https://www.servicenow.com/docs/access?context=eaw-relate-dig-interface-api&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

Create a relationship between a digital interface and a CMDB API from the digital interface related list. Find out which digital integration uses which API. Find the environments where they’re deployed and group the deployed APIs.

-   **[Working with the Enterprise Architecture Workspace dashboard](https://www.servicenow.com/docs/access?context=eaw-workspace-dashboard&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

The following widgets are available on the TCO tab of the Enterprise Architecture Workspace dashboard.

    -   **Business applications by TCO score**
    -   **Business application TCO by cost type and planned disposition for FY:Q \(Current quarter\)**
    -   **Top 10 business applications with the highest cost for FY:Q \(Current quarter\)**
-   **[Manage information objects of a business application in EA Workspace](https://www.servicenow.com/docs/access?context=eaw-associate-info-obj-ba&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

Relate a business application to an information object using the CI relationship \[cmdb\_rel\_ci\] table of type Uses::Used by. Use this suggested relationship to get the logical data of the information object, which can be used to leverage the business application.

-   **[Technology portfolio management \(TPM\) enhancements](https://www.servicenow.com/docs/access?context=eaw-tpm&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

Added support for all CMDB configuration items in Technology Portfolio Management \(TPM\). By default, TPM support docker containers and serverless hardware tables. An admin user can configure any of the supported CMDB CIs for TPM.

-   **[TRM product enhancements](https://www.servicenow.com/docs/access?context=eaw-create-trm-prod-lifecycle&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**
    -   For a software TRM product, the **Operating system** field is added. Using this field, the operating system on which the software TRM product can be deployed, is tracked.
    -   Added support for creating wildcard for TRM lifecycle versions, to make it easier to specify a TRM standard without the need to specify the minor version.
-   **[Support for Architectural Decision Record \(ADR\) type artifact](https://www.servicenow.com/docs/access?context=eaw-create-edit-adr&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

Create or update an artifact with type architectural decision record \(ADR\) to align it with your business requirements.


</td></tr><tr><td>

Enterprise Asset Management

</td><td>

-   **[Define required calibrations for your enterprise assets by using calibration attributes](https://www.servicenow.com/docs/access?context=add-calibration-attributes-enterprise-asset&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Use calibration attributes to define the calibrations that are required for your enterprise assets. Specify the details and requirements of each calibration, such as the calibration frequency, the calibration quality standard, and the accuracy measurement guidelines. Maintain comprehensive and up-to-date records of each calibration so that you can improve the performance, safety, and longevity of your enterprise assets.

-   **[Schedule and track enterprise asset calibrations through work orders](https://www.servicenow.com/docs/access?context=create-manage-wo-enterprise-assets&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Use work orders to schedule, to execute, and to track the progress of your enterprise asset calibrations. View and manage corresponding work order tasks by using the guided playbook experience on either your ServiceNow® instance or the ServiceNow Mobile Agent application.

-   **[Use personalized workspaces and roles tailored for healthcare and facility management industries](https://www.servicenow.com/docs/access?context=medical-facility-workspaces&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Enhance data security within your organization by creating and managing medical and facility assets and models in their customized workspaces. Use specific roles to limit access to these assets and models to improve the confidentiality and integrity of your data.

-   **[Manage repair of defective enterprise assets in the stockroom by using the Repair flow](https://www.servicenow.com/docs/access?context=requesting-repair-eam-assets&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Request repair of assets that are defective or pending repair by using the Repair flow. Enterprise asset manager can submit an asset repair request in the Enterprise Asset Workspace or by using the Service Catalog. The Repair flow includes troubleshooting, repair, and evaluation tasks. Repair orders are processed either in the Enterprise Asset Workspace or the ServiceNow mobile Mobile Agent application.

-   **[Drop off and receive assets at a stockroom](https://www.servicenow.com/docs/access?context=drop-off-receive-assets-eam&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Return the assets that you have in your personal stockroom to a different stockroom by creating a Drop off task. The asset manager of the destination stockroom receives the assets that you dropped off through a Receive task. The asset manager then verifies the received asset and closes the Drop off task.

-   **[Manage inventory picking within your stockroom](https://www.servicenow.com/docs/access?context=managing-ent-asset-pickup&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Pick assets in your stockroom easily for sourcing, enterprise asset requests, and enterprise asset refresh workflows by enabling the Pick task for your stockroom. The task lists the assets that you should pick from the stockroom. The aisle and space details of the asset provide the exact location from where the asset should be picked. You can work on pick tasks assigned to you by using the ServiceNow mobile Mobile Agent application. With the indoor mapping capabilities, you can also get directions to the location of the asset in the stockroom on your ServiceNow mobile Mobile Agent application.

-   **[Access Planned Work Management application’s capabilities through the Enterprise Asset Workspace](https://www.servicenow.com/docs/access?context=create-work-plan-eam&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Enable users of Field Service Management Pro or Field Service Management Enterprise to utilize the Planned Work Management application's functionality to manage work plans from within the Enterprise Asset Workspace.

-   **[Manage your operational assets efficiently in the workspace](https://www.servicenow.com/docs/access?context=ot-asset-management&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Get a comprehensive view of all your Operational Technology \(OT\) and Operational Equipment \(OE\) assets and manage them efficiently in the OT Asset Workspace. The OT asset manager and OT asset technician roles enable you to manage these assets.

-   **[View the hierarchy details of an enterprise model in the Enterprise Asset Workspace](https://www.servicenow.com/docs/access?context=view-model-hierarchy-eam&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Gain visibility into hierarchy details of enterprise models directly on the contextual sidebar of the Model form. You can view all the model components of the pre-assembled and user-assembled models in a tree-like format.

-   **[Manage the life cycle of enterprise models efficiently](https://www.servicenow.com/docs/access?context=create-calculated-model-lc-template-eam&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Manage the complete life cycle of your enterprise models efficiently by applying calculated model life-cycle templates. When you associate any life-cycle template with an enterprise model record, details of all the life-cycle phases are calculated and shown on the Model form.

-   **[Start the process of onboarding multiple assets directly in the Enterprise Asset Workspace](https://www.servicenow.com/docs/access?context=onboarding-multi-asset-from-ws&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Onboard multiple assets in one go by creating Onboarding orders in the Enterprise Asset Workspace. The asset onboarding playbook is a guided experience that includes a deployment activity. This activity enables you to create deployment tasks for assets using Enterprise asset deployment tasks or Work order tasks. You can also specify the location where you want to deploy the assets.

-   **[Firmware model classes added to the Expanded Model and Asset Classes Store application](https://www.servicenow.com/docs/access?context=enterprise-model-asset-classes-app&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Manage the firmware details by using Discovered firmware model and Firmware model classes available with the Expanded Model and Asset Classes Store application.


</td></tr><tr><td>

Event Management

</td><td>

-   **[Customize the default order of the alert correlation algorithm](https://www.servicenow.com/docs/access?context=Alert-Groups&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Configure the alert correlation algorithm sequence by customizing it according to your needs.

-   **[Create team-based alert management rules](https://www.servicenow.com/docs/access?context=alert-management-rule&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Assign alert management rules to specific assignment groups so that only those alerts that are assigned to the specified group are executed.

-   **[Create tag based alert clustering definitions by teams](https://www.servicenow.com/docs/access?context=alert-clustering-definitions&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Create tag clusters only for alerts that are assigned to an alert group by assigning tag-based alert clusters to specific groups.

-   **[Restrict alert groups across alert assignment groups](https://www.servicenow.com/docs/access?context=alert-filtering&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Improve the accuracy and relevance of the alert correlation by grouping alerts according to a diverse set of requirements.

-   **[Scale out for alert group creation](https://www.servicenow.com/docs/access?context=Alert-Groups&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Ensure efficiency when running a job during high-alert traffic by scaling out the alert grouping job.

-   **[View unified service map and the impact paths in Service Operations Workspace](https://www.servicenow.com/docs/access?context=view-impact-tree&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Explore the updated service map in the Service Operations Workspace, designed to focus on the path that was affected by an alert to help you quickly assess its impact on a service. The map displays all configuration items \(CIs\) for services with up to 60 CIs, regardless of alert status. For services with over 60 CIs that have alerts, it shows the path of the most severe, most recent alert. You can also investigate an even broader view of the service topology. Access the service map directly from Service Operations Workspace, or through the preview panel or an impacted service in Express List.

-   **[Perform bulk actions on alerts in Express List](https://www.servicenow.com/docs/access?context=acknowledge-alerts&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Perform an action on up to 1,000 alerts in the Active alerts list simultaneously.

-   **[Remove alerts from an alerts group in Express List](https://www.servicenow.com/docs/access?context=el-remove-alerts-from-group&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Remove secondary alerts from an alert group directly from the Express List pane or from the preview panel.

-   **[Hide closed alerts on the preview panel and in Link View in Express List](https://www.servicenow.com/docs/access?context=el-hide-closed-alerts&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

View only the open alerts on the preview panel and in Link View in Express List by toggling to hide the closed alerts.

-   **[View data on impacted services on the preview panel in Express List](https://www.servicenow.com/docs/access?context=el-impacted-services-data&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

View information about Impacted Services on the preview panel and in Link View in Express List and open the Service Map and Metric Explorer directly from the panel.

-   **[Create an incident with Now Assist in Express List](https://www.servicenow.com/docs/access?context=el-create-incident-now-assist&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Generate incidents from alerts in Express List with a summary created by genAI that includes details on configuration items and impacted services.

-   **[View data on configuration items on the preview panel in Express List](https://www.servicenow.com/docs/access?context=el-ci-data&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

View additional details about configuration items \(CIs\) that are bound to alerts on the Express List preview panel.

-   **[Speed up alert resolution with a Now Assist analysis of past related incidents](https://www.servicenow.com/docs/access?context=nai-past-incidents&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Enhance efficiency and reduce downtime with a Now Assist analysis of past incidents on the same or related CIs. Now Assist investigates historical data to identify past incidents related to the current alert and reports their frequency and criticality levels. It also provides a summary of effective strategies used to resolve them. In addition, Now Assist offers contact information for individuals or teams who have resolved similar incidents in the past and could assist when needed.

-   **[Generate an alert group description in Express List using Now Assist](https://www.servicenow.com/docs/access?context=alert-group-descr-generate-el&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Use Now Assist to generate a description of an alert group in Express List that encompasses all the alerts within the group. The generated description replaces the original description of the group.

-   **[Launch an alert analysis from the Now Assist panel](https://www.servicenow.com/docs/access?context=alert-analysis-now-assist-panel&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Analyze an alert from the Now Assist panel. The alert analysis displays directly in the Now Assist panel for convenient review.


</td></tr><tr><td>

External Content Connectors

</td><td>

-   **[Atlassian Jira Cloud external content connector](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-jira&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Retrieve searchable content and user permissions from projects in your Atlassian Jira Cloud source system.

-   **[Google Drive external content connector](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-gdrive&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Retrieve searchable content and user permissions from shared drives in your Google Drive source system.

-   **[Microsoft Teams external content connector](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-msteams&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Retrieve searchable content and user permissions from teams in your Microsoft Teams source system.

-   **[Predefined web sources external content connector](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-websources&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Retrieve searchable content from pages and subdomains in predefined public web sites.

-   **[ServiceNow product documentation external content connectors](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-snowdoc&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Retrieve searchable content from the ServiceNow product documentation site.

-   **[Slack external content connector](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-slack&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Retrieve searchable content and user permissions from public channels in your Slack source system.

-   **[Warning messages for indexed document counts](https://www.servicenow.com/docs/access?context=exploring-ext-cont-connectors&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

When an external content connector's indexed document count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit of 1,000,000 documents.

-   **[Add external content search results to Now Assist in Virtual Agent conversations](https://www.servicenow.com/docs/access?context=add-ext-cont-srch-src-na-va&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Expand the range of information available to Virtual Agent users by adding external content search results to Now Assist in Virtual Agent conversations.


-   **[Semantic vector indexing for crawled content](https://www.servicenow.com/docs/access?context=semantic-search-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Improve recall for external content searches with support for semantic vector indexing of crawled content. Semantic vector indexing is supported for all external content connectors.


</td></tr><tr><td>

Field Service Management

</td><td>

-   **[Schedule Optimization features](https://www.servicenow.com/docs/access?context=schedule-optimization-engine&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

Use Schedule Optimization to do the following tasks:

    -   Use new objectives such as **Maximize SLA compliance buffers**, **Minimize task time penalties**, and **Maximize preferred agent assignments** when you're creating a policy.
    -   Define start-of-day and end-of-day location for territory users, improving scheduling accuracy by calculating travel times based on actual agent locations.
    -   Keep similar tasks together by scheduling pre-made bundles.
    -   Reduce the beans.ai travel estimate processing time with asynchronous processing.
    -   Access the Field Service Management Scheduling Health dashboard to view task metrics, technician metrics, and optimization configuration details.
    -   Enable dispatchers to influence the behavior of schedule optimization by allowing dispatchers to edit select fields on a work order task. Dispatchers can override work order task parameters, assign tasks based on technician preferences, and allow overtime.
-   **[Field Service Territory Capacity Analytics dashboard](https://www.servicenow.com/docs/access?context=capacity-dashboard&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

Use the Field Service Territory Capacity Analytics dashboard for the following tasks:

    -   Use interactive charts and graphs to track capacity trends, including overall demand versus allocated capacity and capacity usage over time.
    -   Perform capacity gap analysis with a customizable pivot table view, which enables you to explore data by territory and demand channel.
    -   Apply filters to view specific data based on your setup, which enables targeted analysis and informed decision-making.
-   **[Agent relocation](https://www.servicenow.com/docs/access?context=relocate-agents-territories&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

Manage your agents by performing the following tasks:

    -   Relocate agents from one territory to another for a particular duration.
    -   Facilitate precise destination territory selection, which ensures that each agent is placed in the most preferable location.
    -   Match resource availability with task requirements through improved schedule planning, which optimizes task execution and efficiently addresses unscheduled work.
    -   Minimize manual overhead and avoid manual tracking processes by simplifying the handling of temporary resource relocations.
-   **[Optimize agent operations with flexible work locations](https://www.servicenow.com/docs/access?context=change-agent-start-end-location&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

Add flexible work locations for agents by performing the following tasks:

    -   Define different start-of-day and end-of-day locations for agents to start their day at one location and end at another location, providing flexibility in their operations.
    -   Offer additional flexibility by implementing exceptions to override default behaviors during specific periods.
    -   Improve scheduling accuracy by calculating travel times based on the agent's start and end locations.
-   **[Sales opportunity in Now Mobile Agent app](https://www.servicenow.com/docs/access?context=create-opportunity&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

Enable field service technicians to perform the following the Now Mobile Agent application.

    -   Create sales opportunities directly from customer locations during field service visits.
    -   Access data to view, search, and filter sales opportunities.
-   **[Dispatcher Workspace](https://www.servicenow.com/docs/access?context=using-dispatcher-workspace&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

Use Dispatcher Workspace to perform the following tasks:

    -   View multiple time zones to see agents who are available for work order tasks across multiple locations.
    -   Receive intelligent guidance about all possible scheduling options for unscheduled tasks. Rank scheduling options based on agent-to-task match percentage, distance, and more.
    -   Hide off-shift agents so dispatchers can focus on who’s available and ready for tasks at that moment.
-   **Beans.ai map integration for bundled tasks**

Optimize routes for bundled tasks with beans.ai.

-   **[Appointment booking enhancements](https://www.servicenow.com/docs/access?context=appointment-booking-administer&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

Use appointment booking enhanced configurations to perform the following tasks:

    -   Book appointments for work order tasks.
    -   Enable the system to calculate or skip lead time when rescheduling appointments, depending on the selected configuration.
    -   Consider holidays when calculating lead time for appointments.
-   **[Field Service Marketplace enhancements](https://www.servicenow.com/docs/access?context=fsm-marketplace&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**
    -   Automate the process of pushing tasks to the marketplace, automatically creating marketplace requests, and listing eligible contractors as determined by your specified criteria.
    -   Set up task filters to identify the work order tasks that qualify for the marketplace.
    -   Incrementally push marketplace requests to eligible contractors based on their ranking using the **Progressive push** check box.
    -   Evaluate contractor responses and automatically assign tasks to the lowest-cost contractor using the **Response evaluation flow** field.
-   **[Field Service Quality Management](https://www.servicenow.com/docs/access?context=quality-management-fsm&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

Use Field Service Quality Management to do the following tasks:

    -   Review the quality and data from work order tasks before completion.
    -   Address work orders that have been reviewed and sent back for more information.
    -   Provide feedback to technicians and communicate as needed during the review process.
-   **[Workforce enhancements](https://www.servicenow.com/docs/access?context=using-manager-workforce&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

Use Workforce enhanced configurations to perform the following tasks:

    -   Extend access across all personas, allowing every user regardless of their role to view their own calendars.
    -   Configure settings to enable group and territory calendar visibility, authoring agents to view the list and calendars of members in their group or within their territory when Workforce Optimization for Field Service isn't enabled.
    -   Enable agents to create personal events for themselves.
-   **[Multiple Work Configurations](https://www.servicenow.com/docs/access?context=configuring-work-configs&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

Create configurations for multiple work types, such as Installation, Repair, Break fix, and Maintenance.

    -   Set up work configurations for different work types ensuring that relevant work types and flows appear for specified business units or departments.
    -   Create Service Management configurations \(SM Configs\) to support multiple workflows.
    -   Extend the work order task table to account for different work types.

</td></tr><tr><td>

Field Service Management for Telecommunication

</td><td>

-   **[Managing the appointments for telecommunication services](https://www.servicenow.com/docs/access?context=manage-appointment-telecommunication-service&version=xanadu&pubname=xanadu-telecom-media-technology&ft:locale=en-US)**

Create, reschedule, get, list, and cancel appointments from your system for the connectivity-related field services. You can book an appointment on an existing work order in the Field Service Management application from an external system using Appointment Open APIs.


</td></tr><tr><td>

Financial Services Card Operations

</td><td>

-   **[Playbook enhancements for dispute](https://www.servicenow.com/docs/access?context=dispute-playbook-for-portal&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

These enhancements enable the cardholders to do the following:

    -   Initiate disputes directly through the portal by selecting your financial account and the transactions that you want to dispute.
    -   Simplify the process of initiating and tracking disputes with the user-friendly dispute portal interface.
    -   Collect detailed information about the dispute through a questionnaire on the portal.
    -   Enable cardholders to attach relevant documents to their dispute cases.
    -   Receive real-time updates on your case through the dispute tracker on the portal.
    -   Submit the dispute through the portal to land on a review page, where the agent can review and modify the details for the case as required before submitting it for investigation.
-   **[Card disputes enhancements](https://www.servicenow.com/docs/access?context=dispute-management&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**
    -   Added a common dispute questionnaire table with questions relevant to various card networks for both agents and cardholders.
    -   Moved the reason code field to the card dispute transaction table.
    -   Updated the logic to determine the reason code from the case to the card dispute transaction table.

</td></tr><tr><td>

Financial Services Operations Integration with Visa

</td><td>

-   **[Updated subflows for Visa Resolve Online \(VROL\) 24.2 revision](https://www.servicenow.com/docs/access?context=components-installed-with-the-financial-services-operations-integration-with-visa&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

Updated the following subflows to support the changes in the Visa Resolve Online \(VROL\) \(VROL\) release 24.2 revision:

    -   Look up Case Details
    -   Submit Fraud Report
    -   Update Case Resolution Status

</td></tr><tr><td>

Flows, subflows, and actions in Workflow Studio

</td><td>

-   **[Generate data pill values during flow generation](https://www.servicenow.com/docs/access?context=flow-generation&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Generate appropriate data pill values for supported flow triggers and action inputs.

-   **[Run an action from a conversation](https://www.servicenow.com/docs/access?context=conversational-actions&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Run a Workflow Studio action from a Now Assist conversation. Create and configure the conversational action from Workflow Studio. View and edit conversational actions within Virtual Agent Designer.

-   **[Run a subflow from a conversation](https://www.servicenow.com/docs/access?context=conversational-subflows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Run a Workflow Studio subflow from a Now Assist conversation. Create and configure the conversational skill from Workflow Studio. View and edit conversational subflows within Virtual Agent Designer.

-   **[Reference specific tables with hash tags during flow generation](https://www.servicenow.com/docs/access?context=flow-generation&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Enter a hash tag character in the flow directions to refer to a specific table by name. Use auto-complete to select a table name from the options that match your partial entry.


-   **[Show annotations of the text directions used by flow generation](https://www.servicenow.com/docs/access?context=create-flow-now-assist&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Show annotations of the text directions used for each item added by flow generation. Receive feedback about how your directions map to specific actions, flow logic, and subflows.


-   **[Control what users with read access can see in execution details](https://www.servicenow.com/docs/access?context=user-access-flow-designer&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Grant a user role to control what users with read access can see in execution details. To limit read access to basic execution details only, grant a user the existing fd\_read\_operations role. To allow read access to all execution details, grant a user the new fd\_read\_operations\_all role.

-   **[Sign flows, subflows, and actions](https://www.servicenow.com/docs/access?context=cs-fdih&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

Sign and validate any flow, subflow, or action.


</td></tr><tr><td>

Generative AI Controller

</td><td>

-   **[Metadata log table for generative AI requests](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Use the new metadata log table that includes information about the requesting conversation, the capability definition, provided feedback \(if any\), and error codes.

-   **[Translation for Now Assist](https://www.servicenow.com/docs/access?context=translation-for-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Support users who speak different languages with new language information in LLM request metadata, better controls for Dynamic Translation, and translated text logging.


-   **Global Model selection for conversational skills**

Enable Now Assist Admins to choose between GPT4.o and Now Assist LLM model for data routing at a global level. This ensures compliance with any regional restrictions and helpful for APAC users who may face limitations with US-based models, such as GPT-4.0.


</td></tr><tr><td>

Goal Framework

</td><td>

-   **[Baseline reference on Target form](https://www.servicenow.com/docs/access?context=target-form&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

The **Baseline reference** field has been added to the Target form. You can use this field to compare future target performance to the actual value achieved either in the last year or before the target was created.


</td></tr><tr><td>

Goal Framework for SPM

</td><td>

-   **[Enhanced target breakdowns](https://www.servicenow.com/docs/access?context=target-breakdowns-gf&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Create Daily, Weekly, or Monthly target breakdowns according to how often you want to update and track the progress of the target. The target breakdowns are created based on the value selected in the **Check-in frequency** field. For example, if you select **Monthly** in the **Check-in frequency** field for a target spanning a year, then 12 monthly target breakdowns are created.


</td></tr><tr><td>

HR Service Delivery for Healthcare

</td><td>

-   **[Healthcare Professional data model](https://www.servicenow.com/docs/access?context=hr-hc-profile&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Use the Healthcare Professional data model to store confidential data pertaining to a healthcare professional, such as practice name, medical degree, and practice locations. The Healthcare Professional data model enables the organization to access, track, and update healthcare profile information throughout the period of employment of a healthcare professional. The profile records are stored confidentially and aren't publicly viewable.

-   **[Customize Healthcare Employee Onboarding workflow](https://www.servicenow.com/docs/access?context=customize-journey-hc&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Use the default Healthcare Employee Onboarding workflow in Journey designer to set up and automate the following tasks for a newly hired healthcare professional at a healthcare organization:

    -   Auto-create a profile and email account for the healthcare professional.
    -   Auto-initiate the necessary form intake tasks for the healthcare professional.
    -   Auto-create credentialing and validation tasks for HR agents so the agents can review and validate information submitted by the healthcare professional.

</td></tr><tr><td>

Hardware Asset Management 11.0.0

</td><td>

-   **[Offer assets and asset management services through Device as a Service feature](https://www.servicenow.com/docs/access?context=exploring-daas&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Provide assets and asset management services to the customers of DaaS providers via a subscription model.

-   **[Manage the hardware asset requests by using the Zero Touch request flow](https://www.servicenow.com/docs/access?context=zero-touch-request&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Fulfill the hardware asset requests directly through an external vendor by using the Zero Touch request flow. When an employee submits a request for a hardware catalog item associated with the Zero Touch request flow, the request is sent to the external vendor who ships the asset directly to the employee.

-   **[Manage repair of defective assets in the stockroom by using the Repair flow](https://www.servicenow.com/docs/access?context=requesting-hardware-asset-repair&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Request repair of assets that are defective or pending repair by using the Repair flow, which includes troubleshooting, repair, and evaluation tasks. Repair orders are processed either in the Hardware Asset Workspace or the ServiceNow Mobile Agent application.

-   **[Manage inventory picking within a stockroom](https://www.servicenow.com/docs/access?context=managing-hardware-asset-pickup&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Pick assets in your stockroom easily for sourcing, hardware asset requests, and hardware asset refresh workflows by enabling the Pick task for your stockroom. The task lists the assets that you should pick from the stockroom, with aisle and space details providing the exact location from which the asset should be picked. Indoor mapping capabilities enable you to get directions to the location of the asset in the stockroom on your ServiceNow Mobile Agent application.


</td></tr><tr><td>

Health Log Analytics

</td><td>

-   **[Enjoy a significantly faster log streaming rate with the Lighting gRPC client for MID Server communication with the ServiceNow instance](https://www.servicenow.com/docs/access?context=hla-configuration-preferences&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Increase log streaming speeds to Health Log Analytics by up to six times through the Lightning gRPC client, which enhances MID Server communication with your ServiceNow instance. Note that the Lightning gRPC client requires manual configuration to activate.

-   **[Stream system logs from Glide to Health Log Analytics](https://www.servicenow.com/docs/access?context=hla-data-input-glide-syslog&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Use the Glide Syslog data input to stream log messages from the System Log table \(Glide Syslog\) in Glide to the Health Log Analytics AI engine \(Occultus\).

**Note:** Only a single Glide Syslog data input can exist in the system. This data input doesn't run on a MID Server.


</td></tr><tr><td>

Healthcare and Life Sciences Service Management Core

</td><td>

-   **[Patient identifier table](https://www.servicenow.com/docs/access?context=hcls-patient-identifier-table&version=xanadu&pubname=xanadu-healthcare-life-sciences&ft:locale=en-US)**

Use the new Patient identifier table to maintain and manage multiple identifiers such as patient MRN, social security number, and more.

For instructions on migrating data from the patient table to the patient identifier table, please reach out to [Now Support](https://support.servicenow.com/now) for the fix script.


</td></tr><tr><td>

Hermes Messaging Service

</td><td>

-   **[Monitor Hermes data usage](https://www.servicenow.com/docs/access?context=monitoring-data-usage-hermes&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Monitor data usage by application and track data usage by topic using the Hermes Usage Dashboard.


</td></tr><tr><td>

ITOM AIOps

</td><td>

-   **[Load the allow list only from the configuration file](https://www.servicenow.com/docs/access?context=acc-yml-options&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Enhance your security by loading the allow list from the configuration file and ignoring the allow-list parameters.

-   **[Configure the agent log level from the instance](https://www.servicenow.com/docs/access?context=set-agent-log-level&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Configure the agent log level directly from the ServiceNow® instance without needing to access the `acc.yml` configuration file.

-   **[Ensure secure agent connections](https://www.servicenow.com/docs/access?context=add-certificate-trust-store&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Ensure that your agent connections are secure by adding a self-signed certificate to your operating system's truststore. Adding a certificate to the truststore verifies that the certificate is authentic.

-   **[Use the new application Service Reliability Management](https://www.servicenow.com/docs/access?context=sr-landing-page&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Use the Service Reliability Management application to respond, collaborate, track, and self-remediate when working on alerts and incidents.

-   **[Configure the Dynatrace connector instance](https://www.servicenow.com/docs/access?context=configure-dynatrace-connector&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Starting in version 3.6.3, Event Management supports collecting raw metric data collection using the Dynatrace metric connector.

-   **[Enable expanded processing for the MID server on Network Interface Controllers \(NICs\) during keepalive operation](https://www.servicenow.com/docs/access?context=acc-yml-options&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Starting in version 3.6.3, benefit from enhanced stability when running a keepalive operation. You can use the enhanced MID Server capability to configure the number of Network Interface Controllers \(NICs\) that can be monitored by a keepalive operation.

-   **[Stream log data from the System Log table in Glide to the Health Log Analytics AI engine](https://www.servicenow.com/docs/access?context=hla-data-input-glide-syslog&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Use the Glide Syslog data input to stream log messages from the System Log table \(Glide Syslog\) in Glide to the Health Log Analytics AI engine \(Occultus\).

**Note:** Only a single Glide Syslog data input can exist in the system. This data input doesn't run on a MID Server.

-   **[Enrich automation](https://www.servicenow.com/docs/access?context=enrich-alert-sow-itom&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Map current alert fields values to specified new values through the **Change alert values** option, in the "If these conditions are met, don't add an alert in ServiceNow" section.

-   **[Group automation](https://www.servicenow.com/docs/access?context=group-alert-sow-itom&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Track and optimize alert grouping efficiency through a new header displaying key details from the Test Automation section, including total alerts, alert groups, ungrouped alerts, and compression.

-   **[View data on configuration items on the preview panel in Express List](https://www.servicenow.com/docs/access?context=el-ci-data&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

View additional details about configuration items \(CIs\) that are bound to alerts on the Express List preview panel.

-   **[Speed up alert resolution with a Now Assist analysis of past related incidents](https://www.servicenow.com/docs/access?context=nai-past-incidents&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Enhance efficiency and reduce downtime with a Now Assist analysis of past incidents related to the current alert. Now Assist investigates historical data to identify past incidents related to the current alert and reports their frequency and criticality levels. It also provides a summary of effective strategies used to resolve them. In addition, Now Assist offers contact information for individuals or teams who have resolved similar incidents in the past and could assist when needed.

-   **[Generate an alert group description in Express List using Now Assist](https://www.servicenow.com/docs/access?context=alert-group-descr-generate-el&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Use Now Assist to generate a description of an alert group in Express List that encompasses all the alerts within the group. The generated description replaces the original description of the group.

-   **[Launch an alert analysis from the Now Assist panel](https://www.servicenow.com/docs/access?context=alert-analysis-now-assist-panel&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Analyze an alert from the Now Assist panel. The alert analysis displays directly in the Now Assist panel for convenient review.


</td></tr><tr><td>

ITOM Optimization

</td><td>

-   **[Cloud Provisioning and Governance](https://www.servicenow.com/docs/access?context=cloud-management-v2-landing-page&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) [Cloud Admin Portal](https://www.servicenow.com/docs/access?context=cloud-admin-portal&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Explore the Next Experience dashboard pages that are now available on Cloud Admin Portal.

The Cloud Admin Portal link to the user portal now points to Employee Center if you have installed and set up the [Cloud Services Catalog](https://servicenow.com/docs/csh?topicname=csc-home&version=xanadu&pubname=xanadu-it-operations-management) application.


</td></tr><tr><td>

ITOM Visibility

</td><td>

-   **[Use Discovery Admin Workspace features to jumpstart discovery implementation.](https://www.servicenow.com/docs/access?context=discovery-admin-workspace&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**
    -   View discovery trends and tasks and access relevant ITOM Visibility apps and information through Discovery Admin Workspace Home.
    -   Gain insights into the performance of all your discoveries through the information in the **Schedules** tab.
    -   Analyze discovery errors and troubleshoot them using information in the **Diagnostics** tab.
    -   Access on-demand reports and optimize discovery operations using information in the**Insights** tab.
-   **[Discover products with Discovery and Service Mapping Patterns](https://www.servicenow.com/docs/access?context=r_SupportedApplications&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Discover the following products through Discovery and Service Mapping Patterns:

    -   [Dell EMC Data Domain storage](https://www.servicenow.com/docs/access?context=emc-data-domain-pattern&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).
    -   [Dell EMC PowerMax storage](https://www.servicenow.com/docs/access?context=emc-powermax-discovery-pattern&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).
    -   [AWS services in the China region](https://www.servicenow.com/docs/access?context=data-discovered-aws-patterns&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) - Available with the Discovery and Service Mapping Patterns November 2024 store release \(1.21.0\) on the ServiceNow AI Platform Xanadu Patch 3 instance.
    -   [REST-based Fortinet firewall and FortiGate VDOMs](https://www.servicenow.com/docs/access?context=fortinet-fw-vdoms-rest-discovery&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) - Available with the Discovery and Service Mapping Patterns November 2024 store release \(1.21.0\).
    -   [Azure Marketplace](https://www.servicenow.com/docs/access?context=azure-cloud-discovery-patterns&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) - Available with the Discovery and Service Mapping Patterns November 2024 store release \(1.21.0\). The pattern supports the discovery of the following Azure Marketplace products:
        -   Virtual Machine
        -   SaaS
        -   Azure Application
-   **[Oracle Java process discovery](https://www.servicenow.com/docs/access?context=oracle-glas-discovery&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Discover Java processes to comply with Oracle licensing agreements- Use the ITOM Oracle GLAS plugin \(1.8.4\) November 2024 store version to track Java installations and usage.

-   **[MID Server features for better discovery performance](../now-platform-capabilities/mid-server-rn.md)**
    -   Run other applications without storing any credentials on the instance with the Microsoft Azure Key vault.
    -   MID Server supports log file compression. The new log file handler settings are available as MID Server properties on the instance. The compression mode isn't enabled out of the box.
-   **[Use CMDB based mapping to create new application services](https://www.servicenow.com/docs/access?context=cmdb-based-mapping&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Use Automated Service Suggestions and CMDB data instead of the MID Server, to create new application services.

-   **[Use the latest CNO for Visibility features](https://www.servicenow.com/docs/access?context=cnov-configuring&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Starting in version 3.6.3, benefit from new features in Cloud Native Operations for Visibility.

    -   Upgrade the CNO for Visibility Informer from the ServiceNow instance.
    -   Control Informer execution parameters from the instance.
    -   Store instance credentials in the Microsoft Azure Vault when Informer uses the Azure Kubernetes Engine \(AKS\)
    -   Enable Informer to connect to the instance using OAuth2.0 authorization
-   **[Enjoy multi-architecture support for docker image](https://www.servicenow.com/docs/access?context=cnov-deploy-prepare&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Starting in version 3.9.0 \(Informer version 2.3.0\), the docker image supports both arm64 and amd64 architectures. Upgrading from the previous image to the new one will not cause any disruptions. However, the new image requires more storage space in your image repository than the previous one.

-   **[Change the Informer's extensibility settings from the instance](https://www.servicenow.com/docs/access?context=cnov-params-override&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Starting in version 3.9.0 \(Informer version 2.3.0\), update the Informer's extensibility configuration directly from the Instance using the **Additional resources ConfigMap** parameter. By providing a JSON map with keys such as `resources`, `mappings`, and `mappings_oob`, you can instruct Cloud Native Operations for Visibility to retrieve additional information. If one of these keys exists and the system finds a change, it patches the ConfigMap and restarts the Informer.

-   **[View the OpenShift version in the Cluster version field on the Kubernetes Cluster CI](https://www.servicenow.com/docs/access?context=cnov-deploy-install&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Starting in version 3.9.0 \(Informer version 2.3.0\), see the OpenShift version and the Kubernetes Cluster version in one place. OpenShift operates on top of Kubernetes, so there's an OpenShift version and a Kubernetes Cluster version. By installing the Informer with the **--set openShift=true** flag, the system adds the OpenShift version number to the **cluster\_version** field on the Kubernetes Cluster CI in addition to the Kubernetes Cluster version.

-   **[Use Service Fingerprints to refine the selection of application service candidates](https://www.servicenow.com/docs/access?context=auto-serv-suggest&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Explore unique, classified components of application service candidates provided by Automated Service Suggestions. By supplying specific information such as the product name and description, gain deeper insights into the most suitable candidate to convert to an application service.


</td></tr><tr><td>

ITSM Success Dashboard

</td><td>

-   The new Self-solved using AI Search QnA and Self-solved using Now Assist Search QnA KPIs are added to the self-solved deflections. These new contributing indicators assist users to resolve their digital issues using AI Search and the Now LLM Service.
-   The ITSM Self-solved using Proactive Engagement for DEX indicator is added to self-solve deflection where employees self-solve their digital experience issues by leveraging the proactive issue detection and resolution capability of the ServiceNow® Digital End-user Experience product.
-   Experience the new KPIs introduced in the On-call dashboard to help track the acknowledged escalations encountered by the users on a daily basis.
-   Access all the change success score related metrics categorized under the **Change Success Score** tab in the new Change Management Dashboard.

</td></tr><tr><td>

Identity

</td><td>

-   **Access Insights**

Use the Access Insights module in the ServiceNow® Access Analyzer V4 tool to get access insights about role or group entitlements assinged to the user at a peer-level \(same organization, department, and Manager\), while comparing the user access.

**Important:** Access Insights \(Access Analyzer V4\) is available in the ServiceNow Store. For more information, visit ServiceNow Store.

-   **SCIM**

Use the System for Cross-domain Identity Management \(SCIM\) API endpoints to create, read, update, and delete operations on users and groups using the SCIM protocol.


</td></tr><tr><td>

Impact

</td><td>

-   **[Initiatives &amp; Accelerators](https://www.servicenow.com/docs/access?context=impact-initiatives&version=xanadu&pubname=xanadu-impact&ft:locale=en-US)**
    -   [Jumpstart Your Now Assist for Creator](https://www.servicenow.com/docs/access?context=jumpstart-now-assist-creator&version=xanadu&pubname=xanadu-impact&ft:locale=en-US) and SPP-AU version
    -   [Jumpstart Your Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=jumpstart-now-assist-itsm&version=xanadu&pubname=xanadu-impact&ft:locale=en-US) and SPP-AU version
    -   [Jumpstart Your Service Mapping](https://www.servicenow.com/docs/access?context=jumpstart-service-mapping&version=xanadu&pubname=xanadu-impact&ft:locale=en-US) and SPP-AU version
    -   [Jumpstart Your Database Management](https://www.servicenow.com/docs/access?context=data-management&version=xanadu&pubname=xanadu-impact&ft:locale=en-US)
    -   [Jumpstart Your CSM Configurable Workspace](https://www.servicenow.com/docs/access?context=csm-configurable-workspace&version=xanadu&pubname=xanadu-impact&ft:locale=en-US)
    -   [TuneUp Your Employee Center](https://www.servicenow.com/docs/access?context=tuneup-employee-center&version=xanadu&pubname=xanadu-impact&ft:locale=en-US)
    -   [Introduction to Instance Readiness Assessment](https://www.servicenow.com/docs/access?context=introduction-instance-readiness-assessment&version=xanadu&pubname=xanadu-impact&ft:locale=en-US)
    -   [CoEI Influencing Funding Strategy](https://www.servicenow.com/docs/access?context=coei-influencing-factor-assessment-part-2&version=xanadu&pubname=xanadu-impact&ft:locale=en-US)
    -   [UX: Catalog Request Experience Review](https://www.servicenow.com/docs/access?context=ux-accelerator-service-request-experience-review&version=xanadu&pubname=xanadu-impact&ft:locale=en-US)
    -   [Generative AI - Virtual Agent Conversational Catalog](https://www.servicenow.com/docs/access?context=generative-ai-conversational-catalog&version=xanadu&pubname=xanadu-impact&ft:locale=en-US)
    -   [Value Potential](https://www.servicenow.com/docs/access?context=value-potential-undeployed-apps&version=xanadu&pubname=xanadu-impact&ft:locale=en-US)
-   **[Initiatives &amp; Accelerators](https://www.servicenow.com/docs/access?context=impact-initiatives&version=xanadu&pubname=xanadu-impact&ft:locale=en-US)**
    -   [Extend Your Employee Center to Pro](https://www.servicenow.com/docs/access?context=extend-employee-center-pro&version=xanadu&pubname=xanadu-impact&ft:locale=en-US): Provides prescriptive guidance on extending the Employee Center capabilities to include Pro features.
    -   [Jumpstart Your CSDM: Foundation](https://www.servicenow.com/docs/access?context=jumpstart-csdm&version=xanadu&pubname=xanadu-impact&ft:locale=en-US): Provides an overview and breakdown of the CSDM with a focus on Foundation data.
    -   [Jumpstart Your Document Intelligence](https://www.servicenow.com/docs/access?context=jumpstart-document-intelligence&version=xanadu&pubname=xanadu-impact&ft:locale=en-US): Provides a demonstration of the possibilities and capabilities of Document Intelligence.
    -   [Jumpstart Your Employee Center](https://www.servicenow.com/docs/access?context=jumpstart-employee-center&version=xanadu&pubname=xanadu-impact&ft:locale=en-US): Includes a demonstration of the possibilities and capabilities available with the ServiceNow Employee Center portal in your instance.
    -   [Jumpstart Your Event Management](https://www.servicenow.com/docs/access?context=jumpstart-event-mgmt&version=xanadu&pubname=xanadu-impact&ft:locale=en-US): Provides a demonstration of the possibilities and capabilities of Event Management.
    -   [Jumpstart Your Issue Auto Resolution](https://www.servicenow.com/docs/access?context=jumpstart-issue-auto-resolution&version=xanadu&pubname=xanadu-impact&ft:locale=en-US): Provides a demonstration of the possibilities and capabilities of Issue Auto Resolution within your ServiceNow platform.
    -   [Jumpstart Your Process Mining](https://www.servicenow.com/docs/access?context=jumpstart-process-mining&version=xanadu&pubname=xanadu-impact&ft:locale=en-US): Provides a demonstration of the possibilities and capabilities of Process Mining.
    -   [UX: Taxonomy Review and Design](https://www.servicenow.com/docs/access?context=ux_review_unified_taxonomy&version=xanadu&pubname=xanadu-impact&ft:locale=en-US): Optimizes content structure and navigation in your portal, with a focus on Knowledge and Catalog to improve usability and help users easily find the correct information.
    -   [Common Service Data Model \(CSDM\) Assessment - Business Services \(Run\) - Advanced](https://www.servicenow.com/docs/access?context=csdm_assessment_business_services&version=xanadu&pubname=xanadu-impact&ft:locale=en-US): Provides an assessment and guidance for CSDM Run maturity, including Business Services, Business Service Offerings, Request Catalog Items, and \(Business\) Service Portfolio.
    -   [Common Service Data Model \(CSDM\) Assessment Technical Services \(Walk\) - Advanced](https://www.servicenow.com/docs/access?context=csdm_assessment_technical_services&version=xanadu&pubname=xanadu-impact&ft:locale=en-US): Provides an assessment and guidance for CSDM Walk maturity, including Technical Services and Technical Service Offerings.
    -   ServiceNow Protected Platform – Australia \(SPP-AU\) versions of Accelerators are available, where applicable. The [Accelerator catalog](https://www.servicenow.com/docs/access?context=accelerator-catalog&version=xanadu&pubname=xanadu-impact&ft:locale=en-US) is updated with this information.
-   **[HealthScan](https://www.servicenow.com/docs/access?context=healthscan&version=xanadu&pubname=xanadu-impact&ft:locale=en-US)**
    -   Consent for the self-service capability that automates monthly Health Assessment scans and reports to provide details that can help you to improve the health of your ServiceNow platform implementation.
    -   Consume HealthScan service environment script outputs in a clear format for Self-hosted NSG Air-gapped customers.
    -   Access HealthScan commercial features as a GCC or NSC customer.
-   **[Value Journey](https://www.servicenow.com/docs/access?context=impact-value-journey&version=xanadu&pubname=xanadu-impact&ft:locale=en-US)**
    -   Use the auto generated objectives and outcomes to save time and effort in the Impact Value Journey.
    -   View monthly or quarterly trends and curated recommendations for generated outcomes. See Trends, Benchmarks, and recommendations related to the outcome.
    -   Trends and Benchmarks will be available for outcomes with data.
    -   Use the Data Collection App, available from the ServiceNow® Store, to transfer data automatically into your Impact portal.
-   **[Impact Instance Observer](https://www.servicenow.com/docs/access?context=io-overview&version=xanadu&pubname=xanadu-impact&ft:locale=en-US)**
    -   Detect additional anomalies for 16 metrics with Release 18.
    -   Configure self-serve alerts for Garbage Collection using Host Health.

</td></tr><tr><td>

Individual Life Claims

</td><td>

-   **[Individual Life Claims application](https://www.servicenow.com/docs/access?context=individual-life-claims-landing-page&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

Record key details at FNOL, verify documents, and manage the tasks for the primary claim and related claims.

-   **[Claims data model](https://www.servicenow.com/docs/access?context=insurance-claims-core-data-model&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

Build a claims flow for individual benefits such as long-term care, disability, critical illness, and so on.

-   **[Customized playbook experience for FNOL](https://www.servicenow.com/docs/access?context=create-an-individual-life-claim-case&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

Use a customized playbook to complete the FNOL process with step-by-step guidance to verify that every task gets completed at the correct stage of the process.

-   **[New adjuster workspace](https://www.servicenow.com/docs/access?context=individual-life-claim-adjuster-tasks&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

Resolve issues, complete tasks, and manage reserves and payments across multiple policies for individual life claims in a new workspace.

-   **[Death benefit workflow](https://www.servicenow.com/docs/access?context=individual-life-claims-workflows&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

Use the included death benefit claim workflow as an example to start building your own workflow.

-   **[Approval engine for reserves and payments](https://www.servicenow.com/docs/access?context=approve-reserve-or-payment-amount&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

Route requests to managers to approve reserves or payments that are above an adjuster's authorized limit.


</td></tr><tr><td>

Industrial Process Manager

</td><td>

-   **[Capture the mapped equipment model entity for your OT devices](https://www.servicenow.com/docs/access?context=view-all-mapped-ot-devices&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Organize your OT device data efficiently by adding the primary equipment model entity for your OT devices. You can also automatically update the primary equipment model entity for your existing devices.

-   **[Use the Unified Map experience in the Industrial Workspace](https://www.servicenow.com/docs/access?context=unified-maps-experience-iw&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

View the relationships between OT devices and other CIs with the Unified Map experience. You can also view related items, such as OT incidents and change requests.

-   **[Map discovery detected devices using the Automated Mapping Across Zone-based IP Network Groups \(AMAZING\) feature](https://www.servicenow.com/docs/access?context=automatedly-map-all-ot-assets&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Map Discovery detected devices that have an IP address on their Network Adapter record using the AMAZING feature.

-   **[Add OT devices to an equipment model entity by IP address](https://www.servicenow.com/docs/access?context=view-ot-assets-equipment-model-entity&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

When you manually add OT devices to the Mapped OT Devices related list in the Equipment Model Manager on the Industrial Workspace, you can add an OT device by its IP address.

-   **[Update the entity name or parent of an equipment model entity](https://www.servicenow.com/docs/access?context=update-the-name-or-parent-equipment-model-entity&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Update the **Entity name** or **Parent** fields in an equipment model entity record as needed to help keep your equipment model information up to date.


</td></tr><tr><td>

Insurance claims

</td><td>

-   **[Set up new lines of business easily](https://www.servicenow.com/docs/access?context=setting-up-insurance-claims-flow&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

Leverage the Insurance claims framework to configure a new line of business for one or more incidents.

-   **[Customize your claims workflow](https://www.servicenow.com/docs/access?context=claim-incident-configuration-table&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

Configure which incidents to display for claim intake, depending on the line of business. Define how adjuster tasks are created based on the selected incidents, and enable or disable itemized loss and expenses as part of the flow.

-   **[Set up persona-based claims workspaces](https://www.servicenow.com/docs/access?context=insurance-claims-flow-workspace&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

Set up workspaces for each persona that can be easily customized without requiring code changes.

-   **[Refer to the travel insurance example](https://www.servicenow.com/docs/access?context=using-insurance-claims-flow&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

Refer to the included travel insurance line-of-business example to review the incident intake and resolution workflow.


</td></tr><tr><td>

Integration Hub

</td><td>

-   **Now Assist in Conversational Spokes**

Use Now Assist in Conversational Spokes to utilize the conversational ability of Integration Hub Spoke actions. Now Assist in Conversational Spokes offers generative AI capabilities to make spoke actions conversational. With this, you can perform business actions and automate business workflows through conversational interface.

Install Now Assist for Conversational Spokes plugin and start utilizing the conversational ability of the Look up User spoke action in Microsoft Active Directory v2 spoke. You can call this action from a conversational interface like Now Assist.


-   **[Send and receive messages in an Avro format with Stream Connect](https://www.servicenow.com/docs/access?context=schema-management&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

Import and create Avro schemas to store in the Stream Connect Schemas \[stream\_connect\_schema\] table. Stream Connect producers and consumers use the schemas to convert plain-text JSON messages into an Avro binary format and back. Using an Avro format can reduce the size of the payload and simplify your integration to your local Apache Kafka instance.

-   **[Track incoming requests for SOAP and REST APIs, and URL Export](https://www.servicenow.com/docs/access?context=integrationhub-usage-dashboard&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

View the data egress details in the enhanced Usage dashboard. Using the dashboard, you can track the data egress usage per source over time. This information is presented in a line chart and, if needed, you can view the amount of data transfer by source on any given date within the specified date range. The dashboard retrieves data from the Data Egress Count table \[data\_egress\_count\].

-   **[Enable parallel loading in custom \(load by script\) type data sources](https://www.servicenow.com/docs/access?context=custom-type-data-source&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

Use a script to partition data into smaller sections, then load the sections in parallel. Parallel loading can enable your integrations to finish faster and reduce the impact on other tasks.

-   **[CyberArk credential storage integration](https://www.servicenow.com/docs/access?context=c_CyberArkCredStorageIntegrate&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) Use the CyberArk Digital Vault to store and access your OAuth 2.0 credentials**

Use the ServiceNow® MID Server to access your OAuth 2.0 credentials stored on the CyberArk Digital Vault. The MID Server uses this information to generate OAuth 2.0 tokens for client credentials grant type that are then used to make REST API calls to the third-party server.

-   **[Make outbound REST and SOAP calls through a MID Server using mTLS](https://www.servicenow.com/docs/access?context=mtls-mid-server&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

Store mTLS password and certificate information on the instance, in a vault, or in a configuration file. The MID Server uses this information to make outbound REST and SOAP calls with the mTLS protocol.

-   **[Use the Personal Authentication dashboard](https://www.servicenow.com/docs/access?context=personal-auth-dashboard&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

Use your personal credentials to connect to third-party integrations. View, authenticate, revoke, and renew your personal authentications through a simplified, consolidated interface.

-   **[Enhancements to the external trigger endpoints](https://www.servicenow.com/docs/access?context=generate-endpt-oauth2&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

Generate an endpoint for webhooks in the third-party applications that support [OAuth 2.0 authentication](https://www.servicenow.com/docs/access?context=generate-endpt-oauth2&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US). The endpoint enables webhooks to connect with your ServiceNow instance.

Generate the endpoints by updating the base system external event sources on your ServiceNow instance. After that, you can configure the endpoint on the third-party application and enable it to send a webhook to the ServiceNow instance to execute a flow. Based on the authentication type that the third-party system supports, you can generate a hash, secret, or token, or add roles or a user to the external event source. Finally, you generate the endpoint that you can use on the third-party system webhook.

-   **[Automatically generate a JSON payload for the JSON Builder step](https://www.servicenow.com/docs/access?context=json-build-step-action-designer&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

Enter a JSON payload into the step's script editor to automatically de-serialize the payload into structured input.

-   **[Enhanced OpenAPI step](https://www.servicenow.com/docs/access?context=open-api-step-action-designer&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

Choose to import an OpenAPI specification or a Postman Collection of a third-party outbound REST web service for building an integration. The OpenAPI step is now enhanced to support Postman API collections and is renamed as **OpenAPI/Postman step**.


</td></tr><tr><td>

Intelligence for CSM

</td><td>

-   **[Recommended Actions - Task Intelligence similarity models integration](https://www.servicenow.com/docs/access?context=ra-csm-resource-generators&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Use similarity models that are integrated with the Task Intelligence \(TI\) admin console to configure, train, and deploy machine learning models.

    -   Resource Generator: The Recommended Actions framework supports a new resource generator that leverages TI similarity models to configure recommendations.
    -   Admin Configuration: Administrators can configure the resource generator to point to TI solutions for predictions and use the topN optional parameter to fetch top recommendations.
-   **Task intelligence for Customer Service - Dependent field predictions**

Help improve the model performance by identifying the dependent fields in a model before displaying the predicted values.

-   **[Task intelligence for Customer Service - Records prediction](https://www.servicenow.com/docs/access?context=view-prediction-on-field-change&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Predict the configured fields on the case record after entering the short description or description and see the predicted values without saving the case form.

-   **[Task intelligence for Customer Service - On change predictions for interaction record](https://www.servicenow.com/docs/access?context=view-prediction-on-field-change&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Predict the configured fields on the interaction record after entering the short description or description and see the predicted values without saving the form.

-   **[Task Intelligence for Customer Service - Implement Task Intelligence for the CSM Similarity Model:](https://www.servicenow.com/docs/access?context=view-similar-case-recommendations&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**
    -   Similar cases recommendations:  Install the Task Intelligence for Customer Service plugin to view the preconfigured open and closed cases that are automatically trained and deployed as recommendations.
    -   Major case recommendations: Install the major issue management plugin and activate the feature as needed to get recommendations.
-   **[Recommended Actions - Create multiple contexts for a single record entity](https://www.servicenow.com/docs/access?context=ra-csm-contexts&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Support multiple contexts for the same table, such as the Case table, with one active context record that can be configured for the Recommended Actions component by using a UI Builder input property. By creating multiple contexts, you can create different experiences that are determined by criteria such as user attributes or domains. The recommendations and AI Search results adjust dynamically according to the configured active context.

-   **[Recommended Actions - Attach knowledge article guidance](https://www.servicenow.com/docs/access?context=ra-csm-guidances&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US#section_jgl_1lv_bdc)**

Enable agents to view and attach knowledge articles to task records and chat interaction records and share articles with customers by using the following guidances:

    -   Attach and share article: Enables the agent to share a recommended knowledge article in a comment, work note, or an email.
    -   Share article in chat interaction: Enables the agent to share a recommended knowledge article in a customer chat.
-   **[Guided Decisions - Run a guidance as a system user](https://www.servicenow.com/docs/access?context=components-installed-with-guided-decisions&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Enable the **guidance\_honor\_subflow** system property to run a guidance in a decision tree as the user that is specified in the guidance action subflow properties. If this property is set to false, the guidance runs as the current user.

-   **[Guided Decisions - Decision Tree as a catalog item content type](https://www.servicenow.com/docs/access?context=service-def-config-catalog-items&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Enable customers to add decision trees as catalog items in a service catalog. From the Customer Service Portal, customers can select the decision tree and open it in a new tab.

-   **[Guided Decisions - Search for decision trees on portal](https://www.servicenow.com/docs/access?context=search-service-portal&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

Enable portal users to search for decision trees with keywords. Selecting a decision tree in the search results opens a page with the decision tree widget.

-   **[Guided Decisions - Enable a start node to contain only task input](https://www.servicenow.com/docs/access?context=guided-decision-tree-node-types&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Create start nodes for a decision tree that start directly from a task input and create paths that are derived from the data in the task reference. You have the option to create a start node from a question or from task input.

-   **[Guided Decisions - Restart a decision tree in a playbook](https://www.servicenow.com/docs/access?context=add-guided-decision-playbook&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Restart the execution of a decision tree. When a user completes the execution of a decision tree in a playbook, they can start and complete the decision tree again if desired. Restarting the playbook retains the history of the previous decision tree executions.


</td></tr><tr><td>

Journey designer

</td><td>

-   **[Support a change of manager](https://www.servicenow.com/docs/access?context=jny-dsgnr-jrny-config-fields&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Enable journeys to support a change of manager.

-   **Base instance demo data of Journey designer to support multiple journeys**

Leverage the parental leave guide shipped as part of Parental Leave demo data to enhance the employee experience.

-   **[Return to the Journey details page after a task is completed](https://www.servicenow.com/docs/access?context=jny-dsgnr-employee-journey-tasks&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Navigate back to the Journey details page after task completion, avoiding the need to go through the breadcrumbs.

-   **[Delete subsequent tasks when a journey is deleted](https://www.servicenow.com/docs/access?context=jny-dsgnr-mngr-mntr-quick-links&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Delete a journey and all the subsequent tasks at the same time.


</td></tr><tr><td>

Knowledge Management

</td><td>

-   **[New report on Knowledge Management dashboard](https://www.servicenow.com/docs/access?context=km-overview-dash&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Make timely decisions on articles expiring in the next 90 days through a report on the Knowledge Management dashboard and determine whether to retire or republish them.


-   **[Now Assist in Knowledge article generation from multiple cases](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-coreui&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Quickly draft knowledge articles from your workspace or classic environment based on similar cases with  Now Assist. Knowledge articles can be generated by selecting a list of similar cases or case numbers or even by searching keywords specific to a case.


-   **[Generate a Knowledge article using multi-language support](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-using-multilanguage-support&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Generate articles for an incident, case, or other supported task type in a language other than English by setting up language options for knowledge article generation in Now Assist.


-   **[Edit an article using the Now Assist context menu](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-using-context-menu&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Rewrite selected parts of a Knowledge article based on context by deploying the Now Assist context menu.


</td></tr><tr><td>

Lead Management

</td><td>

-   **[Create a lead](https://www.servicenow.com/docs/access?context=create-new-lead&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

Create and manage your leads for potential sales opportunities.

-   **[Needs analysis using lead workspace](https://www.servicenow.com/docs/access?context=lead-management-use-needs-analysis&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

Understand your lead's needs through questionnaires, and recommend and capture the product offering through lead line items.

-   **[Manage leads using Kanban view](https://www.servicenow.com/docs/access?context=lead-management-use-kanban-view&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

Quickly assess the status of your various leads by navigating and visualizing these leads across different stages with the help of a Kanban board that shows a card-based view of your leads.

-   **[Nurture leads and track lead activities](https://www.servicenow.com/docs/access?context=lead-management-use-emails-tab&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

Compose emails, create tasks, and schedule appointments to nurture leads by tracking the interest and need analyses of your leads.

-   **[Convert leads to opportunities](https://www.servicenow.com/docs/access?context=lead-management-use-convert-lead&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

Qualify leads by creating opportunities for new and existing contacts.


</td></tr><tr><td>

Leader Hub

</td><td>

-   **[At a glance](https://www.servicenow.com/docs/access?context=td-lh-explore&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Supply your organizational and HR leaders with instant access to a comprehensive overview of their organization's talent via the At a glance page. This page is the home page for Leader Hub and it offers a glance at data that measures employee engagement and skill proficiency, along with a glimpse of the teams that comprise your organization. The At a glance page gives leaders quick and easy access to the following information about the teams in their organization:

    -   Skill scores
    -   Significant skill gaps
    -   Employee engagement with the growth tools available in the Talent Development suite of applications.
Leaders can access the At a glance page by selecting **At a glance** from the Leader hub drop-down list.

-   **[Org talent](https://www.servicenow.com/docs/access?context=td-lh-explore&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Provide your leaders with a centralized location to view the talents of each team that exists within their organization via the Org talent page. Leaders can view talent data at any level of granularity through an interactive organizational chart that illustrates the structure of their organization and the reporting relationships between managers and employees for each team in their organization.

Leaders can access the Org talent page by selecting **Org talent** from the Leader hub drop-down list.

-   **[Org skills](https://www.servicenow.com/docs/access?context=td-lh-explore&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Equip your leaders with the tools to understand the skill composition of their organization via the Org skills page. The Org skills page displays skills relevant to your leader's organization and provides metrics that leaders can use to identify critical skill gaps and hold managers responsible for developing talent within their teams. Leaders can further examine the details associated with each skill by selecting the name of the skill that they want to view to access the Skill details page.

Leaders can access the Org skills page by selecting **Org skills** from the Leader hub drop-down list.

-   **[Orgs you support](https://www.servicenow.com/docs/access?context=td-lh-explore&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Give organizational supporters insights into their leader's workforce via the Orgs you support page. Supporters entrusted with delegated responsibilities can be designated by their leaders to access Leader Hub so they can provide support in the capacity required for the organization to succeed.

Supporters can access the Orgs you support page by selecting **Orgs you support** on the mega menu from the Employee Center portal.

-   **[Quick start tests for Leader Hub](https://www.servicenow.com/docs/access?context=quick-start-tests-leader-hub&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Leader Hub still works. If you customized Leader Hub, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

MID Server

</td><td>

-   **[MID Server support for Azure Key vault](https://www.servicenow.com/docs/access?context=mid-azure-key-vault-integration&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

The MID Server integration with the Azure Key vault enables Orchestration, Discovery, and Service Mapping to run without storing any credentials on the instance.


</td></tr><tr><td>

Manufacturing Commercial Operations

</td><td>

-   **[Automate the order exceptions management process with Manufacturing Commercial Operations Exception and Dispute Management](https://www.servicenow.com/docs/access?context=manufacturing-edm-exploring&version=xanadu&pubname=xanadu-manufacturing&ft:locale=en-US)**

Streamline operational tasks by using the order exceptions case type. Enable greater visibility and traceability into cases and order exceptions by capturing all the change requests for orders and order line items in a consolidated case with case lines. Manage and track the progress by creating case tasks for other team members or assign case lines to other agents.

-   **[Create a sales contract from customer-approved quotes with integration with CM Pro](https://www.servicenow.com/docs/access?context=manufacturing-cso-exploring&version=xanadu&pubname=xanadu-manufacturing&ft:locale=en-US)**

Automate the process of creating contracts from customer-approved quotes, improve data accuracy, and streamline dispute resolution by allocating responsibilities between parties.


</td></tr><tr><td>

Microsoft Azure DevOps Integration for Agile Development

</td><td>

-   **[OAuth authentication for integration setup](https://www.servicenow.com/docs/access?context=setting-up-agile-azure-integration&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Enhance security for integrations using OAuth authentication while setting up the integration between Azure DevOps and Agile Development 2.0.


</td></tr><tr><td>

Mobile Platform

</td><td>

-   **Now Assist for Mobile Agent app**

Use the power of generative AI in the Mobile Agent app to summarize records and complete tasks more efficiently. Users can create a condensed summary of work order tasks or generate resolution notes.

-   **[User criteria permissions](https://www.servicenow.com/docs/access?context=roles-user-criteria&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US)**

Control the visibility of different areas of the mobile platform by defining user criteria permissions. User criteria permissions, unlike the user roles permissions, enable you to segment your users into different groups, like location, department, or company. With user criteria permissions, you can change information within a single area of a group to update all users' details associated within that group. For example, a company relocates, and the management requires that users in the new location have access to different mobile content. Admins can update the user criteria permissions, so that this new content is displayed to all users in this group.

-   **[Mobile App Builder](https://www.servicenow.com/docs/access?context=mab-concept&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US)**
    -   Support for all Mobile Platform Xanadu features.
    -   Component recommendations by Now Assist across many records.

</td></tr><tr><td>

Next Experience

</td><td>

-   **[Next Experience keyboard shortcuts](https://www.servicenow.com/docs/access?context=next-experience-keyboard-shortcuts&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

Use a new keyboard shortcut to reduce the time required to open the OpenFrame window.

-   **[User experience user preference group added](https://www.servicenow.com/docs/access?context=set-up-preferences-next-experience&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

A new "User experience" user preference group has been added for the Turn off Next Experience, Enable analytics, and Current start page preferences.

-   **[Pin your notifications menu](https://www.servicenow.com/docs/access?context=using-the-next-experience-global-header&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

Pin your notifications menu for quick access to important updates.

-   **[View Next Experience performance metrics](https://www.servicenow.com/docs/access?context=measuring-performance-next-experience&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

View performance metrics for any Next Experience page.

-   **[Preserve your custom Next Experience theme during a clone](https://www.servicenow.com/docs/access?context=preserve-next-experience-theme-during-clone&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

Cloning is optimized to preserve your Next Experience and Theme Builder themes. This helps ensure that the themes are not overwritten during the cloning process.


</td></tr><tr><td>

Next Experience Components

</td><td>

|Component|Description|
|---------|-----------|
|Custom illustration|Insert theme-able, inline Scalable Vector Graphics \(SVG\)s on a Workspace page.|
|Feedback|Capture granular user feedback for AI products through a series of pre-determined options or free-text responses.|

</td></tr><tr><td>

Next Experience Developer \(NED\) Tools

</td><td>

-   **[Health indicators in the Next Experience Inspector](https://developer.servicenow.com/dev.do#!/reference/next-experience/washingtondc/developer-tools/inspector-tab/home)**

The Home view provides information and communicates potential issues on the page through a dashboard of health indicators for components and actions.

-   **[View traces in the Next Experience Inspector](https://developer.servicenow.com/dev.do#!/reference/next-experience/washingtondc/developer-tools/inspector-tab/trace)**

The Trace view provides a waterfall of calls made to the page with information on how the duration for each call.

-   **[Server-side logs in the Logs tab for Next Experience Inspector](https://developer.servicenow.com/dev.do#!/reference/next-experience/washingtondc/developer-tools/inspector-tab/logs)**

Record and view backend data by changing your preference from client logs to server logs when you're logged in as an admin.

-   **[Manage events in the Next Experience Inspector](https://developer.servicenow.com/dev.do#!/reference/next-experience/washingtondc/developer-tools/inspector-tab/events)**

The Events view provides contextual information and actions for managing events.

-   **[Service workers tab in the Next Experience Inspector](https://developer.servicenow.com/dev.do#!/reference/next-experience/washingtondc/developer-tools/inspector-tab/service-workers)**

The Service workers tab provides visibility into service worker behavior.


</td></tr><tr><td>

Notifications

</td><td>

-   **[Sensitive data redaction](https://www.servicenow.com/docs/access?context=sensitive-data-redaction&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Redact sensitive data for inbound emails.

-   **International characters support**

Support added for International characters in the email addresses.


</td></tr><tr><td>

Now Assist

</td><td>

-   **[Now Assist Readiness Evaluation](https://www.servicenow.com/docs/access?context=now-assist-readiness-evaluation-landing-page&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Use the Now Assist Readiness Evaluation app to help you evaluate your organization's readiness to implement agentic and generative AI Now Assist capabilities.

Assessments for agentic AI include:

    -   IT Service Management \(ITSM\)
    -   Customer Service Management \(CSM\)
Assessments for generative AI include:

    -   AI Search
    -   Virtual Agent \(VA\)
    -   IT Service Management \(ITSM\)
    -   Customer Service Management \(CSM\)
    -   HR Service Delivery \(HRSD\)
Results shown are estimates. You should evaluate results provided by Now Assist Readiness Evaluation for accuracy and appropriateness for your use case.


-   **[Now Assist Guardian adds guardrails to log, block, and redirect unwanted content](https://www.servicenow.com/docs/access?context=now-assist-guardian&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Protect your users from offensive content, certain kinds of prompt injection attacks, and sensitive topics by logging attempts, blocking content, or redirecting to a new Virtual Agent topic.

-   **[Translation for Now Assist with native translation](https://www.servicenow.com/docs/access?context=translation-for-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Use the native translation capabilities of the Now LLM Service models or to translate user-generated and LLM-generated content into the preferred languages of your users.

-   **[Troubleshoot a Now Assist skill](https://www.servicenow.com/docs/access?context=troubleshoot-a-now-assist-skill&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Run diagnostics on certain Now Assist skills to identify common configuration errors that help to prevent your skills from working as intended.

-   **[Analyze Now Assist performance](https://www.servicenow.com/docs/access?context=now-assist-analytics&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Use the Now Assist Analytics dashboard to monitor the usage and performance of generative AI features and capabilities offered under Now Assist.

-   **[Configure and use a retriever with Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=add-retriever&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Augment and add context to your prompts with AI Search results from custom retriever inputs.

-   **[Get prompt assistance with Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=use-prompt-assistance&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Use prompt assistance to get a jump-start with your prompt development by selecting an example from the prompt library or using Now Assist to generate one.

-   **[Evaluate skill prompts](https://www.servicenow.com/docs/access?context=evaluate-prompt&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Evaluate your prompts created within Now Assist Skill Kit using data collections created within Now Assist Data Kit. Evaluations return information on the correctness and faithfulness of the responses from running the custom skill.

-   **[View skill run test history](https://www.servicenow.com/docs/access?context=test-prompt-template&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

View the history of your test results to assist your understanding of how changes to the prompt have adjusted the outcome.

-   **[Generate a Knowledge article using multi-language support](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-using-multilanguage-support&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Generate a Knowledge article for an incident, case, or other supported task type in languages other than English using the multi-language capabilities of Now Assist.

-   **[Edit an article using the Now Assist context menu](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-using-context-menu&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Use generative AI capabilities of Now Assist to shorten or elaborate content within a Knowledge article.

-   **[Use Now Assist Data Kit to add a dataset to the data catalog](https://www.servicenow.com/docs/access?context=now-assist-data-kit-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Create a data collection and select the sampling data for publication. Once published, the evaluation data is available in Now Assist Skill Kit.

-   **[Now Assist context menu](https://www.servicenow.com/docs/access?context=now-assist-write-overview&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**
    -   Write with Now Assist is now called the Now Assist context menu.
    -   Explain the assessed and calculated change request risk with the Now Assist context menu in workspaces and UI16.
    -   Use the **Elaborate** and **Shorten** content editing capabilities of the Now Assist context menu in Knowledge articles.
    -   Configure the maximum number of content refinement calls using the Now Assist context menu.
    -   Use the Now Assist context menu recommendations to compose an email and complete the drafts.

-   **[Dynamic theming enables different themes to be applied to chat summarization cards](https://www.servicenow.com/docs/access?context=now-assist-chat-summary&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Support dynamic theming for chat summarization cards.

-   **[Write with Now Assist](https://www.servicenow.com/docs/access?context=now-assist-write-overview&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Enable your agents to use Write with Now Assist for generative AI-powered text generation and editing assistance. This feature helps to improve and streamline their writing responsibilities.

-   **Use Now Assist [Platform skills](https://www.servicenow.com/docs/access?context=na-platform-skills&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**
    -   Use generative AI Platform skills in the Platform workflow starting with the Xanadu release to enhance and streamline your user experience.
    -   Enter search commands in plain language to retrieve and filter records and tables by using the [Navigation](https://www.servicenow.com/docs/access?context=now-assist-global-navigation&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) skill.
-   **Use [Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=now-assist-skill-kit-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for Generative AI app developers**

Create and activate custom prompts and skills for your Now Assist agent use cases.

-   **Generate a knowledge article from multiple cases or incidents with [Now Assist in Knowledge Management](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-coreui&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Draft Knowledge articles quickly from a configurable workspace or the classic environment based on similar cases or incidents with  Now Assist. Knowledge articles can be generated by selecting from a list of similar cases or incidents, case or incident numbers, or even by searching keywords specific to a case or incident.


</td></tr><tr><td>

Now Assist AI agents

</td><td>

-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Configure the access control lists \(ACLs\) for who can discover and trigger AI agents and agentic workflows in their guided setups in the AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to only authenticated users or publicly available.


-   **[Create an AI agent](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Create AI agents accomplish discrete tasks to use in a use case:

    -   Create AI agents to gather data, make decisions, and complete tasks that would otherwise need to be done by a human.
    -   Add one of the following tools or information sources for the AI agent to execute:
        -   Catalog item
        -   Conversational topic
        -   Flow action
        -   Now Assist skill
        -   Record operation
        -   Script
        -   Search retrieval
        -   Subflow
        -   Web search
-   **[Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Create a use case with an execution plan to solve complex tasks with Now Assist. You can also do the following tasks:

    -   Clone an existing use case to avoid manual configuration.
    -   Create triggers when creating a use case that calls the AI agent when a condition or objective is observed.
    -   Test a use case before execution.
    -   Resolve record-based cases with AI agents.
-   **[Enable Now Assist Guardian in AI agents](https://www.servicenow.com/docs/access?context=enable-aia-na-guardian&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Enable Now Assist Guardian in AI agents to automatically identify and block offensive messages that are sent by human agents.

-   **[Multiple conversations in Now Assist AI agents](https://www.servicenow.com/docs/access?context=multiple-conversations-aia&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Enable live agents to interact with multiple AI agent conversations through the Now Assist panel.

-   **[AI Agent Analytics dashboard](https://www.servicenow.com/docs/access?context=ai-agent-dashboard&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Analyze the performance, efficiency gain, and usage of AI agents through preconfigured dashboards.


</td></tr><tr><td>

Now Assist for Creator

</td><td>

-   **[Add visualization to any dashboard](https://www.servicenow.com/docs/access?context=use-dv-generation&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

You can add a generated data visualization to any dashboard you can edit. Previously, you could add a visualization only to a dashboard that was open when you opened the Now Assist panel.

-   **[Generate a playbook from an image](https://www.servicenow.com/docs/access?context=generate-a-playbook-outline&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Generate a playbook with out-of-the-box activities from text, an image, or both.

-   **[Generate a UI experience](https://www.servicenow.com/docs/access?context=ui-generation-landing&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Generate a UI experience using natural language description.

-   **[Edit code with Now Assist](https://www.servicenow.com/docs/access?context=edit-code-now-assist&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Edit code by telling Now Assist how to improve the code. You can refactor code, add comments, validation rules, error handling, and rename variables.

-   **[Generate data pill values during flow generation](https://www.servicenow.com/docs/access?context=flow-generation&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Generate appropriate data pill values for supported flow triggers and action inputs.

-   **[Use Now Assist to create spokes and actions](https://www.servicenow.com/docs/access?context=now-assist-in-spk-gen&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Build custom spokes for the required third-party application by using its API documentation. Kickstart spoke creation by copying and pasting the required API documentation snippet in Workflow Studio. This feature is useful when the required third-party application doesn't have an OpenAPI specification or Postman collection. To use the feature, activate the spoke generation skill in the Now Assist for Creator feature.

-   **[Modify generated data visualizations](https://www.servicenow.com/docs/access?context=use-dv-generation&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

After you generate a data visualization, you can go on through an iterative conversation to modify the visualization.

-   **[Reference specific tables with hash tags during flow generation](https://www.servicenow.com/docs/access?context=flow-generation&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Enter a hash tag character in the flow directions to refer to a specific table by name. Use auto-complete to select a table name from the options that match your partial entry.

-   **[Support more chart types for generating data visualizations](https://www.servicenow.com/docs/access?context=limitations-generating-dv&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

The Analytics Generation data visualization generation skill now supports dial, gauge, horizontal bar, area, column, scatter, spline, and step charts, in addition to the original chart types.

-   **[Edit in ServiceNow Studio after generating an application](https://www.servicenow.com/docs/access?context=sns-app-gen-review-apps&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Use Now Assist for App Generation in ServiceNow Studio, which offers an advanced application development environment.

-   **[Preview an application before generating](https://www.servicenow.com/docs/access?context=generate-apps-from-prompts&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Visually preview an application in a new tab before generating to review for accuracy and reduce the amount of corrective work.

-   **[Update applications that have already been generated](https://www.servicenow.com/docs/access?context=sns-app-gen-edit-apps&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Augment existing applications with new application objects, such as tables, roles, ACLs, and record producers.

-   **[Create new tables by extending existing tables](https://www.servicenow.com/docs/access?context=sns-app-gen-edit-apps&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Create new tables for an application created with app generation by extending existing tables, such as the task table.

-   **[Edit existing applications without having the admin role](https://www.servicenow.com/docs/access?context=app-generation-roles&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Non-admin users with the delegated developer role can edit applications.

-   **[Use Now Assist to call Microsoft Active Directory v2 actions](https://www.servicenow.com/docs/access?context=ms-ad-v2-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

Install Now Assist for Conversational Spokes plugin and start utilizing the conversational ability of Disable User, Enable User, and Look up User actions. You can call these actions from a conversational interface like Now Assist.


-   **[Get Playbook recommendations](https://www.servicenow.com/docs/access?context=playbook-recommendations&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Get suggestions on which activities to replace placeholder activities with.

-   **[Re-prompt and preview while generating a playbook](https://www.servicenow.com/docs/access?context=generate-a-playbook-outline&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Preview and modify your prompt before generating your playbook outline.

-   **[Show annotations of the text directions used by flow generation](https://www.servicenow.com/docs/access?context=create-flow-now-assist&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Show annotations of the text directions used for each item added by flow generation. Receive feedback about how your directions map to specific actions, flow logic, and subflows.

-   **[Data visualization generation](https://www.servicenow.com/docs/access?context=now-assist-data-visualization-generation&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Generate Platform Analytics charts through conversations.


</td></tr><tr><td>

Now Assist for Customer Service Management \(CSM\)

</td><td>

Xanadu Patch 9

-   **[Suggested steps in Recommended Actions](https://www.servicenow.com/docs/access?context=suggested-steps-generation-in-now-assist-for-customer-service-management-csm&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Use Recommended Actions to generate suggested resolution steps for cases. You can increase agent productivity by outlining the next best actions for unfamiliar cases and automatically providing logical next steps.

-   **[Triage cases agentic workflows enhancements](https://www.servicenow.com/docs/access?context=case-resolving-use-case&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Added new standalone AI agents to check duplicate cases and split some existing standalone AI agents to focus on more specific tasks. The AI agents available are the Triage cases planner AI agent, Context validator and analyzer agent, Duplicate identifier AI agent, Informational queries AI agent, Transactional queries AI agent, Case creation AI agent, Entity extraction AI agent, Document verification AI agent, and Email response AI agent.


Xanadu Patch 7

-   **Triage cases AI agents use case**

Use the Triage cases AI agents use case to improve agent productivity through faster assessment.

    |AI agent use case|Description|
    |-----------------|-----------|
    |Triage cases|Use AI agents to handle all routine cases coming in through email and other offline channels, so that it improves customer satisfaction and reduces resolution times.|

-   **[Summarizing sidebar conversations](https://www.servicenow.com/docs/access?context=summarize-sidebar-conversations&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Use Now Assist for CSM to summarize sidebar discussions between agents, requesters, and subject matter experts.

-   **[Real-time chat reply recommendations](https://www.servicenow.com/docs/access?context=generate-chat-reply-recommendations&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Use generative AI to provide the agent with relevant contextual recommendations from sources such as knowledge bases, FAQs, similar cases, chats, and calls before they respond to the customer. Agents can also write a chat response with the help of generative AI. This feature helps agents stay focused on conversations with customers instead of doing manual tasks.

-   **[Generative AI-powered email reply recommendations](https://www.servicenow.com/docs/access?context=generate-email-reply-recommendations&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Get recommendations for email responses that can be reviewed and sent by agents. Agents can also edit email replies recommendation with the help of generative AI.

-   **[Multilingual support for Now Assist for CSM skills](https://www.servicenow.com/docs/access?context=now-assist-csm-supporting-info&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Large language model \(LLM\) now supports the following languages across all skills in Now Assist for CSM: German, French, Japanese, Dutch, and French Canadian, Spanish, Brazilian Portuguese, and Italian.


</td></tr><tr><td>

Now Assist for Enterprise Architecture \(EA\)

</td><td>

-   **[Implement access control lists for security in AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Enable security implementation to execute AI agents and agentic workflows through access control lists \(ACLs\) and user identities.

ACLs provide you with the capability to run AI agents and agentic workflow executions either as a dynamic user or an AI user.

To learn about ACLs for Now Assist for Enterprise Architecture \(EA\) agents and skills, see [Configure Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=configure-now-assist-ea&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US) and [Enterprise Architecture AI agent generate enterprise architecture diagram agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-aiagents-ea-diagramming-usecase&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US).

-   **Xanadu Patch 7 [Using Enterprise Architecture Diagramming AI agent](https://www.servicenow.com/docs/access?context=using-na-ea-ai-agents&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

Use the Enterprise Architecture Diagrammer AI agent to create Enterprise Modeling and Visualization diagrams for business applications hierarchy and summarize them.

-   **Xanadu Early Availability [Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=now-assist-ea&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**
    -   Use the ServiceNow® Now Assist for Enterprise Architecture \(EA\) application to summarize Architectural Decision Records \(ADR\) in the Enterprise Architecture Workspace. Use the Architectural Decision Records \(ADR\) to explain your infrastructure. ADR is a type of artifact that helps you to understand the background of a specific architectural decision.
    -   Register a business application and a digital integration with an interactive generative AI experience using the Now Assist in Virtual Agent. For more information, see [Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=now-assist-ea&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US).

</td></tr><tr><td>

Now Assist for Field Service Management \(FSM\)

</td><td>

-   **Now Assist context menu for KB creation**

Use the enhanced Now Assist context menu to rewrite knowledge articles with generative AI. Opt to shorten or expand upon the existing content within articles.

-   **Multilingual support for Now Assist for FSM skills**

Generate knowledge articles in multiple languages for work order tasks using the new multilingual support in Now Assist for FSM skills.


-   **KB Generation**

Generate knowledge articles from work order tasks so agents can resolve known issues faster.

-   **Sidebar summarization**

Summarize Sidebar discussions from the platform and the Mobile Agent application.


</td></tr><tr><td>

Now Assist for Financial Services Operations \(FSO\)

</td><td>

-   **[ACL security implementation](https://www.servicenow.com/docs/access?context=configuring-security-in-now-assist-for-fso&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

Now Assist for FSO can be configured to enable security implementation to execute generative AI skills through ACLs and user identities. Some predefined ACLs are provided for case summarization.


-   **[Case summarization skill](https://www.servicenow.com/docs/access?context=now-assist-case-summary&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Designed to save time for your agents by allowing them to condense a record to a short summary \(when configured\). Now Assist for FSO includes the customized skills that can be configured to use for specific card dispute and insurance claim use cases.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Enable your agents to access Now Assist skills in a panel that is available in Financial Services Workspace. After configuration, agents can summarize the viewed record or a specific case number in Now Assist panel.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Use the Now Assist Admin console to activate and configure the capabilities and individual skills. For example, you can designate which roles have access to a skill, or whether the skill is available in Financial Services Workspace, the Now Assist panel, or both.

-   **[Skill availability restricted by user role](https://www.servicenow.com/docs/access?context=configure-now-assist-for-fso&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

Specify the roles that can access the case summarization skill.


</td></tr><tr><td>

Now Assist for Hardware Asset Management \(HAM\)

</td><td>

[Xanadu Patch 10](../quality/xanadu-patch-10.md)

</td></tr><tr><td>

Now Assist for IT Operations Management \(ITOM\)

</td><td>

[Xanadu Patch 1](../quality/xanadu-patch-1.md)

-   **[Speed up alert resolution with a Now Assist analysis of past related incidents](https://www.servicenow.com/docs/access?context=nai-past-incidents&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Enhance efficiency and reduce downtime with a Now Assist analysis of past incidents on the same or related CIs. Now Assist investigates historical data to identify past incidents related to the current alert and reports their frequency and criticality levels. It also provides a summary of effective strategies used to resolve them. In addition, Now Assist offers contact information for individuals or teams who have resolved similar incidents in the past and could assist when needed.

-   **[Generate an alert group description in Express List using Now Assist](https://www.servicenow.com/docs/access?context=alert-group-descr-generate-el&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Use Now Assist to generate a description of an alert group in Express List that encompasses all the alerts within the group. The generated description replaces the original description of the group.

-   **[Launch an alert analysis from the Now Assist panel](https://www.servicenow.com/docs/access?context=alert-analysis-now-assist-panel&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Analyze an alert from the Now Assist panel. The alert analysis displays directly in the Now Assist panel for convenient review.


</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

**Xanadu Patch 9**

-   **[Using IT Service Management AI agent collection](https://www.servicenow.com/docs/access?context=now-assist-itsm-ai-agents-use-cases&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Use the IT Service Management AI agent collection to boost productivity, and autonomously resolve business tasks.

    |Agentic workflows|Description|
    |-----------------|-----------|
    |Triage and categorize ITSM incidents|Identify the category, subcategory, and configuration item for an incident automatically, and link associated major incidents or known problems.|
    |Investigate and resolve ITSM incidents|Get recommendations to resolve an incident based on the incident number. Check for related catalog items, Knowledge articles, and similar resolved incidents to generate resolution steps for the incident.|
    |Manage Microsoft 365 group members|Add or remove groups and email distribution lists from the Microsoft 365 group.|

-   **[IT Service Management AI agent collection Generate change request plans agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-change-planner-usecase&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Use the following additional AI agents to handle change requests.

    |AI agent|Description|
    |--------|-----------|
    |Change risk and impact analysis AI agent|Analyzes the potential risk and impact of a change request.|
    |Change justification proposal AI agent|Proposes justification for a change request.|

-   **[Generate a Major Incident email content recommendation by using Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm-mim-email-recommendation&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Draft a communication for a major incident using an email template. You can fill in the template field values with an AI-generated response.

-   **[Generate comments and work notes using the Now Assist context menu](https://www.servicenow.com/docs/access?context=request-gen-ai-capabilities-itsm-now-assist-panel&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Enable your agents to generate comments and work notes quickly and add them to incidents using the Now Assist panel.

-   **[Incident sentiment and sentiment trend](https://www.servicenow.com/docs/access?context=now-assist-itsm-skills&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Make informed decisions on incidents by considering the requester's sentiments and the reasoning behind them.

-   **[Suggested steps generation in Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=resolution-steps-generation-now-assist-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Automatically generate suggested steps to resolve an incident by analyzing the solutions from clusters of similar resolved incidents.

-   **[Summarizing attachments in the Incident summarization skill](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-skill&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Summarize, analyze, and extract data from attachments that are of type PNG or JPEG using Document Intelligence in the Incident summarization skill.

-   **[Using self service to deflect incidents in a ServiceNow portal by using Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=deflect-incidents-now-assist-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Designed to reduce the number of incidents to be resolved by deflecting issues with self-service.

-   **[Customizing a Now Assist for IT Service Management \(ITSM\) change risk skill](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-change-risk-skill&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Efficiently explain the risk of a change request by adding custom input fields to the following input tables:

    -   Change request
    -   Past similar change request
    -   Incident caused by change
-   **[Refining a change risk explanation response](https://www.servicenow.com/docs/access?context=change-risk-exp-now-assist&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Refine the explanation to a change risk by shortening or lengthening a response by using Now Assist for IT Service Management \(ITSM\).

-   **[Risk Assessment as input to calculate a change risk](https://www.servicenow.com/docs/access?context=change-risk-exp-now-assist&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Use risk assessment values as an input to explain the risk of a change request.

-   **[Generating an email response by using Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm-email-recommendation&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Get recommendations for email responses that agents can review and send to users. Agents can also get email template and content edit recommendations from Now Assist for IT Service Management \(ITSM\).

-   **[Monitoring task status using pre-built LLM topics with Now Assist in ITSM Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-customize-itsm-llm-topic&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Copy and customize a ITSM Virtual Agent core ITSM topic template to track the status of a task by using Now Assist in ITSM Virtual Agent.


-   **[Using IT Service Management AI agent collection](https://www.servicenow.com/docs/access?context=now-assist-itsm-ai-agents-use-cases&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Use IT Service Management AI agent collection to boost productivity, and autonomously resolve business tasks.

<table id="table_gjc_gkw_g2c"><thead><tr><th>

AI agent use case

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Generate post incident reviews

</td><td>

Enhance IT productivity during major incidents by minimizing the time required to generate post-incident reviews using AI agents. This process helps improve communication and avoid outages​.**Important:** To enable the display of the Generate post incident reviews use case, you must activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\). For more information, see [Activate Incident Management - Major Incident Management](https://www.servicenow.com/docs/access?context=activate-major-incident-management-plugin&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

</td></tr><tr><td>

Generate change request plans

</td><td>

Enhance IT productivity and help decrease the time to schedule change and manage change risk using AI agents. These AI agents can look up similar changes, generate implementation, back out, and test plans to manage change effectively.

</td></tr><tr><td>

Categorize incidents

</td><td>

Autonomously recommend incident categorization using AI agents. The AI agent assigns a category, subcategory, and a configuration item \(CI\) to incidents based on the incident description. The assigned CI is also based on callers associated with that item.

</td></tr><tr><td>

Notify users with Twilio

</td><td>

Send text messages via SMS to recipients manually using AI agents to help improve the time required for subject matter expert response.**Important:** To enable the display of the Notify users with Twilio use case, you must activate the Twilio Spoke plugin \(sn\_twilio\_spoke\). For more information, see [Twilio Spoke](https://www.servicenow.com/docs/access?context=twilio-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

</td></tr></tbody>
</table>
-   **[Risk rating explanation for a change request](https://www.servicenow.com/docs/access?context=change-risk-exp-now-assist&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Provide your change managers with a better understanding of the risk rating of a change request, including the potential impacts and risks, by generating the risk explanation by using the Now Assist icon. The risk rating explanation can be generated on the change request form and in the Now Assist panel.

-   **[Ask questions about an incident by using the Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Enable your agents to quickly obtain common incident information conversationally within the incident record by asking questions in the Now Assist panel. Topics include the caller's assets, caller's recent incidents, on-call experts, and similar resolved incidents.

-   **[Enhanced incident resolution notes using the Now Assist context menu](https://www.servicenow.com/docs/access?context=resolve-incident-now-assist&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Provide your agents with enhanced resolution notes information in the incident summary, including the root cause and steps taken to resolve the issue, by using the Now Assist context menu.

-   **[Proactive actionable ITSM Virtual Agent notifications](https://www.servicenow.com/docs/access?context=itsm-va-prebuilt-topics&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Provide your agents with proactive actionable notifications as part of ITSM Virtual Agent pre-built Large Language Model \(LLM\) topic conversations that are designed to help your users complete common IT-related tasks.

-   **[Change request summarization enhancements](https://www.servicenow.com/docs/access?context=summarize-change-now-assist&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Provide your change managers with an improved change request summary including additional details, such as the affected configuration items \(CIs\) and impacted services.

-   **[Incident summarization enhancements](https://www.servicenow.com/docs/access?context=summarize-incident-now-assist&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Provide your agents with an improved incident summary by including additional details, such as the service level agreements \(SLAs\), affected CIs and impacted services, and child incidents.


-   **[Summarize a change request](https://www.servicenow.com/docs/access?context=summarize-change-now-assist&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Provide your change managers with a better understanding of the content, intent, and impact of a change request by viewing the change summarization on the change request form and in the Now Assist panel.

-   **[Generating a knowledge article from similar incidents](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-SOW-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Enable your agents to generate a comprehensive knowledge article by leveraging information from a similar set of incidents.

-   **[Generating chat reply recommendations](https://www.servicenow.com/docs/access?context=now-assist-itsm-chat-recommendation&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Provide your agents with quick answers to common questions that are asked in chats by using the Now Assist icon ![Now assist icon.](../../common/image/icon-ai-sparkle.png) in chat reply recommendations.

-   **[Summarizing a Sidebar discussion](https://www.servicenow.com/docs/access?context=now-assist-itsm-sidebar-discussion&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Enable your agents to summarize Sidebar chats and post summaries into the work notes of incidents, changes, requests, problems, and knowledge base tasks \(any record type where Sidebar discussions are enabled\) by using Sidebar discussion summarization.


</td></tr><tr><td>

Now Assist for Source-to-Pay Operations

</td><td>

-   **[Now Assist for Sourcing and Procurement Operations \(SPO\)](https://www.servicenow.com/docs/access?context=now-assist-spo&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

With ServiceNow® Now Assist for Sourcing and Procurement Operations \(SPO\), fulfillers can easily summarize procurement-related records, providing real-time progress updates and action items. Available summarization skills include

    -   Sourcing request summarization
    -   Purchase requisition summarization
    -   Procurement case summarization
If you're entitled to Source-to-Pay Operations Pro SKU and Sourcing and Procurement Operations Pro SKU, you can install this application.

-   **[Request the generative AI capabilities by using the Now Assist for SPO Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-spo-va-using&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

Requesters can leverage contextual generative AI using the Now Assist for SPO Virtual Agent to complete self-service tasks, such as purchasing products or tracking the status of purchase requisitions, sourcing requests, or procurement cases.


-   **[Now Assist for Supplier Lifecycle Operations \(SLO\)](https://www.servicenow.com/docs/access?context=now-assist-slo&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

With ServiceNow® Now Assist for SLO, supplier managers and fulfillers can summarize the details of supply-related records to keep them informed about their progress and action items.

-   **[Now Assist for Accounts Payable Operations \(APO\)](https://www.servicenow.com/docs/access?context=now-assist-apo&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

With ServiceNow® Now Assist for APO application, AP fulfillers can easily summarize invoice case and inquiry case-related records, providing real-time progress updates and action items.


</td></tr><tr><td>

Now Assist for Strategic Portfolio Management \(SPM\)

</td><td>

-   **Xanadu Patch 7 [Using AI agent agentic workflows in Now Assist for Strategic Portfolio Management \(SPM\)](https://www.servicenow.com/docs/access?context=using-na-spm-ai-agents&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Use Now Assist for SPM AI agents to help enhance project efficiency by monitoring your tasks autonomously.

    |AI agent use case|Description|
    |-----------------|-----------|
    |Monitor project tasks|Track project tasks with AI agents to detect important updates such as delayed end dates, status turning red, or state updates. AI agents can help project managers to enhance productivity by delivering real-time visibility into key task changes, enabling proactive decision-making.|

-   **[Summarize multiple feedback records](https://www.servicenow.com/docs/access?context=now-assist-spm&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Summarize multiple feedback records through generative AI and save time by not having to do manual feedback analysis. You can generate a short summary for one or multiple feedback records at once and use it to make informed decisions on your product.

-   **[Generate a summary in Now Assist in Docs](https://www.servicenow.com/docs/access?context=summarize-documents-genai-skill-spw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Use Now Assist in Docs to create a concise summary of the selected text and quickly gain relevant information.

-   **[Schedule the project summary emails with Email project summary skill](https://www.servicenow.com/docs/access?context=email-project-summary-skill-pw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Generate a comprehensive summary of the entire content in Docs by using the Gen AI Docs skill and reduce the time spent on manually analyzing all the information. The Gen AI Docs skill name is Project Gen AI Docs in Project Workspace, Planning item Gen AI Docs in Strategic Planning, and EAP Teams Gen AI Docs in Enterprise Agile Planning.

-   **[Generate the summary for selected or complete content with Planning item doc summarization skill in Strategic Planning](https://www.servicenow.com/docs/access?context=summarize-documents-genai-skill-spw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Set up automated emails by using the email project summary skill to stay updated on the project progress. The email is shared on a weekly, bi-weekly, or monthly cadence.


</td></tr><tr><td>

Now Assist for Telecommunications, Media and Technology \(TMT\)

</td><td>

-   **[Monitor engagement health](https://www.servicenow.com/docs/access?context=now-assist-tmt-resolve-risk&version=xanadu&pubname=xanadu-telecom-media-technology&ft:locale=en-US)**

Monitor the health score of all engagements, create trend charts, and generate risk signals when a decline is detected.

-   **[Analyze risk signals and recommend solutions](https://www.servicenow.com/docs/access?context=now-assist-tmt-monitor-health&version=xanadu&pubname=xanadu-telecom-media-technology&ft:locale=en-US)**

Retrieve unaddressed risk signals and identify appropriate success plays based on a back-end decision table.


-   **[Using Telecommunications, Media, and Technology AI agent collection](https://www.servicenow.com/docs/access?context=using-aiagents-usecases&version=xanadu&pubname=xanadu-telecom-media-technology&ft:locale=en-US)**

Use Now Assist for TMT AI agents to troubleshoot and autonomously resolve customer issues.

    |AI agent use case|Description|
    |-----------------|-----------|
    |Test and repair telecom service issues|Use AI agents to handle task requests that require troubleshooting, diagnosis, and resolution of a case task.|


-   **[Service Problem Case summarization skill](https://www.servicenow.com/docs/access?context=now-assist-case-summary&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Designed to save agents time by condensing the service problem case record to a short summary.

-   **[Resolution notes generation skill](https://www.servicenow.com/docs/access?context=now-assist-rn-summarization&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Enable your agents to generate the resolution information for a service problem case, propose the resolution to the customer, and add the information to the service problem case record through the resolution summarization skill.

-   **[Test summarization skill](https://www.servicenow.com/docs/access?context=now-assist-tmt-exploring&version=xanadu&pubname=xanadu-telecom-media-technology&ft:locale=en-US)**

Identify the root cause of a problem diagnosed during the test run by generating a clear and concise root-cause analysis of the service issue through the test summarization skill.

-   **[Now Assist Panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Enable your agents to access Now Assist skills in a panel available on CSM/FSM Configurable Workspace. Now Assist is aware of context, so it can summarize the currently viewed record or conversation, or you can specify a case number.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Activate and configure capabilities and individual skills on the Now Assist Admin console. For example, you can designate which roles have access to a skill, or whether the skill is available in CSM/FSM Configurable Workspace, the Now Assist panel, or both.

-   **[Add conditions to skill availability](https://www.servicenow.com/docs/access?context=now-assist-tmt-configuring&version=xanadu&pubname=xanadu-telecom-media-technology&ft:locale=en-US)**

Determine when the skills for the case and the resolution notes summarization are available by adding conditions to the fields on the service problem case record.

-   **[Restrict skill availability by user role](https://www.servicenow.com/docs/access?context=now-assist-tmt-configuring&version=xanadu&pubname=xanadu-telecom-media-technology&ft:locale=en-US)**

Specify the roles that can access the case summarization and resolution notes summarization skills.

-   **[Minimum text requirement for case summarization](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-case&version=xanadu&pubname=xanadu-telecom-media-technology&ft:locale=en-US)**

Enable the case summarization skill for cases that have the minimum amount of information in the case activity stream.


</td></tr><tr><td>

Now Assist in AI Search

</td><td>

-   **AI Search Genius Results widget for record producers**

Administrators can configure the AI Search Genius Results widget on record producers to enhance the user experience when creating an incident. The widget displays actionable Genius Result suggestions relevant to the user's incident description. Users can select from these Genius Result suggestions to address their own issues, or can continue with their incident submission if none of the suggestions resolve their problem.


</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

-   **[Use enhanced chat](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Enhanced chat is a conversational support experience within a resizable and moveable window that also includes the ability to have multiple active conversations and superior search capabilities. Using enhanced chat's full-page experience further intertwines chat and search capabilities by redirecting users into a full-page chat after entering a query into a portal's search bar.

-   **[View inline citations](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

View the expanded list of inline citations for standard and enhanced chat:

    -   Catalog
    -   Topic, subflows, or actions
    -   Q&amp;A Knowledge Base articles
    -   External content connections

**Note:** External content connections now include the following connection types:

        -   Microsoft SharePoint
        -   Confluence
        -   Atlassian Jira Cloud
        -   Google Drive
        -   Microsoft Teams
        -   Predefined web sources
        -   ServiceNow® documentation
        -   Slack
    -   People

**Note:** If Knowledge Graph is turned on, you can view information about a person. The people information in the Virtual Agent response typically includes their title, department, location, and email address. The people popover shows additional information.

-   **[Use suggested actions](https://www.servicenow.com/docs/access?context=suggested-actions&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

View suggested actions that were related to your prior conversation and that you consider doing next. After completing a conversational catalog request, conversational subflow, or Virtual Agent topic, two suggested actions appear after a `Here's what you can do next` header.

-   **[Stream enhanced chat responses](https://www.servicenow.com/docs/access?context=streaming-responses-requestor&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Stream LLM response messages as they’re generated instead of the response text appearing all at once to end users. Responses stream in either one letter or one word at a time.

-   **[Use language detection to automatically switch the conversational language for enhanced chat conversations](https://www.servicenow.com/docs/access?context=dynamic-lang-detection-translation-enhanced-chat&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Automatically switch the conversational language to the user's detected language during LLM enhanced chat conversations when language detection is turned on. This automatic switch can occur when a user enters an utterance at the start of a new conversation or within the portal home page’s search field.

-   **[Recognize the Boolean user input control during dynamic translation](https://www.servicenow.com/docs/access?context=multi-language-options-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Recognize the Boolean user input control in chat conversations during dynamic translation.

-   **[Adjust Shorten responses toggle to impact Show more option in chat](https://www.servicenow.com/docs/access?context=va-text-response&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

For bot text responses, adjust the **Shorten responses** toggle in Virtual Agent Designer to turn off the **Show more** option on the user side. When **Shorten responses** is turned off, the **Show more** option does not appear in the chat to the user and the full answer is displayed rather than a truncated response.

-   **[Configuring Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

In addition to configuring Now Assist in Virtual Agent assistants, admins can configure the default Now Assist panel assistants. Options may vary for Now Assist panel assistants.

[Create an assistant](https://www.servicenow.com/docs/access?context=create-assistant&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)

    -   If multiple assistants are created, users can chat simultaneously with multiple assistants. Conversations are independent from each other.
    -   Turn on or off Now Assist panel \(agent or creator\) assistant. Contact support to configure Now Assist panel assistants.
[Assign Now Assist skills to an assistant](https://www.servicenow.com/docs/access?context=assign-na-skills-assistant&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)

    -   Now Assist Topic skill must be turned on at the assistant level for document uploads to be activated when managing the chat experience. For more information, see [Manage an assistant chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).
    -   Create and manage agentic workflows in Now Assist AI Agents Studio and assign the workflows to the assistant.
[Display your assistant on a portal or channel](https://www.servicenow.com/docs/access?context=display-assistant-portal-channel&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)

    -   Display Now Assist in Virtual Agent enhanced chat, with or without the full-page experience, on your portal or mobile app. This dynamic window includes the ability to have multiple active conversations and search capabilities. To use enhanced chat, portals and mobile apps require AI Search to be enabled. For more information on the prerequisites, see [Portal prerequisites for enhanced chat](https://www.servicenow.com/docs/access?context=prerequisites-enhanced-chat&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US) and [Mobile app prerequisites for enhanced chat](https://www.servicenow.com/docs/access?context=mobile-prereqs-enhanced-chat&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).
[Manage an assistant chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)

    -   Upload documents to Now Assist in Virtual Agent standard chat or enhanced chat experience. The Now Assist topics skill must be enabled in Now Assist skills. For more information on file formats, see [Upload documents in Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=upload-documents-na-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).
[Review assistant settings](https://www.servicenow.com/docs/access?context=review-assistant-settings&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)

    -   Document uploads appear as active if it's turned on when managing the chat experience.
-   **[Upload documents in Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=upload-documents-na-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Upload or drag and drop files to Now Assist in Virtual Agent \(standard chat or enhanced chat\). The assistant analyzes and understands the content of the files, and a user can ask questions about the content of the files or get a summary.

-   **[Now Assist in Virtual Agent system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Enable suggested actions in Now Assist in Virtual Agent so that users are offered options for what they can do after completing a prior action. Suggested actions is applicable to standard and enhanced chat, mobile, and Microsoft Teams.


-   **[Stream chat responses](https://www.servicenow.com/docs/access?context=streaming-responses-requestor&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Stream LLM response messages as they’re generated instead of the response text appearing all at once to end users. Responses stream in either one letter or one word at a time.


-   **[Use Now Assist to call Microsoft Active Directory v2 actions](https://www.servicenow.com/docs/access?context=ms-ad-v2-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

Install Now Assist for Conversational Spokes plugin and start utilizing the conversational ability of the Look up User spoke action. You can call this action from a conversational interface like Now Assist.

-   **[Run an action from a conversation](https://www.servicenow.com/docs/access?context=conversational-actions&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Run a Workflow Studio action from a Now Assist conversation. Create and configure the conversational action from Workflow Studio. View and edit conversational actions within Virtual Agent Designer.

-   **[Run a subflow from a conversation](https://www.servicenow.com/docs/access?context=conversational-subflows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Run a Workflow Studio subflow from a Now Assist conversation. Create and configure the conversational skill from Workflow Studio. View and edit conversational subflows within Virtual Agent Designer.

-   **[AI generated topic description message within topic migration](https://www.servicenow.com/docs/access?context=migrate-nlu-llm&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

A `Topic description generated by Now Assist` message now appears near the **Topic Description** field during the topic migration's Review descriptions step.

-   **[Small talk for LLM conversations](https://www.servicenow.com/docs/access?context=create-small-talk&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Use small talk in LLM conversations for greetings and farewells along with gratitude and complaint statements. A Semantic Filtering Framework \(SFF\) detects small talk and generates an appropriate response.

-   **[Language detection for LLM conversations](https://www.servicenow.com/docs/access?context=multi-language-options-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Use language detection for your LLM conversations to improve your user's experience.

-   **[Virtual Agent Designer home page](https://www.servicenow.com/docs/access?context=vad-topics-page&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

A new list-based Virtual Agent Designer home page appears for users who have activated Now Assist in Virtual Agent and the Agent assist Topics skill. The card-based UI is still available for those users who use only NLU/keyword or Virtual Agent Lite.

-   **[Virtual Agent Designer user input controls](https://www.servicenow.com/docs/access?context=va-user-inputs&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Updates to LLM user inputs include:

    -   Use the Validation toggle in the Advanced section of User Inputs to confirm user input values by scripts.
    -   Use the Allow slot filling toggle on User Inputs to switch between static \(single field\) and dynamic \(define with scripts or data pill picker\) detail description modes.
    -   Get a message that a mandatory field cannot be skipped when you attempt to skip a user input with conditions not set to be skippable.
-   **[Configuring Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Updates to the admin guided setup include:

    -   Enhance functionality and efficiency of your Virtual Agent by linking primary assistants to secondary assistants, enabling a primary assistant to use search sources from secondary assistants.
    -   View the relationship between primary and secondary assistants within a map view.
    -   Select portals and mobile applications to display Virtual Agents.
    -   Create conversational subflows and actions by launching Workflow Studio to make conversational subflows and actions available to the assistant.
-   **[Synthesized response](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

For Now Assist in Virtual Agent users, a synthesized response can appear. A synthesized response includes a brief summary of the requested information and search results along with Genius Results. Mid-topic switching can occur during a conversation with synthesized response. Users can continue with their original request or switch the conversation's focus.

-   **[New system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

The following system property was added to increase flexibility of the search results and response:

    -   **sn\_nowassist\_va.synthesized\_autostart\_items**: When synthesized response only returns a singular action, configure whether to directly launch into that action. By default, whenever synthesized response returns a single Virtual Agent topic, that action is auto-launched. The following actions can be configured to auto-launch:
        -   Synthesized response returns a single conversational catalog item.
        -   Synthesized response returns a single Virtual Agent topic, along with Knowledge Base information.
        -   Synthesized response returns a single conversational catalog item, along with Knowledge Base information.

-   **[Delete virtual agents](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Delete a Virtual Agent from the assistants list.

-   **[Support virtual agents on a portal](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Allow public availability of an LLM-based Virtual Agent on a portal.

-   **[Display a virtual agent in a channel](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Integrate your preferred messaging channels to display your Virtual Agent.

-   **[Install proactive triggers](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Install Proactive Triggers from within the Review page.

-   **[Support notifications in virtual agents](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Support actionable and non-actionable notifications for LLM conversations in Virtual Agent.


</td></tr><tr><td>

Operational Resilience

</td><td>

-   **[Managing Operational vulnerability](https://www.servicenow.com/docs/access?context=operational-vulnerability&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Address operational vulnerabilities through reporting, assessing impact, evaluating criticality, managing issues, and planning treatments in Operational Resilience Workspace. Report operational vulnerabilities by using either Employee Center or Operational Resilience Workspace.

-   **[Maintaining Digital resilience third-party registers](https://www.servicenow.com/docs/access?context=digi-resi-third-party-registers&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Comply with Digital Operational Resilience Act \(DORA\) regulation requirements by creating contractual arrangements between the financial entities and the ICT service providers in Digital resilience third-party registers. The ICT third-party service provider records are maintained in Digital resilience third-party registers for DORA compliance.

Add or modify the records in bulk or individually for assessments, branches, contracts, functions, legal entities, supply chains, third parties, or third-party engagements. Export the records to Microsoft Excel format for the European Union to streamline the auditing process as per the regulation. You have the option to import the records from external sources into the Digital resilience third-party registers application.


</td></tr><tr><td>

Operational Sustainability Management

</td><td>

-   **[Track scope 3 emissions](https://www.servicenow.com/docs/access?context=scope-3-dashboard&version=xanadu&pubname=xanadu-environmental-social-governance&ft:locale=en-US)**

Track Scope 3 emissions using the Scope 3 dashboard to fully grasp and manage your organization's environmental impact. These emissions constitute the largest part of your greenhouse gas output, stemming from indirect sources. This comprehensive understanding aids in regulatory compliance, and obtaining full carbon footprint disclosures. After you identify your scope 3 emission sources, you can take action to mitigate the largest sources of indirect emissions.

-   **[View emission factors in ESG content accelerator](https://www.servicenow.com/docs/access?context=esg-content-accelerator&version=xanadu&pubname=xanadu-environmental-social-governance&ft:locale=en-US)**

Use the ESG content accelerator to automatically obtain the emission factors that are published by the standard sources. Emission factors are coefficients that quantify the emissions produced per unit of activity, material, or energy consumption. They’re crucial for calculating the amount of greenhouse gases \(GHGs\) or pollutants emitted into the atmosphere based on various activities.

-   **[Create fiscal calendars to collect metrics from different geographical locations](https://www.servicenow.com/docs/access?context=enable-custom-fiscal-year&version=xanadu&pubname=xanadu-environmental-social-governance&ft:locale=en-US)**

Collect, aggregate, and report data according to your fiscal calendars that could be different from the standard Gregorian calendar. Many global organizations might have operations in different countries that could follow their own fiscal calendars. This feature enables the entities in other locations to collect data according to their own fiscal calendars.

-   **[Choose the approval flow for metrics](https://www.servicenow.com/docs/access?context=components-installed-with-esg&version=xanadu&pubname=xanadu-environmental-social-governance&ft:locale=en-US)**

Set the sn\_esg.metric\_approval property to use either a simple approval flow for your metrics and metric definitions or use the GRC: Approver Configurator to define multiple levels of approvals based on the business rule definitions. This property has two choices.

If you choose the **Simple** option, the Approval section is enabled both on the manual metric definition form and within the metrics. Using this section, you can designate approvers directly on the metric definition form. This option has a single level of approval.

If you choose the **Advanced** option, the Approval section is unavailable on the manual metric definition form and within the metrics, helping to prevent you from assigning approvers there. Instead, approval can be obtained by setting the approval conditions, tables, and approvers in the GRC: Approver Configurator application. This application also enables you to define multiple levels of approvals.

-   **[Create ad hoc metric data tasks](https://www.servicenow.com/docs/access?context=create-an-adhoc-metric-data-task&version=xanadu&pubname=xanadu-environmental-social-governance&ft:locale=en-US)**

Handle off-cycle requests for up-to-date information on existing metric definitions and metrics by creating ad hoc metric data tasks. These tasks address off-cycle requests and provide the latest information.

-   **[Metric data table](https://www.servicenow.com/docs/access?context=metric-data-table&version=xanadu&pubname=xanadu-environmental-social-governance&ft:locale=en-US)**

Use the enhanced filters on the metric data table to filter your tasks. The filters help to show only the relevant and open tasks for data owners and approvers.

-   **[Identify the energy usage and emission of every asset](https://www.servicenow.com/docs/access?context=managing-sustainable-it&version=xanadu&pubname=xanadu-environmental-social-governance&ft:locale=en-US)**

Use the Sustainable IT dashboard to explore models within a specific category and view the energy consumption of each asset model and all its assets, listed in descending order. This functionality provides deeper insights into your energy usage, helping you identify the models that are in use and are consuming the most energy.


</td></tr><tr><td>

Operational Technology Incident Management

</td><td>

-   **[Create an OT incident from an OT change request](https://www.servicenow.com/docs/access?context=create-ot-incident-from-ot-change&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Create an OT incident related to an OT change request directly from the OT change record in the Industrial Workspace.


</td></tr><tr><td>

Operational Technology Manager

</td><td>

-   **[Operational Technology Visibility dashboard](https://www.servicenow.com/docs/access?context=ot-manager-dashboard&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Track your OT data across different sites with the Operational Technology Visibility dashboard available in the Industrial Workspace.

-   **[Automatic conversion of IT to OT devices using CMDB groups](https://www.servicenow.com/docs/access?context=use-cmdb-groups-it-ot-conversion&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Use CMDB groups to group IT configuration items \(CIs\) based on additional information, such as software installed, so that you can convert the CIs to OT devices.

-   **[Mapped equipment model entity for your OT devices](https://www.servicenow.com/docs/access?context=view-all-mapped-ot-devices&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Identify the equipment model entity that your OT devices are mapped to in the Industrial Workspace and help group your device data by equipment model entity.

-   **[Important actions configuration on the OT Action-Oriented Landing Page](https://www.servicenow.com/docs/access?context=configure-order-important-actions-aolp&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Configure the OT Action-Oriented Landing Page by using the **Sort items** field for your important actions.

-   **[OT Action-Oriented Landing Page](https://www.servicenow.com/docs/access?context=oper-tech-task-oriented-landing-page&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Track critical tasks related to your OT network on the OT Action-Oriented Landing Page in the Industrial Workspace. This landing page provides a big-picture view of your site and business unit data, and it calls out important actions that the signed-in user must prioritize.

-   **[Operational Technology Progress Scorecard](https://www.servicenow.com/docs/access?context=ot-progress-scorecard&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Compare your sites by their key metrics with the OT Progress Scorecard in the Industrial Workspace. To access the OT Progress Scorecard, you must have the OT Progress Scorecard viewer \(ot\_progress\_scorecard\_viewer\) role.

-   **[Redirection to different pages in the Industrial Workspace](https://www.servicenow.com/docs/access?context=industrial-workspace-homepage-destination-rules&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Get redirected to different pages in Industrial Workspace depending on your assigned roles with the new homepage destination rules. This redirection helps you gain access to the data that you need.

-   **[Map IP addresses to OT devices through the SyncIPAddressToOT scheduled job](https://www.servicenow.com/docs/access?context=map-ip-addresses-to-ot-devices&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Use the `SyncIPAddressToOT` scheduled job to update and synchronize the IP address information for all the available OT devices. The scheduled job acquires the IP address information from the IP address \[cmdb\_ci\_ip\_address\] table and adds it to the **IP address** field of the Configuration Item \(CI\).

-   **[CMDB OT class model updates](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-operation-technology&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Utilize an enhanced OT user experience and make additional configurations with the following CMDB OT class model updates:

    -   Product Instance Identifier was added as an identifier for the OT Identification Rule.
    -   The OT backup management model was added to help you store multiple backups against a configuration item.
    -   Firmware Installation \[cmdb\_firmware\_install\], Key Value \[cmdb\_key\_value\], and Software Instance \[cmdb\_software\_instance\] tables were added as a related entry for OT classes.
    -   The **ire\_criterion\_attribute** attribute was added to the OT Entity \[cmdb\_ot\_entity\] table to act as a criterion attribute for an OT entity-related entry.
    -   Optional conditions to filter the records during identification and reconciliation were added to the OT identification rules.
    -   The OT Class Mapping Template \[ot\_class\_mapping\_template\] table was introduced to capture class mappings used for Service Graph Connectors.
    -   Required conditions were added under **Advanced Configuration** that must be met for lookup identification rules.
    -   Industrial printer \(industrial\_printer\) was added as an OT device type.
    -   The Quality Inspection Control System \[cmdb\_ci\_ot\_qics\] class represents the control systems that assist in quality and inspection functions. This new class is a child class of the OT Control System \[cmdb\_ci\_ot\_control\] class.
    -   The Backup Storage Information \[cmdb\_backup\_storage\_information\] class helps manage backups of your OT device data.
    -   The OT System Service \[cmdb\_ci\_ot\_system\_service\] class can model OT systems and their related software, hardware, and communication network components, such as a Distributed Control System \(DCS\).
    -   You can now bulk-validate NIDS records from the list view instead of validating each NIDS record individually.
-   **[Pre-import OT Worksheet Entry Review \(POWER\) tool](https://www.servicenow.com/docs/access?context=service-graph-connector-for-OT-excel&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Use distributed Microsoft Excel spreadsheets to import OT devices for better manageability of your OT system and its devices. The POWER tool includes the following new features:

    -   Firmware Installation records can be created when a firmware version is available.
    -   OT entity update issues can be resolved through the Service Graph Connector for Microsoft Excel.
    -   The new Industrial Core \[com.sn\_ot\_core\] plugin is required for class mapping when using the Service Graph Connector for Microsoft Excel.
    -   Supports the import and classification of the Quality Inspection Control System \[cmdb\_ci\_ot\_qics\] class. If you manually create an OT device in the SG-OT Excel Staging Table, the Quality Inspection Control System class is an option in the **What is the type of OT device?** task.
    -   Supports capturing the Backup Storage Information \[cmdb\_backup\_storage\_information\] class attributes on the staging table, staging table form, and the ETL.
    -   Maps the **Status** field in a staging table record to the **Life Cycle Stage** and **Life Cycle Status** fields on a configuration item \(CI\) record. The **Status** field no longer maps to the **Install Status** field on a CI record.
    -   Creates assets in the Industrial product model category for OT class devices. This enables compatibility with the Enterprise Asset Management product for full lifecycle management of OT class devices.

</td></tr><tr><td>

Operational Technology Request Management

</td><td>

-   **[Create catalog items for your OT Service Catalog](https://www.servicenow.com/docs/access?context=create-catalog-item&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Create a catalog item for the OT Service Catalog using the catalog builder so that other users can submit OT requests that are categorized by catalog item.

-   **[Create fulfillment flows that can fulfill an OT request](https://www.servicenow.com/docs/access?context=create-a-fulfillment-flow-ot-request&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Create a fulfillment flow that catalog items follow to fulfill an OT request. Fulfillment flows for catalog items in the OT Service Catalog include catalog tasks.

-   **[Create an OT request](https://www.servicenow.com/docs/access?context=create-ot-service-request-industrial-workspace&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Once Operational Technology Request Management is configured, create OT requests in the Industrial Workspace to address a product or service needed for an OT device or incident.

-   **[Manage your OT requests and catalog tasks in the Industrial Workspace](https://www.servicenow.com/docs/access?context=operational-technology-request-management-lists-in-industrial-workspace&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

View and access OT requests and catalog tasks in the Industrial Workspace list view under the **OT Request** and the **OT Task** modules respectively.


</td></tr><tr><td>

Operational Technology Vulnerability Response

</td><td>

-   **[Hardware Vulnerability Assessment menu in the Industrial Workspace](https://www.servicenow.com/docs/access?context=understanding-hwd-vuln-assessment&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Automatically and periodically assess the OT device firmware vulnerabilities that are in your inventory and create vulnerable items against the impacted assets \(CI\).

-   **[Risk scores on the OT Vulnerability Risk Rollup dashboard](https://www.servicenow.com/docs/access?context=ot-risk-rollup-dashboard&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

View a table of risk scores for your OT devices at each level of the equipment model with the OT Vulnerability Risk Rollup dashboard.

-   **[Enhanced OTVR \(PA\) dashboard experience](https://www.servicenow.com/docs/access?context=operational-technology-vulnerability-response-dashboard&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

View and manage all of your OT vulnerability data and data visualizations in a centralized location with the enhanced OTVR \(PA\) dashboard, which is accessible on the Dashboard Library page.

-   **[OT Vulnerability Remediation Owner \(sn\_otvr.remediation\_owner\) role](https://www.servicenow.com/docs/access?context=components-installed-with-operational-technology-vulnerability-response&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Assign the OT Vulnerability Remediation Owner \(sn\_otvr.remediation\_owner\) role to users who primarily work on an assigned remediation task and can create change tasks when needed. The OT Vulnerability Remediation Owner role contains the following roles:

    -   cmdb\_ot\_isa\_viewer
    -   cmdb\_ot\_viewer
    -   sn\_vul.close\_vi\_vg
    -   sn\_vul.remediation\_owner
-   **[Automatically set a start time for a remediation task based on the ISA maintenance schedule](https://www.servicenow.com/docs/access?context=create-remediation-task&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Start a remediation task automatically based on the ISA maintenance schedule. After you create the remediation task, it’s picked up during the next scheduled maintenance.

-   **[Common Security Advisory Framework \(CSAF\) supported for Operational Technology Vulnerability Response](https://www.servicenow.com/docs/access?context=csaf-overview&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Use the Common Security Advisory Framework \(CSAF\) with multiple vendor support when importing solutions from Aggregators or Trusted Providers.

-   **[OTVR \(PA\) dashboard Guided Setup](https://www.servicenow.com/docs/access?context=setting-up-the-otvr-pa-dashboard&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Use the OTVR \(PA\) dashboard Guided Setup under the Operational Technology Vulnerability Response section in the Industrial Workspace Guided Setup to configure data collection and review indicator sources.

-   **[Change the Operational Technology Vulnerability Response \(OT VR\) assignment group field in a bulk edit](https://www.servicenow.com/docs/access?context=bulk-edit-assignment-group-otvr&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Use the bulk edit feature to update the **OT VR assignment group** field in multiple site records at once.

-   **[Use compensating controls for Operational Technology](https://www.servicenow.com/docs/access?context=compensating-controls-for-ot&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Use compensating controls for OT to reduce vulnerability risks that can't be patched immediately. Compensating controls help mitigate risks.


</td></tr><tr><td>

Opportunity Management

</td><td>

-   **[Use the Sidebar integration with Microsoft Teams](https://www.servicenow.com/docs/access?context=opportunity-management-sidebars-teams&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

Collaborate on an opportunity with your sales managers and solution consultants, or product and legal teams by using the sidebar integrated with Microsoft Teams to close the deal or opportunity. Additionally, you can communicate with the stakeholders through messages, emojis, and attachments.

**Note:** To use this feature, you must upgrade your ServiceNow AI Platform to Xanadu. To learn more, see [Upgrade to the Xanadu release](../upgrades/concept/upgrades-overview.md).

-   **[Create quotes from opportunity line items](https://www.servicenow.com/docs/access?context=opportunity-management-create-quote-line-items&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

Create quotes by selecting individual line items within an opportunity record.

-   **[Location-based transactions for Opportunity Management](https://www.servicenow.com/docs/access?context=location_based_transactions_for_opportunity&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**
    -   Enable agents to specify a customer location in the product catalog and display only the eligible products for that location when they're adding products to opportunities.
    -   Copy products \(line items\) to other customer locations within the same opportunity.
-   **[Sync quote and opportunity](https://www.servicenow.com/docs/access?context=synchronise_quote_and_opportunity&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**
    -   Establish a synhronisation between quote and opportunity to ensure that values across Opportunity-Quote, and Opportunity Line items-Quote Line items are consistent. This synchronisation allows changes to automatically copy into the opportunity record.
    -   Track revenue from an opportunity accurately by keeping opportunities and quotes in synchronisation.
-   **Subscription revenue metrics**

Provide system-calculated recurring and one-time revenue amounts for product and service subscriptions for opportunities. These amounts help sales agents and managers to gain visibility into revenue metrics and recurring revenue dynamics.


</td></tr><tr><td>

Opportunity Marketplace

</td><td>

-   **[Explore Opportunity Marketplace \(OPM\)](https://www.servicenow.com/docs/access?context=egd-oppt-mrktplc-explore&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Opportunity Marketplace originally had a single opportunity type, Internal jobs. In the Xanadu release there are three additional opportunity types Projects, Gigs, and Volunteer. These opportunity types differ from traditional opportunities in that they’re temporary for a fixed duration. The duration can be short-term or long-term, but not permanent.

-   **[Introduced the opportunity owner persona](https://www.servicenow.com/docs/access?context=egd-oppt-mrktplc-explore&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

The Opportunity owner is the leader or host of the opportunity. Owners can create and publish opportunities to the marketplace for employees to view and apply to. Additionally, Opportunity owners can manage and view status updates to their opportunities from the **Opportunities you own** dashboard.

Owners use the detail pages to review and select applicants. Applicants are employees who have applied for an opportunity. The applicant review experience includes match scores based on how well an employee meets the skills and criteria specified for the role.

-   **[Enhanced opportunities browsing](https://www.servicenow.com/docs/access?context=egd-oppt-mrktplc-explore&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Employees can search and browse opportunities that match their preferences and skills from the **Other opportunities** page.

-   **[Enhanced detail views of opportunities and roles](https://www.servicenow.com/docs/access?context=egd-oppt-mrktplc-explore&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Employees can view the details of the opportunities and roles from an opportunity's details page. Employees see the required and preferred skills and understand their match scores for one or more roles. The opportunity details help employees to understand their own strengths and weaknesses compared to a role they’re interested in applying for.


</td></tr><tr><td>

Order Management

</td><td>

-   **[Add sales agreements to orders](https://www.servicenow.com/docs/access?context=som-add-sales-agreement-to-order&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

When an agent creates an order, the sales agreement associated with the account is automatically applied and the catalog is filtered with the agreement products and prices.

-   **[Add business hours to Jeopardy Management tasks](https://www.servicenow.com/docs/access?context=configuring-jeopardy-management&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

Admins can set planned task due dates, which are calculated based on business hours during weekdays in Jeopardy Management.

-   **[Update specification versions](https://www.servicenow.com/docs/access?context=som-specification-version-update&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

Admins can perform a batch version update to a product inventory’s specification version.

-   **[Add covered products to an order](https://www.servicenow.com/docs/access?context=som-update-covered-products&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

Agents can create covered products and modifications as part of an order capture to establish coverage relationships. They can also create change orders that remove sold products or install base items as covered products from entitlements and contracts.

-   **Order to Cash Operations**
    -   [Order Operations Case Management](https://www.servicenow.com/docs/access?context=csm-case-mgmt-order-ops&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US): Use the Order Operations Case Management application \(com.sn\_order\_case\) to create order cases that reference multiple line items, including orders and order lines. Agents can use these cases to process order-related services such as order changes, inquiries, and disputes.
    -   [Case lines and workflows](https://www.servicenow.com/docs/access?context=csm-case-mgmt-case-lines&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US): Use the Case lines and workflows application \(com.sn\_case\_line\) to reference multiple line items on a case record, including orders or order lines, invoices or invoices lines, contracts, and sold products.

</td></tr><tr><td>

Performance AnalyticsITSM dashboards

</td><td>

-   **Next Experience [Legacy: IT Executive dashboard](https://www.servicenow.com/docs/access?context=it-executive-dashboard&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Get insights into the IT Service Management \(ITSM\) data using the ITSM Success Dashboard. This dashboard provides metrics for executives and managers to take informed decisions. Agents can use the [Service Operations Workspace for ITSM](https://www.servicenow.com/docs/access?context=sow-landing-page&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US) Agent dashboard to get information about their work. These dashboards replace the existing Performance Analytics dashboards.


</td></tr><tr><td>

Platform Analytics experience

</td><td>

-   **[Create a Process Mining project from dashboard insights](https://www.servicenow.com/docs/access?context=pm-projects-insights-suggestions&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

With a single click, create a Process Mining project from the list of suggestions in the Insights panel on a dashboard. Suggestions are available when an issue is identified that might be improved through Process Mining.

-   **[Control data source availability by role](https://www.servicenow.com/docs/access?context=dv-use-data-source-acl&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

Restrict the ability to create data visualizations for a data source to roles that you specify.


</td></tr><tr><td>

Playbooks in Workflow Studio

</td><td>

-   **[Variants](https://www.servicenow.com/docs/access?context=playbook-variants&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Use one playbook for multiple scenarios with variants.

-   **[Playbook recommendations](https://www.servicenow.com/docs/access?context=playbook-recommendations&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Get suggestions on which activities to replace placeholder activities with.

-   **[Re-prompt and preview](https://www.servicenow.com/docs/access?context=generate-a-playbook-outline&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Preview and modify your prompt before building your playbook.

-   **[Image to playbook generation](https://www.servicenow.com/docs/access?context=generate-a-playbook-outline&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Generate a playbook with out-of-the-box activities from text, an image, or both.

-   **[Questionnaire activity](https://www.servicenow.com/docs/access?context=questionnaire-activity&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Reference flow glide variable input and output values in an activity's condition builders to collect up to 10 pieces of information from an agent or fulfiller to use later during a playbook run, without requiring an existing table or fields.

-   **[Greater access controls](https://www.servicenow.com/docs/access?context=user-access-playbooks&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Better manage access to your playbooks and playbook components.

-   **[Archived data enhancements](https://www.servicenow.com/docs/access?context=archive-process-executions&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Schedule process execution data to be archived, and view the JSON files for your archived data.

-   **[Script support for activate, restart, deactivate, and duplicate](https://servicenow.com/docs/bundle/xanadu-release-notes/page/release-notes/now-platform-app-engine/api-rn.html)**

Use a script include or business rule that calls the activate, deactivate, restart, or duplicate playbook APIs.

-   **[Washington 25.2 release](https://servicenow.com/docs/bundle/washingtondc-release-notes/page/release-notes/now-platform-app-engine/process-automation-designer-rn.html)**

See 25.2 features in the [Washington DC Playbooks release notes](https://servicenow.com/docs/bundle/washingtondc-release-notes/page/release-notes/now-platform-app-engine/process-automation-designer-rn.html):

    -   Playbook Assist

</td></tr><tr><td>

Policy and Compliance Management

</td><td>

-   **[Upload policy document from your local machine to Microsoft OneDrive](https://www.servicenow.com/docs/access?context=upload-word-doc-onedrive&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Upload a Microsoft Word document that exists in your local machine to Microsoft OneDrive and link the document with the policy. You can access the document from any device and enable multiple users to collaborate on the policy document.

-   **[Create and associate a policy text document in Google Drive](https://www.servicenow.com/docs/access?context=create-policy-redlining-docu-google-drive&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Integrate your ServiceNow instance with Google documents to manage documents in Google Drive. Create a Word document in Google Drive that you can access through a browser and store in Google Drive. You also have the option to create a Microsoft Word document that you can manage in Google Drive.

-   **[Upload policy document from your local machine to Google Drive](https://www.servicenow.com/docs/access?context=upload-word-doc-googledrive&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Upload a Microsoft Word document that exists in your local machine to Google Drive and link the document with the policy to enable multiple users to collaborate on the policy document.

-   **[Upload policy document from your local machine to Microsoft SharePoint](https://www.servicenow.com/docs/access?context=upload-word-doc-sharepoint&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Upload a Microsoft Word document that exists in your local machine to Microsoft SharePoint and link the document with the policy to enable multiple users to collaborate on the policy document.

-   **[Policy authoring using Microsoft SharePoint](https://www.servicenow.com/docs/access?context=connect-sharepoint-doc&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Monitor and revise your organization's policies at regular intervals to maintain their relevance and compliance. Integrating Microsoft Word document files with multiple Microsoft SharePoint sites helps your policy owners, reviewers, and approvers to author, modify, and maintain different versions of a policy text and thus retain its history. You can also collaborate on policy drafting and review processes. The policy text is updated automatically. You can copy and paste text from a document into the **Policy text** field in HTML and then convert it to a PDF format.

-   **[Using CRI assessment questions to profile an entity](https://www.servicenow.com/docs/access?context=perform-cri-assess-pc-ws&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Perform a CRI tiering assessment for an entity to determine its tier, and then perform a CRI assessment for that entity. Based on the response to the CRI questionnaire from the assessor, the compliance status of each mapped control to a question is determined. The overall compliance score of the entity is also calculated.

-   **[User role enhancements in Policy and Compliance Management](https://www.servicenow.com/docs/access?context=manage-pol-comp-emp-center&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Respond to policy acknowledgments and request a policy exception from the Employee Center portal with the employee operator role.


</td></tr><tr><td>

Portfolio Planning

</td><td>

-   **[Show or hide features for your portfolio plan](https://www.servicenow.com/docs/access?context=show-or-hide-the-features-for-your-portfolio-plan-ppw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

As a portfolio manager, show or hide the features, such as Prioritization and Roadmap, of your portfolio plan. This capability helps you share only the portfolio plan data that matters to your stakeholders and restrict access to the other data.

-   **[Planning enhancements](https://www.servicenow.com/docs/access?context=exploring-portfolio-planning&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Filter planning items in the Prioritization page and roadmap bars in the Roadmap page with multivalue fields, such as tags, business applications, and business capabilities.
    -   As a portfolio plan viewer, you can copy a portfolio plan that you don't have edit access to and edit the plan as needed. For more information, see [Copy a portfolio plan](https://www.servicenow.com/docs/access?context=copy-portfolio-plan-in-portfolio-planning&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).
-   **[Optimize planning using scenario planning](https://www.servicenow.com/docs/access?context=scenario-planning-in-strategic-planning&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Create scenarios in a simulated environment and adjust the prioritization and timelines of planning items.
    -   Check the alignment of planning items with goals to verify the delivery of strategic outcomes.
    -   Visualize trade-off decisions between scenarios by comparing scenarios side by side.
    -   Approve the best scenario as the live portfolio plan for execution and making informed decisions.
-   **[Export a roadmap or free-form roadmap to PowerPoint](https://www.servicenow.com/docs/access?context=export-portfolio-plan-status-to-ppt-portfolio-planning-workspace&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Export a roadmap or free-form roadmap from a portfolio plan into a Microsoft PowerPoint file to share data and collaborate with your business stakeholders. The predefined template helps you generate reports for your roadmap, including roadmap milestones, item milestones, vertical lines, and horizontal lanes.

You can export a roadmap for the maximum tenure of lanes a year at a time. You can also choose between Compact mode, which exports 25 horizontal lanes per slide, or Default mode, which exports 15 horizontal lanes per slide, when exporting your roadmap.

You can select the data that you want to be exported into the report by editing the predefined templates or creating your own branded template. For more information, see [Create a Microsoft PowerPoint template](https://www.servicenow.com/docs/access?context=create-ppt-template&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

-   **[Plan at a high level using the Project Program lens](https://www.servicenow.com/docs/access?context=lens-and-portfolio-plans&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Plan at a high level by building portfolio plans for program \[pm\_program\] items using the Project Program lens. Prioritize the programs and track them using roadmaps.

-   **[Docs for planning items in Portfolio Planning](https://www.servicenow.com/docs/access?context=docs-for-planning-items-in-ppw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Store the information of key artifacts and other details of planning items, such as Demands, Projects, and Epics, directly from within the workspace.
    -   Create multiple rich-text documents at each planning item level.
        -   Help avoid data loss and parallel editing with real-time collaboration.
        -   Tag team members to their action items.
        -   Insert media and URLs.
-   **[Financials in Portfolio Planning](https://www.servicenow.com/docs/access?context=fin-migrate-budget-project-ppm&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Migrate the existing budget for planning items from the classic UI to Next Experience using the **Migrate Budget** option.
    -   As a portfolio manager, allocate and manage the budget of your planning items using the Budget vs cost view.
    -   As a project manager, compare a budget to the captured costs of your planning items and reforecast the planned costs to meet the approved budget.
    -   Compare financial baselines to view simple financials and budgets.
    -   View the cost plans, expense lines, and financial baselines of sub-projects using the Financial view of a parent project.
    -   Widgets in the Cost view of parent projects display the rolled-up value of the planned costs, expense lines, budget, and variance.
    -   Create custom labor cost types and map them with a unique sys\_id to generate labor costs.

</td></tr><tr><td>

Privacy Management

</td><td>

-   **[Personal Data Rights](https://www.servicenow.com/docs/access?context=exploring-personal-data-rights&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Use the Personal Data Rights application that provides configurable workflows to manage and automate personal data rights requests efficiently, reducing the risk of non-compliance. The Personal Data Rights application enables customers to efficiently manage and fulfill Data Subject Access Requests \(DSARs\), consumer rights requests, and so on, ensuring compliance with privacy regulations. The application helps organizations to handle requests related to the personal data rights of their consumers while ensuring that employees can maintain data protection standards globally.

-   **[Create data lineage](https://www.servicenow.com/docs/access?context=processing-activity-hierarchy&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Establish a data lineage to understand how data is being consumed and shared in a given processing activity. Creating a data lineage also helps you to understand and manage the associated risks for the data being shared. This feature provides a visual representation of data lineage or hierarchy.

-   **[Create a regulatory agency](https://www.servicenow.com/docs/access?context=add-a-regulatory-agency&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Create regulatory agencies in the Privacy Workspace to identify the relevant regulatory authorities that are responsible for overseeing the businesses in the public interest. The centralized library consolidates all regulatory communication via emails.

-   **[Collaborate and chat with cross-functional teams for processing activities, privacy cases, privacy assessments, and personal data rights requests](https://www.servicenow.com/docs/access?context=manage-discussions-of-a-pa&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Initiate quick discussions with key stakeholders while working on a processing activity, privacy case, or a personal data rights request. The chat feature is integrated with Microsoft Teams and a group is automatically created on Microsoft Teams when a discussion is initiated. The chat conversations that take place using the **Discuss** button are stored in the respective record making it simpler for the privacy teams to refer to them when working on a task.

-   **[View smart attestations on the processing activities](https://www.servicenow.com/docs/access?context=ropa-record&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Use the Smart Assessment Engine feature to respond to attestations. View the reports of the new control attestations on the landing pages of the privacy analyst and the privacy manager. Utilize the filter in the Attestations report to select if you want to view the classic attestations or the new attestations.

-   **[Changes in roles with the Privacy Employee user application](https://www.servicenow.com/docs/access?context=roles-installed-prm&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

**Note:** Only applicable to the customers with the GRC Privacy Employee User application \(sn\_privacy\_emp\) installed.

When you install the new GRC Privacy Employee User application and assign the sn\_privacy\_emp.privacy\_employee role to your employees, the role enables your employees to perform the following operations from the Employee Center:

    -   Proactively request privacy impact assessments \(PIAs\) for new implementations, applications, and processes from the Employee Center.
    -   Report privacy cases related to data privacy policy and regulatory violations.
    -   Read and acknowledge organizational privacy policies.
    -   Create policy exceptions.
    -   Create privacy issues.
-   **[Changes in roles with the GRC: Privacy Lite User application](https://www.servicenow.com/docs/access?context=roles-installed-prm&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

If the GRC: Privacy Lite User application \(sn\_privacy\_lite\) is installed, the following roles are considered as lite operators:

    -   sn\_privacy.business\_user
    -   sn\_privacy.assessment\_responder
    -   sn\_privacy\_case.privacy\_case\_business\_user
    -   sn\_grc\_pdr.data\_owner\_admin
Users with the lite operator role can do the following:

    -   Respond to privacy assessment tasks as business users.
    -   Respond to the processing activity's criticality risk assessments and object-based assessment.
    -   View, update, and close assigned issues.
    -   Respond to the assigned control attestations.
    -   Respond to the assigned manual indicator tasks.
    -   Create, update, and close assigned remediation tasks.
    -   Work on the processing activity as a business user when it’s assigned to you to collect the required details.
    -   Work on breach assessments and other privacy case tasks.
    -   Respond to the detailed privacy risk assessments on each risk identified on a processing activity.
    -   Respond to the assessment and investigation tasks assigned by the privacy team.
    -   Work on personal data rights action tasks to handle data according to the requester's requests.

</td></tr><tr><td>

Proactive Engagement

</td><td>

-   **[Exploring Proactive Engagement](https://www.servicenow.com/docs/access?context=exploring-proactive-engagement&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Use Proactive Engagement to empower employees to self-solve digital experience issues by using the proactive issue detection and resolution capability of Digital End-User Experience.

-   **[Configuring Proactive Engagement resolutions with DEX](https://www.servicenow.com/docs/access?context=configuring-metric-rule&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Engage employees through ServiceNow® Virtual Agent and configure Engagement settings to define how employees can self-solve digital experience issues.

-   **[Proactive Engagement life-cycle management](https://www.servicenow.com/docs/access?context=proactive-engagement-lcm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

View and manage the life cycle of Proactive Engagement resolutions through the workbench.


-   ****

Explore and utilise the different use cases ServiceNow® has to offer as part of the Proactive Engagement base system.


</td></tr><tr><td>

Proactive Service Experience Workflows

</td><td>

-   **[Customer Service Problem Management](https://www.servicenow.com/docs/access?context=cspm-landing-page&version=xanadu&pubname=xanadu-proactive-service-exp-workflows&ft:locale=en-US)**

Manage the entire process of reviewing, diagnosing, and providing a resolution for service problem cases with Customer Service Problem Management.

-   **[Proactive Service Experience Workflows Account 360 Analytics](https://www.servicenow.com/docs/access?context=review-customer-account-360-psew&version=xanadu&pubname=xanadu-proactive-service-exp-workflows&ft:locale=en-US)**

Better understand your customers, the services sold, and the progress of ongoing customer account tasks through a centralized dashboard.


</td></tr><tr><td>

Problem Management

</td><td>

-   **[Initial support for Problem Management models](https://www.servicenow.com/docs/access?context=problem-mgmt-models&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Introduction of Problem Management models, beginning with one default problem model \(General\) and two default problem task models \(Root cause analysis and General\).

The default models are equivalent to the base life cycle in the Washington DC release. This initial support allows for the creation of custom models to tailor additional scenarios for specific use cases.

**Note:**

If you are using Service Operations Workspace 5.x and you enable Problem Management models, you will manage problems and problem tasks in the classic UI16 experience, rather than in Service Operations Workspace.

Service Operations Workspace 6.x is based on the Xanadu release and it supports Problem Management models.


</td></tr><tr><td>

Process Mining

</td><td>

-   **[Process Mining evaluation version available](https://www.servicenow.com/docs/access?context=process-mining&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

Try sample mining and limited features on the Incident table without an entitlement so you can decide whether the advanced features are beneficial to your organization.

-   **[Process Mining graph enhanced with perspectives](https://www.servicenow.com/docs/access?context=set-perspective&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

Filter the Process Mining graph by the activity definitions you want to view at a particular time.

-   **[Understanding the root cause of inefficiency made easier](https://www.servicenow.com/docs/access?context=annotate-project&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

Generate a summary of all work notes to see the history of the inefficiency rather than having to read each individual work note separately.

-   **[Configure finding definitions](https://www.servicenow.com/docs/access?context=configuring-finding-definitions&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

Configure and view automated and rule-based finding definitions efficiently using a comprehensive guided setup.

-   **[Include additional use case analysis in a project automatically](https://www.servicenow.com/docs/access?context=adv-settings&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

Set Approval analysis or SLA breach analysis automatically for applicable processes when creating a project so you don't need to make this selection manually.

-   **[Variation analysis introduced in Summary and Insights page](https://www.servicenow.com/docs/access?context=summary-insights-dashboard&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

Analyze various routes the records in the process took based on parameters like mostly traversed, more steps, and so on. This information is accessible on the Summary and Insights page.

-   **[Customize the outline of the process mining graph dashboard](https://www.servicenow.com/docs/access?context=analyst-workbench-dashboard&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

Customize the orientation of the outline of the process graph set for the current project workbench for nodes within the graph. For example, when using a vertically oriented widget, you might prefer the graph and star diagram to be displayed in a vertical layout rather than a horizontal one.

-   **[Inflow and outflow analysis: node star diagram](https://www.servicenow.com/docs/access?context=node-diagram&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

View the records for any node or arc from the map dashboard.

-   **[Option to filter out incoming or outgoing arcs](https://www.servicenow.com/docs/access?context=analyst-workbench-dashboard&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

View only incoming or only outgoing arcs to see the inflow/outflow of work for a particular process with respect to other related processes on the graph.


</td></tr><tr><td>

Product Catalog Management and Pricing Management

</td><td>

-   **[Location-based transactions](https://www.servicenow.com/docs/access?context=config-location-transaction&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

Enable agents to specify a service location in the product catalog UI and display only the eligible products for that location when they’re adding products to opportunities, quotes, and orders. Agents can create line items for the specified location, as well as copy line items to multiple service or installation locations in the same opportunity, quote, or order. Set up eligibility rules to filter the product catalog, catalog categories, or product offerings by service location.

-   **[Control cascading quantity values in child product offerings](https://www.servicenow.com/docs/access?context=som-activate-cascade-quantity&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

Control how quantity values on top-level product offerings are cascaded to child lines.

-   **[Product offer eligibility](https://www.servicenow.com/docs/access?context=product-catalog-managment&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

Use business rules to filter the product catalog, product categories, and product offerings dynamically, displaying only eligible product offerings for a customer in the product catalog. Define the business rules using product eligibility matrices. If you're using sales agreements, the product catalog displays only the eligible product offers set in the sales agreement.

The November 2024 release provides the following:

    -   Version 2 of product eligibility matrices: Supports eligibility rules based on transaction line attributes along with document header attributes.
    -   System-defined context variables for service locations: Service City, Service State, Service Country, and Service Zip context variables are available to specify service locations in the product eligibility and pricing matrices.
-   **[Product offer bundling with product specifications](https://www.servicenow.com/docs/access?context=som-offer-bundles-with-specs&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

Support bundling of offers that have an associated product specification or specification hierarchy. For example, you can create a product offer that has an associated product specification and indicate whether to inherit the characteristics from the child specifications in addition to the parent specification.


-   **[Configurable pricing plan](https://www.servicenow.com/docs/access?context=configuring-pricing-plan&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

Define the sequence of steps in which pricing rules and calculations are applied. The November 2024 release provides a default pricing plan. You can customize the default plan by copying it and then adding new steps, modifying existing steps, changing the sequence of steps, and adding conditions for running an existing step.

-   **[Subscription revenue metrics](https://www.servicenow.com/docs/access?context=som-subscription-pricing&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

View system-calculated recurring revenue amounts for product and service subscriptions in opportunities and quotes. These amounts help sales agents and sales managers assess the financial value of monthly and annual subscriptions.

-   **[Sales Agreement price lists](https://www.servicenow.com/docs/access?context=pricing-management&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

If you're using the Sales Agreement feature, a published sales agreement price list is generated automatically when a sales agent creates a sales agreement from a completed quote. The sales agreement price list reflects the final unit price for each product captured in the sales agreement and is valid for the start and end dates specified for the agreement. To learn more about sales agreements, see [Sales Agreement Management](https://www.servicenow.com/docs/access?context=sales-agreement-mgmt&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US).

The November 2024 release supports hierarchical price lists and multiple price lists for a sales agreement. Hierarchical price lists enable agents to negotiate different pricing for an offer depending on whether it is sold in the context of a bundle or parent offer or as a standalone product. If multiple price lists exist for a sales agreement, the default price list used is based on currency and the sales agreement. Agents can select from different options, products, and characteristics within a configurable bundle or product, which determines what is available as part of the sales agreement and resulting order.


</td></tr><tr><td>

Project Portfolio Management

</td><td>

-   **[Time Card Management](https://www.servicenow.com/docs/access?context=time-card-management&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Starting with the Xanadu release, new customers can directly access the Analytics Time sheet, Analytics User manager, and Analytics Project manager dashboards in Next Experience.


</td></tr><tr><td>

Project Workspace

</td><td>

-   **[Now Assist in Project Workspace](https://www.servicenow.com/docs/access?context=summarize-docs-genai-skill-pw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Generate a concise summary of selected text on the Docs component using Now Assist.
    -   Summarize, elaborate, and shorten the selected content on the Docs component using the Project Gen AI Docs skill.
    -   Set up automated emails using the Email project summary skill to stay updated on project progress. Schedule the day and frequency for the skill to send the generated emails.
    -   Generate a quick summary on the complete content of the document with Project Gen AI Docs skill and save time on manual content analysis.
-   **[Managing projects with Project Workspace](https://www.servicenow.com/docs/access?context=use-projects-pw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Migrate the budget of your projects from Classic UI to Next Experience.
    -   Allocate and approve the budget of a project using Financials in Next Experience.
-   **[Resource planning with Project Workspace](https://www.servicenow.com/docs/access?context=use-resource-mgmt-prj-wksp&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Follow the assigned schedule for allocation when a resource has a schedule.
    -   Allocate users or groups based on the selected effort type when creating an assignment.
    -   Display allocations inline with the selected effort type.
-   **[Project details page enhancements](https://www.servicenow.com/docs/access?context=update-project-details-from-project-workspace&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Add stakeholders, extend or confirm a resource plan, and add new resource allocations daily.
    -   View a status report for the programs and save the project as a template with the **Save as New Template** option.
    -   Create an Agile phase or a Test phase from the Agile or Hybrid execution type.
    -   Create or add existing stories to a project, as well as add new epics.
    -   View the project or project task details from the side panel.
    -   Use the **Open task in new tab** icon \(![Open task in new tab icon.](../../product/project-workspace/image/open-task-new-tab-icon.png)\) to open a project in a different tab.
    -   Use the **Full details** link to add work notes and attachments, as well as view related lists of a project or task.
-   **[Financials in Project Workspace](https://www.servicenow.com/docs/access?context=using-financials-prj-wrkspc&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Migrate existing project budgets from Classic UI to Next Experience using the migrate budget option.
    -   As a Portfolio Manager, allocate and manage the budget of your projects using the Budget vs cost view.
    -   As a Project Manager, view the comparison of budgets to captured costs for your planning items.
    -   Compare financial baselines to view simple financials and budget.
    -   View the cost plans, expense lines, financial baselines of the subprojects using the Financial view of the parent project.
    -   Widgets in the Cost view of the parent projects display the rolled up value of the planned costs, expense lines, budget, and variance.
    -   Create custom labor cost types and map them with unique sys\_id to generate labor costs.
-   **[Status reporting in Project Workspace](https://www.servicenow.com/docs/access?context=status-reporting-in-pw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Create an overview of the current project status, highlighting key metrics such as health, schedule, scope, cost, and resources, offering a clear snapshot of progress.
    -   Create a new report with or without using a template. A status report captures important details such as milestones, risks, issues, decisions, actions, and change requests, ensuring comprehensive tracking.
    -   Use dynamic data tokens, such as Planned End Date, Status Date, and Actual Cost, which automatically pull and update relevant data, making the report accurate and up-to-date.
    -   Leverage the Docs component to fully customize and configure status reports. Edit and update status reports directly within the Docs component, ensuring they remain accurate and up to date.

</td></tr><tr><td>

Public Sector Digital Services

</td><td>

-   **[Agent updates to License and Permit Playbook](https://www.servicenow.com/docs/access?context=public-sector-resolving-lpr-case-playbooks&version=xanadu&pubname=xanadu-government-industry&ft:locale=en-US)**

Specify the license details and add license endorsements directly from the workspace in License and Permit Playbook.

-   **[Guided Constituent Experience for License and Permit Playbook](https://www.servicenow.com/docs/access?context=psds-create-license-request-user&version=xanadu&pubname=xanadu-government-industry&ft:locale=en-US)**

Streamline how you communicate with your constituents with easy appointment booking. You can also simplify complex license and permit applications with the save and resume and guided data entry functionality in License and Permit Playbook as part of the playbooks-on-portal experience.​

-   **[Document redaction for Information Request Playbook](https://www.servicenow.com/docs/access?context=psds-ir-playbooks-doc-redaction&version=xanadu&pubname=xanadu-government-industry&ft:locale=en-US)**

Redact sensitive content, data, or entire documents within the document management tool in the Information Request Playbook. You can either highlight bodies of text, or search for strings of text and designate them to be redacted. This functionality is only available to information request case agents for documents in the Published or Draft state. New versions of the same document are generated each time that text is redacted or unredacted.

-   **[Now Assist for Public Sector Digital Services \(PSDS\)](https://www.servicenow.com/docs/access?context=now-assist-for-psds&version=xanadu&pubname=xanadu-government-industry&ft:locale=en-US)**

Condense case records into short summaries by using the case summarization skill in the Now Assist for PSDS application. Agents can use the resolution summarization skill to generate resolution information for a case, propose the resolution to the customer, and add the information to the case record. The Now Assist for PSDS application brings generative AI case summarization and resolution notes generation to Public Sector Digital Services.


</td></tr><tr><td>

Quote Management

</td><td>

-   **[Sales agreement in quotes include product bundles](https://www.servicenow.com/docs/access?context=sales-agreement-mgmt&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

Add a sales agreement to a quote that contains configurable product bundles with the ability to choose from available child offers and optional characteristics.

-   **[Location function filters products and creates line items](https://www.servicenow.com/docs/access?context=quote-using-product-location&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

Location-based quoting is a new feature where line items can be created for different service or installation locations and agents can copy line items from one location to another. Agents can also filter products in the catalog by location.

-   **[Add covered products to a quote](https://www.servicenow.com/docs/access?context=som-quote-add-covered-products&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

As an agent, add covered products to quote line items. Covered products include entitlements, service agreements, and warranties. Adding a covered product to a quote enables you to add start and end dates for the agreements.


-   **[Synchronize a quote with an opportunity](https://www.servicenow.com/docs/access?context=som-sync-quote-with-opportunity&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

As an agent, synchronize quote information to an opportunity. As quote information changes, use this function to update the opportunity with information from the quote to keep records accurate.


</td></tr><tr><td>

RPA Hub

</td><td>

-   **[Credential Management in RPA Hub](https://www.servicenow.com/docs/access?context=credential-management-rpa-hub&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

Create application credentials, robot credentials, and Time-based One-time Password \(TOTP\) authentications and reuse them in multiple bot processes through a credential group.

-   **[Migration of a bot process configuration in RPA Hub](https://www.servicenow.com/docs/access?context=bot-process-migration&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

Migrate the bot process configuration and associated assets from one environment to another environment.

For example, when the bot process is ready to be migrated from a developer’s environment to a UAT environment, an RPA developer or RPA administrator can select the **Ready for Migration** button on a published bot process. This action enables the **Migrate** button to appear. This button is only visible when the bot process migration isn’t in progress. Then, the RPA release manager or RPA administrator can initiate the migration process by selecting the **Migrate** button. After the bot process and associated assets are migrated, a release manager can make any necessary changes, create and associate credentials, create an associated bot process record, and publish the bot process on the UAT \(target\) environment.

-   **[Enhanced element interrogations using the recorder feature](https://www.servicenow.com/docs/access?context=recording-automations&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

In the RPA Desktop Design Studio application, while using the recorder feature, you can move and position your recorded actions and screens in the Recorded actions pane. You can also edit a recorded action and element name.

-   **[New sample automations](https://www.servicenow.com/docs/access?context=rpa-studio-ui&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

Use the unattended and attended sample automations that were added to the Sample Automations page of RPA Desktop Design Studio. You can also view them in the Samples Explorer section.

    -   Merge CSV files
    -   Convert Excel to JSON
    -   Fetch contact info from email
    -   Resume Skill Matcher
    -   Copying a Range from One Excel File to Another
    -   Email Archiving or Deletion
    -   Streamlining Report Data Analysis
    -   Extract Excel Table to Embed in Email Body
    -   Zip and Unzip files
    -   XML to Excel Conversion
    -   Extract Data from Table and Saving to Excel
    -   Merge Excel Sheets
    -   Download attachments from Outlook
A sample automation is a prebuilt automation that shows how an automation works in the RPA Desktop Design Studio. The RPA Desktop Design Studio provides multiple sample automations that cater to different use cases.

-   **[Skill enhancements](https://www.servicenow.com/docs/access?context=override-skill-version-rpahub&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

View a skill package version for an associated package in a bot process or attended and unattended packages in RPA Hub. As an RPA release manager, you can override a skill version to use a specific skill package version for your bot process.

For example, to use a latest version of the skill package, you can override the skill package version in RPA Hub without publishing the attended or unattended package again. You can either override a skill version for a bot process or select the bot processes to override in the skill package version.

You can use the different versions of the same skill for different bot processes depending on your specific requirements. When the bot process executes, it uses the selected version instead of the version that was defined in the automation.

The following tabs were added:

    -   Use the **Skill Overrides** tab on the bot process form to view the skill version that was used. You can also use this tab to override the skill version for a specific bot process.
    -   Use the **Skills** tab on the package version of either the type attended or unattended to see the skills that were used in the package version.
    -   Use the **Bot process** tab on the skill package version to override the skill version for one or more bot processes.
In the RPA Desktop Design Studio, the Assign Bot Process feature is enabled for Skills automation projects. It shows both attended and unattended bot processes in the **Bot process** field. For the unattended processes, the associated robots are listed in a drop-down menu. For more information, see [Assign bot process to an automation project](https://www.servicenow.com/docs/access?context=assign-bot-process&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

If any skills are overridden in the bot process, use the Assign Bot Process feature in the RPA Desktop Design Studio to use the revised skill version during the current execution.

If a skill is overridden while the robot is in execution, the robot doesn't use the overridden skill for the current execution. Instead, the robot considers the updated skill version starting from the next execution.

-   **[Sensitive request content in queues](https://www.servicenow.com/docs/access?context=work-queue-form&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

Pass both sensitive data and non-sensitive data separately in work items.

In the Work item form, the **Sensitive Request Content** field was added to store the sensitive content. For more information, see [Work item form in RPA Hub](https://www.servicenow.com/docs/access?context=work-queue-form&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

In the RPA Desktop Design Studio, RPA developers can handle the sensitive data in the Queue connector methods:

    -   For the **CreateJSONWorkItem**, **PickWorkItem**, and **UpdateWorkItem** methods, RPA developers can identify and mark specific JSON fields as sensitive.
    -   For the **CreateStringWorkItem** method, RPA developers have an option to include both sensitive and non-sensitive request content. A new parameter **Sensitive Request Content** was added to capture those details. The data that is passed in the sensitive request content is stored as encrypted data and the data that is passed in the request content field is stored as plain data.
For more information about these methods, see [Queue connector methods](https://www.servicenow.com/docs/access?context=connectors-queues-methods&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

-   **[New CreateFile component in the Zip category](https://www.servicenow.com/docs/access?context=use-zip-createfile&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

Zip an existing folder or create a zip file by using the CreateFile component in RPA Desktop Design Studio.

-   **[Robot user mapping in RPA Hub](https://www.servicenow.com/docs/access?context=create-unattended-robot&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

Map an authorized user to an unattended robot to make the robot credentials accessible only to the mapped user.

In the Unattended robot form, the **User** field was added.

For upgrading customers, the **User** fields are automatically mapped with the user names who have recently created the process jobs for the selected unattended robots. If no process jobs are found for a selected robot, the RPA release managers must manually map the appropriate users to the robots.

-   **[Guided Tours in RPA Hub](https://www.servicenow.com/docs/access?context=use-guided-tour-rpa-hub&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

The following guided tours are available in the classic environment:

    -   Queues: Get step-by-step quick instructions in your instance on how to create queues.
    -   Bot process: Get step-by-step quick instructions in your instance on how to do an end-to-end configuration of the bot process and its related lists. You can select the tour to create an unattended bot process, attended bot process, or Embedded Task Automation.
-   **[What's New tab in the Help Center for RPA Hub](https://www.servicenow.com/docs/access?context=whats-new&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

Learn about the newly released features of RPA Hub in your instance.

If new content is available for you, the blue indicator on the **Help Center** button notifies that the feature content is new and unread by you on your instance.


</td></tr><tr><td>

Regulatory Change Management

</td><td>

-   **[Assign rule-based regulatory alerts](https://www.servicenow.com/docs/access?context=set-up-assignment-configuration&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Define the routing rules to automatically distribute regulatory alerts to internal stakeholders. You can apply conditions to filter incoming regulatory feeds by Title, Description, Key dates, and many other fields. You can also auto-assign filtered regulatory alerts to domain experts for further review.

-   **[Add an AI-recommended citation to a regulatory alert](https://www.servicenow.com/docs/access?context=add-recommended-citations-to-a-regulatory-alert&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Add AI-powered recommendations from the most relevant citations through incoming regulatory changes, authority documents, child citations, and related control objects. You can drill down into the recommendations to explore the details within the context of the alert.


</td></tr><tr><td>

Resource Management Workspace

</td><td>

-   **[Resource Management Workspace](https://www.servicenow.com/docs/access?context=rsrc-mgmt-wrkspc&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

View updates to any approved task by using the new iconography. Use the Group By feature to group resources on a board.

-   **[Create a resource card](https://www.servicenow.com/docs/access?context=rmw-create-rsrc-card&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US) in Resource Management Workspace**

Create resource cards in Resource Management Workspace to filter and view resources by primary attributes or project item of work. Use the **Unassigned tasks** toggle to create a custom filter and view the unassigned tasks in the bottom tray.


-   **[Create resource assignments and operation resource assignments in Resource Management Workspace](https://www.servicenow.com/docs/access?context=create-ra-rmw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Resource Managers and Project Managers can directly create resource assignments and operational resource assignments from the resource board view to allocate, and approve the efforts.

-   **[Manage unassigned and assigned tasks](https://www.servicenow.com/docs/access?context=allocate-resources-rmw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Assign the unassigned tasks from the bottom tray and approve the assigned tasks from the top tray.


-   **[Split resource a assignment](https://www.servicenow.com/docs/access?context=split-resource-assignment-rmw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US), [Reassign or unassign the assigned tasks](https://www.servicenow.com/docs/access?context=rmw-reassign-unassign-work&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Split a resource assignment to create a duplicate assignment from a specific date. Resource managers can assign this split work to other resources with the same primary attributes. Reassign the assigned tasks from the primary resource to another resource who has the same primary attributes to manage the primary resource's work load, resource time offs, or to allocate operational work.


</td></tr><tr><td>

Retail Operations

</td><td>

-   **[Retail data model](https://www.servicenow.com/docs/access?context=rahi-retail-data-model&version=xanadu&pubname=xanadu-retail-industry&ft:locale=en-US)**

Optimize retail operations by modeling the hierarchical structure of your retail organization.

-   **[Retail case type](https://www.servicenow.com/docs/access?context=rahi-retail-case&version=xanadu&pubname=xanadu-retail-industry&ft:locale=en-US)**

Use the retail case type to manage in-store issues effectively.

-   **Store support portal**

Use the Store Support Portal for retail to utilize self-service tools.


</td></tr><tr><td>

Sales Agreement Management

</td><td>

-   **[Sales Agreement Management application](https://www.servicenow.com/docs/access?context=sales-agreement-mgmt&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

Create sales agreements from quotes to capture the scope and conditions for future sales transactions between a buyer and a seller.​ A sales agreement contains information such as details about the buyer and seller, the validity period of the agreement, and the quantities​ and pricing of the products and services.


</td></tr><tr><td>

Security Center

</td><td>

-   **[Security Event Notifications](https://www.servicenow.com/docs/access?context=security-policies&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

Receive prompt notifications on user behaviors that you specify with the Security Event Notifications tool. Users that you choose receive email notifications when a policy is triggered, enabling you to promptly remediate issues.

-   **[Security Posture Dashboards](https://www.servicenow.com/docs/access?context=scc-sec-posture-dashboard&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

Monitor the security health of all your instances with the Security posture dashboards. The single instance dashboard provides graphical widgets for key security key process indicators \(KPIs\). The multi-instance dashboard, only available on production instances, shows the same KPIs for all instances in a table format. The dashboards can be cloned and then fully customized.

-   **[Security banner announcements](https://www.servicenow.com/docs/access?context=scc-banner&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

Prepare for potential future security announcements from ServiceNow using the Security Banner Announcements. This feature enables ServiceNow to trigger new banners in customer instances that are visible to system administrators. These messages inform them of new and urgent potential security issues and include a link to more details.

-   **[Data Classification](https://www.servicenow.com/docs/access?context=data-classification-security-metrics&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

Monitor your sensitive data with the Data Classification metrics in the Security Metrics tool. Updates to the tool include two new metrics. Classifiable Data metrics displays the amount of data that is available for classification and what portion has been already classified. The Classified Data metrics displays the breakdown of the classified data across your classification labels.

-   **[Security Center version 2.0 introduces a new set of hardening settings](https://www.servicenow.com/docs/access?context=hardening-settings-baseline&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

Security Center version 2.0, introduced in the November store release, includes several new hardening settings, updates to existing ones, and the removal of some unnecessary settings. The new hardening settings come with recommended configurations to restrict access control lists \(ACLs\) for human resources apps, minimizing data exposure and enforcing the principle of least privilege. Additional settings help configure service portal widgets to reduce sensitive data exposure in tables, enforce strict code signing, and set role-based restrictions on apps. Several technical configuration names and descriptions have been updated for clarity, and outdated hardening settings have been removed.

-   **[Improved Security Center architecture](https://www.servicenow.com/docs/access?context=sec-center-v2&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

The Security Center has been redesigned to help admins understand what tasks they can accomplish with Security Center and to pick the right tools for their tasks.


</td></tr><tr><td>

Security Incident Response

</td><td>

-   **[Security Incident Response integration with AWS Security Hub](https://www.servicenow.com/docs/access?context=aws-security-hub-integration&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Security Incident Response supports the AWS Security Hub findings integration. This enables you to ingest AWS Security Hub findings and automatically create security incidents in Security Incident Response.

Security Incident Response supports a bidirectional exchange of data with AWS Security Hub. SIR ingests findings from AWS Security Hub to create aggregated security incidents. Simultaneously, any change in a security incident is also updated on the related AWS Security Hub findings.

-   **[Internet Content Adaption Protocol \(ICAP\) integration for DLP IR](https://www.servicenow.com/docs/access?context=icap-dlp-integration&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Internet Content Adaption Protocol \(ICAP\) integration helps you to track the usage and movement of sensitive data on various platforms.

    -   Configure and schedule DLP alerts ingestion from the specified Amazon S3 buckets which includes the capability to perform the delta imports to ensure only new or modified data is ingested.
    -   Display the ingested alerts in the DLP workspace by providing the key details on each alert such as the match content, alert severity, and relevant metadata.
    -   Download associated evidence files directly from the DLP workspace for further investigation or review.
    -   Enable users to apply automatic responses based on predefined criteria such as alert escalation, notifications, or enforcement policies.
    -   Remediate response actions such as blocking or quarantining sensitive data, or sending out alerts to stakeholders.
    -   Customize and define the severity mapping between ICAP DLP incidents with ServiceNow incidents.
-   **[Playbook for zero-day vulnerability](https://www.servicenow.com/docs/access?context=playbook-for-zero-day&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Get step-by-step procedure to address and mitigate zero-day threats—vulnerabilities in the software that are unknown to the vendor, leaving systems exposed to attacks.

-   **[Configure Shift Handover Templates](https://www.servicenow.com/docs/access?context=configure-shift-handover-templates&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Provide detailed communication of critical information, tasks, and updates between outgoing and incoming personnel for a seamless transition between shifts by using the Shift Handover feature. Improve operational continuity, reduce errors, and increase overall efficiency in the workplace.

-   **[Configure Slack chat connector for major security incidents](https://www.servicenow.com/docs/access?context=configure-slack-chat-connector-msi&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

View and filter collaboration chat activities on Slack to more efficiently collaborate to resolve major security incidents.

-   **[Playbook for Legal Request](https://www.servicenow.com/docs/access?context=playbook-legal-request&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Get step-by-step guidance on how you can inform the legal team about the latest summary of a major security incident so they can notify the SEC in the 4-day time frame that is required for material breaches.

-   **[Add Zscaler Internet Access URL category lists](https://www.servicenow.com/docs/access?context=create-zscaler-internet-access-url-category-manually&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Enable Zscaler approvers to add observables to the list of required approvals or remove them when the Require Approval option is selected.

-   **[Configure how an automatic event is created](https://www.servicenow.com/docs/access?context=configure-automatic-event-creation-profile&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) and [MISP event data](https://www.servicenow.com/docs/access?context=misp-event-data&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Add security tags during automatic MISP profile configuration.

-   **[Mapping DLP incident status with Netskope](https://www.servicenow.com/docs/access?context=map-incident-status&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Provide the mappings between the DLP Incident status in your ServiceNow instance and the Netskope Object status.

-   **[Define the new Risk Score Calculator Rules](https://www.servicenow.com/docs/access?context=define-risk-score-calculator-rules-sir&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

The Risk score configuration in the Security Incident Response workspace has been enhanced with the following capabilities:

    -   Set up a Risk Score Calculator from either script or condition builders.
    -   Apply multiple conditions while setting up rule-based scoring.
    -   Apply weightage to each scoring line. Weights should add up to 100.
    -   For rule-based scoring, select table fields and values for setting up a condition.
    -   Capture conditions and scoring via scripts.
    -   Manually execute risk score calculators to recalculate after making changes.
-   **[Managing MSIM status reports](https://www.servicenow.com/docs/access?context=reports-and-metrics&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Share mobile-friendly Executive Status Reports with users outside your ServiceNow instance, including third-party vendors, other entities, or email distribution lists.


</td></tr><tr><td>

Security Posture Control

</td><td>

-   **[Mitigation Controls Monitoring with Security Posture Control](https://www.servicenow.com/docs/access?context=spc-mitigation-exploring&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

From within the Security Posture Control workspace, detect mitigation controls of various types as described by MITRE on all on-premise and cloud enterprise assets. Gain insight into which threats to your assets are mitigated by available mitigation controls based on how various security tools are configured.

    -   Activate mitigation control policies that are included with the application that identify MITRE mitigations on your assets.
    -   Identify your assets that have Web Application Firewall \(WAF\) protection with supported tools that include F5 BIG-IP. Automatically map a WAF mitigation to vulnerable items by analyzing the policy signatures in the firewall and the Common Vulnerabilities and Exposures \(CVE\) information.
    -   Identify exploit mitigation controls from endpoint protection or Endpoint Detection and Response \(EDR\) tools like CrowdStrike and Microsoft Defender. Automatically map the EDR exploit mitigation controls to relevant vulnerable items by analyzing the vulnerability information and the EDR mitigation control configuration.
    -   Populate vulnerable items with relevant attributes that can be used in your Vulnerability Response risk calculator rules.
    -   Import agent information from the SentinelOne product into your ServiceNow AI Platform® with the [Service Graph Connector for Sentinel One](https://www.servicenow.com/docs/access?context=sgc-sentinelone-integration&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
    -   Import asset data from the Splunk product into your ServiceNow AI Platform® with the [Service Graph Connector for Splunk](https://www.servicenow.com/docs/access?context=sgc-splunk-integration&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
-   **[Enhancements to custom insights in the Security Posture Control Workspace](https://www.servicenow.com/docs/access?context=spc-custom-insight-overview&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

The name of the Custom insights module has been changed to the Configured insights module in the Security Posture Control Workspace.

You must assign groups to organize your reports by categories when you create custom insight records. Groups determine where your data visualizations are displayed on the dashboard in the Configured insights module according to the criteria you set.

-   **[Enhancements to the Condition policy builder in the Policies and findings module](https://www.servicenow.com/docs/access?context=spc-create-policy&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Select **With aggregated data** for **Connection** to ensure that your policy matches assets that have slight variations in reported data. The following properties for policies for hardware assets are supported as they’re reported by different sources:

    -   Host name
    -   FQDN
    -   OS
    -   OS Version
    -   OS Domain
    -   OS Service Pack
-   **[Test result and remediation task state transitions](https://www.servicenow.com/docs/access?context=spc-findings-state-transition&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Enhancements to policy audits ensure that retired assets are not evaluated by activated policies. If the state of an asset transitions from **Retired** back to **Active**, it is included in the next policy evaluation.


</td></tr><tr><td>

Service Catalog

</td><td>

-   **[Added inline render type support of catalog item in Virtual Agent](https://www.servicenow.com/docs/access?context=request-topic-blocks-va&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Fill a catalog item form inline in the Virtual Agent powered by Natural Language Understanding \(NLU\).

For example, while requesting a catalog item that’s marked inline render type, the requester can fill the item and its options within the Virtual Agent conversation.


</td></tr><tr><td>

Service Exchange

</td><td>

-   **[Service Exchange mismatched version support](https://www.servicenow.com/docs/access?context=service-bridge-v2-mismatch-version&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US)**

Providers and consumers can run different versions of the Service Exchange applications without affecting their ability to exchange data. Providers can adopt new features without coordinating their application upgrades with their consumers.

-   **[Configuration revisions](https://www.servicenow.com/docs/access?context=service-bridge-v2-config-revision&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US)**

Providers can develop and deploy new versions or revisions of entitlements with updated functionality to compatible consumers without affecting consumers who have not updated their application. Consumers can therefore use older revisions of entitlements including remote task definitions, remote record producers, and foundation data sync offerings while deploying new revisions.

-   **[Consumer pre-flows](https://www.servicenow.com/docs/access?context=service-bridge-v2-conf-consumer-flow&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US)**

Consumers can control data synchronization with their providers by associating a flow with a Service Exchange remote record producer and run consumer-defined processes, such as approvals, before a task is synchronized to their provider.

-   **[Integration with Sales Customer Relationship Management](https://www.servicenow.com/docs/access?context=service-bridge-v2-omt-intg&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US)**

Providers can enable customers to quickly order entitled Sales Customer Relationship Management product offerings from their service catalog by publishing them as remote record producers on consumer instances.


</td></tr><tr><td>

Service Graph Connector Integration for Claroty CTD

</td><td>

-   **[View the class mappings available for the Service Graph Connector](https://www.servicenow.com/docs/access?context=sgc-claroty-ctd-classes&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Use the **Claroty CTD SGC Class Mappings** table to view the available class mappings and targeted CMDB classes.

-   **[Avoid importing empty rack slots](https://www.servicenow.com/docs/access?context=configuring-sgc-claroty-ctd-guided-setup&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

During import, empty rack slots are removed to avoid importing them into the CMDB.

-   **[Capture firmware version of devices](https://www.servicenow.com/docs/access?context=sgc-claroty-ctd-classes&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Use the Firmware Installation \[cmdb\_firmware\_install\] table to capture the firmware version of your Service Graph Connector Integration for Claroty CTD devices.

-   **[Use the ire\_criterion\_attribute in the OT Entity \[cmdb\_ot\_entity\] table](https://www.servicenow.com/docs/access?context=sgc-claroty-ctd-classes&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

The ire\_criterion\_attribute acts as a criterion attribute for an OT entity-related entry and helps avoid entity update issues.

-   **[Clean up serial number data](https://www.servicenow.com/docs/access?context=sgc-claroty-ctd-classes&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Clean up the serial number \[cmdb\_serial\_number\] records imported into the Source \[sys\_object\_source\] table from the Service Graph Connector Integration for Claroty CTD with a fixed script. This script establishes that a null pointer exception doesn't occur when the serial number and MAC address are the same. The script runs automatically when the plugin is upgraded.

-   **[Categorize your OT devices into the industrial product model category](https://www.servicenow.com/docs/access?context=model-categories-for-ot&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

The enhanced Service Graph Connector Integration for Claroty CTD creates assets in the Industrial product model category for OT class devices. This enables compatibility with the Enterprise Asset Management product for full lifecycle management of OT class devices.


</td></tr><tr><td>

Service Graph Connector for Microsoft Defender for IoT \(Azure\)

</td><td>

-   **[Categorize your OT devices into the industrial product model category](https://www.servicenow.com/docs/access?context=model-categories-for-ot&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

The enhanced Service Graph Connector for Microsoft Defender for IoT \(Azure\) creates assets in the Industrial product model category for OT class devices. This enables compatibility with the Enterprise Asset Management product for full lifecycle management of OT class devices.


</td></tr><tr><td>

Service Operations Workspace for ITSM

</td><td>

-   **[Admin Center changes](https://www.servicenow.com/docs/access?context=manage-admin-console-sow-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**
    -   Migrate your ITSM Agent Workspace features to Service Operations Workspace by using the on-screen utility without having to rebuild these features. This migration includes customizations done on ITSM Agent Workspace for various forms, UI actions, and lists.
    -   Configure the availability and order of the contextual side panel tabs in record pages.
    -   Configure modern Change Management features from the Service Operations Workspace Admin Center to increase change efficiency, accelerate change approvals, drive data-driven risk analysis, and leverage DevOps data for change automation.
    -   Configure the visibility settings of the **Overview** tab for each problem record state.
    -   Configure the visibility settings of the **Overview** tab in the incident record page for tier 1 agents from the Incident record section of Incident Management in Admin Center.
    -   Configure Service Desk assisted Password Reset to accomplish the following tasks:
        -   Assign the password reset service desk role to the user.
        -   Create a credential store record to configure access to your credential store server while a user is changing or resetting a password.
        -   Configure the verification methods for the service desk process.
        -   Configure the password policies.
    -   Starting in version 6.1, you can do the following actions from the SOW Admin Center:
        -   Configure Interaction Management in SOW.
        -   Browse through a collection of SOW learning resources to help users understand more about SOW configuration.
-   **[Granular roles](https://www.servicenow.com/docs/access?context=roles-in-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Configure the user access for various record pages in Service Operations Workspace for ITSM by using the following granular roles, and the user’s access to these record pages is based on the role assigned.

    -   Incident: sn\_incident\_read and sn\_incident\_write
    -   Request: sn\_request\_read, sn\_request\_write
    -   Problem: sn\_problem\_read, sn\_problem\_write
    -   Change: sn\_change\_read and sn\_change\_write
Because these granular roles inherit the sn\_sow.sow\_home and sn\_sow.sow\_list roles, the users with the granular roles can access the Service Operations Workspace for ITSM home and list pages.

**Note:** When upgrading to Xanadu, the email\_composer user role is added to the users along with the respective granular roles. The time to add the role depends on the number of users having the granular roles for write function and impacts the overall instance upgrade time. Adding the email\_composer user role ensures that the granular write users have access to the email templates in SOW.

-   **[Interaction record page enhancements](https://www.servicenow.com/docs/access?context=create-interactions&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

View the requester's details, their assets, recent interactions, and related links from the Opened for card. This centralized access point provides an agent with a comprehensive overview to efficiently manage the requester's information.

To streamline the workflow and maintain focus on interactions, a modal-based interface for record association is implemented for the interaction record in Service Operations Workspace. This interface simplifies the workflow by automatically suggesting tables that are frequently associated with Interactions, including the change, incident, knowledge, problem, and request. This enhancement is designed to streamline operations and enhance user efficiency.

Starting in version 6.1, view all available metrics of the requester’s assets that are collected through the Digital End-User Experience \(DEX\) architecture from the interaction record.

-   **[Incident record page enhancements](https://www.servicenow.com/docs/access?context=view-update-inc-overview-tab&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

The incident record page has the following enhancements:

    -   View the Configuration Item \(CI\) dependency for the following reference fields:
        -   Configuration item
        -   Service
        -   Service Offering
    -   View the VIP field decorator for a caller field in the **Details** tab and in the **Record information** tab of the contextual side panel for VIP users.
    -   Search and filter the configuration items \(CI\) that are based on the configuration class when you add the affected CIs to an incident record.
    -   When an agent reports a knowledge gap from an incident record, the success message that contains the created knowledge feedback task record link is displayed. You can select the link to open the knowledge feedback task record on a separate tab to provide the information and create an article for the knowledge gap.
    -   For issues related to Password Reset, you can now select **Password Reset** as the incident category. After this category is set and the incident record is saved, you can resolve the incident by using the Reset password UI action. For more information on Password Reset, see [Password Reset in SOW](https://www.servicenow.com/docs/access?context=exploring-password-reset-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).
    -   Starting in version 6.1, the incident record has the following enhancements:
        -   The activity stream displays the activity information in tiles that are collapsible. By default, the first activity tile, either a work note or comment, is expanded and the consecutive tiles are collapsed. This ensures a clean UI and enables you to expand and view the activity information when required. It ensures a clean UI and enables you to view the activity information when required. To enable this feature, set the **Enable the expandable activity stream tiles** \(**enableExpandableActivityStreamTiles**\) UX page property to `true`.
        -   An internal tag is added to the work notes.
        -   You can define, customize, and apply tags to the activity streams. These tags help you filter the activity based on the tags. You can use the **Activity stream property** \(**activitystreamprops**\) property to define and customize your tags.
        -   Add related interaction records to an incident from the Interactions related list of the **Related records** tab.
        -   Resolve cases or support issues faster and more efficiently with response templates. Access the response templates \(formerly known as templated snippets\) from the contextual side panel of an incident record to quickly copy the reusable messages and provide quick and consistent messages to users, or to display standard chat response messages to the requesters in chat.
        -   Use the **Opened By** field in the Origin card of the Record information side panel tab of an incident to view the user who created the incident's origin record.
        -   Use the **Type** field in the Origin card of the Record information side panel tab of an incident to view the channel type of the incident's origin record. For example, if the origin is an interaction record, the type can be Chat.
        -   If an incident is created from an interaction record, you have the following options:
            -   View chat transcript: View the chat history with the caller of the interaction record. This option is available only if the interaction record is of the Chat type and is in Closed complete or Closed Abandoned state.
            -   View work notes: View the work notes history of the interaction record.
-   **[Announcements for a major incident](https://www.servicenow.com/docs/access?context=create-announcements-major-inc&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Keep your users informed about an ongoing major incident by broadcasting communication messages about it. Create and configure announcements from the **Communicate** tab of the major incident record. Announcements can appear in an announcement banner or an announcement widget that users can view on their IT service portal.

-   **[Major incident record enhancements](https://www.servicenow.com/docs/access?context=review-update-pir-mim-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Starting in version 6.1, you can do the following:

    -   View the information on the **Post incident report** tab using the incident management granular roles such as sn\_incident\_read and sn\_incident\_write.
    -   Flag events on the activity stream of a major incident to include them in the post incident report events timeline.
    -   Access the Collaborate side panel tab and its features from the incident communication task \(ICT\) record associated with the major incident record.
    -   Select or change the SMS templates for the major incident SMS communication to the required end users with the following roles:
        -   major\_incident\_manager
        -   sn\_incident\_write user who has the required communication related roles
        -   ITIL user to whom the major incident is assigned
-   **[Automatic closure of an interaction from an incident](https://www.servicenow.com/docs/access?context=view-update-inc-overview-tab&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Starting in version 6.1, when an incident record created from an interaction record is resolved, the interaction record is automatically set to **Wrap up** or **Closed complete** state. You must set the **Auto close the origin interaction** \(**sn\_sow\_inc.autoclose\_origin.interaction**\) system property to `true` and the **Close interaction from incident** business rule must be `Active`.

-   **[SOW list page enhancements](https://www.servicenow.com/docs/access?context=incident-list-page&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Starting in version 6.1, you can do the following:

    -   View the user who updated the incident record using the **Updated** column on the SOW incident list page.
    -   Copy the sys ID or the URL of a record from the SOW list page to share with other agents, enabling quicker resolution of the issue.
    -   Configure the **fuzzyCount** property to display the number of records on the list page.
-   **[Collaboration in Problem Management](https://www.servicenow.com/docs/access?context=problem-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Starting in version 6.1, you can chat or make calls to communicate with stakeholders using the [**Collaborate** option in the contextual side panel](https://www.servicenow.com/docs/access?context=collaboration-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US) of problem and problem task records.

-   **[Change Management enhancements](https://www.servicenow.com/docs/access?context=change-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Starting in 6.1, you can do the following:

    -   Find your change model or template when raising new changes by using the enhanced filtering and search capabilities for the Standard Change Catalog.
    -   Manage the Standard Change life cycle.
    -   Propose, modify, and retire Standard Change templates.
    -   Propose mass configuration item \(CI\) updates.
    -   Propose changes to single CIs.
    -   Automate the update and audit trail of CIs, with mass updates and change proposals recording the attributes being changed and \(optionally\) updating the CMDB automatically.
-   **[Quick start tests for Incident Management in Service Operations Workspace for ITSM](https://www.servicenow.com/docs/access?context=quick-start-tests-im-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Incident Management features work as expected. If you customized Incident Management, copy quick start tests and configure them for your customizations. The following quick start tests are added for Incident Management in Service Operations Workspace for ITSM:

    -   Create problem from incident: Enables you to test the problem creation from an incident by using the Create problem UI option.
    -   Verify Assign to me button functionality: Enables you to test the incident assignment by using the Assign to me UI option.
-   **[Password Reset in Service Operations Workspace for ITSM](https://www.servicenow.com/docs/access?context=exploring-password-reset-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Assist users to quickly access their accounts by enabling them to reset the user password.

-   **[Exploring Recommended Actions for ITSM in Service Operations Workspace](https://www.servicenow.com/docs/access?context=exploring-recommended-actions-for-itsm-in-service-operations-workspace&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Manually search for AI-powered recommendations that assist in swiftly addressing issues. AI-enhanced search results are available for these record types: incident, incident task, problem, problem task, change request, change request task, interaction, and request.

-   **[__Overview__ tab for problem records](https://www.servicenow.com/docs/access?context=problem-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Configure how and what information is displayed in the sections of the dynamic **Overview** tab for each problem state.

-   **[Manage life cycle of problem tasks](https://www.servicenow.com/docs/access?context=work-on-problem-task-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Provide additional flexibility for problem task analysts, including the ability to reassess problem tasks from the Work in Progress state.

-   **[Initial support for problem models](https://www.servicenow.com/docs/access?context=problem-mgmt-models-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Introduction of Problem Management models, one default problem model \(General\) and two default problem task models \(Root cause analysis and General\).

The default models are equivalent to the base life cycle in the Xanadu release. This initial support enables you to create custom models to tailor additional scenarios for specific use cases.

**Note:**

If you’re using Service Operations Workspace 5.x and you enable Problem Management models, you manage problems and problem tasks in the classic UI16 experience, rather than in Service Operations Workspace.

Service Operations Workspace 6.x is based on the Xanadu release and it supports Problem Management models.

-   **[Shortcuts for creating fix tasks from a problem](https://www.servicenow.com/docs/access?context=problem-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Use the following shortcuts from the **Overview** tab of a problem:

    -   **Create defect** \(part of Agile Development 2.0\)
    -   **Create enhancement** \(part of Agile Development 2.0\)
    -   **Create improvement initiative** \(part of Continual Improvement Management\)
-   **[Guided tours](https://www.servicenow.com/docs/access?context=explore-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Learn about Service Operations Workspace for ITSM through a sequence of interactive steps that guide you through a specific concept or process.

Starting in version 6.1, the following guided tours are available:

    -   Overview of the PAR dashboard
    -   Overview of the various tabs and actions of an incident record page.
    -   Generate and download a post incident report for sharing it with all the stakeholders.
    -   Overview of the various tabs and actions of a problem record page.
    -   Get tailored recommendations for problems
    -   Get tailored recommendations for interactions
    -   Get tailored recommendations for requests
-   **[Add approvers to approve a request](https://www.servicenow.com/docs/access?context=add-approvers-request-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Starting in version 6.1, to expedite the process and effectively meet the user's request, you can add one or more approvers to the request or to a specific request item. This helps to streamline the approval workflow and ensure that the user's needs are fulfilled quickly and efficiently.


</td></tr><tr><td>

Service Portal

</td><td>

-   **[Deactivate portals](https://www.servicenow.com/docs/access?context=deactivate-portal&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

Turn off access to a portal that you don't want users to visit and redirect them to another portal.


</td></tr><tr><td>

Service Portfolio Management

</td><td>

-   **[Set the time zone for availability results in Service Portfolio Management](https://www.servicenow.com/docs/access?context=SPM2-set-timezone&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Set the availability system property \[com.snc.availability.v2\] to true so you can set the time zone that you want to calculate availability results. The Availability calculations settings page provides you with the choice to calculate availability using the service offering commitment time zone \(yes or no\). It also provides you with the option to set the global availability time zone by selecting a time zone from a provided list. After you select **Yes** to calculate availability with the commitment time zone, the **Time zone** field on the commitment record is used to calculate the availability results. The **Time zone** field on the availability record is read only. After you opt to set the global time zone, all the availability results will use the time zone that you set as global.

**Note:** The underlying system properties that govern the global time zone and the commitment time zone are exclusive. You can set the global time zone or set the time zone to reflect a service offering commitment but you can't set both at the same time.

-   **[Assign multiple teams to support a service offering in Service Portfolio Management](https://www.servicenow.com/docs/access?context=spm2-assign-teams&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Use the added Teams related list in service offerings to assign different group types to support a service offering. The related list functionality is an existing platform feature that was added to the Service Portfolio Management application so you can see the related support teams in the Digital Portfolio Management view. For more information on the platform feature, see [Teams related list](https://www.servicenow.com/docs/access?context=teams-related-list&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).


</td></tr><tr><td>

Service Reliability Management

</td><td>

-   **[Service Reliability Management](https://www.servicenow.com/docs/access?context=sr-landing-page&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) and [Service Level Objective Management](https://www.servicenow.com/docs/access?context=slo-landing-page&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Explore the Service Reliability Management and Service Level Objective Management pages in the Service Operations Workspace.


</td></tr><tr><td>

ServiceNow IDE

</td><td>

-   **[Work in an IDE based on Visual Studio Code for the Web](https://www.servicenow.com/docs/access?context=servicenow-ide-user-interface&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Create and develop applications in a familiar integrated development environment based on Visual Studio Code for the Web. The ServiceNow IDE has many of the same features as Visual Studio Code, including type safety, IntelliSense, dependency enforcement, code search, and source control integration.

-   **[Build scoped applications in source code](https://www.servicenow.com/docs/access?context=servicenow-fluent&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Write source code to define the metadata that makes up applications using ServiceNow Fluent. ServiceNow Fluent is a domain-specific programming language with APIs for defining the different types of application metadata. Developing applications in source code enables you to work in familiar development environments, create and modify complex applications, manage code in source control more easily, and catch errors at build time. Language processing and validation for ServiceNow Fluent is included in the ServiceNow IDE by default.

-   **[Create and use JavaScript modules and third-party libraries](https://www.servicenow.com/docs/access?context=create-use-javascript-modules-ide&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Organize and reuse code within scoped applications with custom JavaScript modules and third-party JavaScript utilities.

-   **[Collaborate on applications with users of different skill sets](https://www.servicenow.com/docs/access?context=developing-applications-servicenow-ide&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Collaborate on an application with users of different skill sets at the same time from the ServiceNow IDE and other ServiceNow AI Platform builder tools and interfaces. Developers build applications to compile source files into metadata, which they can view in embedded ServiceNow AI Platform user interfaces. Developers can synchronize applications to pull in changes to application metadata from other interfaces into source code.

-   **[Manage applications in source control](https://www.servicenow.com/docs/access?context=integrating-source-control-servicenow-ide&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Integrate with remote Git repositories to use source control in the ServiceNow IDE. Use basic authentication or OAuth 2.0 to connect to remote Git providers and repositories.


</td></tr><tr><td>

ServiceNow SDK

</td><td>

-   **[Turn off synchronizing changes to ServiceNow Fluent code](https://www.servicenow.com/docs/access?context=servicenow-fluent&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Turn off synchronizing changes to ServiceNow Fluent objects or files using the `@fluent-disable-sync` or `@fluent-disable-sync-for-file` comment directives.


-   **[Authenticate to an instance using OAuth 2.0](https://www.servicenow.com/docs/access?context=authenticate-instance-now-sdk&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Authenticate to a ServiceNow instance using OAuth 2.0 by setting the `type` parameter on the `now-sdk auth` command to `oauth`.

-   **[Ignore ServiceNow Fluent diagnostics](https://www.servicenow.com/docs/access?context=servicenow-fluent&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Suppress ServiceNow Fluent and TypeScript diagnostics using the `@fluent-ignore` comment directive.


-   **[Build scoped applications in source code](https://www.servicenow.com/docs/access?context=servicenow-fluent&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Write source code to define the metadata that makes up applications using ServiceNow Fluent. ServiceNow Fluent is a domain-specific programming language with APIs for defining the different types of application metadata. Developing applications in source code enables you to work in familiar development environments, create and modify complex applications, manage code in source control more easily, and catch errors at build time.

-   **[ServiceNow Fluent Language server in Visual Studio Code](https://www.servicenow.com/docs/access?context=install-fluent-language-extension-vs-code&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Get language processing and validation for ServiceNow Fluent in Visual Studio Code by installing the ServiceNow Fluent Language server from the Visual Studio Code Marketplace.


</td></tr><tr><td>

ServiceNow Studio

</td><td>

-   **[Consolidated access to all integrated ServiceNow® builders and tools](https://www.servicenow.com/docs/access?context=integrated-development-tools&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Use all of your favorite ServiceNow builders and tools in one place, without opening them in different products. For example, you can open files for flows in the Workflow Studio tool directly within ServiceNow Studio.

-   **[Work with all supported file types and metadata](https://www.servicenow.com/docs/access?context=sn-studio-working-with-metadata&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Use the Navigator panel to quickly find, bookmark, and edit any type of supported ServiceNow metadata.

-   **[Deploy updates within ServiceNow Studio](https://www.servicenow.com/docs/access?context=working-with-update-sets-in-servicenow-studio&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Manage your deployments using several of the ServiceNow app life-cycle options, such as pipelines, update sets, or the Application Repository, directly within ServiceNow Studio.

-   **[Generate apps using Now Assist](https://www.servicenow.com/docs/access?context=sns-now-assist-app-gen-landing&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Edit applications created with Now Assist for app generation directly in ServiceNow Studio.


</td></tr><tr><td>

Sidebar

</td><td>

-   **[Add user groups to Sidebar discussions](https://www.servicenow.com/docs/access?context=using-sidebar&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

In addition to individual users, you can now add user groups to Sidebar discussions.

-   **[Use Sidebar on Mobile Platform for agents](https://www.servicenow.com/docs/access?context=exploring-sidebar&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

If you're an agent, use Sidebar, which is now available on the Mobile Platform.

-   **[Create Sidebar discussions on all record types](https://www.servicenow.com/docs/access?context=exploring-sidebar&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Create Sidebar discussions on all record types, and not just on interaction and task-based records.

-   **[Use different expert finder services in Sidebar](https://www.servicenow.com/docs/access?context=configure-sidebar&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Use different expert finder services depending on where you access Sidebar from.

-   **[Use the chat summarization quick action](https://www.servicenow.com/docs/access?context=using-sidebar&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Generate a chat summarization by using a quick action.


</td></tr><tr><td>

Skills Intelligence

</td><td>

-   **[Skills Workspace](https://www.servicenow.com/docs/access?context=skills-intelligence-workspace&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

See how the Job architecture is currently structured and how job families and role groups and the skills related to them through the Job architecture view in Skills Workspace. Get a sense of issues that need to be fixed by looking at the node map.

Select role groups and skills from the recommendations displayed in the Skills Workspace.

Select and update Role level and skills through an interface for employees in Employee Portal.

Import and review skills through a dynamic and interactive playbook experience called Skill imports.


</td></tr><tr><td>

Skills Management

</td><td>

-   **[Using the Skills Management dashboard in the Next Experience user interface](https://www.servicenow.com/docs/access?context=using-skills-management&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Analyze the trends to assess the skill gaps in your organization by using the Next Experience user interface.

-   **[Multi-lingual capabilities in Skills Management](https://www.servicenow.com/docs/access?context=translating-skills-skills-management&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Translate the skill names and the descriptions by using the following fields that support the translated text data type in the Skill \[cmn\_skill\] table:

    -   **Display Skill Name**: Auto-populates the corresponding value in the **Name** field.
    -   **Description**

</td></tr><tr><td>

Smart Assessment Engine

</td><td>

-   **[Using the template designer](https://www.servicenow.com/docs/access?context=sae-template-designer&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

By using the template designer in Smart Assessment Engine, you can easily create assessment templates and add instructions, questions, and reference information to an assessment template.

    -   [Add instructions and questions to an assessment template](https://www.servicenow.com/docs/access?context=sae-asmnt-template-populate&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US): SAE supports the most commonly used question types such as radio buttons, check boxes, drop-down lists, and more. Smart assessments are highly customizable so that you can do the following tasks:
        -   Organize questions into sections and subsections for clarity.
        -   Add instructions to help the assessors understand the context and requirements of each question to improve the accuracy and relevance of the responses.
        -   Configure the question guidance texts to help the assessors answer questions.
        -   Configure the questions to appear or hide depending on the assessor's previous answers.
        -   Integrate the response justification prompts that provide the assessors with the explanations that are based on their selected responses.
        -   Require the assessors to attach the supporting documents like contracts, permits, or invoices that are based on the responses.
    -   [Add reference information to an assessment template](https://www.servicenow.com/docs/access?context=sae-asmnt-add-reference&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US): Incorporate the live data from the Assessment Scope as reference information to help ensure that the assessors have immediate access to the necessary information while they’re responding to the assessments. This live data minimizes the need for external references.
    -   [Create an assessment template category](https://www.servicenow.com/docs/access?context=sae-asmnt-template-category-create&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US): Create a template category as a container of related assessment templates. By creating an assessment template category, you can help to ensure that only authorized personnel can access and change the template.
-   **[Respond to assessments](https://www.servicenow.com/docs/access?context=sae-respond-to-asmnt&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Navigate through the assessments more efficiently by using a progress indicator that shows how much of the assessment is completed. The questions are paginated to help you more easily navigate the assessment. Your work is automatically saved, which eliminates the need for manual saving and helps to prevent data loss. You also have the option to reassign in-progress assessments to another user or cancel assessments that are no longer needed.

-   **[Trigger assessments](https://www.servicenow.com/docs/access?context=sae-asmnt-triggering&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Initiate an assessment by using the Trigger Smart Assessment flow action that is based on a published assessment template. You can assign an assessment to a designated assessor with a defined scope and deadline.

-   **[Combine multiple assessments into a single, unified submission](https://www.servicenow.com/docs/access?context=sae-asmnt-combine&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Combine multiple assigned assessments into a single, streamlined view. You can efficiently manage, submit, or reassign these combined assessments at one time. You can use features, like Bulk Submit or Bulk Reassign, to handle all assessments in one action.

-   **[Domain-separated Deployment](https://www.servicenow.com/docs/access?context=sae-domain-separation&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Domain separation in the Smart Assessment Engine is supported starting with the Xanadu release, enabling data, processes, and administrative tasks to be organized into distinct domains. Within this framework, templates are separated by a process, while assessments are separated by data, helping to ensure controlled access and visibility according to the domain.

-   **[Migrate legacy assessment metric types to Smart assessment templates](https://www.servicenow.com/docs/access?context=sae-asmnt-template-migrating&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Migrate existing assessment designs from the ServiceNow® Assessments and Surveys application. Your templates are automatically transferred as drafts with just one click. After you migrate the designs, you must review and publish these drafts, and confirm the results. The sets of questions in the Assessments and Surveys application are saved as metric types. When migrated, these metric types are saved as question types. Custom, Duration, Image scale, Percentage, Rankings, and Ratings question types aren’t supported for migration.


</td></tr><tr><td>

Software Asset Management

</td><td>

-   **[Direct integration support for the Tableau Cloud application](https://www.servicenow.com/docs/access?context=integrate-with-tableau-cloud&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Gain visibility into the subscriptions and reclaim stale licenses by integrating your ServiceNow instance with the Tableau Cloud application.

-   **[Gain a complete view of your GitHub Enterprise Cloud Subscriptions](https://www.servicenow.com/docs/access?context=integrate-github-cloud&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Take advantage of the enhanced ability to optimize your GitHub Enterprise Cloud subscriptions, including outside collaborators, pending invitations, and pending outside collaborators.

-   **[Minimize cost while optimizing Smartsheet subscriptions without the need for the Event Reporting add-on](https://www.servicenow.com/docs/access?context=create-integration-profile&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Optimize your Smartsheet subscriptions without the additional Smartsheet Event Reporting add-on. Use the Smartsheet integration to retrieve the last login information, enabling you to analyze the subscriptions that aren't used efficiently, reducing software spend for Smartsheet.

-   **[Integrate your SaaS applications with minimal user permissions](https://www.servicenow.com/docs/access?context=create-integration-profile&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Minimize security risks and protect information by granting access only to the necessary user or API permissions for optimizing SaaS licenses.

-   **[Get visibility into the login-based licenses of Salesforce CRM applications](https://www.servicenow.com/docs/access?context=integrate-with-salesforce-crm&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Gain insights into the number of Salesforce CRM login consumptions without the need to create user subscriptions.

-   **[License your organization for Oracle Java SE Universal with the Employee license metric](https://www.servicenow.com/docs/access?context=oracle-publisher-pack&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

License all your employees that are using Oracle Java SE Universal with the Employee license metric. The tier-based licensing model also supports licensing discounts.

-   **[Expand your analysis of asset information using the export capabilities in the Software Asset Workspace](https://www.servicenow.com/docs/access?context=sam-workspace&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Gain more insights and streamline operations with support for exporting asset information from the Software Asset Workspace.

-   **[Improve Software Asset Management licensing outcomes with actionable insights into discovered inventory](https://www.servicenow.com/docs/access?context=analytics-workspace&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Gain insights into discovered inventory, normalization, EOL software products, software version, and edition proliferation in your estate. Act to improve normalization, reduce version and edition proliferation, and remediate EOL software.

-   **[Expand your analysis of overlapping software usage with added insights from spend transactions](https://www.servicenow.com/docs/access?context=app-ration&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

View data related to spend transactions in the Overlapping usage view in Software Asset Workspace. You can gain insights into the combined data from applications including spend detection, Direct integration profiles, and SSO integration profiles.

-   **[Determine license compliance for Microsoft Windows Server, SQL Server, and RHEL Server deployed on Nutanix virtualization technology](https://www.servicenow.com/docs/access?context=software-recon-virt-tech&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Address your license compliance requirements for Microsoft Windows Server, SQL Server, and RHEL Server with deployments on Nutanix virtualization technology.

-   **[Reduce manual effort for managing Microsoft Windows Server Client Access Licenses \(CAL\) with automated usage tracking](https://www.servicenow.com/docs/access?context=user-device-license-consumption&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Track and manage the users and devices that are accessing your server software using ServiceNow® Discovery and use the automatic base CAL creation support for Microsoft Windows Server.

-   **[Optimize Microsoft Visio, Project Online, and Microsoft 365 Copilot subscriptions on the Microsoft 365 Admin Center](https://www.servicenow.com/docs/access?context=microsoft-o365&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Track the usage of Microsoft Visio, Project Online, and Microsoft 365 Copilot subscriptions through the Microsoft 365 Admin Center and create reclamation candidates for any unused subscriptions. Additionally, you can monitor blocked users across all subscriptions who are consuming licenses for potential removal.

-   **[Improve licensing accuracy for software suites with additional configuration for detecting software suites](https://www.servicenow.com/docs/access?context=software-suites-inference&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Improve licensing accuracy for software suites by setting an inference number for suite components. For newly created software models that include suite components, the **Number** inference option is selected by default.

-   **[Limit the License usage view to managed software](https://www.servicenow.com/docs/access?context=sam-workspace-workbench&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Display software model results for only those software models that are associated with entitlements, limiting the License usage view to managed software.

-   **[Gain comprehensive insights into cluster configuration, licensing, and optimization](https://www.servicenow.com/docs/access?context=understand-sam-cluster&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Simplify cluster analysis by consolidating infrastructure, license usage, optimization, and cluster health data into a single, comprehensive view. This consolidation empowers Software Asset Management \(SAM\) managers to comprehend their cluster setup, examining details such as hosts, virtual machines, and software running on the cluster. Additionally, they gain insights into software license usage, optimization, and health issues. Equipped with this knowledge, SAM managers can make informed decisions that cover all aspects of their clusters.

-   **[Gain improved normalization coverage for similar discovery models through wide-net normalization](https://www.servicenow.com/docs/access?context=c_SAMDiscovery&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Achieve improved normalization of software products that have similar discovery models through wide-net normalization. With wide-net normalization, the Software Asset Management application uses a single normalization rule to normalize software products that share the same patterns for the discovered major version, discovered publisher, and discovered product. The Software Asset Management application can then immediately normalize your discovered software products without requiring the Content Service team to create additional normalization rules for similar discovery models. With this streamlined normalization process, you can reconcile and determine the license compliance of your software products more efficiently.

-   **[Manage content requests for software products directly through the Software Asset Management application](https://www.servicenow.com/docs/access?context=add-custom-software-products-workspace&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Submit, review, and disposition content requests for software products directly through the Software Asset Management application. If any publicly available software products don't exist in the Software Asset Management Content Library, you can add them to your ServiceNow instance as custom software products. By adding these custom software products to your instance, you can immediately use them in your downstream processes while automatically submitting corresponding content requests to the Content Service team. After these content requests are processed by the Content Service team, you can consolidate the custom software products with the software products that are added to the Software Asset Management Content Library.

-   **[Manage license compliance for Red Hat Enterprise Linux \(RHEL\) software across hybrid infrastructures](https://www.servicenow.com/docs/access?context=byol-concepts&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Use bring your own subscription \(BYOS\) support for Red Hat Enterprise Linux \(RHEL\) to determine the license compliance of your RHEL software across both on-premise and public cloud environments. Supported public cloud providers include AWS, Microsoft Azure, and Google Cloud Platform \(GCP\). Use your license compliance information to remediate any RHEL software installations that are non-compliant.

-   **[Optimize IBM licensing across public clouds by using the IBM License Compliance for Software Asset Management application](https://www.servicenow.com/docs/access?context=ibm-licensing-public-cloud-environments&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Use the IBM License Compliance for Software Asset Management application to track and measure IBM licenses across public clouds. Supported public cloud providers include AWS, Microsoft Azure, and Google Cloud Platform \(GCP\).

-   **[Optimize license costs for Microsoft Windows Server and Microsoft SQL Server deployments on your clusters](https://www.servicenow.com/docs/access?context=view-cost-based-licensing-optimizations-microsoft&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Use the Microsoft Core License Optimization reports to gain insight into the recommended cost-based licensing optimizations for your Microsoft clusters. Use this information to maximize cost savings across your Microsoft cluster deployments.

-   **[Manage licenses for indirect access to SAP applications using SAP Digital Access licensing model](https://www.servicenow.com/docs/access?context=sap-publisher-pack&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Track the usage of SAP applications through a third-party application or a non- SAP intermediary software by using the SAP Digital Access model. In this licensing model, the usage of SAP applications is licensed by the count of documents created by the third-party application. The documents include the following:

    -   Sales
    -   Invoices
    -   Purchase Orders
    -   Service &amp; Maintenance
    -   Manufacturing
    -   Quality Management
    -   Time Management
    -   Financial
    -   Material
-   **[Access software content data in National Security Cloud \(NSC\) Department of Defense \(DOD\) Impact Level 5 \(IL5\) deployments](https://www.servicenow.com/docs/access?context=c_SAMContentService&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

Access Software Asset Management Content Library data and receive regular software content updates for your NSC DOD IL5 deployments through the NSC DOD IL5 Content Data Service \(CDS\).

-   **[Gain increased visibility to Java landscape with enhanced ServiceNow Discovery application and reporting certified by Oracle Global License Advisory Services \(GLAS\)](https://www.servicenow.com/docs/access?context=download-oracle-glas-data&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Access Oracle verified GLAS data by downloading Oracle Java reports populated by the ServiceNow Discovery application. The Discovery application also supports the discovery and evidence download of the Oracle database and middleware.


</td></tr><tr><td>

Sourcing and Procurement Operations

</td><td>

-   **[Now Assist for Sourcing and Procurement Operations \(SPO\)](https://www.servicenow.com/docs/access?context=now-assist-spo&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

With Now Assist for Sourcing and Procurement Operations \(SPO\), fulfillers can easily summarize procurement-related records, providing real-time progress updates and action items. Available summarization skills include:

    -   Sourcing request summarization
    -   Purchase requisition summarization
    -   Procurement case summarization
If you're entitled to Source-to-Pay Operations Pro SKU and Sourcing and Procurement Operations Pro SKU, you can install this application.

-   **[Request the generative AI capabilities by using the Now Assist for SPO Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-spo-va-using&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

Requesters can leverage contextual generative AI using the Now Assist for SPO Virtual Agent to complete self-service tasks, such as purchasing products or tracking the status of purchase requisitions, sourcing requests, or procurement cases.

-   **[Log in to Shopping Hub for the first time](https://www.servicenow.com/docs/access?context=login-shoppinghub-first-time&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

Specify a default delivery address when logging in to Shopping Hub for the first time after initial setup to ensure supplier products display correctly.

-   **[Complete sourcing checkout](https://www.servicenow.com/docs/access?context=complete-sourcing-checkout&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

Add users to the watch list on sourcing requests and purchase requisitions:

    -   Provide visibility into state changes of purchase requisitions and sourcing requests to the users who aren't submitters or business owners.
    -   Configure the number of users allowed to be added to the watch list.
    -   Enable fulfillers to add users to the watch list at any stage of the request life cycle.
    -   Configure notifications to include watch list users regarding updates on the request.
-   **[Edit a purchase requisition line](https://www.servicenow.com/docs/access?context=edit-request&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

Fulfillers can use the enhanced **Edit a purchase** option to edit the service date, delivery date, delivery address, and quantity on purchase requisition lines and purchase order lines. For more information, see [Edit a purchase order line](https://www.servicenow.com/docs/access?context=edit-purchase-order&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US).

-   **[Purchasing from punchout or third-party suppliers](https://www.servicenow.com/docs/access?context=purch-punchout-third-party-supp&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

Shoppers can search for all the products, including those from external suppliers, directly within Shopping Hub. The configuration of the Search API, Order API, and Product Details API determines whether shoppers can complete their purchases directly in Shopping Hub or are redirected to external supplier websites. Products from third-party suppliers with configured Order API and Product details API can be viewed, added to cart, and purchased from within Shopping Hub. For suppliers without this configuration, a notification appears, redirecting shoppers to the supplier’s external site to add items to the cart and place the order. The shopper is subsequently redirected to Shopping Hub where they can continue with the checkout process. For more information, see [Configure punchout for third-party site purchases](https://www.servicenow.com/docs/access?context=configure-supplier-punchout&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US).

-   **[Configure punchout for third-party site purchases](https://www.servicenow.com/docs/access?context=configure-supplier-punchout&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

Set up cXML and API connections through a configuration framework to enable your shoppers to use AI search within Shopping Hub, enabling them to browse both third-party and native catalog items.

-   **[Process visibility](https://www.servicenow.com/docs/access?context=process-visibility&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

Render end-to-end process visibility in Shopping Hub so that your shoppers have transparency into the procurement process after they submit a request. You can also configure this feature to meet your own business processes. For example, you can use a default content and configuration framework to modify and edit your own content.

    -   Configure end-to-end process visibility through a configuration framework that enables administrators to define and modify steps, and the work that is within each step. You can also sequence and change labels to promote flexibility and alignment with your business processes.
    -   Provide your shoppers with the following end-to-end visibility on sourcing requests, purchase requisitions, and purchase orders in Shopping Hub:
        -   Progress of the requests and expected completion timelines.
        -   Step dependencies and progress of the sequential and concurrent steps.
        -   Completed, current, and future steps, enabling oversight of the status of the work within steps.
        -   Sequencing of work, such as approvals, cases, and tasks.
        -   Enhanced communication for your shoppers so that they can message task assignees and task assigners directly from within the platform. You can track this communication through audit trails.
        -   Record of your shoppers' page navigation between My Purchases List and Details view pages on Shopping Hub.

</td></tr><tr><td>

Strategic Planning

</td><td>

-   **[Show or hide features for your portfolio plan](https://www.servicenow.com/docs/access?context=show-or-hide-the-features-for-your-portfolio-plan-spw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

As a portfolio manager, show or hide the features, such as Goals, Scoring, Prioritization, and Roadmap, of your portfolio plan. This capability helps you share only the portfolio plan data that matters to your stakeholders and restrict access to the other data.

-   **[Goal management enhancements](https://www.servicenow.com/docs/access?context=managing-goals-in-alignment-planner-workspace&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Create daily, weekly, or monthly target breakdowns according to how often you want to update and track the progress of the target. The target breakdowns are created based on the value selected in the **Check-in frequency** field. For example, if you select **Monthly** in the **Check-in frequency** field for a target spanning a year, then 12 monthly target breakdowns are created.
    -   Updating actuals for a target has been simplified with an enhanced UI:
        -   In the Check-in actuals window on the **Progress** tab of the target’s side panel, update the actual value of any time period or breakdown.
        -   In the **Progress** tab of the target’s side panel, view the trend of the target’s progress in a line or bar graph. You can also edit the planned target and view the check-in history of the target actuals.
    -   When creating a target, the **Target breakdown details** section of the Target modal shows the planned target values for each target breakdown in a tabular format, which helps you visualize the final target value spread across the target’s time period.
    -   On the Target form, use the **Baseline reference** field to compare future target performance with the actual value that was achieved in the last year or before the target was created.
    -   Add targets to a new goal using the **Save and add target** option on the Goal modal. Also, you can use the **Save and add new target** option to add more targets for the goal.
    -   Run the **Create Goals Demo Data with Target Breakdowns** scheduled job to create demo data with goals and target breakdowns. For more information on this scheduled job, see [Create goals demo data with target breakdowns](https://www.servicenow.com/docs/access?context=create-goals-demo-data-with-target-breakdowns&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).
    -   Create a copy of a goal or target using the **Duplicate** option from the row context menu icon \(![Row context menu icon.](../image/row-context-menu-icon.png)\). For more information, see [Create a copy of a goal or target](https://www.servicenow.com/docs/access?context=create-a-copy-of-a-goal-or-target&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).
    -   Activity stream is enabled for the targets and goals in the full details record page.
-   **[Planning enhancements](https://www.servicenow.com/docs/access?context=planning-in-spw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Filter planning items in the Prioritization page and roadmap bars in the Roadmap page with multi-value fields, such as tags, business applications, and business capabilities.
    -   In the Child items related list of an EAP planning item, view child items associated with the epic in EAP.
    -   When you view a portfolio plan, you can copy a portfolio plan that you don't have edit access to and edit the plan as needed. For more information, see [Copy a portfolio plan](https://www.servicenow.com/docs/access?context=copy-portfolio-plan-in-strategic-planning&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).
-   **[Now Assist in Strategic Planning](https://www.servicenow.com/docs/access?context=now-assist-spm&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Generate a summary of selected text on Docs using the Planning item Gen AI Docs skill. You can summarize, elaborate, and shorten the selected content on Docs.
    -   Summarize a large volume of feedback using the multi feedback summarization skill on the Feedback page.
    -   Create a demand within the Employee Service Management \(ESC\) portal using the Now Assist conversational catalog creation capability.
    -   Summarize the complete content of a document with the Planning item Gen AI Docs skill to help save time on manual content analysis.
-   **[Collaborate using Docs in EAP](https://www.servicenow.com/docs/access?context=docs-for-eap-teams-and-planning-items&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Store the information of key artifacts and other details of planning items, such as Epics, Capabilities, and Features, directly from within the workspace.
    -   Manage team-level documentation for Agile team, ART, Solution Train, and Portfolio.
    -   Create multiple rich-text documents at each planning item level or Agile team level.
        -   Help avoid data loss and parallel editing with real-time collaboration.
        -   Tag team members to their action items.
        -   Insert media and URLs.
-   **[Docs for planning items in Strategic Planning](https://www.servicenow.com/docs/access?context=docs-for-planning-items-in-spw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Store the information of key artifacts and other details of planning items, such as Demands, Projects, and Epics, directly from within the workspace.
    -   Create multiple rich-text documents at each planning item level.
        -   Help avoid data loss and parallel editing with real-time collaboration.
        -   Tag team members to their action items.
        -   Insert media and URLs.
-   **[Migrating from SAFe to EAP](https://www.servicenow.com/docs/access?context=migrating-from-safe-to-eap&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Transition from Scaled Agile Framework \(SAFe\) applications, such as Essential SAFe and Portfolio SAFe, to EAP. Use the Guided Setup module in the Strategic Planning application to execute your migration step by step.

This migration is intended to be one-time only. Initiating the migration again later while continuing to use SAFe applications with EAP won't carry any changes made to the SAFe records that are already migrated.

-   **[Override the default planning calendar for Agile Teams](https://www.servicenow.com/docs/access?context=create-planning-calendar-type-in-eap&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

For Agile Teams and Agile release trains \(ARTs\), the **Override planning calendar** field enables team members to change their planning calendar. The updated calendar is automatically applied to any child teams and takes effect at the beginning of the next iteration.

-   **[Persistence of personalization settings for the EAP PI planning board](https://www.servicenow.com/docs/access?context=pi-planning-eap&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Personalization of the settings made in the PI planning board for a team type are applied across the workspace according to user, team type, and work item type. For example, settings applied to one ART, such as enabling the Dependencies toggle, Team backlog lane, or compact cards, are applied to all ARTs in the workspace for a user.

-   **[Optimize planning using scenario planning](https://www.servicenow.com/docs/access?context=scenario-planning-in-strategic-planning&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Create scenarios in a simulated environment and adjust the prioritization and timelines of planning items.
    -   Check the alignment of planning items with goals to verify the delivery of strategic outcomes.
    -   Visualize the differences between goal alignment and trade-off decisions between scenarios by comparing scenarios side by side.
    -   Approve the best scenario as the live portfolio plan for execution and making informed decisions.
-   **[Export goals and targets data to Excel or CSV](https://www.servicenow.com/docs/access?context=export-goals-and-targets-to-excel&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Export goals and targets from your portfolio plan into a Microsoft Excel or CSV file to share the data and collaborate with your business stakeholders.

-   **[Export a roadmap or free-form roadmap to PowerPoint](https://www.servicenow.com/docs/access?context=export-a-portfolio-plan-to-powerpoint-strategic-planning&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Export a roadmap or free-form roadmap from a portfolio plan into a Microsoft PowerPoint file to share data and collaborate with your business stakeholders. The predefined template helps you generate reports for your roadmap, including roadmap milestones, item milestones, vertical lines, and horizontal lanes.

You can export a roadmap for the maximum tenure of lanes a year at a time. You can also choose between Compact mode, which exports 25 horizontal lanes per slide, or Default mode, which exports 15 horizontal lanes per slide, when exporting your roadmap.

You can select the data that you want to be exported into the report by editing the predefined templates or creating your own branded template. For more information, see [Create a Microsoft PowerPoint template](https://www.servicenow.com/docs/access?context=create-ppt-template&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

-   **[Plan at a high level using the Project Program lens](https://www.servicenow.com/docs/access?context=portfolio-plans-in-strategic-planning&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Plan at a high level by building portfolio plans for program \[pm\_program\] items using the Project Program lens. Score and prioritize the programs and track them using roadmaps.

-   **[Feedback enhancements](https://www.servicenow.com/docs/access?context=managing-product-feedback-in-strategic-planning&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Manage the feedback filter card directly from the feedback homepage by sorting, pinning, sharing, updating, or deleting it.
    -   Allow access to specific users or groups when sharing the feedback filter card, and review the users who have access to it.
-   **[Financials in Strategic Planning](https://www.servicenow.com/docs/access?context=using-financials-spw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Migrate the existing planning items budget from the classic UI to Next Experience using the **Migrate Budget** option.
    -   As a portfolio manager, allocate and manage the budget of your planning items using the Budget vs cost view.
    -   As a project manager, compare a budget to the captured costs of your planning items and reforecast the planned costs to meet the approved budget.
    -   Compare financial baselines to view simple financials and budget.
    -   View the cost plans, expense lines, and financial baselines of sub-projects using the Financial view of a parent project.
    -   Widgets in the Cost view of parent projects display the rolled-up value of the planned costs, expense lines, budget, and variance.
    -   Create custom labor cost types and map them with a unique sys\_id to generate labor costs.

-   **[Capacity Planning in Strategic Planning](https://www.servicenow.com/docs/access?context=using-cap-plan-spw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Select a primary attribute to auto-select the resource criteria based on the planning items in the portfolio.
    -   Automatically generate resource capacity using a scheduled job at your desired cadence.
    -   View only prioritized planning items in the bottom tray of the Capacity Planning screen.
    -   View the total capacity, estimate, and available efforts of a resource using the heatmap view.

</td></tr><tr><td>

Stream Connect dashboard

</td><td>

-   **[Using the Stream Connect Dashboard](https://www.servicenow.com/docs/access?context=stream-connect-dashboard&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

View detailed statistics for your Stream Connect integrations, and create or edit topics, replicators, and consumers with the ServiceNow Stream Connect dashboard.


</td></tr><tr><td>

Subscription Management

</td><td>

-   **[Monitor Now Assist usage](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

View an account-level summary of your Now Assist entitlements and track Now Assist usage across all your instances.

-   **[Monitor Now Assist creators](https://www.servicenow.com/docs/access?context=monitoring-now-assist-creator&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

View an account-level summary of your Creator Plus entitlements and track allocations across all your instances.

-   **[Monitor cloud capacity](https://www.servicenow.com/docs/access?context=monitoring-cloud-entitlements&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Monitor cloud capacity and track storage capacity across all the instances associated with your account.

-   **[Subscription allocation counts according to active users](https://www.servicenow.com/docs/access?context=subscription-details-v2&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

View the total number of active users in a product subscription. Only active users count toward the subscription allocation totals that appear throughout Subscription Management.

-   **[Allocate subscriptions to all recommended groups](https://www.servicenow.com/docs/access?context=allocate-subscriptions-v2&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Select all recommended groups when allocating subscriptions.

-   **[Recommended subscription reasoning](https://www.servicenow.com/docs/access?context=addressing-issues-subscription-management-v2&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Determine why a subscription is recommended by Subscription Management when mapping custom tables or custom applications.


</td></tr><tr><td>

Supplier Lifecycle Operations

</td><td>

-   **[Now Assist for Supplier Lifecycle Operations \(SLO\)](https://www.servicenow.com/docs/access?context=now-assist-slo&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

With the Now Assist for Supplier Lifecycle Operations \(SLO\) application, supplier managers and fulfillers can summarize the details of supply-related records to keep them informed about their progress and action items.

-   **[Supplier Relationship and Performance Management](https://www.servicenow.com/docs/access?context=supplier-performance-management-overview&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**
    -   Manage supplier relationship and performance to optimize the value and quality of the products and services delivered by suppliers.
    -   Establish clear expectations and criteria for measuring supplier performance, monitor and assess their performance against those criteria, provide feedback and recognition, and implement corrective actions and improvement plans when needed.
-   **[Supplier Lifecycle Operations integration framework](https://www.servicenow.com/docs/access?context=slo-int-framework&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

Exchange supplier data with any third-party ERP system using enhanced transform maps and inbound and outbound integration tables.

-   **[View supplier details in the Source-to-Pay Workspace](https://www.servicenow.com/docs/access?context=supp-ws-details-page&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**
    -   View supplier details such as contracts and supplier products in the Related Links section on the **About** tab of the Source-to-Pay Workspace supplier page.
    -   View supplier details such as purchase orders and invoices on the **Related work** tab of the Source-to-Pay Workspace supplier page.
-   **[View supplier details in the Supplier Collaboration Portal](https://www.servicenow.com/docs/access?context=supplier-central&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

View supplier details in the following tiles in the My active items widget:

    -   Contracts
    -   Supplier Products
    -   Purchase Orders
    -   Invoices
**Note:** These new tiles are displayed if you have installed the Sourcing and Purchasing Automation \(com.snc.sn\_pr\) and Source-to-Pay Common Architecture \(com.snc.sn\_shop\) plugins.


</td></tr><tr><td>

Talent Development Core

</td><td>

Xanadu Patch 9

-   **Create a growth conversation with the help of an agent in Now Assist**

As a manager using Talent Development, start a growth conversation with your reportees with the help of Conversation management AI agent in Now Assist.


-   **Generate talking points for a growth conversation with the help of an agent in Now Assist**

As a manager using Career Conversations in Talent Development, generate talking points for a growth conversation with the help of Employee data summarization AI agent in Now Assist.

**Note:** For the Growth Conversations AI agents to work, you need to be on 3.5.2 version Career Conversations and have the Now Assist for HR Service Delivery \(HRSD\) plugin which will install Now Assist for Talent and HR Talent AI Agent Collection.


-   **[Name update from Employee Growth and Development Core to Talent Development Core.](https://www.servicenow.com/docs/access?context=egd-landing-page&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

The name changed to provide better alignment with your organization's talent, growth, and development initiatives.


</td></tr><tr><td>

Task Intelligence for ITSM

</td><td>

-   **[Set up a similarity model](https://www.servicenow.com/docs/access?context=using-task-intelligence-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Set up and configure a similarity model that learns the patterns of similarity between two types of tables by comparing their fields.

You can use the similarity template card to set up a new similarity model or select the Incident Similarity model available in the base system.

-   **[Metrics of similarity model](https://www.servicenow.com/docs/access?context=admin-console-ti&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

View the number of predictions made by a selected similarity model and the number of incidents records that provided predictions.

-   **[Edit and redeploy the model](https://www.servicenow.com/docs/access?context=edit-your-model&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

You can edit, retrain, and redeploy a similarity model to enhance the performance based on the model performance and impact.


</td></tr><tr><td>

Telecommunications Network Inventory

</td><td>

-   **[Visualization of a rack or cabinet](https://www.servicenow.com/docs/access?context=visualization-of-rack&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US)**

Gain visibility of your data centers infrastructure through advanced rack and cabinet insights. Edit a rack or cabinet to add, reserve, move, and remove any equipment. This enables you to create equipment from the rack or cabinet view.

-   **[Revise a configuration item](https://www.servicenow.com/docs/access?context=revise-a-configuration-item&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US)**

Perform a comparative validation between the revision and the original connections to identify any changes between them.

-   **[Import Models and Templates](https://www.servicenow.com/docs/access?context=import-models-and-templates&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US)**

Import the models and templates from an external system via XLS template.

-   **[Visualization of circuits](https://www.servicenow.com/docs/access?context=unified-map-view-of-connection-elements&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US)**

Provide a visualization of the circuit and its underlying connection elements on a dedicated window. View the revisions and protection paths of a logical connection, and selectively collapse expanded layers instead of collapsing the entire structure.

-   **[Create a cable record by using design and assign](https://www.servicenow.com/docs/access?context=create-cable-record-using-design-assign&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US)**

Instantiate cables and associated strands using a cable template.

-   **[Modify a network topology record using design and assign](https://www.servicenow.com/docs/access?context=modify-network-topology-record-design-assign&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US)**

Modify a network topology for adding or removing the nodes and edges by using a new change model.

-   **[Create capacity function](https://www.servicenow.com/docs/access?context=create-capacity-function&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US)**

Identify and prioritize the capacity function by using the category and order attributes. Access the capacity management forms from the Workspace lists view.

-   **[Network Inventory Workspace](https://www.servicenow.com/docs/access?context=exploring-network-inventory-workspace&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US)**

View your and your team's work in the new landing page.


</td></tr><tr><td>

Theme Builder

</td><td>

-   **[Publish multiple themes with Theme Builder](https://www.servicenow.com/docs/access?context=tb-apply-theme&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

Publish multiple themes with their alternate color palettes to your web instance. Set a default theme for your users.

-   **[Add a dark alternate color palette](https://www.servicenow.com/docs/access?context=tb-edit-color-palette&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

Add a dark alternate color palette to your Theme Builder theme. You can edit this alternate color palette to further enhance your brand style.

-   **[Set the presentation order of your themes in Next Experience](https://www.servicenow.com/docs/access?context=configure-presentation-order-of-themes&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

Define the presentation order of the themes that are displayed in the ServiceNow® Next Experience user preferences.

-   **[Select from multiple themes in Next Experience user preferences](https://www.servicenow.com/docs/access?context=select-a-theme-in-next-experience&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

View multiple themes and their alternate color palettes in Next Experience user preferences.

-   **[Set the presentation order of your Theme Builder themes](https://www.servicenow.com/docs/access?context=set-presentation-order-themes&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

As of Theme Builder version 4.1, you can control the order in which the themes created with Theme Builder appear in Next Experience user preferences by using the List view within the Manager page.

-   **[Remove Global Style overrides](https://www.servicenow.com/docs/access?context=tb-edit-theme&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

As of Theme Builder version 4.1, you can remove any overrides that you made to Global Styles and return to your initial values by using the Remove Override button.

-   **[Use drag-and-drop to publish and unpublish your themes](https://www.servicenow.com/docs/access?context=tb-apply-theme&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

As of Theme Builder version 4.1, use the drag-and-drop feature in the List view to publish and unpublish your themes for your web instance.

-   **[Adjust a component to meet accessibility standards](https://www.servicenow.com/docs/access?context=tb-adjust-component-wcag&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

As of Theme Builder version 4.1, the Accessibility Inspector now displays the total number of accessibility errors in your theme and lists the specific components with contrast issues. See the Accessibility section for details.


</td></tr><tr><td>

Third-party Risk Management

</td><td>

-   **[Third-party element collection](https://www.servicenow.com/docs/access?context=tprm-monitor-tp-elements&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Confirm that third-party elements adhere to the same security and compliance standards as an engagement by monitoring them through TPRM. Use this data to help identify, assess, and manage the risks that are related to your engagements that depend on third-party elements.

-   **[Risk intelligence report requests](https://www.servicenow.com/docs/access?context=tprm-riskintel-using&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Make informed decisions about working with an engagement or third party by requesting and managing risk intelligence reports or scores from external risk intelligence content providers using the Third-party Risk Management application.

-   **[Third-party risk management data model](https://www.servicenow.com/docs/access?context=tprm-data-model&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Take full advantage of Third-party Risk Management by viewing its data model to see how you can best use it to assess, monitor, and mitigate the risks that are required for your risk management program.

-   **[Digital resilience third-party registers](https://www.servicenow.com/docs/access?context=tprm-dora&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Create, update, and track records for digital resilience third-party registers by using the Digital resilience third-party registers application within the Vendor Management Workspace Vendor Management Workspace. You can bulk create or edit individual records for assessments, branches, contracts, functions, legal entities, supply chains, third parties, or third-party engagements using the Excel download/upload requests feature. This application helps you maintain records with information and communication technology \(ICT\) third-party service providers, helping ensure compliance with the Digital Operational Resilience Act \(DORA\).


</td></tr><tr><td>

Threat Intelligence Security Center

</td><td>

-   ****

All observables, indicators, and entities now supports MITRE technique associations.


-   **[Roll up of MITRE technique associations](https://www.servicenow.com/docs/access?context=tisc-mitre-roll-up&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

MITRE techniques can now be rolled up from artifacts at a case level both manually and automatically.


-   **[Palo Alto Networks integration](https://www.servicenow.com/docs/access?context=palo-alto-networks-integration&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Integration with Palo Alto is now available to manage External Dynamic Lists \(EDLs\) directly from TISC.


-   **[CrowdStrike Falcon EDR integration](https://www.servicenow.com/docs/access?context=crowdstrike-edr-integration&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Integration with CrowdStrike Falcon EDR is now available for continuous monitoring and real-time alerting based on TISC intelligence.


-   **[Working with Investigation Canvases](https://www.servicenow.com/docs/access?context=tisc-investigation-canvases&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Introduced a new Investigation Canvas for deeper and interactive case analysis.


-   **[View details in Relationship Graph](https://www.servicenow.com/docs/access?context=objects-visualizer&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Enhanced the user experience on relationship visualizations.


-   **[Bulk import Taxonomies](https://www.servicenow.com/docs/access?context=tisc-import-taxonomy&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Supports bulk taxonomy values upload.


-   **[TISC API References](https://www.servicenow.com/docs/access?context=tisc-api-references&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Creating observables in TISC is now available through the implementation of TISC API 2.0.

-   **[Defining Expiration Rules](https://www.servicenow.com/docs/access?context=tisc-expiration-rules&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Define expiration policies at a more granular level by creating expiration rules for data source and record type combinations.

-   **[Working with Webhooks](https://www.servicenow.com/docs/access?context=tisc-webhooks&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Initiate trigger-based notifications by using Webhooks.

-   **[Working with automated flows](https://www.servicenow.com/docs/access?context=tisc-automated-flows&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Automate analyst actions through sample automation flows.

-   **[Add observables to TISC Case](https://www.servicenow.com/docs/access?context=observables-to-case&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Add security incident and observables directly to a TISC case in the Security Incident Response Workspace.

-   **[MITRE ATT&amp;CK Technique Extraction Rules](https://www.servicenow.com/docs/access?context=mitre-extraction-rules&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Capture automatically extracted MITRE techniques to the intelligence records such as observables, indicators, and all STIX entities.


</td></tr><tr><td>

UI Builder

</td><td>

-   **[Set screen conditions declaratively](https://www.servicenow.com/docs/access?context=control-conditions-for-your-variant&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Control the visibility of pages using a condition builder as an alternative to writing a script.

-   **[Configure contextual sidebar with tabs](https://www.servicenow.com/docs/access?context=add-contextual-sidebar&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

The Contextual sidebar component now uses the Tabs component as a foundation instead of viewports for simplified configuration as a vertical set of tabs.

-   **[Control page layout for different device sizes](https://www.servicenow.com/docs/access?context=responsive-authoring&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Create tailored pages that are appropriate for different size screens.

-   **[Retrieve data from varied sources for a component](https://www.servicenow.com/docs/access?context=multi-source-data-configuration&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

More easily add data from different data sources to a single component based on field mappings.

-   **[Support for multiple forms on a page](https://www.servicenow.com/docs/access?context=add-forms-to-ui-builder-pages&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Add multiple forms and form controllers to a single page.


</td></tr><tr><td>

UI Component CLI Extension

</td><td>

-   **Module caching**

Module caching improves developer server performance by storing a module in memory when imported and returning the module from the cache for future uses.


</td></tr><tr><td>

Upgrade Center

</td><td>

-   **[UI messages to manage upgrade risk](https://www.servicenow.com/docs/access?context=uc-manage-upgrade-risk&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

New UI messages were added to manage metadata records based on the severity of the files.

-   **[Default skipped rules](https://www.servicenow.com/docs/access?context=uc-default-skipped-rules&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Reduce upgrade processing time with the new default skipped rules to auto-retain high-friction causing configuration metadata types.


</td></tr><tr><td>

Vendor Management Workspace

</td><td>

-   **[Updated Vendor KPIs](https://www.servicenow.com/docs/access?context=vendor-manager-workspace-default-wep&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Use the new vendor KPIs that replace the legacy KPIs in the deprecated Service Offering Metric Data \[service\_offering\_metric\_data\] table.


</td></tr><tr><td>

Verifi Spoke

</td><td>

-   **[Verifi spoke actions](https://www.servicenow.com/docs/access?context=verifi-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

Use the Verifi Spoke actions to access various API functions, including creating cases, revoking or closing cases, retrieving case details, and obtaining merchant inquiries.


</td></tr><tr><td>

Virtual Agent

</td><td>

-   **[AI agents in Virtual Agent Designer](https://www.servicenow.com/docs/access?context=managing-use-cases-ai-agents&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

View AI agents created in AI Agent Studio in Virtual Agent Designer.


-   **Quick start tests for [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Virtual Agent works as expected. If you customized Virtual Agent, copy the quick start tests and configure them for your customizations.

-   **Rich text for Static and Dynamic Choice controls: [Static Choice user input control](https://www.servicenow.com/docs/access?context=va-static-choicelist&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US) and [Dynamic Choice user input control](https://www.servicenow.com/docs/access?context=va-reference-choicelist&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Use rich text options when creating Static and Dynamic Choice nodes in ServiceNow® Virtual Agent Designer.

-   **Virtual Agent Web Client branding: [Set up your Virtual Agent bot's branding](https://www.servicenow.com/docs/access?context=ac-configure-chat-branding&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Customize colors in the New Messages Above and New Messages Below banners in the chat window.

-   **LLM topic type association: [Create a Virtual Agent topic](https://www.servicenow.com/docs/access?context=create-virtual-agent-topic&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Associate LLM Assistants to Setup topics, Topic blocks, and Custom controls.

-   **[LLM topic testing](https://www.servicenow.com/docs/access?context=test-llm-topics&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Define an assistant on the Virtual Agent \(VA\) testing panel, when selecting Test All Active Topics with selecting an assistant.

-   **[LLM Text bot response control](https://www.servicenow.com/docs/access?context=va-ai-response&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Use the LLM Text bot response control to generate messages in conversations using LLM topic discovery.

-   **[Conversational Analytics dashboard in Platform Analytics experience](https://www.servicenow.com/docs/access?context=VA-dashboard-landing-page-pae&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

The Conversational Analytics dashboard in the ServiceNow® Platform Analytics experience meets the compliance requirements of data regulated market environments, for example, Government Community Cloud \(GCC\). The dashboard contains indicators and breakdowns for rich visualizations and detailed analysis. You can access the dashboard by navigating to **All** &gt; **Conversational Interfaces** &gt; **Analytics**.

-   **[New system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Determine whether actions for Virtual Agent notifications and Proactive Triggers are created after completing the full topic migration workflow via the **com.glide.cs.notification.create\_llm\_actions\_after\_topic\_migration** and **com.glide.cs.proactive\_trigger.create\_llm\_actions\_after\_topic\_migration** system properties.

-   **[NLU to LLM topic migration enhancements](https://www.servicenow.com/docs/access?context=llm-topic-migration&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**
    -   Migrate Virtual Agent notifications and Proactive Triggers actions on the Review connections step after publishing the newly migrated LLM topics in the NLU to LLM topic migration workflow.
    -   Review, edit, and test LLM topic descriptions against existing NLU utterances, if available, in the Review descriptions step. The Review descriptions step occurs after migration but before publication in the NLU to LLM topic migration workflow.
    -   Migrate NLU vocabulary sources automatically into either Dynamic Choice or Static Choice nodes, depending on the vocabulary sources setup in NLU.
-   **[Max wait time queue allows LLM topic selection](https://www.servicenow.com/docs/access?context=awa-create-queue-triggers&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Select LLM topics to be chosen after the max wait time is met during a Now Assist in Virtual Agent conversation. ServiceNow® Advanced Work Assignment queue triggers support LLM topics whenever the **Trigger Type** field's value is **Max Wait** and you’re prompted to select a Virtual Agent topic.

-   **[Catalogs for Virtual Agent](https://www.servicenow.com/docs/access?context=va-catalogs&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Search for and order services or products from catalog macroponents in Virtual Agent chat by using plain language. Customize the appearance of your catalogs to match your business’ branding.

-   **[Integrating Now Assist in Virtual Agent with Microsoft Copilot](https://www.servicenow.com/docs/access?context=ms-copilot-na-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Use your Self-configured bot to connect with Microsoft Copilot. The process of integrating the Self-configured bot with Microsoft Copilot is similar to that of integrating the Self-configured bot with Microsoft Teams.

You can @-mention the bot name to initiate a chat within Copilot and Copilot provides you the response based on your utterance.

Microsoft Copilot, when integrated with Now Assist in Virtual Agent, understands the ServiceNow context and routes users to Now Assist to conduct ServiceNow -related questions and tasks within Microsoft Teams.

Use your Now Virtual Agent bot to connect with Microsoft Copilot by @-mentioning the bot name.

Support for using declarative agents with Self-configured bots and transferring to live agents is available.

Support for the default Now Virtual Agent bot plugin is available on the Microsoft Teams Store.

-   **[Integrating Virtual Agent with enterprise messaging apps](https://www.servicenow.com/docs/access?context=integ-va-enterprise-apps&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

Now LLM Service support for channels enables LLM-based conversations with Now Assist in Conversational Integration with Microsoft Teams and Conversational Integration with Slack.

The Now LLM Service support also provides new ServiceNow AI Search experience in channels with the following features:

    -   Legal disclaimers
    -   Pagination
    -   Search
    -   Generative AI Q&amp;A card
-   **[Configure rate limiting for providers](https://www.servicenow.com/docs/access?context=configure-rate-limit&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Configure rate limiting at the provider level to control the request flow for requests made within a stipulated time.


-   **[Primary and secondary assistants are honored in Virtual Agent Designer](https://www.servicenow.com/docs/access?context=llm-assistants&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

View which conversational assets are applicable to primary or secondary assistants.

-   **Language detection for LLM conversations**

For Now Assist in Virtual Agent users, use language detection for your LLM conversations to improve your user's experience.

-   **[Synthesized response](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

For Now Assist in Virtual Agent users, a synthesized response can appear. A synthesized response includes a brief summary of the requested information and search results along with Genius Results. Mid-topic switching can occur during a conversation with synthesized response. Users can continue with their original request or switch the conversation's focus.

-   **[New system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

The following system property was added to increase flexibility of the search results and response:

    -   **sn\_nowassist\_va.synthesized\_autostart\_items**: When synthesized response only returns a singular action, configure whether to directly launch into that action. By default, whenever synthesized response returns a single Virtual Agent topic, that action is auto-launched. The following actions can be configured to auto-launch:
        -   Synthesized response returns a single conversational catalog item.
        -   Synthesized response returns a single Virtual Agent topic, along with Knowledge Base information.
        -   Synthesized response returns a single conversational catalog item, along with Knowledge Base information.

</td></tr><tr><td>

Vulnerability Response

</td><td>

-   **[Identify Wiz Resource Types for import](https://www.servicenow.com/docs/access?context=wiz-assets-resources-tab&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Identify the Resource Types \(assets\) that are reported by Wiz that you want to import with the Wiz Integration Resource Type configuration page in your ServiceNow AI Platform instance.

The Resource Types that you select apply to all the primary Wiz vulnerability and compliance integrations except the Wiz Container Vulnerability Integration. See the [Wiz Vulnerability Response Integrations](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) for more information about the vulnerability and compliance integrations.

-   **[Wiz Backfill Integrations](https://www.servicenow.com/docs/access?context=wiz-backfill&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Retrieve and process data stored on the Wiz Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table for assets that were not processed by the primary Host Vulnerability Integration with a specialized Wiz Backfill Integration.

The Host Vulnerability Backfill Integration is activated by default.

**Note:** The Wiz Asset Integration and the Wiz Container Vulnerability Integration do not have backfill integrations. The Wiz Asset Integration can discover assets and create and update discovered item records on the Discovered item \[sn\_sec\_cmn\_src\_ci\] table. The Wiz Container Vulnerability Integration imports and processes discovered container image records.

-   **[Create solutions from scanners](https://www.servicenow.com/docs/access?context=vuln-solution-mgmt&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, solution records can now be configured to be created from scanners such as Tenable, Qualys, and Microsoft Threat and Vulnerability Management \(MS TVM\). These solutions are set as preferred in the absence of options from software vendors.

-   **[Activate or deactivate CVEs for exposure assessment](https://www.servicenow.com/docs/access?context=vr-ws-activate-deactivate-cves&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with version 4.0.1 of Vulnerability Exposure Assessment, if a Common Vulnerability Entry \(CVE\) has not been updated or had vulnerable items \(VITs\) created in the past 30 days, the exposure assessment record for that CVE is automatically marked as inactive. However, you can manually activate or deactivate these records. Additionally, the scheduled job **Check potential vulnerability**exposure regularly scans for such CVEs to designate them as inactive. If there is an update, it marks them as active.

-   **[Split detections from Tenable and Microsoft TVM scanners](https://www.servicenow.com/docs/access?context=vuln_integrations&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, you can split the detections from Tenable and Microsoft Threat and Vulnerability Management \(MS TVM\) scanners, enabling the creation of a unique vulnerable item \(VIT\) for each detected vulnerability instance. This split enables the assignment of VITs to various remediation teams, enhancing the management and tracking of vulnerabilities. 

-   **[New Properties module](https://www.servicenow.com/docs/access?context=installed-with-vr&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, a new **Properties** module has been added to the navigation menu under the **Administration** section. This module enables direct modification of the values, offering a user-friendly method to manage and update system properties directly from the interface.

-   **[Deletion of classification rules and application on discovered items](https://www.servicenow.com/docs/access?context=delete-vulnerability-classification-rule&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, if a classification rule is deleted or deactivated, it’s no longer applied to the discovered item and the data in the **Classification** and **Classification\_type** fields get cleared.

-   **[Exceptions for CI creation](https://www.servicenow.com/docs/access?context=ci-creation-using-IRE&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, if Identification and Reconciliation engine \(IRE\) encounters exceptions that prevent the creation of configuration items \(CIs\), the specifics of these exceptions are recorded in the Additional Information field.

-   **[View configuration item history](https://www.servicenow.com/docs/access?context=reapply-discovered-items-ci-changes&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, you can view the updates to a CI in the Discovered Item table. Information including the previous CI, the updated CI, and the user who made the changes is documented in the Audit History related list.

-   **[Customize the calculation of Age and Age closed values of a vulnerable item](https://www.servicenow.com/docs/access?context=vulnerable-item-fields&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, the Age and Age Closed durations of a Vulnerable Item can be configured to be calculated from the date in the Created, Opened, or First Found fields.

-   **Open the search results in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-change-app-scope-search&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) or [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-change-app-scope-search&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) rather than the Classic UI**

Starting with v24.0.6 of Vulnerability Response, automatically open your search results in the Vulnerability Manager Workspace or IT Remediation Workspace rather than the Classic UI, by adjusting the application scope in the unified navigation bar to Vulnerability Manager Workspace or IT Remediation Workspace respectively. These application scopes are available to you based on your assigned role.

-   **[Vulnerability Manager Workspace access to the sn\_vul.read\_all role](https://www.servicenow.com/docs/access?context=installed-with-vr&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, as a user with the sn\_vul.read\_all role, you can view the host vulnerable items in the Vulnerability Manager Workspace.

-   **[IT Remediation Workspace access to the sn\_vul.read\_assigned role](https://www.servicenow.com/docs/access?context=installed-with-vr&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, as a user with the sn\_vul.read\_assigned role, you can view the host vulnerable items assigned to you and your assignment groups in the IT Remediation Workspace and remediate them.

-   **Navigate to the List page in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) or [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) by selecting the links from the All menu**

Starting with v24.0.6 of Vulnerability Response, when you enable the 'sn\_vul\_cmn\_ws.navigate\_to\_workspace' system property, selecting predefined filter links in the Vulnerability Response module from the 'All' menu will automatically open these links in the List page in the Vulnerability Manager Workspace or IT Remediation Workspace based on your role.

-   **Hide the record count on the Host Vulnerable Items list in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) and [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, you can hide the record count on the lists in the List page of the Vulnerability Manager Workspace and IT Remediation Workspace by adding the table names to the **glide.ui.list.seismic.omit.count** system property.

-   **[Enable automatic refresh for the Home page dashboard in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-home-page-create-filter&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, when creating and editing filters in the Host Vulnerabilities tab on the Home page of the Vulnerability Manager Workspace, you can configure the widgets to refresh automatically. Otherwise, you can manually refresh the widgets by selecting the **Refresh** button on the Host Vulnerabilities tab.

-   **[Re-evaluating remediation properties for all records in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-reevaluate-remediation-parameters&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, you can evaluate the remediation properties for all the Vulnerable Items from the Host Vulnerable Items list by selecting the **All items** option in the **Record selection** field of the Re-evaluate remediation properties modal in the Vulnerability Manager Workspace.

-   **[Reevaluate the remediation properties for vulnerable items in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-reevaluate-remediation-parameters&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Select the vulnerable items conditionally for reevaluating the following remediation properties in the Vulnerability Manager Workspace:

    -   Assignments
    -   Remediation tasks
    -   Remediation target date
    -   Exceptions \(Vulnerability Response v24.0.6\)
    -   Risk score
-   **[Navigate to the Exposure Assessment page in workspaces from the All menu](https://www.servicenow.com/docs/access?context=vr_sw_expsure_task&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

With the Vulnerability Response Pro or Enterprise subscription, you’re redirected to the Exposure Assessment page in the Vulnerability Manager Workspace or Vulnerability Assessment Workspace based on your role, on selecting the Exposure Assessment link in the All menu.

-   **[Common Security Advisory Framework \(CSAF\) scanner mapping is optional](https://www.servicenow.com/docs/access?context=import-csaf-file&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

The Scanner mapping field is now optional for the following Common Security Advisory Framework \(CSAF\) import methods:

    -   File import
    -   Advisories
    -   CSAF URL
-   **[Multiple vendors supported for CSAF through Rolie feed](https://www.servicenow.com/docs/access?context=import-csaf-url&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Import vulnerability solutions from CSAF aggregators or trusted providers via URL import supporting Resource-Oriented Lightweight Information Exchange \(ROLIE\) feed. These vulnerability solutions are automatically mapped to the correct vendor and vulnerable items \(VITs\) based on the Common Vulnerabilities and Exposures \(CVEs\).

-   **[Enhanced processing performance of scheduled job](https://www.servicenow.com/docs/access?context=installed-with-vr&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

The **Rollup vulnerable item values to vulnerability and group** scheduled job is enhanced to create background jobs with multithreading capabilities. This upgrade involves segmenting the job into several smaller child jobs, which are executed either in parallel or concurrently. This modification enables processing of multiple records simultaneously, thus significantly speeding up the overall task.

-   **[Workflow deprecation and replacement by flow designer](https://www.servicenow.com/docs/access?context=cj-common-vuln-tasks&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

The following workflows have been deprecated and replaced by the flow designer:

    -   Exception Rule State Approval
    -   Remediation Task State Approval
    -   Vulnerability Response - Scan Vulnerability
    -   Vulnerable Item State Approval
    -   Vulnerability Response - Scan Vulnerable Item
.

-   **[Risk score updates in the Notes section](https://www.servicenow.com/docs/access?context=vuln-calculators-rules&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Access information on how an item's risk score is adjusted according to modifications in the vulnerability calculators. These details are available in the Notes section and include:

    -   Calculator group name
    -   Calculator name
    -   Field values along with their weightage and impact on the risk score
    -   Final risk score
-   **[Vulnerability Crisis Management \(VCM\) is available as a separate subscription in the store](https://www.servicenow.com/docs/access?context=vulnerability-crisis-management&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v1.0.1 of Vulnerability Crisis Management, the application is available as a separate subscription in the store. You can access Vulnerability Crisis Management from the Vulnerability Assessment workspace only if you have fine- grained entitlement or have installed the application from the store. Previously, Vulnerability Crisis Management was included with the Vulnerability Emergency Response plugin.

-   **[Vulnerability Exposure Response is renamed as Vulnerability Exposure Assessment](https://www.servicenow.com/docs/access?context=vr-ws-exposure-assessment&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v3.2.2, the Vulnerability Emergency Response plugin has been renamed as Vulnerability Exposure Assessment.


</td></tr><tr><td>

Vulnerability Response Integration with Claroty CTD

</td><td>

-   **[Enhanced filters for the Vulnerability Response Integration with Claroty CTD to support Claroty CTD v5.1](https://www.servicenow.com/docs/access?context=connect-to-claroty-ctd-vr-integration&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Identify and import vulnerabilities according to your requirements by using the additional filter properties that have been added in Claroty CTD. The filter properties are based on a Common Vulnerability Scoring System \(CVSS\) V3 score and Exploit Prediction Scoring System \(EPSS\) score that is available in Claroty CTD v5.1.


</td></tr><tr><td>

Vulnerability Response Integration with Microsoft Defender for IoT \(Azure\)

</td><td>

-   **[Vulnerability Response Integration with Microsoft Defender for IoT \(Azure\)](https://www.servicenow.com/docs/access?context=vulnerability-response-integration-with-microsoft-defender-for-iot-azure&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

Use the Vulnerability Response Integration with Microsoft Defender for IoT \(Azure\) application with the Operational Technology Vulnerability Response application to track, prioritize, and resolve vulnerabilities on OT devices used in the production process.


</td></tr><tr><td>

Vulnerability Response integrations

</td><td>

-   **[Scan vulnerabilities on running hosts](https://www.servicenow.com/docs/access?context=vr-pcc-integration&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Starting with v3.0.3 of Vulnerability Response Integration with Palo Alto Networks Prisma Cloud Compute, you can scan vulnerabilities on running hosts. The Prisma Host APIs enable retrieval of comprehensive vulnerability information for a specific host and enable assignment and remediation workflows

-   **[Populating the CPE information for a Tenable TPE](https://www.servicenow.com/docs/access?context=tenableIntegration&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

The newly added Softwares column in the Third-Party Vulnerability Entries table populates the Common Platform Enumerations \(CPEs\) information for the Tenable plugins.


</td></tr><tr><td>

Workflow Studio

</td><td>

-   **[Create workflow items from a button on the tab header](https://www.servicenow.com/docs/access?context=exploring-workflow-studio&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Create workflow items from any Workflow Studio page by using the **Create** button on the tab header.

-   **[Create a category to organize your actions](https://www.servicenow.com/docs/access?context=create-action&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Create your own categories to organize actions.

-   **[Create a category to organize your data stream actions](https://www.servicenow.com/docs/access?context=create-data-stream-action&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

Create your own categories to organize data stream actions.

-   **[Create a category to organize your subflows](https://www.servicenow.com/docs/access?context=create-subflow&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Create your own categories to organize subflows.

-   **[See when a new version of Workflow Studio is available](https://www.servicenow.com/docs/access?context=update-to-the-latest-version-of-workflow-studio&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

See an information banner when a new version of Workflow Studio is available.


</td></tr><tr><td>

Workforce Optimization for Customer Service CSM

</td><td>

-   **[Performance metrics for voice channel](https://www.servicenow.com/docs/access?context=components-installed-configurable-wfo-cs&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Monitor and manage the health of voice queues on Channel Management by viewing more metrics and reports from Amazon Connect.

-   **[Recurring meetings in scheduling](https://www.servicenow.com/docs/access?context=scheduling-configurable-wfo-cs&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Schedule and track recurring meetings such as training sessions or one-on-one sessions with teammates.

-   **[Scheduling enhancements](https://www.servicenow.com/docs/access?context=scheduling-configurable-wfo-cs&version=xanadu&pubname=xanadu-customer-service-management&section=swap-agent-shifts-configurable-wfo-cs&ft:locale=en-US)**

Efficiently manage and monitor time off and shift swap requests.


</td></tr><tr><td>

Workforce Optimization for ITSM

</td><td>

-   **[Admin Console Experience](https://www.servicenow.com/docs/access?context=admin-console-wfo-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Use the admin console to set up and configure the Workforce Optimization for ITSM application.

-   **[Synchronize the schedule calendar with Microsoft Outlook](https://www.servicenow.com/docs/access?context=synchronize-microsoft-outlook-wfo-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

When you synchronize the agent's calendar in the Schedule module with Microsoft Outlook, agents can view all your schedule, shifts, and events that display in the agent calendar also in your Microsoft Outlook calendar.

-   **[Recurring events in the team calendar](https://www.servicenow.com/docs/access?context=add-events-team-calendar-wfo-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

When you create an event, you can make it a recurring event.


</td></tr><tr><td>

Workspace

</td><td>

-   **International characters supported in email addresses**

Enter international characters for email addresses without running into errors.

Enable international characters for your users according to RFC6530 standards or disable them by changing a system property and performing additional configurations.

-   **[Email client plugin system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Ensure your agents leverage the latest functionality in the email client by using updated plugin \(**glide.ui.email.composer.enabled\_plugins**\) and toolbar \(**glide.ui.email.composer.toolbar**\) system properties offered by default for Tiny MCE v6.

-   **[Tags for Activity Stream records](https://www.servicenow.com/docs/access?context=tags-activity-stream-agent&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

Use tags to categorize and filter records shown in the Activity Stream.

As admins, you can enable, add, customize, and edit tags for your users' Activity Stream records.

-   **Reference searches with queries**

Help users access relevant reference search results by applying pre-filtered and removable query parameters to reference lists. These query parameters act as an addition to fixed queries that cannot be removed by end users.

-   **Client scripts for field decorators**

Add field decorators to field types using client scripts.

-   **Pre-filter records on the multi-record associator**

Pre-filter records with typeahead on the multi-record associator using scripts.

-   **[Use a keyboard shortcut to insert response templates](https://www.servicenow.com/docs/access?context=add-response-templates-shortcut&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

Enter the keyboard shortcut `/r` and a keyword to insert a response template directly into an email body.

-   **[Configure response templates for email composer](https://www.servicenow.com/docs/access?context=configure-response-templates&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

You can enable or disable response templates for agents with a system property.


</td></tr><tr><td>

Zero Copy Connector for ERP

</td><td>

-   **OData integration**

Extract data securely from ERP OData APIs using ETL to be used in remote tables and extraction tables.

-   **Schedule extraction**

Schedule data extractions into extraction tables with encoded query for delta updates.

-   **Monitor transactions**

Use the new monitoring feature to track each transaction and its progress; filter the ERP Data Hub task information, such as successes, failures, and more, as needed.

-   **Enhanced heartbeat data**

Use the enhanced heartbeat feature that now shows RFC, HTTP, and other connectivity status for better visibility to the end user.


</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Xanadu features](../release-notes-summaries.md)

