---
title: New features and products in Yokohama
description: Cumulative release notes summary on new Yokohama features and products.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2026-04-08"
reading_time_minutes: 314
breadcrumb: [Release notes summaries for Yokohama features, Release notes for upgrading from Xanadu, Learn about the Yokohama release, Yokohama release notes]
---

# New features and products in Yokohama

Cumulative release notes summary on new Yokohama features and products.

New products were introduced in Yokohama, and additional features were added to existing  products.

<table id="rn-summary-new-features-tables" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Control Tower

</td><td>

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   **[Health tab in AI Control Tower](https://www.servicenow.com/docs/access?context=aict-health-tab&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Monitor and evaluate the effectiveness of offensive content and prompt injection guardrails active on your AI assets.

-   **[Evaluation tab in AI Control Tower](https://www.servicenow.com/docs/access?context=ai-evaluation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Measure and improve the quality of interactions with virtual agents using the Evaluation tab.


-   **[Explore AI model providers](https://www.servicenow.com/docs/access?context=ai-model-providers&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Enable choice for third party model providers powering ServiceNow® skills and agents.


-   **[AI Control Tower](https://www.servicenow.com/docs/access?context=ai-control-tower-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**
    -   A single pane view of the AI inventory, its state, and its risk and compliance posture.
    -   Lifecycle to manage AI asset onboarding and deployment.
    -   Helps user oversee and manage AI Asset inventory's risk profile with regard to enterprise policies and global regulations, as defined by the user, with a focus on privacy, data governance, and ethical AI.
    -   AI Case management to oversee AI asset-related inquiries and cases, enabling faster response and improved tracking.
    -   Multi-instance management to synchronize AI asset inventory from sub-prod to prod instances to initiate governance early in the build process.
    -   Control settings to block only ''other'' skills in Now Assist AI deployment pending approvals.

-   **[AI Control Tower](https://www.servicenow.com/docs/access?context=ai-control-tower-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**
    -   AI Steward role- Facilitate and coordinate governance activities between innovation, legal, security, risk and compliance teams.
    -   AI Asset inventory- Unified data model on the ServiceNow AI Platform to catalog AI Model, datasets, prompts, and other related artifacts including Now Assist and AI leveraging Generative AI Controller.
    -   AI skills Approvals- Review and approval flows for Now Assist skills and other related assets like AI Models and AI datasets deployed through Now Assist or generative AI Controller.
    -   AI Control Tower Workspace- Intuitive workspace to surface governance tasks, reports, inventory, and insights.

</td></tr><tr><td>

AI Risk and Compliance

</td><td>

-   **[AI asset lifecycle management](https://www.servicenow.com/docs/access?context=ai-asset-lifecycle&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Manage the complete life-cycle of AI assets, from selecting appropriate AI systems to developing, deploying, and monitoring AI models and datasets. This feature helps maintain a centralized inventory, confirms consistent governance practices, and improves traceability and oversight across all stages of AI development and usage.

-   **[Perform impact assessment on an AI use case](https://www.servicenow.com/docs/access?context=perform-impact-assessment-of-ai-use-case&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Perform impact assessments to identify how AI systems, models, and datasets affect fundamental rights. This feature detects potential risks, such as copyright issues, algorithmic bias, privacy breaches, misinformation, and surveillance concerns, to support better oversight and risk management.

-   **[AI asset inventory risk management](https://www.servicenow.com/docs/access?context=request-risk-assessments-for-ai-systems&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Identify individual and specific risks associated with AI assets, such as AI systems, models, and datasets. Perform risk assessments on each identified risk separately.

-   **AI case management**

Manage and track cases or incidents related to AI use cases across the organization. This feature provides a structured approach to documenting, investigating, and resolving AI-related issues and cases, supporting consistent oversight and accountability.

-   **[AI framework content pack](https://www.servicenow.com/docs/access?context=install-ai-risk-content-pack&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Use the default AI framework content pack to prepare a compliance-ready inventory of AI assets. The content pack provides mappings to key AI regulations and standards, such as the European Union AI Act and the National Institute of Standards and Technology \(NIST\) AI Risk Management Framework \(AI RMF\). This feature helps organizations to align AI governance activities with regulatory requirements.

-   **[AI Risk and Compliance workspace](https://www.servicenow.com/docs/access?context=ai-risk-and-compliance-workspace&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

See a comprehensive overview of all your AI inventory-related information in the AI Risk and Compliance workspace. The AI Risk and Compliance workspace enables you to:

    -   Identify the risk classification of AI asset inventory.
    -   Identify the compliant and noncompliant controls for authority documents and policies.
    -   View AI systems based on state and department.
    -   View the AI assessments and risk assessments information.
    -   View information related to the control attestation, indicators, AI issues, AI cases, and policy exceptions.
    -   Generate report to help leaders identify, assess, and mitigate risks.
-   **360° Relationship Visualization of AI assets**

Explore the relationships between critical AI assets that impact your business, including controls, risks, and issues.

-   **[Collaborate with internal users](https://www.servicenow.com/docs/access?context=perform-impact-assessment-of-ai-use-case&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Collaborate with internal users by starting chats focused on the ethical, transparency, and accountability aspects of AI assets. Use discussions to document considerations, share feedback, and drive informed decision-making throughout the AI asset life-cycle.

-   **[Roles installed with AI Risk and Compliance](https://www.servicenow.com/docs/access?context=roles-installed-with-ai-risk-and-compliance&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

The following roles related to AI Risk and Compliance for managing AI systems across the enterprise were added:

    -   AI Risk and Compliance Admin \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_admin\]: Configure AI Risk and Compliance and delete AI systems.
    -   AI Risk and Compliance Manager \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager\]: Initiate impact assessment, risk assessment, and control attestations. Manage the life cycle of the AI system.
    -   AI Risk and Compliance Analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\]: Initiate impact assessment, risk assessment, and control attestations. Manage the life cycle of the AI system.

**Note:** AI Risk and Compliance Analyst can perform these actions only on the records assigned to them.

    -   AI Risk and Compliance User \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user\]: Create an AI case on the Employee Center and work on the assigned tasks. Perform control attestations.
    -   AI Risk and Compliance Reader \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_reader\]: Read the AI systems and AI impact assessments.

</td></tr><tr><td>

AI Search

</td><td>

-   **[Improve search precision and contextual relevance with hybrid search](https://www.servicenow.com/docs/access?context=hybrid-search-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Beginning with Now Assist in AI Search 15.0, customers with Now Assist in AI Search installed can enable the new hybrid search mode. Hybrid search combines keyword-based search with semantic understanding to deliver more accurate and relevant search results, with fewer zero-result searches.


-   **[Improve semantic search with third-party embedding models](https://www.servicenow.com/docs/access?context=ais-rag&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Use custom and third-party embedding models supported by the AI Search RAG application to generate more accurate and relevant semantic search results.


-   **[Limit the number of Task and Alert records indexed with indexed source guardrails](https://www.servicenow.com/docs/access?context=indexed-source-guardrails-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Index guardrail settings restrict index size and increase search performance by limiting the number of Task and Alert table records indexed for search.

-   **[Exclude search sources in a search profile from search result or Genius Result generation](https://www.servicenow.com/docs/access?context=genius-results-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Tune your search results by configuring search source exclusion settings in your search profiles. You can exclude a search source from being used to generate regular search results, Genius Result answers, or both. When excluding a search source's records from Genius Result answer generation, you can also choose to exclude its attachments.

-   **[Knowledge block content indexing](https://www.servicenow.com/docs/access?context=exclude-know-blocks-ais-index&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

When you index knowledge articles for search, AI Search now includes content from knowledge blocks to improve search recall. Administrators can disable indexing of knowledge block content if desired.

-   **[Boost relevancy for search results that match synonyms from a synonym dictionary](https://www.servicenow.com/docs/access?context=boost-results-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Define synonyms in a synonym dictionary and configure a result improvement rule to apply relevancy boosts \(positive or negative\) to search results that match any of those synonyms.

-   **[Customize semantic indexing settings for indexed sources](https://www.servicenow.com/docs/access?context=semantic-index-cfg-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Customize semantic indexing settings for your indexed sources.

-   **[Fuzzy numeric search](https://www.servicenow.com/docs/access?context=fuzzy-numeric-search&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Find records by their Number using numeric search terms like `23583`, with no need to match alphabetical prefixes or leading zeroes.


</td></tr><tr><td>

AIOps LEAP

</td><td>

-   **[Incident clustering and comprehensive summaries](https://www.servicenow.com/docs/access?context=aiops-leap-features&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

AIOps LEAP smartly categorizes IT incidents based on short descriptions and assignment groups. It uses historical data to get a deeper understanding of issues and summarizes them into actionable resolutions. AIOps LEAP consolidates information from different incidents to help with decision making and serves as a repository of knowledge.

-   **[Group incidents to create automation opportunities](https://www.servicenow.com/docs/access?context=aiops-leap-features&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

AIOps LEAP uses the ServiceNow® GAF \(Group Action Framework\) plugin to organize and group incidents based on specific parameters. These groups are clusters or automation opportunities. They are created by analyzing incident data such as work notes and resolution notes. AIOps LEAP uses these automation opportunities to generate resolution steps to help solve similar future incidents.

-   **[Automation recommendations and playbook generation](https://www.servicenow.com/docs/access?context=aiops-leap-features&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

AIOps LEAP identifies frequent issues and offers automation recommendations to address them. It streamlines and optimizes operational processes by creating actionable playbooks based on historical data and resolution workflows. Additionally, it builds a knowledge base by documenting workflows and solutions through detailed resolution steps, enabling further analysis, learning, and continuous improvement. These resolution steps can be shared across teams to facilitate collaboration and enhance operational efficiency, even without formal playbook creation. Thus, automated playbook generation is a valuable output of the AIOps LEAP platform.


-   **[Enhanced opportunities page](https://www.servicenow.com/docs/access?context=aiops-leap-features&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Enhancements &amp; Design changes to load all opportunities and enable to select all cards.


</td></tr><tr><td>

API

</td><td>

<table id="table_tcd_5v3_wqb"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[Console - Scoped, Global](https://www.servicenow.com/docs/access?context=ConsoleAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   error\(\)
-   group\(\)
-   groupCollapsedString\(\)
-   groupEnd\(\)
-   info\(\)
-   log\(\)
-   table\(\)
-   time\(\)
-   timeEnd\(\)
-   timeLog\(\)
-   trace\(\)
-   warn\(\)

</td></tr><tr><td>

[Fetch - Scoped, Global](https://www.servicenow.com/docs/access?context=FetchAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

fetch\(\)

</td></tr><tr><td>

[Fetch Headers - Scoped, Global](https://www.servicenow.com/docs/access?context=Fetch.HeadersAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   Headers\(\)
-   append\(\)
-   delete\(\)
-   entries\(\)
-   forEach\(\)
-   get\(\)
-   getSetCookie\(\)
-   has\(\)
-   keys\(\)
-   set\(\)
-   values\(\)

</td></tr><tr><td>

[Fetch Request - Scoped, Global](https://www.servicenow.com/docs/access?context=Fetch.RequestAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   Request\(\)
-   arrayBuffer\(\)
-   blob\(\)
-   bytes\(\)
-   clone\(\)
-   formData\(\)
-   json\(\)
-   text\(\)

</td></tr><tr><td>

[Fetch RequestInit - Scoped, Global](https://www.servicenow.com/docs/access?context=Fetch.RequestInitAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

requestInit\(\)

</td></tr><tr><td>

[Fetch Response - Scoped,Global](https://www.servicenow.com/docs/access?context=Fetch.ResponseAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   arrayBuffer\(\)
-   blob\(\)
-   bytes\(\)
-   formData\(\)
-   json\(\)
-   text\(\)

</td></tr><tr><td>

[GlideUser - Scoped](https://www.servicenow.com/docs/access?context=c_GlideUserScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   getTimeZoneLabel\(\)
-   getTimeZoneLabelLang\(\)

</td></tr><tr><td>

[OrderUtil - Scoped](https://www.servicenow.com/docs/access?context=OrderUtilScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   getStateFromOrder\(\)
-   isOrderInDraftState\(\)

</td></tr><tr><td>

[PDFGenerationAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=PDFGenerationAPIBothAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   convertToPDFAsync\(\)
-   convertToPDFWithHeaderFooterAsync\(\)

</td></tr><tr><td>

[ProcessMiningIntegrationAPI - Scoped](https://www.servicenow.com/docs/access?context=ProcessMiningIntAPIScoped&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   createProject\(\)
-   deleteProject\(\)
-   getBreakDownStats\(\)
-   getFindings\(\)
-   getMiningStatus\(\)
-   getProject\(\)
-   scheduleMining\(\)

</td></tr><tr><td>

[RESTMessageV2 - Scoped, Global](https://www.servicenow.com/docs/access?context=c_RESTMessageV2API&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

setAllowedRedirectURIs\(\)

</td></tr><tr><td>

[SOAPMessageV2 - Scoped, Global](https://www.servicenow.com/docs/access?context=c_SOAPMessageV2API&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   setAllowedRedirectURIs\(\)
-   setFollowRedirect\(\)

</td></tr><tr><td>

[UriMatcher - Scoped](https://www.servicenow.com/docs/access?context=UriMatcherScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   UriMatcher\(\)
-   match\(\)

</td></tr><tr><td>

[UriMatcherResponse - Scoped](https://www.servicenow.com/docs/access?context=UriMatcherResponseScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   getErrorMessages\(\)
-   isError\(\)
-   isFragmentMatches\(\)
-   isHostMatches\(\)
-   isMatch\(\)
-   isPathMatches\(\)
-   isSchemeMatches\(\)

</td></tr><tr><td>

[v\_record - Scoped, Global](https://www.servicenow.com/docs/access?context=v_recordAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

setLastErrorMessage\(\)

</td></tr></tbody>
</table><table id="table_ldq_g3c_tcc"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[Console - Scoped, Global](https://www.servicenow.com/docs/access?context=ConsoleAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   error\(\)
-   group\(\)
-   groupCollapsedString\(\)
-   groupEnd\(\)
-   info\(\)
-   log\(\)
-   table\(\)
-   time\(\)
-   timeEnd\(\)
-   timeLog\(\)
-   trace\(\)
-   warn\(\)

</td></tr><tr><td>

[Fetch - Scoped, Global](https://www.servicenow.com/docs/access?context=FetchAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

fetch\(\)

</td></tr><tr><td>

[Fetch Headers - Scoped, Global](https://www.servicenow.com/docs/access?context=Fetch.HeadersAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   Headers\(\)
-   append\(\)
-   delete\(\)
-   entries\(\)
-   forEach\(\)
-   get\(\)
-   getSetCookie\(\)
-   has\(\)
-   keys\(\)
-   set\(\)
-   values\(\)

</td></tr><tr><td>

[Fetch Request - Scoped, Global](https://www.servicenow.com/docs/access?context=Fetch.RequestAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   Request\(\)
-   arrayBuffer\(\)
-   blob\(\)
-   bytes\(\)
-   clone\(\)
-   formData\(\)
-   json\(\)
-   text\(\)

</td></tr><tr><td>

[Fetch RequestInit - Scoped, Global](https://www.servicenow.com/docs/access?context=Fetch.RequestInitAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

requestInit\(\)

</td></tr><tr><td>

[Fetch Response - Scoped,Global](https://www.servicenow.com/docs/access?context=Fetch.ResponseAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   arrayBuffer\(\)
-   blob\(\)
-   bytes\(\)
-   formData\(\)
-   json\(\)
-   text\(\)

</td></tr><tr><td>

[GlideDynamicAttribute - Global](https://www.servicenow.com/docs/access?context=GlideDynamicAttributeAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   getSysId\(\)
-   getName\(\)
-   getType\(\)
-   getGroupName\(\)
-   getPath\(\)
-   isTransient\(\)

</td></tr><tr><td>

[GlideDynamicAttributeStore - Global](https://www.servicenow.com/docs/access?context=GlideDynamicAttStoreAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

getDynamicAttributes\(\)

</td></tr><tr><td>

[GlideElementDynamicAttributeStore - Global](https://www.servicenow.com/docs/access?context=GlideElementDynamicAttStoreAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   getDynamicAttributesInSchema\(\)
-   getDynamicAttributesInStore\(\)

</td></tr><tr><td>

[GlideTransientDynamicAttribute - Global](https://www.servicenow.com/docs/access?context=GlideTransientDynamicAttributeAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   getSysId\(\)
-   getName\(\)
-   getType\(\)
-   getGroupName\(\)
-   getPath\(\)
-   isTransient\(\)

</td></tr><tr><td>

[GlideUser - Global](https://www.servicenow.com/docs/access?context=GUserAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   getTimeZoneLabel\(\)
-   getTimeZoneLabelLang\(\)

</td></tr><tr><td>

[PDFGenerationAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=PDFGenerationAPIBothAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   convertToPDFAsync\(\)
-   convertToPDFWithHeaderFooterAsync\(\)

</td></tr><tr><td>

[RESTMessageV2 - Scoped, Global](https://www.servicenow.com/docs/access?context=c_RESTMessageV2API&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

setAllowedRedirectURIs\(\)

</td></tr><tr><td>

[SOAPMessageV2 - Scoped, Global](https://www.servicenow.com/docs/access?context=c_SOAPMessageV2API&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   setAllowedRedirectURIs\(\)
-   setFollowRedirect\(\)

</td></tr></tbody>
</table><table id="table_gmt_y3c_tcc"><thead><tr><th>

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>

[AWA Offer Work API](https://www.servicenow.com/docs/access?context=awa-offer-work-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

POST /now/awa/documents/\{document\_table\}/\{document\_sys\_id\}/offer

</td></tr><tr><td>

[Continuous Integration and Continuous Delivery \(CICD\) Update Set API](https://www.servicenow.com/docs/access?context=cicd-update-set-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   POST /sn\_cicd/update\_set/retrieve
-   POST /sn\_cicd/update\_set/commitMultiple
-   POST /sn\_cicd/update\_set/preview/\{remote\_update\_set\_id\}
-   POST /sn\_cicd/update\_set/back\_out
-   POST /sn\_cicd/update\_set/commit/\{remote\_update\_set\_id\}
-   POST /sn\_cicd/update\_set/create

</td></tr></tbody>
</table><table id="table_x3d_kjc_tcc"><thead><tr><th>

Application

</th><th>

App Version

</th><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

Lead Management

</td><td>

v3.0

</td><td>

[LeadAPIHelperOOB - Scoped](https://www.servicenow.com/docs/access?context=LeadAPIHelperOOBAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   getJSONFromGR\(\)
-   getLeadsJSON\(\)
-   getTransformedLead\(\)

</td></tr><tr><td>

Lead Management

</td><td>

v3.0

</td><td>

[LeadAPIProcessUtilOOB - Scoped](https://www.servicenow.com/docs/access?context=LeadAPIProcessUtilOOBAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   processCreateLead\(\)
-   processGetAllLeads\(\)
-   processGrtLeadById\(\)
-   processUpdateLead\(\)

</td></tr><tr><td>

Lead Management

</td><td>

v3.0

</td><td>

[LeadAPIValidationUtilOOB - Scoped](https://www.servicenow.com/docs/access?context=LeadAPIValidationUtilOOBAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   validateLeadObjectForPatchCall\(\)
-   validateLeadObjectForPostCall\(\)

</td></tr><tr><td>

Sales and Service API Core

</td><td>

7.0.0

</td><td>

[IBQConfigBase API - Scoped](https://www.servicenow.com/docs/access?context=IBQConfigBaseAPIBoth&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   generateParentRecord\(\)
-   getRunMode\(\)
-   processInboundQueueRequest\(\)

</td></tr><tr><td>

Order Management

</td><td>

v12.5.0

</td><td>

[OrderGuide - Scoped](https://www.servicenow.com/docs/access?context=OrderGuideScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

isOrderInDraftState\(\)

</td></tr></tbody>
</table>|Application|App Version|Class|Methods|
|-----------|-----------|-----|-------|
|Customer Service Management|v1.2|[openFrameAPI - Client](https://www.servicenow.com/docs/access?context=c_openFrameAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)|setICContext\(\)|
|Mobile SDK|v2.9.0|[NowChatService class - Android](https://www.servicenow.com/docs/access?context=NowChatServiceAndroidAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)|updateTheme\(\)|
|Mobile SDK|v2.9.0|[NowWebService class - Android](https://www.servicenow.com/docs/access?context=NowWebServiceAndroidAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)|updateTheme\(\)|
|Mobile SDK|v2.9.0|[NowChatService class - iOS](https://www.servicenow.com/docs/access?context=NowChatServiceiOSAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)|updateTheme\(\)|
|Mobile SDK|v2.9.0|[NowChatServiceDelegate protocol - iOS](https://www.servicenow.com/docs/access?context=NowChatServiceDelegateiOSProtocol&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)|chatService\(\_chatService: NowChatService, systemThemeDidChange traitCollection: UITraitCollection\)|
|Mobile SDK|v2.9.0|[NowWebViewController class - iOS](https://www.servicenow.com/docs/access?context=NWebViewControlleriOSAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)|updateTheme\(\)|
|Mobile SDK|v2.9.0|[NowWebViewControllerDelegate protocol - iOS](https://www.servicenow.com/docs/access?context=NWViewControllerDelegateiOSProtocol&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)|nowWebViewController\(\_ nowWebViewController: NowWebViewController, systemThemeDidChange traitCollection: UITraitCollection\)|

<table id="table_qlh_nlc_tcc"><thead><tr><th>

Application

</th><th>

App Version

</th><th>

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>

Accounts Payable Operations

</td><td>

v2.0.0

</td><td>

[AP Invoice API](https://www.servicenow.com/docs/access?context=ap-invoice-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   POST /sn\_spend\_intg/ap\_invoice/xml

</td></tr><tr><td>

Expanded Product Model and Asset Classes

</td><td>

v1.0

</td><td>

[AI Assets API](https://www.servicenow.com/docs/access?context=ai-assets-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   GET /sn\_ent/asset/ai\_dataset/\{sys\_id\}
-   GET /sn\_ent/asset/ai\_model/\{sys\_id\}
-   GET /sn\_ent/asset/ai\_prompt/\{sys\_id\}
-   GET /sn\_ent/asset/ai\_system/\{sys\_id\}
-   POST /sn\_ent/asset/ai\_dataset
-   POST sn\_ent/asset/ai\_model
-   POST /sn\_ent/asset/ai\_prompt
-   POST /sn\_ent/asset/ai\_system
-   PUT /sn\_ent/asset/ai\_dataset/\{sys\_id\}
-   PUT /sn\_ent/asset/ai\_model/\{sys\_id\}
-   PUT /sn\_ent/asset/ai\_prompt/\{sys\_id\}
-   PUT /sn\_ent/asset/ai\_system/\{sys\_id\}

</td></tr><tr><td>

Customer Contracts and Entitlements

</td><td>

v6.0

</td><td>

[Service Contract API](https://www.servicenow.com/docs/access?context=servicecontract-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   POST /sn\_pss\_core/servicecontract
-   GET /sn\_pss\_core/servicecontract/\{id\}
-   POST /sn\_pss\_core/servicecontract/contractline
-   GET /sn\_pss\_core/servicecontract/contractline/\{id\}

</td></tr><tr><td>

Customer Contracts and Entitlements

</td><td>

v6.0

</td><td>

[Verify Entitlements API](https://www.servicenow.com/docs/access?context=verifyentitlements-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

GET /sn\_ent\_verify/verifyentitlements

</td></tr><tr><td>

Lead Management

</td><td>

v3.0

</td><td>

[lead API](https://www.servicenow.com/docs/access?context=lead-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   GET /sn\_lead\_mgmt\_core/lead
-   GET /sn\_lead\_mgmt\_core/lead/\{sys\_id\}
-   PATCH /sn\_lead\_mgmt\_core/lead/\{sys\_id\}
-   POST /sn\_lead\_mgmt\_core/lead

</td></tr><tr><td>

Sales Customer Relationship Management

</td><td>

v4.0

</td><td>

[Sales Agreement API](https://www.servicenow.com/docs/access?context=sales_agreement-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   GET /sn\_sales\_agmt\_core/salesagreement /\{id\}
-   POST /sn\_sales\_agmt\_core/salesagreement 

</td></tr></tbody>
</table>

</td></tr><tr><td>

Access Management

</td><td>

-   **[Security data filters](https://www.servicenow.com/docs/access?context=security-data-filters&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

Security data Filters enable you to control who can access sensitive data by restricting access to authorized users, regardless of how the data is accessed. Security data filters are applied before query execution, ensuring restricted data never leaves the database and prevents data leakage at the query level. Filters integrate into queries for GlideRecordSecure, GlideRecordSandbox, and GlideAggregateSandbox by default.

-   **[Related record access](https://www.servicenow.com/docs/access?context=related-record-access&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

Related record access integrated into the ACL framework enhances access management by enabling administrators to enforce specific ACLs for related tables. This ensures users can only access records in related tables, such as costs, estimations, or tasks, based on their permissions for the parent table, like projects or cases. Combined with broader ACL capabilities, Related record access ensures consistent, granular, and enforceable


</td></tr><tr><td>

Accounts Payable Operations

</td><td>

-   **[Tax Engine Integration](https://www.servicenow.com/docs/access?context=tax-engine-integration&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

The tax engine integration framework validates supplier-provided tax against system tax at invoice line level, maintains compliance with regional and global tax regulations. This integration triggers automatic tax validation, handles exceptions for tax variance and missing data, enables manual revalidation and rolling up of system tax.


-   **[Using Supplier Collaboration Portal in APO](https://www.servicenow.com/docs/access?context=using-supplier-collaboration-portal&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

In the supplier collaboration portal home page, the supplier contact can choose to view invoice and inquiry cases associated with their account.

Supplier contacts can be assigned with multiple suppliers.


-   **[Set APO properties](https://www.servicenow.com/docs/access?context=set-apo-properties&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

The one-stop property page provides great flexibility and ease of configuration to users with admin roles. AP admin and integrator use the APO properties page to set the parameters that control the invoice line mapping, invoice ingestion API, and exception management. Depending on the invoice line-mapping properties set, AP admin and integrator can choose to review and confirm the invoice line mapping results generated by rule-based engine and Now Assist.


-   **[Using Playbook in Accounts Payable Operations](https://www.servicenow.com/docs/access?context=how-to-use-playbook&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Playbook activity card displays updated invoice statuses. AP specialist reviews and acts on the mapping recommendations by Now Assist.


-   **[Now Assist for Accounts Payable Operations \(APO\)](https://www.servicenow.com/docs/access?context=now-assist-apo&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Activate the purchase order line-mapping skill in the Now Assist Admin console to enable automatic mapping of invoice lines with purchase order lines using Now Assist.

Activate the invoice data extraction skill in the Now Assist Admin console to leverage GPT-4o capabilities in extracting invoice information using Document Intelligence and reducing the manual effort.

Generate invoice case summarization in multiple languages with the multi-language support in the Now Assist console.

With the Now Assist panel, you can get assistance from generative AI to solve invoice case-related issues faster.

As a fulfiller, you can learn about the details of a purchase order and its associated cases from record summarization generated by Now Assist.

Take advantage of the translation capabilities available in the Now Assist for user-generated content.

A new requester role is added to access Now Assist Accounts Payable Operations features powered by generative AI. Customers need to explicitly grant these roles to users for access to GenAI features and capabilities.


-   ****

Use agentic workflows in Accounts Payable Operations to resolve invoice inquiry cases raised by employees and suppliers. These workflows also help track associated invoice records efficiently. With an agentic workflow, you can process a high volume of invoice inquiries that come through email attachments to significantly reduce the workload of human agents.


</td></tr><tr><td>

Adoption Services

</td><td>

-   **[Guided Setup](https://www.servicenow.com/docs/access?context=guided-setup&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

Create additional tasks under Guided Setup using page macroponent as an app owner. You can also access and execute these tasks with an admin role.

Add new steps to guided setups in progress during Playbook Experience.


</td></tr><tr><td>

Advanced AI Search Management Tools

</td><td>

-   **[AI Search analytics dashboard](https://www.servicenow.com/docs/access?context=ai-search-analytics-dashboard&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

The **Search application** interactive filter now allows analysts to review performance metrics and trends for search applications used in Recommended Actions.


-   **[AI Search analytics dashboard](https://www.servicenow.com/docs/access?context=ai-search-analytics-dashboard&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

The **Search application** interactive filter now allows analysts to review performance metrics and trends for the Mobile Platform search application.


</td></tr><tr><td>

Advanced Risk

</td><td>

-   **[Generative AI risk assessment summarization](https://www.servicenow.com/docs/access?context=generate-risk-assessment-summary-genai&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Generate a risk assessment summary from your inherent, residual, target risks, and control effectiveness data using the Now Assist for IRM application. The summary highlights key insights to help your approvers quickly understand the context before approving the risk assessments. You can also analyze details such as open issues, risk response tasks, action items, and calculated risk scores to support your approval decision. Check your entitlements to confirm whether you have access to risk assessment summarization.

-   **[Reassess a risk assessment project](https://www.servicenow.com/docs/access?context=reassess-risk-assessment-project&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Review completed risk assessment projects to reflect new insights or changing conditions. All previously assessed risks in this project are automatically carried over and reassigned to the designated assessor. Confirm continuity, minimize manual effort, and enhance efficiency in your risk management process.

-   **[Copy risk responses from the previous assessment](https://www.servicenow.com/docs/access?context=perform-assessment-on-risk-assessment-project&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Copy responses from a previous risk assessment during the reassessment of a risk assessment project to streamline the assessment process. All prior responses are automatically copied, saving time and maintaining consistency.

-   **[Remove risks from assessment](https://www.servicenow.com/docs/access?context=perform-assessment-on-risk-assessment-project&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

As a risk assessor, you can remove risks from the risk assessment project while performing the assessment, which also removes all responses associated with that risk. Removed scoped risks remain part of the project but are marked as not applicable for reporting purposes. However, removed ad hoc risks are completely deleted.

-   **[Manage risk response task workflow](https://www.servicenow.com/docs/access?context=configure-ram&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Manage and enable the risk response task workflow from the RAM form to enable users to create, delete, remove, edit, and link risk response tasks within an assessment.

-   **[Reassign assessor for a risk assessment project](https://www.servicenow.com/docs/access?context=reassign-assessor-for-risk-assessment-project&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Reassign assessors for multiple in-progress risk assessment projects simultaneously to minimize disruptions during stakeholder transitions.

-   **[Configure risk color styles for the Next Experience](https://www.servicenow.com/docs/access?context=create-risk-color-style&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Define and preview colors for the risk and advanced risk components in the Next Experience through a configurable system rather than having to use hex codes. The transition has been made from a hex code color management system to a configurable system that supports the highlighted value component colors. This feature addresses theming and accessibility issues. You can define the color and variant, and preview them using the Next Experience color styles tab on the Risk color style form.

**Note:** The default color for the customized risk color style is set to Critical, with the variant set to Primary. You can manually change the color and variant based on the requirement.


</td></tr><tr><td>

Advanced Work Assignment

</td><td>

-   **[Service channels](https://www.servicenow.com/docs/access?context=awa-service-channels&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

Run AWA assignments on different nodes or cadences for different service channels to improve performance and resilience.


-   **[Using Advanced Work Assignment](https://www.servicenow.com/docs/access?context=using-awa&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

Enable agents with the ability to provide wrap-up codes or notes for interactions or segments that the agent was involved in.


</td></tr><tr><td>

Agent Client Collector

</td><td>

-   **[Scan your resource directories for file attributes](https://www.servicenow.com/docs/access?context=directory-scan-checks-policies&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Starting in version 3.13.0, run a check to receive information on the directory file's integrity, size, space, response time, and age.

-   **[Conserve MID Server resources by using MID-less installation for Agent Client Collector](https://www.servicenow.com/docs/access?context=acc-itom-cloud-services&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Starting in version 3.6.5, conserve MID Server resources for more persistent features by using the MID-less installation when installing Agent Client Collector. With this installation, you don't need a MID Server in your system architecture.

-   **[Create tasks to address Agent Client Collector errors](https://www.servicenow.com/docs/access?context=create-error-task&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Starting in version 4.3.0, create tasks to resolve errors relating to the Agent Client Collector. Tasks are assigned to personnel who investigate the underlying issues and work to resolve the errors.

-   **[Use a proxy server with MID-less installation](https://www.servicenow.com/docs/access?context=acc-yml-options&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Starting in version 4.3.0, enable using a proxy server when installing Agent Client Collector without a MID Server.

-   **Discovery MSSQL server components**

Starting in version 1.3.0, enable discovery of MSSQL components by running Discovery as a local system user.

-   **Java certification Discovery through file-based discovery**

Starting in version 1.3.0, discover java file information using Agent Client Collector for Visibility - Content \(ACC-VC\) file based discovery. File based discovery locates java files that are installed on the system but not running, enabling retrieval of data used for licensing and auditing.

-   **[Enable high volume upgrade of agents](https://www.servicenow.com/docs/access?context=acc-high-volume-upgrade&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Starting in version 4.3.0, enhance efficiency by performing high-volume upgrade of large numbers of Agent Client Collector installations at once.

-   **[Block event creation for non-existent entities](https://www.servicenow.com/docs/access?context=prevent-events-nonexistent-entities&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Starting in version 3.13.0, block the creation of events and alerts if the process monitoring and log files don't exist in their indicated location.

-   **[Control how check results are sent](https://www.servicenow.com/docs/access?context=create-edit-policies&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Starting in version 3.6.5, configure the circumstances when check results are sent.

-   **[Configure and receive notifications of agent key expiration](https://www.servicenow.com/docs/access?context=agent-registration-key-configuration&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Starting in version 3.6.5, receive notifications that indicate when an agent registration key is expiring.

-   **[Monitor network host availability](https://www.servicenow.com/docs/access?context=network-host-availability-check&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Starting in version 4.1.0, use a new check to verify network host availability.

-   **[Identify software running on Linux and Windows devices](https://www.servicenow.com/docs/access?context=acc-visibility-checks-policies&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Starting in version 4.1.0, identify the software that is running on your Linux and Windows servers and devices by using file-based Discovery. File-based Discovery enables you to maintain the records of your software licenses and helps you to evaluate any threats from unwanted files.

-   **[Store ServiceNow instance credentials in the Google Cloud Secret Manager when the Informer uses Google Kubernetes Engine \(GKE\)](https://www.servicenow.com/docs/access?context=cnov-deploy-prepare&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

If your organization uses Google Kubernetes Engine \(GKE\) you can store the secret in Google Cloud Secret Manager. The Kubernetes Visibility Agent Informer can then pull the ServiceNow credentials for accessing your instance from the Google Cloud Secret Manager.

-   **[Use a custom CA to enable the Informer to communicate with the ServiceNow instance when using a custom root CA](https://www.servicenow.com/docs/access?context=cnov-deploy-prepare&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Mount a custom certificate authority into the Kubernetes Visibility Agent Informer pod to enable the Informer to communicate with the instance when a custom root CA is used.


</td></tr><tr><td>

Agent Workspace for HR Case Management

</td><td>

-   **[Survey responses](https://www.servicenow.com/docs/access?context=t_ViewAnHRTask&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

View employee responses collected from an employee via the survey form sent through an HR task.


-   **[Response templates](https://www.servicenow.com/docs/access?context=hr-agent-ws-using-response-template&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Display response templates based on the language preference of selected user.

-   **[Copy a case in Agent Workspace for HR Case Management](https://www.servicenow.com/docs/access?context=copy-case-hr&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Avoid having to fill in the fields of a case manually by creating a copy of a case to auto-populate the case values.

-   **[HR Triaging Dashboard](https://www.servicenow.com/docs/access?context=hr-triaging-dashboard&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

View your teams' case assignments based on categories such as priority, HR service, or HR assignment group. Drag a case card from one lane to another to automatically update the priority, HR service, or assignment group of a case.

-   **[HR Walk-up](https://www.servicenow.com/docs/access?context=hr-walkup&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Provide a convenient and efficient way for users to seek in-person or remote assistance, report issues, and receive guidance from HR agents through designated walk-up centers.


-   **[Page configurations](https://www.servicenow.com/docs/access?context=page-configurations&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Configure the layout and functionality of the HR Agent landing page or HR case page. You can preview your settings before implementing them.


-   **[PDF template preview](https://www.servicenow.com/docs/access?context=hr-agent-ws-create-temp&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Preview a PDF document template attached to an HR case rather than being able to preview only HTML document templates.


-   **[Link child cases](https://www.servicenow.com/docs/access?context=t_CreateAnHRCase&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Associate child cases to an HR case.


-   **[Delegation list](https://www.servicenow.com/docs/access?context=hr-agent-ws-lists&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

View cases delegated to you or that you have delegated to other HR agents. The Delegation list appears only when you have activated the Granular Delegation \(com.glide.granular\_service\_delegation\) plugin.

-   **[Agent Workspace for HR Case Management contextual side panel](https://www.servicenow.com/docs/access?context=agent-ws-hr-case-mgmt-context-sidebar&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**
    -   Apply template values to the HR case without having to fill in values manually.
    -   Download or delete multiple attachments at once.

-   **[Configure fields for Bulk case request](https://www.servicenow.com/docs/access?context=segment-group-aws&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Configure fields that you want to view in the User segment group form in bulk case request through the Case Creation Configuration form.


</td></tr><tr><td>

Agent experience for CSM

</td><td>

-   **[Chat interaction session tabs](https://www.servicenow.com/docs/access?context=csm-workspace-chat-session-tabs&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Use the following features to provide your agents with information about their current chats:

    -   Display informational messages in the session tabs that notify the agent of the current chat condition such as "Chat is in wrap-up" or "Chat has ended."
    -   Use background colors to distinguish between the active and inactive tabs. For inactive tabs, configure different colors to alert agents to the chat threshold timers.
    -   Use a counter to display the number of unread chat messages.
    -   Use a separator in the chat window between the older messages and the newer unread messages.
    -   Configure a minimum of one and up to a maximum of three chat SLA threshold timers that alert agents to unread messages in inactive chats. For each level, you can also select a time value and a unique color.
-   **[Voice interaction record page](https://www.servicenow.com/docs/access?context=csm-native-voice-record-page&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Enable Contact Center as a Service \(CCaaS\) providers to display native voice integrations in CSM Configurable Workspace that agents can use to handle phone calls.

-   **[Interaction wrap-up for call and chat](https://www.servicenow.com/docs/access?context=interaction-wrapup-modeless-dialog&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Provide agents with enough dedicated time after each call or chat to finalize the interaction details and wrap up their work before starting a new conversation.

-   **[Customer history component](https://www.servicenow.com/docs/access?context=customer-central&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Enable agents to view a customer's activities in the contextual side panel. Agents can search and filter the activities in the list and select a date range. For more information about the Customer history component, see [Next Experience Components documentation](https://developer.servicenow.com/dev.do#!/reference/next-experience/components?&query=&order_by=nameAsc&limit=120&offset=0&categories[]=uib_component&categories[]=uib_macroponent-component&categories[]=uib_facades).

-   **[Quick start tests for Customer Service Management](https://www.servicenow.com/docs/access?context=quick-start-tests-csm&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Customer Service Management works as expected. If you customized Customer Service Management, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

App Engine Studio

</td><td>

-   **[App Readiness and Compliance Report](https://www.servicenow.com/docs/access?context=app-readiness-report&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

As an App Engine Admin, use the App Readiness and Compliance report in AEMC to check if the apps you’re making are ready to go live. You can run an instance scan suite that looks for any issues that can impact app deployments. This feature helps determine if the app is prepared for use in the real world.


</td></tr><tr><td>

Application Manager

</td><td>

Yokohama patch 11

-   **[Now Assist suites for version compatibility](https://www.servicenow.com/docs/access?context=now-assist-app-mgr&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Use the Application Manager to install and update Now Assist applications with suites of compatible application versions. Now Assist suites help verify that new Now Assist applications and versions remain compatible with the ones already installed to your instance.

-   **[Application state indicators](https://www.servicenow.com/docs/access?context=app-mgr-state-indicators&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Review information about any applicable installation considerations, requirements, and blockers in the header of application details.


</td></tr><tr><td>

Application Vulnerability Response

</td><td>

-   **Enhancements to Application Vulnerability Response**

The Unassign workflow is supported for application vulnerable items \(AVITs\) and remediation tasks \(AVULs\).

    -   Streamline application vulnerability assignments with the **Unassign** UI action from the more actions menu on an AVIT.
    -   Reassign incorrectly assigned AVITs, clarify ownership for reassessment, and maintain accurate triage records in workspace views.
    -   You have the option to send unassign requests for approval prior to clearing the Assigned to and Assignment group fields on records.
-   **[SBOM document upload via Github Action](https://www.servicenow.com/docs/access?context=vr-sbom-supported-apps&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Upload valid Software Bill of Material \(SBOM\) documents to ServiceNow platform with the help of GitHub Action.

-   **[Create application remediation tasks manually in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-create-remediation-task&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

With the sn\_vul.app\_sec\_manager role, you can create application remediation tasks manually by selecting some or all the records in the Application vulnerable items’ lists in the Vulnerability Manager Workspace. These records are grouped into one or more remediation tasks according to the grouping criteria selected while creating application remediation tasks.

-   **[Create application remediation tasks manually in the IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-create-remediation-task&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

With the sn\_vul.app\_security\_champion role, you can create application remediation tasks manually by selecting desired records in the Application vulnerable items’ lists in the IT Remediation Workspace. These records are grouped into one or more remediation tasks according to the grouping criteria selected while creating application remediation tasks.

-   **[Manual Ingestion of vulnerabilities for application vulnerability response](https://www.servicenow.com/docs/access?context=manual-ingestion-of-vulnerabilities-for-application-vulnerability-response&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Import AVITs from external sources via a standardised template \(e.g., CSV, Excel\) and manage Penetration test findings lifecycle. Now, you can ingest vulnerability data, including details such as affected application, vulnerability description, severity, remediation recommendations, including other necessary details. This enhancement allows you to simplifies the process of consolidating vulnerability data from diverse sources into a centralised Penetration test workspace.

-   **[Penetration Test Workspace](https://www.servicenow.com/docs/access?context=penetration-testing-dashboard&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Monitor your penetration test requests and findings as well as your team's overall progress in the Penetration Test Workspace. Prioritize tests that need your attention, track findings, and view assignments with the following data visualizations on the dashboard:

    -   Important items.
    -   Penetration test requests that are critical and by state.
    -   Reported findings.
    -   Overall remediation progress based on assignment.
-   **[Enhancements to Penetration Test Assessment Requests](https://www.servicenow.com/docs/access?context=pen_test_dashboard_components&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Along with Full Penetration, Focused, and Re-test, the following assessment types are included for Penetration Test Assessment Requests forms in the Penetration Test Workspace:

    -   Emergency Release - Supports emergency releases that are required for rapid software updates to address critical issues like security vulnerabilities.
    -   Bug Bounty Program - Rewards ethical hackers to find and report security vulnerabilities.
    -   Release Approvals - Ensure that all necessary checks are completed before deploying new software.
    -   One-off reviews - Assess specific projects outside regular development and release cycles to evaluate performance and implement improvements.
    -   Executive Interest - Report on senior management's engagement and support for critical projects within the organization.
Enhancements to the Release Approval and Release Notes fields help you ensure quality and security for your pen test findings.

The following states have been added to the Release approval field:

    -   **Not Applicable** \(Default\).
    -   **Approved**.
    -   **Denied**.
You can add details to justify your release approvals in the Release notes field.

-   **[Associate CWEs for manual AVIT creation from Penetration Test Assessment Requests](https://www.servicenow.com/docs/access?context=penetration-testing-dashboard&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

On the Penetration test findings tab on Penetration Test Assessment Requests, you have the option to associate Common Weakness Enumerations \(CWE\)s or Common Vulnerabilities and Exposures \(CVE\)s in the **Vulnerability** field for manually created AVITs.

-   **Create change requests in Application Vulnerability Response**

Users with the sn\_vul.app\_sec\_manager and sn\_vul.app\_sec\_champion roles as well as users with the sn\_vul.app\_developer role who have the ITIL role can create change requests from remediation tasks in the Application Vulnerability Response application. Create change requests to expedite your investigation for application vulnerabilities \(AVIT\)s that require manual intervention.

    -   Create change requests with prepopulated information for scanned applications that are classified as configuration items \(CI\)s.
    -   The change request workflow in Application Vulnerability Response is similar to the workflow supported in Vulnerability Response. For more information about the Vulnerability Response change request workflow, see [Change management for Vulnerability Response](https://www.servicenow.com/docs/access?context=vuln-change_mgmnt_ovrvw&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US).
**Note:** Change requests are supported for Application Vulnerability Response only if the discovered application is associated with a configuration item \(CI\). You must set `Product model` to **False** in the Use Product Model \[sn\_vul.use\_product\_model\] system property to associate a discovered application with a CI.

-   **[Enhancements to the Software Bill of Materials Workspace](https://www.servicenow.com/docs/access?context=sbom-landing&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**
    -   You can delete multiple BOM entity records and their related components with bulk edit from the Software Bill of Materials SBOM SBOM Workspace.
    -   Any Application Vulnerable Items \(AVIT\)s that are associated with deleted BOM entities automatically transition to **Closed**.
-   **[View risk score details of a vulnerable items in the Work notes section](https://www.servicenow.com/docs/access?context=avm-calculators-rules&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Starting with v25.0.3 of Application Vulnerability Response, the system property **sn\_sec\_cmn.risk\_score\_changes\_add\_worknotes** is inactive by default. If you enable it, only then you can see all the changes related to the risk score of an application vulnerable item in the Work notes section. Additionally, the work notes are updated only if there’s a change in the risk score.


</td></tr><tr><td>

Audit Management

</td><td>

-   **[Matrix report in the Audit Workspace](https://www.servicenow.com/docs/access?context=matrix-report-audit-ws&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Analyze relationships between different variables by using a Matrix report that presents data in a structured format. Assess and document risks and the internal controls designed to mitigate those risks through the Risk and Controls Matrix.

-   **Entity Based Access for Audit Management**

Entity-based access enables you to create configurations for entities, entity classes, and entity types. When a user is qualified based on these configurations and has the minimum required roles, they can access to the following tables:

    -   Engagement
    -   Test Plan
    -   Control Test
    -   Observation
    -   Control to Engagement
    -   Test Plan to Engagement
    -   Risk to Engagement
    -   Issue to Engagement
    -   Entity to Engagement

</td></tr><tr><td>

Authentication

</td><td>

-   **[Continuous Authentication](https://www.servicenow.com/docs/access?context=ca-homepage&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

Use Continuous Authentication to require step-up authentication or re-authentication to the users before allowing access to sensitive or high-privilege information.

-   **[OAuth Grant Types for MID Server](https://www.servicenow.com/docs/access?context=oauth-outbound&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

Use the Authorization code, resource owner password credential, SAML bearer, and JWT bearer OAuth grant types of OAuth for outbound integration requests through the MID Server. Personal Auth is also supported through the MID server. MID Servers facilitate communication and data movement between a single ServiceNow® instance and external applications, data sources, and services.


</td></tr><tr><td>

Automated Test Framework

</td><td>

-   **[Reusable tests](https://www.servicenow.com/docs/access?context=atf-reuse-tests&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Reduce duplication of tests while invoked in several other tests by creating reusable tests, enabling test design to be more modular, reducing the effort and time while duplicating tests to manage a large number of tests across your instance. You can access the reusable tests from the new Reusable Test test step category. Use the Reusable Input Variables and Reusable Output Variables related lists to define data passing from one test step to another.

-   **[Reusable Tests category](https://www.servicenow.com/docs/access?context=test-steps-reusable-tests-category&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Reuse the test records created in the Reusable Test table from the new Reusable Test test step category. By default, the test records show up in the Reusable Test test step category, unless you define the record in a custom category in the Category field.


</td></tr><tr><td>

Benchmarks

</td><td>

-   The new KPI **Knowledge Articles created using Now Assist** is added to Productivity moments. This primary indicator shows how many knowledge base articles are created using Now Assist in a given period of time.
-   Leverage benchmarking for HRSM indicators to evaluate your performance in comparison to your peers.
-   New KPIs are added to the Call deflection - percentage. These new KPIs help you understand the number of Incidents that are created using Proactive Engagement and Digital End-User Experience self service.
-   New KPI is added to the self-solved percentage. This new KPI shares the number of times the issue is resolved using the Digital End-User Experience self service channels like Desktop Assistant, Now Assist panel, and Employee portal.

</td></tr><tr><td>

Business Continuity Management

</td><td>

-   **[Using latest assessment template for conducting BIAs](https://www.servicenow.com/docs/access?context=using-smart-asmt-template&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Conduct a Business Impact Analysis \(BIA\) by using the latest assessment template. The assessment template enables you to create questions of different types and automate the responses from existing data sources. You can configure the logic for calculating the recovery tier, recovery point objective, recovery time objective, or maximum tolerable downtime.

-   **[Adopting UIB page for improved performance](https://www.servicenow.com/docs/access?context=crisis-map-migration&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Leverage the Crisis map functionality that includes the latest UIB components. By adopting the UIB components, you can help to minimize development efforts and get more configuration options within the Crisis map application.

You can filter alerts by their state \(active or inactive\), severity level, location \(regions\), or source. You can refine your search, perform detailed queries, or edit actions on the alerts, so that it's easier to find both the alerts and assets on the map. Additionally, you can set the secondary values such as urgency, severity, category for the alerts in the Details card.

-   **[Using nested plans](https://www.servicenow.com/docs/access?context=creating-nested-plan-in-event&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Create nested plans in an event so that you can activate cross-references to multiple plans. You can use the hierarchical view to organize nested event tasks according to their dependencies with the work-breakdown structure \(WBS\) functionality. You can also monitor the progress bar to track the creation of related plans, event assets, or event tasks.


</td></tr><tr><td>

Care Team Operations for Biomed

</td><td>

-   **[Healthcare Biomed case overview](https://www.servicenow.com/docs/access?context=hcls-cto-biomed-case&version=yokohama&pubname=yokohama-healthcare-life-sciences&ft:locale=en-US)**

Expand biomed cases to support custom support requests for your organization’s biomed department.

-   **[Care Team Portal biomed requests](https://www.servicenow.com/docs/access?context=requesting-cto-biomed&version=yokohama&pubname=yokohama-healthcare-life-sciences&ft:locale=en-US)**

Request support from your organization’s biomed department with preconfigured record producers.

-   **[Healthcare biomed case and work order synchronization](https://www.servicenow.com/docs/access?context=cto-fulfilling-biomed&version=yokohama&pubname=yokohama-healthcare-life-sciences&ft:locale=en-US)**

Care Team Operations for Biomed links biomed cases and work orders. For customers with Clinical Device Management, care teams will gain visibility into all biomed cases reported by their team while also providing biomed support teams with the ability to fulfill cases as work orders and work order tasks.


</td></tr><tr><td>

Care Team Operations for Healthcare IT

</td><td>

-   **[Healthcare IT case overview](https://www.servicenow.com/docs/access?context=hcl-cto-it-case&version=yokohama&pubname=yokohama-healthcare-life-sciences&ft:locale=en-US)**

Expand healthcare cases to support custom support requests for your organization’s IT department.

-   **[Care Team Portal IT requests](https://www.servicenow.com/docs/access?context=requesting-cto-it&version=yokohama&pubname=yokohama-healthcare-life-sciences&ft:locale=en-US)**

Request support from your organization’s IT department with pre-configured record producers.

-   **[Healthcare IT cases and incident synchronization](https://www.servicenow.com/docs/access?context=fulfilling-cto-it&version=yokohama&pubname=yokohama-healthcare-life-sciences&ft:locale=en-US)**

Care Team Operations for Healthcare IT links Healthcare IT cases and incidents, enabling care teams to get visibility into all IT cases reported by their team while also providing IT support teams with the ability to fulfill cases as incidents


</td></tr><tr><td>

Case and Knowledge Management

</td><td>

-   **[HR Benchmarks](https://www.servicenow.com/docs/access?context=hr-benchmarks&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Use your key performance indicators \(KPIs\) to compare your performance with global benchmarks, which contributes to improved performance for your organization. Gain deeper insights by comparing your performance with your peers based on industry, size, or region, and implement recommendations for improving performance.

-   **[Employee passport](https://www.servicenow.com/docs/access?context=employee-passport&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Enable movement of employee data between departments and agencies for tracking, compliance, and regulatory purposes. Enable employee profile data, such as employment history and progression to be made available across different ServiceNow instances.

-   **[Survey responses](https://www.servicenow.com/docs/access?context=t_ViewAnHRTask&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

View employee responses by selecting the **View Responses** related link on an HR case. The **View Responses** related link displays responses that are collected from an employee via the survey form sent through the HR task of type **Collect Employee Input**.

-   **[Personal Data Rights in HR Service Delivery](https://www.servicenow.com/docs/access?context=rtbi-compliance-hr&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**
    -   Enable employees or alumni to request their personal information reports and have better visibility of their personal data that is held in the database of an organization.
    -   Include an approval step before deletion of data, confirming better compliance and audit capabilities with respect to General Data Protection Regulation \(GDPR\) requirements.
    -   Have HR Agents manage the approval process by generating reports using the Real-Time Business Intelligence \(RTBI\) configuration from the Data Classification \(com.glide.data\_classification\) plugin.

</td></tr><tr><td>

Case management for CSM

</td><td>

-   **[Case Management for Invoice Operations](https://www.servicenow.com/docs/access?context=csm-invoice-operations&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Use the Case Management for Invoice Operations application \(com.sn\_csm\_invoice\) to create cases for multiple invoices or for specific invoice lines. Agents can use these cases to process invoice-related services such as invoice disputes or requested corrections.

-   **[Process mining](https://www.servicenow.com/docs/access?context=process-mining&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

Use the following features to find process improvement opportunities:

    -   Use work notes analysis to learn the operational reasons behind activity transitions. This feature is Now LLM based.
    -   Mine the configured base system project to investigate the causes and get a clear view of the long resolution times and delays.
-   **[Quick start tests for Customer Service Management](https://www.servicenow.com/docs/access?context=quick-start-tests-csm&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Customer Service Management works as expected. If you customized Customer Service Management, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Change Management

</td><td>

-   **[User role for service desk agents](https://www.servicenow.com/docs/access?context=installed-with-cm-itsm-roles&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

With the sn\_service\_desk\_agent user role, increase operational efficiency by streamlining the process of asking about, gathering, and verifying information, as well as delivering quick resolutions. This role is designed for tier 1 service desk agents and is accessible when the ITSM Roles plugin \(com.snc.itsm.roles\) installed.

The sn\_service\_desk\_agent role includes the following roles:

    -   sn\_incident\_write
    -   sn\_problem\_write
    -   sn\_change\_write
    -   sn\_request\_write
    -   tracked\_file\_reader
Additionally, with the installation of the **ITSM Gen AI** \(**com.sn.itsm.gen.ai**\) plugin, the knowledge\_user and now\_assist\_panel\_user roles are integrated within the sn\_service\_desk\_agent role.

The sn\_service\_desk\_agent user role can be used starting with Service Operations Workspace version 6.1.

-   **[Change model Type field](https://www.servicenow.com/docs/access?context=t_CreateAChange&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

A new **Model** option has been added to the change model Type field to help users identify a change that is controlled by a change model. **Model** is the default if a Type has not been set for the change request of a certain change model.

-   **[No default Risk value for change requests](https://www.servicenow.com/docs/access?context=t_CreateAChange&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

There is no longer a default value for the Risk field on the Change Request table. The Risk value is set to **-- None --** until the risk is evaluated for the change request. This change ensures that no risk value is pre-assigned, allowing for a more accurate assessment before advancing the change

-   **[Mandatory field transition condition](https://www.servicenow.com/docs/access?context=create-a-change-model&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Ensure mandatory fields are completed before advancing through states for a change request, as defined by the Change Model. This feature enables change managers to mandate the completion of required fields before states can progress according to the Change Model.

-   **[Deny-unless ACLs on core tables](https://www.servicenow.com/docs/access?context=features-itsm-enhanced-security-change&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Prevent unauthorized access to change\_request and change\_task tables using deny-unless ACLs. The deny-unless ACLs restrict access on these tables for a non-authenticated user to perform actions such as read, write, delete, or create.

This feature is available for new or zBoot customers with the installation of the ITSM Enhanced Security Features \(com.snc.itsm.enhanced\_security\) plugin. Existing or upgrade customers must test and evaluate in their sub production instance before installing the plugin and implementing the security change in their production instance.


</td></tr><tr><td>

Cloud Account Management

</td><td>

-   **[About data visualization in Cloud Account Management](https://www.servicenow.com/docs/access?context=about-data-visualzation-cam&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Identify account violations and their severity using prebuilt policies in the Cloud Configuration Governance component. These scans support AWS, Azure, and GCP accounts. Confirm compliance and strengthen security by automatically detecting violations and categorizing them by severity across multiple cloud platforms.

Support for AWS account and Azure subscription requests via direct API integrations or Terraform and GitHub integrations.

Track cloud account spending details through integration with the Cloud Cost Management Workspace component. Provides real-time visibility into cloud expenditures, helping organizations stay within budget and optimize cost management.

**Note:** Tracking of cloud account spending only works when you've a Cloud Cost Management Workspace subscription.

-   **[About provision modes in Cloud Account Management](https://www.servicenow.com/docs/access?context=about-provision-modes&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Take advantage of flexible infrastructure management through provision mode, which also supports both Terraform Cloud/Terraform Enterprise \(supported in AWS\) and cloud native interface \(supported in AWS and Azure\).

-   **[Set up suspension of an AWS account using service control policy](https://www.servicenow.com/docs/access?context=configure-suspension-policy&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)[Set up suspension of a subscription using Azure policy](https://www.servicenow.com/docs/access?context=configuring-lock-unlock-policy-for-azure&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Suspend and reactivate accounts quickly in response to security or operational issues by leveraging a predefined AWS or Azure policy.

-   **[Add an unmanaged cloud account](https://www.servicenow.com/docs/access?context=add-unmanaged-account-cam&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Confirm consistent governance across all accounts with the ability to onboard accounts \(AWS and Azure\) created outside the CAM workflow, even for accounts that weren’t initially created through CAM.

-   **[Set up Terraform API key in ServiceNow](https://www.servicenow.com/docs/access?context=admin-setup&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Automate account provisioning and management using popular tools through integration with Terraform Cloud/Terraform Enterprise and AWS APIs.

-   **[Update cloud account details](https://www.servicenow.com/docs/access?context=update-account-ownership&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Manage account ownership for an account and optionally propagate the change to all CIs associated with that account.

-   **[Certify an account](https://www.servicenow.com/docs/access?context=certify-account&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Promote compliance with organizational standards by certifying cloud accounts using defined data certification processes.

-   **[Review request policies](https://www.servicenow.com/docs/access?context=viewing-pace-policy&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Set guardrails for processes like account approval, budget approval, and configuration assignments through customizable default automated policies. Manage these policies using the existing Policy as Code Engine component.

Customize the sequence of your approval process by using the standard playbook designer, also known as the Playbooks.


</td></tr><tr><td>

Collaborative Work Management

</td><td>

-   **[Keyboard shortcuts for workspace actions](https://www.servicenow.com/docs/access?context=cwm-spaces&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Use the keyboard shortcut to quickly search for and go to a Space, Board, or Doc.

    -   Mac OS: Option + F
    -   Windows OS: Alt + F
Also, the Search bar displays all the recent Spaces, Boards, and Docs that you've navigated to within the CWM workspace so that you can quickly select from the recent items without having to search for them again.

-   **[Real-time collaboration in Docs](https://www.servicenow.com/docs/access?context=cwm-docs&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Edit a Doc page concurrently with multiple other editors. Colored cursors denote the current location of editors on the page. You can choose to show or hide these indicators.

**Note:** To use the full functionality of Docs when using Docs v6.0.0 within CWM workspace, ensure that you upgrade Collaborative Work Management to v5.0.0. For more information, see [KB2017926](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2017926).

-   **[Requesting access to a Space or Board from its URL](https://www.servicenow.com/docs/access?context=cwm-spaces&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   CWM users can quickly request access to a Space or Board through the **Request access** button, which sends an actionable email request to Space owners and editors.
    -   Space owners can approve or reject the request directly from the email without having to open the CWM workspace.
-   **[Requesting to elevate user access role to Editor](https://www.servicenow.com/docs/access?context=share-space-in-cwm&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Easily send a request to Space owners and editors to request elevating your role to Editor by selecting the Viewing mode indicator in the Board header that indicates that you have only the Viewer role.

-   **[Managing access in the Share permissions modal](https://www.servicenow.com/docs/access?context=share-space-in-cwm&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Easily identify users who already have access to your Space and the users who requested access using the following two sections in the Share permissions modal.

    -   **People with Access** section: Manage the access level of existing collaborators to Editor, Viewer, or Owner, or remove them from the Space.
    -   **Pending Access** section: Review requests from users and choose to grant or deny them access to your Space.
-   **[Managing Space permissions for task assignees and other users](https://www.servicenow.com/docs/access?context=share-space-in-cwm&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Identify task assignees who don’t have access to the workspace through a lock icon next to the user name. This icon is visible in the List view of the Board in the columns of type People such as **Assigned to**, **Additional Assignee**, and **Assignment group**.

You can either use the workspace prompt to grant assignees Viewer access or choose to manage their access level later from the Share permissions modal.

-   **[Share task details with Task URLs](https://www.servicenow.com/docs/access?context=add-tasks-to-board-in-cwm&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Provide direct access to a specific CWM Task record to share with team members and stakeholders by copying its URL. The task opens in the side panel in the context of the Board that it belongs to, eliminating the need to search through multiple items on the Board.

-   **[Improved user experience for Board views](https://www.servicenow.com/docs/access?context=update-a-cwm-board-view&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Avoid accidentally losing unsaved Board view edits when you try to navigate away from the Board or refresh the browser tab by responding to a displayed workspace prompt.


</td></tr><tr><td>

Common Core

</td><td>

-   **[Entity Based Access](https://www.servicenow.com/docs/access?context=entity-based-access&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Implement data segregation and detailed access management so that users can access only the permitted data through entity-based access. Administrators can grant access to an entity's related records by adding users or user groups or by using entity user fields for entity-based access configuration. You can enhance your data security and minimize the risk of unnecessary data exposure while ensuring that only authorized users can access an entity's related records.

-   **[Gen AI issue summarization](https://www.servicenow.com/docs/access?context=generate-grc-issue-resolution&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Optimize the GRC issue resolution agentic AI workflow in the Integrated Risk Management application to help your issue managers and analysts resolve GRC issues with AI agents in the Now Assist panel. This workflow makes the issue resolution process more efficient by introducing targeted solutions for key steps in the issue management life cycle.

-   **[Gen AI issue summarization](https://www.servicenow.com/docs/access?context=now-assist-for-irm&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Summarize an issue by using the Now Assist for IRM application to provide quicker context gathering and contextual awareness. You can quickly analyze the issue records, including the description, activity log, and remediation tasks, and then generate a concise summary that provides you with a concise context of the issue to help you resolve it. Check your entitlements to determine whether you have access to issue summarization.

-   **[Searching user groups to understand the licensing treatment](https://www.servicenow.com/docs/access?context=grc-licensing-summary-dashboard&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Use the enhanced GRC licensing summary dashboard to understand the licensing treatment of users that are added to the group by roles that are mapped or assigned to the group.

-   **[Overview of an agency record](https://www.servicenow.com/docs/access?context=regulatory-agency-library-rcm&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

View the pie charts that depict the total number of emails that are sent to the various regulatory domains. On the overview page of a regulatory agency, you can view the domains where the maximum number of emails were sent and access the Emails Tracker page directly from an agency record. You can also filter and display only the relevant emails that were sent to a specific agency.

-   **[Document designer integration](https://www.servicenow.com/docs/access?context=configuring-audit-word-based-templates&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Update and add content by using Microsoft 365 for ServiceNow Reporting, which is now integrated with the Document designer application. You can insert data and reports into a Microsoft Word document.


</td></tr><tr><td>

Compliance Case Management

</td><td>

-   **[Smart assessments in Compliance Case Management](https://www.servicenow.com/docs/access?context=smart-assessment-in-ccm&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Utilize the Smart Assessment Engine to assess if your employees are compliant with the necessary regulations. The compliance case administrator configures the questionnaire, and when an action task moves from the **Draft** to the **Assigned** state, the assessment is sent. After the assessment, the compliance case manager examines the nature of the non-compliance and its impact on the organization. Based on the findings, appropriate remediation measures are identified and implemented to resolution. To use the smart assessment, a new property called enable\_smart\_assessments \(sn\_grc\_case\_mgmt.enable\_smart\_assessments\) is introduced with the default value as **true**.

-   **[Unified Task-driven UI experience](https://www.servicenow.com/docs/access?context=perform-smart-assessment-on-action-task&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

As a business user, use the **Tasks** page on the Employee Center for a consolidated view of all your tasks, enabling you to access and complete them efficiently. This page provides an easy way to manage all your assessments in one place, enabling you to view and perform tasks seamlessly.


</td></tr><tr><td>

Configuration Compliance

</td><td>

-   **[Identify Wiz Resource Types for import](https://www.servicenow.com/docs/access?context=wiz-assets-resources-tab&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Identify the Resource Types \(assets\) reported by Wiz in your environment on the Wiz Integration Resource Type configuration page in your ServiceNow AI Platform instance that you want to import.

The Resource Types that you select apply to all the primary Wiz vulnerability and compliance integrations except the Wiz Container Vulnerability Integration.

-   **[Wiz Backfill Integrations](https://www.servicenow.com/docs/access?context=wiz-backfill&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Retrieve and process data stored on the Wiz Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table for missing assets that were not processed by the primary compliance integrations with specialized Wiz Backfill Integrations.

    -   Test Results Backfill Integration
    -   Host Test Results Backfill Integration
    -   Issues Backfill Integration
The Wiz Backfill Integrations are activated by default.

-   **[Wiz Host Test Result Vulnerability Integration](https://www.servicenow.com/docs/access?context=wiz-host-test-result-tab-filters&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Import test results associated with the resource type, `VIRTUAL MACHINE` with the Wiz Host Test Result Vulnerability Integration. This integration is activated by default.

-   **[Create remediation tasks manually in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-create-remediation-task&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

With the sn\_vulc.admin role, you can create remediation tasks manually by selecting some or all the records in the Configuration Test Results lists in the Vulnerability Manager Workspace. These records are grouped into one or more remediation tasks according to the grouping criteria selected while creating remediation tasks.

-   **[Create remediation tasks manually in the IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-create-remediation-task&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

With the sn\_vulc.remediation\_owner role, you can create remediation tasks manually by selecting desired records in the Configuration Test Results lists in the IT Remediation Workspace. These records are grouped into one or more remediation tasks according to the grouping criteria selected while creating remediation tasks.

-   **[View risk score details of a test result in the Work notes section](https://www.servicenow.com/docs/access?context=config-compliance-calculator-rules&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Starting with v15.2.1 of Configuration Compliance, the system property **sn\_sec\_cmn.risk\_score\_changes\_add\_worknotes** is inactive by default. If you enable it, only then you can see all the changes related to the risk score of a test result in the Work notes section. Additionally, the work notes are updated only if there’s a change in the risk score.

-   **[Quick Start Tests for Configuration Compliance](https://www.servicenow.com/docs/access?context=available-quick-start-tests&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Configuration Compliance works as expected. If you customized Configuration Compliance, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

-   **[CMDB Workspace v8.0](https://www.servicenow.com/docs/access?context=cmdb-workspace&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US):**

You can now use the Create CI experience in CMDB Workspace to create a CI with a lookup identifier entry that contains mandatory attributes. When you select a lookup identifier entry on the Required attributes page, those mandatory attributes now appear and you can set their values for proper IRE processing. For more information, see [Create a CI manually in CMDB Workspace](https://www.servicenow.com/docs/access?context=create-ci-manual-cmdb-workspace&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

-   **[CMDB Workspace v7.6](https://www.servicenow.com/docs/access?context=cmdb-workspace&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US):**
    -   Access a centralized location with a comprehensive view of CI details by using the new CI form in CMDB Workspace. The form shows the attributes \(key attributes are highlighted on a Summary page\), tags, resources, activities, relationships, related services, health state, performance indicators, and CMDB 360 data that is associated with the CI. While viewing, you can also modify many of those CI details. For information about all the details on a CI form, see [Manage CI details in CI Form](https://www.servicenow.com/docs/access?context=ci-form-cmdb-workspace&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).
    -   Access the Data Certification dashboard in CMDB Workspace. The Data Certification dashboard provides the insights about the data certification activities and progress, policies and tasks, reports about certification instances, charts that show the aging certification tasks, and group and individual workloads. For more information, see [Data Certification Dashboard](https://www.servicenow.com/docs/access?context=data-cert-dashboard-workspace&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).
    -   [Create or manage a shared preset](https://www.servicenow.com/docs/access?context=unified-map-manage-shared-preset&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US). Save Unified Map filter settings as shared presets that any user on the team can access. This task requires the sn\_cmdb\_admin, sm\_admin, or admin role.
    -   [Access Unified Map from the main navigation panel](https://www.servicenow.com/docs/access?context=cmdb-workspace-unified-map&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US). Access Unified Map from the main navigation panel by navigating to **All** &gt; **CMDB Workspace** &gt; **Unified Map**.
    -   Archival and destroy processes of certification policy related records, are now separated from those processes for records of all other policy types. This separation facilitates the extension of the retention period of certification policy records, as follows:
        -   The table cleanup rule for table CMDB Data Management Policy Executions \[cmdb\_data\_management\_policy\_execution\], which is stored in the Auto Flushes \[sys\_auto\_flush\] table, now excludes certification policy execution records from recurring cleanups.

Retaining certification policy execution records instead of deleting them after 7 days is useful in situations where those records are needed for audits and are also useful for the Data Certification Dashboard, which is populated by these records.

        -   The Archive CMDB Data Management Tasks archive rule, that applied to all CMDB Data Manager policy execution records, now excludes certification policy records. At each archive run, this archive rule is configured to also automatically archive its related records in table CMDB Data Management Certification Task To Document \[sn\_cmdb\_ws\_dm\_certification\_task\_to\_document\] \(Archive Related Records\).
        -   The archive rule, Archive Certification Instances, is added to specifically archive certification policy execution records from the CMDB Data Management Policy Execution \[cmdb\_data\_management\_policy\_execution\] table. This new archive rule is configured to archive certification policy execution records 2 years after creation, and to destroy those records 7 years after they are archived.
        -   The archive rule, Archive Certification tasks, is added to specifically archive certification task records from the CMDB Data Management Task \[cmdb\_data\_management\_task table\].
        -   The archival of related records in table CMDB Data Management Certification Task To Document \[sn\_cmdb\_ws\_dm\_certification\_task\_to\_document\] is now moved as an Archive Related Records entry from the Archive CMDB Data Management Tasks archive rule to the new Archive Certification tasks archive rule.
-   **[SGC Central](https://www.servicenow.com/docs/access?context=sgcc-landing&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

Use the Service Graph Connector Central view, also known as the SGC Central view, in the CMDB Workspace to discover and install connectors, and then effectively manage the full life cycle of creating, editing, monitoring, and debugging connections.

-   **[Now Assist for Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=now-assist-landing-cmdb&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

Use the new Now Assist for CMDB agentic workflows, AI agents, and skills. The Now Assist CI summarizer AI agent summarizes the key details for CIs, such as the discovery and incident details, directly on the CI forms. The Manage duplicate CIs skill guides you step by step on how to use the deduplication templates to help maintain the health and integrity of CMDB.

-   **[Use Now Assist to search the CMDB for CIs](https://www.servicenow.com/docs/access?context=na-cmdb-awf-search&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

The CMDB search agentic workflow enables you to search for CI data by specifying any of several attributes of the CI of interest. The workflow accepts your natural language request, verifies your search goal, and then generates a keyword search, a single-table search with dot walks, or a multi-table search, depending on the information you provide. The workflow can infer CI relationship data to generate an appropriate query.

-   **[Getting advice from Now Assist on CMDB governance](https://www.servicenow.com/docs/access?context=na-cmdb-awf-governance&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

Data governance can be an overwhelming task. The CMDB Governance agentic workflow supports admins and owners by methodically working through the process of improving CMDB data governance. The objective is to ensure that users trust their data for the evolving outcomes they want to achieve.

-   **[Create a CI using Now Assist](https://www.servicenow.com/docs/access?context=na-cmdb-awf-ci-creator&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

Occasionally, you might need to create a CI manually. To help you, the workflow accepts your natural language request and verifies that it understands which class the new CI should belong to. The workflow then checks IRE policies to determine the required attributes for the CI and request that information. After you provide sufficient data, the workflow uses IRE to ensure that the proposed CI is not a duplicate, and then creates the Cl.

-   **[Configuring Unified Map — Admin settings](https://www.servicenow.com/docs/access?context=administer-unified-map&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

Configure general Unified Map settings for the workspace on your instance. Only a user with the sn\_cmdb\_admin role can configure these settings.

-   **[Viewing a summary of Unified Map contents in the Overview panel](https://www.servicenow.com/docs/access?context=unified-map-show-overview-panel&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

Use the new Overview panel to show the summary data for a map that is associated with the home node, including the counts and types of CIs, connections, and discovery sources.

-   **[Editing maps in Unified Map](https://www.servicenow.com/docs/access?context=unified-map-editing-map&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

While you work in the map editor, you can add CIs to the map and remove CIs from the map. You can also add, modify, and delete CI relationships in the CMDB.

-   **[Quick start tests for CMDB](https://www.servicenow.com/docs/access?context=quick-start-tests-cmdb&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that CMDB works as expected. If you customized CMDB, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Container Vulnerability Response

</td><td>

-   **Enhancements to the Vulnerability Manager and IT Remediation workspaces starting with version 2.13**

The Unassign workflow is supported for container vulnerable items \(CVITs\) and remediation tasks \(CVULs\).

    -   Streamline vulnerability assignments in the workspaces with the **Unassign** UI action from the more actions menu on a CVIT.
    -   Reassign incorrectly assigned CVITs, clarify ownership for reassessment, and maintain accurate triage records in workspace views.
    -   You have the option to send unassign requests for approval prior to clearing the Assigned to and Assignment group fields on records.
. You can use the following values imported from the Prisma Cloud Compute integration as conditions when you create or update your assignment rules to help you track ownership across your container environments.

    -   Cloud account IDs
    -   Image namespaces
    -   Registry
    -   Hosts
    -   Labels
    -   Status - Vendor status for a resolved \(`Fixed`\) vulnerability
-   **[Create container remediation tasks manually in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-create-remediation-task&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

With the sn\_vul\_container.vulnerability\_analyst or sn\_vul\_container.vulnerability\_admin role, you can create container remediation tasks manually by selecting some or all the records in the Container vulnerable items lists in the Vulnerability Manager Workspace. These records are grouped into one or more remediation tasks according to the grouping criteria selected while creating container remediation tasks.

-   **[Create container remediation tasks manually in the IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-create-remediation-task&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

With the role sn\_vul\_container.remediation\_owner, you can create container remediation tasks manually by selecting some or all the records in the Container vulnerable items’ lists in the IT Remediation Workspace. These records are grouped into one or more remediation tasks according to the grouping criteria selected while creating container remediation tasks.

-   **[Configure container vulnerable items \(CVITs\) granularity using Registry and data source](https://www.servicenow.com/docs/access?context=pcc-integration&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Starting with v2.12.2 of Container Vulnerability Response, you can configure the granularity of container vulnerable items \(CVITs\) using Registry information and data sources. Depending on the chosen data source, you can view either image or kubernetes information related to a CVIT record.

-   **[Additional columns in the container vulnerable items \(CVITs\) table](https://www.servicenow.com/docs/access?context=container-vul-items-fields&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Starting with v2.12.2 of Container Vulnerability Response, you can see the precise date and time when a CVIT was first discovered, last opened, resolved, and last found, ensuring clarity and accounting for different time zones.

-   **[View risk score details of a container vulnerable item in the Work Notes section](https://www.servicenow.com/docs/access?context=cvr-calculator-rules&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Starting with v2.12.2 of Container Vulnerability Response, the system property **sn\_sec\_cmn.risk\_score\_changes\_add\_worknotes** is inactive by default. If you enable it, only then you can see all the changes related to the risk score of a container vulnerable item in the Work notes section. Additionally, the work notes are updated only if there’s a change in the risk score.


</td></tr><tr><td>

Continuous Authorization and Monitoring

</td><td>

-   **[OSCAL Import landing page](https://www.servicenow.com/docs/access?context=import-oscal&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Import files for catalog and SSP models on the new OSCAL Import landing page. Once the import process is initiated, you can check the status under the Import status section.

-   **[OSCAL Export button](https://www.servicenow.com/docs/access?context=export-catalog-cam-ws&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Export selected control objectives in the OSCAL format with the new **OSCAL Export** button while in the control objectives list view.

-   **[ATO artifacts in Microsoft Word](https://www.servicenow.com/docs/access?context=generate-ato-artifacts-cam-ws&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Generate ATO artifacts from an authorization package in the Microsoft Word format. In CAM Workspace, you can use the **Generate SSP** drop-down list in a selected authorization package to generate the following reports:

    -   Security Assessment Plan \(SAP\)
    -   Authorization to Operate \(ATO\) Letter
    -   Executive Summary
This enhancement verifies that all ATO artifacts are formatted consistently and can be shared and reviewed.


</td></tr><tr><td>

Contract Management Pro

</td><td>

-   **[Link parent contract requests](https://www.servicenow.com/docs/access?context=cmpro-link-parent-cmr&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Establish a hierarchical relationship between the parent and child contract requests by using the **Link** option in the **Related contract requests** tab during drafting and negotiation phases.

Establish a hierarchical relationship between the parent and child contract requests and automatically inherit the configured fields from the parent request by using the **Link and inherit fields** option in the **Related contract requests** tab during drafting and negotiation phases.

The linked parent contract request appears in the **Related contract requests** tab and displays the parent-child hierarchy. The contract repository records that are associated with the parent and child contract requests are automatically linked after the contracts are signed.

Use the **Remove linked contract** option in the **Related contract requests** tab to remove the linked parent contract request when you have linked a wrong contract request or the linking is no longer required.

-   **[Perpetual contracts](https://www.servicenow.com/docs/access?context=cncore-work-ss-cntr-request-fulfiller&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Select the **Perpetual** check box in the Details tab of a contract request to classify it as a perpetual contract. When this check box is selected, the contract end date must be blank.

The **Perpetual** check box is available in contract requests that are initiated from Sales Customer Relationship Management and Source-to-Pay Operations.

-   **[Signature workflow for a contract request](https://www.servicenow.com/docs/access?context=cncore-signature-workflow&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

During the electronic signature process, one or more signatories can now choose to use a wet signature. In this scenario, the contract fulfiller uploads the partially signed document and sends the uploaded document to the remaining signatories to complete the signature process.


-   **[Add document content controls using Microsoft Word add-in for ServiceNow Contracts](https://www.servicenow.com/docs/access?context=cncore-add-contrl-wrd-addin&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Logout and application scope change functionality in Microsoft Word add-in for ServiceNow contracts.


</td></tr><tr><td>

Contract Management Pro for Legal Service Delivery

</td><td>

-   **[Contract amendments](https://www.servicenow.com/docs/access?context=snlc-amend-req-landing&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Contract amendments enable you to formally change, add, or remove terms in an existing contract without replacing the entire agreement. The Amendment feature enhances contract lifecycle management by enabling you to initiate, track, and finalize amendments to existing contracts with audit trail.

A new field, **Request type**, has been added to clearly distinguish between contract and amendment requests.

Each amendment is linked to its parent contract, and you can easily view the amendment history directly from the contract request. Additionally, a record producer is available in the base system, allowing you to submit and monitor amendment requests efficiently.

The following related lists are now available within the contract repository record to provide amendment details:

    -   Contract Requests: Displays all contract and amendment requests associated with the contract.
    -   Amendment Field Changes: Shows a detailed log of all field changes made through amendments, enabling easy tracking of modifications over time.
    -   Contract Documents: Provides access to all documents related to the contract, including those generated or updated as part of amendment processes. The signed contract and its amendment documents are stored in a centralized repository under the parent contract for easy access and managing all related documents from a single location.

</td></tr><tr><td>

Conversation Insights

</td><td>

-   **[Inferred CSAT](https://www.servicenow.com/docs/access?context=exploring-conversation-insights&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Inferred CSAT provides an estimated score computed using AI in real time by analyzing the entire sequence of the conversation.

-   **[CSAT factors](https://www.servicenow.com/docs/access?context=exploring-conversation-insights&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

The following CSAT factors provide explainability to the Inferred CSAT score.

    -   Resolution
    -   Confusion
    -   Effort
    -   Empathy
    -   Next Steps
    -   Frustration
    -   Transfers and Escalations
-   **[AI Agent Analytics dashboard](https://www.servicenow.com/docs/access?context=ai-agent-dashboard&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

The AI Agent Analytics dashboard includes visualizations with Inferred CSAT scores and factors by default.


</td></tr><tr><td>

Creator Studio

</td><td>

-   **[Generate a form from text prompts using the Build with Now Assist tab](https://www.servicenow.com/docs/access?context=creator-studio-dynamic-behavior&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Enable users to generate forms automatically from text prompts by using the Build with Now Assist dialog box.

-   **[Auto-populate question values on a form](https://www.servicenow.com/docs/access?context=creator-studio-edit-form&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Help users complete forms faster with the new **Add auto-fill** option, which automatically populates answers based on answers to questions that are record choices.

-   **[Use catalog variables in playbook activities and decisions](https://www.servicenow.com/docs/access?context=creator-studio-add-automation&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Playbook activities and decision branches can now be triggered by answers to one or more questions on a form when you configure the conditions.

-   **[Select your development experience](https://www.servicenow.com/docs/access?context=crs-choosing-your-experience&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Seamlessly change between development environments using the new experience switcher. Depending on the products and versions that are installed and the role you have, you can switch between the following environments:

    -   Creator Studio to get a no-code experience
    -   ServiceNow Studio to get a platform coding experience
    -   ServiceNow IDE to get a pro-code ServiceNow experience
-   **[Test forms with the new Try it button](https://www.servicenow.com/docs/access?context=creator-studio-try-it&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

As of Creator Studio version 27.2.2,you can test using published forms through a **Try it** button. After you submit the form, any associated playbooks run and their results appear in the generated record that opens in a new tab within Creator Studio.

-   **[Change the table for an app](https://www.servicenow.com/docs/access?context=creator-studio-admin-app-table&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

As of Creator Studio version 27.2.2, admins can change the table where data from apps built in Creator Studio is saved.

-   **[Seamlessly open apps in ServiceNow Studio](https://www.servicenow.com/docs/access?context=view-apps-creator-studio-home-page&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

As of Creator Studio version 27.2.2, you can open an app in ServiceNow Studio to make additional, more complicated edits by selecting an **Open with ServiceNow Studio** link from the app's tile on the Creator Studio home page.


</td></tr><tr><td>

Customer Contracts and Entitlements

</td><td>

-   **[Create contracts from product inventory](https://www.servicenow.com/docs/access?context=create-cont-ent-workflows-csm&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Enables customer to create and manage contracts for product inventory records.


-   **[New workspace view for service contracts and entitlements](https://www.servicenow.com/docs/access?context=components-installed-pss&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

A new workspace view named Service Contract Workspace has been added for customers on service contracts and entitlements in the Customer Service Management workspace. This view is set as the default view and can be changed by an administrator.


-   **[Enhancement on contract lines and entitlements](https://www.servicenow.com/docs/access?context=using-post-sales-support&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

View location and subscription pricing information on contract lines and entitlements.


-   **[Automatic renewal of contracts](https://www.servicenow.com/docs/access?context=using-customer-cnt-ent-wf&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Enables customers to configure the date and pricing details of contract renewal while creating initial contracts.


-   **[Enable renewal opportunity creation](https://www.servicenow.com/docs/access?context=using-customer-cnt-ent-wf&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Create an opportunity or an opportunity and quote when you renew service contracts and service contract lines.


-   **[Co-terminating of Contract lines](https://www.servicenow.com/docs/access?context=using-customer-cnt-ent-wf&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Enables customers to assign same start and end date to multiple quote lines.


-   **[End-of-life check​](https://www.servicenow.com/docs/access?context=cce-renew-service-contract&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Alert customers when the contract end date is exceeding the product offering end date during quote processing. Customers can then match the contract and product offering end date if required.


-   **[Renewal Uplift feature](https://www.servicenow.com/docs/access?context=cce-renew-service-contract&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Enables customers to set the pricing parameters of future renewals of contracts. You can select the markup or mark down percentage of the current contract price or you can apply the market price of the contract at the time of renewal.


</td></tr><tr><td>

Customer Success Management

</td><td>

-   **[Health framework](https://www.servicenow.com/docs/access?context=account-lifeycle-health-frmwk&version=yokohama&pubname=yokohama-acct-lifecycle-events&ft:locale=en-US)**

Define the key business and operational indicators and their impact on the overall health of an engagement. You can provide insights that help identify the trends and determine if the engagement is stable.

-   **[Risk framework](https://www.servicenow.com/docs/access?context=account-lifecycle-risk-frmwrk&version=yokohama&pubname=yokohama-acct-lifecycle-events&ft:locale=en-US)**

Centralize, track, and monitor the relational risks so that you can reduce customer turnover. You can identify risk signals and create repeatable remediation plans.

-   **[Success blueprint builder](https://www.servicenow.com/docs/access?context=account-lifecycle-success-blueprint&version=yokohama&pubname=yokohama-acct-lifecycle-events&ft:locale=en-US)**

Create standardized objectives and outcomes for an engagement. Your customer success managers can prioritize the requirements and identify the outcomes that provide the maximum customer impact.

-   **[Success initiative roadmap](https://www.servicenow.com/docs/access?context=account-lifecycle-success-roadmap&version=yokohama&pubname=yokohama-acct-lifecycle-events&ft:locale=en-US)**

Create a timeline view of the success initiatives and view the status, timing, and priority of these activities.

-   **[Touchpoints enhancements](https://www.servicenow.com/docs/access?context=account-lifecycle-touchpoints&version=yokohama&pubname=yokohama-acct-lifecycle-events&ft:locale=en-US)**

Use a touchpoint to track and manage your customer interactions through meetings and emails. With the touchpoint planner, you can help to ensure that all customer interactions and related activities are taking place on time with expected results.

-   **[Case summarization for onboarding cases, engagements, and touchpoints](https://www.servicenow.com/docs/access?context=now-assist-spmc&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Use generative AI to get a high-level summary of the status of your engagements, onboarding cases, and touchpoints.


</td></tr><tr><td>

Data Loss Prevention Incident Response

</td><td>

-   **[Create a Data Loss Prevention Incident Response SLA trigger](https://www.servicenow.com/docs/access?context=sla-records&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Enable prompt and efficient responses to incidents by creating SLA triggers.

-   **[Create a Data Loss Prevention Incident Response SLA definition](https://www.servicenow.com/docs/access?context=dlp-sla-definitions&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Outline the conditions and duration for responding to data breaches by creating Data Loss Prevention Incident Response SLA definitions.

-   **[Create an Application in Proofpoint and Obtain Client Credentials](https://www.servicenow.com/docs/access?context=create-application-proofpoint-dlp&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Create an application in Proofpoint and configure the required settings to obtain client credentials. These credentials enable secure access to the Proofpoint API for seamless integration and automation.

-   **[Internet Content Adaption Protocol \(ICAP\) integration for DLP IR](https://www.servicenow.com/docs/access?context=icap-dlp-integration&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Integration supports the ingestion of Data Loss Prevention Incident Response alerts, allows the fetching of match content, and evidence files from Amazon S3 created on the ICAP supported Data Loss Prevention Incident Response deployment.

-   **[Configure evidence file storage](https://www.servicenow.com/docs/access?context=configure-evidence-file-storage&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Store evidence files directly in your ServiceNow instance with Proofpoint integration, by enhancing the ability to manage and track evidence files within the platform.

-   **[Configure evidence file storage](https://www.servicenow.com/docs/access?context=config-evidence-file&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Symantec DLP supports evidence file storage to securely store the evidence files for the DLP Incidents.

-   **[Preview Evidence files for DLP incidents of type Exchange Online, OneDrive, and SharePoint](https://www.servicenow.com/docs/access?context=preview-file-dlp-microsoft&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US).**

With the DLP Microsoft integration, preview evidence files in the DLP Workspace in the Microsoft OneDrive, Microsoft Exchange Online, and Microsoft SharePoint formats. You can preview and download evidence files directly from the preview interface, simplifying evidence review and retrieval.

-   **Netskope integration: [Preview evidence files](https://www.servicenow.com/docs/access?context=preview-files-netskope&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US) and [Download evidence files](https://www.servicenow.com/docs/access?context=download-files-netskope&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

With Netskope integration you can preview and download evidence files directly from the preview interface, simplifying evidence review and retrieval.

-   **[Preview evidence files](https://www.servicenow.com/docs/access?context=using-dlp-ops-portal&version=yokohama&pubname=yokohama-security-management&section=preview-evidence-files&ft:locale=en-US)**

Preview evidence files and download them directly from the preview interface, simplifying evidence review and retrieval.

-   **[Playbook for Data Loss Prevention Incident Response](https://www.servicenow.com/docs/access?context=using-dlp-ops-portal&version=yokohama&pubname=yokohama-security-management&section=playbook-for-dlp&ft:locale=en-US)**

Introduced playbooks in the DLP Workspace to enhance operational efficiency.

-   **[Create incident consolidation rules](https://www.servicenow.com/docs/access?context=configure-incident-consolidation-rules-to-consolidate-your-dlp-incidents&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Parent incident is always assigned the highest priority among consolidated incidents, enhancing incident management accuracy.


</td></tr><tr><td>

Data Management

</td><td>

-   **[Data Management Console](https://www.servicenow.com/docs/access?context=viewing-data-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

View a summary of storage consumption on your instance and manage the growth of data directly from the Data Management Console.

-   **[Table cleaner scalability improvements](https://www.servicenow.com/docs/access?context=deleting-older-records&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Automatically delete older or unwanted records at scale.


</td></tr><tr><td>

Data Privacy

</td><td>

-   **[AL/ML Based Data Discovery for Real Time Anonymization](https://www.servicenow.com/docs/access?context=now-assist-for-data-privacy-landing&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

Use AI/ML data discovery using Named Entity Recognition \(NER\) models to discover sensitive data that does not follow a pattern like name, address, organizations, and more; and run real-time anonymization.

-   **[Configuring Data Privacy for Now Assist](https://www.servicenow.com/docs/access?context=configure-now-assist-data-privacy&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

Sanitize sensitive data entered in Now Assist prompts to prevent data leakage without impacting the response.

-   **[Discover sensitive data from attachments.](https://www.servicenow.com/docs/access?context=configure-data-discovery-jobs&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

Discover and report on sensitive data from attachments.


</td></tr><tr><td>

Data management for CSM

</td><td>

-   **[Naming customer relationship records](https://www.servicenow.com/docs/access?context=adding-related-party-to-case&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Use the Type field through related party configurations to name records in the account team member, contact relationship, consumer relationship, and household member relationship tables. With this functionality, you can identify the relationship that is based on the industry use case.

-   **[Ordering customer relationship records](https://www.servicenow.com/docs/access?context=adding-related-party-to-case&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Organize records in tables such as account team members, consumer relationships, and more by using the **Order** field. You can set the order manually or auto-populate it based on the selected Type through related party configurations. This way, you can arrange records logically based on your use case.

-   **[Enhancements to the declarative responsibility framework](https://www.servicenow.com/docs/access?context=declarative-resposibility-framework&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Enhance the declarative responsibility framework to simplify administration and access management by enabling administrators to do the following tasks:

    -   Add new granular roles for accessing customer data that is based on responsibility definitions.
    -   Include additional entities in the framework.
-   **[Subscription metrics for sold products](https://www.servicenow.com/docs/access?context=create-sold-item&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Enable agents to track and analyze the pricing information for products and services by using the pricing and subscription revenue metrics on the sold product form on the CSM Configurable Workspace.

-   **[Project Management for business locations​](https://www.servicenow.com/docs/access?context=csm-ppm-integration&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Integrate SPM project management with business locations to support operations such as opening, closing, or modernizing locations. With the project management integration, your teams can track the timelines, collaborate, and execute the business location-facing tasks more effectively.

-   **[Work orders for business locations​](https://www.servicenow.com/docs/access?context=track-work-orders-on-the-blsp&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Fulfill Field Service Management \(FSM\) work orders at business locations. This way, you can enable location members to view and complete the assigned tasks. By using the existing business location data, you can streamline work order assignments.

-   **[Enhanced data fields for business locations](https://www.servicenow.com/docs/access?context=data-model-business-location-form&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Track additional information about business locations by using new fields for opening and closing dates, status, and description.

-   **[Staff movement between internal business locations](https://www.servicenow.com/docs/access?context=create-internal-business-location&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Enable managers to transfer the staff between internal business locations. You can streamline updates for organizations that have frequent staff movements.

-   **[Company-owned, third-party operated business locations](https://www.servicenow.com/docs/access?context=add-user-internal-bus-location&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Assign external staff to internal business locations to support various operating models, including company-owned, third-party operated locations.

-   **[Customer Life Cycle workflows for Sold Products and Product Inventory records](https://www.servicenow.com/docs/access?context=customer-life-cycle-management-workflows&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Use the Customer Life Cycle workflows to do the following tasks:

    -   Create a Modify, Suspend, Resume, and Disconnect order for single or multiple root product inventory records that are associated with a service specification.
    -   Select multiple root product inventories to perform the modify action to create both orders and quotes.
    -   Track the status of the Modify, Suspend, Resume, and Disconnect flows on sold products and product inventory record by using the Sales and Order Management Request Tracker \(sn\_tmt\_core\_inbound\_queue\) table.
-   **[Inbound Request Configuration table](https://www.servicenow.com/docs/access?context=inbound-request-configuration-table&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Use the Inbound Request Configuration \[sn\_tmt\_core\_inbound\_queue\_config\] table to enable configurations that determine how a flow is executed, whether synchronous or asynchronous.

Use the **Trigger Notifications** field on the Inbound Request Configuration \[sn\_tmt\_core\_inbound\_queue\_config\] table to enable configuration of notification types, whether default, custom,or no notifications.

-   **[Activate Customer Life Cycle Management Self-Service](https://www.servicenow.com/docs/access?context=activate-customer-life-cycle-management-self-service&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Enable customers who are primary contacts associated to a sold product to perform the Modify, Suspend, Resume, and Disconnect actions on the Business portal.

.

-   **Billing account store application**

Use the new CSM Billing Account Core store app that provides a foundational data model for managing billing accounts across organizations and users. It enables businesses to define, organize, and maintain billing relationships, supporting accurate billing, payments, and scalable financial operations.


</td></tr><tr><td>

Decision Builder in Workflow Studio

</td><td>

-   **[Filter decision tables](https://www.servicenow.com/docs/access?context=filtering-overview&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

Apply filters to both condition and result column values in decision tables. Once filters are applied, only the relevant decisions are displayed, making it easier to refer or edit large tables.

-   **[Use enhanced reference record](https://www.servicenow.com/docs/access?context=using-enhanced-reference-record&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

When choosing a reference value as a condition or result, a new lookup icon enables you to select the reference record from the default list view. Additionally, you can preview the selected reference record by selecting the info icon.

-   **[Set rows active or inactive](https://www.servicenow.com/docs/access?context=set-active-inactive-rows&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

Turn the rows on or off. Activating a row includes its data while executing a decision table, while deactivating a row excludes it. This feature helps you to temporarily use or skip conditions without deleting them.


</td></tr><tr><td>

DevOps Change Velocity

</td><td>

-   **[Harness integration](https://www.servicenow.com/docs/access?context=harness-integration-with-devops-change-velocity&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Discover Harness pipelines and configure real-time notifications to enable change traceability and automation by integrating the Harness orchestration tool with DevOps Change Velocity.

-   **[DevOps Health instance scan](https://www.servicenow.com/docs/access?context=run-health-scan-check&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Detect anomalies and issues in the instance by running or scheduling health scans on your DevOps Change Velocity instance.

-   **[Bitbucket Cloud tool integration with ServiceNow](https://www.servicenow.com/docs/access?context=bitbucket-integration-dev-ops&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Integrate the Bitbucket Cloud coding tool with DevOps Change Velocity to connect, discover, import, and process real-time repository events in DevOps Change Velocity.

-   **[DevOps Change Workspace UI for simplified creation of custom tool integration with planning, coding and orchestration capabilities](https://www.servicenow.com/docs/access?context=create-a-tool-integration-from-the-devops-change-workspace&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Integrate a new custom tool across planning, coding and orchestration capabilities with basic know-how of ServiceNow using an intuitive DevOps Change Workspace UI. It offers easy navigation to the ServiceNow Platform for defining transformer or adapter rules, or integrate the ability to do so within the Workspace wherever applicable, and embeds necessary documentation links and tooltips to support self-service.

-   **[Import based evidence collection](https://www.servicenow.com/docs/access?context=import-based-evidence-collection-for-orchestration-capability&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Improve instance efficiency by skipping step-level pipeline processing for accelerated change management and evidence collection for GitHub Actions, Azure DevOps \(ADO\), GitLab and  Jenkins orchestration tools.


</td></tr><tr><td>

Digital End-User Experience

</td><td>

-   **[Manage your system compliance report](https://www.servicenow.com/docs/access?context=manage-compliance-report&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Identify vulnerabilities and keep end-user devices secure and efficient by confirming that they meet security policies and regulatory standards. The Compliance report provides a comprehensive view of how well the end-user devices are adhering to the security measures of your organization.

-   **[Monitor system performance](https://www.servicenow.com/docs/access?context=monitor-system-performance&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Identify high-performance devices by monitoring critical metrics, such as CPU usage, memory consumption, disk activity, and input/output \(IO\) reading and writing speeds. Monitoring system performance provides information about how device performance impacts overall system health.

-   **[Check your device's health](https://www.servicenow.com/docs/access?context=exploring-dex-self-service&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Digital End-user Experience Self-service \(DEX Self-service\) enables you to check the performance of your device using a Device health check. You can check the device health on demand and resolve the issues detected by DEX by leveraging the recommended resolutions for the issues. The resolutions can either be remedial actions \(that you can trigger via a button\), self-help instructions, or URL. You can also use Device actions which can be triggered even when no issues are detected on the device.  These actions enable you to maintain good performance of the devices and applications

-   **[Monitor your user apps network](https://www.servicenow.com/docs/access?context=monitor-user-apps-network&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Monitor the advanced metrics like jitter, latency, and packet loss with a visual representation of network hops. These metrics provide real-time insights into network performance, helping to identify bottlenecks and areas for optimization quickly.

-   **[Additional device metrics](https://www.servicenow.com/docs/access?context=user-device-details-pages&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Get insights into device health and performance using the newly added device-level and application metrics. These metrics include memory usage, system time, energy consumption, and page file size. They're available in the following pages under Device health or Advanced app metrics:

    -   Operating system
    -   System compliance metrics
    -   Windows power plan
    -   File management
    -   Windows registry
    -   Microsoft Configuration Manager \(MCM\) application
    -   Application freeze
-   **[Digital Experience Score​](https://www.servicenow.com/docs/access?context=dexscr-digital-experience-score&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Measure and consolidate both quantitative and qualitative data to gain a holistic view of the digital employee experience. The Digital Experience Score​ dashboard \(DEX Score\) provides data-driven insights to improve your employees' digital experience.

DEX Score compiles health metrics scores, user sentiment scores, and service experience scores for applications and devices to calculate the overall digital experience score.

Access device lists based on individual device or application health metric scores. Review the list to identify devices with scores below the average for each metric.

-   **[Proactive Engagement](https://www.servicenow.com/docs/access?context=proactive-engagement-landing-page&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Inform employees by providing any self-help instructions or notifications by Desktop Assistant and email as the two new notification channels along with the existing Virtual Agent option.

Explore what Proactive Engagement has to offer with new use cases as part of the base system. The new use cases include poor Wi-Fi connectivity, device crash, app crash, app freeze, Jamf execution, and disconnected Zscaler.

User criteria help in grouping the users based on certain conditions. You can set the user criteria settings through Proactive Engagement.

Depending on the remedial action chosen from the list while creating a new metric rule, specific input parameters can be configured with advanced settings that will fetch a static input.


</td></tr><tr><td>

Digital Portfolio Management

</td><td>

-   **[Use the Admin Center in Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-admin-center&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Use the added Troubleshoot tab on the DPM Admin Center landing page to help you recalculate availability results and indicators for service offerings. You select a specific time period for the recalculation and then you can check the progress in the event log.

-   **[Configure personal portfolio solution cards in the DPM Admin Center](https://www.servicenow.com/docs/access?context=dpm-configure-solution-cards&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Configure the fields that are displayed on the personal portfolio solution cards in the DPM Workspace. Solution cards display information about the four main types of solutions \(service, service offering, business application, and application service\). This configuration determines the fields that are displayed on each solution card.

-   **[View relationships of business applications and application services in the DPM Admin Center](https://www.servicenow.com/docs/access?context=dpm-view-related-records&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

See all incidents, problems, and changes that are related to your business applications and application services. You can view the data in these areas:

    -   The DPM Admin Center
    -   In the DPM Workspace, in the Needs attention panels and in the life-cycle tabs that present key performance indicator \(KPI\) data.
-   **[KPI groups in Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-configure-kpi&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Added the ability to select the spark lines \(time series chart\) for a KPI indicator to open its details.

-   **[Update KPIs in Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-kpi-descriptions&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Added an Active flag so that you can hide KPIs in a KPI group from the DPM Workspace. The Active flag is available for all KPIs so that you can hide an individual KPI even when it's part of a larger KPI group.

-   **[View application service details](https://www.servicenow.com/docs/access?context=dpm-app-service-details&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Expanded the DPM data model so that when an incident, problem, or change is in the application service's Impacted services or Affected CIs related list, the updates roll up to the related business application. You can see the impacts in the related business application's KPIs and Needs attention panels\). For more information, see [Work with Needs attention panels in Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-needs-attn-panels&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

-   **[Work with lists in Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-list-modules&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Use the updated logic in the list address bar to copy the link of any list item to share that list with others. The list address includes a unique list ID for every list item. This updated logic applies wherever lists are used in the DPM Workspace:

    -   In the list module \(for both provided lists and created lists\).
    -   In the DPM Admin Center.

</td></tr><tr><td>

Document Intelligence

</td><td>

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


-   **[Document and visual insights AI agent](https://www.servicenow.com/docs/access?context=document-and-visual-insights-ai-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Use an AI agent to help process tasks that analyze and extract data from documents and images.


-   **[Now Assist in Document Intelligence](https://www.servicenow.com/docs/access?context=docintel-nowassist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Use Now Assist in Document Intelligence to extract information from documents and provide answers to defined questions using generative AI.


</td></tr><tr><td>

Domain Separation

</td><td>

-   **[Post-Production Domain Separation Activation Utility](https://www.servicenow.com/docs/access?context=post-prod-domain-sep-utility&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

Begin using domain separation on a live environment with the guided Post-Production Domain Separation Activation Utility.


</td></tr><tr><td>

Dynamic Translation

</td><td>

-   **[Exclusion Framework in Dynamic Translation](https://www.servicenow.com/docs/access?context=dyn-translation-exclusion-framework&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Preserve text such as product names or technical terms during machine translation. With Exclusion Framework, you can specify words and patterns that shouldn't be translated.

-   **[The APIs used by default Translator Configurations are upgraded to v4](https://www.servicenow.com/docs/access?context=migrate-v3-dynamic-translation&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

The APIs used by default translator configurations are automatically upgraded to v4. If you want to use v4 APIs with customized translator configurations, you must migrate them manually. The previous v3 is still supported.


</td></tr><tr><td>

ERP Semantic Mining

</td><td>

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   **[Reset AI/ML analysis to control the ML training](https://www.servicenow.com/docs/access?context=erpcm-check-data-connection&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Use **Reset AI/ML analysis** option to clear the AI/ML analysis so the flow can run again.


</td></tr><tr><td>

Employee Center

</td><td>

-   **[Favoriting topic pages](https://www.servicenow.com/docs/access?context=app-launcher-usability&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Enable one-click access for employees to their most frequently accessed topics through topic pages added to the Favorites widget.

-   **[Single-click taxonomy sync](https://www.servicenow.com/docs/access?context=config-adv-portal-nav-as-menu&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Sync taxonomy updates across Advanced Portal Navigation hierarchy levels with one click.

-   **[Guided Self-Service enhancements](https://www.servicenow.com/docs/access?context=gss-guided-self-service-overview&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**
    -   Admins can provide more detailed answers or guidance to a Guided Self-Service response by adding rich media, including images and videos and formatted text.
    -   Employees can review and edit their previous responses.
    -   Employees can search for and discover Guided Self-Service processes using AI-powered search.
-   **[Enhanced apps discovery and visibility preferences \(Employee Center Pro\)](https://www.servicenow.com/docs/access?context=applauncher-enable-availability&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Employees can search for authorized work applications using the AI-powered global search bar.

-   **[Appointment booking with HR representative \(Employee Center Pro\)](https://www.servicenow.com/docs/access?context=appointment-booking&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Employees can schedule in-person or virtual appointments to get help through a quick link in the Mega Menu or Quick links widget.

-   **[Rich Content Editor updates \(Employee Center Pro\)](https://www.servicenow.com/docs/access?context=ec-rich-content&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Build more visually engaging content in microsites and news through additional formatting elements including bulleted and numbered lists, table or grid layouts, and accordion lists.

-   **[Portal shortcuts for content authoring \(Employee Center Pro\)](https://www.servicenow.com/docs/access?context=ec-create-content-widgets&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Content authors can now easily edit or create news articles and banners using shortcuts in the Content Experiences or News widgets. The system auto-generates publishing plans, streamlining content delivery to the selected widget and reducing the effort needed for configuration.

-   **[Integrated experience and service feedback](https://www.servicenow.com/docs/access?context=ex-fdback-ovrvw&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) \(Employee Center Pro\)**
    -   Set a rating threshold that automatically generates a feedback task.
    -   Receive feedback tasks from negative feedback submitted through Now Mobile®.
    -   Receive automated email notifications when feedback tasks are completed.
    -   Track your feedback responses through the Feedback Analytics dashboard for portal, email, Virtual Agent, kiosks, and Now Mobile®.
-   **[Live company events hosting and communications framework \(Employee Center Pro\)](https://www.servicenow.com/docs/access?context=ec-company-events&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Live company events can now be hosted directly in the Employee Center Pro portal, with prebuilt configurations to streamline the pre-event communications and handle traffic surges. Content authors can easily create and share event content using the drag-and-drop Rich Content Editor, combined with mass-publishing capabilities similar to news articles.

-   **Improved topic search ranking**

The Topic content search widget now ranks topics based on user clicks, improving the relevance of search results and making it easier for employees to find their frequently used topics.

-   **[Quick start tests for Employee Center](https://www.servicenow.com/docs/access?context=quick-start-tests-employee-center&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Employee Center works as expected. If you customized Employee Center, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Encryption Key Management

</td><td>

-   **[Column Level Encryption is now Field Encryption](https://www.servicenow.com/docs/access?context=column-level-encryption-landing&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

Column Level Encryption has been rebranded to Field Encryption Starter \(FES\), while Column Level Encryption Enterprise is now Field Encryption Enterprise \(FEE\).

-   **[Access observer](https://www.servicenow.com/docs/access?context=access-observer&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

Use access observer to understand the people and processes that access data on your instance.

-   **[Improved migration process from Edge Encryption to Field Encryption](https://www.servicenow.com/docs/access?context=column-level-encryption-landing&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

Use the new process for migration from Edge Encryption to Field Encryption \(formerly Column Level Encryption\). This improved workflow ensures that your data migrates from Edge Encryption to Field encryption without spending time in an unencrypted state.


</td></tr><tr><td>

Enterprise Architecture \(formerly Application Portfolio Management\)

</td><td>

-   **Yokohama Patch 6 [Application rationalization page enhancements](https://www.servicenow.com/docs/access?context=eaw-rationalize-business-applications&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
    -   Apply the fiscal period filter to filter and view business applications for a specific fiscal period.
    -   Apply the application rationalization filters to filter and view specific business applications on the bubble chart or list view page. An indicator is displayed on top of the filter icon to show the number of filters currently applied.
    -   View the business application technical debt indicator score on the application rationalization list view page. On the application rationalization bubble chart view page, you can use the TRM technical debt indicator to form the bubble size based on the indicator score.
    -   Export the list view of application rationalization data to Excel or CSV file format. You can use the data to obtain insights, share with stakeholders, and prepare for analysis.
    -   Business applications with Retired or End of Life lifecycle stage aren’t displayed on the Application Rationalization bubble chart page.
-   **[Enterprise Modeling and Visualization in the EA Workspace](https://www.servicenow.com/docs/access?context=eaw-modeling&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
    -   Create diagrams for business process maps using the specific shapes related to the business processes.
    -   Search shapes within the shape libraries.
    -   Reorganize the order of shapes in a shape library according to your requirement.
    -   Show or hide shapes in different diagram types.
    -   General shapes can be rotated.
    -   Enhanced the overall appearance of the diagram by hiding the connector ports and displaying them only when hovering over the shapes.
    -   Open the Enterprise Modeling and Visualization diagrams from the following sections:
        -   From the Architectural Artifacts related list of a business application, business capability, or a business process record.
        -   From the My approvals tab of the Needs Attention section on the EA Workspace home page.
        -   From the Architectural Artifacts section of the Portfolio page.
    -   Added support for all ArchiMate shapes.
    -   Model Value stream diagrams.
    -   Create diagram actions for newly added custom shapes that can be used in Enterprise Modeling and Visualization to create diagrams.
    -   Add custom shapes to use in the Enterprise Modeling and Visualization.
    -   Create your own modeling diagrams using the Blank diagram option.
-   **[Business application related list enhancements](https://www.servicenow.com/docs/access?context=eaw-app-portfolio&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

In the **Architectural Artifacts** tab of the business application related list, selecting the **New** button displays a modal to create an architectural artifact.

-   **[Architectural Decision Records \(ADR\) enhancements](https://www.servicenow.com/docs/access?context=eaw-managing-arch-decision-records&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
    -   Create artifact type Architectural Decision Records \(ADR\) in one step.
    -   Create and add multiple pages to the Architectural Decision Records \(ADR\) from the Artifact content tab.
    -   In the Architectural Decision Records \(ADR\) page, you can tag the following:
        -   Tag a user
        -   Tag a record
            -   Architectural artifact
            -   Business application
            -   Business capability
            -   Business process
            -   Digital integration \(requires the digital integration plugin\)
            -   Digital interface \(requires the digital integration plugin\)
            -   Information object
            -   TRM product \(requires the TRM plugin\)
            -   Value stream \(requires the value stream plugin\)
    -   Request approval workflow for Architectural Decision Records \(ADR\).
    -   The version drop-down list is added to the Architectural Decision Records \(ADR\) page header. Select a version from the drop-down list to open the specific ADR version.
-   **[Data Certification changes](https://www.servicenow.com/docs/access?context=eaw-config-cert-schedules&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

In the Enterprise Architecture Workspace, the certifications data is saved to and fetched from the CMDB Data Management Task Control \(cmdb\_data\_management\_task\) table.

If your certification data is still fetched from the Certification Schedules \(cert\_schedule\) table, you might consider migrating your certification policies to the CMDB Data Management Task Control \(cmdb\_data\_management\_task\) table. For more information, see [Convert legacy certification schedules into Data Manager Certification policies](https://www.servicenow.com/docs/bundle/yokohama-servicenow-platform/page/product/configuration-management/task/convert-data-cert-definitions.html)and[Publish a draft Data Manager policy in CMDB Workspace](https://www.servicenow.com/docs/bundle/yokohama-servicenow-platform/page/product/configuration-management/task/data-manager-publish-draft-policy.html%22%20HYPERLINK%20%22https:/www.servicenow.com/docs/bundle/yokohama-servicenow-platform/page/product/configuration-management/task/data-manager-publish-draft-policy.html)

-   **[Regenerate indicator scores in Enterprise Architecture Workspace](https://www.servicenow.com/docs/access?context=eaw-regenerate-indicator-score&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

Generate a score for application and capability indicators for a particular period. Also, generate scores for an application scoring profile and capability scoring profile, to calculate scores for all indicators attached to that particular scoring profile.

-   **[Business stakeholder role for Enterprise Architecture Workspace](https://www.servicenow.com/docs/access?context=eaw-business-stakeholder-role&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

Read-only access to the  Enterprise Architecture Workspace is added to the business stakeholder role \(sn\_apm.apm\_read\).

-   **[TRM technical debt form](https://www.servicenow.com/docs/access?context=eaw-trm-technical-debt-form&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

The **TPM Discovered Technologies and Lifecycles** scheduled job fetches the server details for the TRM products.

-   **[Technology portfolio management \(TPM\) enhancements](https://www.servicenow.com/docs/access?context=eaw-tpm&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
    -   Added a restart button on the TPM Logs page to restart the Populate TPM Discovered Technologies and Lifecycles scheduled job, in case the job is stuck and doesn’t refresh the log data for more than an hour. For more information, see [View TPM logs](https://www.servicenow.com/docs/access?context=eaw-view-tpm-logs&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US) and [Restart Populate TPM Discovered Technologies and Lifecycles scheduled job](https://www.servicenow.com/docs/access?context=eaw-restart-tpm-scheduled-job&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US).

</td></tr><tr><td>

Enterprise Asset Management

</td><td>

-   **[Gain normalization coverage for firmware in your Operational Technology \(OT\) assets](https://www.servicenow.com/docs/access?context=normalizing-firmware-ot-assets&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Achieve enhanced normalization across your OT deployments by normalizing the firmware that is embedded into your OT assets. Use the normalized data to track and manage the life cycles of your firmware separately from your OT assets so that you can directly detect and mitigate firmware vulnerabilities. You can view the firmware model details in the OT model management view of the OT Asset Workspace.

**Note:** Firmware normalization is applicable only to OT Asset Management.

-   **[Manage hardware models and assets in the Operational Technology \(OT\) Asset Management application](https://www.servicenow.com/docs/access?context=ot-asset-ws-otam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Enable your OT managers to create hardware models and assets in the OT Workspace. You can integrate hardware models and OT assets into such Enterprise Asset Management flows as asset request, asset refresh, stock order, multi-asset onboarding, Return Merchandise Authorization \(RMA\), repair, and disposal. You can also generate maintenance plans and work orders for your OT hardware assets.

-   **[Synchronize asset and CIs for Operational Technology \(OT\) assets](https://www.servicenow.com/docs/access?context=asset-ci-sync-ot-assets&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Synchronize the MAC addresses between the asset and network adapter CI for OT assets.

-   **[License your OT hardware assets using the new resource categories available in OTAM licensing](https://www.servicenow.com/docs/access?context=licensing-ot-asset-management&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Access OT Asset Management features and workflows for OT hardware assets through the following hardware resource categories:

    -   OT Servers
    -   OT Network Gear
    -   OT Storage
    -   OT End User Computers
    -   OT Mobile Devices
    -   OT Monitors
    -   OT Printers
    -   OT Unclassified Hardware
The hardware resource categories are opted in by default. The OT hardware assets are counted only under OTAM licensing. They are excluded from the HAM licensing that is based on the OT entity flag.

**Note:** The OTAM licensing changes apply only to OT Asset Management.

-   **[Manage mission-critical enterprise assets and linear assets for telecommunications networks](https://www.servicenow.com/docs/access?context=eam-dcnam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Use the Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\) application to track and manage mission-critical facility-based enterprise assets and linear assets for telecommunications networks. Get a comprehensive view of these assets throughout their life cycles so that you can help optimize their performance and improve their longevity.

-   **[Fulfill Return Merchandise Authorization \(RMA\) requests as a Device as a Service \(DaaS\) provider, vendor, or manufacturer](https://www.servicenow.com/docs/access?context=eam-providers&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Use the Enterprise Asset Management for Providers application to fulfill the RMA requests that you receive from customers as a DaaS provider, vendor, or manufacturer. The application adds support for RMA response orders, which enable you to track and manage the process of repairing or replacing defective assets for your RMA requests. The application also adds support for inbound asset orders, which enable you to track and manage the process of providing assets for your RMA requests. By managing these orders from a consolidated location, you can streamline your operations and improve efficiency.


</td></tr><tr><td>

Event Management

</td><td>

-   **[Group alerts using network traffic-based grouping](https://www.servicenow.com/docs/access?context=network-traffic-correlation-grouping&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Group alerts efficiently with network traffic-based alert grouping, which uses discovered TCP connections with ML Service Mapping to correlate alerts on host CIs that have network traffic connections between them.

-   **[View links between alerts in network traffic-based alert groups](https://www.servicenow.com/docs/access?context=el-network-traffic-based-link-view&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Once a network traffic correlation is enabled, investigate network traffic alert group details and visualize connections through Link View in Express List®.

-   **[New role for team level operators](https://www.servicenow.com/docs/access?context=r_InstalledWithEventManagement&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Enhance team-level control over alert management with the evt\_team\_operator role. This role enables operators to manage Event Management operations within their assigned team, including reading and writing alerts, making configuration changes,updating Alert Automation, and setting up new integrations in the Integrations Launchpad.

-   ****

Starting in version 26.7.0, execute response subflows automatically, manually, or both for alerts that match specific conditions through the Run Other Response Actions option of Respond Automatic. This enhancement offers better control over automated responses with configurable execution limits and multiple response actions.

-   ****

Starting in version 26.7.0, link a CI to an alert for more accurate IT component mapping though the Improve Configuration Item \(CI identification option of Enrich Automation. This enhancement improves alert visibility, speeds up issue resolution, and ensures better correlation between alerts and infrastructure components.


</td></tr><tr><td>

External Content Connectors

</td><td>

-   **[Connector admin role](https://www.servicenow.com/docs/access?context=installed-with-ext-content-connectors&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Users with the sn\_ext\_conn.xcc\_admin role can create, configure, and review details for external content connectors and crawls.

-   **[Adobe Experience Manager as a Cloud Service external content connector](https://www.servicenow.com/docs/access?context=adobe-expmgr-cs-external-content-connector&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Adobe Experience Manager as a Cloud Service source system.

-   **[Asana external content connector](https://www.servicenow.com/docs/access?context=asana-external-content-connector&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Asana source system.

-   **[Docusign external content connector](https://www.servicenow.com/docs/access?context=docusign-external-content-connector&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Docusign source system.

-   **[Dropbox external content connector](https://www.servicenow.com/docs/access?context=dropbox-external-content-connector&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Dropbox source system.

-   **[GitHub Enterprise Cloud external content connector](https://www.servicenow.com/docs/access?context=github-enterprise-cloud-external-content-connector&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your GitHub Enterprise Cloud source system.

-   **[HubSpot external content connector](https://www.servicenow.com/docs/access?context=hubspot-external-content-connector&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your HubSpot source system.

-   **[Lucidchart external content connector](https://www.servicenow.com/docs/access?context=lucidchart-external-content-connector&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Lucidchart source system.

-   **[Miro external content connector](https://www.servicenow.com/docs/access?context=miro-external-content-connector&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Miro source system.

-   **[monday.com external content connector](https://www.servicenow.com/docs/access?context=monday-com-external-content-connector&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your monday.com source system.

-   **[Notion external content connector](https://www.servicenow.com/docs/access?context=notion-external-content-connector&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Notion source system.

-   **[SAP DMS external content connector](https://www.servicenow.com/docs/access?context=sap-dms-external-content-connector&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your SAP DMS source system.

-   **[Smartsheet external content connector](https://www.servicenow.com/docs/access?context=smartsheet-external-content-connector&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Smartsheet source system.

-   **[Trello external content connector](https://www.servicenow.com/docs/access?context=trello-external-content-connector&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Trello source system.

-   **[WordPress external content connector](https://www.servicenow.com/docs/access?context=wordpress-external-content-connector&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your WordPress source system.

-   **[Workday external content connector](https://www.servicenow.com/docs/access?context=workday-external-content-connector&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Workday source system.

-   **[Zoom external content connector](https://www.servicenow.com/docs/access?context=zoom-external-content-connector&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Zoom source system.

-   **[Configure user permission settings for an external content connector](https://www.servicenow.com/docs/access?context=configure-user-mapping-settings-external-content-connector&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Specify the source system and User \[sys\_user\] table fields to examine for matches when an external content connector maps source system users to your ServiceNow AI Platform users.

-   **[Statistics for external content connector content crawls](https://www.servicenow.com/docs/access?context=document-statistics-external-content-connectors&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Review statistics about the documents \(items or files with searchable content and metadata\) retrieved by a content crawl.

-   **[Statistics for external content connector user permission crawls](https://www.servicenow.com/docs/access?context=permission-statistics-external-content-connectors&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Review statistics about the permissions \(user and group-membership security principals\) retrieved by a user permission crawl.

-   **[Analytics for external content connectors](https://www.servicenow.com/docs/access?context=analytics-external-content-connectors&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Review metrics that show how your external content connector has run over time.


-   **[Amazon S3 external content connector](https://www.servicenow.com/docs/access?context=amazon-s3-external-content-connector&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from buckets in your Amazon S3 source system.

-   **[Box external content connector](https://www.servicenow.com/docs/access?context=box-external-content-connector&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from user boxes in your Box source system.

-   **[GitLab external content connector](https://www.servicenow.com/docs/access?context=gitlab-external-content-connector&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from issues, wikis, merge requests, tags, branches, and commits in your GitLab source system's groups, projects, and repositories.

-   **[Microsoft OneDrive external content connector](https://www.servicenow.com/docs/access?context=microsoft-onedrive-external-content-connector&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from individual drives in your Microsoft OneDrive source system.

-   **[Microsoft Viva Engage external content connector](https://www.servicenow.com/docs/access?context=microsoft-viva-engage-external-content-connector&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from conversations in your Microsoft Viva Engage source system's communities.

-   **[ServiceNow® instance external content connector](https://www.servicenow.com/docs/access?context=servicenow-instance-external-content-connector&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from KB articles in your ServiceNow AI Platform instance.

-   **[Webcrawler external content connector](https://www.servicenow.com/docs/access?context=webcrawler-external-content-connector&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from pages and subdomains in public web sources. Select a predefined web source or specify a custom web source.

-   **[Zendesk Guide external content connector](https://www.servicenow.com/docs/access?context=zendesk-guide-external-content-connector&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from articles in your Zendesk Guide source system's knowledge bases.

-   **[Statistics for external content connector content crawls](https://www.servicenow.com/docs/access?context=document-statistics-external-content-connectors&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Review statistics for searchable items retrieved by a content crawl.

-   **[Statistics for external content connector user permission crawls](https://www.servicenow.com/docs/access?context=permission-statistics-external-content-connectors&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Review statistics for user and group permissions retrieved by a user permission crawl.


-   **[Atlassian Jira Cloud external content connector](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-jira&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and user permissions from projects in your Atlassian Jira Cloud source system.

-   **[Google Drive external content connector](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-gdrive&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and user permissions from shared drives in your Google Drive source system.

-   **[Microsoft Teams external content connector](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-msteams&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and user permissions from teams in your Microsoft Teams source system.

-   **[ServiceNow product documentation external content connectors](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-snowdoc&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content from the ServiceNow product documentation site.

-   **[Slack external content connector](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-slack&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Retrieve searchable content and user permissions from public channels in your Slack source system.

-   **[Warning messages for indexed document counts](https://www.servicenow.com/docs/access?context=exploring-ext-cont-connectors&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

When an external content connector's indexed document count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit of 1,000,000 documents.

-   **[Add external content search results to Now Assist in Virtual Agent conversations](https://www.servicenow.com/docs/access?context=add-ext-cont-srch-src-na-va&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Expand the range of information available to Virtual Agent users by adding external content search results to Now Assist in Virtual Agent conversations.


-   **[Semantic vector indexing for crawled content](https://www.servicenow.com/docs/access?context=semantic-search-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Improve recall for external content searches with support for semantic vector indexing of crawled content. Semantic vector indexing is supported for all external content connectors.


</td></tr><tr><td>

Field Service Management

</td><td>

-   **[Dispatcher Workspace](https://www.servicenow.com/docs/access?context=using-dispatcher-workspace&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

Use Dispatcher Workspace to perform the following tasks:

    -   View the Field Service agent’s real-time location and completed daily route.
    -   Use a condition builder to filter relevant resources. You can also extend existing tables to filter custom fields.
    -   Use advanced filters with hierarchical structures to filter territories.
    -   View task scheduling conflict messages in the Dispatcher Workspace to improve visibility and facilitate resolutions for dispatchers.
-   **[Field Service Agent Efficiency](https://www.servicenow.com/docs/access?context=configuring-agent-efficiency&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

Use Agent Efficiency to perform the following tasks:

    -   Define the agent efficiency criteria to calculate the Agent Efficiency for a task.
    -   Calculate the estimated work duration for a work order task more accurately based on the Agent Efficiency feature.
    -   Enhance manual task assignment and dynamic scheduling for a task by leveraging Agent Efficiency.
    -   Optimize Intelligent Task Recommendation by incorporating Agent Efficiency values so that dispatchers can assign tasks more effectively.
-   **[Appointment Booking](https://www.servicenow.com/docs/access?context=appointment-booking-administer&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

Use Appointment Booking to perform the following tasks:

    -   Replicate the application and service-based configurations across instances.
    -   Grade the appointment booking slots by recommended or available slots to ensure optimal scheduling.
    -   Use the seismic appointment booking calendar across all user interfaces to ensure a consistent and seamless scheduling experience.
-   **[Task dependencies](https://www.servicenow.com/docs/access?context=t_SetAnUpstreamTask&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

Use task dependencies to perform the following tasks:

    -   Enable administrators and dispatchers to define advanced task dependencies, such as start together or start after start, so that you can ensure that tasks are executed in the right order.
    -   Enable dispatchers to create task dependencies within or between work orders.
-   **[Schedule Optimization](https://www.servicenow.com/docs/access?context=schedule-optimization-engine&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

Use Schedule Optimization to perform the following tasks:

    -   Enable dispatchers to optimize resource assignments that are based on the dependency relationship between tasks.
    -   Generate more accurate scheduling and assist your field technicians in navigating traffic conditions more effectively by configuring Schedule Optimization. You can consider time-of-day and set up intraday scheduling to leverage real-time traffic data when certain conditions are met.
    -   Use new optimization features, such as **Maximize consecutive collocated task assignments** and **Minimize task start times**, when you're creating a policy.
    -   Provide greater control over task distribution by enabling a new drip feed property, **Number of tasks**, to enhance your scheduling capabilities.
    -   Expect more reliable and efficient task scheduling due to resolved conflicts between the various scheduling engines.
    -   View the task scheduling conflict messages on the task, user, and group records when optimization is in progress.
-   **[Capacity and Reservations Management](https://www.servicenow.com/docs/access?context=capacity-management&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

Use Capacity and Reservations Management to perform the following tasks:

    -   Leverage the capacity console to efficiently manage resource allocation across territories and demand channels so that you can enable your teams to analyze field technician performance and make data-driven decisions.
    -   Set flexible reservation rules to define the minimum and maximum resource allocations so that you can enable dynamic adjustments to capacity based on shifting demands.
    -   Create recurring capacity assignments for specific days of the week for long-term capacity planning and management.
    -   Enable multiple overrides for the same date range to address demand fluctuations so that you can manage exceptions with more precision and flexibility.
-   **[Scheduling Health dashboard](https://www.servicenow.com/docs/access?context=scheduling-health-dashboard&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

Use the Scheduling Health dashboard to view these additional Schedule Optimization metrics:

    -   Tasks without skills
    -   Technicians without skills
    -   Tasks without parts
    -   Technicians without parts
-   **[Business location-based work management](https://www.servicenow.com/docs/access?context=industry-products-integration&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

Enable your staff across various industries to efficiently manage work orders. Your employees can resolve tasks that are specific to their assigned location, while your managers can oversee the tasks across their assigned locations. You can reinforce your security by ensuring that your staff can only access the work orders that are related to their designated locations.

-   **[Managing agents and tasks from Workforce](https://www.servicenow.com/docs/access?context=using-manager-workforce&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

Use Workforce to perform the following tasks:

    -   Enable additional users to use Workforce by adding additional managers to assignment groups.
    -   Enable managers to view the event management tab when Workforce Optimization for Field Service is active.
-   **[Smart Assessment for Field Service Questionnaire](https://www.servicenow.com/docs/access?context=configuring-smart-assessment-questionnaire&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

Use Smart Assessment templates to perform the following tasks:

    -   Migrate from a survey-based questionnaire to Smart Assessment based questionnaires.
    -   Create work order questionnaires.
    -   Set up detailed instructions that include rich text and images.
    -   Configure conditional questions based on responses of all other types of questions and across sections.
    -   Allow additional comments or attachments on a question's response.
    -   Improve the work order questionnaire in the Mobile Agent® application by implementing a paginated layout, providing instructions with questions, and offering in-line choices.
-   **Planned Work Management**

Seamlessly migrate monthly and annual plans from Planned Maintenance to Planned Work Management.


</td></tr><tr><td>

Financial Services Card Operations

</td><td>

-   **[Detect friendly fraud](https://www.servicenow.com/docs/access?context=resolve-friendly-fraud&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US)**

Resolve friendly fraud disputes with predefined rules to ensure consistent and precise detection of friendly fraud in Visa disputed transactions. Agents can decline requests, issue credits, or proceed with chargebacks, allowing for tailored responses based on the situation.

-   **[Enhanced Visa disputes playbook](https://www.servicenow.com/docs/access?context=managing-card-disputes&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US)**

Leverage an updated card disputes processing flow to associate additional transactions, manage multiple transaction disputes, and handle pre-arbitration, arbitration, and appeal requests to Visa for allocation and collaboration chargeback workflows.


</td></tr><tr><td>

Financial Services Operations Integration with Visa

</td><td>

-   **[Added new VROL integration subflows](https://www.servicenow.com/docs/access?context=components-installed-with-the-financial-services-operations-integration-with-visa&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US)**

Enables seamless integration with the card operations dispute management playbook with VROL subflows. The following new VROL subflows have been added:

    -   Look Up Transaction Inquiry Results
    -   Accept Dispute
    -   Conduct Cardholder Purchase Inquiry
    -   Look Up Transaction Details
    -   Look Up Dispute Response Details
    -   Create Dispute Pre-Arbitration
    -   Look Up Dispute Pre-Arbitration Details
    -   Create Dispute Pre-Arbitration Response
    -   Look Up Dispute Pre-Arbitration Response Details
    -   Submit Dispute Filing
    -   Look Up Dispute Filing Details
    -   Mark Batch Queue Item as Read

</td></tr><tr><td>

Flows, subflows, and actions in Workflow Studio

</td><td>

-   **[Add and edit flows in Now Assist for app generation](https://www.servicenow.com/docs/access?context=sns-app-gen-add-flow&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Create a flow when creating an application in Now Assist for app generation. Enhance an existing application by adding a flow.

-   **[Call a Now Assist skill from an action](https://www.servicenow.com/docs/access?context=call-now-assist-skill-step&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

Run a published Now Assist skill from an action. Configure the Now Assist skill inputs and skill outputs from the step inputs and step outputs.

-   **[Check for conversational compatible actions](https://www.servicenow.com/docs/access?context=check-for-conversational-compatible-actions&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

Run a compatibility check on new or all actions to determine if they are conversational compatible. Review the inputs of an action to determine if their data types are compatible.

-   **[Check for conversational compatible subflows](https://www.servicenow.com/docs/access?context=check-for-conversational-compatible-subflows&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

Run a compatibility check on new or all subflows to determine if they are conversation compatible. Review the inputs of a subflow to determine if their data types are compatible.

-   **Create a flow or subflow from an image**

Create a flow or a subflow from an image by using Now Assist. Capture the detailed process in an image and attach the image to Workflow Studio. Now Assist generates a preview of the flow that you can modify and regenerate.

-   **[Display text descriptions of the data used by actions and flow logic](https://www.servicenow.com/docs/access?context=exploring-flows&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

See a natural language description of the data each component of a flow uses. Understand what data flow triggers, actions, and flow logic blocks use without having to open their configuration details.

-   **[Generate skill and input descriptions for conversational actions](https://www.servicenow.com/docs/access?context=configure-action-conversation-settings&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

Configure conversational settings for conversational actions by generating skill and input descriptions with generative AI.

-   **[Generate skill and input descriptions for conversational subflows](https://www.servicenow.com/docs/access?context=configure-subflow-conversation-settings&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

Configure conversational settings for conversational subflows by generating skill and input descriptions with generative AI.

-   **[Set default values for action inputs](https://www.servicenow.com/docs/access?context=configure-action-conversation-settings&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

Set a default value for a conversational action input. Hide action inputs that have a default value if you don't want users to change the input value in a conversation.

-   **[Set default values for subflow inputs](https://www.servicenow.com/docs/access?context=configure-subflow-conversation-settings&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

Set a default value for a conversational subflow input. Hide subflow inputs that have a default value if you don't want users to change the input value in a conversation.

-   **[Summarize a flow or subflow](https://www.servicenow.com/docs/access?context=flow-summarization&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

Summarize what a flow or subflow does by using generative AI.

-   **[Support additional input data types for conversational actions](https://www.servicenow.com/docs/access?context=conversational-actions&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

Support conversational actions that have Dynamic Choice and Array of Objects input types.

-   **[Support additional input data types for conversational subflows](https://www.servicenow.com/docs/access?context=conversational-subflows&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

Support conversational subflows that have Dynamic Choice and Array of Objects input types.

-   **[Create the recommended automation type](https://www.servicenow.com/docs/access?context=design-considerations-consolidated&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

Answer a few questions about your automation and Workflow Studio displays recommendations on whether you should create a playbook, flow, subflow, action, or a data stream.


-   **[Configure conversational settings](https://www.servicenow.com/docs/access?context=configure-subflow-conversation-settings&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

View the subflows and actions that are conversational compatible. Configure conversational settings to make a subflow or action available to conversational interfaces.


-   **[Debug flows and subflows](https://www.servicenow.com/docs/access?context=flow-debugger&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

Debug flows and subflows from a dedicated Workflow Studio tab. Set breakpoints and step through a paused flow to review configuration and runtime values.

-   **[Save a flow trigger for reuse in other flows](https://www.servicenow.com/docs/access?context=saved-flow-triggers&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

Save a set of trigger definitions as a reusable trigger. Enable flow authors to select the saved trigger from some or all application flows. Specify whether flow authors can see the trigger details or add conditions to the trigger.

-   **[Use the Flow API to send a message to a paused flow](https://www.servicenow.com/docs/access?context=ScriptableFlowAPI&version=yokohama&pubname=yokohama-api-reference&section=FlowAPI-sendMessage_S_S_S&ft:locale=en-US)**

Send a specific message and payload response to a flow that is paused and waiting for a message.

-   **[Wait for a specific message from the Flow API](https://www.servicenow.com/docs/access?context=wait-for-message-action&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

Pause a flow until it receives a specific message from the flow API. Specify the string message that resumes running the flow, and optionally provide a time out value to resume the flow if no message is received after a specific amount of time.


</td></tr><tr><td>

Generative AI Controller

</td><td>

-   **[Administrator access to Gen AI log](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Access the Gen AI log \[sys\_generative\_ai\_log\] table to gain insights for debugging purposes. Records related to HR remain restricted to HR admins.

-   **[Enhanced AI asset inventory](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Track the enhanced AI asset inventory through AI Control Tower using new metadata fields in the Model \[sys\_generative\_ai\_model\_config\] and Prompt \[sys\_generative\_ai\_config\] tables. Gain better visibility into AI asset status and life-cycle details, such as retirement dates.


-   **[AI Model Version Mappings](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Review the mappings between AI model versions, their providers in the Gen AI Model Version Mapping \[sys\_gen\_ai\_model\_version\_mapping\] table. It shows mapping between source and target models, along with associated metadata, such as skill type, model type, resource associations, and provider information.


-   **[Identify third-party LLM information](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Access the Gen AI Log Metadata \[sys\_gen\_ai\_log\_metadata\] table to identify which LLM model, version, and requested language was used to generate the AI content.

-   **[Restrict LLM usage based on the domain](../analytics-intelligence-reporting/generative-ai-controller-rn.md)**

Enable or disable Now Assist for each domain so that you can restrict the use of LLMs and avoid using AI for data processing, if needed.


-   **[Global Model selection for conversational skills](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Enable Now Assist Admins to choose between GPT4.o and Now Assist LLM model for data routing at a global level. This ensures compliance with any regional restrictions and helpful for APAC users who may face limitations with US-based models, such as GPT-4.0.


</td></tr><tr><td>

Hardware Asset Management

</td><td>

-   **[Maintain accurate asset details by creating Asset Attestations](https://www.servicenow.com/docs/access?context=asset-attestation-ham&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Validate whether assets are in use and confirm asset assignment by performing audits through Asset Attestation to verify through confirmation by employees whether they are still using assigned serialized hardware assets.

-   **[Hardware Model Normalization for Operational Technology \(OT\) assets](https://www.servicenow.com/docs/access?context=hardware-normalization&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

When the OT Asset Management application is installed, standardize your hardware and consumable models with a minimum of one OT asset in addition to the model categories that belong to the opted-in HAM resource categories through the Hardware Model Normalization process. The OT entity flag on the asset indicates whether it's an OT asset.


</td></tr><tr><td>

Health Log Analytics

</td><td>

-   **[Pull data from Splunk regularly using the Splunk Polling data input](https://www.servicenow.com/docs/access?context=hla-data-input-splunk-polling&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Make your data workflows more consistent and productive by fetching data consistently over time using the Splunk Polling data input, which sends recurring queries \(polls\) to Splunk. Handling most configurations on the HLA side means you need minimal additional stakeholder involvement, which enables swift integration with your existing Splunk setup. This enhancement accelerates proofs of concept \(POCs\) and enables faster iterations using real data.

-   **[Use your Splunk data input to ingest preprocessed data from Splunk](https://www.servicenow.com/docs/access?context=hla-data-input-splunk&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Ingest data from Splunk in a preprocessed, structured format using your existing Splunk data input.

-   **[Integrate with log data connectors from the Integrations Launchpad](https://www.servicenow.com/docs/access?context=hla-data-input-setup-integrations&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Take advantage of the Integrations Launchpad's unified interface for convenient integration with log data connectors that feed raw log data from external sources into your instance. You set up log data connectors for HLA from the Event Management Integrations Launchpad in Service Operations Workspace for ITOM. In this release, the Integrations Launchpad enables integration with the following connectors: Elasticsearch, ServiceNow System Logs, UDP, and TCP.

-   **[Use Cribl and Edge Delta data inputs to streamline HLA data ingestion with tools handling large log volumes](https://www.servicenow.com/docs/access?context=hla-data-input-setup-manual&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Use dedicated data inputs to facilitate data ingestion from Cribl or Edge Delta when using these tools to handle large volumes of log data from multiple sources before sending it to HLA.

-   **[Configure log data integrations from the Integrations Launchpad](https://www.servicenow.com/docs/access?context=hla-data-input-setup-integrations&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Starting in version 36.0.19, benefit from additional log data integrations for Splunk TCP/UDP, Splunk Poller, MID Server, Apache Kafka, Microsoft Azure Log Analytics, and REST API that can be easily set up through the Integrations Launchpad.

-   **[Set up an Amazon Data Firehose integration for real-time log data streaming from multiple sources](https://www.servicenow.com/docs/access?context=il-connector-hla-firehose&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Starting in version 36.0.19, leverage an integration for streaming log data from Amazon Data Firehose directly to the collector service in ITOM Gateway, where it is queued and then processed by Health Log Analytics. This integration doesn't run on a MID Server and can be configured from the Integrations Launchpad.


</td></tr><tr><td>

Healthcare Operations Core

</td><td>

-   **[Care Team Portal](https://www.servicenow.com/docs/access?context=hcls-cto-care-team-portal&version=yokohama&pubname=yokohama-healthcare-life-sciences&ft:locale=en-US)**

Create requests for supporting service departments and maintain visibility into all requests created by you or your team. This experience can be used on a standalone portal or embedded in EMR systems.

-   **[Healthcare Operations Case overview](https://www.servicenow.com/docs/access?context=hcls-cto-hco-case&version=yokohama&pubname=yokohama-healthcare-life-sciences&ft:locale=en-US)**

Create and customize cases for supporting service departments that can be used within the Care Team Portal.


-   **[Healthcare organization admin experience](https://www.servicenow.com/docs/access?context=hcls-cto-create-healthcare-organization&version=yokohama&pubname=yokohama-healthcare-life-sciences&ft:locale=en-US)**

Create healthcare organizations and hierarchies, add or edit members, and automatically create associated Service Model Foundation records \(internal business locations\).


</td></tr><tr><td>

Hermes Messaging Service

</td><td>

-   **[Topic audit history](https://www.servicenow.com/docs/access?context=view-messages-hermes-topic&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

Track changes made to a Hermes topic by viewing the topic's audit information.

-   **[Search for messages in a topic](https://www.servicenow.com/docs/access?context=view-messages-hermes-topic&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

Filter messages in a topic using keywords or regular expressions in the Hermes Messaging Service topic inspector.

-   **[Improved diagnostics](https://www.servicenow.com/docs/access?context=run-hermes-messaging-service-diagnostics&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

Monitor the health of Hermes components over time.


</td></tr><tr><td>

ITOM AIOps

</td><td>

-   **[Pull data from Splunk regularly using the Splunk Polling data input](https://www.servicenow.com/docs/access?context=hla-data-input-splunk-polling&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Fetch data consistently over time by using the Splunk Polling data input, which sends recurring queries \(polls\) to Splunk. Handling most configurations on the HLA side, you need minimal additional stakeholder involvement, enabling swift integration with your existing Splunk setup. This enhancement accelerates proofs of concept \(POCs\) and enables faster iterations using real data.

-   **[Use your Splunk data input to ingest pre-processed data from Splunk](https://www.servicenow.com/docs/access?context=hla-data-input-splunk&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Ingest data from Splunk in a preprocessed, structured format using your existing Splunk data input for streaming log messages to Health Log Analytics with a heavy forwarder.

-   **[Create Group automation](https://www.servicenow.com/docs/access?context=group-alert-sow-itom&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

View key details from the Test Automation section, including total alerts, alert groups, ungrouped alerts, and compression, to help track and optimize alert grouping efficiency. Simulate other group types, such as CMDB, ML, and text-based grouping. The simulation processes only alerts that match the condition filter.

-   **[Integrate with log data connectors from the Integrations Launchpad](https://www.servicenow.com/docs/access?context=hla-data-input-setup-integrations&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Set up your log data connectors for HLA from the Event Management Integrations Launchpad in Service Operations Workspace for ITOM. The Integrations Launchpad provides a unified interface for convenient integration with log data connectors that feed raw log data from external sources into your instance. In this release, the Integrations Launchpad enables integration with the following connectors: Elasticsearch, ServiceNow System Logs, UDP, and TCP.

Starting in version 36.0.19, benefit from additional log data integrations for Splunk TCP/UDP, Splunk Poller, MID Server, Apache Kafka, Microsoft Azure Log Analytics, and REST API that can be easily set up through the Integrations Launchpad.

-   **[Set up an Amazon Data Firehose integration for real-time log data streaming from multiple sources](https://www.servicenow.com/docs/access?context=il-connector-hla-firehose&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Starting in version 36.0.19, leverage an integration for streaming log data from Amazon Data Firehose directly to the collector service in ITOM Gateway, where it is queued and then processed by Health Log Analytics. This integration doesn't run on a MID Server and can be configured from the Integrations Launchpad.

-   **[View links between alerts in Network Traffic-based alert groups](https://www.servicenow.com/docs/access?context=el-network-traffic-based-link-view&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Once network traffic correlation is enabled, investigate network traffic alert group details and visualize connections through Link View in Express List®.


</td></tr><tr><td>

ITOM Cloud Accelerate

</td><td>

-   **[Cloud Account Management](https://www.servicenow.com/docs/access?context=cam-landing&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Cloud Account Management is the first feature from ITOM Cloud Accelerate in the Cloud Workspace application that brings together ServiceNow cloud solutions in a unified experience as part of the Cloud Governance Suite.


</td></tr><tr><td>

ITOM Visibility

</td><td>

-   **[Discover additional AWS Services using Patterns](https://www.servicenow.com/docs/access?context=aws-service-discovery-pattern&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**
    -   Starting with store version 1.25.0, Discovery and Service Mapping Patterns discovers 27 additional AWS cloud services.
    -   Starting with store version 1.27.0, Discovery and Service Mapping Patterns discovers 7 additional AWS cloud services.
-   **[Discover products with Discovery and Service Mapping Patterns](https://www.servicenow.com/docs/access?context=available-patterns&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Discover the following products using Discovery and Service Mapping Patterns version 1.27.0:

    -   [NVIDIA GPUs](https://www.servicenow.com/docs/access?context=nvidia-gpu-discovery-pattern&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)
    -   [Microsoft SQL Always On availability groups](https://www.servicenow.com/docs/access?context=mssql-data-collected-pattern&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)
    -   [Azure tenants and management groups](https://www.servicenow.com/docs/access?context=azure-cloud-discovery-patterns&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)
    -   [AWS Application Load Balancer targets](https://www.servicenow.com/docs/access?context=data-discovered-aws-patterns&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)
    -   [AWS web ACL](https://www.servicenow.com/docs/access?context=data-discovered-aws-patterns&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)
    -   [AWS Systems Manager \(SSM\) agents](https://www.servicenow.com/docs/access?context=data-discovered-aws-patterns&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)
    -   [Tag collection for Azure VM instance - Uniform scale set](https://www.servicenow.com/docs/access?context=AzureVMScaleSetInstance&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)
-   **[Automatically generate a Certificate Signing Request](https://www.servicenow.com/docs/access?context=request-new-csr-automated&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Generate a Certificate Signing Request and a private key with the Employee Center experience, starting with version 3.6.0 of Certificate Inventory and Management.

-   **[Use Service Graph Connectors for extended discovery](https://www.servicenow.com/docs/access?context=cmdb-sgc-available&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

Service Graph Connectors are a collection of predefined integrations that ingest data into the Configuration Management Database \(CMDB\) from third-party sources.

    -   Discover device details from Chromebook and ingest them into the CMDB by using Service Graph Connector for Google Console store version 1.8.
    -   Discover data from public cloud instances and resources in AWS, Azure, and GCP environments and ingest them into the CMDB by using Service Graph Connector for Wiz. 
-   **[Detect anomalies in Discovery schedules](https://www.servicenow.com/docs/access?context=discovery-admin-workspace-diagnostics&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Starting with Discovery Admin Workspace version 1.8.0, machine learning \(ML\) or statistical methods can detect anomalies in Discovery schedules and display this data in dashboards for admins. It identifies unusual behaviors like failed runs, significant deviations from user-defined thresholds for high error counts, longer discovery status duration, and fewer discovered Configuration Items \(CIs\) or Cloud resources. The ML-based approach to this feature is enabled by default. Thresholds are configurable via the new Settings page, and the results will be shown throughout the workspace.

-   **[Cloud-based Discovery schedules](https://www.servicenow.com/docs/access?context=discovery-admin-workspace-schedules&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Starting with version 1.8.0, Cloud-based discovery scheduling and reporting is available in Discovery Admin Workspace.

-   **[Configure Discovery to use Event Framework](https://www.servicenow.com/docs/access?context=t_ConfigureDiscoveryEventFramework&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Starting with version 1.9.0, Discovery jobs can be configured to use an event-based system, reducing database activity by queuing and processing events at regular intervals with priority and memory monitoring.


</td></tr><tr><td>

ITSM Mobile Agent

</td><td>

-   **[Summarize the incident record and activity information](https://www.servicenow.com/docs/access?context=gen-inc-rec-task-summariz&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

When adding work notes to an incident record, use the GenAI task summarization capabilities to summarize an incident record and activity information, such as the issue details or actions taken.

You can also summarize the incident information when adding work notes when reassigning the incident record. After an information summary is generated, you can edit and add the information as work notes. This feature helps reduce the effort required to draft work notes. The feature is available in the following applets:

    -   My team applet
    -   Major incidents
    -   My work
To enable this feature in ITSM Mobile Agent, you must configure the Incident summarization skill in Now Assist for ITSM.

-   **[Set alert tones for incident with different priority levels](https://www.servicenow.com/docs/access?context=set-alert-tones-incident-priority&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Set alert tones for incident with different priority levels. The alert tone can notify you of important actions so you can respond to them quickly.

-   **[Email notification redirection behavior](https://www.servicenow.com/docs/access?context=my-work-application&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Redirect from the mobile web browser to the ITSM Mobile Agent app seamlessly when opening and viewing different task records. This feature is applicable on the following type of records:

    -   Incident
    -   Incident task
    -   Catalog task
    -   Change request
    -   Change task
When you select the record link from an email notification on a mobile device, the link opens in the mobile web browser. A pop-up banner then prompts you to view the record in the ITSM Mobile Agent app, which provides a fast and intuitive way to access the records. This feature is applicable only if the following conditions are met:

    -   The ITSM Mobile Agent application is installed on the mobile device.
    -   The **Enable universal links** \(**glide.sg.universal\_links.enabled**\) system property is set to `true`.
-   **[Set the incident impact, urgency, and priority levels](https://www.servicenow.com/docs/access?context=create-incident-mobile&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Automatically set the incident priority level by defining the impact and urgency levels. This feature determines an incident priority level by maintaining uniform synchronization and consistency between the priority, impact, and urgency levels. When you edit the **Impact** and **Urgency** fields, you must add to the **Work notes** field.


</td></tr><tr><td>

ITSM Success Dashboard

</td><td>

-   The all new KPIs **Successful Change Summarization - Now Assist** and **Successful Change Risk Explanation - Now Assist** are added to the Productivity moments. These new contributing indicators help you understand the benefits of using change summarization and change risk explanation through Now Assist.
-   The Key Performance Indicator \(KPI\) **Knowledge Articles created using Now Assist** is added to Productivity moments. This primary indicator shows how many knowledge base articles are created using Now Assist in a given period.
-   New KPI is added to the self solved - percentage. This new KPI shares the number of times the issue is resolved using the Digital End-User Experience self service channels like Desktop Assistant, Now Assist panel, and Employee portal.

</td></tr><tr><td>

Identity

</td><td>

 

</td></tr><tr><td>

Impact

</td><td>

-   **[Impact Store Application](https://www.servicenow.com/docs/access?context=impact-store-app&version=yokohama&pubname=yokohama-impact&ft:locale=en-US)**
    -   [Impact Home page](https://www.servicenow.com/docs/access?context=impact-in-platform-home&version=yokohama&pubname=yokohama-impact&ft:locale=en-US)Use the Impact home page, an organized collaborative portal, which guides you to your relevant content and helps focus and accomplish your tasks with seamless interaction with Impact application features.
    -   [Use Guided Setup to synchronize and migrate data to the Impact Store Application](https://www.servicenow.com/docs/access?context=guided-setup-impact-in-app&version=yokohama&pubname=yokohama-impact&ft:locale=en-US): Use the simplified interface to synchronize and configure your Impact Store App with the Impact Delivery Instance.
    -   [Grant temporary instance access to your Impact Squad](https://www.servicenow.com/docs/access?context=hop-access-impact-squad&version=yokohama&pubname=yokohama-impact&ft:locale=en-US) to facilitate effective support and rapid issue resolution.
    -   [Convert an Impact entity to SPM entity as a work item](https://www.servicenow.com/docs/access?context=convert-spm-entity-impact-entity-recommendations&version=yokohama&pubname=yokohama-impact&ft:locale=en-US): Create an Impact entity and associate the SPM record details to it, which helps you to avoid manual intervention in converting the entities from Impact to SPM portals to avoid duplication of entities in the process.
    -   [Using recommendations list in Impact home page](https://www.servicenow.com/docs/access?context=using-recommendations-iip-ws&version=yokohama&pubname=yokohama-impact&ft:locale=en-US):
        -   Sort the recommendations list using the search and filter options by entering a keyword or phrase to narrow down the list and find the recommendations that you’re looking for.
        -   Convert Impact recommendations and free-form initiatives into actionable, trackable Strategic Portfolio Management \(SPM\) or Collaborative Work Management \(CWM\) work items. [Creating work items using recommendations and initiatives](https://www.servicenow.com/docs/access?context=creating-work-items-using-recommendations-and-initiatives&version=yokohama&pubname=yokohama-impact&ft:locale=en-US).
    -   [Impact Store Application product adoption](https://www.servicenow.com/docs/access?context=impact-in-platform-product-adoption&version=yokohama&pubname=yokohama-impact&ft:locale=en-US)
        -   Use the Product Adoption Roadmap \(PAR\) to view a recommended implementation sequence for your capabilities:
            -   [Create and publish a product adoption roadmap](https://www.servicenow.com/docs/access?context=create-product-adoption-roadmap&version=yokohama&pubname=yokohama-impact&ft:locale=en-US): Use pre-defined ServiceNow templates or build from your own.
            -   Use Product Adoption Roadmap Templates with pre-defined sequence of capabilities for ITSM \(\(IT Service Management\)\), ITOM \(\(IT Operations Management\)\), and Security Operations.
            -   View and edit phase-specific notes for a capability to understand prerequisites, plan training, and additional implementation considerations.
            -   Customize your roadmap by adding or removing capabilities as needed.
            -   Request Related Accelerators \(if available\) to improve adoption of the capabilities
    -   [Manage Capabilities Map](https://www.servicenow.com/docs/access?context=manage-capability-maps&version=yokohama&pubname=yokohama-impact&ft:locale=en-US):
        -   Explore, track, and manage the descriptions, notes, and related resources for your entitled capabilities.
        -   Use the updated Data Collection Content Packs to automatically transfer Impact Value Metrics to the centralized Impact instance to manage the Value Journey, including Setting Value Baselines and Targets, Outcome Performance Reviews, and the Value Report.
        -   Use the Capability Details page to view and manage comprehensive information related to a capability in your product adoption journey. The full-page layout replaces the previous pop-up view, making it easier to access, navigate and manage important details, such as usage status and notes in one centralized location.
        -   View and add adoption guidance for different phases, such as prerequisites and implementation instructions in notes specific to a phase.
        -   Measure a selected business objective under the same product across multiple ServiceNow instances. Use the Instance option on the Objectives and Outcomes, and Outcomes Insights to filter business objectives and outcomes by the ServiceNow instance. Add and edit the business objectives connected to the capability.
    -   [Impact Platform Health](https://www.servicenow.com/docs/access?context=impact-healthscan-store-app&version=yokohama&pubname=yokohama-impact&ft:locale=en-US):
        -   Use Proactive Code Check to track compliance against coding leading practices and organizational standards.
        -   Activate Proactive Code Check in the Health Store Application to scan update sets and check compliance standards and adherence to leading practices.
        -   Scan update sets for leading practice violations in a non-production environment with Proactive Code Check and improve code quality, reduce errors, and enhance system stability.
-   **[Impact Delivery Instance \(formerly Impact Digital Experience\)](https://www.servicenow.com/docs/access?context=impact-digital-experience&version=yokohama&pubname=yokohama-impact&ft:locale=en-US)**
    -   [Connect to the provider instance](https://www.servicenow.com/docs/access?context=connect-instance-impact-store-app&version=yokohama&pubname=yokohama-impact&ft:locale=en-US): The administrator or a named contact log in to your instance to facilitate the connection of data with the Impact Store Application.
    -   [Product Adoption](https://www.servicenow.com/docs/access?context=product-adoption&version=yokohama&pubname=yokohama-impact&ft:locale=en-US): Start an initiative from an individual capability to log and track your activities toward the implementation. The reference of the created initiative is available in the capability details and initiatives roadmap. The reference of the created initiative is available in the capability details and initiatives roadmap.
    -   [Healthscan definitions updates: May 2025 store](https://www.servicenow.com/docs/access?context=healthscan-definitions-may-store&version=yokohama&pubname=yokohama-impact&ft:locale=en-US): Some HealthScan definitions have been updated or deprecated for the May store release.
-   **[Accelerator catalog](https://www.servicenow.com/docs/access?context=accelerator-catalog&version=yokohama&pubname=yokohama-impact&ft:locale=en-US)**
    -   [Jumpstart Your Employee Journey Management](https://www.servicenow.com/docs/access?context=jumpstart-employee-journey-management&version=yokohama&pubname=yokohama-impact&ft:locale=en-US): Provides a demonstration of the possibilities and capabilities of Employee Journey Management.
    -   [Jumpstart Your Knowledge Management](https://www.servicenow.com/docs/access?context=jumpstart-knowledge-management&version=yokohama&pubname=yokohama-impact&ft:locale=en-US): Provides a demonstration of the possibilities and capabilities of Knowledge Management.
    -   [Jumpstart Your Legacy Workflow Migration](https://www.servicenow.com/docs/access?context=jumpstart-legacy-workflow-migration&version=yokohama&pubname=yokohama-impact&ft:locale=en-US): Provides a demonstration of the possibilities and capabilities of Legacy Workflow Migration.
    -   : Provides a demonstration of the possibilities and capabilities of Now Assist for CSM.
    -   [Jumpstart Your Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=jumpstart-now-assist-skill-kit&version=yokohama&pubname=yokohama-impact&ft:locale=en-US): ​Provides a demonstration of the possibilities and capabilities of Now Assist Skill Kit.
    -   [Jumpstart Your Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=jumpstart-now-assist-virtual-agent&version=yokohama&pubname=yokohama-impact&ft:locale=en-US): Provides a demonstration of the possibilities and capabilities of Now Assist in Virtual Agent.
    -   [Jumpstart Your Strategic Portfolio Management – Resource Management Workspace](https://www.servicenow.com/docs/access?context=jumpstart-strategic-portfolio-management-resource-management-workspace&version=yokohama&pubname=yokohama-impact&ft:locale=en-US): Provides a demonstration of the possibilities and capabilities of Resource Management Workspace within SPM.
    -   [Jumpstart Your GenAI](https://www.servicenow.com/docs/access?context=jumpstart-gen-ai&version=yokohama&pubname=yokohama-impact&ft:locale=en-US): Provides a demonstration of the possibilities and capabilities of ServiceNow® Generative AI application \(Artificial Intelligence\)
    -   [Release and Deployment Advisory for Pro-code Development](https://www.servicenow.com/docs/access?context=release-deployment-advisory-pro-code-development&version=yokohama&pubname=yokohama-impact&ft:locale=en-US): Provides guidance to assist pro-code developers in the tools and techniques to release and deploy ServiceNow application configurations and customizations.
    -   UX: The basics to unlock your ServiceNow success
    -   [UX: Why It Matters and How to Apply It](https://www.servicenow.com/docs/access?context=ux-why-it-matters-how-to-apply-it&version=yokohama&pubname=yokohama-impact&ft:locale=en-US): Takes examples directly from your instance to demonstrate how improving UX can directly influence the success of your ServiceNow investment.
    -   [LSD Maturity Assessment](https://www.servicenow.com/docs/access?context=lsd-maturity-assessment&version=yokohama&pubname=yokohama-impact&ft:locale=en-US): Provides guidance on fine-tuning your Legal Service Delivery \(LSD\) on the ServiceNow platform.
    -   [Introduction to CMDB: Ingestion](https://www.servicenow.com/docs/access?context=introduction-to-cmdb-ingestion&version=yokohama&pubname=yokohama-impact&ft:locale=en-US): Demonstrates the possibilities and capabilities of automating and standardizing the data entry from the input sources for their Configuration Management Database \(CMDB\).
    -   [Extend Your AI Search](https://www.servicenow.com/docs/access?context=extend-your-ai-search&version=yokohama&pubname=yokohama-impact&ft:locale=en-US): Provides prescriptive guidance on extending your AI Search beyond foundational levels.
    -   [Jumpstart Your Subscription Management](https://www.servicenow.com/docs/access?context=Jumpstart-your-subscription-management&version=yokohama&pubname=yokohama-impact&ft:locale=en-US): Provides a demonstration of the possibilities and capabilities available with the Subscription Management Application in your instance.
    -   [Jumpstart Your AI Agent Studio](https://www.servicenow.com/docs/access?context=jumpstart-ai-agent-studio&version=yokohama&pubname=yokohama-impact&ft:locale=en-US): Provides Impact customers with an overview and applied demonstration of AI agents within the platform.
-   **[Impact Instance Observer](https://www.servicenow.com/docs/access?context=io-overview&version=yokohama&pubname=yokohama-impact&ft:locale=en-US)**
    -   Use [Root Cause Correlation](https://www.servicenow.com/docs/access?context=root-cause-correlation&version=yokohama&pubname=yokohama-impact&ft:locale=en-US) to resolve issues that are identified by configured alerts and drill directly into the records causing the issues.
    -   [Instance Observer user configurable dashboard](https://www.servicenow.com/docs/access?context=user-configurable-dashboard&version=yokohama&pubname=yokohama-impact&ft:locale=en-US): Create your own dashboard according to your preferences of metrics to help analyze the health of your system in a snapshot or use the default home page to see a snapshot of instance overall health with key insights, such as performance, reliability, and availability at a glance with the available widgets.
    -   Use the Instance Observer Seats Add-on to obtain additional seats to your eligible Impact package.

</td></tr><tr><td>

Incident Management

</td><td>

-   **[User role for service desk agents](https://www.servicenow.com/docs/access?context=inci-roles-instld-itsm-roles&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

With the sn\_service\_desk\_agent user role, increase the operational efficiency by streamlining the process of asking about, gathering, and verifying information, as well as delivering quick resolutions. This role is designed for tier 1 service desk agents and is accessible when the ITSM Roles plugin \(com.snc.itsm.roles\) installed.

The sn\_service\_desk\_agent role includes the following user roles:

    -   sn\_incident\_write
    -   sn\_problem\_write
    -   sn\_change\_write
    -   sn\_request\_write
    -   tracked\_file\_reader
Additionally, with the installation of the ITSM Gen AI \(com.sn.itsm.gen.ai\) plugin, the knowledge\_user, and now\_assist\_panel\_user roles are integrated within the sn\_service\_desk\_agent role.

The sn\_service\_desk\_agent role can be used starting with SOW version 6.1.

-   **[Enhanced security model adoption for incident tables](https://www.servicenow.com/docs/access?context=activate-itsm-enhanced-security-inci-mangmnt&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Help prevent unauthorized access to incident-related tables using Deny-Unless ACLs. A Deny-Unless authentication ACL restricts access for a non-authenticated user, such as a public role user. Without access, the user can't perform any actions on incident-related tables, including reading, writing, deleting, creating, or accessing the report view.

This feature is activated automatically and applicable on the following incident-related tables:

    -   kb\_template\_incident\_kcs\_articl
    -   kb\_template\_incident\_kcs\_template
Additionally, this feature is available on the following incident-related tables of new or zBoot instances after installing the ITSM Enhanced Security Features \(com.snc.itsm.enhanced\_security\) plugin:

    -   incident
    -   incident\_task
    -   task\_ci
    -   task outage
The ITSM Enhanced Security Features \(com.snc.itsm.enhanced\_security\) plugin can be installed and activated by an admin via a support request. Existing or upgrade users must test and evaluate the results in their non-production instance, and then install the plugin and implement the security change in their production instance.

For more information, see [Deny-Unless ACL](https://www.servicenow.com/docs/access?context=acl-denial-behavior&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).


</td></tr><tr><td>

Industrial Process Manager

</td><td>

-   **[Set the operational status for equipment model entity sites](https://www.servicenow.com/docs/access?context=equipment-model-workspace&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Set equipment model entity sites to not in use in the Industrial Workspace by selecting the **Not in use** value for the **Operational Status** field.

-   **[Filter out Not in use and Retired equipment model entities from view](https://www.servicenow.com/docs/access?context=filter-out-non-operational-equipment-model-entities&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Filter out **Not in use** and **Retired** equipment model entities in the Industrial Workspace using the **Operational Status** field value for a site.

-   **[Add child equipment model entities to a Favorites view in the Industrial Workspace](https://www.servicenow.com/docs/access?context=favorite-child-equipment-model-entity&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Use the Favorite icon \(![](../image/mark-as-favorite.png)\) to add a child equipment model entity as a favorite in the Equipment Model Manager on the Industrial Workspace. You can then use the **Show Favorites** toggle to display them.

-   **[Assign Processing Order to sort equipment model entities in a site](https://www.servicenow.com/docs/access?context=view-child-entities-equipment-model-entity&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Use the **Processing Order** field to assign values to an equipment model entity that determines their functional importance in a site.

-   **[The Daily Activity tab in the Equipment Model view in the Industrial Workspace](https://www.servicenow.com/docs/access?context=view-ot-eme-daily-summary&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

View the list of previous day's activities on the **Daily Activity** tab of an OT device. The activities include adding an OT device and changing the field-level attributes for existing OT devices. For example, IP address, Device Criticality, and more.

-   **[Capture the mapped equipment model entity for your OT devices](https://www.servicenow.com/docs/access?context=view-all-mapped-ot-devices&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Organize your OT device data efficiently by adding the primary equipment model entity for your OT devices. You can also automatically update the primary equipment model entity for your existing devices.

-   **[Use the Unified Map experience in the Industrial Workspace](https://www.servicenow.com/docs/access?context=unified-maps-experience-iw&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

View the relationships between OT devices and other CIs with the Unified Map experience. You can also view related items, such as OT incidents and change requests.

-   **[Map Discovery detected devices using the Automated Mapping Across Zone-based IP Network Groups \(AMAZING\) feature](https://www.servicenow.com/docs/access?context=automatedly-map-all-ot-assets&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Map Discovery detected devices that have an IP address on their Network Adapter record using the AMAZING feature.


</td></tr><tr><td>

Instance Data Replication

</td><td>

-   **[Scheduled seeding](https://www.servicenow.com/docs/access?context=set-up-scheduled-replication-idr&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

Replicate data from a producer to a consumer at scheduled times each day.

-   **[Multiple seeding requests](https://www.servicenow.com/docs/access?context=seed-consumer-instance&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

Run concurrent seeding requests across multiple replication sets, with up to one active request per set.

-   **[Automatically seed missing or mismatched records](https://www.servicenow.com/docs/access?context=compare-replicated-data&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

Automatically seed missing or mismatched records when you create a data comparison request.


</td></tr><tr><td>

Integration Hub

</td><td>

-   **[Stream Connect alerting](https://www.servicenow.com/docs/access?context=stream-connect-alert&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**
    -   Get alerts for your Stream Connect integrations. Stream Connect uses both active and scheduled monitoring to detect events across multiple Stream Connect components. If an issue is detected, an alert is created, and a message is logged to the Stream Connect Log.
    -   Specify alert thresholds by configuring alerting properties. For example, you can specify a maximum amount of time to process the current message queue. If the estimated processing time exceeds your specified time, an alert is generated.
    -   Receive alert notifications via email, SMS, or the ServiceNow® mobile app. Notifications contain detailed alert information, including the alert number, level, and a description. You can configure notification settings based on alert types, severity, and user preferences.
-   **[View producer statistics in the Stream Connect dashboard](https://www.servicenow.com/docs/access?context=stream-connect-dashboard&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

Get detailed information about Stream Connect producers and their performance, including a producer’s status and type, the number of bytes and messages produced to a topic, and producer data trends over time, in the Stream Connect dashboard.

-   **[Check data usage in the Stream Connect dashboard](https://www.servicenow.com/docs/access?context=stream-connect-dashboard&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

View total data usage and data usage per month and topic with the Stream Connect dashboard. Data usage history is available for the last 12 complete months plus the current month.

-   **[Use error evaluation with Data Stream actions](https://www.servicenow.com/docs/access?context=data-stream-actions&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

Catch step errors and specify error behavior for each step in a Data Stream action. Create your own error conditions by specifying when an action returns an error state and the status codes and messages they return.

-   **[View connection aliases in integration actions](https://www.servicenow.com/docs/access?context=managing-connections-integration-hub&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

Edit, configure, and create connection aliases in the Action Properties section of actions in ServiceNow® Workflow Studio. View connection error details for connection aliases that are not set up or configured.


</td></tr><tr><td>

Intelligence for CSM

</td><td>

-   **[Recommended Actions - Front-line case page integration with knowledge guidance](https://www.servicenow.com/docs/access?context=csm-front-line-case-page&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Enable agents to attach and share knowledge article links in comments, work notes, or emails by using modeless dialogs.

-   **[Recommended Actions - Default guidance for search results](https://www.servicenow.com/docs/access?context=ra-csm-guidances-default-guidance-search&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Enable agents to view search results for any records. Use a default guidance for any search sources that don't have a dedicated, mapped guidance.

-   **[Recommended Actions - Improved timeout handling for resource generators](https://www.servicenow.com/docs/access?context=ra-csm-resource-generators&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Handle timeout errors when calling Machine Learning \(ML\) resource generators. The system uses a subflow API with a 1-second timeout ensures the RA generation engine prioritizes faster response times by terminating stalled ML prediction calls.

-   **[Recommended Actions - Custom guidances](https://www.servicenow.com/docs/access?context=ra-csm-custom-guidances&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Use a custom guidance to provide actions that are based on the search results from the Case, Problem, Incident, or Change Request tables. Agents can use these actions to link records to the current case and copy resolution codes and notes from resolved cases.

-   **[Recommended Actions - Field values for predicted records](https://www.servicenow.com/docs/access?context=ra-csm-guidances&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US#section_lmj_cl3_c2c)**

Leverage the actual field value for a predicted record and show it in a custom guidance in place of the display value.

-   **[Recommended Actions for Customer Service - Display Recommended Actions on the CSM Interaction record page](https://www.servicenow.com/docs/access?context=ra-csm-chat-interaction-record&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Enable agents to view Recommended Actions in the contextual side panel on the CSM Interaction record page. The search tab dynamically displays relevant actions based on the context of the chat interaction.

-   **[Recommended Actions for Customer Service - Interaction Context record](https://www.servicenow.com/docs/access?context=ra-csm-context-records&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Use the Interaction Context record to display the search results from the Knowledge table. The results are based on the interaction's short description. This context record includes a search-mapping record that maps knowledge results to the Share KB in chat interactions guidance.

-   **[Recommended Actions - Question font size customization for a Decision tree](https://www.servicenow.com/docs/access?context=configure-decision-trees-gdb&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Enables you to customize the font size of questions in a Decision tree for a better look and feel. This font size is applied to the questions in the decision trees of playbooks, and recommendations, within the CSM Configurable Workspace and service portal.

-   **[Recommended Actions - Control the visibility of completed guidance information](https://www.servicenow.com/docs/access?context=create-guidances&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Allows you to manage the visibility of the completed guidance history information of a decision tree in playbooks, and recommendations for an agent, within the CSM Configurable Workspace, and service portal for a streamlined experience.

-   **[Recommended Actions – AI search on CSM default record page, Front line case page, and CSM interaction record page](https://www.servicenow.com/docs/access?context=ra-csm-ai-search&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

The Recommended Actions – AI search is introduced on the [CSM default record page](https://www.servicenow.com/docs/access?context=csm-default-record-page&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US), [Front-line case page](https://www.servicenow.com/docs/access?context=csm-front-line-case-page&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US), and [CSM Interaction record page](https://www.servicenow.com/docs/access?context=csm-interaction-record-page&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US) \(for the chat, video, walk-up, and email type channels\) and it’s enabled by default for new customers. The default guidance is also enabled for these pages. Agents can attach and share knowledge article links in comments, work notes, and emails.

-   **[Recommended Actions - Catalog item source type for AI search](https://www.servicenow.com/docs/access?context=ra-csm-ai-search&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Search and filter the catalog items easily in the AI search tab of Recommended Actions in the CSM Configurable Workspace.

-   **[Recommended Actions - Ability to have multiple active contexts for the same table](https://www.servicenow.com/docs/access?context=ra-csm-contexts&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Enables multiple active contexts for the same table, so that tailored recommendations are displayed in the CSM Configurable Workspace:

    -   For different user personas based on their requirements.
    -   For different Predictive Intelligence models or AI model variants.
    -   For the same record in different channels, such as chat, email, and so on.
-   **[Recommended Actions - Ability to inherit active rules and their recommendations from a parent table context to extended table context](https://www.servicenow.com/docs/access?context=ra-csm-contexts&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Assign the active rules and their recommendations from the parent table context to the extended context table for a streamlined process.

-   **[Recommended Actions - Asynchronous evaluation for recommendations](https://www.servicenow.com/docs/access?context=ra-csm-contexts&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Enables you to configure loading behavior at the context level by choosing between synchronous and asynchronous modes. In the asynchronous mode, recommendations load in the background without blocking the UI, allowing agents to interact with the record immediately.


</td></tr><tr><td>

Knowledge Graph

</td><td>

-   **[Test a Knowledge Graph schema](https://www.servicenow.com/docs/access?context=test-a-knowledge-graph-schema&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Enter a query and test the Knowledge Graph schema using different LLM options. You can also add previous conversations before you run the query.


-   **[Access Knowledge Graph Schema](https://www.servicenow.com/docs/access?context=access-knowledge-graph-designer&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Knowledge Graph now has a new NLQ graph schema available prebuilt along with user profile schema. See [KB article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2069778) for schema attributes.


-   **[Leverage Knowledge Graph prebuilt integration with Virtual Agent](https://www.servicenow.com/docs/access?context=example-use-case-for-knowledge-graph&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Knowledge Graph provides the following new prebuilt integrations:

    -   Integration with Now Assist Virtual Agent: Helps requesters with personalized responses on people queries and Natural Language queries. Also supports people citation card.

-   **[Leverage Knowledge Graph prebuild integration with AI agents](https://www.servicenow.com/docs/access?context=leverage-knowledge-graph-prebuild-integration-with-agentic-ai&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Knowledge Graph provides the following prebuilt integrations:

    -   Integration with Now Assist AI agents for User Context: Helps users with personalized responses.
    -   Integration with AI agents as a tool: Used to perform specific tasks that are assigned to the AI agents.

-   **[Exploring Knowledge Graph](https://www.servicenow.com/docs/access?context=exploring-knowledge-graph&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Knowledge Graph helps requesters with personalized responses using its Integration with Now Assist Virtual Agent for User Context.

Use Knowledge Graph integration with Now Assist Virtual Agent for Slot filling to helps pre-fill the slots for Virtual Agent topics using Natural Language Querying feature of Knowledge Graph.

-   **[Leverage Knowledge Graph prebuilt integration with Virtual Agent](https://www.servicenow.com/docs/access?context=example-use-case-for-knowledge-graph&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Use the Knowledge Graph integrations with Now Assist Virtual Agent to utilize Knowledge Graph APIs built with LLM models, for personalized responses and slot-filling fields to execute LLM topics and skills in Virtual Agent.

-   **[Using Knowledge Graph Designer](https://www.servicenow.com/docs/access?context=using-knowledge-graph-designer&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Use Knowledge Graph designer to manage Knowledge Graph schemas, their nodes, node properties and edges. You can also use the interface to create, edit, duplicate, or delete a Knowledge Graph schema.


</td></tr><tr><td>

Knowledge Management

</td><td>

-   **[Configure skills with custom prompts for knowledge article templates](https://www.servicenow.com/docs/access?context=Now-assist-configure-custom-prompts-for-templates&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

As an admin, you can clone the KB generation skill, and update prompts for AI model providers. This helps the agent to use custom templates and custom prompts to generate Knowledge articles with Now Assist from single and multiple knowledge bases.


</td></tr><tr><td>

Lead Management

</td><td>

-   **[REST APIs for Lead Management](https://www.servicenow.com/docs/access?context=create-new-lead&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

REST APIs provide the following capabilities:

    -   Integrate lead management with external applications and websites.
    -   Create and modify leads and lead line items from applications like marketing automation systems.
    -   Retrieve leads and lead line items from your ServiceNow instance.

</td></tr><tr><td>

Legal Hold Notification

</td><td>

-   **[Legal hold matter management](https://www.servicenow.com/docs/access?context=lg-hold-notif-landing-page&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Manage legal hold matters by submitting, updating, tracking, and closing them through a streamlined process that reduces effort and ensures organizational compliance.


-   **[Submitting legal hold matter](https://www.servicenow.com/docs/access?context=submit-lg-hold-notif-matter&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Submit a legal hold matter to initiate the data preservation process when a legal hold is issued.


-   **[Issuing legal hold notice](https://www.servicenow.com/docs/access?context=issue-lg-hold-notif-matter&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Issue a legal hold notice to custodians to initiate timely data preservation, ensure accountability, and reduce the risk of data loss.


-   **[Legal hold notice acknowledgement](https://www.servicenow.com/docs/access?context=acknow-lg-hold-notif&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Record custodian acknowledgments of legal hold notices to confirm their responsibility to preserve data and ensure accountability.


-   **[Assign new custodians](https://www.servicenow.com/docs/access?context=add-new-custodian-lg-hold-notif&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Assign newly identified custodians to existing legal hold matters to ensure comprehensive and up-to-date data preservation.


-   **[Acknowledge reminders](https://www.servicenow.com/docs/access?context=send-reminder-for-acknowledgment&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Send reminders to custodians who haven’t acknowledged legal hold notices to ensure accountability in data preservation.


-   **[Closing legal hold matter](https://www.servicenow.com/docs/access?context=close-lg-hold-notif-matter&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Close a legal hold matter once the hold is lifted to complete the data preservation life cycle.


</td></tr><tr><td>

MID Server

</td><td>

-   **[External Credential Storage and Management supports certificate-based authentication for Azure Key Vault](https://www.servicenow.com/docs/access?context=mid-azure-key-vault-integration&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

The External Credential Storage and Management added support for certificate-based authentication when connecting to Azure Key Vault. This provides a more secure and flexible way to authenticate, especially for enterprise environments that prefer certificate credentials over client secrets.


</td></tr><tr><td>

Manager Hub

</td><td>

-   **[Know your team members](https://www.servicenow.com/docs/access?context=use-mr-mh&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

View employee availability and schedule conversations with employees using the **Create a conversation** panel if you do not have Microsoft Outlook integration enabled or the **Schedule a conversation** panel if you do.

-   **[View employee cards in Skills Expectations section](https://www.servicenow.com/docs/access?context=emp-card-mh&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Track skill proficiency, assign targeted learning, and view in-depth skill progress bars to monitor employee development by using the **Skill score analysis** panel.

-   **[Know your team members](https://www.servicenow.com/docs/access?context=use-mr-mh&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Enable managers to view all direct and indirect reporting details, daily team stats, and other employee details such as tasks submitted for approval, upcoming time off, and employee profiles.


</td></tr><tr><td>

Manufacturing Commercial Operations

</td><td>

-   **[Manufacturing Commercial Operations users](https://www.servicenow.com/docs/access?context=manufacturing-explore&version=yokohama&pubname=yokohama-manufacturing&ft:locale=en-US)**

User roles provide the information on the users and their responsibilities.

-   **[Dealer](https://www.servicenow.com/docs/access?context=dealer-data-model-overview&version=yokohama&pubname=yokohama-manufacturing&ft:locale=en-US)**

The dealer framework helps you manage the day-to-day business activities and monitor the real-time data insight.

**Note:** Q2 release includes only the data model and not the playbook.

-   **[Sales Promotion data model](https://www.servicenow.com/docs/access?context=sales-promotion-campaign-claims&version=yokohama&pubname=yokohama-manufacturing&ft:locale=en-US)**

The sales promotion framework helps the OEM to publish the promotions and the dealers to raise the claims against these promotions after the product sales transaction is completed.

**Note:** Q2 release includes only the data model and not the playbook.

The sales promotion supports bulk import functionality. To enable bulk import, you must customize it on existing CSM or Business Location Service Portal \(BLSP\) portals.

-   **[Install Manufacturing Commercial Operations plugin](https://www.servicenow.com/docs/access?context=manufacturing-commercial-operations-plugins&version=yokohama&pubname=yokohama-manufacturing&ft:locale=en-US)**

List of all the plugins that are installed with Manufacturing Commercial Operations plugin.


-   **[Support multiple line items on a case to track requests on the Business Portal​](https://www.servicenow.com/docs/access?context=manufacturing-using&version=yokohama&pubname=yokohama-manufacturing&ft:locale=en-US)**

Capture and track requests for multiple items on the Business Portal.​ Case line items, case tasks, and case line tasks all appear on the case page​.

-   **[Enable copy of catalog items from Service Catalog to Remote Catalog in Service Exchange](https://www.servicenow.com/docs/access?context=mco-using-servicebridge-manufacturers&version=yokohama&pubname=yokohama-manufacturing&ft:locale=en-US)**

Eliminate duplication effort in Remote Catalog creation and maintenance​, by enabling the copying of standard portal catalog items. This process eliminates the need to manually recreate Service Catalog items in the Service Exchange Remote Catalog.

-   **[View products from the catalog and place orders directly through the Sales CRM self-service portal](https://www.servicenow.com/docs/access?context=mco-som-using&version=yokohama&pubname=yokohama-manufacturing&ft:locale=en-US)**

Enable B2B customers to configure products and place orders via an uptake of the Sales Customer Relationship Management self-service order placement portal​.​


</td></tr><tr><td>

Mastercard Spoke

</td><td>

-   **[Mastercard Spoke actions](https://www.servicenow.com/docs/access?context=mastercard-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

The following Mastercard Spoke actions were built for Mastercom Extended:

    -   Attach Document by Case ID - Extended
    -   Attach Documents by Claim ID and Event ID - Extended
    -   Check Document Details - Extended
    -   Create a Report - Extended
    -   Create Chargeback Reversal - Extended
    -   Create Claim - Extended
    -   Create Pre-Arbitration/Arbitration Case - Extended
    -   Create Pre-Compliance/Compliance Case - Extended
    -   Initiate a Dispute by Claim ID - Extended
    -   Look up Case Details by ID - Extended
    -   Look up Claim Details by ID Request Builder - Extended
    -   Look up Claim Details by ID Response Parser - Extended
    -   Look up Claim Details Request Builder - Extended
    -   Look up Claim Details Response Parser - Extended
    -   Look up Claims in a Queue by ID Stream - Extended
    -   Look up Completed Report - Extended
    -   Look up Processed Documents by Case ID Request Builder - Extended
    -   Look up Processed Documents by Case ID Response Parser - Extended
    -   Look up Processed Documents by Document Completed ID Request Builder - Extended
    -   Look up Processed Documents by Document Completed ID Response Parser - Extended
    -   Look up Queue by ID - Extended
    -   Look up Queues Stream - Extended
    -   Look up Report Fields - Extended
    -   Look up Report Fields Stream - Extended
    -   Look up Report Status - Extended
    -   Look up Reports Stream - Extended
    -   Look up Statuses for Documents Associated with Cases - Extended
    -   Look up Transactions Request Builder - Extended
    -   Look up Transactions Response Parser - Extended
    -   Update Pre-Arbitration/Arbitration Case - Extended
    -   Update Pre-Compliance/Compliance Case - Extended
    -   Update Representment by Claim ID and Event ID - Extended
    -   Upload Documents - Extended

</td></tr><tr><td>

Mentoring

</td><td>

-   **[Snapshot of preferences](https://www.servicenow.com/docs/access?context=edit-mentee-preferences&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Store a Mentoring snapshot of all overlapping preferences at the time of relationship acceptance by the mentor.

-   **[Mentor match insights](https://www.servicenow.com/docs/access?context=view-match-insights&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Mentees and Mentors can view suggested matches based on their enrolled preferences or skills.


</td></tr><tr><td>

Mobile Platform

</td><td>

-   **[Now Assist Context Menu](https://www.servicenow.com/docs/access?context=now-assist-context-menu-mobile&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)**

Write and edit text natively from within your mobile app using the Now Assist Context Menu. Refine your selected text by asking Now Assist to shorten it, make it more elaborate, or change the tone, and so on. Now Assist Context Menu is supported for the Task Summarization skill for input form screens.

-   **[Single instance login](https://www.servicenow.com/docs/access?context=mobile-instances-admin-concept&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)**

Customers with a single instance can bypass the instance selection page and navigate users directly to the login screen. This process shortens the login process.

-   **[Display a customized page before user login](https://www.servicenow.com/docs/access?context=branded-landing-page&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)**

Configure your own branded landing page to appear before users log in to their ServiceNow mobile apps. The branded landing page can contain a login button or deep link that redirects users to an area of a ServiceNow mobile app. For example, a municipality can add a button to open a ticket, which navigates the user to complete a record in the Now Mobile® app.

This feature is available to customers using a single instance, and is supported for both Mobile Publishing apps.

-   **[Define attachment sources available to users](https://www.servicenow.com/docs/access?context=attachment-source-define&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)**

Control the types of attachments used from a phone's gallery, camera, or file system. This capability confirms that images can’t be reused or are AI-generated images. This feature is supported for all attachment locations, including: activity stream, functions with type “attachment”, input form screen with field type “attachment”, Mobile App Bridge, and Cabrillo JS uploads.

-   **[Add annotations to uploaded images](https://www.servicenow.com/docs/access?context=image-annotation-adjust&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)**

Edit and annotate uploaded images within ServiceNow mobile apps. Markup options include adding text, drawing, and highlighting areas. This feature is supported for all attachment locations, including: activity stream, functions with type “attachments”, input form screen with field type “attachment”, Mobile App Bridge, and Cabrillo JS uploads.

-   **[Mobile App Builder live mobile previews](https://www.servicenow.com/docs/access?context=mab-record-example-panel&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)**

See your mobile content change in real-time with live previews for most mobile components. The mobile interface changes according to what component you have selected, and updates when you add, change, or remove UI-based elements.

-   **[Web to mobile AI card creation](https://www.servicenow.com/docs/access?context=web-mobile-component-conversion&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)**

Use Now Assist to create a new mobile card for use on a record screen created using the Web to Mobile functionality. Now Assist will automatically choose the optimal card template and map the most relevant table fields from the selected web form view.

-   **[Agentic AI in Mobile Virtual Agent](https://www.servicenow.com/docs/access?context=agentic-ai-mobile-va&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)**

Use AI agents in your mobile app to boost live agent productivity. AI agents handle tasks from automated responses to complex problem-solving with human-like intelligence.

-   **[Now Assist in the Virtual Agent mobile client](https://www.servicenow.com/docs/access?context=now-assist-mobile-va&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)Mobile Virtual Agent&gt;**

Use the following enhancement added to Virtual Agent:

    -   Enhanced chat offers a more robust conversational experience. Check the status of previous and on-going chats with the chat history button and view Now Assist’s responses with streamlined in-line citations. Enhanced chat also allows you to use your custom mobile search configuration to launch the standard search results page from within enhanced chat.
    -   Use Now Assist’s people match function to search for information about a specific employee.
    -   Now Assist can now suggest follow-up actions for your queries using the next best action feature.
    -   Updated UI for choice list pickers and other actions for improved usability.
    -   Added multi-language support.

</td></tr><tr><td>

Next Experience

</td><td>

-   **[Fuzzy search results returned within the Unified Navigation menus](https://www.servicenow.com/docs/access?context=using-the-next-experience-global-header&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

Find relevant search results even with shortened text by using the fuzzy results filter, which ranks results based on their similarity to your search query. Adjust the minimum accuracy score to help fine-tune filter behavior.

-   **[Customizing the Next Experience keyboard shortcuts](https://www.servicenow.com/docs/access?context=customize-keyboard-shortcuts&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

Assign specific actions to unique key combinations to quickly execute tasks. See the Accessibility information section for details.

-   **[Activity stream user preference available](https://www.servicenow.com/docs/access?context=next-experience-workspace-preferences&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

Enable the activity stream to automatically expand all activities from within the Workspace user preference group.

-   **[Next Experience keyboard shortcuts](https://www.servicenow.com/docs/access?context=next-experience-keyboard-shortcuts&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

Use a new keyboard shortcut to open and close the Now Assist panel and another keyboard shortcut to enable Now Assist voice input mode.


</td></tr><tr><td>

Next Experience Components

</td><td>

|Component|Description|
|---------|-----------|
|Active call|Handles phone calls as part of the Interaction controls component \(ICC\). Manages call functions, including actions such as disconnect, mute, hold, record, and transfer.|
|Animation|Places Lottie animations in Next Experience pages or components created in UI Builder.|
|Dialpad|Dial a phone number in Workspace.|
|Feedback|Captures detailed feedback from users for AI products or skills through a series of pre-determined options or free-text responses.|
|Filter group|Groups up to 3 filter components into a single container with configurable **Apply**, **Clear**, and **Reset** buttons that apply to all filters in the group.|
|Flyout menu|Menu that organizes multiple levels of options within a hierarchical structure.|
|Knowledge view|Embeddable container that renders a Next Experience Knowledge article view.|
|Loader custom|Renders custom animations with an optional progress bar and label.|
|Skeleton loader|Decorative placeholder for generated content.|

</td></tr><tr><td>

Notifications

</td><td>

-   **[Email notifications dashboard](https://www.servicenow.com/docs/access?context=email-notifications-dashboard&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Use the new notifications dashboard with key metrics. This dashboard is available to administrators by default. You can configure this dashboard to enable access to other users.


</td></tr><tr><td>

Notify

</td><td>

-   **[Deny-Unless ACL](https://www.servicenow.com/docs/access?context=acl-denial-behavior&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

Enhance the security of Notify tables by restricting access for non-authenticated users through Deny ACLs.

-   **[Enhanced security for client-callable script includes](https://www.servicenow.com/docs/access?context=r_NotifyRoles&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

Enhanced security for all client-callable script includes by introducing the ability to switch off the sandbox mode, providing greater control and protection against unauthorized script execution for Notify tables.


</td></tr><tr><td>

Now Assist

</td><td>

-   **[Monitor sensitive topic invocations](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Access the Gen AI Metrics \[sys\_generative\_ai\_metric\] table to review the logged invocations of sensitive topics and gain insights into how these topics are being triggered and monitored.


-   **[Now Assist Readiness Evaluation](https://www.servicenow.com/docs/access?context=now-assist-readiness-evaluation-landing-page&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

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


-   **[Manage large language models](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Choose and update your preferred large language model \(LLM\) provider at the instance, skill or skill group level for Now Assist out-of-box skills with ServiceNow® third-party model strategy.

Deactivate skills that are not compliant with any of the LLM providers and access the audit history to view updates by the AI steward.

-   **[Configure multilingual service for Now Assist applications](https://www.servicenow.com/docs/access?context=enable-dynamic-translation-for-now-assist-applications&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Manage the default and supported languages by the different LLM providers under Multilingual service for translation.

-   ****

Access the citations to the articles referenced from the knowledge base. Explore references and insert the suggested reply to your email.

-   **[Now Assist Guardian supports third-party LLMs](https://www.servicenow.com/docs/access?context=now-assist-guardian&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Extend guardrail support to third-party LLMs, such as Amazon Bedrock, Google Cloud \(AI Studio and Vertex\), and OpenAI to ensure any inappropriate content is logged and blocked during content generation.


-   **[Increase the maximum response token limit for custom skills](https://www.servicenow.com/docs/access?context=configure-skill-prompt&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Increase the maximum response token limit for Now Assist custom skill beyond default value 1000 to support dynamic pricing based on output tokens and calculate the price for each skill executed per assist.


-   **[Exploring Now Assist](https://www.servicenow.com/docs/access?context=exploring-now-assist-platform&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Access the Now Assist skills through an identifier tab on the Now Assist Admin console, and find the associated workflows.

Navigate to your skills by using the intuitive list or grid view. The skill details are displayed, which means that you don't have to make additional selections.

Access the Data privacy section under Now Assist Admin settings. View and edit the data privacy policies that apply to your Now Assist skills.

-   **Accessing the external content in Now Assist panel Q&amp;A capability**

Get relevant answers to your questions from external content sources, such as Microsoft SharePoint, Google Drive, and Confluence Cloud, within the Now Assist panel, without manual indexing. Each response shows the source of information to reference later.

-   **[Enhanced log visibility](https://www.servicenow.com/docs/access?context=now-assist-guardian&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**
    -   Access the Generative AI Metric table \[sys\_generative\_ai\_metric\] to gain insights into the guardian logs and determine if they are for monitoring only or for both logging and blocking. Each guardrail shows its status value as Monitor, Block, or Off, to help administrators to manage their security policies.
    -   View the logs of masking that involve personal identifiable information \(PII\) in the Generative AI Metric table \[sys\_generative\_ai\_metric\]. You can identify which data is masked, the type of request, system response, processing time, errors, or error codes.
-   ****

Define the output field destination so that you can select any multi-line text field from the base table You can customize incident forms and improve the usability of the resolution notes generation skill.

Enable requesters to extract information from emails and email attachments to generate tasks. This email-to-task agentic workflow effectively addresses the challenge of task creation from emails.

-   **[Identify and review duplicate Knowledge articles](https://www.servicenow.com/docs/access?context=Now-Assist-identify-and-review-duplicate-articles&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

Identify duplicate Knowledge articles by using Now Assist capabilities. You can review the list and deselect articles that you don’t consider to be duplicates.

-   **[Streaming responses](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Enable streaming responses on the Now Assist panel. Only synthesized responses are streamed.

-   **[Multiple Now Assist panels](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Create separate, independent Now Assist panels that work across Next Experience and ServiceNow® Studio app shells.

-   **[Create Now Assist context Menu configuration](https://www.servicenow.com/docs/access?context=create-now-assist-configuration-with-guided-setup&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Create a Now Assist context menu configuration for a streamlined custom skill deployment process with the help of a guided setup.


-   **[Now Assist Guardian analytics](https://www.servicenow.com/docs/access?context=now-assist-guardian&version=yokohama&pubname=yokohama-intelligent-experiences&section=now-assist-guardian-analytics&ft:locale=en-US)**

Monitor the performance of offensive content and prompt injections guardrails with the help of the Now Assist Guardian analytics dashboard.

-   **[Configuring Now Assist settings and features](https://www.servicenow.com/docs/access?context=configuring-na-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

For custom skills, explore an additional display option in the form of **Conversational experiences**. You can select Now Assist Virtual Agent to assist you with the display.

Create and activate a Now Assist skill copy, and have both the original skill and its copy to remain active simultaneously.


-   **[Now Assist Context Menu usage dashboard](https://www.servicenow.com/docs/access?context=now-assist-context-menu-dashboard&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

View and monitor the use of the Now Assist context menu across the different applications. Gain insights into the usage patterns, frequency, and effectiveness of the context menu actions with the Now Assist context menu usage dashboard.

-   **[Customizing ServiceNow skills in the Now Assist Skill Kit to tailor skills to meet your specific business requirements.](https://www.servicenow.com/docs/access?context=clone-and-edit-servicenow-skill&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Clone the skills provided by ServiceNow in Now Assist applications by using the Now Assist Skill Kit so that you can edit the prompt or change the AI service provider. By editing the prompt, you can choose the additional inputs to be considered by the large language model \(LLM\) and arrange the formatting and content of the LLM response. After the skill is edited, you can activate the edited skill in the Now Assist Admin console to enable it.

-   **[Enabling the voice input for the Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Enable the Voice Input setting for the Now Assist panel in the Now Assist Admin console. This setting gives users a voice-to-text input option to access the skills in the Now Assist panel in any supported language. After it’s enabled, the option is available in individual user accessibility preferences.

-   **[Setting your data overflow processing preferences to control your data](https://www.servicenow.com/docs/access?context=configure-na-data-overflow&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Set your data overflow processing preferences to control your data. By default, all Now Assist network traffic is managed within ServiceNow datacenters, but during periods of high traffic, the traffic is burst to Microsoft Azure datacenters. You can choose whether you want to opt out of cloud bursting from the Now Assist Admin console data overflow processing settings.

-   **Using multi-turn Q&amp;A in the Now Assist panel**

Ask questions and get relevant answers directly in the Now Assist panel. The system remembers your previous questions for effortless follow-ups and pulls answers from multiple sources to give you the best results. You can select the source name in the response to access the full Knowledge article for more details.


-   **Using dashboard and visualization export in the Now Assist panel**

Export Platform Analytics dashboards and data visualizations through conversations. You can select from several output formats, and download or email the files.


-   **[Summarize records with the Now Assist context menu](https://www.servicenow.com/docs/access?context=summarize-with-now-assist-context-menu&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Generate summaries by using the Now Assist context menu for the Core UI and Workspace. You can also expand or collapse the summary card, regenerate the summary, copy and share the summary, or provide feedback.


-   **[Email recommendations using the Now Assist context menu](https://www.servicenow.com/docs/access?context=email-recommendations-nacm&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Select and choose the tone of your content with the change tone feature. You can select from the elaborate, shorten, casual, formal, or sympathetic tone.


</td></tr><tr><td>

Now Assist AI agents

</td><td>

-   **[Configure role masking for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-role-masking&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Role masking restricts access to specific roles based on configuration to verify that agentic workflows, AI agents, and tools run within the boundaries of the roles configured to meet their business needs while reducing the risk of unauthorized access to the agents and the agentic data.

-   **[Add AI agent learning](https://www.servicenow.com/docs/access?context=agent-learning&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Enhance AI agent learning through episodic memory, enabling AI agents to improve by learning from past successful interactions.

-   **[Select channels and access for an agentic workflow](https://www.servicenow.com/docs/access?context=channels-access-aw&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Create and update UI actions for workflow executions and display handling. You can specify conditions for the display of the UI actions.

-   **[Add a desktop action to an AI agent](https://www.servicenow.com/docs/access?context=add-desktop-action-ai-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Add Desktop action as a tool to an AI agent to perform desktop automation for repetitive tasks.

-   **[Configuring Now Assist AI agents](https://www.servicenow.com/docs/access?context=configuring-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Support multilingual conversations for AI agents across languages.

-   **[Manually test the execution of an AI agent](https://www.servicenow.com/docs/access?context=test-ai-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) and [Manually test the execution of an agentic workflow](https://www.servicenow.com/docs/access?context=test-aia-use-case&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

The testing page on AI Agent Studio has two testing options:

    -   Manual test
    -   Automated evaluation
Observe the different versions of an AI agent behavior in manual tests and in automated evaluations using the **Manual tests** and **Automated tests** tabs.

-   **[Test user access to an AI agent](https://www.servicenow.com/docs/access?context=test-aia-access&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) and [Test user access to an agentic workflow](https://www.servicenow.com/docs/access?context=test-aw-access&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Test how an AI agent or agentic workflow completes a task and if it enables users permission to access it.

-   **[Model Context Protocol Client](https://www.servicenow.com/docs/access?context=mcp-client&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**
    -   Authorization upgrades to support segregation of Resource Server and Authentication Server through Protected Resource Metadata \(PRM\).
    -   Use the **mcp\_guardian\_check** property to enable guardian checks for MCP Client when there’s an MCP tool call.
    -   Supervise the pagination with mouse device support to show large number of services from an MCP server through the **sn\_mcp\_client.cursor.max\_iterations** system property.
    -   Add a title field for human-friendly display names that can be used as a programmatic identifier.
-   **[Use in-product experiences for agentic workflows on forms](https://www.servicenow.com/docs/access?context=in-product-agentic-ai&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

In the Core UI and workspaces, you can use UI and declarative actions to run agentic workflows. You can also see the presence, progress, and output of agentic workflows performed on a record. The execution details for each agentic workflow include who is supervising the workflow, estimated and total time taken, processing messages, and step history.

-   **[Review and approve requests and tickets with the Approval Assistance AI agent](https://www.servicenow.com/docs/access?context=platform-approval-aia&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

You can use the new approval assistance AI agent to view all pending approval requests and access detailed information about them. You can then approve requests and tickets and make updates to them from Now Assist in Virtual Agent.

-   **[Configure email notification alerts for AI agent and agentic workflow executions](https://www.servicenow.com/docs/access?context=config-aia-notifications&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Configure alert email notifications for unexpected or undesired behavior from AI agents and agentic workflows. You can configure the thresholds for triggering the alerts on the Agent Properties table, and you can add or update the recipients of the email notifications from the Notifications table.

-   **[Create an external AI agent](https://www.servicenow.com/docs/access?context=create-external-aia&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Create new external AI agents that connect to third-party agentic AI systems. Use Agent2Agent protocol or integrate agents manually to configure them in AI Agent Studio to use in the ServiceNow agentic AI system.

-   **[Add a Knowledge Graph to an AI agent](https://www.servicenow.com/docs/access?context=add-knowledge-graph&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Use Enterprise Graph \(Small\) as a resource to create a Knowledge Graph tool for an AI agent in the AI Agent Studio.


-   **[AI Agent Studio](https://www.servicenow.com/docs/access?context=ai-agent-studio&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

View and troubleshoot the agentic workflow and AI agent executions on AI Agent Studio.

-   **[Configuring Now Assist AI agents](https://www.servicenow.com/docs/access?context=configuring-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) - Dynamic Orchestrator**

Maps the right agents for an agentic workflow with Dynamic Orchestrator for better performance and accuracy of the agentic workflow execution.

-   **[View analytics for customer satisfaction with AI interactions](https://www.servicenow.com/docs/access?context=ai-agent-dashboard&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Multiple new metrics have been added to the AI Agent Analytics dashboard, accessible from the AI Agent Studio to provide insight into average customer satisfaction and customer satisfaction with the best and worst performing agentic workflows and agents.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[Add tools and information to an AI agent](https://www.servicenow.com/docs/access?context=add-tool-aia&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

The output transformation strategy for an AI agent output now contains a new option called **Custom**.

With Custom output transformation strategy, a **Transformation Instructions** field with a text area is enabled for the user to provide their specific instructions for refining the output as per the agentic workflow. The instructions will also ensure that the transformation is done as per the user's need.

-   **[Configuring Now Assist AI agents](https://www.servicenow.com/docs/access?context=configuring-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) - AI Agent Background Channel**

Invoke the agentic conversations from the Workspace or Core UI via the AI Agent Background channel, that is associated with the AI Agent Background Provider, to execute the AI agents and agentic workflows.

-   **[Configuring Now Assist AI agents](https://www.servicenow.com/docs/access?context=configuring-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) - Interactive and non interactive AI agents**

Run AI agents and agentic workflows execution in one of the following ways:

    -   **Interactive Mode**: AI agents reach out to the user for information during fallback.
    -   **Non interactive Mode**: AI agents do not reach out to the user during fallback but send the execution output to the user.

-   **[Select Virtual Agent as a display option for AI agents](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Choose to display AI agent output in Virtual Agent. You can also discover AI agents in Virtual Agent conversations.

-   **[Disable citations in AI Agent Studio](https://www.servicenow.com/docs/access?context=aia-hide-citations&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Disable citations for specific agentic workflows or AI agents in AI Agent Studio where citations are not required or involve confidential information.

-   **[Create an AI agent](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**
    -   **Long term memory**: Add or delete categories for AI agents to store and retrieve memories.
    -   Additional tools available while creating an AI agent.
        -   Knowledge graph
        -   File retrieval
-   **[Evaluate agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=execute-aia-eval&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

In Now Assist Skill Kit, you can execute evaluation runs for your agentic workflows. You can select evaluation plans and the execution log datasets to judge whether your agentic workflows are consistently completing tasks and using the correct tools.


-   **[Create an AI agent](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Create an AI agent to assist your live agents while resolving cases, incidents, or tasks:

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
-   **[Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Create an agentic workflow with an execution plan to solve complex tasks with Now Assist. You can also do the following tasks:

    -   Clone an existing agentic workflow to avoid manual configuration.
    -   Create triggers when creating an agentic workflow that calls the AI agent when a condition or objective is observed.
    -   Test an agentic workflow before execution.
    -   Resolve record-based cases with AI agents.
-   **[Enable Now Assist Guardian in AI agents](https://www.servicenow.com/docs/access?context=enable-aia-na-guardian&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Enable Now Assist Guardian in AI agents to automatically identify and block offensive messages that are sent by human agents.

-   **[Multiple conversations in Now Assist AI agents](https://www.servicenow.com/docs/access?context=multiple-conversations-aia&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Enable live agents to interact with multiple AI agent conversations through the Now Assist panel.

-   **[AI Agent Analytics dashboard](https://www.servicenow.com/docs/access?context=ai-agent-dashboard&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Analyze the performance, efficiency gain, and usage of AI agents through preconfigured dashboards.


</td></tr><tr><td>

Now Assist Analytics

</td><td>

-   **[Usage and adoption](https://www.servicenow.com/docs/access?context=usage-and-adoption&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Monitor key usage and adoption indicators of your Now Assist implementation.

-   **[Custom skill details](https://www.servicenow.com/docs/access?context=custom-skill-details&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

View usage and performance indicators of custom skills from the predefined custom skills dashboard page.

-   **[Now Assist Guardian analytics](https://www.servicenow.com/docs/access?context=now-assist-guardian&version=yokohama&pubname=yokohama-intelligent-experiences&section=now-assist-guardian-analytics&ft:locale=en-US)**

Monitor the performance of guardrails enabled through Now Assist Guardian.

-   **[User search analyzer](https://www.servicenow.com/docs/access?context=user-search-analyser&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Gain insights into the search performance in Now Assist self-service experiences like Now Assist in Virtual Agent.

-   **[Now Assist context menu analytics](https://www.servicenow.com/docs/access?context=now-assist-context-menu-analytics&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).**

Monitor the usage and performance of Now Assist context menu actions.

-   **[Now Assist value insights](https://www.servicenow.com/docs/access?context=now-assist-value-insights&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Track the estimated efficiency and productivity gains enabled through Now Assist.


</td></tr><tr><td>

Now Assist Skill Kit

</td><td>

-   **[New skill deployment option](https://www.servicenow.com/docs/access?context=configure-skill-settings&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Deploy skills using UI Builder.

-   **[Choose a language for data generation](https://www.servicenow.com/docs/access?context=na-data-kit-generate-data&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

When you create synthetic data, you can select what language you want to receive the data in.

-   **[AI-assisted ground truth](https://www.servicenow.com/docs/access?context=add-ground-truth&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Use AI to assist creating ground truth for your data.

-   **[Import data with a CSV file](https://www.servicenow.com/docs/access?context=add-dataset&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Import data from a CSV file to create a dataset.

-   **[Create a custom data generator](https://www.servicenow.com/docs/access?context=create-custom-data-generator&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Create and use a custom data generator to create synthetic data.


-   **[Customize ServiceNow skills in Now Assist Skill Kit to tailor skills to meet your specific business requirements.](https://www.servicenow.com/docs/access?context=clone-and-edit-servicenow-skill&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Eligible skills provided in ServiceNow Now Assist applications can be cloned in Now Assist Skill Kit so that you can edit the prompt or change the AI service provider. Editing the prompt enables you to arrange the formatting and content of the large language model \(LLM\) response. After the skill is edited, activate the edited skill in the Now Assist Admin console to enable it.

-   **[Add and manage tools visually in the new Tools editor, including decision branching, to execute different tools for your skill.](https://www.servicenow.com/docs/access?context=add-a-tool&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Adding decision branches between tools enables you to define the conditions that must be met for a tool to run. If no conditions are met, the default branch's step is executed.


</td></tr><tr><td>

Now Assist for App Engine

</td><td>

-   **[Create an AI agent](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Create a custom AI agent in AI Agent Studio to assist your application users with their tasks.

-   **[Create a skill](https://www.servicenow.com/docs/access?context=create-new-skill&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Create a custom skill for Now Assist, enabling you to have greater flexibility with the generative AI capabilities available on the ServiceNow AI Platform.


</td></tr><tr><td>

Now Assist for Collaborative Work Management

</td><td>

-   **[Generate tasks from Docs in Collaborative Work Management \(CWM\)](https://www.servicenow.com/docs/access?context=generate-tasks-cwm-docs-now-assist&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Help increase efficiency and save time by using Now Assist to automatically generate CWM Tasks for your Board. Using the information in your doc, Now Assist provides task recommendations. You can choose to refine or modify these recommendations. You can iterate multiple times to tweak the task recommendations according to your requirements.

After you're satisfied with the recommendations, Now Assist can help you add these tasks to a board of your choice.

-   **[Summarize and paraphrase Docs content](https://www.servicenow.com/docs/access?context=cwm-docs&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US#section_ucs_wn1_hdc)**

Use Now Assist capabilities to refine selected content in docs, or to get a summary of the whole document.

    -   Summarize, elaborate, or shorten selected text.
    -   Summarize the entire content on the page.

</td></tr><tr><td>

Now Assist for Configuration Management Database \(CMDB\)

</td><td>

-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[Preview deduplication template results](https://www.servicenow.com/docs/access?context=now-assist-cmdb-mng-dupe-cis-skill&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US#li-preview-template-results)**

While you're working in the manage duplicate CIs skill, select **Review existing templates** to help you to decide which deduplication template to apply. Now Assist generates a summary of the results of applying a template without actually running the remediation process. You can preview the results for any existing template. When you see the desired result in a preview, you can specify that template and proceed with the deduplication process.


</td></tr><tr><td>

Now Assist for Creator

</td><td>

-   **[Build Agent, an autonomous AI agent for ServiceNow application development](https://www.servicenow.com/docs/access?context=build-agent&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Build Agent, located in a chat panel within the ServiceNow IDE, functions as an autonomous AI agent capable of independently generating a complete ServiceNow application. It can handle various code-related tasks, such as rewriting tables, explaining code, validating and improving existing applications, fixing application errors, and more.

-   **[Generate catalog items conversationally with Now Assist in Catalog Builder](https://www.servicenow.com/docs/access?context=create-catalog-item-using-now-assist&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

Create catalog items and record producers efficiently using the conversational interface within Catalog Builder. Communicate your requirements and specifications for your desired catalog items through guided conversation. Now Assist for catalog generation helps to simplify and streamline the catalog item creation process.


-   **[New third-party AI model provider options available for Now Assist](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Google Gemini 2.0 Flash, Google Gemini 2.5 Pro, and AWS Claude 3.7 Sonnet are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI GPT-4.1 and GPT-4.1 mini.

**Note:** Additional AI model providers are supported for the following Now Assist for Creator skills:

    -   App generation
    -   App summarization
    -   Catalog item generation
    -   Code generation
    -   Flow generation
    -   Flow summarization
    -   Playbook generation
    -   Process Mining
    -   RPA bot generation
    -   Spoke generation
    -   Test generation

-   **[Add columns to existing tables with Now Assist for app generation](https://www.servicenow.com/docs/access?context=sns-app-gen-review-apps&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Add columns to existing tables in Now Assist for app generation.

-   **[Add flows in Now Assist for app generation](https://www.servicenow.com/docs/access?context=sns-app-gen-add-flow&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Create a flow when creating an application in Now Assist for app generation. Enhance an existing application by adding a flow.

-   **[Add workspaces in Now Assist for app generation](https://www.servicenow.com/docs/access?context=sns-app-gen-add-workspace&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Create a workspace when creating an application in Now Assist for app generation. Enhance an existing application by adding a workspace.

-   **[Configure an event handler with Now Assist](https://www.servicenow.com/docs/access?context=configure-an-event-handler-with-now-assist&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Use Now Assist in UI Builder to configure event handlers. At present, you can configure links to a destination, open or close modals, and view load requested event handlers using Now Assist in UI Builder.

-   **[Create a flow or subflow from an image](https://www.servicenow.com/docs/access?context=exploring-flow-generation-with-images&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

Create a flow or a subflow from an image by using Now Assist. Capture the detailed process in an image and attach the image to Workflow Studio. Now Assist generates a preview of the flow that you can modify and regenerate.

-   **[Enable Code Explain and Summarize](https://www.servicenow.com/docs/access?context=enable-code-explain-and-summarize&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Support Code Explain and Code Summarize features with the Now LLM Service. Ensure compliance with any regional restrictions and help APAC users who may face limitations with US-based models.

-   **[Summarize client scripts](https://www.servicenow.com/docs/access?context=client-script-summarization-generation&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Use client script summary generation to get both a high-level summary and a detailed explanation of the client scripts.

-   **[Summarize a flow or subflow](https://www.servicenow.com/docs/access?context=flow-summarization&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

Summarize what a flow or subflow does by using generative AI.

-   **[Support additional components in the RPA Bot generation skill](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1808191)**

Support 97 additional components with Now Assist for RPA Hub.

-   **[Support Retrieval Augmented Generation \(RAG\) with playbook generation](https://www.servicenow.com/docs/access?context=playbook-assist&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

Generate playbooks from inputs that refer to custom actions, flows, subflows, content from installed spokes, or activity definitions. Include the names of commonly used and recently published actions, subflows, flows, and activity definitions that are available on your instance in your playbook generation requests.

-   **[Time out long running app summaries](https://www.servicenow.com/docs/access?context=sns-now-assist-app-summarize-landing&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Time out app summary generation after two minutes.

-   **[Use the Now LLM Service with Now Assist for app generation](https://www.servicenow.com/docs/access?context=sns-exploring-now-assist-gen&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Choose Now LLM Service or OpenAI GPT-4o to ensure compliance with any regional restrictions. This feature is helpful for APAC users who may face limitations with US-based models, such as GPT-4.0.


-   **[Create applications in ServiceNow Studio by using Now Assist with the guided app creator role](https://www.servicenow.com/docs/access?context=sns-app-gen-using-landing&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Enable your users with the guided app creator role \(in addition to users with the admin role\) to create applications with the Now Assist for app generation skill.

-   **[Create and edit automations and activities and extend automation logic flow in RPA Desktop Design Studio by using Now Assist](https://www.servicenow.com/docs/access?context=rpa-now-assist-studio&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

Use the Robotic Process Automation \(RPA\) bot generation skill in RPA Desktop Design Studio to create and edit automations and activities through short text instructions and preview options. This feature helps you to accelerate automation development because new and existing users can develop and build faster automations.

Enhance the automation logic by using the **Build automation** option, starting from components or from an empty design surface that is based on text instructions.

-   **[Summarize an app in ServiceNow Studio](https://www.servicenow.com/docs/access?context=sns-now-assist-app-summarize-landing&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Use the new Now Assist for app summary generation skill to quickly generate a summary of an app. You can then copy the summary to the app description, and then use the summaries to find duplicate or redundant apps.

-   **[Generate and edit automated tests faster by using the Test generation skill](https://www.servicenow.com/docs/access?context=test-generation-intro&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Use the new Test generation skill to generate automated tests faster by simply describing your test requirements. Review the generated test, make edits directly, or refine your original prompt to generate a revised version of the test.


</td></tr><tr><td>

Now Assist for Customer Service Management \(CSM\)

</td><td>

-   **[Enabled the is\_template property](https://www.servicenow.com/docs/access?context=clone-the-now-assist-for-csm-skills&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Enabled the is\_template property for all Now Assist skills to ensure consistent cloning. Added the ability to clone any base system GenAI skill and customize it in the Now Assist Skill Kit \(NASK\) to reduce setup time and simplify skill modification. Applies to all Now Assist for CSM skills.

-   **Access Sentiment analysis dashboard in Core UI**

Defined the navigation path in Sentiment Analysis dashboard in the Core UI interface to make it easier for users to locate and access sentiment analysis data without searching through multiple menus.

-   **[Sentiment trends analysis dashboard](https://www.servicenow.com/docs/access?context=use-sentiment-analysis-dashboard&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Get a comprehensive view of customer sentiment across case. The dashboard uses LLM-powered insights to explain sentiment changes and lets you drill down to find root causes and real time insights—helping managers take targeted actions.

-   **[Trending topics dashboard](https://www.servicenow.com/docs/access?context=view-trending-topics-dashboard&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Get a comprehensive view of trending topics across cases along with insights and visualizations to facilitate deeper analysis. This feature helps support teams track trend progression, regional impact, and drill down into specific trends using customizable filters.

-   **[Provide customer 360 insights agentic workflow](https://www.servicenow.com/docs/access?context=customer-service-management-ai-agent-collection-customer-360&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Use the provide customer 360 insights agentic workflow to provide synthesized and relevant customer insights to live agents via conversations. This agentic workflow is designed to support human agents by responding to natural language queries regarding cases, customer history, products, and interactions. This feature expedites access to vital information and case resolution, identifies patterns, and leverages past similar cases for guidance as well as triggers actions from the Now Assist panel.

-   **[Activity response generation skill](https://www.servicenow.com/docs/access?context=generate-a-recommendation-to-respond-to-an-activity&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Use the activity response generation skill to automatically generate recommendations for resolution notes, work notes, and comments. This feature helps agents add meaningful updates to case records, improving efficiency, and interaction.

-   **[Now Assist context menu configuration for extended tables within resolution notes](https://www.servicenow.com/docs/access?context=customize-now-assist-context-menu-for-skills&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Configure output fields for resolution notes through the Now Assist context menu configuration page so skills apply to extended tables without any additional setup.


-   **[Triage cases agentic workflow security directives](https://www.servicenow.com/docs/access?context=case-resolving-use-case&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Implement security on AI agents and agentic workflows through ACLs and user identities.

-   **[Now Assist for CSM Gen AI security directives](https://www.servicenow.com/docs/access?context=configure-chat-summarization-in-now-assist_0&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Implement security in Now Assist for CSM skills through ACLs and user identities.


[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   **[Sentiment analysis on a case](https://www.servicenow.com/docs/access?context=analyze-sentiments-in-now-assist-for-csm&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Make informed decisions on cases that are based on your requester’s sentiment and the reasoning behind it. You can update the sentiment when new comments or emails from your customers come in to ensure that the sentiment is always up to date​.

-   **Sentiment analysis on an account**

Track the sentiment of a business-to-business account and analyze it by using various filters and sorting dashboards. You can get the right insights and reduce the number of escalated cases.

-   **[Suggested steps in Recommended Actions](https://www.servicenow.com/docs/access?context=suggested-steps-generation-in-now-assist-for-customer-service-management-csm&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Use Recommended Actions to generate suggested resolution steps for cases. You can increase agent productivity by outlining the next best actions for unfamiliar cases and automatically providing logical next steps.

-   **[Support for conversational subflows and actions in the Now Assist panel](https://www.servicenow.com/docs/access?context=request-gen-ai-capabilities-csm-now-assist-panel&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Use natural language to describe your intent to trigger a subflow or action. This feature helps to improve your agent productivity and enables them to accomplish everything in one place within the Now Assist panel.

-   **[External web content in Q&amp;A Genius Results](https://www.servicenow.com/docs/access?context=using-ai-search-with-q-a-within-the-portal-form&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Provide the support for your public web content so that your requesters can use search queries in both standard search and conversational search. You can also see whether the content is internal or external, with direct links to the source.

-   **[Troubleshooting steps identification AI agent](https://www.servicenow.com/docs/access?context=troubleshooting-steps-identification-ai-agent&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Gather context from cases, identify missed fixes, and troubleshoot potential solutions by using the Troubleshooting steps identification AI agent.


[Yokohama Patch 1](../quality/yokohama-patch-1.md)

-   **[Triage cases AI agents use case](https://www.servicenow.com/docs/access?context=csm-ai-agents-use-cases&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Use the Triage cases AI agents use case to improve agent productivity through faster assessment.

    |AI agent use case|Description|
    |-----------------|-----------|
    |Triage cases|Use AI agents to handle all routine cases coming in through email and other offline channels, so that it improves customer satisfaction and reduces resolution times.|


Yokohama Early Availability

-   **[Conversational search in the Now Assist panel with results from knowledge articles](https://www.servicenow.com/docs/access?context=using-conversational-search-in-now-assist-panel&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Ask questions directly within the Now Assist panel. If the answer is found in the knowledge bases \(KBs\), the answer is shown with the source information. If the answer isn't available in the KB search, you’re redirected to the global search experience for further assistance.

-   **[Now Assist in Virtual Agent-Scheduling Assistant via GenAI](https://www.servicenow.com/docs/access?context=using-scheduling-assistant-via-genai-in-virtual-agent&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Use the enhanced scheduling assistant with Now LLM Service capabilities to make it more conversational, enabling users to easily schedule, reschedule, and cancel appointments.

-   **[Now Assist in portal case form](https://www.servicenow.com/docs/access?context=using-ai-search-with-q-a-within-the-portal-form&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Guide requesters through a self-service flow to find solutions to their problems by using Genius Results. You can reduce the number of cases created and decrease the effort required by your agents to close open cases.


</td></tr><tr><td>

Now Assist for Enterprise Architecture \(EA\)

</td><td>

-   **Yokohama Patch 1 [Using Enterprise Architecture Diagramming AI agent](https://www.servicenow.com/docs/access?context=using-na-ea-ai-agents&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

Use the Enterprise architecture diagrams AI agent to create Enterprise Modeling and Visualization diagrams for business applications hierarchy and summarize them.

-   **Yokohama Early Availability [Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=now-assist-ea&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
    -   Use the ServiceNow® Now Assist for Enterprise Architecture \(EA\) application to summarize Architectural Decision Records \(ADR\) in the Enterprise Architecture Workspace. Use the Architectural Decision Records \(ADR\) to explain your infrastructure. ADR is a type of artifact that helps you to understand the background of a specific architectural decision.
    -   Register a business application and a digital integration with an interactive generative AI experience using Now Assist in Virtual Agent. For more information, see [Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=now-assist-ea&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US).

</td></tr><tr><td>

Now Assist for Field Service Management \(FSM\)

</td><td>

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[Custom template and custom prompt support](https://www.servicenow.com/docs/access?context=customize-a-skill&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

As an admin, you can clone the KB generation skill and customize the input fields. You can also clone the Work order task summarization skill, then access the skill in the Now Assist skill kit, and update the prompts.


-   **[Create an Assistant for Field Service Management](https://www.servicenow.com/docs/access?context=activate-virtual-agent-for-field-service-management&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US) to do the following:**
    -   Initiate the Now Assist panel from a work order task record or the **My tasks** tab.
    -   Provide technicians with a consistent and intuitive interface for quick and effortless interaction.
    -   Display a summary of work order tasks.
-   **[Use conversational search for technician support](https://www.servicenow.com/docs/access?context=use-conversational-search-for-technician-support&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US) to do the following:**
    -   Enable technicians to ask questions in natural language for quick and clear answers.
    -   Enable technicians to receive accurate and reliable responses sourced exclusively from the Knowledge Base.
    -   Provide technicians with context-aware follow-ups, including related parts or steps, for better support.

</td></tr><tr><td>

Now Assist for Financial Services Operations \(FSO\)

</td><td>

-   **[Long term stable models](https://www.servicenow.com/docs/access?context=long-term-stable-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.


-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[ACL security implementation](https://www.servicenow.com/docs/access?context=configuring-now-assist-skills-for-fso&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US)**

Enable security implementation to execute AI agents, agentic workflows, and generative AI skills through ACLs and user identities in Now Assist for FSO.

Predefined ACLs are provided for case summarization, Disputes intake via Virtual Agent, and the Help resolve friendly fraud AI agent and agentic workflow.


-   **[Using agentic workflows in Now Assist for Financial Services Operations \(FSO\)](https://www.servicenow.com/docs/access?context=using-ai-agent-use-cases-in-now-assist-for-fso&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US)**

Resolve disputes that are flagged as friendly fraud with comprehensive guidance from the friendly fraud AI agent. Leverage the AI agent's step-by-step recommendations and detailed responses to explain the decisions made regarding disputes. Based on the AI agent recommendations, issue credit to customers, decline disputes, or initiate an exception process.


-   **[Disputes intake via Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-for-financial-services-operations&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US)**

Provide an intuitive dialog-based channel experience for your customers to submit details on a dispute case. The dispute intake via Virtual Agent leverages questions that are required by the card processing networks. Now LLM Service rephrases these questions in a conversational format and infers the answers for the unanswered questions from customer responses.


</td></tr><tr><td>

Now Assist for HR Service Delivery \(HRSD\)

</td><td>

Yokohama Patch 6

-   **[Resolve HR cases agentic workflow](https://www.servicenow.com/docs/access?context=employee-issue-resolver-na&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Generate a step-wise fulfillment plan for an HR case by selecting the **Generate Plan** button on the HR Case. HR agents can add prompts to further refine the AI generated fulfillment plan before the plan is published to the work notes of the case.


-   **[Growth Conversations agentic workflow](https://www.servicenow.com/docs/access?context=agentic-wf-conversations-na-td&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Use the new growth conversations workflow to streamline your employee growth discussions in Career Conversations.


-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


-   **[Generate a knowledge article from HR Agent Workspace with Now Assist](https://www.servicenow.com/docs/access?context=gen-kb-now-assisthr&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Create a copy of the KB generation skill to create custom templates that are based on your organization's requirements. When a skill copy is activated, the main skill is automatically deactivated.


-   **[Generate an email reply recommendation by using Now Assist for HR Service Delivery \(HRSD\)](https://www.servicenow.com/docs/access?context=email-recommendation-nahr&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

View the list of KB articles, related records, and current records that are used to generate email reply recommendations.

-   **[Generate onboarding ramp-up plan agentic workflow](https://www.servicenow.com/docs/access?context=onboarding-ramp-up-plan-agentic-wf&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Simplify employee onboarding with AI agents that gather inputs, structure tasks, enable manager review, and deliver personalized onboarding plans.


Yokohama Patch 3

-   **[Resolve HR cases agentic workflow](https://www.servicenow.com/docs/access?context=employee-issue-resolver-na&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Use the Resolve noncritical HR cases agentic workflow for faster mean time to repair \(MTTR\) cases, automate the resolution of routine employee inquiries, and reduce the costs for HR operations organizers.

    |Agentic workflow|Description|
    |----------------|-----------|
    |Resolve noncritical HR cases|AI agents detect criticality and retrieve relevant knowledge-based responses to automate the resolution of employee queries.|

-   **[Access knowledge from internal and external content sources](https://www.servicenow.com/docs/access?context=explore-now-assist-hr&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Find reliable answers to HR management queries from multiple data sources, including the research and articles from The Josh Bersin Company, with attribution to each source.

-   **[Override sensitivity detection false positives](https://www.servicenow.com/docs/access?context=explore-now-assist-hr&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Proceed with the interaction when the virtual agent incorrectly identifies a phrase as containing sensitive information.

-   **[Create a growth conversation with the help of an agent in Now Assist](https://www.servicenow.com/docs/access?context=agentic-wf-conversations-na-td&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

As a manager, use the growth conversations preparation AI agent to schedule and prepare for employee growth discussions. The agent provides a clear summary of employee activity and career journey, with data-driven talking points to make conversations more focused and impactful.

**Note:** This feature is available when you have both Now Assist for HR Service Delivery \(HRSD\), which will install Now Assist for Talent and HR Talent AI Agent Collection


Yokohama Patch 1

-   **[Help resolve tuition requests agentic workflow for Now Assist for HRSD](https://www.servicenow.com/docs/access?context=now-assist-hrsd-ai-agents-policy-resolving-tr-usecase&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Use the Resolve policy use case for faster mean time to repair \(MTTR\) cases that require validation that is based on the policies that are built for tuition reimbursement.

    |AI agent use case|Description|
    |-----------------|-----------|
    |Resolve policy for tuition reimbursement|AI agents resolve tuition reimbursement requests by connecting to various parties \(for example, the manager for approval\) and resolving the case, while keeping the human agent in the loop.|


Yokohama Early Availability

-   **[Now Assist for HRSD Virtual Agent topics](https://www.servicenow.com/docs/access?context=now-assist-ohcm&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Use the [Now Assist for HR Service Delivery \(HRSD\)](https://www.servicenow.com/docs/access?context=now-assist-hrsd&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) Virtual Agent topics to place employee requests in the HCM system. Examples of requests are when an employee requests time off or updates their personal details.

-   **[Use Knowledge Graph in Now Assist for HRSD](https://www.servicenow.com/docs/access?context=na-kb-graph&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Create and manage personalized knowledge models as Knowledge Graph schemas that are represented as nodes, edges, and their properties. Virtual Agent uses the assigned Knowledge Graph schema to resolve employee requests and queries.

-   **[Create a journey using Now Assist](https://www.servicenow.com/docs/access?context=create-journey-na&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Create Journey Accelerator plans by entering prompts to Virtual Agent without having to manually create lists and forms.


</td></tr><tr><td>

Now Assist for Hardware Asset Management \(HAM\)

</td><td>

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   **[Optimize hardware asset repair process with the suite of AI agents](https://www.servicenow.com/docs/access?context=now-assist-ham-repair-agent-workflow&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Automate the repair of defective and out-of-warranty hardware assets by using AI agents in the Help repair hardware assets agentic workflow. These AI agents validate the repair tasks, provide detailed troubleshooting and repair instructions, and complete the tasks on receiving user confirmation.


-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Configure the Access Control Lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


[Yokohama Patch 4](../quality/yokohama-patch-4.md)

-   **[Optimize hardware asset sourcing with the suite of AI agents](https://www.servicenow.com/docs/access?context=now-assist-ham-agentic-workflow&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Automate your hardware asset sourcing by using AI agents in the Help manage hardware asset requests agentic workflow. These AI agents can efficiently handle tasks such as automatically consuming assets from local stock, creating transfer orders, and generating purchase orders. By automating complex and repetitive tasks in the hardware asset request process, AI agents help to reduce manual intervention significantly, speed up request resolution, enhance the productivity of asset managers, and improve operational efficiency.


</td></tr><tr><td>

Now Assist for IT Operations Management \(ITOM\)

</td><td>

-   **[Enhance IT operations with AI-driven, autonomous alert management using the manage alerts autonomously workflow](https://www.servicenow.com/docs/access?context=itom-autonomous-operator-workflow&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Automate alert triage, impact analysis, and root cause investigation with an AI-driven workflow that replaces manual operator steps with autonomous decision-making. The workflow processes incoming alerts end-to-end and surfaces consolidated insights through Express List, giving operators immediate visibility into what happened, what's affected, and why.

-   **[Configure the Datadog and Gemini Cloud Assistant observability skills](https://www.servicenow.com/docs/access?context=itom-ai-agent-configuration&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Set up the new Datadog and Gemini Cloud Assistant observability skills to get insights from those tools in the manage alerts autonomously agentic workflow. With Datadog and Google Gemini, the workflow now supports five observability tools, including Dynatrace, Kentik, and New Relic, helping you investigate and respond to a wider range of alerts.


-   **[Configure the Dynatrace analysis AI agent](https://www.servicenow.com/docs/access?context=now-assist-itom-config-dynatrace&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Set up the Dynatrace analysis AI agent in the Analyze alert impact agentic workflow to investigate Dynatrace alerts. With Dynatrace, the agentic workflow now supports three observability tools, including Kentik and New Relic, helping you investigate and respond to a wider range of alerts.

-   **[Expand the Analyze alert impact agentic workflow with four new AIOps agents](https://www.servicenow.com/docs/access?context=now-assist-itom-use-aia&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Get a fuller view of alert impact with four new AIOps agents in the Analyze alert impact agentic workflow. Along with observability data, the agentic workflow now includes information from within ServiceNow to help surface business impact and related issues. Activate the AIOps agents to include them in the agentic workflow.

-   **[Enhance your decision-making process with the Analyze Potential Impact agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itom-analyze-potential-impact-workflow&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Assess the potential impact of a change using the Analyze Potential Impact agentic workflow. This workflow provides an analysis of the relevant servers and suggested services that might be impacted by your change request, ensuring you have all the insights needed to make informed decision before a change.

-   **[Add access control lists for security in AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Enable security settings to run AI agents and agentic workflows using ACLs and user identities. You can configure and manage the ACLs in AI Agent Studio.

-   **[Utilize the Triage and analyze alerts agentic workflow in the context of an incident](https://www.servicenow.com/docs/access?context=itom-alert-triage-agentic-workflow&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Initiate the Triage and analyze alerts agentic workflow from the Now Assist panel in the context of the incident form to perform all the functions of the workflow. This workflow automatically assigns, acknowledges, and summarizes origin alerts, determines their significance through historical analysis, and analyzes related incidents.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


-   **[Analyze alert impact agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itom-agentic-aia&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Analyze the impact of alerts and identify the possible causes with the Analyze alert impact agentic workflow. The workflow interacts with observability tools, such as Kentik and New Relic, to surface alert details and provide insights.

-   **[Now Assist for IT Operations Management \(ITOM\) Triage and analyze alert agentic workflow](https://www.servicenow.com/docs/access?context=itom-alert-triage-agentic-workflow&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Automatically assign, acknowledge, and summarize the alerts, determine their significance through history analysis, and analyze the related incidents. Initiate multiple parallel processes to triage and analyze the different alerts.


</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

-   **[Adding self-service and deflection to phone channels using Voice AI agents](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Enhance employee productivity with Voice AI agents by adding self-service and deflection to their phone channel.

-   **[Getting password reset instructions using an AI agent](https://www.servicenow.com/docs/access?context=itsm-va-ai-agents&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

The **DEMO Password reset agent** is a demo AI agent that provides requesters with password reset instructions for the account that they need help with.

-   **[Editing the incident summarization skill prompts and inputs using the Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-record-summ-skill&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

You can edit the prompts and inputs for the incident summarization skill within the Now Assist Skill Kit \(NASK\) and test the updates you've made.

-   **[Expanding attachment summarization capabilities to include additional document formats and language](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-record-summ-skill&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

You can now summarize, analyze, and extract data from attachments in additional formats and languages.

-   **[Enhancing the efficiency of the Investigate and resolve ITSM incidents agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-incident-resolver-workflow&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

For better efficiency, the ITSM incident resolution investigation AI agent and Find catalog item AI agent have been combined into one agent. This agent is called the ITSM incident resolution plan investigation AI agent.

-   **[Enhancing the efficiency of the Triage and categorize ITSM incidents agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-catincidents-usecase&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

For better efficiency, the Link major incident AI agent and the Link incident to problem AI agent have been combined into one agent. This agent is called the Link major incident or problem AI agent.

-   **[Enhancing the efficiency of the Generate change request plans agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-change-planner-usecase&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

For better efficiency, the existing six agents in the change request plans agentic workflow have been combined into one agent. This agent is called the Change request plans AI agent.

-   **[Display the risk factors sources that contribute to the calculation of a change risk explanation](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-change-risk-skill&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

When a change risk is calculated, Now Assist for ITSM provides the list of the change requests that were used to identify the potential risks for the change risk explanation so that you can understand which risk factors contributed to the calculated risk.

-   **[Generating resolution notes using the Now Assist context menu](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-gen-resolution-notes-skill&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

As an admin, you can view and configure the Now Assist context menu \(NACM\) to generate resolution notes using the **Resolution notes generation** skill.

-   **[Generating an activity response using the Now Assist context menu](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-activity-response-skill&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

As an admin, you can view and configure the Now Assist context menu \(NACM\) for an activity response using the **Incident activity response generation** skill.

-   **[Masking roles for controlled access to agentic workflows, AI agents, and skills](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-itsm&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Mask roles to restrict access to agentic workflows, AI Agents, and skills, ensuring that users receive only the necessary permissions.

-   **[Suggest configuration items for a change request agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-suggest-configuration-items-for-a-change-request&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Find and link applicable configuration items \(CIs\) to a change request from the Now Assist panel in a conversational and intuitive way using the Suggest configuration items for a change request agentic workflow.

-   **[Create outages for a change request agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-create-outages-for-a-change-request&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Associate outages with a change request in a conversational and intuitive way from the Now Assist panel using the Create outages for a change request agentic workflow.

-   **[Create standard change request agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-create-change-request-workflow&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Create a standard, normal, or emergency change request in a conversational and intuitive way from the Now Assist panel using the Create standard change request agentic workflow.

-   **[Create standard change template proposal agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-create-standard-change-template-proposal&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Create a change template proposal record based on similar change requests in a conversational and intuitive way from the Now Assist panel using the Create standard change template proposal agentic workflow.

-   **[DEX issue diagnosis and resolution agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-dex-diagnosis-resolution-workflow&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Diagnose and resolve issues on DEX monitored devices through a structured process that includes diagnosis of the cause, a resolution plan with actionable steps, and documenting the resolution in the incident record.

-   **[Generate comprehensive release notes for a release in Digital Product Release](https://www.servicenow.com/docs/access?context=dpr-generate-release-notes&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Automatically generate structured release notes for a release using the Generate Release Notes skill. This AI-driven capability compiles enhancements, features, incidents, and change records into structured notes with an executive summary and scope of work sections, reducing manual effort and ensuring consistency. You can edit the AI-generated draft as needed, then publish and share via link or PDF download.


-   **[Classify service and CI AI agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-catincidents-usecase&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Automatically assign the related service, service offering, and configuration item \(CI\) to an incident using the Classify service and CI AI agent in the Triage and categorize ITSM incidents agentic workflow.

-   **[Setting the AI user as the Run as user in the Triage and categorize incidents agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-catincidents-usecase&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Create AI users for the identity type **AI agent** and assign roles to the AI user based on your needs. Run the agentic workflow as the AI user that determines the data access defined by the role.

-   **[Matching flow action access control roles with the agent roles for the Notify users with Twilio agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-twilio-text-usecase&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

When you update the agent role for the Notify users with Twilio agentic workflow, you must also update the corresponding access controls with those roles.

-   **[Matching flow action access control roles with the agent roles for the Manage Microsoft 365 group members agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-O365-groupmembers-workflow&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

When you update the agent role for the Manage Microsoft 365 group members agentic workflow, you must also update the corresponding access controls with those roles.

-   **[Using the itil role to add or update work notes in the Now Assist panel](https://www.servicenow.com/docs/access?context=request-gen-ai-capabilities-itsm-now-assist-panel&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

To add or update work notes in the Now Assist panel, the logged-in user must have the itil role.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[Editing prompts using the Now Assist skill kit](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-skill&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

As an admin, you can clone the following skills, then access the skill in the Now Assist skill kit, and update the prompts:

    -   Resolution notes generation skill
    -   Knowledge article generation skill
    -   Incident summarization skill
-   **[Prompt inputs for Major incident email content recommendation](https://www.servicenow.com/docs/access?context=now-assist-itsm-skills&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Use related tables and fields as prompt inputs to generate a Major incident email content recommendation.


-   **[Using IT Service Management AI agent collection](https://www.servicenow.com/docs/access?context=now-assist-itsm-ai-agents-use-cases&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Use the IT Service Management AI agent collection to boost productivity, and autonomously resolve business tasks.

    |Agentic workflows|Description|
    |-----------------|-----------|
    |Triage and categorize ITSM incidents|Identify the category, subcategory, and configuration item for an incident automatically, and link associated major incidents or known problems.|
    |Investigate and resolve ITSM incidents|Get recommendations to resolve an incident based on the incident number. Check for related catalog items, Knowledge articles, and similar resolved incidents to generate resolution steps for the incident.|
    |Manage Microsoft 365 group members|Add or remove groups and email distribution lists from the Microsoft 365 group.|

-   **[IT Service Management AI agent collection Generate change request plans agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-change-planner-usecase&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Use the following additional AI agents to handle change requests.

    |AI agent|Description|
    |--------|-----------|
    |Change risk and impact analysis AI agent|Analyzes the potential risk and impact of a change request.|
    |Change justification proposal AI agent|Proposes justification for a change request.|

-   **[Generate a Major Incident email content recommendation by using Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm-mim-email-recommendation&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Draft a communication for a major incident using an email template. You can fill in the template field values with an AI-generated response.

-   **[Generate comments and work notes using the Now Assist context menu](https://www.servicenow.com/docs/access?context=request-gen-ai-capabilities-itsm-now-assist-panel&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Enable your agents to generate comments and work notes quickly and add them to incidents using the Now Assist panel.

-   **[Incident sentiment and sentiment trend](https://www.servicenow.com/docs/access?context=now-assist-itsm-skills&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Make informed decisions on incidents by considering the requester's sentiments and the reasoning behind them.

-   **[Suggested steps generation in Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=resolution-steps-generation-now-assist-itsm&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Automatically generate suggested steps to resolve an incident by analyzing the solutions from clusters of similar resolved incidents.

-   **[Summarizing attachments in the Incident summarization skill](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-skill&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Summarize, analyze, and extract data from attachments that are of type PNG or JPEG using Document Intelligence in the Incident summarization skill.


-   **[Using IT Service Management AI agent collection](https://www.servicenow.com/docs/access?context=now-assist-itsm-ai-agents-use-cases&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Use the IT Service Management AI agent collection to boost productivity, and autonomously resolve business tasks.

<table id="table_gjc_gkw_g2c"><thead><tr><th>

AI agent use case

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Generate post incident reviews

</td><td>

Enhance IT productivity during major incidents by minimizing the time required to generate post-incident reviews using AI agents. This process helps improve communication and avoid outages​.**Important:** To enable the display of the Generate post incident reviews use case, you must activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\). For more information, see [Activate Incident Management - Major Incident Management](https://www.servicenow.com/docs/access?context=activate-major-incident-management-plugin&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

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

Send text messages via SMS to recipients manually using AI agents to help improve the time required for subject matter expert response.**Important:** To enable the display of the Notify users with Twilio use case, you must activate the Twilio Spoke plugin \(sn\_twilio\_spoke\). For more information, see [Twilio Spoke](https://www.servicenow.com/docs/access?context=twilio-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

</td></tr></tbody>
</table>
-   **[Using self service to deflect incidents in a ServiceNow portal by using Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=deflect-incidents-now-assist-itsm&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Designed to reduce the number of incidents to be resolved by deflecting issues with self-service.

-   **[Customizing a Now Assist for IT Service Management \(ITSM\) change risk skill](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-change-risk-skill&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Efficiently explain the risk of a change request by adding custom input fields to the following input tables:

    -   Change request
    -   Past similar change request
    -   Incident caused by change
-   **[Refining a change risk explanation response](https://www.servicenow.com/docs/access?context=change-risk-exp-now-assist&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Refine the explanation to a change risk by shortening or lengthening a response by using Now Assist for IT Service Management \(ITSM\).

-   **[Risk Assessment as input to calculate a change risk](https://www.servicenow.com/docs/access?context=change-risk-exp-now-assist&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Use risk assessment values as an input to explain the risk of a change request.

-   **[Generating an email response by using Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm-email-recommendation&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Get recommendations for email responses that agents can review and send to users. Agents can also get email template and content edit recommendations from Now Assist for IT Service Management \(ITSM\).

-   **[Monitoring task status using pre-built LLM topics with Now Assist in ITSM Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-customize-itsm-llm-topic&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Copy and customize a ITSM Virtual Agent core ITSM topic template to track the status of a task by using Now Assist in ITSM Virtual Agent.


</td></tr><tr><td>

Now Assist for Legal Service Delivery \(LSD\)

</td><td>

-   **[Now LLM LTS support for Now Assist for Legal Service Delivery \(LSD\)](https://www.servicenow.com/docs/access?context=now-llm-model-updates&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


</td></tr><tr><td>

Now Assist for Order Management

</td><td>

-   **[Enable the manage order operations agent in the Business Portal](https://www.servicenow.com/docs/access?context=enable-manage-order-operations-ai-agent&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

Activate the manage order operations agent so that you can make it available to your customers on the Business Portal.

-   **[Request order changes using Now Assist](https://www.servicenow.com/docs/access?context=request-order-changes-now-assist&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

Use the manage order operations agent to provide a seamless experience to your customers on the Business Portal, enabling them to create order cases using a virtual assistant effortlessly. The AI agent can intelligently categorize requests for expedited delivery by creating order-related cases linked directly to the specific order, significantly reducing manual case creation and speeding up resolution times. Interaction channels include chat and voice options.

-   **[Summarize an order using Summarization for Order Management](https://www.servicenow.com/docs/access?context=now-assist-order-mgmt-summarize-order&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

Generate a summary of a complex order for a unified view of the order's current state to:

    -   Respond confidently to customer queries with accurate, real-time order status.
    -   Track changes and validate details to maintain consistency and transparency.
    -   Minimize errors and improve communication across suppliers and partners.
    -   Monitor tasks that are at risk of missing deadlines.
    -   Assign tasks to appropriate resources based on priority and skill.
    -   Make rapid prioritization decisions to prevent delays and help ensure timely fulfilment.

</td></tr><tr><td>

Now Assist for Sales Force Automation \(SFA\)

</td><td>

-   **[Yokohama Patch 11](../quality/yokohama-patch-11.md)[Use agentic workflows in Now Assist for Sales Force Automation \(SFA\)](https://www.servicenow.com/docs/access?context=using-agentic-worklflows-in-lead-management&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

The Help nurture new leads agentic workflow works with a team of AI agents to assist the sales agents to manage the life cycle of leads, either independently or under supervision.

<table id="table_tbs_1xz_v2c"><thead><tr><th>

Workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Help nurture new leads

</td><td>

-   Outlines the steps required to engage the lead with the sales agent.
-   Sends initial outreach and follow-up emails.
-   Retrieves emails, classifies the intent, and routes it to the right sales agent to take action.
-   Schedules, reschedules, or deletes the appointments based on sales agent availability.
-   Manages the leads who want to opt out or uninterested.


</td><td>

-   Lead outreach AI agent
-   Inbound email AI agent
-   Appointment management AI agent
-   Lead disinterest AI agent


</td></tr></tbody>
</table>


</td></tr><tr><td>

Now Assist for Security Incident Response

</td><td>

-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add.

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Generate a quality assessment report](https://www.servicenow.com/docs/access?context=na-sir-quality-assessment&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Use generative AI to create a quality assessment report of a security incident. The reports are generated using a predefined, natural language rule set. The report provides an overall assessment summary followed by the detailed assessment for all the rules.


-   **[Generate SIR Shift Handover Report](https://www.servicenow.com/docs/access?context=add-incidents-shifthandover-ai-agent&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

The AI Agent helps add security incident details to a shift handover report. The agent populates the different sections of the shift handover with appropriate content by identifying the relevant details from the security incident. The AI agent can fetch details of the security incident and identify if the analyst has access to the shift handover record. The AI agent can generate content for each section of the shift handover record and asks for analysts feedback on the content. The AI agent refines the content based on the feedback and saves the content to the records on approval.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


-   **[Using AI agentic workflows in Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=using-now-assist-ai-agents-sir&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

The Analyze security operations metrics agentic workflow enables security managers to analyze their teams' performance.

    -   Generate metrics for Security Incident Response \(SIR\) records for case volume, mean time to assign \(MTTA\), and mean time to resolve \(MTTR\) for a date range of your choosing.
    -   Request suggestions for how to improve MTTR, MTTA, and volume based on your metrics.
-   **[Enhancements to correlation insights in Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=generating-insights-for-now-assist-for-security&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

You can generate and view results for correlation insights in the Security Incident Response Workspace.

    -   Correlation insights are not limited to the primary configuration item \(CI\) or affected users associated with a security incident. You can base your correlation insights on any CI or affected user for a security incident.
    -   You can generate correlation insights from the **Investigation** tab for a security incident in any state in the Security Incident Response Workspace.
    -   You can generate insights for multiple items simultaneously for Associated Observables, Configuration items, and Affected Users.
    -   Results are displayed in a modeless dialog that you can size and move.
-   **[Using Security incident resolution agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-sir-resolve-incident-ai-workflow&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Use the Security incident resolution agentic workflow to close your security incidents. Analysts can chat with the AI agents in natural language to resolve the security incidents. The AI agent analyzes the incident details, existing runbooks, knowledge articles, and past similar security incidents as inputs, and provides a resolution plan. The AI agent also assists the analysts to resolve the security incident.


-   **[Using Security Incident Response AI agents](https://www.servicenow.com/docs/access?context=using-now-assist-ai-agents-sir&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Yokohama Patch 1: Use the Close security incident use case to close your security incidents:

    -   Analysts can chat with the AI agents in natural language to close the security incidents. The AI agent can cancel the associated response tasks, generate resolution notes, close code, or close notes and post incident analysis \(PIA\) during incident closure. Analysts can provide feedback on the content and the AI agent can refine the content​ based on the feedback.
    -   Analysts can also close false positive security incidents with minimal user intervention.
-   **[Yokohama Early Availability](https://www.servicenow.com/docs/access?context=now-assist-security-incident-landing&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**
    -   [Generate correlation insights](https://www.servicenow.com/docs/access?context=generate-correlation-insights-now-assist-for-security&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)

Generate correlation insights to connect current security incidents to past events. You can identify the affected users, configuration items \(CI\)s, or observables \(IP addresses and file hashes\) from existing incidents and records to help you more quickly triage your new security incidents. Correlation insights are supported in Workspace, the Core UI, and from the Now Assist panel.

    -   Enhancements to [closure \(resolution\) notes](https://www.servicenow.com/docs/access?context=generate-closure-notes-si-now-assist-sec-incident&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US) and [post incident analysis](https://www.servicenow.com/docs/access?context=generate-pia-report-now-assist-security-incident&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US) generation

Generate resolution notes from the Close the security incident modal or the Now Assist context menu on a security incident record \(SIR\). You can also generate resolution notes from the Now Assist panel. If you choose the Now Assist context menu, you have the following options to help you refine the generated text:

        -   **Shorten**: Select the text to remove details.
        -   **Elaborate**: Generate more details about the context of a security incident.
**Note:** Generating resolution notes is supported in Workspace and Core UI. Generating a post incident analysis is supported from the Close the security incident modal in Workspace.


</td></tr><tr><td>

Now Assist for Software Asset Management \(SAM\)

</td><td>

-   **[Automate the creation of user resolution rules to accelerate reconciliation and ensure consistent user mappings](https://www.servicenow.com/docs/access?context=automate-userresolution-saas-now-assist-sam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Use generative AI to resolve user subscriptions by creating user resolution rules without manual intervention. AI automatically creates the user resolution rules, and these rules analyze and map incoming subscription data to corresponding user records in the Software Asset Management application.


-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[Use an agentic workflow to automate software asset sourcing to improve operational efficiency](https://www.servicenow.com/docs/access?context=using-now-assist-sam-ai-agents-usecases&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Use AI agents in the Help manage software request agentic workflow to automate sourcing of software assets either through automatic license allocation or by creating purchase orders.

-   **[Use an agentic workflow to create reclamation rules for enhancing software license utilization tracking and reducing waste](https://www.servicenow.com/docs/access?context=now-assist-sam-create-software-reclamation-rule-workflow&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Use AI agents to automatically create reclamation rules for installed or subscription-based software, reducing the need for manual analysis of product usage and expenditure. The AI agent analyzes factors such as spend and utilization to suggest reclamation rules.

-   **[Use an agentic workflow to reclaim unused software to minimize compliance risk and optimize savings](https://www.servicenow.com/docs/access?context=now-assist-sam-evaluate-removal-candidate-workflow&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Use AI agents to automate reclamation of removal candidate for an installed or subscription-based software. The AI agent evaluates software removal candidates and provides suggestions for reclamation, based on intelligent checks that help ensure safe removal.


-   **[Gain insights into product compliance and optimization with AI-powered product summaries](https://www.servicenow.com/docs/access?context=summarize-product-compliance-now-assist-sam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Get comprehensive product summaries to better understand your product compliance position across software deployment, license compliance, optimization, and configuration health. The AI-based product summaries simplify the complexity of license management and ensure adherence to publisher contracts.

-   **[Use AI-powered recommended actions to mitigate your license compliance risk](https://www.servicenow.com/docs/access?context=recommended-actions-now-assist-sam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Use recommended actions to guide you through the appropriate steps to achieve compliance. Take actionable steps to address any configuration, maintenance, or optimization issues and gain faster compliance.


-   **[Gain insights into your publisher license compliance by using Now Assist for SAM](https://www.servicenow.com/docs/access?context=summarize-publisher-compliance-now-assist-sam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Use generative AI to gain a comprehensive summary of publisher license compliance. The detailed publisher summaries that cover software deployment, license compliance, optimization, and configuration health enable you to understand the publisher license compliance details.


</td></tr><tr><td>

Now Assist for Source-to-Pay Operations

</td><td>

-   **[Now Assist for Sourcing and Procurement Operations \(SPO\)](https://www.servicenow.com/docs/access?context=now-assist-spo&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Now Assist for SPO includes an agentic workflow that enhances conversational intake capabilities. This AI-powered agent team streamlines user inquiries to sourcing and procurement teams by gathering knowledge, clarifying requests, deflecting common questions, providing product information, and recommending the appropriate purchase plan. For more information, see [Using agentic workflows in Now Assist for Sourcing and Procurement Operations](https://www.servicenow.com/docs/access?context=agentic-ai-now-assist-spo&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US).

The following new skills are available in Now Assist for SPO:

    -   Negotiation summarization for fulfillers: Summarize negotiations to keep fulfillers informed on their current status, progress, and action items.
    -   Negotiation event summarization for fulfillers: Summarize negotiation events to keep fulfillers informed on their current status, progress, and action items.
    -   Purchase order summarization for requesters: Summarize purchase orders to keep requesters informed about their current status, progress, and action items.
    -   Purchase requisition summarization for requesters: Summarize purchase requisitions to keep requesters informed about their current status, progress, and action items.
    -   Sourcing request summarization for requesters: Summarize sourcing requests to keep requesters informed about their current status, progress, and action items.
-   **[Now Assist for Supplier Lifecycle Operations \(SLO\)](https://www.servicenow.com/docs/access?context=now-assist-slo&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Now Assist for SLO includes an agentic workflow to streamline the supplier onboarding process by automating supplier registration. AI agents automate the supplier onboarding process, including data validation, duplicate checking, task generation, and communication with suppliers, streamlining the entire process for faster time-to-activation. For more information, see .

The following new skills are available in Now Assist for SLO:

    -   Conversational intake for suppliers: Suppliers can request profile updates, submit cases, and track inquiry statuses through a conversational interface powered by AI.
    -   Now Assist summarization panel: Case summaries are generated directly within the Now Assist Panel with no need to open individual case records.
    -   Multilingual support for summarization: Case details are summarized in the user's preferred language, improving accessibility for global teams.
-   **[Now Assist for Accounts Payable Operations \(APO\)](https://www.servicenow.com/docs/access?context=now-assist-apo&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

With the Now Assist for APO application, AP fulfillers can leverage generative AI capabilities to chat with live agents, submit a request, and track its status.

The ServiceNow®Now Assist experience brings generative AI powered purchase order line mapping feature designed to enhance matching accuracy and reducing manual intervention.

Generate purchase order summarization using Now Assist skills powered by generative AI.

Use agentic workflows in Accounts Payable Operations to resolve invoice inquiry cases raised by employees and suppliers. These workflows also help track associated invoice records efficiently. With an agentic workflow, you can process a high volume of invoice inquiries that come through email attachments to significantly reduce the workload of human agents.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


</td></tr><tr><td>

Now Assist for Strategic Portfolio Management \(SPM\)

</td><td>

-   **[Identify similar records using Now Assist](https://www.servicenow.com/docs/access?context=identify-similar-demand-records&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Detect similar existing demand records when creating or editing a demand using the identify similar records skill. The skill compares the **Name**, **Description**, and **Business Case** fields for contextual similarity.

-   **[Accelerate target creation with the target generation skill](https://www.servicenow.com/docs/access?context=generate-targets-for-goal&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Generate measurable targets from goals information and optional context with the target generation skill. The skill automatically populates key fields in the target creation form, helping teams define clear, measurable outcomes and create targets quickly.

-   **[Schedule project insights email](https://www.servicenow.com/docs/access?context=email-project-summary-skill-pw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   Schedule project insights email in the Configure project insights modal. The project email is emailed to the project managers and users and continues on the selected schedule that you select until the project is inactive or paused.
    -   Schedule and instantly send the project insights email to your project managers by selecting the **Send preview** button.
    -   Track important updates such as the delayed end dates, the status turning red, or the state updates of your projects and receive project insights email on the schedule that you select.
    -   Select the email frequency that works for you: weekly, bi-weekly or monthly.
    -   Monitor critical elements such as milestones, resources, projects, and project tasks.
    -   Receive proactive, AI-based notifications when project milestones or critical tasks could lead to delays using Monitor project task agent. Use the Enable critical task alerts option from planning page to enable the project task monitor AI agent.
    -   Choose the recipients to whom you want to send the project insights email.

-   **[New third-party AI model provider options available for Now Assist](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Google Gemini 2.0 Flash, Google Gemini 2.5 Pro, and AWS Claude 3.7 Sonnet are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI GPT-4.1 and GPT-4.1 mini.

-   **[Write planning item skill](https://www.servicenow.com/docs/access?context=using-now-assist-for-spm&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   Use this skill to improve record quality and user satisfaction by enabling AI assistance in the Description field across all Strategic Planning Workspace forms, including product idea, demand, epic, project, capability, feature, and story.
    -   Enable text refinement with the **Elaborate** and **Shorten** options on planning items to support product managers and agile team members in creating and editing content more effectively.

</td></tr><tr><td>

Now Assist for Telecommunications, Media and Technology \(TMT\)

</td><td>

-   **[Address voice quality issues](https://www.servicenow.com/docs/access?context=now-assist-customer-voice&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Collect customer details about the voice quality issue, open a service ticket with RADCOM \([https://radcom.com/](https://radcom.com/)\), and generate a resolution plan.

-   **[Risk signals and issues summarization](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-risk-signals-issues&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Generate summary details including the record and associated risk solutions and risk occurrences for risk signal and issues records.


-   **[Help remediate bill issues](https://www.servicenow.com/docs/access?context=billissue-remediation-usecase&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Handle billing inquiry case requests, analyze customer invoices, and recommend better plans based on customer usage patterns.

-   **[Analyze network incidents](https://www.servicenow.com/docs/access?context=network-incident-analysis-usecase&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Identify historic incidents and determine resolution plans. The AI agent also has the capabilities to identify field values, estimate resolution time, and create actionable tasks.

-   **[Support renewals and expansion](https://www.servicenow.com/docs/access?context=now-assist-tmt-renewal-analyzer&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Streamline customer success management by automatically assessing account health, value realization, and adoption trends. Deliver timely, data-driven insights that guide renewal planning and play recommendations.

-   **[Trigger risk mitigation touchpoint](https://www.servicenow.com/docs/access?context=now-assist-tmt-touchpoint-meeting-scheduler&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Enable customer success agents to optimize meeting schedules within the customer success workflow by creating and managing meetings. Create and manage meetings based on key details such as invitees, agenda, meeting type, and scheduling preferences.

-   **[Success summarization](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-plays&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Generate summary details including overview, current status, and open tasks for success initiatives, internal plays, and customer plays. Enhance Zoom meeting summaries by updating key notes, and enabling sentiment tracking.

-   **[Analyze metric data trend](https://www.servicenow.com/docs/access?context=now-assist-tmt-analyze-metric-trend&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Collect and analyze metric data for engagements, identify patterns, and generate a trend chart.

-   **[Service summary generation](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-knowledge-graph&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Generate a service summary for a product inventory.

-   **[Knowledge graph schema generation](https://www.servicenow.com/docs/access?context=now-assist-tmt-create-knowledge-graph&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Use the Knowledge Graph \(KG\) to create Knowledge Graph schema.

-   **[Customize a summary card for service summary](https://www.servicenow.com/docs/access?context=customize-uib-builder-service-summary&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Customize the summary card of the service summary and UI actions according to your needs.

-   **[Register consumers using Agentic AI](https://www.servicenow.com/docs/access?context=now-assist-tmt-register-consumer-users-sb&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Initiate the consumer registration process using agentic AI to receive step-by-step guidance, including error checks during registration and support for resolving those errors.

-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


-   **[Monitor engagement health](https://www.servicenow.com/docs/access?context=now-assist-tmt-resolve-risk&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Monitor the health score of all engagements, create trend charts, and generate risk signals when a decline is detected.

-   **[Analyze risk signals and recommend solutions](https://www.servicenow.com/docs/access?context=now-assist-tmt-monitor-health&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Retrieve unaddressed risk signals and identify appropriate success plays based on a back-end decision table.


-   **[Using Telecommunications, Media, and Technology AI agent collection](https://www.servicenow.com/docs/access?context=using-aiagents-usecases&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Use Now Assist for TMT AI agents to troubleshoot and autonomously resolve customer issues.

    |AI agent agentic workflow|Description|
    |-------------------------|-----------|
    |Test and repair telecom service issues|Use AI agents to handle task requests that require troubleshooting, diagnosis, and resolution of a case task.|


-   **[Dynamic prompt configuration](https://www.servicenow.com/docs/access?context=now-assist-tmt-customize&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Use the Now Assist for Telecommunications, Media and Technology \(TMT\) application to provide concise, context-driven summaries that are specific to each case. Your agents can ensure that critical case details are captured and can provide personalized and informed resolutions.

-   **[Enhanced test summarization](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-test&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Use AI-generated test summaries that include the metric descriptions and contextual notes from cases. Your agents can focus on high-priority issues and make better informed decisions that enhance the product quality and performance.

-   **[Resolution notes generation](https://www.servicenow.com/docs/access?context=now-assist-tmt-generate-resolution&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Generate resolution notes and then shorten or elaborate the content by using the Now Assist context menu in the resolution notes field of the case form in both the Core UI and Workspace.

-   **[Knowledge article generation](https://www.servicenow.com/docs/access?context=now-assist-tmt-generate-knowledge-article&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Select and gather insights and data from multiple similar cases to create an article by using Now Assist for TMT. Use the Now Assist icon \(![Now Assist icon.](../../common/image/icon-ai-sparkle.png)\), which is accessible as an inline capability to create and refine Knowledge articles.

-   **[Account onboarding case summarization](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-onboard-case&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Generate a concise account onboarding case summary that enables your agents to get a quick overview of the case details.

-   **[Engagement summarization](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-engagement&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Generate a high-level summary with a list of the key items about an engagement.

-   **[Touchpoint summarization](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-touchpoint&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Generate a quick summary of the various touchpoints in the engagement life cycle. Your agents can get a quick summary of all meetings and emails exchanged between the different stakeholders and any follow-up activities.

-   **[Transform mapping assist](https://www.servicenow.com/docs/access?context=now-assist-tmt-generate-transform-maps&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

While using the Service Exchange for a provider's application, use the Transform Mapping Assist feature to generate transform mappings between provider and consumer tables automatically. This skill enables you to streamline the transformation mapping process by reducing errors and improving overall efficiency.


</td></tr><tr><td>

Now Assist for Vulnerability Response

</td><td>

-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add.

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Use Now Assist for Vulnerability Response in Security Posture Control](https://www.servicenow.com/docs/access?context=using-now-assist-api-connector&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

You have the option to use Now Assist to help you automatically complete some of the steps in the Connector builder in the Security Posture Control workspace. Use the Connector builder to create your own service graph connectors for Security Posture Control.

-   **[Generate insights to prioritize risks](https://www.servicenow.com/docs/access?context=sem-insights-skill&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Use generative AI to provide contextual summaries, actionable recommendations, and quick links in the Security Exposure Management Workspace, helping you prioritize critical risks and accelerate remediation.

-   **[Generate recommendation for approval impact analysis](https://www.servicenow.com/docs/access?context=sem-approval-recommendation-skill&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Use generative AI to provide on-demand recommendations to approve or reject a request directly from the Exception Change Approval record, enabling approvers to make fast, consistent decisions while reducing manual analysis effort.


-   **[Granular roles](https://www.servicenow.com/docs/access?context=now-assist-vr-acticvate-agentic-workflow&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

The sn\_vul\_ai.write\_rem\_insights and sn\_vul\_ai.read\_rem\_insights granular roles have been added and are inherited by the sn\_vul.vulnerability\_admin and sn\_vul.vulnerability\_analyst roles automatically. These roles provide you with more control over read and write access for the records on the Remediation Compliance Insights \[sn\_vul\_ai\_remediation\_insights\] caching table. The VR.System role also inherits these granular roles so background job execution for the workflow can occur.


-   **[Identify duplicate vulnerable items with Now Assist for Vulnerability Response](https://www.servicenow.com/docs/access?context=dedupe-host-vi-now-assist-vulnerability-response&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Use generative AI to identify duplicates for your active host vulnerable items that are imported by your vulnerability scanners. Use generative AI reasoning with Now Assist to help your analysts differentiate between primary vulnerability items \(VITs\) and those VITs that are duplicates. Close duplicate VITs and move their associated detections automatically to the primary VIT records.

-   **[Suggest preferred vulnerability solutions with Now Assist for Vulnerability Response](https://www.servicenow.com/docs/access?context=solutions-now-assist-vulnerability-response&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Use generative AI to analyze available remediation options pulled from integrated third-party products like Red Hat, Tenable for Vulnerability Response, or internal solution management systems. Evaluate each option against the specific configuration item context, for example, the OS version or software version, and get recommendations for the most viable fix for implementation.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


-   **[Using agentic workflows in Now Assist for Vulnerability Response](https://www.servicenow.com/docs/access?context=using-now-assist-ai-agents-vr&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

The Assess vulnerability exposure agentic workflow enables vulnerability managers to determine your exposure to vulnerabilities.

    -   Determine your exposure to the most current Cybersecurity and Infrastructure Security Agency \(CISA\) known vulnerabilities in your environment and assess their potential impact to your configuration items \(CIs\) and business services.
    -   Identify assets with Common Vulnerabilities and Exposures \(CVEs\).
    -   Determine the number of active vulnerability items \(VITs\) that correspond to CVEs. Create watch topics for VIT remediation.
The Analyze vulnerability remediation status agentic workflow enables vulnerability managers to monitor and assess remediation target compliance.

    -   Track Service Level Agreement \(SLA\) compliance - Understand how effectively your organization is meeting remediation goals for vulnerabilities based on your SLAs.
    -   Analyze missed SLAs by severity, assignment group, and configuration item \(CI\) class - Pinpoint gaps in remediation by categorizing overdue VITs based on severity, assignment groups, and CI classes to enable targeted interventions and smarter resource allocation.

</td></tr><tr><td>

Now Assist for Workplace Service Delivery \(WSD\)

</td><td>

-   **[Optimize cleaning activities agentic workflow](https://www.servicenow.com/docs/access?context=optimize-cleaning-activities-agent&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Use the Optimize cleaning activities agentic workflow to manage cleaning and maintenance schedules of a maintenance case based on the space utilization rate of the location where a maintenance case is created.

-   **[Automate map updates agentic workflow](https://www.servicenow.com/docs/access?context=automate-map-updates-agent-ai&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Use the Automate map updates AI agentic workflow to configure the map during bulk updates to Indoor Mapping.

The Map Admin Agent autonomously retrieves the sources for the CAD file and resumes the import task. If the correct source isn't found, the agent moves the task to the Waiting user input state.


</td></tr><tr><td>

Now Assist in AI Search

</td><td>

-   **[Automatic activation for Now Assist Multi-Content Response Genius Results](https://www.servicenow.com/docs/access?context=now-assist-multi-content-qna-genius-results&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

When you use Guided Setup to activate the Now Assist panel, Now Assist Multi-Content Response Genius Results are automatically activated for relevant search profiles.

-   **[Hybrid search](https://www.servicenow.com/docs/access?context=hybrid-search-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Hybrid search blends keyword search and semantic vector search to offer a blend of superior search recall and contextual relevance for knowledge article, Catalog Item, external content, and topic retrieval searches.

-   **[Configure AI Search as the source for Ask Now Assist suggestions](https://www.servicenow.com/docs/access?context=configure-ai-search-source-ask-now-assist-suggestions&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Admins can configure the system to use AI Search as the source for Ask Now Assist suggestions, enabling suggestion term highlighting and more flexible search operators in enhanced chat.


-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


-   **[AI Search Genius Results widget for record producers](https://www.servicenow.com/docs/access?context=cfg-ais-genius-results-widget&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Administrators can configure the AI Search Genius Results widget on record producers to enhance the user experience when creating an incident. The widget displays actionable Genius Result suggestions relevant to the user's incident description. Users can select from these Genius Result suggestions to address their own issues, or can continue with their incident submission if none of the suggestions resolve their problem.


</td></tr><tr><td>

Now Assist in Contract Management

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Automated obligation extraction](https://www.servicenow.com/docs/access?context=cmpro-na-reminder-agentic-wf&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US#section_tgm_mt3_dhc)**

Use the manage contract repository agentic workflow to automatically identify and capture key contractual obligations from signed contracts and create obligation records in the contract repository. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **[Using contract playbook to review AI-extracted obligations](https://www.servicenow.com/docs/access?context=cmpro-na-review-obligations&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Review extracted obligations in the contract playbook, with options to edit, approve, or reject each obligation. Approved obligations are added as obligation records in the contract repository while rejected obligations are deactivated.

-   **[Contract obligation extraction skill in Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=cncore-conf-obligation-extraction&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Configure and map use cases for obligation extraction skill in the Now Assist Admin console to automatically extract key contractual obligations from signed contracts. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **[Conversational contract search and insights Workflow](https://www.servicenow.com/docs/access?context=cmpro-agentic-use-conv-search&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Contract documents are often complex and stored across multiple formats and repositories, making keyword-based search inefficient and error-prone. The new Now Assist powered conversational search feature enables you to search contract documents using natural language and dialogue-driven queries.

The conversational search feature does not support searching within contract documents that are scanned PDFs.

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Now LLM LTS support for Contract Management Pro](https://www.servicenow.com/docs/access?context=now-llm-model-updates&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.


-   **[Reviewing AI-extracted results in the playbook](https://www.servicenow.com/docs/access?context=cmpro-na-review-ai&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Use the playbook within a contract repository record to review the metadata extracted by the AI agents in the Manage contract repository agentic workflow. You can make necessary changes to the extracted information, and submit it to update the contract repository. If the contract end date is available, the **Review contract reminders** tab appears in the playbook, enabling you to review and update the AI-calculated contract reminder date and specify recipients for contract renewal or terminations.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[Select large language models for use cases in Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=cmpro-na-manage-llm&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Select a large language models \(LLM\) provider at for a contract analysis or metadata extraction use case. The selected LLM is applicable only for the specific use case and overrides the LLM selected for Now Assist in Contract Management skills.


-   **[Manage contract repository agentic workflow](https://www.servicenow.com/docs/access?context=cmpro-na-reminder-agentic-wf&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Use the Manage contract repository agentic workflow to improve productivity by autonomously creating milestone reminders for the notice period of contract renewals or the notice period for termination of contract renewals.

    |Agentic workflows|Description|
    |-----------------|-----------|
    |Manage contract repository|Uses AI agents to retrieve contract details such as renewal notice period, termination notice period, or auto-renewal clause information, and determine the average lead time for similar contracts to create contract milestone reminders for the notice period of contract renewals or the notice period for termination of contract renewals.|


</td></tr><tr><td>

Now Assist in Document Intelligence

</td><td>

-   **[Document and visual insights AI agent enhancements](https://www.servicenow.com/docs/access?context=document-and-visual-insights-ai-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

The document and visual insights AI agent can recognize and provide citations for multiple attachments.


-   **[LLM selection for use cases](https://www.servicenow.com/docs/access?context=set-up-use-case-for-now-assist-document-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Configure a different LLM to generate predictions for extraction and Q&amp;A use cases.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


-   **[Document and visual insights AI agent](https://www.servicenow.com/docs/access?context=document-and-visual-insights-ai-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Use an AI agent to help process the tasks that analyze and extract data from documents and images.

-   **[Full automation for document data extraction](https://www.servicenow.com/docs/access?context=turn-on-full-automation-for-document-extraction-na&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Automatically extract the document data and process the document task without agent review.

-   **[Data extraction from accounts payable \(AP\) invoices](https://www.servicenow.com/docs/access?context=exploring-now-assist-apo&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Extract data from invoices with Now Assist for APO.

-   **[Document chat in Virtual Agent](https://www.servicenow.com/docs/access?context=upload-documents-na-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Integrate Now Assist for Virtual Agent with Now Assist in Document Intelligence to enable the chat responses that are based on the document content.

-   **[Attachment summarization in ITSM](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-skill&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

View the summaries of attachments with the record summary in ITSM.


-   **[Document extraction](https://www.servicenow.com/docs/access?context=extract-document-data-with-now-assist-document-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Extract the data from documents by using LLMs to provide the recommended field values.

-   **[Document Q&amp;A](https://www.servicenow.com/docs/access?context=review-document-qnas-with-now-assist-document-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Use generative AI to find the answers to the predefined questions in a document.

-   **[Setting up use cases for Now Assist in Document Intelligence](https://www.servicenow.com/docs/access?context=set-up-use-case-for-now-assist-document-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Set up Document Intelligence use cases to enable agents to use the document extraction and document Q&amp;A skills.


</td></tr><tr><td>

Now Assist in Platform Analytics

</td><td>

-   **[Gather insights, plan, and collaborate in the AI Data Explorer](https://www.servicenow.com/docs/access?context=now-assist-explorer&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US) \(January 2026\)**

Ask quick questions, receive tailored recommendations, and collaborate with AI and your colleagues to build long-term analysis. Enable teams to discuss and act on findings instantly. Centralize insights and narratives for better decision making. Guide users with contextual insights and suggestions.

Main features include:

    -   [Optional deeper level of analysis](https://www.servicenow.com/docs/access?context=hidden-insights&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)
    -   [Add a data visualization from an exploration to a dashboard](https://www.servicenow.com/docs/access?context=add-data-viz-from-expl-to-dboard&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)
    -   [Share explorations with tagged users](https://www.servicenow.com/docs/access?context=share-now-assist-explorer&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)
    -   [Duplicate an exploration](https://www.servicenow.com/docs/access?context=nowass-expl-duplicate-exploration&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)
    -   [Duplicate an answer in an exploration](https://www.servicenow.com/docs/access?context=nowass-expl-dup-del-question-resp&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)
    -   [Summarize an exploration](https://www.servicenow.com/docs/access?context=summarize-exploration&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)
AI Data Explorer leverages Query Generation to translate natural language questions into actionable insights. Query Generation enables users of AI Data Explorer to analyze their data and access a broader range of data sets. Key capabilities include:

    -   [Ability to add tables to the semantic data layer](https://www.servicenow.com/docs/access?context=add-table-semantic-layer&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)
    -   [Multi-table source support](https://www.servicenow.com/docs/access?context=ask-expl-questions&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)
    -   [Workflow Data Fabric table support](https://www.servicenow.com/docs/access?context=create-integrations-applications&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)
    -   [Database view support](https://www.servicenow.com/docs/access?context=add-table-semantic-layer&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)

</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

-   **[Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience. Assistant Designer is comprised of three main areas: Assistants, Asset library, and Analytics.

[Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Access the **Assistants** tab within [Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US) by navigating to **All** &gt; **Assistant Designer**. The **Assistants** tab is only available for customers who have the Now Assist license. NLU-only customers don't have access to [Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).
[View assistants](https://www.servicenow.com/docs/access?context=view-assistants&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   View chat and voice assistants within the **Assistants** tab of [Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).
        -   The card view is the default view for the assistants.
        -   An inactive \(gray\) or active \(green\) label is shown for each assistant.
        -   Activate, deactivate, test, edit, or delete an assistant.
        -   A display experience label is shown on each chat assistant card.
        -   A domain label is shown on assistant cards if an assistant is created outside of the global domain. If assistants are only created within the global domain, the label isn’t shown.
        -   The ability to view or edit an assistant depends on the domain that the admin has access to.
        -   The name and date are shown for when the assistant was last updated.
        -   Voice assistants show a voice icon and label on the card. Voice assistants can't be tested within Assistant Designer.
        -   The map view shows the assistant hierarchy where you can open, turn on or off, or delete an assistant.
    -   View the side panel for quick access to **Pick up where you left off**, **Recent activity**, and **Resources**.
[Create a voice assistant](https://www.servicenow.com/docs/access?context=configure-voice-assistants&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Start creating an AI voice assistant by providing a name and description. Tag to a business unit to analyze your voice assistant.
    -   Power your voice assistant with agentic experience by adding AI agents.
    -   Personalize your voice assistant by choosing a language, adding a welcome message, and an AI voice persona.

**Note:** The supported languages are:

        -   English
        -   German
        -   Spanish
    -   Secure the voice interactions by setting up caller authentication methods and safeguards.
[Create a chat assistant](https://www.servicenow.com/docs/access?context=create-assistant&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Add basic details such as a name and description for your chat assistant, and set your assistant as a primary assistant. The Basic details page within the UI has replaced the Overview page.
    -   Now Assist panel – Platform \(default\) assistant can be set as a primary assistant and linked to secondary assistants. Now Assist panel – Developer assistant doesn't have this option.
    -   The name and description of the Now Assist panel assistants can't be changed.
[Use agentic support for a chat assistant](https://www.servicenow.com/docs/access?context=use-agentic-support&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Let the assistant use AI agent skills and agentic orchestration. Admins can choose between agentic or standard \(Q&amp;A\) modes depending on business needs and user experience goals. Turn on or off the **Prioritize AI agents during skills discovery** feature.
[Assign search sources to a chat assistant](https://www.servicenow.com/docs/access?context=add-info-sources-assistant&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Restore search sources back to the default \(Now Assist Multi-Turn Catalog Ordering and Now Assist Q&amp;A\).
    -   Now Assist panel - Platform \(default\) assistant now has the option to copy an existing search configuration.
    -   Dynamic global search configuration has been added to the list of search application configurations.
    -   Create or configure additional search sources by selecting the **External Content Connectors** link. This replaces a card view.
    -   Manage knowledge articles by selecting the **Knowledge Center** link.
    -   In edit mode, search sources are found within the Information Sources sub-tab.
[Add a Knowledge Graph schema to a chat assistant](https://www.servicenow.com/docs/access?context=add-kg-schema-assistant&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Adding a Knowledge Graph schema has moved from the Information sources page to its own page.
    -   Add a Knowledge Graph schema is now available for the Now Assist panel - Platform \(default\) assistant. For the NLQ schema, if Global Graph or Global Graph Mini is selected, you have the option to select tags for specific workspaces that are active on the instance.
    -   Define the mapping relationship between individual workspaces on the instance and predefined Knowledge Graph tags when Global Schema is selected for NLQ.
    -   In edit mode, Knowledge Graph is found within the Information Sources sub-tab.
[Add assets to a chat assistant](https://www.servicenow.com/docs/access?context=add-assets&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   By default, all Now Assist skills \(Now Assist Q&amp;A, Now Assist multi-turn catalog ordering, Now Assist topics, subflows and actions, custom skills, and AI agents\) are turned on. Therefore, the Now Assist skills page has been removed.
    -   Map an asset to an assistant. Assets are the building blocks of each assistant, providing them with instructions and functionality for helping users. Assets include topics, subflows and actions, custom skills, and AI agents. For Now Assist panel - Developer assistant, only topics \(asset type\) is available.
    -   In edit mode, assets are found within the Information Sources sub-tab.
[Display your chat assistant on a portal, channel, or mobile app](https://www.servicenow.com/docs/access?context=display-assistant-portal-channel&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Leverage Now Assist capabilities in Google chat.
    -   Use **Prominent action button override** to allow a different chat assistant other than the default assistant to be launched on a mobile app.
    -   In edit mode, display experiences are found within the Settings sub-tab.
[Display your assistant on Platform or ServiceNow Studio](https://www.servicenow.com/docs/access?context=display-nap-assistant&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   The **Add ServiceNow Platform** drop-down menu has replaced the **Add agent experience** drop-down menu. A Now Assist panel assistant can't be added to other display experiences.
    -   In edit mode, display experiences are found within the Settings sub-tab.
[Brand an assistant](https://www.servicenow.com/docs/access?context=brand-assistant&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Minor enhancements to the look-and-feel of the standard chat preview pane.
    -   In edit mode, branding is found within the Settings sub-tab.
[Manage an assistant chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   A standard chat preview pane is shown for the default greeting topic \(Now Assist – Greeting\) and the default closing topic \(Now Assist – Closing\). Selecting custom topics won’t show a preview pane.
    -   Fallbacks have a standard chat preview pane and each fallback is shown if toggled on.
    -   For the Now Assist panel - Platform \(default\) assistant, web search, record producer, and custom fallback are available options. End this chat and survey are available for the standard chat experience.
    -   In edit mode, chat experience is found within the Settings sub-tab.
[Enable additional chat features](https://www.servicenow.com/docs/access?context=additional-chat-features&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Web search, response streaming, document uploads, and closed chat were moved from the Manage chat experience page to its own page. By default all chat features except web search are turned on.
    -   Response streaming can be turned on at the assistant level regardless of whether Dynamic Translation is turned on or off. However, response streaming doesn't work when Dynamic Translation is being used.
    -   In addition to web search, response streaming, document uploads, and closed chat, Now Assist panel Platform assistant has voice input. Voice input allows users to use a microphone to enter the input.
    -   In edit mode, additional chat features are found within the Settings sub-tab.
[Review chat assistant settings](https://www.servicenow.com/docs/access?context=review-assistant-settings&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   New sections that have been added include: Agentic support, Knowledge Graphs, Assets, and Chat features.
    -   Testing an assistant has been removed from the Review page.
[Test a chat assistant](https://www.servicenow.com/docs/access?context=test-assistant&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Test a chat assistant from **Assistant Designer** &gt; **Assistants** tab or from within each page while in edit mode.
[Edit a chat assistant](https://www.servicenow.com/docs/access?context=edit-assistant&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Edit a chat assistant from **Assistant Designer** &gt; **Assistants** tab. You will be directed through an edit flow with a slightly different UI from the create flow.
[Analyzing assistants](https://www.servicenow.com/docs/access?context=ai-engagement-analytics&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Monitor, evaluate, and optimize the performance of your AI-powered assistants within the **Analytics** tab of [Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).
-   **[Copy received messages](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Use the copy message icon in the feedback panel to copy received Virtual Agent responses.

-   **[New system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**
    -   Set the **com.glide.cs.nass.synthesized\_response.disabled\_popover.hide** to `true` to hide the popover for disabled catalog items for Now Assist in Virtual Agent and Now Assist panel's enhanced chat.
    -   Set the **sn\_ais\_assist.enable\_pi\_in\_nba** property to `true` to allow conversational history-based suggested actions and fill multiple suggested action slot options.
    -   View the **sn\_nowassist\_va.enable\_nass\_show\_all\_options** property to decide whether to allow the **View all options** link in an enhanced chat conversation's greeting topic.
    -   The **com.glide.interactive\_view.enabled** property opens an interactive side panel view next to the chat window. The default value is `true` to activate AI Engagement Experience on your instance.
-   **[View org chart in the interactive view](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Select **View org chart** from the people citation's popover in Now Assist panel's enhanced chat or Now Assist in Virtual Agent enhanced chat/enhanced chat's full-page experience. The person's organizational chart appears to the right of the chat conversation in an area known as the interactive view. You can switch between multiple organizational charts via a drop-down in the interactive view if you open multiple people citations' org charts in the same conversation.


-   **[Select continue or move to next task button](https://www.servicenow.com/docs/access?context=nava-standard-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

The **Continue to next task** button appears in the new **Ready to move on to your next task** card whenever multiple questions are found in a single standard chat user's message. The **Move on to the next task** citation appears at the end of an enhanced chat's synthesized response whenever multiple questions or requests are found along with an action in the user's single message. Whenever either **Continue to next task** \(standard chat\) or **Move on to the next task** \(enhanced chat\) is selected, the second question or request is reviewed and a synthesized response is sent back regarding the user's second question or request.

-   **[Multiple questions in a single user message are answered consecutively](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Virtual Agent can answer multiple questions that were submitted in a single message query. Now Assist panel or Now Assist in Virtual Agent answers the multiple questions consecutively in a response.

-   **[Now Assist in Virtual Agent system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Use **sn\_aia.use\_agents\_in\_planner** to configure AI agent discovery behavior. The default value is `true`, preferring AI agents over assets including catalogs, topics, Q&amp;A knowledge base articles, workflows, and sub-workflows. When set to `false`, there’s no preference for AI agents. AI agents and assets are treated the same.


-   **[Configure additional user interface and experience options for enhanced chat](https://www.servicenow.com/docs/access?context=ac-configure-chat-branding&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Customize and configure the Search Toggle Button Label for enhanced chat's full-page experience. Additionally, you can configure the Enable Unread Conversation Count Display and Left Panel Header Label for enhanced chat and enhanced chat's full-page experience.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[View agentic conversations processing steps](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

View agentic conversational processing steps and stop the flow, if needed.

-   **[View extended entities and records](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

View extended entities and records in standard and enhanced chat conversations that come from the additional custom tables associated with the Knowledge Graph natural language query \(NLQ\) schema such as:

    -   Assets
    -   Incidents
    -   Recently viewed knowledge base articles
    -   Requests
    -   Tasks
-   **[View suggested queries in the portal’s search bar and chat window](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

View the most frequently asked queries in the portal’s search bar and enhanced chat’s Virtual Agent. Any search query entered into the portal’s search bar or Virtual Agent is incorporated into the greeting topic for future conversations as a suggested query. Suggested queries are only included in the Virtual Agent greeting topic whenever no promoted assets are designated.

-   **[Work with suggested queries](https://www.servicenow.com/docs/access?context=nava-sys-props&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Two system properties were added to enable the suggested queries feature: **sn\_nowassist\_va.enable\_suggested\_queries** and **sn\_nowassist\_va.max\_suggested\_queries**.

-   **[Configure AI search answers OneExtend capability for web search](https://www.servicenow.com/docs/access?context=configure-ai-search-answers-capability-for-web-search&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Configure the AI Search answers capability via `sys_one_extend_capability.list` to establish the web search AI provider and work with API keys, if needed.

-   **[Expanding AI provider support for web search](https://www.servicenow.com/docs/access?context=configure-ai-search-answers-capability-for-web-search&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

OpenAI, Perplexity, and Google Gemini support web search.

-   **[Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Enhancements to Now Assist in Virtual Agent assistants and Now Assist panel Platform and Developer assistants. Options vary for Now Assist panel assistants.

[Create a chat assistant](https://www.servicenow.com/docs/access?context=create-assistant&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Configure assistants by domain.


    -   Now Assist in Virtual Agent assistants: By default, all global skill types are turned on in Now Assist Admin console.
    -   Now Assist panel Platform assistant: By default, all global skill types, except for Catalog skill, are turned on in Now Assist Admin console.
    -   Now Assist panel Developer assistant: By default, Now Assist Topic skill is turned on in Now Assist Admin console. No other skills are available for the Now Assist panel Developer assistant.
[Display your chat assistant on a portal, channel, or mobile app](https://www.servicenow.com/docs/access?context=display-assistant-portal-channel&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Now Assist in Virtual Agent: For mobile search widgets, allow the search bar to open into a full-page experience.
[Display your assistant on Platform or ServiceNow Studio](https://www.servicenow.com/docs/access?context=display-nap-assistant&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Now Assist panel Platform assistant: Enable enhanced chat for a conversational experience that includes a dynamic, movable, and resizable chat window, plus access to multiple active conversations.
    -   Now Assist panel Developer assistant: Not applicable.
[Assign search sources to a chat assistant](https://www.servicenow.com/docs/access?context=add-info-sources-assistant&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Now Assist in Virtual Agent:
        -   Add internal and external search sources, such as catalog items and Microsoft Sharepoint, from a drop-down list.
        -   Add a slot filling schema to input user information from your organization's Knowledge Graph. Add a Natural language query schema to allow users to perform a data query during a conversation.
    -   Now Assist panel Platform assistant:
        -   Add internal and external search sources, such as catalog items and Microsoft Sharepoint, from a drop-down list.
        -   Add a slot filling schema to input user information from your organization's Knowledge Graph. Add a Natural language query schema to allow users to perform a data query during a conversation.
    -   Now Assist panel Developer assistant: Not applicable.
[Manage an assistant chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Now Assist in Virtual Agent:
        -   Select a custom greeting topic, closing topic, error topic, and survey for your assistant.
        -   Select one or more fallback options: live agent, web search, record producer, end this chat, and custom fallback.
        -   Enable web search fallback option and web search mode to allow users to search the web from within a chat window.
    -   Now Assist panel Platform assistant:
        -   Select a custom greeting topic or error topic for your assistant.
        -   Fallback options don't apply to Now Assist panel Platform assistant.
        -   Enable web search mode to allow users to search the web from within a chat window.
    -   Now Assist panel Developer assistant: Not applicable.
-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Use the enhanced Now Assist panel for a more intuitive and personalized experience. The updated Now Assist panel is re-sizable and can be moved anywhere on the ServiceNow AI platform.


-   **[Now Assist in Virtual Agent system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Enable pinning a chat window on a portal by using the **sn\_nowassist\_va.enhanced\_chat\_pin\_enabled.&lt;portal-url&gt;** system property.


-   **[Use enhanced chat](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Enhanced chat is a conversational support experience within a resizable and moveable window that also includes the ability to have multiple active conversations and superior search capabilities. Using enhanced chat's full-page experience further intertwines chat and search capabilities by redirecting users into a full-page chat after entering a query into a portal's search bar.

-   **[View inline citations](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

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

-   **[Use suggested actions](https://www.servicenow.com/docs/access?context=suggested-actions&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

View suggested actions that were related to your prior conversation and that you consider doing next. After completing a conversational catalog request, conversational subflow, or Virtual Agent topic, two suggested actions appear after a `Here's what you can do next` header.

-   **[Stream enhanced chat responses](https://www.servicenow.com/docs/access?context=streaming-responses-requestor&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Stream LLM response messages as they’re generated instead of the response text appearing all at once to end users. Responses stream in either one letter or one word at a time.

-   **[Use language detection to automatically switch the conversational language for enhanced chat conversations](https://www.servicenow.com/docs/access?context=dynamic-lang-detection-translation-enhanced-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Automatically switch the conversational language to the user's detected language during LLM enhanced chat conversations when language detection is turned on. This automatic switch can occur when a user enters an utterance at the start of a new conversation or within the portal home page’s search field.

-   **[Recognize the Boolean user input control during dynamic translation](https://www.servicenow.com/docs/access?context=multi-language-options-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Recognize the Boolean user input control in chat conversations during dynamic translation.

-   **[Adjust Shorten responses toggle to impact Show more option in chat](https://www.servicenow.com/docs/access?context=va-text-response&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

For bot text responses, adjust the **Shorten responses** toggle in Virtual Agent Designer to turn off the **Show more** option on the user side. When **Shorten responses** is turned off, the **Show more** option does not appear in the chat to the user and the full answer is displayed rather than a truncated response.

-   **[Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

In addition to configuring Now Assist in Virtual Agent assistants, admins can configure the default Now Assist panel assistants. Options may vary for Now Assist panel assistants.

[Create a chat assistant](https://www.servicenow.com/docs/access?context=create-assistant&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   If multiple assistants are created, users can chat simultaneously with multiple assistants. Conversations are independent from each other.
    -   Turn on or off Now Assist panel \(agent or creator\) assistant. Contact support to configure Now Assist panel assistants.


    -   Now Assist Topic skill must be turned on at the assistant level for document uploads to be activated when managing the chat experience. For more information, see [Manage an assistant chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).
    -   Create and manage agentic workflows in Now Assist AI Agents Studio and assign the workflows to the assistant.
[Display your chat assistant on a portal, channel, or mobile app](https://www.servicenow.com/docs/access?context=display-assistant-portal-channel&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Display Now Assist in Virtual Agent enhanced chat, with or without the full-page experience, on your portal or mobile app. This dynamic window includes the ability to have multiple active conversations and search capabilities. To use enhanced chat, portals and mobile apps require AI Search to be enabled. For more information on the prerequisites, see [Portal prerequisites for enhanced chat](https://www.servicenow.com/docs/access?context=prerequisites-enhanced-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US) and [Mobile app prerequisites for enhanced chat](https://www.servicenow.com/docs/access?context=mobile-prereqs-enhanced-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).
[Manage an assistant chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Upload documents to Now Assist in Virtual Agent standard chat or enhanced chat experience. The Now Assist topics skill must be enabled in Now Assist skills. For more information on file formats, see [Upload documents in a chat](https://www.servicenow.com/docs/access?context=upload-documents-na-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).
[Review chat assistant settings](https://www.servicenow.com/docs/access?context=review-assistant-settings&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Document uploads appear as active if it's turned on when managing the chat experience.
-   **[Upload documents in a chat](https://www.servicenow.com/docs/access?context=upload-documents-na-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Upload or drag and drop files to Now Assist in Virtual Agent \(standard chat or enhanced chat\). The assistant analyzes and understands the content of the files, and a user can ask questions about the content of the files or get a summary.

-   **[Now Assist in Virtual Agent system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Enable suggested actions in Now Assist in Virtual Agent so that users are offered options for what they can do after completing a prior action. Suggested actions is applicable to standard and enhanced chat, mobile, and Microsoft Teams.

-   **[Web Search custom skill](https://www.servicenow.com/docs/access?context=web-search-custom-skill&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Use the Web Search custom skill to query the internet for information using a third-party AI. The skill triggers when the LLM and AI Search cannot provide an answer. Both values are shown in the System Properties \[sys\_properties\] table item **sn\_nowassist\_va.websearch\_fallback\_enabled**. Set a chosen definition \(such as Perplexity\) to `true` in the AI Search answers OneExtend capability along with its matching API in the Credentials list. You can set one definition and credential to true at any one time.


-   **[Stream chat responses](https://www.servicenow.com/docs/access?context=streaming-responses-requestor&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Stream LLM response messages as they’re generated instead of the response text appearing all at once to end users. Responses stream in either one letter or one word at a time.

-   **[Benefit from Knowledge Graph integration](https://www.servicenow.com/docs/access?context=exploring-knowledge-graph&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Receive fewer Virtual Agent slot-fill questions during conversations whenever Knowledge Graph is activated.

-   **[Receive personalized synthesized response answers with Knowledge Graph integration](https://www.servicenow.com/docs/access?context=access-knowledge-graph-designer&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Discover more personalized conversational catalog, topic, subflows, or action responses and receive more personalized answers for Q&amp;A Knowledge Base synthesized responses. Personalized responses may appear depending on whether the questions or requests sent to Virtual Agent trigger the Knowledge Graph user profile schema. These personalized responses are slot-filled based on the following table and column attributes:

    -   sys\_user table's columns:
        -   Name
        -   First name
        -   Last name
        -   Username
        -   Employee number
        -   Email
        -   Business phone
        -   Mobile phone
        -   Title
        -   Preferred language
        -   Time format
        -   Date format
        -   Time zone
        -   Zip code
        -   City
        -   State
    -   cmn\_location table's columns:
        -   City
        -   State
        -   Country
    -   cmn\_department table's column:
        -   Name
        -   Headcount
    -   core\_company table's column:
        -   Name
    -   manager table's columns:
        -   Name
        -   First name
        -   Last name
        -   Username
        -   Employee number
        -   Email
        -   Business phone
        -   Mobile phone
        -   Title
        -   Preferred language
        -   Time format
        -   Date format
        -   Time zone
        -   Zip code
        -   City
        -   State
    -   reportees table's columns:
        -   Name
        -   First name
        -   Last name
        -   Username
        -   Employee number
        -   Email
        -   Business phone
        -   Mobile phone
        -   Title
        -   Preferred language
        -   Time format
        -   Date format
        -   Time zone
        -   Zip code
        -   City
        -   State
    -   assets table's columns:
        -   Display name
        -   Purchase date
        -   Retired date
-   **[Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)'**

Now Assist skills:

    -   An alert appears, at the assistant level, if a global level skill is turned off.
    -   By default, all global level skills are turned on in the Now Assist Admin console, except for subflows and actions.
    -   Custom skill is a new skill that has been added to the list of Now Assist skills.
Display experience:

    -   Select the chat launcher function to open an assistant.
    -   Select a custom mobile app, integrated with the mobile SDK, to open an assistant.
    -   Custom apps section appears if the mobile SDK plugin is installed.
Information sources:

    -   Add an external search source to your assistant's search profile.
    -   Create custom skills in the Now Assist Skill Kit and assign the skills to the assistant.
    -   Associate Knowledge Graph with an assistant if Knowledge Graph is enabled.
Chat experience:

    -   Promoted topics has been renamed to promoted assets.
    -   Tags appear in promoted assets indicating whether it's a topic, subflow, or action.
    -   Streaming responses can be activated if Dynamic Translation is deactivated.
    -   Activate or deactivate pre-chat surveys as an admin with the sys\_properties.list item **com.glide.cs.nass.prechat.enabled**.
Review:

    -   Shows whether stream responses is turned on or off.
-   **[Using Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Search through external content connections such as Microsoft SharePoint or Confluence if external search sources are added to information sources when [Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

Select an inline citation to show a popover containing a link to an article or source, or a description and action to start a request.

Citations with an action are shown after a second clarifying question from Virtual Agent.

Change the order of the fallback and revisit options in the **View more options** results list that appears in the synthesized response. Use the **sn\_nowassist\_va.synth\_response\_revisit\_position** system property with either the **BEFORE\_FALLBACK** or **AFTER\_FALLBACK** values.

Show or hide the **Need more help** button in the synthesized response by using the **show\_view\_more\_for\_synthesized** system property.

Turn on or off regular results in Virtual Agent from the following Now Assist Search Results Output Types table using the parameter **now\_assist\_va\_search\_results\_output\_type.list** parameter.

Use prechat and postchat surveys with GPT4o and LLAMA. Users can select data pills or enter strings for responses.

Use new prebuilt topics for prechat and postchat surveys in LLM conversations.


</td></tr><tr><td>

Now Mobile

</td><td>

-   **[Now Assist genius results in Now Mobile®](https://www.servicenow.com/docs/access?context=na-qa-mobile&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Now Assist genius results in Now Mobile® provides a personalized way of using the search functionality as opposed to the traditional AI Search experience.

The following plugins are required to access this functionality.

    -   Now Mobile® version 29.2
    -   Employee Center version 35.0

</td></tr><tr><td>

Operational Resilience

</td><td>

-   **[Measure resilience metrics using the CSDM model](https://www.servicenow.com/docs/access?context=using-csdm-v5&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Define the entity types and pillars in Operational Resilience and generate the entities. Establish relationships between CSDM objects, including business services, service offerings, business processes, and application services. Specify the type of main node configuration that you want to use by setting the **sn\_oper\_res.opres\_csdm\_main\_node\_config** property.

After generating the entities and setting up the main node configurations, you can import CMDB data into Operational Resilience for reporting. CSDM and their dependencies are updated weekly while the red flags data is calculated daily. The outcome is displayed on the Homepage or in the related list of the CSDM objects.

-   **[Specify the primary origin of an operational vulnerability](https://www.servicenow.com/docs/access?context=add-impacted-area-to-vul&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Identify the primary origin of an operational vulnerability in its record. Once the primary origin is specified, its upstream dependencies are automatically included in the impacted areas, enabling you to view the operational vulnerability from all affected perspectives.

-   **[Using Digital resilience incident reporting](https://www.servicenow.com/docs/access?context=drir-module&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Assess whether any critical services are affected and classify the reported incident as a major incident if necessary. Notify regulators of major incidents, categorized by their severity and security ratings.

The Digital resilience incident reporting module, accessible from the Operational Resilience Workspace, is integrated with Incident Management and Security Incident Response to generate and share reports in the format that is specified by the regulators.

You can generate an initial report within 24 hours, an intermediate report within 72 hours, and a final report within 1 month. All of these reports are automatically triggered by the application from the time that the incident is classified as a major incident.


</td></tr><tr><td>

Operational Sustainability Management

</td><td>

-   **[Forecast planning and analysis](https://www.servicenow.com/docs/access?context=scenario-analysis-forecast&version=yokohama&pubname=yokohama-environmental-social-governance&ft:locale=en-US)**

Model and prepare for potential outcomes by using forecast planning analysis. With these tools, you can create, save, or visualize multiple scenarios.

-   **[Formula tree](https://www.servicenow.com/docs/access?context=reviewing-formula-tree&version=yokohama&pubname=yokohama-environmental-social-governance&ft:locale=en-US)**

Explore the calculated metric definitions by reviewing a structured and visual representation of the entire calculation chain. By using a formula tree, you can access the calculation details and view how the different metrics and emission factors are interconnected.

-   **[Historical metric data](https://www.servicenow.com/docs/access?context=importing-metric-data&version=yokohama&pubname=yokohama-environmental-social-governance&ft:locale=en-US)**

Import the historical metric data by using a pre-defined import template with instructions. With this process, you can update and manage the metric data within your organization and help to ensure that all data complies with the established business rules.

-   **[Dynamic filtering for Microsoft 365 for ServiceNow Reporting](https://www.servicenow.com/docs/access?context=add-related-fields-0365&version=yokohama&pubname=yokohama-environmental-social-governance&ft:locale=en-US)**

Filter the fields dynamically and set up dependencies by using related fields. In the Microsoft 365 add-in, you can configure fields so that cascading filters are supported dynamically. You can select a value in a field and have the related fields automatically update to show the relevant options. This process helps you to streamline data entry and improve efficiency.


</td></tr><tr><td>

Operational Technology \(OT\) Manager Foundation

</td><td>

-   **[Search for related records in an OT CMDB table](https://www.servicenow.com/docs/access?context=search-related-records-ot-cmdb-tables-now-assist-otm&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Use the OT CMDB search function to find an OT configuration item \(CI\) and OT device information in an OT CMDB table.

-   **[Upload, validate, and import your OT device inventory spreadsheet using the Import OT device spreadsheet into OT CMDB agentic workflow](https://www.servicenow.com/docs/access?context=upload-import-validate-ot-device-inventory-spreadsheet&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Use the Import OT device spreadsheet into OT CMDB agentic workflow to begin the process for uploading, validating, and importing your OT device inventory into ServiceNow.


</td></tr><tr><td>

Operational Technology Incident Management

</td><td>

-   **[Create an OT incident from an OT change request](https://www.servicenow.com/docs/access?context=create-ot-incident-from-ot-change&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Create an OT incident related to an OT change request directly from the OT change record in the Industrial Workspace.


</td></tr><tr><td>

Operational Technology Manager

</td><td>

-   **[About the Industrial Workspace page](https://www.servicenow.com/docs/access?context=view-installed-ot-applications&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Use the About Industrial Workspace page on the ServiceNow AI Platform to view the OT applications and the versions that you have installed on your instance.

-   **[Search for a record in the Industrial Workspace](https://www.servicenow.com/docs/access?context=search-in-industrial-workspace&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Search for CMDB tables in the Industrial Workspace to find CMDB related records. The search function was previously limited only to other Operational Technology records.

-   **[Check whether an OT device is virtual](https://www.servicenow.com/docs/access?context=ot-assets-form&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Check whether an OT device is virtual using the **Is Virtual** field for OT devices in the following categories:

    -   OT Supervisory System
    -   OT Control System
    -   OT Field Devices
    -   Unclassed OT Devices
-   **[Create remediation tasks for invalid staging records from an import task](https://www.servicenow.com/docs/access?context=create-remediation-task-for-validation-errors&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

After validating the imported staging records, create remediation tasks for invalid staging records directly in the import task record.

-   **[Operational Technology Visibility dashboard](https://www.servicenow.com/docs/access?context=ot-manager-dashboard&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Track your OT data across different sites with the Operational Technology Visibility dashboard available in the Industrial Workspace.


-   **[Automatic conversion of IT to OT devices using CMDB groups](https://www.servicenow.com/docs/access?context=use-cmdb-groups-it-ot-conversion&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Use CMDB groups to group IT configuration items \(CIs\) based on additional information, such as software installed, so that you can convert the CIs to OT devices.

-   **[Mapped equipment model entity for your OT devices](https://www.servicenow.com/docs/access?context=view-all-mapped-ot-devices&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Identify the equipment model entity that your OT devices are mapped to in the Industrial Workspace and help group your device data by equipment model entity.


-   **[Important actions configuration on the OT Action-Oriented Landing Page](https://www.servicenow.com/docs/access?context=configure-order-important-actions-aolp&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Configure the OT Action-Oriented Landing Page by using the **Sort items** field for your important actions.


-   **[CMDB OT class model updates](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-operation-technology&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

Leverage an enhanced OT user experience and make additional configurations for your OT devices with the following CMDB OT class model updates:

    -   The OT Device Network Connection \[sn\_ot\_device\_network\_connection\] table references the CMDB CI relationships \[cmdb\_rel\_ci\] table to support device-to-device connections on the OT network.
    -   The Key Value \[cmdb\_key\_value\], Software Instance \[cmdb\_software\_instance\] and Firmware Install \[cmdb\_firmware\_install\] table references were added to the OT view on IT and OT classes.
    -   The Backup Storage Information \[cmdb\_backup\_storage\_information\] and Backup Job Execution History \[cmdb\_backup\_job\_execution\_history\] tables reference the CMDB CI relationships \[cmdb\_rel\_ci\] table to support backup management use cases.
    -   Product Instance Identifier was added as an identifier for the OT Identification Rule.
    -   The OT backup management model was added to help you store multiple backups against a configuration item.
    -   Firmware Installation \[cmdb\_firmware\_install\], Key Value \[cmdb\_key\_value\], and Software Instance \[cmdb\_software\_instance\] tables were added as a related entry for OT classes.
    -   The **ire\_criterion\_attribute** attribute was added to the OT Entity \[cmdb\_ot\_entity\] table to act as a criterion attribute for an OT entity-related entry.
    -   Optional conditions to filter the records during identification and reconciliation were added to the OT identification rules.
    -   The OT Class Mapping Template \[ot\_class\_mapping\_template\] table was introduced to capture class mappings used for Service Graph Connectors.
    -   Required conditions were added under **Advanced Configuration** that must be met for lookup identification rules.
    -   Industrial printer \(industrial\_printer\) was added as an OT device type.
-   **[Pre-import OT Worksheet Entry Review \(POWER\) tool updates](https://www.servicenow.com/docs/access?context=service-graph-connector-for-OT-excel&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Import OT devices with distributed Microsoft Excel spreadsheets to help manage your OT system and its devices. The Pre-Import OT Worksheet Entry Review \(POWER\) tool includes the following new functionality:

    -   Improve validations with access to ISA sites using the cmdb\_ot\_isa\_viewer role that has been added to the ot\_staging\_user role needed for running validations.
    -   Upload, validate, and import Microsoft Excel spreadsheet data for the Service Graph Connector for Microsoft Excel by creating an import task and attaching the spreadsheet to the import task record.
    -   Firmware Installation records can be created when a firmware version is available.
    -   OT entity update issues can be resolved through the Service Graph Connector for Microsoft Excel.
    -   The new Industrial Core plugin \(com.sn\_ot\_core\) is required for class mapping when using the Service Graph Connector for Microsoft Excel.

</td></tr><tr><td>

Operational Technology Vulnerability Response

</td><td>

-   **[Configuring Operational Technology Vulnerability Response from the SEM Workspace](https://www.servicenow.com/docs/access?context=configuring-oper-tech-vulnerability-response&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Starting from Operational Technology Vulnerability Response version 30.0.x, users may be redirected to the Unified Security Exposure Management \(USEM\) Workspace to perform some configuration tasks. The Vulnerability Response plugin is consolidated under USEM from version 30.0.x.

-   **[Demo data not required for Operational Technology Risk Calculator plugin](https://www.servicenow.com/docs/access?context=calculate-vulnerability-risk&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

You can directly access and use the Operational Technology Vulnerability Response Risk Calculator without loading the demo data while installing the plugin. In previous releases, the risk calculation was included as part of the demo data.

-   **[Enhanced features for Hardware Vulnerability Assessment for OT devices](https://www.servicenow.com/docs/access?context=understanding-hwd-vuln-assessment&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

The following enhancements are available in Hardware Vulnerability Assessment:

    -   Assessments without Normalization: Ability to assess discovery models without content available for normalization.
    -   Confidence Scores: New scoring mechanism for all types of assessments.
    -   Version Range Support: The range information provided by the National Vulnerability Database \(NVD\) is used to create assessments without explicitly creating Common Platform Enumeration \(CPEs\) in the NVD.
    -   Partial assessment for partially normalized discovery model: Creates partial assessments for discovery models without firmware version. The partial assessments are done if the other versions of the discovery model have the same publisher and model.
    -   Expiring of assessments: If you update the firmware version of a CI, the corresponding normalized discovery model also updates. The assessment records based on the older firmware version expires while new assessments are generated for new firmware version.
-   **[Hardware Vulnerability Assessment menu in the Industrial Workspace](https://www.servicenow.com/docs/access?context=understanding-hwd-vuln-assessment&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Automatically and periodically assess the OT device firmware vulnerabilities that are in your inventory and create vulnerable items against the impacted assets \(CI\).

-   **[Vulnerability risk scores on the OT Risk Management dashboard](https://www.servicenow.com/docs/access?context=otvr-risk-management-dashboard&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

View a table of vulnerability risk scores for your OT devices at each level of the equipment model with the OT Risk Management dashboard.

-   **[Enhanced OTVR \(PA\) dashboard experience](https://www.servicenow.com/docs/access?context=operational-technology-vulnerability-response-dashboard&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

View and manage all of your OT vulnerability data and data visualizations in a centralized location with the enhanced OTVR \(PA\) dashboard, which is accessible on the Dashboard Library page.


</td></tr><tr><td>

Opportunity Management

</td><td>

-   **[View the roll-up amount in the Opportunity Kanban View](https://www.servicenow.com/docs/access?context=opportunity-management-kanban-view&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

Enables customers to view the roll-up amount that is automatically calculated in the base currency for all opportunity stages in the Kanban View.


-   ****

Enables the sales representatives to customize the complex product offerings by using the product configurator. This ensures that the sales representatives identify and share the detailed requirements and price to the customer much earlier in the cycle.

-   **[Revise existing opportunities after an upgrade](https://www.servicenow.com/docs/access?context=revise-existing-opportunities-post-upgrade&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

Enable the sales representatives to use the scheduled job to modify older opportunities to incorporate the functionality of supporting parent-child opportunity line items.


</td></tr><tr><td>

Opportunity Marketplace

</td><td>

-   **[Create project opportunities by importing project details from Project Workspace](https://www.servicenow.com/docs/access?context=egd-create-other-opportunities&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Opportunity owners create gigs, projects, and volunteer opportunities. Opportunity details for Project type opportunities can be imported from projects in the ServiceNow Project Workspace. These opportunities are different from internal jobs. OPM enables you to manage any opportunities that you create and track applications. The ability to create opportunities is based on user criteria.

-   **[Select multiple user criteria groups](https://www.servicenow.com/docs/access?context=egd-create-other-opportunities&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Access to opportunities is controlled by assigning user criteria groups to an opportunity. From the Opportunity details page of the Create an opportunity widget, you can select multiple user criteria to manage access to the opportunity.


</td></tr><tr><td>

Order Management

</td><td>

-   **[Business Portal for order case management](https://www.servicenow.com/docs/access?context=order-mgt-business-portal&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

Enable your customers to create cases for common order-related issues such as delivery delays, quantity disputes, and other routine inquiries directly using the Business Portal, ensuring faster issue resolution and improved customer satisfaction. This application is a feature of Customer Service Management and the Order to Cash Operations functionality for Order Management.

-   **Hierarchical view of order line items**

Enable order agents and order managers to use the hierarchical list view to view parent and child relationships within order lines.

-   **[Price adjustment details for order lines](https://www.servicenow.com/docs/access?context=view-price-adjustment-details-order-lines&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

Provides order agents and order managers the visibility into the price adjustments applied at each step of the pricing plan, including a detailed breakdown of all adjustments applied to the unit base price and unit list price to see how the unit net price is derived.

-   **[Multi-instance product offering configurations](https://www.servicenow.com/docs/access?context=product-catalog-managment&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

Create multiple instances of a child product offering in orders to generate a custom configuration for each product offering instance. When a child product offering has a quantity greater than 1, agents can clone or split a child product offering to create multiple product offering instances so that each quantity has its own configuration.

-   **[Transient products](https://www.servicenow.com/docs/access?context=product-catalog-managment&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

Add transient products, which are defined as one-time-use products or services, to new orders. Sold product and product inventory records are created but not maintained for transient products. Move, Add, Change and Disconnect \(MACD\) actions are not supported for transient products.

-   **[Business Portal for Order Management](https://www.servicenow.com/docs/access?context=order-mgt-create-an-order-using-customer-portal&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

Use the Business Portal to view product catalogs, select product options, and place orders. Customers can also view their order status using the Business Portal.

-   **[Cases for multiple invoices](https://www.servicenow.com/docs/access?context=csm-invoice-operations&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Create cases for multiple invoices or for specific invoice lines. Agents can reference multiple invoices or invoice lines as case line items on an invoice case record. By using case line items, agents can track multiple issues for the same invoice case and resolve the issues in each case line item independently before resolving and closing the order case. This application is a feature of Customer Service Management and the Order to Cash Operations functionality for Order Management.

-   **[Add subscription pricing to an order](https://www.servicenow.com/docs/access?context=add-subscription-pricing-to-an-order&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

Enable order agents and order managers to access and view key calculated metrics such as monthly recurring price and annual recurring price. The subscription pricing fields are automatically calculated based on contract start date and contract end date. These metrics enhance revenue reporting and help you to better understand recurring revenue dynamics.


</td></tr><tr><td>

Password Reset

</td><td>

-   **[Deny ACLs for Password Reset Access](https://www.servicenow.com/docs/access?context=r_InstalledWithPasswordReset&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

Enhance the security of Password Reset related tables by restricting access to non-authenticated users through Deny ACLs.


</td></tr><tr><td>

Performance Analytics

</td><td>

-   **[Apply multiple levels of breakdown to an indicator](https://www.servicenow.com/docs/access?context=multi-level-breakdowns&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

Migrate indicators from traditional Performance Analytics architecture to change data capture \(CDC\)-based data snapshots. This new architecture allows for more than two levels of breakdown to apply to an indicator. RaptorDB Professional is required, and not all indicators qualify for migration.


</td></tr><tr><td>

Platform Analytics experience

</td><td>

-   **[Generate data visualizations conversationally](https://www.servicenow.com/docs/access?context=analytics-assist-landing-page&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

Generate Platform Analytics artifacts from conversational interactions using Analytics Generation. Analytics Generation is part of the Now Assist for Creator application.

-   **[Implement filters in groups](https://www.servicenow.com/docs/access?context=create-filter-group&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

Create filter groups with shared apply, clear, and reset buttons. Filters in a group appear in their own container. Grouping filters reduces the number of calls and improves performance compared to cascading filters for big data use cases.

-   **[Apply multiple levels of breakdown to an indicator](https://www.servicenow.com/docs/access?context=multi-level-breakdowns&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

Migrate indicators from traditional Performance Analytics architecture to change data capture \(CDC\)-based data snapshots. This new architecture allows for more than two levels of breakdown to apply to an indicator. RaptorDB Professional is required, and not all indicators qualify for migration.

-   **[Show the distribution of data in box plot data visualizations](https://www.servicenow.com/docs/access?context=create-dv-box-plot&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

Show the median and lower and upper quartiles of numeric data along with outliers by using box plots. You can also compare the distribution of different groups of this data.

-   **[Target suggestion cards](https://www.servicenow.com/docs/access?context=proactive-analytics&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

Be notified of missing target values and review dates for indicators. If you have target Insights active for your dashboard, Target suggestion cards alert you to the missing values and provide an easy way to fix them.


</td></tr><tr><td>

Playbooks in Workflow Studio

</td><td>

-   **[Translate playbooks content](https://www.servicenow.com/docs/access?context=add-translations-playbooks&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

Add custom translations for labels, descriptions, and UI Layout properties in your playbooks.

-   **[Restart playbook activities that end in error](https://www.servicenow.com/docs/access?context=restart&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

Configure activities so that end users can restart any activity that ends in an error and variant conditions are automatically re-evaluated when playbooks are restarted.

-   **[Support for Retrieval Augmented Generation \(RAG\) with playbook generation](https://www.servicenow.com/docs/access?context=playbook-assist&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

Generate playbooks from inputs that refer to custom actions, flows, subflows, content from installed spokes, or activity definitions. Include the names of commonly used and recently published actions, subflows, flows, and activity definitions available on your instance in your playbook generation requests.

-   **Generate playbooks with the OpenAI GPT-4o LLM**

Use the OpenAI GPT-4o LLM to generate a playbook from text.

-   **[Add more fields in Create Task activities](https://www.servicenow.com/docs/access?context=create-task-activity&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

Add more fields in a more configurable Create Task activity.

-   **[Create a checklist directly in Workflow Studio](https://www.servicenow.com/docs/access?context=checklist-task-activity&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

Create a checklist directly in the side panel without needing a checklist template.


</td></tr><tr><td>

Policy and Compliance Management

</td><td>

-   **[Calculate compliance score and roll up to entity](https://www.servicenow.com/docs/access?context=compliance-score-calculation-pc-ws&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

View a comprehensive compliance score at the entity level that includes all the child entities rolled up to the parent entity along with the compliance score of the parent entity's direct controls.

-   **[Elimination of duplicate citations from UCF Shared list download](https://www.servicenow.com/docs/access?context=ucf-deduplication-pc&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Eliminate duplicate citations associated with the authority documents when you download UCF content. You can retain one citation as active and mark the duplicate citations as inactive. Move the control objectives of the duplicate citations to the active citation, and update the duplicate citation records with the Source ID of the active citation.

-   **[Improve compliance workspace performance](https://www.servicenow.com/docs/access?context=compliance-manager-compliance-ws&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Improved the performance of the compliance workspace by removing the issue widget to ensure a faster and smoother user experience. You can still access issue details from the "Issues Overview" section.

-   **[Entity based access](https://www.servicenow.com/docs/access?context=c_GRCControls&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Entity based access aims to provide a more granular approach to data access, ensuring that users can only access data through entity-based access. The entity-based access has been enabled for controls, attestations and policy exception to control mappings. Administrators can grant access to an entity's related records by adding users or user groups, or by using entity user fields for entity-based access configuration.

-   **[Deduplication of control objectives](https://www.servicenow.com/docs/access?context=now-assist-for-irm&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Using Generative AI, identify and recommend similar control objectives. You can choose to accept a control objective as duplicate, dismiss those that are not similar, or retain a control objective as primary in which details from all other similar control objectives are merged. Additionally, the system automatically copies related records, including policies and risk statements, to ensure comprehensive information is maintained in one location after retiring the accepted control objectives.


</td></tr><tr><td>

Portfolio Planning

</td><td>

-   **[View financial data of your planning items at the portfolio level](https://www.servicenow.com/docs/access?context=using-portfolio-financials-ppw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   View the rolled-up financial costs and benefits data of your planning items Epics, Demands, and Projects at the portfolio level for different time scales and ranges.
    -   View the financial values such as the Budget, Planned cost, Variance, Actuals, and Remaining Estimates of your planning items by expense type or cost type.
    -   View the Forecasts, Actuals, and Variance of your planning items for monetary benefits.
    -   View the financial data of the planning items while creating multiple prioritization scenarios to promote efficient use of budget and to help increase ROI.
-   **[Create and manage financial scenarios of planning items](https://www.servicenow.com/docs/access?context=optimizing-scenarios-in-strategic-planning&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   Optimize your portfolio by creating financial scenarios to validate and arrive at a profitable outcome.
    -   Plan and manage the budget of the planning items in a simulation mode for efficient financial planning and to help prevent overspending.
    -   Manage prioritization and budget allocation of the planning items to meet business priorities.
    -   Compare financial scenarios and automatically allocate the planned budget from approved scenarios to planning items.
    -   Enable a budget allocation property to analyze finances in scenario planning and take effective decisions using data-driven insights.
-   **[Dashboards for data analysis and decision-making](https://www.servicenow.com/docs/access?context=using-dashboards-in-ppw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Consolidate key data and metrics from multiple sources onto dashboards, enabling you to monitor performance, track progress, and make informed decisions related to planning and execution.

You can create, edit, and copy a dashboard, customizing as needed. Add widgets to a dashboard to display key data, metrics, and visualizations. You can also share dashboards to collaborate with the business stakeholders who have access to the portfolio plan.

-   **[Create and share views for portfolio plans and free-form roadmaps](https://www.servicenow.com/docs/access?context=managing-portfolio-plan-views-ppw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Create, edit, and switch views in portfolio plans and free-form roadmaps using display preferences. You can create personal views that are private to you or public views that can be shared with stakeholders who have access.

Portfolio plan display preferences include column selection, grouping and filtering. Free-form roadmap preferences include grouping, milestones selection, dependencies selection, and tracking mode. The portfolio plan view saves your display preferences across the Prioritization, Roadmap, Capacity, and Financials tabs.

**Note:** Portfolio plan views are available only for the Planning module and are supported in live mode, but not in scenario mode.

-   **[Real-time collaboration for Planning item Docs](https://www.servicenow.com/docs/access?context=docs-for-planning-items-in-ppw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Edit a doc page concurrently with multiple other editors. Colored cursors denote the current location of editors on the page. You can choose to show or hide these indicators.

**Note:** To use the full functionality of Docs v6.6.0 within Portfolio Planning Workspace, upgrade to Portfolio Planning Workspace v8.5.0. For more information, see the [Incompatibility After Upgrading Docs to Version 6.0.0 \[KB2017926\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2017926) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Predictive Intelligence

</td><td>

-   **[Model Explainability](https://www.servicenow.com/docs/access?context=predictive-intel-explainability&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Learn which classes contribute most to your model's predictions by optionally adding Model Explainability to Workflow Classification solutions. Model Explainability provides a new tab labeled **Feature Importance** where you can run an analysis of each class's contribution to the overall prediction.

-   **[Leverage new advanced options for classification solutions](https://www.servicenow.com/docs/access?context=configuring-advanced-settings-ml-solutions&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US), from Yokohama Patch 4.**
    -   [Configure include only top N labels](https://www.servicenow.com/docs/access?context=predictive-intel-only-top-n-labels&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). Limit the classification model to use only the top most frequent labels. You can choose a number as the limit.
    -   [Minimum records needed for label to include it](https://www.servicenow.com/docs/access?context=predictive-intel-minimum-records-needed-label&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). Set a threshold for the minimum number of records a label must have in your dataset to be included in model training.
    -   [Remove others label](https://www.servicenow.com/docs/access?context=predictive-intel-remove-others-label&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). Reduce noise in the model and enhance predictive accuracy by removing records with the label "others" from training data.
    -   [Use LightGBM algo for classification model training](https://www.servicenow.com/docs/access?context=predictive-intel-lightgbm-algo&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). Enable the LightGBM \(Light Gradient-Boosting Machine\) algorithm for training classification models.
    -   [Config parameters for model config in classification](https://www.servicenow.com/docs/access?context=predictive-intel-config-parameters-classification&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). Customize training behavior by including a dictionary of parameters in the JSON format.

</td></tr><tr><td>

Privacy Management

</td><td>

-   ****

Leverage criticality factors to evaluate the initial risks associated with processing activities. Integrate these factors into privacy assessments and automatically generate a criticality score upon assessment approval. These factors are also added to processing activities, enabling you to make updates at any time. Integrating these factors in a privacy assessment eliminates the need for a separate criticality assessment. This consolidation reduces the workload for the privacy teams.

-   **[Smart assessments in Privacy Management](https://www.servicenow.com/docs/access?context=smart-assessments-in-privacy-management&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Use the new and improved assessment experience that enables:

    -   capturing the data elements, the information object attributes, hierarchies
    -   building the assessment questionnaire
This new experience enables responders to update all the necessary details within the assessments, eliminating the need to update the processing activity separately.

-   **[Configure information object categories](https://www.servicenow.com/docs/access?context=configure-information-object-categories&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Implement Information object categories to tag and classify information objects effectively. For example, attributes like iris scans and fingerprints are often referred to as biometric data, or email addresses and phone numbers can be tagged as contact information. Information object categories enable you to categorize these information objects under these broader classifications. This approach is useful in the following ways:

    -   Enhances compliance with regulations such as GDPR, CCPA, and so on by accurately capturing and tracking required data categories.
    -   Improves clarity for business users, ensuring they can easily identify and work with terms they’re familiar with while adhering to regulatory standards.
    -   Streamlines data governance by creating a structured framework that supports both regulatory needs and business operations.
-   **[Smart assessment for privacy case management action tasks](https://www.servicenow.com/docs/access?context=accept-a-case-task&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Use the new assessment experience of Smart Assessment Engine for privacy case action tasks. Only when an action task moves from the **Draft** to the **Assigned** state, the assessment can be sent. To use the smart assessment, a new property called enable\_smart\_assessments \(sn\_grc\_case\_mgmt.enable\_smart\_assessments\) is introduced with the default value as **true**.


</td></tr><tr><td>

Problem Management

</td><td>

-   **[User role for service desk agents](https://www.servicenow.com/docs/access?context=prob-roles-instld-itsm-roles&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

With the sn\_service\_desk\_agent user role, increase operational efficiency by streamlining the process of asking about, gathering, and verifying information, as well as delivering quick resolutions. This role is designed for tier 1 service desk agents and is accessible when the ITSM Roles plugin \(com.snc.itsm.roles\) installed.

The sn\_service\_desk\_agent role includes the following roles:

    -   sn\_incident\_write
    -   sn\_problem\_write
    -   sn\_change\_write
    -   sn\_request\_write
    -   tracked\_file\_reader
Additionally, with the installation of the **ITSM Gen AI** \(**com.sn.itsm.gen.ai**\) plugin, the knowledge\_user and now\_assist\_panel\_user roles are integrated within the sn\_service\_desk\_agent role.

The sn\_service\_desk\_agent user role can be used starting with Service Operations Workspace version 6.1.

-   **[Problem Models for Streamlined Problem Management](https://www.servicenow.com/docs/access?context=problem-mgmt-models&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Problem Management models are used to simplify management of problems and problem tasks. These models provide an efficient way to configure state transitions and define conditions to move from one state to another.

This functionality is enabled out of the base system for new or zBoot customers.


</td></tr><tr><td>

Process Mining

</td><td>

-   **[Now Assist based work notes analysis](https://www.servicenow.com/docs/access?context=worknotes-analysis&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

Work notes analysis is now enhanced using Now Assist to understand the operational reasons behind activity transitions by examining the work notes and comments recorded around the time of these transitions.

-   **[Process configuration builder introduced](https://www.servicenow.com/docs/access?context=create-process-config&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

Configure and view the process configurations efficiently by using the new comprehensive Process configuration builder. It is a guided setup to configure and view the process configurations.

-   **[Content pack importer introduced for process configurations](https://www.servicenow.com/docs/access?context=po-content-pack&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

Import and customize the content pack process configuration templates to activate new features. Content pack process configuration templates are now read-only.

-   **[Process Mining evaluation project available for HR and CSM](https://www.servicenow.com/docs/access?context=evaluation-pm-inci-manag&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

Ability to try out the sample mining and limited features available for HR and CSM without an entitlement. For the advanced features, you can purchase a license.

-   **[Access control \(ACL\) rules updated](https://www.servicenow.com/docs/access?context=access-control&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

The ACL rules have been updated for broader visibility on the try-out version while also increasing the security.

    -   No Process Mining role is required to access a shared project and to generate Platform Analytics insights for some tables.
    -   Some breakdown filters or activity definitions are blocked for certain users based on the column access.
-   **[Process Mining performance improved](https://www.servicenow.com/docs/access?context=analyst-workbench-overview&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

The following improvements boost Process Mining performance and lead to quicker insights:

    -   Introduced lazy loading of improvement opportunities and variants for faster workspace loading.
    -   Introduced applying a transition filter before mining to reduce scope of data and speed up the mining process.
    -   Improved Process Mining workbench load time.
-   **[Transition filters enhanced](https://www.servicenow.com/docs/access?context=node-to-node-conditions&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

The enhanced transition filters now provide more flexibility and precision in filtering the process map by providing the following:

    -   Ability to use `OR` clause on steps to create a more complex and nuanced criteria for process transitions.
    -   Include predicates like "is empty" and "is not empty" allowing for more refined control over the conditions under which transitions occur, ensuring that workflows are both comprehensive and adaptable to a variety of scenarios.
    -   Ability to select more than one value with a single click that contains a specific text.
-   **[Enhanced the Process Mining engine](https://www.servicenow.com/docs/access?context=set-activity-def&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

Key updates include:

    -   Defining integer fields as activity definitions.
    -   Grouping journal fields to identify how quickly an agent reacted to an assigned case.
    -   Defining the order of simultaneous activities on the graph.
-   **[Addition﻿al breakdown capacity for Process Mining on external data](https://www.servicenow.com/docs/access?context=external-dataset&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

Ability to import a maximum of 10 breakdown fields enabling to segment and analyze specific subsets of the external process data using Process Mining.

-   **[API for accessing Process Mining data](https://www.servicenow.com/docs/access?context=define-workflow-model&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

Create, mine, and access Process Mining data via an API \(ProcessMiningIntegrationAPI\). For more information, see the API documentation.


</td></tr><tr><td>

Product Catalog Management and Pricing Management

</td><td>

-   **[Product offering recommendations](https://www.servicenow.com/docs/access?context=product-catalog-managment&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

Provide sales agents with offer recommendations for upselling or cross-selling additional products in quotes. Product catalog admins create the offer recommendations for sellable products. Sales agents can view the recommendations when adding products to quotes from the product catalog or when reviewing the lines items for a quote.

-   **[Product catalog and product configurator in the Business Portal for Order Management](https://www.servicenow.com/docs/access?context=order-mgt-create-an-order-using-customer-portal&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

Enable customers to view the product catalog and order products using the product configurator in the Business Portal for Order Management.


</td></tr><tr><td>

Project Portfolio Management

</td><td>

-   **[Identify similar records using Now Assist](https://www.servicenow.com/docs/access?context=identify-similar-demand-records&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Detect similar existing demand records when creating or editing a demand using the identify similar records skill. This skill compares the **Name**, **Description**, and **Business Case** fields for contextual similarity.

-   **[Migrate old status reports to new reporting tool](https://www.servicenow.com/docs/access?context=view-status-report-in-project-workspace&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Import your old status reports to a new status report tool for a consistent and organized reporting system.

-   **[Apply confidentiality settings to your projects](https://www.servicenow.com/docs/access?context=configuring-security-for-a-project-in-pw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Secure sensitive projects by applying confidentiality settings to your projects and make sure only authorized users can access confidential data and sub-projects.

-   **[Use checklist for project tasks](https://www.servicenow.com/docs/access?context=c_project-task-checklists&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Track the list of activities to be completed for a task by creating a checklist for your project tasks.

-   **[Migrate notes of resource plans to resource assignments](https://www.servicenow.com/docs/access?context=migrate-rsrc-plan-rsrc-asgnmnt&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Migrate the existing resource plan notes along with the allocation details to resource assignments and get clear insights while working with resource assignments in Resource Management Workspace.

-   **[Resource allocation and heatmap enhancements](https://www.servicenow.com/docs/access?context=use-resource-mgmt-prj-wksp&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   Use the allocation heatmap modal to view resource status, remaining capacity, and utilization and enable resource managers to assess task efforts.
    -   Use inline editing to update one or multiple cells in child resource assignments.
    -   Added new fields for resource assignment:
        -   Name
        -   Ready for review
        -   Notes
    -   Extend a resource assignment for a project or project task using the **Extend** row context menu action.

</td></tr><tr><td>

Project Workspace

</td><td>

-   **[Analyze the status report in Project Workspace](https://www.servicenow.com/docs/access?context=view-status-report-in-project-workspace&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   You can't edit the status report, but you can change the system property to enable editing.
    -   Import your old status reports to a new status report tool for a consistent and organized reporting system.
-   **[Duplicate a status report in Project Workspace](https://www.servicenow.com/docs/access?context=duplicate-status-report-pw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Reduce effort by duplicating a status report to transfer all project information without manual copying.

-   **[Configuring security for a project in Project Workspace](https://www.servicenow.com/docs/access?context=configuring-security-for-a-project-in-pw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   Apply confidentiality settings to safeguard sensitive projects and make sure that only authorized users can access confidential data and sub-projects.
    -   When a project is marked confidential in one workspace, such as Project Management or Strategic Portfolio Workspace, these settings automatically extend across all associated workspaces, maintaining consistent protection.
    -   To promote security, at least one user must be assigned access to any confidential project.
-   **[Project task checklists](https://www.servicenow.com/docs/access?context=c_project-task-checklists&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   Create a checklist for your project tasks and manage a list of activities or steps to be completed for a task.
    -   As an Administrator, you can add or remove checklists as needed.
-   **[View the roll-up financial values for project tasks at parent project level](https://www.servicenow.com/docs/access?context=using-financials-prj-wrkspc&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

View and manage the cost plans and expense lines recorded on a project task level on the parent project.

-   **[Resource allocation and heatmap enhancements](https://www.servicenow.com/docs/access?context=use-resource-mgmt-prj-wksp&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   Use the allocation heatmap modal to view resource status, remaining capacity, and utilization and enable resource managers to assess task efforts.
    -   Use inline editing to update one or multiple cells in child resource assignments.
    -   Added new fields for resource assignment:
        -   Name
        -   Ready for review
        -   Notes
    -   Extend a resource assignment for a project or project task using the **Extend** row context menu action.

</td></tr><tr><td>

Public Sector Digital Services

</td><td>

-   **[Grants Management](https://www.servicenow.com/docs/access?context=using-public-sector-digital-services&version=yokohama&pubname=yokohama-government-industry&ft:locale=en-US)**

Simplify and streamline Grant application intake and screening​ with Grants Management:​ Intake and Screening, a part of Grants Management. Improve self-service with a Grants Portal that streamlines finding, applying for, and tracking grants, with added features such as guided intake, and a save, resume, and export functionality. Set up and manage grant programs easily with guided steps​ using Grants Management: ​Program Set Up​, which guides grant program managers through the process of creating, publishing, and managing grant programs.​

-   **Communicate and share citizen and agent data securely between agencies using Service Exchange for Public Sector Digital Services**

Connect multiple ServiceNow instances to provide seamless support and service experiences across the Public Sector​ using Service Bridge for Public Sector Digital Services. Service Bridge enables unified case collaboration across agencies, streamlined approval workflows for funding distribution, and real-time crisis coordination with dynamic task management. Agencies can share citizen &amp; agency data securely through ​compliance-driven access.​​​

-   **[Post-chat summarization in Now Assist for Public Sector Digital Services \(PSDS\)](https://www.servicenow.com/docs/access?context=now-assist-psds-summarize-chat&version=yokohama&pubname=yokohama-government-industry&ft:locale=en-US)**

Condense chat records into short summaries using the chat summarization skill in the Now Assist for PSDS application. Agents can use the chat summarization skill to generate chat records for a case, auto-populate the chat summary into the Interaction section of the case record, and obtain a summary of the main points discussed during the chat, helping them propose a case resolution. The Now Assist for PSDS application brings generative AI chat summarization to Public Sector Digital Services.


</td></tr><tr><td>

Quote Management

</td><td>

-   **[Apply a sales agreement to a quote in Quote Management](https://www.servicenow.com/docs/access?context=quote-add-sales-agreement-quotes&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

Create a new sales agreement or apply an existing sales agreements to a quote. When a sales agreement is enabled in a quote, the products and services added to the quote are also added to a sales agreement. When an existing sales agreement is added to a new quote, the catalog is filtered to show the products and options from the sales agreement, the price list is set to the agreement price list, and the sales agreement line is referenced on quote line.

-   **[View price adjustment details for a quote line item](https://www.servicenow.com/docs/access?context=view-price-adjustment-details-for-quote-lines&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

Agents gain visibility into the price adjustments that were applied to the base and list price of the product ordered. This provides sales agent the visibility of how the net price is determined.


-   **[Quote PDF documents generation](https://www.servicenow.com/docs/access?context=quote-create-pdf-document&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

Generate a quote PDF document. Quote PDF documents can have designated signers and be emailed to customers for signatures through Docusign. Customers can also create PDF templates that reflect customer branding and logos.


-   **[Hierarchical quote line list view](https://www.servicenow.com/docs/access?context=quote-management-view-hierarchical-line-items&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

View quote lines as a hierarchical list. Agents can then view parent and child relationships for quote line items.


-   **[Product offer recommendations for quotes](https://www.servicenow.com/docs/access?context=quote-get-product-offer&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

Enable your agents to get product offer recommendations that complement or supplement existing products within a quote.


</td></tr><tr><td>

RPA Hub

</td><td>

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for RPA bot generation skill in addition to Now LLM Service and Azure OpenAI.

-   **[Enhanced ACLs for security measures](https://www.servicenow.com/docs/access?context=installed-with-rpa-hub&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

Enhanced access controls for RPA bot generation skill for Now Assist for RPA Hub in compliance with AI security directives.

Access to RPA bot generation skill is now restricted to users with the RPA developer or RPA admin role. These roles contain the RPA Hub Admin user role \(sn\_nowassist\_admin.user\).

-   **[RPA bot generation](https://www.servicenow.com/docs/access?context=rpa-now-assist-studio&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

Use the Robotic Process Automation \(RPA\) bot generation skill in RPA Desktop Design Studio to create and edit automations and activities through short text instructions and preview options, accelerating automation development for both new and existing users. For more information about creating automations using Now Assist, see [Create an automation with Now Assist](https://www.servicenow.com/docs/access?context=create-automation-now-assist&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US). For more information about creating activities using Now Assist, see [Create an activity with Now Assist](https://www.servicenow.com/docs/access?context=create-activity-now-assist&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

Enhance automation logic using the **Build automation** option, starting from components or from a blank canvas based on text instructions. For more information, see [Build an automation with Now Assist](https://www.servicenow.com/docs/access?context=build-automation-now-assist&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

-   **[High density robots](https://www.servicenow.com/docs/access?context=high-density-robots-rpa-hub&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

Enable multiple unattended robots to run simultaneously on the same Windows Server machine using the high-density robots feature. These unattended robots run automations in separate Remote Desktop Protocol \(RDP\) sessions. For more information, see [High density robots in Unattended Robot](https://www.servicenow.com/docs/access?context=high-density-robots-uat&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) and [Set up Windows Server machine for high density robots](https://www.servicenow.com/docs/access?context=setup-windows-server-hdr&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

-   **[Sample automations](https://www.servicenow.com/docs/access?context=sample-automations-rpa-studio&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

Use sample automations to jumpstart your automation journey with a library of pre-built automations.

The following unattended and attended sample automations were added to the Sample Explorer and home page of RPA Desktop Design Studio:

    -   User Creation in Badging App
    -   Universal Timezone Converter
    -   Decode Barcode and QR Code to Text
    -   PDF Text to Images
    -   PDF to Word
    -   HTML to CSV
    -   Word Operations
    -   Excel Operations
    -   Highlight Excel Rows
    -   City Weather Reports
    -   Tiff to PDF
    -   Add Word Footer
    -   Date Delta Across Apps
    -   File Ops: Copy, Delete, Move
    -   Extract Data from JSON to Excel
    -   Automate Offer Letters
    -   Summarize Sales Data
    -   Invoice Data Extraction to Excel
    -   Download File from URL
    -   Health Check Bot
-   **[Secure Shell \(SSH\) connector](https://www.servicenow.com/docs/access?context=ssh-connector&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

Establish an Secure Shell \(SSH\) connection to a remote server and execute commands in the RPA Desktop Design Studio. In the UNIX environment, SSH is the preferred way to access remote systems. Robots often interact with remote systems such as UNIX servers.

The connector comprises three methods:

    -   Connect: Establishes an SSH connection.
    -   Run Command: Executes commands over an established connection.
    -   Disconnect: Disconnects the session that was established using connect method.
Ensure to install the SSH plugin from the Plugins Manager as a prerequisite.

-   **[Bypassing the legal notice](https://www.servicenow.com/docs/access?context=rpahub-sys-properties&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

In RPA Hub, enable the **sn\_rpa\_fdn.bypass\_legal\_notice** system property to authorize the unattended robot to clear the legal notice message set by the system-level policy. This property ensures that a legal notice isn't displayed during the robot's login process.

-   **[What's New tab in the Help Center for RPA Hub](https://www.servicenow.com/docs/access?context=whats-new&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

Learn about the following newly released RPA features in your instance in the What's New tab in the Help Center for RPA Hub:

    -   Now Assist for RPA Hub
    -   High density robot
-   **[SAP connector](https://www.servicenow.com/docs/access?context=sap-connector&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

The SAP connector helps identify the screens and elements and automating workflows on the SAP GUI. For example, create and save a vendor entry. The SAP Connector is built by Bristlecone, Inc.

-   **[New methods for Universal app connector](https://www.servicenow.com/docs/access?context=universal-app-connector&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

In the RPA Desktop Design Studio, the following three new methods for Universal app connector are added.

    -   GetValue: Retrieves a value from an element.
    -   SetValue: Assigns a specified value into an element.
    -   Click: Performs a click action on an element.

</td></tr><tr><td>

Recommended Actions for Operational Technology Service Management \(OTSM\)

</td><td>

-   **[Apply Recommended Actions to your Operational Technology incidents](https://www.servicenow.com/docs/access?context=use-recommended-actions-ot-incidents&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Use Recommended Actions to see relevant actions that can help resolve your OT incidents.


</td></tr><tr><td>

Regulatory Change Management

</td><td>

-   **[Generating a summary of a regulatory alert](https://www.servicenow.com/docs/access?context=create-a-summary-of-a-reg-alert&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Transform your detailed regulatory information into concise, business-focused summaries that emphasize the most critical changes and impending deadlines. You can significantly cut down the time that is required to interpret complex updates, ensuring that no vital details are overlooked. By streamlining compliance processes, your organization becomes more efficient and minimizes the risks.

-   **[Regulatory mapping with AI](https://www.servicenow.com/docs/access?context=recommendations-for-a-regulatory-alert&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Leverage artificial intelligence to help your organizations identify, track, and manage regulatory requirements that are specific to their industry. AI automates the mapping of incoming regulatory changes to internal business operations, such as citations and control objectives, making it easier to ensure compliance. By analyzing the incoming regulatory changes and vast amounts of internal regulatory data, AI highlights the relevant policies for association and mapping, which helps your organization to streamline the compliance process and reduce manual effort.

-   **[Recommendation contexts and templates](https://www.servicenow.com/docs/access?context=recommendation-contexts&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Enable your administrators to use a framework engine to create decision templates for primary records. This framework simplifies the enterprise decision-making processes and includes the configurable user interface elements that provide contextual insights and improve the display of these elements. By integrating this framework, your organization can help to ensure that every recommendation is both relevant and informed.

-   **[Impact radius extension](https://www.servicenow.com/docs/access?context=add-impacted-area-reg-alert&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Identify the impacted areas of your business operations, such as the citations, control objectives, policies, risks, controls, and authority documents, that you can add to a regulatory alert. You can then conduct a review for implementation acceptance that triggers a change management program by assigning ownership and accountability through a Change Task. Additionally, an existing dashboard was improved so that you can get a clear overview of the impacted business operations.

-   **[Regulatory assessment for a regulatory alert](https://www.servicenow.com/docs/access?context=regulatory-assessment-in-rcm&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

View the new Regulatory assessments related list for a regulatory alert. This list displays the uniquely generated regulatory assessments that are powered by the Smart Assessment Engine application so that you can analyze and track the completion status for compliance users. Your users with the sn\_grc.business\_user role can work on these assessments.


</td></tr><tr><td>

Request Management

</td><td>

-   **[User role for service desk agents](https://www.servicenow.com/docs/access?context=req-mgmnt-roles-instld-itsm&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Improve operational efficiency by providing level 1 or tier 1 service desk agents with access to change, incident, problem, and request records by assigning the sn\_service\_desk\_agent user role.

**Note:**

The sn\_service\_desk\_agent user role is available starting with Service Operations Workspace version 6.1.

-   **[Enhanced security model adoption for Request Management](https://www.servicenow.com/docs/access?context=request-management-architecture&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Prevent unauthorized access to request-related tables using deny ACLs. Non-authenticated user cannot perform any actions such as read, write, delete, create, or report view.

This feature is available for new or zBoot customers with the installation of the ITSM Enhanced Security Features \(com.snc.itsm.enhanced\_security\) plugin. Existing or upgrade customers must test and evaluate in their sub-production instance before installing the plugin and implementing the security change in their production instance.


</td></tr><tr><td>

Resource Management Workspace

</td><td>

-   **[Using Resource Management Workspace](https://www.servicenow.com/docs/access?context=using-rmw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US#section_fmx_yrl_b1c)**
    -   View the Resource status, Remaining capacity, and Utilization columns to the allocation heatmap modal to help resource managers to view detailed insights and the total efforts for Approved and Pending tasks.
    -   Use the Total row in the heatmap modal to view the aggregate utilization for approved and pending tasks.
    -   Update the resource status and the efforts for child assignments using the new modal.
    -   Capture additional details required to the Project manager or Resource manager while creating a New Resource Assignment and New Operational Assignment using the following new fields.
        -   **Name**
        -   **Ready for review**
        -   **Notes**
    -   Access the assigned resource assignments or the parent resource assignment directly from the resource board view.
-   **[Using Resource Management Workspace](https://www.servicenow.com/docs/access?context=using-rmw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US#section_v4k_rtg_1fc)**

View and access the resource assignments from high-level to get an overview of all the resource assignments, based on their states, completion dates, start dates, resources with allocations over their capacity, and resources allocations within their available.

    -   Filter the resource board using the primary attributes and dates to build a custom view.
    -   Edit the dashboard further to manage the data representation view of existing widgets or add new elements to build the required widgets.
    -   Access the custom resource boards from dashboard using the interactive widgets to manage the allocations details.
    -   Edit the Start and End dates, Task efforts, and Resource status for assigned tasks in the top tray using the inline editing feature.

</td></tr><tr><td>

Retail Core

</td><td>

-   **[Retail portal](https://www.servicenow.com/docs/access?context=rahi-retail-portal&version=yokohama&pubname=yokohama-retail-industry&ft:locale=en-US)**

Use the new Retail Portal experience to use self-service tools, view cases, and gain visibility into metrics for your retail organizations.


</td></tr><tr><td>

Retail Task Management Core

</td><td>

-   **[Retail multi-store case](https://www.servicenow.com/docs/access?context=rahi-retail-multistore-case&version=yokohama&pubname=yokohama-retail-industry&ft:locale=en-US)**

Use the multi-store case generator to assign work from HQ to multiple retail locations simultaneously. View and track these cases in the retail portal alongside other requests, monitoring completion status across all assigned locations.


</td></tr><tr><td>

Sales Agreement Management

</td><td>

-   **[REST APIs for Sales Agreement Management](https://www.servicenow.com/docs/access?context=sales-agreement-mgmt&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

Import, export, and synchronize sales agreements with external systems through REST APIs.


-   **[Request Tracker on Sales Agreement Management](https://www.servicenow.com/docs/access?context=sales-agreement-mgmt&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

Enable agents to monitor the progress of sales agreement creation from quotes by using the Request Tracker.


</td></tr><tr><td>

Sales Forecasting

</td><td>

-   **[View the Sales Forecasting dashboard](https://www.servicenow.com/docs/access?context=using-sales-forecasting&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

Sales Forecasting uses data from the opinions and insights of your sales representatives reflecting how they feel about the deals in their pipeline. View the dashboard to see the sales forecast for your teams in various stages. You can see the total amount of opportunity in each stage for selected time periods or teams.

-   **[Categorizing the sales opportunities](https://www.servicenow.com/docs/access?context=configure-forecast-categories&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

Categorize the opportunities in the system based on the probability of closing the sales deal.

-   **[Set up sales team hierarchy](https://www.servicenow.com/docs/access?context=setup-sales-group&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

Set up the sales teams and assign managers to each team. Once the users, team, and opportunity data is added, and a selection of categories, you can calculate the forecast for any group or specific sales team and view the dashboard.

-   **[Set up Sales Quota Management](https://www.servicenow.com/docs/access?context=setup-sales-quota&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

Assign quota targets to sales representatives and managers for specific periods. A **Quota** column displays the sales target for the managers and their team. The **Gap** column displays the remaining target amount to achieve the required quota target.

-   **[Set up forecast schedule](https://www.servicenow.com/docs/access?context=setup-forecast-schedule&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

Create a forecast scheduled job to update or create the forecast data at a specific time or on a recurring schedule. The forecast scheduled job automatically fetches all the opportunities in the system and generates forecast data.


</td></tr><tr><td>

Security Incident Response

</td><td>

-   **[Process Mining for security incidents](https://www.servicenow.com/docs/access?context=sir-process-mining&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Identify factors contributing to delays in processing Security Incident Response \(SIR\) incidents that take a long time to close or resolve by scanning historical SIR records through Process Mining. Time-consuming factors can include multiple reassignments, prolonged hold times, and periods of inactivity.

-   **[CrowdStrike Next-Gen SIEM integration](https://www.servicenow.com/docs/access?context=crowdstrike-next-gen-integration-secops&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

As a Profile Admin:

    -   Discover CrowdStrike Next-Gen SIEM detections that are candidates for security incidents and automate the creation of these security incidents.
    -   Create detection profiles.
    -   Map CrowdStrike Next-Gen SIEM Detection and Events Fields to SIR security incident fields.
    -   Filter CrowdStrike Next-Gen SIEM defects.
    -   Aggregate detections to existing open security incidents so that you don't have to create duplicate security incidents.
    -   Schedule ongoing detection ingestion.
    -   Automate CrowdStrike Next-Gen SIEM detection status updates for Security Incident Response.
    -   Synchronize CrowdStrike Next-Gen SIEM detection comments with SIR Work notes.
-   **[Create and name an event profile for the Splunk Enterprise Security event ingestion integration](https://www.servicenow.com/docs/access?context=splunk-event-ingest-create-profile-security&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**
    -   Enables bidirectional updates and closure synchronization between Splunk ES and Splunk integrations.
    -   Enables retrieval of historical, and ongoing data including closed events, with an option to pull the closed events into the ServiceNow Splunk ES instance.
    -   Receive updates for the mapped fields in SIR.
-   **[Components installed with Security Incident Response](https://www.servicenow.com/docs/access?context=installed-with-sir&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

A new Profile Admin role \(sn\_si.ingestion\_profile\_admin\) provides access to configure plugins, and create, edit, delete, and manage profiles for the Splunk, Splunk ES, and Azure Sentinel Integration for Security Operations application.

-   **[Add indirectly linked VITs to CVEs](https://www.servicenow.com/docs/access?context=configure-mitre-att-ck-properties&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Identify all the Third-Party Entities \(TPEs\) associated with a Common Vulnerabilities and Exposures \(CVE\) and then calculate and display the total number of vulnerable items \(VITs\) indirectly linked to those CVEs through the TPEs by setting the sn\_ti.include\_cve\_vit\_indirect\_relation property.

-   **[Configure on-call schedules](https://www.servicenow.com/docs/access?context=on-call-schedule-sir&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

As an admin:

    -   Create a shift and assign or remove members to/from the shift.
    -   Create/edit on-call schedules for groups.
    -   View any group’s on-call schedule, including those to which they belong.
As an analyst:

    -   Specify your availability and preferred contact methods.
    -   View your on-call schedule and see other members of your shift.
-   **[Configure report templates in Security Incident Response](https://www.servicenow.com/docs/access?context=daily-status-sir&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

As an admin, create report templates that can be used to generate an incident summary or an executive summary for analysis and sharing.

As an analyst, use the templates to generate analyst summary or executive summary reports for a SIR incident that can be shared over email.

-   **[Security Incident Response conference call integration](https://www.servicenow.com/docs/access?context=sir-conf-call-capability&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Initiate conference calls using communication channels such as Microsoft Teams, Cisco Webex, or Zoom with customers and peer agents to resolve security incidents over a call by using the SIR conference call feature.

-   **[Enhancements to relationship graphs](https://www.servicenow.com/docs/access?context=sir-relationship-graph&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

As an admin:

    -   Define default child nodes to populate in the relationship graph.
    -   Configure relationship labels.
As an analyst:

    -   Add or remove child nodes at the parent node level.
    -   Save the state of the relationship graph.
    -   Retrieve updated data.
-   **[Proofpoint integration for Security Operations](https://www.servicenow.com/docs/access?context=proofpoint-integration-secops-landing&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Proofpoint integration for Security Operations supports integration between SOAR \(Security Orchestration, Automation, and Response\) and Proofpoint Targeted Attack Protection \(TAP\) software. This integration provides the following benefits:

    -   Detect and block threats such as business email compromise and tags suspicious emails for tracking, analysis, and audit.
    -   Import data to automatically create security incidents for email events that are not captured by TAP products.
-   **[Data Loss Prevention Incident Response Analyst Workspace](https://www.servicenow.com/docs/access?context=using-dlp-ops-portal&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Preview the evidence file of the incident from either the Data Loss Prevention analyst workspace or the DLP end user workspace.


</td></tr><tr><td>

Security Posture Control

</td><td>

-   **[Create a custom API service graph connector in the Security Posture Control workspace](https://www.servicenow.com/docs/access?context=spc-creating-sgc-template&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Use generative AI to help your developers create SPC API connectors quickly with the Connector builder framework module in the Security Posture Control workspace. With a Now Assist skill that is included with the Now Assist for Vulnerability Response application, your developers have the option to automate steps in the Connector builder framework.

    -   You have the option to automate the steps for selecting API templates, populating request and header parameters, and response field mapping with generative AI.

**Note:** You must install [Yokohama Patch 11](../quality/yokohama-patch-11.md) of the Now Assist for Vulnerability Response application to have access to the generative AI skill for the Connector builder framework. See the [Now Assist for Security Incident Response release notes](../security-operations/secops-now-assist-security-operations-rn.md) and [Supporting information for Now Assist for Vulnerability Response](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-vr&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US) for more information.

    -   Use your custom API connector to integrate with security tools and import asset data that is based on the unique requirements of your environment.
    -   Help your cybersecurity teams monitor your overall security posture and identify assets that are missing key security tools with the API connectors that you build.
-   **[Enhancements to policies and asset profiles included with the Security Posture Control application](https://www.servicenow.com/docs/access?context=spc-policies-overview&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Get insights into your overall security posture and configuration gaps in your security tools using new policies and asset proﬁles that are included with the Security Posture Control application. Activate these asset proﬁles and policies in the Security Posture Control workspace so that you can identify gaps in configuration or coverage for the following tools:

    -   CrowdStrike
    -   Microsoft Intune, Defender, and SCCM
    -   HCL Big Fix
    -   SentinelOne
    -   Qualys
    -   Rapid7
-   **[SentinelOne integration for mitigation controls monitoring](https://www.servicenow.com/docs/access?context=spc-controls-policies-for-edr&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

You can import SentinelOne mitigation controls data with this integration to help you detect which mitigation controls are on your assets. Use this integration with the asset and software data that you import with the SentinelOne Service Graph Connector to help you monitor your security tool coverage on your enterprise assets.

-   **[Service Graph Connector for Netskope](https://www.servicenow.com/docs/access?context=sgc-netskope-integration&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

This product pulls in asset inventory data for hardware and software from the Netskope database into the ServiceNow Configuration Management Database \(CMDB\) application.


</td></tr><tr><td>

Self-service and omnichannel engagement for CSM

</td><td>

-   **[Business Portal](https://www.servicenow.com/docs/access?context=configure-business-portal&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Support your customers through the Business Portal self-service capabilities, such as knowledge articles, service catalogs, case management, Virtual Agent, and others. Help reduce maintenance effort through low-code configurations on pages with configurable widgets.

-   **[Email as an Interaction](https://www.servicenow.com/docs/access?context=omnichannels-communicating-customers&version=yokohama&pubname=yokohama-customer-service-management&section=email-channel&ft:locale=en-US)**

Enhance case management with the Email as an Interaction feature.

    -   Transform emails into interactions, enabling customer communication to be tracked in a central location and help avoid unnecessary case creation.
    -   Manage straightforward customer inquiries via email, create cases for more complex issues, or link emails to existing cases.
    -   Notify agents on email responses received from customers.
-   **[Contact Center Integration Core](https://www.servicenow.com/docs/access?context=contactcenter-integration&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

As an admin, import data automatically from a third-party contact center as a service \(CCaaS\) application to facilitate external routing and third-party telephony integration in their ServiceNow® instance.

**Note:** The Contact Center Integration Core is a framework that includes voice call features, which doesn't work unless CCaaS implements it.

    -   Import records such as queues, skills, and wrap-up codes from a third party into your ServiceNow instance.
    -   Maintain data consistency between your ServiceNow instance and third-party systems. Verify that chats and cases are routed to the correct agent and that the correct wrap-up codes are available when dispositioning an interaction.
-   **[Interaction Controls Component \(ICC\)](https://www.servicenow.com/docs/access?context=contact-center-integration-with-icc&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

As an agent, manage calls, such as muting, holding, and transferring, directly within the Configurable Workspace. As a part of the new Voice interaction page experience, the ICC framework helps improve workflow efficiency and promotes a consistent agent experience across all channels.

**Note:** ICC must be integrated with your specific Contact Center as a Service \(CCaaS\) plugin to establish the telephony connection.

Connect customers with field agents or third-party support teams in the embedded call interface. Choose between the following transfer options:

    -   Consult transfer: Share the call context with the external contact before transferring the customer.
    -   Blind transfer: Immediately transfer the call to the external contact.
-   **[OpenFrame Integration to Interaction Controls Component \(ICC\)](https://www.servicenow.com/docs/access?context=interaction-controls-component&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

ICC is a new component for a native call controls interface embedded in Agent Workspace. With the ICC component, you can do the following:

    -   Create the state context in OpenFrame to read the state of idle and active call state, and the state of the transfer.
    -   Provide iframe sandbox parameters to allow iframe access to security features and to enable additional iframe restrictions.
    -   Create an extension point implementation to create and get phone log segments.
-   **[Integrating Conversational SMS with AWS End User Messaging](https://www.servicenow.com/docs/access?context=conversational-sms-integration-amazon&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Integrate the ServiceNow SMS channel with AWS end-user messaging to engage in conversations with Now Virtual Agent and live agents to address and resolve any customer queries or issues.


</td></tr><tr><td>

Service Catalog

</td><td>

-   **[Use non-English language for creating or editing catalog items](https://www.servicenow.com/docs/access?context=create-item-cat-builder&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

Enable your users to use supported languages when creating or editing catalog items. A non-English language user can create or edit a catalog item in their language that is supported in Catalog Builder. For example, if a Spanish language user logs in to Catalog Builder and creates or edits an item, the Spanish version of the item is created or updated.


</td></tr><tr><td>

Service Exchange

</td><td>

-   **[Remote Catalog Item Client Scripts](https://www.servicenow.com/docs/access?context=service-bridge-v2-add-scripts-to-rrp&version=yokohama&pubname=yokohama-service-bridge&ft:locale=en-US)**

Provider: Perform more complex tasks and gain better control over the completeness and correctness of catalog requests from the consumer by including catalog client scripts, UI Policy scripts, and other common scripts that consumers can choose to include for Remote Catalog items.

-   **[Copy From Service Catalog Item to Remote Catalog Item](https://www.servicenow.com/docs/access?context=service-bridge-v2-copy-catalog-as-rrp&version=yokohama&pubname=yokohama-service-bridge&ft:locale=en-US)**

Providers: Eliminate the need to re-create catalog items manually in the Service Exchange remote catalog by copying single and multiple catalog items through the UI to remote record producers that can be synchronized to the consumer instance.

-   **[Transform Mapping Assist](https://www.servicenow.com/docs/access?context=now-assist-tmt-exploring&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Providers: Streamline the transformation mapping process and reduce errors by generating transform mappings between provider and consumer tables automatically using the Transform Mapping Assist feature that leverages the NOW large language model \(LLM\).

-   **[Consumer Variable Sets](https://www.servicenow.com/docs/access?context=service-bridge-v2-consumer-variables&version=yokohama&pubname=yokohama-service-bridge&ft:locale=en-US)**

Consumers: Manage requested content and flow better by adding additional variables to add customization to your remote record producers.


</td></tr><tr><td>

Service Graph Connector Integration for Claroty CTD

</td><td>

-   **[View the class mappings available for the Service Graph Connector](https://www.servicenow.com/docs/access?context=sgc-claroty-ctd-classes&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Use the **Claroty CTD SGC Class Mappings** table to view the available class mappings and targeted CMDB classes.

-   **[Avoid importing empty rack slots](https://www.servicenow.com/docs/access?context=configuring-sgc-claroty-ctd-guided-setup&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

During import, empty rack slots are removed to avoid importing them into the CMDB.

-   **[Capture firmware version of devices](https://www.servicenow.com/docs/access?context=sgc-claroty-ctd-classes&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Use the Firmware Installation \[cmdb\_firmware\_install\] table to capture the firmware version of your Service Graph Connector Integration for Claroty CTD devices.

-   **[Use the ire\_criterion\_attribute in the OT Entity \[cmdb\_ot\_entity\] table](https://www.servicenow.com/docs/access?context=sgc-claroty-ctd-classes&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

The ire\_criterion\_attribute acts as a criterion attribute for an OT entity-related entry and helps avoid entity update issues.

-   **[Clean up serial number data](https://www.servicenow.com/docs/access?context=sgc-claroty-ctd-classes&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Clean up the serial number \[cmdb\_serial\_number\] records imported into the Source \[sys\_object\_source\] table from the Service Graph Connector Integration for Claroty CTD with a fixed script. This script establishes that a null pointer exception doesn't occur when the serial number and MAC address are the same. The script runs automatically when the plugin is upgraded.


</td></tr><tr><td>

Service Graph Connector for Microsoft Defender for IoT \(Azure\)

</td><td>

-   **[View the class mappings available for the Service Graph Connector](https://www.servicenow.com/docs/access?context=sgc-microsoft-d4iot-azure-classes&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

View the available class mappings and targeted CMDB classes on the MSFT D4IoT Azure SGC Class Mappings page.

-   **[Capture firmware version of devices](https://www.servicenow.com/docs/access?context=sgc-microsoft-d4iot-azure-classes&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Firmware versions of your Service Graph Connector for Microsoft Defender for IoT \(Azure\) devices are captured in the Firmware Installation \[cmdb\_firmware\_install\] table.

-   **[Use the ire\_criterion\_attribute in the OT Entity \[cmdb\_ot\_entity\] table](https://www.servicenow.com/docs/access?context=sgc-microsoft-d4iot-azure-classes&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

The ire\_criterion\_attribute identifies configuration items \(CIs\) for an OT entity-related entry and helps avoid entity update issues.

-   **[Actively scan device data from Microsoft Defender for IoT with the Site Mappings table](https://www.servicenow.com/docs/access?context=actively-scan-device-data-msft-azure&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Access the Site Mappings table to actively scan devices from Microsoft Defender for IoT and assign them to a site in your ServiceNow instance.


</td></tr><tr><td>

Service Observability

</td><td>

-   **[Create and manage data mappings](https://www.servicenow.com/docs/access?context=create-and-manage-observability-data-mappings&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Map services in the CMDB Workspace to the data from a connected application performance monitoring \(APM\) data source. Service Observability supports Dynatrace and New Relic. This mapping lets you view metrics from entities deep within your system, like a database or host, that might be affecting the health of a service.

Starting in version 1.7.3, metrics from Datadog are supported.

Starting in version 1.7.3, you can map Business Services and Service Offerings to APM data. Service Offerings are not available in Xanadu.

-   **[View overall service health](https://www.servicenow.com/docs/access?context=view-overall-service-health&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Use the Overview tab to view rate, error, and duration \(RED\) metrics from the APM related to a service. You can also view related open alerts, incidents, and change requests from the Configuration Management Database \(CMDB\) to help identify possible causes and blast radius.

-   **[View service health metrics](https://www.servicenow.com/docs/access?context=view-service-health-metrics&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

View the extended health metrics for a service on the new **Observability** tab when issues are found on the **Overview** tab. In addition to the extended health metrics, you can view host and database metrics related to the service based on the configured data mappings.

-   **Customize dashboard templates**

Starting in version 1.6.4, customize the templates used to display dashboards in the **Overview** and **Observability** tabs.

-   **Domain separation**

Starting in version 1.6.4, Service Observability can be run in separate domains.


</td></tr><tr><td>

Service Operations Workspace for ITSM

</td><td>

-   **[User role for service desk agents](https://www.servicenow.com/docs/access?context=roles-in-sow&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Enable tier 1 service desk agents to quickly gather and verify information by granting the sn\_service\_desk\_agent role, which is accessible when the ITSM Roles plugin \(com.snc.itsm.roles\) is installed.

The sn\_service\_desk\_agent role can be used starting with Service Operations Workspace version 6.1 with the Yokohama release.

-   **[Incident management configuration changes in the Service Operations Workspace Admin Center](https://www.servicenow.com/docs/access?context=manage-admin-console-sow-itsm&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

The Incident record of the Incident Management section in the Service Operations Workspace Admin Center has the following enhancements:

    -   Configure and use response templates to quickly respond to incidents.
    -   Configure additional properties to control incident features such as auto-closing incidents and copying or creating child incidents.
-   **[Reopen an incident in Service Operations Workspace](https://www.servicenow.com/docs/access?context=reopen-incident-sow&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Enable agents with incident write access, callers, or end user who opened the incident to reopen a resolved incident.

-   **[List page enhancements](https://www.servicenow.com/docs/access?context=work-incident-list-page-sow&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

The Service Operations Workspace list page has the following enhancements:

    -   Ability to assign the incident record to yourself if you’re the logged-in user or to reassign it to another user or assignment group.
    -   An animated dot symbol that indicates whether a list has been customized.
-   **[Major incident management record page enhancements](https://www.servicenow.com/docs/access?context=communicating-with-stakeholders-sow&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Enhance incident and major incident-related communications including ad hoc communications and major incident playbooks in SOW by adding DEX Desktop Assistant as a channel.

-   **[Direct approvals in Service Operations Workspace](https://www.servicenow.com/docs/access?context=view-approvals-sow&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Service desk agent can approve records directly within the SOW without having to navigate to the Core UI. By approving records from the SOW, you can reduce response times, and ensure quick resolution of the tasks.

-   **[Automatically close an interaction in Service Operations Workspace](https://www.servicenow.com/docs/access?context=automatically-close-interaction-sow&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Interactions are now automatically closed when the associated incident is resolved, streamlining the workflow and ensuring consistent status updates.

-   **[Enhanced side panel features](https://www.servicenow.com/docs/access?context=get-field-recommendations&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    -   Access the Recommended Actions and AI Search features from the contextual side panel for request items and catalog tasks.
    -   Determine the order of the items in the contextual side panel.
The Recommended Actions and AI Search features are now available in the contextual side panel for both request Items and catalog tasks.

-   **[Enable email redirection to SOW from SOW Admin Center](https://www.servicenow.com/docs/access?context=manage-admin-console-sow-itsm&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Stay within the SOW and work on your tasks more efficiently by enabling email redirection. By enabling email redirection within the SOW Admin Center, you can simplify communication management, enabling the users to stay within the SOW and focus on their tasks without interruption.

-   **[Initiate a chat from Sidebar in Service Operations Workspace](https://www.servicenow.com/docs/access?context=initate-sidebar-chat-sow&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Use Slack as a primary mode of communication from the Sidebar so you can send direct messages to users without having to leave the SOW.

-   **[View the device health of user assets](https://www.servicenow.com/docs/access?context=work-on-interaction-sow&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

DEX is integrated with SOW to monitor CIs or assets associated with SOW records such as incidents and interactions to determine the health of devices. You can view the device health information of the user's assets on the Record information side panel of the incident and interactions record page. This feature is available only if the DEX plugin \[sn\_dex\] is installed and DEX monitoring is enabled for the asset.

-   **[Using MRA Async for adding child incident, affected CIs, impacted services and assets](https://www.servicenow.com/docs/access?context=view-update-inc-overview-tab&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

When adding a list containing more than 50 child incidents, affected CIs, impacted services or assets from the **Overview** tab or **Related records** tab of an incident or problem record, the Multiple Record Associator \(MRA\) component batch processes in async and helps adding them in background thereby increasing the overall performance of the system. This feature works only if the number of items to be added is more than 50 as the **async Threshold** configuration property is set to 50.

-   **[Viewing the device health of the user assets](https://www.servicenow.com/docs/access?context=work-on-interaction-sow&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

View the device health information of the user's assets from the Assigned assets section on the Record information side panel of the incident and interactions record page. This helps in providing a quick resolution to the user. This feature is available only if the DEX plugin \[sn\_dex\] is installed and DEX monitoring is enabled for the asset.

-   **[Guided tours for SOW](https://www.servicenow.com/docs/access?context=play-guided-tour-sow&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Learn about Service Operations Workspace for ITSM through a sequence of interactive steps that guide you through a specific concept or process.

The following guided tours are available:

    -   Create an incident task
    -   Overview of the Interaction record in SOW
-   **[Enhanced security model adoption in Service Operations Workspace](https://www.servicenow.com/docs/access?context=components-installed-investigate&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Help prevent unauthorized access to the tables of the following applications with Deny-Unless ACLs:

    -   Metrics and CI actions framework
    -   Remedial actions framework
    -   Agent client collector for investigation
    -   Microsoft Endpoint Configuration Manager for Investigation
A Deny-Unless authentication ACL restricts access for a non-authenticated user, such as a public role user. Without access, the user can't perform any actions on the tables related to the above mentioned applications, including reading, writing, deleting, creating, or accessing the report view. This feature is available to both new \(zboot\) and upgrade instances.

-   **[Known error article for a problem](https://www.servicenow.com/docs/access?context=work-on-problem-sow&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Starting in version 7.1, share the workaround for a problem and deflect additional incidents by creating a known error article for the problem.

-   **[On-Call Scheduling configurations in Admin Center](https://www.servicenow.com/docs/access?context=manage-admin-console-sow-itsm&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Starting in version 7.1, use the simplified navigation from Admin Center to manage configurations for On-Call Scheduling in Service Operations Workspace for ITSM. It improves the administrator's experience.

-   **[Configure Notify in SOW](https://www.servicenow.com/docs/access?context=configure-notify-sow&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Configure the provider preferences for Notify to manage the conference calls in Service Operations Workspace.

-   **[Create CAB meetings in Service Operations Workspace](https://www.servicenow.com/docs/access?context=cm-create-cab-meeting-sow&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Define and create Change Advisory Board \(CAB\) meetings, invite attendees and dynamically populate agenda items for each meeting in Service Operations Workspace.

Run CAB meetings through CAB Workbench, available within Service Operations Workspace to review and authorize change requests. For more information, see [Conduct a CAB meeting in the CAB workbench](https://www.servicenow.com/docs/access?context=cm-manage-cab-meeting-workbench-sow&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).


</td></tr><tr><td>

Service Portal

</td><td>

-   **[Analyze the performance of portal pages and their widgets](https://www.servicenow.com/docs/access?context=analyze-page-performance&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

Set benchmarks against which to analyze the performance of a portal page. Identify widgets on the page that don't meet the performance benchmarks and view details about their performance.

-   **[Compare a cloned widget with its base widget](https://www.servicenow.com/docs/access?context=compare-with-base-system&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

Compare cloned widgets with the base widget from which they were cloned. View differences between the code of the cloned widget and the base widget highlighted in the code comparator.


</td></tr><tr><td>

Service Portfolio Management

</td><td>

-   **[Edit and manage service portfolios in Service Portfolio Management](https://www.servicenow.com/docs/access?context=SPM2-edit-manage-portfolios&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Use the updated options to edit and manage your service portfolios:

    -   [Manage the CSDM life cycle fields in Service Portfolio Management](https://www.servicenow.com/docs/access?context=SPM2-lifecycle-fields&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)
    -   [Remap service portfolio taxonomy nodes in Service Portfolio Management](https://www.servicenow.com/docs/access?context=SPM2-remap-taxo-nodes&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)
-   **[Use Service Portfolio Management services](https://www.servicenow.com/docs/access?context=SPM2-services&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

Recognize the updated label for technical services. The updated label aligns with the CSDM, version 5.0. Even though the table name hasn't changed, the services label is updated in the Service Portfolio Management application and in all ServiceNow applications or workspace environments that display services. The label for service offerings remains the same for all releases: Service offering in the \[service\_offering\] table.

    |Table name|Label in Xanadu and prior releases|Label in Yokohama and later releases|
    |----------|----------------------------------|------------------------------------|
    |\[cmdb\_ci\_service\_technical\]|Technical Service|Technology Management Service|


</td></tr><tr><td>

Service Reliability Management

</td><td>

-   **[Enhance monitoring for distributed teams with Express List](https://www.servicenow.com/docs/access?context=express-list&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Improve monitoring with Express List. Express List replaces the **Alerts** tab and helps distributed SRM teams focus on the services, priorities, or alerts that matter to them.

-   **[Track SLO update history](https://www.servicenow.com/docs/access?context=sr-edit-sli-slo&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

View and track SLO update history with new naming conventions. Edited SLOs now receive unique names, such as Uptime \(1\) or Uptime \(2\), instead of keeping their original names. This update improves clarity and helps you distinguish between versions.

-   **[Add SLOs to change approval policies](https://www.servicenow.com/docs/access?context=sr-add-change-approval-slos&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Define change approval policies to approve updates or modifications in your system. You can now add the following policy inputs, helping you integrate critical information into the approval process:

    -   SLO with the lowest percentage of error budget remaining
    -   SLO with the highest burn rate
-   **[Assign teams to TSOs](https://www.servicenow.com/docs/access?context=sr-add-service&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Manage your services effectively by assigning teams to TSOs. TSOs, which are specific components within a parent technical service, can now be used in the SRM service list. Assigning SRM teams to TSOs helps decentralized teams focus on the services they’re responsible for.

-   **[Stay connected and keep services reliable with ITOM Mobile Agent](https://www.servicenow.com/docs/access?context=itom-mobile-landing&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Starting in version 6.3, use ITOM Mobile Agent to access SRM features on iOS and Android devices. With ITOM Mobile Agent, you can track alerts, manage incidents, and work on tasks on the go. You can also manage on-call schedules by checking shifts, requesting time off, and filling gaps.

-   **[Create SLIs on configuration items](https://www.servicenow.com/docs/access?context=sr-create-slo-sli&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Starting in version 6.3, filter an SLI to a specific configuration item within the parent service hierarchy. This feature lets you monitor the individual components of a service, helping you accurately track service health and identify root causes faster.

-   **[Keep teams informed with notification destinations](https://www.servicenow.com/docs/access?context=create-notification-destination&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Starting in version 6.4, send notifications about error budget policy violations to notification destinations. The first supported destination is Microsoft Teams, which lets you post details in specific channels and link back to SRM for further investigation.

-   **[Monitor service reliability in a dashboard](https://www.servicenow.com/docs/access?context=sr-service-dashboard-visualizations&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Starting in version 6.4, use the Service reliability dashboard to monitor and manage service performance. The dashboard offers multiple visualizations to help you track error budgets, monitor SLOs, and identify issues across your services. Starting in version 6.4.1, you can select charts to access further details and use the new SLO table to monitor reliability.

-   **[Customize team approval settings with more flexibility](https://www.servicenow.com/docs/access?context=sr-add-approval-teams&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Starting in version 6.4, customize team governance with more flexibility and less manual effort. You can assign different approval teams for new and existing team requests. The customization options are also fully available in the Service Operations Workspace Admin Center and no longer require manual setup in the Catalog Builder.


</td></tr><tr><td>

ServiceNow AI Lens

</td><td>

-   **[ServiceNow AI Lens UI enhancement](https://www.servicenow.com/docs/access?context=servicenow-lens-explore&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Use ServiceNow AI Lens to launch the scanner window by using the context defined in Lens actions or as a standalone application. You can preview the gathered insights or extracted data. You can also see the logged-in user and instance details.

-   **[Use Lens actions to customize Lens behavior](https://www.servicenow.com/docs/access?context=servicenow-lens-actions&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**
    -   Define Lens behavior depending on how ServiceNow AI Lens is triggered and what context is set. With Lens actions, you can customize how a classic form is auto-filled. You can define default instructions, trigger options, custom context, transform response logic, and post processing instructions for the ServiceNow AI Lens execution.

For example, you can define a Lens action that is used when Lens is triggered from an instance to populate a form of a table. You can also define form fields that must be used as context.

    -   As part of your integration logic, configure a Lens action as one of the steps to invoke a ServiceNow AI Lens service from any part of the ServiceNow AI Platform, such as a workspace form or portal.
-   **[Use ServiceNow AI Lens in Virtual Agent](https://www.servicenow.com/docs/access?context=enabling-lens-for-virtual-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Trigger ServiceNow AI Lens from a Virtual Agent conversation by using ServiceNow AI Lens topic in Virtual Agent.

-   **[Auto-attach images to a record](https://www.servicenow.com/docs/access?context=servicenow-lens-actions&version=yokohama&pubname=yokohama-intelligent-experiences&section=create-sn-lens-recipe&ft:locale=en-US)**

View captured images that are automatically attached to the record that is auto-filled using ServiceNow AI Lens. You can view the images to understand the source of the auto-filled information.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Use Google Gemini and Anthropic Claude on AWS as AI model providers for ServiceNow AI Lens in addition to Azure OpenAI.


-   **[Capture data](https://www.servicenow.com/docs/access?context=servicenow-lens-explore&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Get actionable insights from such visual data as images, handwritten notes and forms, emails, websites, and applications. For example, ServiceNow AI Lens can scan an email to gather data for auto-filling the fields on the Incident form.

-   **[Act on visual data](https://www.servicenow.com/docs/access?context=servicenow-lens-explore&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Provide instructions to Now Assist on what to do with the captured data. For example, you can convert the extracted data into a JSON format.

-   **[Launch from ServiceNow forms](https://www.servicenow.com/docs/access?context=servicenow-lens-explore&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Launch ServiceNow AI Lens from a form to fill the extracted data automatically into the form fields.

-   **[Use as a standalone application](https://www.servicenow.com/docs/access?context=servicenow-lens-explore&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

Use ServiceNow AI Lens as a standalone application for previewing extracted data when you're connected to a ServiceNow instance.


</td></tr><tr><td>

ServiceNow AI Platform core feature

</td><td>

-   **[Add dynamic attributes to a dynamic category](https://www.servicenow.com/docs/access?context=add-dynamic-attributes-dynamic-category&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Add individual attributes or a group of attributes to a dynamic category.

-   **[Reference a dynamic attribute or a list of dynamic attributes](https://www.servicenow.com/docs/access?context=create-dynamic-schema-reference&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Build a dependency between a dynamic attribute store field and either a dynamic attribute or a list of dynamic attributes.

-   **[Edit data in remote tables on an instance](https://www.servicenow.com/docs/access?context=create-remote-table-script&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

Insert, update, and delete data in an external data source from a remote table on an instance when you enable editing for the table. Customize the script definitions that enable you to insert, update, or delete data from a remote table.


</td></tr><tr><td>

ServiceNow Add-in for Microsoft 365

</td><td>

-   **[Create a manifest file](https://www.servicenow.com/docs/access?context=create-ms365-addin-manifest&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Create a manifest file with the configurations that you want to enable for the ServiceNow Add-in for Microsoft 365.

-   **[Map email fields to a catalog item](https://www.servicenow.com/docs/access?context=map-email-catalog&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Map fields from an email or meeting invite to copy and auto-populate a catalog form.

-   **[Map email fields to a form](https://www.servicenow.com/docs/access?context=map-email-form&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Map fields from an email or meeting invite to copy and auto-populate a ServiceNow form.

-   **[Configure single sign-on for ServiceNow Add-in for Microsoft 365](https://www.servicenow.com/docs/access?context=configure-sso-sn-addin-ms365&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Enable employees to access the add-in from any Microsoft 365 app without having to sign in to Employee Center.


</td></tr><tr><td>

ServiceNow IDE

</td><td>

-   **[Convert scoped applications for use in the ServiceNow IDE](https://www.servicenow.com/docs/access?context=convert-application-servicenow-ide&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Convert existing scoped applications to support development in source code in the ServiceNow IDE.

-   **[Use TypeScript in JavaScript modules](https://www.servicenow.com/docs/access?context=create-application-servicenow-ide&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Create an application that uses the TypeScript template to use TypeScript in modules and compile them to JavaScript when building your application.

-   **[Use npm packages from private registries as third-party libraries](https://www.servicenow.com/docs/access?context=use-library-private-npm-registry&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Install npm packages from a private registry to use as third-party libraries in your application.

-   **[Switch between development experiences](https://www.servicenow.com/docs/access?context=servicenow-ide-user-interface&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Work in the right environment for your task by using the experience switcher to switch between developing in ServiceNow IDE, ServiceNow Studio, and Creator Studio.


</td></tr><tr><td>

ServiceNow SDK

</td><td>

-   **[Init command replaces create and convert commands](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&version=yokohama&pubname=yokohama-application-development&section=now-sdk-create-command&ft:locale=en-US)**

Create a custom scoped application or convert an existing scoped application from a ServiceNow instance or local directory to support development in source code using the `now-sdk init` command.

-   **[Download application metadata and transform it into source code](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&version=yokohama&pubname=yokohama-application-development&section=now-sdk-transform-command&ft:locale=en-US)**

Download application metadata \(XML\) from a ServiceNow instance and transform the metadata into ServiceNow Fluent source code.

-   **[Refer to content from a file in ServiceNow Fluent APIs](https://www.servicenow.com/docs/access?context=servicenow-fluent&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Use content from files in ServiceNow Fluent APIs by referring to the file from a property using the syntax `Now.include('path/to/file')`.

-   **[Map metadata to custom directories](https://www.servicenow.com/docs/access?context=servicenow-fluent-api-reference&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Map any application metadata to output directories that load only in specific circumstances using the `$meta` property in ServiceNow Fluent APIs.

-   **[Specify a path to a custom tsconfig.json file](https://www.servicenow.com/docs/access?context=building-applications-source-code&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US#application-structure)**

Use the `tsconfigPath` parameter in the `now.config.json` file for your application to specify the location of a `tsconfig.json` file with custom options for transpiling TypeScript into JavaScript during the build process.


</td></tr><tr><td>

ServiceNow Studio

</td><td>

-   **[Change your development experience in ServiceNow Studio](https://www.servicenow.com/docs/access?context=change-your-development-experience&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Use the best tool for your app development by switching between Creator Studio, ServiceNow Studio, and ServiceNow IDE.

-   **[Summarize the contents of an app in ServiceNow Studio](https://www.servicenow.com/docs/access?context=summarize-an-app-in-servicenow-studio&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Help prevent duplicate app creation by summarizing the contents of an app using Now Assist app summary generation in ServiceNow Studio and using the summary if accurate as the app description.

-   **[Modify an app's settings in ServiceNow Studio](https://www.servicenow.com/docs/access?context=modify-an-apps-settings-in-servicenow-studio&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Change settings or see related links for an app from the app details page. Refresh your app to load updated details.

-   **[Create an application in ServiceNow Studio](https://www.servicenow.com/docs/access?context=create-an-application-in-servicenow-studio&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

In the November 2024 release, only admins could create apps in ServiceNow Studio. Now, users with Guided Application Creator \(GAC\) roles can also create applications.

-   **[File Navigator performance has been improved for large applications](https://www.servicenow.com/docs/access?context=configuring-servicenow-studio&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

As of version 27.2.4, smaller apps load all files on open, while larger apps \(exceeding a configurable limit\) load a subset initially, with additional files available on demand. Search for files in larger apps will perform server-side calls to decrease load times. Contact your ServiceNow support team to change the app size limits.

-   **[Create an app file in ServiceNow Studio](https://www.servicenow.com/docs/access?context=sn-studio-create-app-file&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

As of version 27.2.4, use the new full-page, guided file creation experience to create any type of file for which you have permission.

-   **[Viewing app origination information in ServiceNow Studio](https://www.servicenow.com/docs/access?context=viewing-app-origination-information-in-sns&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

As of version 27.2.4, the app details page for each app shows which development environment your app was created in. Use this information to switch between environments as needed in the course of app development and deployment.


</td></tr><tr><td>

Sidebar

</td><td>

-   **[Exploring Sidebar](https://www.servicenow.com/docs/access?context=exploring-sidebar&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Integrate Sidebar and Slack to enable the users of both platforms to seamlessly collaborate with each other.

-   **[Using Sidebar](https://www.servicenow.com/docs/access?context=using-sidebar&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Create standalone Sidebar conversations that aren’t associated with a specific record.

-   **[Using Sidebar](https://www.servicenow.com/docs/access?context=using-sidebar&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Create private discussions on a record that are accessible only to the participants within that discussion.


</td></tr><tr><td>

Skills Foundation

</td><td>

-   **[Bring in skills through Skills import](https://www.servicenow.com/docs/access?context=import-and-validate-custom-skills-onboarding&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

Import skill sets from the Workday Employee spoke using the existing import flow in the Skills Workspace. The imported sets of skills can either be the full list of skills from a given input or a subset.

Import skills data from the external systems with the new Integration option in the Skills import.

Automatically identify skills that are similar to the existing skills in the library \(cmn\_skills\) and display them in the Existing matches section.

Import skills from any external source and harmonize them with the new **Custom import** option.


</td></tr><tr><td>

Smart Assessment Engine

</td><td>

-   **[Copy an assessment template](https://www.servicenow.com/docs/access?context=sae-asmnt-template-duplicate&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Create a copy of an existing smart assessment template, including all questions, sections, and existing configurations. This feature enables you to duplicate a fully configured assessment, so you don't need to recreate the content. You can then customize the copied template to fit new requirements or scenarios.

-   **[Filter unanswered questions](https://www.servicenow.com/docs/access?context=sae-respond-to-asmnt&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US#fig_ztw_wm2_ndc)**

Filter questions in the assessments to display only unanswered questions, helping you focus on the remaining questions.

-   **[Using the template designer](https://www.servicenow.com/docs/access?context=sae-template-designer&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Search for text within assessment sections, subsections, or questions, enabling you to locate specific information or keywords. This feature enhances navigation and enables you to find relevant content without manually scrolling through the entire assessment.

-   **[Auto-copy responses to all templates](https://www.servicenow.com/docs/access?context=combine-assessments&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Replicate your responses across all applicable assessments while combining assessments by enabling the auto-copy feature. It saves time and effort by copying your answers consistently without the need for manual repetition.

-   **[Automate responses](https://www.servicenow.com/docs/access?context=automate-response&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Set up automatic responses for questions to enable assessors to complete assessments efficiently. You can either create default responses for all question types or define a script to fetch and map the values or data to responses.

-   **[Assessment scoring and analysis](https://www.servicenow.com/docs/access?context=scoring-in-assessments&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Calculate meaningful scores for assessment responses at the assessment, section, or subsection levels. These scores can then be used for reporting.

-   **[Post-assessment automation](https://www.servicenow.com/docs/access?context=impact-automation&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Automate actions based on assessment responses. Template designers can predefine actions using a rule engine, such as updating fields, creating follow-up assessments, or generating other records.

-   **[Descriptive images in assessment questions](https://www.servicenow.com/docs/access?context=sae-q-text-create&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Attach descriptive images in the guidance section of the assessment questions. This means that template managers can include helpful visuals to assist respondents, making the instructions clearer and easier to understand.


</td></tr><tr><td>

Software Asset Management

</td><td>

-   **[Gain insights into your publisher license compliance by using Now Assist for Software Asset Management](https://www.servicenow.com/docs/access?context=now-assist-sam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Use generative AI to gain a comprehensive summary of publisher license compliance. The detailed publisher summaries enable you to understand the publisher license compliance details.

-   **[Manage Microsoft 365 license compliance and optimization through Microsoft 365 Guided Setup](https://www.servicenow.com/docs/access?context=playbook-entitlementsetup-workspace&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Get a prescriptive guidance for the tasks that you must perform in the Software Asset Management application, Microsoft 365 admin center, and other applications to configure Microsoft 365. This Guided Setup organizes the configuration activities into various categories so that you can see the list of tasks that need to be performed.

-   **[Optimize Microsoft 365 subscriptions](https://www.servicenow.com/docs/access?context=microsoft-o365&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Optimize how to manage Microsoft 365 licensing with these enhancements:

    -   Auto removal of licenses from the Microsoft 365 admin center by detecting low usage and overlapping subscriptions.
    -   Expanded support for usage-based optimization such as Microsoft 365 E3 Teams and Microsoft 365 government plans.
-   **[Optimize Microsoft Dynamics 365 subscriptions](https://www.servicenow.com/docs/access?context=integrating-with-microsoft365&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**
    -   Receive recommendations to save costs by removing low-usage subscriptions for MRS applications.
    -   Receive guidance on cost-saving strategies while purchasing multiple base subscription licenses for various Microsoft Dynamics 365 applications. Using a combination of base and attach licenses can provide a more cost-effective solution.
-   **[Simplify the activation process for SaaS License Management](https://www.servicenow.com/docs/access?context=request-saas-license-management&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Simplify your activation process by optimizing your SaaS subscriptions. You can activate just the SaaS applications that you want to manage.

-   **[SaaS security permissions](https://www.servicenow.com/docs/access?context=create-integration-profile&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

While integrating your SaaS applications, you can now grant the minimum permissions required to enable key use cases, such as downloading subscriptions, calculating activity, and reclaiming subscriptions.

-   **[Optimize subscriptions for SAP Ariba](https://www.servicenow.com/docs/access?context=integrate-with-ariba&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Gain visibility to the subscriptions and reclaim stale licenses by integrating your ServiceNow instance with the SAP Ariba application.

-   **[Configure and map users from SaaS portals to ServiceNow AI Platform with ease](https://www.servicenow.com/docs/access?context=map-user-data&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Determine your licensed users by mapping user subscriptions from SaaS applications to users in ServiceNow AI Platform.

-   **[Optimize CrowdStrike subscriptions](https://www.servicenow.com/docs/access?context=integrate-with-crowdstrike&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Software Asset Management now includes support for CrowdStrike products with license metrics such as Sensor Subscription and Reserved Hourly Average Sensor. The introduction of a new license metric group, CrowdStrike, improves data coverage and reconciliation. By managing the entitlements for various CrowdStrike products, including CrowdStrike Falcon Endpoint Protection, CrowdStrike Falcon Discover, and others, you can get better tracking and compliance.

-   **[Manage onboarding of products to support the Software Asset Management \(SAM\) application through SAM Guided setup](https://www.servicenow.com/docs/access?context=playbook-entitlementsetup-workspace&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Get step-by-step guidance on the activities that you must perform to onboard SaaS and on-premises products. The guided setup helps you to create or associate success goals, configure product integrations, create software entitlements, or run reconciliation to get the most out of the Software Asset Management application.

-   **[Manage license compliance for Oracle Database and WebLogic Server deployed on Solaris Logical Domain \(LDOM\)](https://www.servicenow.com/docs/access?context=oracle-licensing-hard-partitioned-environments&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Support Oracle Database and WebLogic Server licensing for Per Processor and Named User Plus \(NUP\) license metrics that are deployed on the hard-partitioned Solaris LDOM infrastructure, also known as Oracle VM Server for SPARC.

-   **[Manage compliance for SAP S/4HANA Cloud Public Edition](https://www.servicenow.com/docs/access?context=integrate-with-hana&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Gain visibility to software usage information and subscriptions by integrating your Software Asset Management application with the SAP S/4HANA Cloud Public Edition. This integration supports the Full User Equivalent \(FUE\) license metric that is used to grant licenses for SAP cloud applications.

-   **[Determine license compliance for Oracle products deployed on Nutanix virtualization technology](https://www.servicenow.com/docs/access?context=software-recon-virt-tech&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

License Oracle Database Server, Options, and WebLogic Server with deployments on the Nutanix virtualization technology.

-   **[Support for revenue-based license metrics for SAP engines](https://www.servicenow.com/docs/access?context=sap-publisher-pack&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Gain the ability to maintain licenses for higher value, revenue-based SAP engine products.

-   **[Leverage machine learning normalization for software recognition in protected government environments](https://www.servicenow.com/docs/access?context=ml-learning-sam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Extend machine learning normalization capabilities to Government Community Cloud \(GCC\) and National Security Cloud \(NSC\) environments.

-   **[Leverage machine learning spend detection in protected government environments](https://www.servicenow.com/docs/access?context=software-spend-detection&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Extend Software Spend Detection capabilities to Government Community Cloud \(GCC\) and National Security Cloud \(NSC\) environments.

-   **[Optimize licensing for IBM Cloud Paks](https://www.servicenow.com/docs/access?context=licensing-ibm-cloud-paks&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Use the IBM License Compliance for Software Asset Management application to track and manage licenses for your IBM Cloud Paks.

-   **[Expand end of life \(EOL\) reporting by creating parent-child relationships between software products](https://www.servicenow.com/docs/access?context=create-parent-child-relationships-between-software-products&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

View, define, or update the parent-child relationships between your software products. Use these relationships to enable your child products to inherit life-cycle dates from their associated parent products.

-   **[View the Export Classification Control Numbers \(ECCNs\) for your software products](https://www.servicenow.com/docs/access?context=view-eccn-software-mappings&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

View the ECCNs that are mapped to your software products. Use this information to identify the products that are subject to U.S. export control regulations so that you can maintain export compliance across your products.

-   **[Create and manage entitlements for your Microsoft 365 From SA and Add-on user subscription licenses \(USLs\)](https://www.servicenow.com/docs/access?context=creating-m365-from-sa-add-on-entitlements&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Create entitlements to track and manage the From SA and Add-on licensing terms for your Microsoft 365 subscriptions. Specify the details of each license, including the license type, license cost, and number of purchased rights. Use this information to determine your license compliance so that you can optimize your licensing costs.

-   **[Improve your compliance position with insights on how your software installations get licensed](https://www.servicenow.com/docs/access?context=install-licenseusage-journey&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Evaluate the installation to license consumption percentages and devise strategies for improving your license usage. Track your installation to license journey by connecting software installations to the licenses consumed and identifying the statuses such as licensed or unlicensed.

-   **[Gain an understanding of how licenses get calculated for your software assets](https://www.servicenow.com/docs/access?context=explanation-rights-post-recon&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Learn how the Software Asset Management application calculates the number of licenses that are required for your software assets with the factors that impact this process.

-   **[Increase the coverage of product life cycles](https://www.servicenow.com/docs/access?context=calculated-lifecycles&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

Expand the life-cycle date calculations to include the custom general availability \(GA\) dates. Additionally, support is also available for the End of Extended Support phase and the End of Support and End of Life phases.


</td></tr><tr><td>

Sourcing and Procurement Operations

</td><td>

-   **[Multi-currency support in Shopping Hub](https://www.servicenow.com/docs/access?context=sh-multicurrency-overview&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

View and select your local currency while shopping for products in Shopping Hub to provide a seamless multi-currency experience.

-   **[Purchase requisition line-level questions in Shopping Hub](https://www.servicenow.com/docs/access?context=prl-question-shoppinghub&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Create configurable, line-level questions during checkout in Shopping Hub. These questions are defined in Catalog Builder and are specific to certain products or product categories.

-   **[Category management tab](https://www.servicenow.com/docs/access?context=category-mgmt-tab&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Access a unified, filter-based view of category performance across spend, savings, pipeline projects, contracts, purchase orders, and suppliers.

-   **[Category analytics](https://www.servicenow.com/docs/access?context=spo-category-analytics&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

View savings opportunities across the sourcing pipeline using the Savings dashboard in the Category Analytics module of the Source-to-Pay Workspace.

-   **[Pipeline management tab](https://www.servicenow.com/docs/access?context=pipeline-mgmt-tab&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Gain insights into savings and pipeline projects to enhance visibility, tracking, and collaboration across teams.

-   **[Report savings when awarding multiple suppliers](https://www.servicenow.com/docs/access?context=report-savings-multiple-suppliers&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Enter the spend and savings data for the sourcing event associated with the pipeline project when awarding multiple suppliers.

-   **[Create a pipeline project from an expiring contract](https://www.servicenow.com/docs/access?context=create-pipeline-expire-contract&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Create a pipeline project directly from an expiring contract using a guided, decision-based workflow.

-   **[Search for punchout products in Employee Center](https://www.servicenow.com/docs/access?context=ec-search-punchout-products&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

In Employee Center, you can search for punchout products directly using the AI search bar. After you search for a product, matching items from the third-party supplier's catalog are displayed on the **Supplier Site Catalog** tab.

-   **[Unified request tracking in Shopping Hub](https://www.servicenow.com/docs/access?context=sh-unified-request-tracking&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

From My Purchases in Shopping Hub, you can search purchased products or services using the original or associated procurement record IDs, tracking details from order to fulfillment. Additionally, you can use keywords or the first three letters of a procurement record type to search for and view your purchases.

-   **[Browse punchout and native catalog items from the Categories and Suppliers lists in Shopping Hub \(SH\)](https://www.servicenow.com/docs/access?context=sh-browse-products&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

In Shopping Hub, you can view both the punchout products and the natively available products from the Categories or the Suppliers list on the Shopping Hub home page.

-   **[Mapping Product Categories and Units of Measure for seamless checkout in Shopping Hub](https://www.servicenow.com/docs/access?context=product-category-mapping-shoppinghub&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

You can map the product categories and units of measure for third-party products to the corresponding model categories. This capability helps to ensure that during checkout, Shopping Hub accurately considers and displays the product category for the purchase order lines \(POL\) and purchase requisition lines \(PRL\) based on your predefined mappings.

-   **[Submit an edit receipt request from Shopping Hub](https://www.servicenow.com/docs/access?context=submit-edit-receipt-request&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Shoppers can submit edit receipt requests from Shopping Hub to correct discrepancies in accepted receipts, ensuring accurate updates to purchase orders, purchase order lines, and received quantities.

-   **[Process an edit receipt request in playbook](https://www.servicenow.com/docs/access?context=playbook-process-edit-receipt&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Fulfillers can review the edit receipt requests and either confirm or reject them. If the request is valid, they can process the request using the Edit a Receipt playbook in the Source-to-Pay Workspace.

-   **[Editing purchase requisitions and orders with cost allocation adjustments](https://www.servicenow.com/docs/access?context=edit-purchase-cost-allocation&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Shoppers can modify purchase requisitions \(PRs\) and purchase orders \(POs\) while maintaining cost allocation across multiple cost centers.

-   **[Spend and Savings Management](https://www.servicenow.com/docs/access?context=spo-spend-mgmt&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Spend and Savings Management \(sn\_spend\_mgmt\) enables category managers to import and maintain their organization’s category taxonomy. Integrating this taxonomy into ServiceNow helps streamline procurement processes, monitor spend, and assess savings more efficiently at the category level.

-   **[Return a product](https://www.servicenow.com/docs/access?context=return-a-product&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Shoppers can now initiate replacements for goods directly from the Shopping Hub/EC. Previously, only returns for refunds were supported. This enhancement allows shoppers to replace faulty or unsatisfactory items, offering greater flexibility and improving the overall shopping experience.

-   **[Using Now Assist for Contract Management in Sourcing and Procurement Operations](https://www.servicenow.com/docs/access?context=use-now-assist-cmpro-spo&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Extract metadata from a signed contract attached in a contract repository record and analyze a contract document with agentic AI to identify non-standard and missing clauses.

-   **[Now Assist for Sourcing and Procurement Operations \(SPO\)](https://www.servicenow.com/docs/access?context=now-assist-spo&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Activate the following new skills for Now Assist for SPO:

    -   Negotiation summarization for fulfillers: Summarize negotiations to keep fulfillers informed on their current status, progress, and action items.
    -   Negotiation event summarization for fulfillers: Summarize negotiation events to keep fulfillers informed on their current status, progress, and action items.
    -   Purchase order summarization for requesters: Summarize purchase orders to keep requesters informed about their current status, progress, and action items.
    -   Purchase requisition summarization for requesters: Summarize purchase requisitions to keep requesters informed about their current status, progress, and action items.
    -   Sourcing request summarization for requesters: Summarize sourcing requests to keep requesters informed about their current status, progress, and action items.
Generate summarization in multiple languages for procurement objects with the multi-language support in the Now Assist console.

    -   For fulfillers, the following procurement objects support multi-language summarization:
        -   Sourcing request
        -   Purchase requisition
        -   Procurement case
        -   Purchase order
        -   Negotiation
        -   Negotiation event
    -   For requesters, the following procurement objects support multi-language summarization:
        -   Sourcing request
        -   Purchase requisition
        -   Purchase order
With the Now Assist panel, fulfillers can use agentic AI to summarize the following procurement objects quickly:

    -   Sourcing request
    -   Purchase requisition
    -   Procurement case
    -   Purchase order
    -   Negotiation
    -   Negotiation event
-   **[Now Assist for Common Finance and Supply Chain features](https://www.servicenow.com/docs/access?context=now-assist-fsc-common&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Use Now Assist for Common Finance and Supply Chain features to summarize purchase orders and keep fulfillers informed of their status, progress, and required actions.

-   **[Using agentic workflows in Now Assist for Sourcing and Procurement Operations](https://www.servicenow.com/docs/access?context=agentic-ai-now-assist-spo&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Use agentic workflows for Sourcing and Procurement Operations to fulfill your procurement needs through intelligent product recommendations, guided checkout and off-catalog purchasing processes, and detailed product information. These workflows also help answer procurement-related questions and efficiently track associated records.


</td></tr><tr><td>

Strategic Planning

</td><td>

-   **[Dashboards for data analysis and decision-making](https://www.servicenow.com/docs/access?context=dashboards-in-spw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Use dashboards to view key data and metrics, enabling you to monitor performance, track progress, and make informed decisions related to ideas, feedback, planning, and execution. Dashboards consolidate data from multiple sources into a single, easily digestible format. Each widget within a dashboard displays key data and metrics and may include visualizations. The default dashboards include the Product Idea Dashboard, Feedback Dashboard, Strategy Execution Dashboard, and Execution Dashboard.

You can create or edit dashboards, copy an existing dashboard and customize it as needed, and share dashboards to collaborate with business stakeholders who have access to the portfolio plan.

-   **[Create and share views for portfolio plans and free-form roadmaps](https://www.servicenow.com/docs/access?context=managing-portfolio-plan-views-spw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

For portfolio plans - Create, edit, and switch between views with display preferences such as column selection, grouping, and filtering for portfolio plans. You can create personal views that are private to you, or public views that can be shared with stakeholders who have access to the portfolio plan. The portfolio plan view saves your display preferences across the **Prioritization**, **Roadmap**, **Capacity**, and **Financials** tabs.

**Note:** Views are available only for the Planning module and are supported in live mode, but not in scenario mode.

For free-form roadmaps - Create, edit, and switch between views with display preferences such as grouping, milestones selection, dependencies selection, and tracking mode for free-form roadmaps. You can create personal views that are private to you, or public views that can be shared with stakeholders who have access to the free-form roadmap.

-   **[Write planning item skill](https://www.servicenow.com/docs/access?context=refine-text-with-write-planning-item-skill&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   Improve record quality and user satisfaction by enabling AI assistance in the **Description** field across all Strategic Planning Workspace forms, including product idea, demand, epic, project, capability, feature, and story.
    -   Enable text refinement with the **Elaborate** and **Shorten** options on planning items to support product managers and agile team members in creating and editing content more effectively.
-   **[Plan efficiently with additional pre-defined lenses](https://www.servicenow.com/docs/access?context=lens-alignment-planner-workspace&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Using the Digital Product lens, portfolio managers can plan, prioritize, and roadmap the work in the Strategic Planning Workspace based on the digital products by aligning with the business strategy.

The lens is supported with the work items, epic, and product idea. With the Digital Product lens, you can also do high-level planning using the Product Enhancement entity. By default, the Product Enhancement entity is enabled for high-level planning.

-   **[Cycle time report for Agile teams in EAP dashboards](https://www.servicenow.com/docs/access?context=eap-agile-team-dashboard&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Analyze how long the stories take for your Agile team to move from an in-progress state to completion. Each bubble on the chart represents a story and the chart shows stories completed in the past 30 days. You can compare the cycle times of stories that have different story points and review the trend in the time taken by the team to complete them.

Using this data, identify the stories that took longer to complete and analyze the reasons so that you can draft an action plan to optimize the team's cycle time in the future.

-   **[Kanban configuration for EAP teams](https://www.servicenow.com/docs/access?context=agile-configurations-in-eap&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Use the Kanban configuration for teams that don't prefer to work in an iteration-based schedule. You can activate the predefined Kanban configuration and add teams to your Agile structure or you can modify an existing configuration by setting the **Planning calendar** field to **None**.

-   **[Column filters in EAP Backlog](https://www.servicenow.com/docs/access?context=using-eap&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Quickly find the work items that you need by using column-level filters for the data on your EAP Backlog. You can filter on any column that is displayed on the **Backlog** tab.

-   **[Generate stories from epics and features using Now Assist for EAP](https://www.servicenow.com/docs/access?context=generate-stories-from-epics-now-assist-eap&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Break down epics and features into stories using the Now Assist Agile story generation skill in the EAP workspace. Using the available details such as name, description, docs content, and any existing stories, Now Assist provides story recommendations for your epic or feature. You can let Now Assist generate stories using its initial recommendations or you can choose to split or combine the story recommendations before prompting Now Assist to create the stories.

-   **[View financial data of your planning items at portfolio level](https://www.servicenow.com/docs/access?context=using-portfolio-financials-spw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   View the rolled-up financial costs and benefits data of your planning items such as Epics, Demands, and Projects at the portfolio level for different time scales and ranges.
    -   View the Budget, Planned, Variance, Actuals, and Remaining Estimates of the financials costs by expense type or cost type.
    -   View the Forecasts, Actuals, and Variance of monetary benefits.
-   **[Create a manage financial scenarios of planning items](https://www.servicenow.com/docs/access?context=optimizing-scenarios-in-strategic-planning&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   Optimize your portfolio by creating financial scenarios to validate and arrive at a profitable outcome.
    -   Plan and manage the budget of planning items in simulation mode for efficient financial planning and to help prevent overspending.
    -   Manage prioritization and budget allocation of the planning items to meet business priorities.
    -   Compare scenarios financially and automatically allocate the planned budget to planning items from approved scenarios.
    -   Enable the **new budget allocation** property \(**sn\_invst\_pln.enable\_budget\_allocation\_v2**\) to perform financial analysis in scenario planning and take effective decisions by data-driven insights.
-   **[Real-time collaboration for EAP Docs](https://www.servicenow.com/docs/access?context=docs-for-eap-teams-and-planning-items&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

Edit a doc page concurrently with multiple other editors. Colored cursors denote the current location of editors on the page. You can choose to show or hide these indicators.

The real-time collaboration feature for docs is also available for planning items in the Strategic Planning Workspace. See [Docs for planning items in Strategic Planning](https://www.servicenow.com/docs/access?context=docs-for-planning-items-in-spw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US).

**Note:** To use the full functionality of Docs v6.6.0 within Strategic Planning Workspace, ensure that you upgrade Strategic Planning Workspace to v4.5.0. For more information, see [KB2017926](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2017926).


</td></tr><tr><td>

Strategic Portfolio Management for Telecom

</td><td>

-   **[Fiber rollout project template](https://www.servicenow.com/docs/access?context=spmt-fiber-rollout-template&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Bring scalability and adaptability to network expansion efforts by enabling organizations to customize them for various deployment scenarios. These templates reduce planning and execution costs through standardized, repeatable workflows while ensuring compliance with regulatory and operational standards.

-   **[5G project template](https://www.servicenow.com/docs/access?context=spmt-overview&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

Accelerate time-to-market by providing pre-configured workflows that simplify complex network deployment processes. The template enhances operational efficiency by streamlining tasks, reducing redundancies, and minimizing errors. It also improves team collaboration by providing clear visibility into timelines, resource allocation, and milestones, aligning stakeholders around shared goals.


</td></tr><tr><td>

Subscription Management

</td><td>

-   **[Subscription allocation counts according to active users](https://www.servicenow.com/docs/access?context=subscription-details-v2&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

View the total number of active users in a product subscription. Only active users count toward the subscription allocation totals that appear throughout Subscription Management.

-   **[Allocate subscriptions to all recommended groups](https://www.servicenow.com/docs/access?context=allocate-subscriptions-v2&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Select all recommended groups when allocating subscriptions.

-   **[Support for on-premises installation](https://www.servicenow.com/docs/access?context=configuring-subscription-management-v2&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Manage subscription usage using Subscription Management on-premises.

-   **[Recommended subscription reasoning](https://www.servicenow.com/docs/access?context=addressing-issues-subscription-management-v2&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Determine why Subscription Management displays a subscription recommendation when mapping custom tables or custom applications.

-   **[Manage custom applications and table mapping through the platform](https://www.servicenow.com/docs/access?context=allocating-custom-tables-subscr-apps-v2&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Map any missing custom applications and tables in Subscription Management to a subscription directly from the Custom Applications list or Custom Table Inventory list.

-   **[Support for domain separation](https://www.servicenow.com/docs/access?context=domain-separation-subscription-mgmt&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

View and filter subscribers by domain for user-based subscriptions.


</td></tr><tr><td>

Supplier Lifecycle Operations

</td><td>

-   **[Supplier Operations](https://www.servicenow.com/docs/access?context=supplier-operations&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Supplier Operations ​ provides support for advanced case management capabilities to handle key supplier lifecycle events such as onboarding, offboarding, and ongoing operations. It includes the ability to resolve cases via Playbooks for a structured and consistent approach.

-   **[Supplier Payment Optimization](https://www.servicenow.com/docs/access?context=supplier-pmnt-opt&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Supplier managers can identify, prioritize, and track suppliers with high potential for accepting credit card payments.

    -   Supplier Managers can initiate credit card enablement cases, enabling suppliers to use a credit card as their preferred payment method.
    -   They can initiate credit card enablement journey for new or existing suppliers after checking their propensity scores \(currently requires manual updates\).
    -   They can view the saving estimates associated with the card for a given supplier using the **Savings calculator** tool. They can also view the calculation details of the savings estimator formulas.

-   **[Relish Integration for Supplier Lifecycle Operations](https://www.servicenow.com/docs/access?context=relish-slo-connector&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Supplier managers can conduct sanction screening, validate banking details change requests, and supplier location change requests via Relish integration.

-   **[Mapping multiple internal stakeholders to a supplier](https://www.servicenow.com/docs/access?context=manage-internal-stakeholders&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

This feature enhances supplier governance in SLO by enabling the mapping of multiple internal stakeholders such as legal, business, technical, and risk teams to suppliers, improving visibility and management of supplier relationships.

-   **[Universal Request](https://www.servicenow.com/docs/access?context=universal-request&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Supplier contacts can create generic cases by selecting **Request Help** in the Supplier Collaboration Portal, if they can't find the relevant search results or are unsure of which department to contact for help. These cases are triaged and routed internally to appropriate case types. Universal requests remove ambiguity and improve efficiency for both suppliers and internal operations.

-   **[Overall supplier dashboard](https://www.servicenow.com/docs/access?context=overall-supplier-db&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

The overall supplier performance dashboard provides detailed information about overall supplier scores, count of all active suppliers, their all-time spend, and overall risk ratings. It also includes the Supplier Insights section and the Action plans section showing relevant details.


-   **[Supplier Relationship and Performance Management](https://www.servicenow.com/docs/access?context=supplier-performance-management-overview&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**
    -   **Flexible KPI tracking**: Supplier managers can create KPIs directly without predefined templates, which results in simplified KPI creation, enabling faster and more efficient performance tracking.
    -   **Enhanced KPI management**: Improved threshold setup, error messaging, and dashboard visualizations for KPI tracking.
    -   **Multiple dimensions for KPI tracking**: Create supplier-level and contract-level KPIs using KPI templates to measure supplier performance. Contract-level KPIs are created under supplier-level KPIs. The overall KPI value of a supplier is calculated based on the latest aggregated values of all the related contract-level KPIs.
    -   **Action Plans for under-performing KPIs**: Address performance gaps by creating Action Plans linked to the under-performing KPIs, enabling visual tracking of milestones and tasks. The tasks triggered by the Action Plans are assigned to the suppliers and they can see and complete those tasks in the Supplier Collaboration Portal, streamlining the overall KPI remediation process.
    -   **Automated KPIs**: Enables automated data collection, KPI template modifications, and calculation at supplier and contract levels. The automated KPI system integrated into action plans can be used for comprehensive performance monitoring.
-   **[Many-to-many \(M2M\) mapping between supplier contact and suppliers](https://www.servicenow.com/docs/access?context=enable-m2m-supplier-contacts&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**
    -   Supplier contacts can manage multiple supplier records under a single login, with the ability to toggle between records in the Supplier Collaboration Portal. One supplier contact can be the contact for multiple suppliers, provided the suppliers share a parent-subsidiary relationship.
    -   M2M mapping between supplier contact and suppliers also enables supplier contacts to register using a company name across different email domains, thus simplifying onboarding for distributed supplier teams.
    -   M2M mapping between supplier contact and suppliers is available from the Xanadu December 2024 release onwards. To enable this feature, see [Enable M2M mapping between supplier contact and suppliers](https://www.servicenow.com/docs/access?context=enable-m2m-supplier-contacts&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US).

-   **[Now Assist for Supplier Lifecycle Operations \(SLO\)](https://www.servicenow.com/docs/access?context=now-assist-slo&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**
    -   View the summarized details of supply-related cases within the **Now Assist Panel** to keep the supplier managers and fulfillers informed about their progress and action items.
    -   Case summarization supports multiple languages.
-   **[AI driven supplier onboarding using Now Assist for SLO](https://www.servicenow.com/docs/access?context=supplier-onboarding-agentic-workflow&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Use agentic AI in Now Assist for Supplier Lifecycle Operations \(SLO\) to streamline the supplier onboarding process by automating supplier registration.

-   **[Smart Assessments](https://www.servicenow.com/docs/access?context=slo-campaign-mgmt&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Supplier managers can use the segmentation rules and assessment templates to create smart assessments in bulk for users. Smart assessments provide a survey-like experience with enhanced UI capabilities for both internal and external users. This feature utilizes the capabilities of the Smart Assessment Engine application.

-   **[Emails view for supplier managers](https://www.servicenow.com/docs/access?context=enabling-emails-view-for-contacts&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Supplier managers can access their emails within the Source-to-Pay Workspace from the **Emails** tab in the case, task, and supplier details pages respectively. Email actions are reflected, incomplete email errors are handled, and email-related activities can be summarized from the workspace.

Supplier contacts receive the emails and they can perform the assigned tasks directly via email without logging in to the Supplier Collaboration Portal.


</td></tr><tr><td>

Synthetic monitoring

</td><td>

-   **[Create and edit a synthetic monitor](https://www.servicenow.com/docs/access?context=create-synthetic-monitor&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

Create and manage synthetic tests to replicate end-user transactions for critical service endpoints. Configure an alert to activate when a test fails, enabling you to address issues before they impact users.

As of version 1.2, you can:

    -   Test for response code: Confirm that your endpoints are returning success codes and know when they aren’t.
    -   Test for response time: Confirm that your services are meeting performance expectations by setting thresholds for response times.
    -   Test for response text: Validate whether specific content exists in the response body, enabling accurate end-to-end checks.
    -   Run tests from your local Glide instance: Enable closer integration with your instance and reduce the need for external test runners.
    -   Run tests from multiple locations.
-   **[Identifying system issues with synthetic monitoring](https://www.servicenow.com/docs/access?context=identifying-system-issues&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

View the Overview page for a monitor where you can:

    -   View the status of the monitor.
    -   View charts that display test failures and response times.
    -   Visit related configuration items \(CIs\) that might be the start to investigating failed tests.
    -   View a historical log of synthetic test runs, including details and the response body text.
    -   Share results by exporting a list of tests for a monitor.

</td></tr><tr><td>

Talent Development Core

</td><td>

-   **[Credly integration](https://www.servicenow.com/docs/access?context=credly-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

As an employee, Credly integration now empowers you to display your digital credentials better demonstrating your skills in a tangible way.


-   **View user credentials**

As an administrator, Achievements and Credentials now enables you to view user credentials and use achievement credential templates to sync credentials from third-party credential providers, for example: Credly

Import latest badges and related skills with the **Refresh credentials** option.

Credential badges are displayed in the skill activity insights.

Skills related to Credentials \(badge template\) are synced to the user profile. New skills identified are added to the harmonisation queue. Once imported, dynamic skills are associated with the respective user profile.

**Note:** Credential Core has a soft dependency on Skills Foundation \(8.0\).


-   **[Create a growth plan with the help of Now Assist](https://www.servicenow.com/docs/access?context=egd-create-growth-plan&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

As a Talent Development user, manage your career growth by creating a growth plan with the help of Now Assist. With Now Assist, you can provide details to craft a prompt that describes your career goals.

**Note:** This feature is available when you have both Talent Development Core and Now Assist for HRSD installed.


</td></tr><tr><td>

Talent Feedback

</td><td>

-   **[Request and view feedback](https://www.servicenow.com/docs/access?context=request-skill-feedback&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

As a manager, request skill feedback for your team members on any skills from the employee's collaborators.

-   **[View feedback and skill activities](https://www.servicenow.com/docs/access?context=view-skill-feedback&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

As a manager, view all the feedback received for a skill along with skill activities, during skill validation to get a full-fledged view of an employee's proficiency.

-   **[Request feedback](https://www.servicenow.com/docs/access?context=request-skill-feedback&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

As an employee, receive feedback requests in your Employee Center To-dos, where you can provide feedback and skill rating for one or more skills in the request.

-   **[Decline a feedback request](https://www.servicenow.com/docs/access?context=accept-deny-feedback&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)Accept or deny feedback requests**

As an employee \(feedback provider\), you can choose to decline requests that are not relevant to you.


</td></tr><tr><td>

Telecommunications Network Inventory

</td><td>

-   **[Design and assign your network services](https://www.servicenow.com/docs/access?context=design-assign-playbook&version=yokohama&pubname=yokohama-telecom-network-inventory&ft:locale=en-US)**

Create and configure playbooks for design and assign a configuration item. The Design and Assign playbook provides step-by-step guidance for designing a network service. Use the playbook to complete guided activities to instantiate a network inventory record.

-   **[Design and Assign function for logical connections](https://www.servicenow.com/docs/access?context=design-logical-connection-design-assign-playbook&version=yokohama&pubname=yokohama-telecom-network-inventory&ft:locale=en-US)**

Use the Design and Assign playbook to instantiate a logical connection and its associated connection elements. Once each activity completes, view the circuit map to visualize the logical connection elements.

-   **[Visualization of geo map](https://www.servicenow.com/docs/access?context=visualization-map&version=yokohama&pubname=yokohama-telecom-network-inventory&ft:locale=en-US)**

Use the Network site map to view the geographical location of your network sites and the information such as site details, connectivity, and capacity.

-   **[Creating an inventory template for a logical composite](https://www.servicenow.com/docs/access?context=creating-inventory-template-logical-composite&version=yokohama&pubname=yokohama-telecom-network-inventory&ft:locale=en-US)**

Instantiate a logical composite record and associated equipment and racks using a logical composite template.

-   **[Add an equipment or rack to logical composite](https://www.servicenow.com/docs/access?context=add-equipment-rack-logical-composite&version=yokohama&pubname=yokohama-telecom-network-inventory&ft:locale=en-US)**

Add equipment or rack to a logical composite using a change model.

-   **[Remove an equipment or rack from logical composite](https://www.servicenow.com/docs/access?context=remove-equipment-rack-logical-composite&version=yokohama&pubname=yokohama-telecom-network-inventory&ft:locale=en-US)**

Remove a rack or equipment from a logical composite using a change model.

-   **[Create an equipment record by using design and assign](https://www.servicenow.com/docs/access?context=create-equipment-record-design-and-assign&version=yokohama&pubname=yokohama-telecom-network-inventory&ft:locale=en-US)**

Create a change request for an equipment record from the All Equipment list view using the **Create equipment** UI action.

-   **[Import models and templates in JSON format](https://www.servicenow.com/docs/access?context=import-models-templates-json&version=yokohama&pubname=yokohama-telecom-network-inventory&ft:locale=en-US)**

Create an import request to import your collection of models and templates in JSON format.

-   **[Export hierarchy of models and templates](https://www.servicenow.com/docs/access?context=export-hierarchy-of-models-and-template&version=yokohama&pubname=yokohama-telecom-network-inventory&ft:locale=en-US)**

Export the hierarchy and all related records of a model or inventory template in JSON format.

-   **[Managing your network functions](https://www.servicenow.com/docs/access?context=services&version=yokohama&pubname=yokohama-telecom-network-inventory&ft:locale=en-US)**

The xNF and xNF instances records are added in the Inventory menu and retained the Services menu for application services.

-   **[Create a telephone infrastructure](https://www.servicenow.com/docs/access?context=telephone_block_telephone_number_and_telephone_number&version=yokohama&pubname=yokohama-telecom-network-inventory&ft:locale=en-US)**

Supports all types of telephone numbers.


</td></tr><tr><td>

Telecommunications Service Operations Management \(TSOM\)

</td><td>

-   **[Pattern-based direct discovery using CLI and SNMP](https://www.servicenow.com/docs/access?context=telecom-discovery-tsom-visibility&version=yokohama&pubname=yokohama-telecom-service-ops&ft:locale=en-US)**

Use pattern-based direct discovery to do the following tasks:

    -   Support deep network discovery of your physical network elements by using CLI and SNMP.
    -   Enable pattern-based discovery for any network elements that support SNMP standard MIBs.
    -   Provide a framework to enable custom Management Information Base \(MIB\)-based discovery.
    -   Enable both scheduled and quick discovery of standalone network elements.
    -   Support the following Cisco and Juniper routers and switches:
        -   Cisco ASR1K
        -   Cisco 7613
        -   Cisco Nexus 9000
        -   Cisco Nexus 3548
        -   Juniper Mx80
        -   Juniper MX104
        -   Juniper MX240
        -   Juniper MX480
-   **[Nokia Altiplano SGC integration](https://www.servicenow.com/docs/access?context=service-graph-connector-for-nokia-altiplano&version=yokohama&pubname=yokohama-telecom-service-ops&ft:locale=en-US)**

With Nokia Altiplano SGC integration, you can:

    -   Support discovery of physical Gigabit Passive Optical Network \(GPON\) network information by integrating with the Nokia Altiplano Service Graph Connector.
    -   Enable scheduled and on-demand discovery.
    -   Support the multi-instance integration of the Nokia Altiplano Service Graph Connector.
-   **[Discrepancy identification and reconciliation](https://www.servicenow.com/docs/access?context=telecom-reconciliation&version=yokohama&pubname=yokohama-telecom-service-ops&ft:locale=en-US)**

Identify the discrepancies between your inventoried and discovered data in the following cases:

    -   -   Model mismatch.
-   Model relationship mismatch.
-   Entities not discovered in the current run but discovered in the previous run.
-   Slots-occupied discrepancy.
-   Most recent discovery not updated.
-   Incorrect number of relationships.
    -   Support a framework to automatically create tasks for reconciling discrepancies.

</td></tr><tr><td>

Theme Builder

</td><td>

-   **[Align with your brand by using the Unified Navigation component](https://www.servicenow.com/docs/access?context=edit-unified-navigation-component&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

Customize the Unified Navigation component from within Theme Builder by using the following new features:

    -   Quickly view how the Unified Navigation component will look in your theme by using the Preview pane.
    -   Use the Component Configuration menu to view any shared styling between subcomponents.
    -   View the background color of your subcomponent and see how it renders in relation to the Unified Navigation component by using the updated canvas color feature.
-   **[Use the double-click feature to quickly access the Component Editor](https://www.servicenow.com/docs/access?context=tb-edit-components&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

Double-click a component tile to access the Component Editor where you can continue to make style adjustments to subcomponents, variants, or interactions.

-   **[Adjust the Unified Navigation component to meet accessibility standards](https://www.servicenow.com/docs/access?context=tb-adjust-component-wcag&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

As of Theme Builder version 5.1, the Accessibility Inspector now displays the total number of accessibility errors with contrast issues for the Unified Navigation component and subcomponents. See the Accessibility section for details.

-   **[Adapt the theme-able illustrations to seamlessly integrate with your brand](https://www.servicenow.com/docs/access?context=working-with-image-styles&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

As of Theme Builder version 5.1, use the new Image styles feature to enhance your theme in the following ways:

    -   Edit the colors of the empty state illustrations from within Theme Builder. When a part of your Next Experience web page doesn't contain data, an empty state illustration appears. Empty state illustrations are theme-able and adapt to your theme colors.
    -   Override empty state illustrations with your own custom images to uniquely align with your branding style.

</td></tr><tr><td>

Third-party Risk Management

</td><td>

-   **[TPRM personalized dashboards](https://www.servicenow.com/docs/access?context=tprm-monitor-dashboards&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Improve your decision-making process by exploring and analyzing your assessment data at various levels by using the Third-party insights dashboard and the TPRM custom analytics dashboard. If you have the Third-party risk manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] or Third-party risk assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] role, you can create and share your own dashboards and reports. If you're a third-party risk manager, you can also customize the report layouts, widgets, and data views to prioritize key metrics and workflows that align with your individual roles and risk programs.

-   **[New Standardized Information Gathering \(SIG\) questionnaire content](https://www.servicenow.com/docs/access?context=grc-sig-integration&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Use the updated SIG templates for 2025 after upgrading to version 20.1.x as part of the Third-party Risk Management application. The latest SIG questionnaires help your organization stay aligned with stricter regulatory compliance and emerging third-party risk governance, covering a wide range of security and privacy concerns.

-   **[Quick start tests for TPRM](https://www.servicenow.com/docs/access?context=quick-start-tests-grc-vrm&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

Verify that TPRM works as expected after upgrades and deployments of new applications or integrations by running quick start tests. If you customized TPRM, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Threat Intelligence Security Center

</td><td>

-   **[Microsoft Defender for EDR Integration](https://www.servicenow.com/docs/access?context=tisc-ms-defender-integration&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Integration with the Microsoft Defender for EDR allows Cyber Threat Intelligence \(CTI\) analysts to automatically push malicious or suspicious IP addresses, domains, file hashes, and URLs to Microsoft Defender for continuous monitoring and real-time alerting.

-   **[Create a security incident from a TISC case](https://www.servicenow.com/docs/access?context=tisc-create-si-case&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Create security incidents and associate observables to the security incidents from a TISC case.

-   **[Duplicate threat intelligence feeds](https://www.servicenow.com/docs/access?context=tisc-duplicate-feeds&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Duplicate threat intelligence feeds to create an exact copy of the existing feed.


</td></tr><tr><td>

Upgrade Center

</td><td>

-   **[Upgrade Preview enhancements](https://www.servicenow.com/docs/access?context=uc-preview-module&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Enhance your upgrade preview experience with the new Application Upgrade Preview and Predicted Schema Changes cards. You can also monitor the status of the preview process from the Upgrade Preview page.

-   **[Upgrade Management Console experience](https://www.servicenow.com/docs/access?context=um-landing-page&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

Use the new Upgrade Management Console experience to access all the relevant information and tools required for a cohesive upgrade on your instance.


</td></tr><tr><td>

Usage Insights

</td><td>

-   **Added filtering capability to all analytics pages**

Analytics pages have various filter options to help segment data including Date range, User type, and Country. Other filters appropriate to each page are available.

-   **Configurable user properties**

Filter usage data by custom user groups across all User Experience Analytics pages. Custom user properties can also be added to User details pages. User roles and department are available by default. Other user-related fields can be added to User Experience Analytics.

-   **Granular event filtering**

Filter event data using event properties to provide more specific and actionable insights into your data.

-   **User information added to events**

The number of unique users who performed an action visible next to the total occurrences of the event.


</td></tr><tr><td>

Virtual Agent

</td><td>

-   **[Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience. Assistant Designer is comprised of three main areas: Assistants, Asset library \(previously Virtual Agent Designer\), and Analytics.

-   **[Conversational settings for Assets in the Asset library](https://www.servicenow.com/docs/access?context=asset-lib-conv-settings&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)Conversational settings**

Manage the settings for an asset directly from the Asset library page.


-   **[Create a Virtual Agent topic](https://www.servicenow.com/docs/access?context=create-virtual-agent-topic&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Start the create flow for all supported conversational LLM assets directly from Virtual Agent Designer.

-   **[Assistants in Virtual Agent Designer](https://www.servicenow.com/docs/access?context=conversation-designer-virtual-agent&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

The Now Assist Panel - Platform \(default\) assistant is now available in Virtual Agent Designer.

-   **[AI Connector utility](https://www.servicenow.com/docs/access?context=vad-ai-connector-utility&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Select AI agents to handle tasks in the AI Connector utility. For more information on AI agents in Virtual Agent Designer, see [Managing AI agents in Assistant Designer](https://www.servicenow.com/docs/access?context=managing-use-cases-ai-agents&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US) and [Using AI agents in Virtual Agent topics](https://www.servicenow.com/docs/access?context=ai-agent-custom-skill&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

-   **Virtual Agent Designer [Table bot response control](https://www.servicenow.com/docs/access?context=table-bot-response&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Slide the new **Show links for each record** toggle switch to activate links for each record in the output in your Virtual Agent conversation.

-   **Virtual Agent server**
    -   In chatHandshake, set **dynamic\_step\_loader\_enabled** to `true` to send stacked Agentic AI messages to server. Set **dynamic\_step\_loader\_enabled** to `false` to avoid sending messages.
    -   Pre-chat and post-chat surveys are now available for Anthropic Claude on AWS and Google Gemini LLMs. For more information on surveys, see [Chat surveys](https://www.servicenow.com/docs/access?context=ci-conversational-chat-surveys&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

-   **[AI Connector Utility](https://www.servicenow.com/docs/access?context=vad-ai-connector-utility&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Link custom skills to generative AI to add their functionality to LLM conversations.

-   **[AI agents and agentic workflows in Virtual Agent Designer](https://www.servicenow.com/docs/access?context=managing-use-cases-ai-agents&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

View AI agents and agentic workflows created in AI Agent Studio in Virtual Agent Designer.

-   **[Shorten responses option for bot text response](https://www.servicenow.com/docs/access?context=va-text-response&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

For bot text responses, use the **Shorten responses** toggle in Virtual Agent Designer to turn on the **Show more** option in the chat on the user side.


-   **[Application scope for topics](https://www.servicenow.com/docs/access?context=vad-topic-creation-form&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Select the application scope for topics in Virtual Agent Designer.


-   **[Synthesized response in Slack conversations](https://www.servicenow.com/docs/access?context=slack-synthesized-response&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Generate synthesized responses in Slack conversations with Now Assist.

-   **[Virtual Agent feature support in Microsoft Teams conversations](https://www.servicenow.com/docs/access?context=va-teams-other-features&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Generate synthesized responses in Microsoft Teams conversations with Now Assist.

-   **[Custom skills in Virtual Agent Designer](https://www.servicenow.com/docs/access?context=managing-custom-skills&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

View skills created in Now Assist Skill Kit in Virtual Agent Designer.

-   **[Chat surveys](https://www.servicenow.com/docs/access?context=ci-conversational-chat-surveys&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

Create chat surveys compatible with LLM-enabled user inputs, aside from the Carousel user input.


</td></tr><tr><td>

Visa Spoke

</td><td>

-   **[Visa Stop Payment Service \(VSPS\) integration](https://www.servicenow.com/docs/access?context=visa-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

The Visa Stop Payment Service \(VSPS\) enables Visa card issuers to stop card-on-file payments \(including recurring and installment payments\) from being authorized, cleared, and settled through VisaNet. This service helps Visa issuers handle cardholder stop payment requests.

The following Visa Spoke actions allow clients to integrate with VSPS APIs and work through the platform:

    -   Create Stop Payment Instruction by Merchant Identifier Request Builder​
    -   Create Stop Payment Instruction by Merchant Identifier Response Parser​
    -   Create Stop Payment Instruction by PAN Request Builder​
    -   Create Stop Payment Instruction by PAN Response Parser​
    -   Create Stop Payment Instructions by Merchant Category Code Request Builder​
    -   Create Stop Payment Instructions by Merchant Category Code Response Parser​
    -   Look up Eligible Transactions for Stop Payment by PAN and Date Range Request Builder​
    -   Look up Eligible Transactions for Stop Payment by PAN and Date Range Response Parser
    -   Look up Stop Instruction Details by Stop Instruction ID Request Builder​
    -   Look up Stop Instruction Details by Stop Instruction ID Response Parser​
    -   Look up Stop Payment Instructions by PAN Request Builder​
    -   Look up Stop Payment Instructions by PAN Response Parser​
    -   Update Stop Instructions Duration by Stop Instruction ID Request Builder​
    -   Update Stop Instructions Duration by Stop Instruction ID Response Parser​
    -   Update Stop Payment Instruction by Merchant Identifier Request Builder​
    -   Update Stop Payment Instruction by Merchant Identifier Response Parser​
    -   Update Stop Payment Instruction by Merchant Category Code Request Builder​
    -   Update Stop Payment Instruction by Merchant Category Code Response Parser​
    -   Look up all linked stop payment instructions by stop instruction id Request Builder​
    -   Look up all linked stop payment instructions by stop instruction id Response Parser
    -   Look up stopped transactions by PAN Request Builder​
    -   Look up stopped transactions by PAN Response Parser​
    -   Look up stopped transactions by stop Instruction id Request Builder​
    -   Look up stopped transactions by stop Instruction id Response Parser
    -   Cancel Multiple Stop Instructions Request Builder​
    -   Cancel Multiple Stop Instructions Response Parser​

</td></tr><tr><td>

Vulnerability Response

</td><td>

-   **[Identify Wiz Resource Types for import](https://www.servicenow.com/docs/access?context=wiz-assets-resources-tab&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Identify the Resource Types \(assets\) that are reported by Wiz that you want to import with the Wiz Integration Resource Type configuration page in your ServiceNow AI Platform instance.

The Resource Types that you select apply to all the primary Wiz vulnerability and compliance integrations except the Wiz Container Vulnerability Integration. See the [Wiz Vulnerability Response Integrations](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US) for more information about the vulnerability and compliance integrations.

-   **[Wiz Backfill Integrations](https://www.servicenow.com/docs/access?context=wiz-backfill&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Retrieve and process data stored on the Wiz Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table for assets that were not processed by the primary Host Vulnerability Integration with a specialized Wiz Backfill Integration.

The Host Vulnerability Backfill Integration is activated by default.

**Note:** The Wiz Asset Integration and the Wiz Container Vulnerability Integration do not have backfill integrations. The Wiz Asset Integration can discover assets and create and update discovered item records on the Discovered item \[sn\_sec\_cmn\_src\_ci\] table. The Wiz Container Vulnerability Integration imports and processes discovered container image records.

-   **[Create host remediation tasks manually in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-create-remediation-task&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

With the sn\_vul.vulnerability\_analyst or sn\_vul.vulnerability\_admin role, you can create host remediation tasks manually by selecting some or all the records in the Host vulnerable items’ lists in the Vulnerability Manager Workspace. These records are grouped into one or more remediation tasks according to the grouping criteria selected while creating host remediation tasks.

-   **[Create host remediation tasks manually in the IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-create-remediation-task&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

With the sn\_vul.remediation\_owner role, you can create host remediation tasks manually by selecting desired records in the Host vulnerable items’ lists in the IT Remediation Workspace. These records are grouped into one or more remediation tasks according to the grouping criteria selected while creating host remediation tasks.

-   **[Questionnaire Support in Exception Management via Smart Assessment](https://www.servicenow.com/docs/access?context=vr-exception-management-smart-assessment&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Configure advanced questionnaires as part of the exception management process using Smart Assessment. This enhancement allows remediation owners to provide detailed context for exception requests and enables approvers to configure conditional questions to gather information for informed decision making.

    -   Collaboration and streamlined approval: Facilitate collaboration between your vulnerability management and remediation teams by streamlining the approval process with clear and complete exception justifications.
    -   Mandatory questionnaires: Block the submission of exception requests until mandatory questionnaires are completed. If a questionnaire is marked as mandatory, the test results and its associated remediation tasks remain in the 'Open' state until the questionnaire is completed and submitted.
    -   If the questionnaire is incomplete, the state change approval record is saved as 'Draft'. Only after completing the questionnaire can the user submit the exception request, which will then move the test results or remediation tasks to the 'In Review' state.
-   **[Lookup rules enhancements](https://www.servicenow.com/docs/access?context=working-unmatched-cis&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

When you reapply Lookup rules, Discovered items \(DIs\) that have been inactive for more than 90 days are ignored. These Discovered items \(DIs\) are also excluded from licensing considerations. Removing them from the lookup logic can improve performance and reduce processing time.

    -   Background job enhancements: New fields have been added to help you view successfully evaluate records, the time taken for processing, the time remaining, and an estimated number of records.
    -   Improved accuracy for non-CSDM Vulnerability Response users: A system property \(sn\_sec\_cmn.ci\_lifecycle\_status\_source\) has been introduced to help users who do not follow Common Service Data Model \(CSDM\) standards. This property ensures that Discovered items \(DIs\) and associated VITs are properly marked as Decommissioned and are excluded from the CI Lookup. Additionally, the Retired Configuration Items PA indicator has been updated to accurately reflect CIs based on the decommissioning flags.
    -   The scheduled job to create reconcile unmatched discovered items feature is deprecated. You can "Reapply Look up Rules" for selected or filtered items in the discovered items table view.
-   **[Tenable.cs integrations with the Vulnerability Response and Container Vulnerability Response application](https://www.servicenow.com/docs/access?context=tenable-cs-integrations-list&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

The Vulnerability Response Integration with Tenable application now supports data ingestion from Tenable.cs, enabling you to bring in cloud and container vulnerabilities directly into ServiceNow. This integration enhances your ability to prioritize and remediate vulnerabilities identified in Tenable cloud resources and container images. Key capabilities are:

    -   Importing vulnerabilities discovered by Tenable.cs in cloud hosts and container images into ServiceNow automatically.
    -   Enabling remediation workflows to triage, assign, and resolve the most critical vulnerabilities across cloud-native and containerized environments.
    -   Using the Setup Assistant to easily configure credentials and integration parameters—get started with minimal manual setup.
    -   Scheduling jobs to run periodically to import findings from Tenable.cs, create vulnerable items \(for cloud hosts\), create container vulnerable items and associate them with the relevant cloud resources and container image records.
-   **[Assess vulnerability exposure by publisher](https://www.servicenow.com/docs/access?context=vr-ws-exposure-publisher&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Starting with v5.0 of Vulnerability Exposure Assessment, a publisher-based assessment is introduced that enables you to assess the vulnerability impact by vendor. For example, Microsoft, and Red Hat. By focusing on recently disclosed vulnerabilities from critical vendors, you can prioritize remediation and proactively address threats, improving your overall security posture.

-   **[View risk score details of a vulnerable item in the Work notes section](https://www.servicenow.com/docs/access?context=vuln-calculators-rules&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Starting with v25.0.3 of Vulnerability Response, the system property **sn\_sec\_cmn.risk\_score\_changes\_add\_worknotes** is inactive by default. If you enable it, only then you can see all the changes related to the risk score of a vulnerable item in the Work notes section. Additionally, the work notes are updated only if there’s a change in the risk score.

-   **[Quick Start Tests for Vulnerability Response](https://www.servicenow.com/docs/access?context=available-quick-start-tests&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Vulnerability Response works as expected. If you customized Vulnerability Response, copy the quick start tests and configure them for your customizations.

-   **Enhancements to exception rules handling**
    -   Exception rules are reevaluated with nightly scheduled jobs.
    -   Vulnerable items that no longer match exception rule conditions are unlinked from remediation tasks.
    -   A deferred vulnerable item \(VIT\) is reopened if it doesn’t match any active exception rules.
    -   Exception rules don’t create remediation tasks. VITs are deferred directly and aren’t associated with a remediation task.
-   **[Tenable's endpoint scanning integration](https://www.servicenow.com/docs/access?context=tenable-io-integrations-list&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

Support for Tenable's endpoint scanning integration to retrieve scan metadata. The integration fetches scan details using the last\_schedule\_id from existing asset data in Tenable.io.

-   **Reopened Count field on vulnerable items**

Added the Reopened Count field on vulnerable items to track the number of times their states change from 'Closed' to 'Open' or to 'Active'.

-   **[Out-of-the-box vendor advisories via Common Security Advisory Framework \(CSAF\) integration](https://www.servicenow.com/docs/access?context=vuln-solution-mgmt&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

The following vendor advisories are configured out-of-the-box and are automatically activated when the Solution Management plugin is enabled: Redhat and Suse.


</td></tr><tr><td>

Vulnerability Response Integration with Claroty CTD

</td><td>

-   **[Enhanced filters for the Vulnerability Response Integration with Claroty CTD to support Claroty CTD v5.1](https://www.servicenow.com/docs/access?context=connect-to-claroty-ctd-vr-integration&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

Identify and import vulnerabilities according to your requirements by using the additional filter properties that have been added in Claroty CTD. The filter properties are based on a Common Vulnerability Scoring System \(CVSS\) V3 score and Exploit Prediction Scoring System \(EPSS\) score that is available in Claroty CTD v5.1.


</td></tr><tr><td>

Vulnerability Response integrations

</td><td>

-   **[Tenable.io CI lookup rules prioritize the non-empty network interface values \(FDQN, IPV4, and MacAddress\) for a discovered item](https://www.servicenow.com/docs/access?context=ci-identifier-rules&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

The Tenable.io CI lookup rules prioritize and populate the non-empty network interface values \(FDQN, IPV4, and MacAddress\) over the regular FDQN, IPV4, and MacAddress values for a discovered item.


</td></tr><tr><td>

Workforce Optimization for Customer Service CSM

</td><td>

-   **[Manager Workspace landing page](https://www.servicenow.com/docs/access?context=csm-configurable-manager-workspace-dashboards-new&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

Empower managers with real-time insights and actionable metrics, organized in a unified view, to drive performance optimization and facilitate prompt action.


**Note:** Existing customers on release versions prior to the Yokohama release can still view the old [Legacy Manager Workspace landing page](https://www.servicenow.com/docs/access?context=csm-configurable-manager-workspace-dashboards&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US).

</td></tr><tr><td>

Workspace

</td><td>

-   **[Configure keyboard shortcut for response templates](https://www.servicenow.com/docs/access?context=configure-response-templates&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

Use a keyboard shortcut to add response templates to journal fields within a form.

-   **[Create collapsible content for email templates](https://www.servicenow.com/docs/access?context=configure-collapsible-email-templates&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

Hide email content behind an ellipsis in email templates.

-   **[Configure the email composer in Core UI](https://www.servicenow.com/docs/access?context=enable-next-experience-email-client-core-ui&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

Access the latest Workspace features for email composer in the Core UI.


</td></tr><tr><td>

Zero Copy Connector Hub

</td><td>

-   **[Established connections](https://www.servicenow.com/docs/access?context=connections-wdf&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

Retrieve real-time data from external sources directly in the ServiceNow AI Platform, without copying any data to your instance using zero copy connections.

-   **[Data fabric tables](https://www.servicenow.com/docs/access?context=data-fabric-tables-wdf&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

Enable data consumers to access external data on the ServiceNow AI Platform to power AI features and build applications using data fabric tables.


</td></tr><tr><td>

Zero Copy Connector for ERP

</td><td>

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   **[Zero Copy Connector for ERP dashboard](https://www.servicenow.com/docs/access?context=erpc-obtaining-erp-canvas-metrics-and-statistics&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

View charts and graphs about transactions on the home page dashboard.

-   **[Implement and deploy faster with ERP content packs](https://www.servicenow.com/docs/access?context=erp-canvas-content-packs&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Use prebuilt content packs containing models to get Zero Copy Connector for ERP running on your instance faster.

-   **[Preview entities in the Model Manager](https://www.servicenow.com/docs/access?context=erpc-add-entity-to-model-op&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

Preview operations, fields, values, inputs, and outputs in the Zero Copy Connector for ERP Model Manager instead of having to open App Engine Studio.

-   **[View detailed software information](https://www.servicenow.com/docs/access?context=view-erp-system-information&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

View software information including machine type, node name, supported database, and more.


</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Yokohama features](../release-notes-summaries.md)

