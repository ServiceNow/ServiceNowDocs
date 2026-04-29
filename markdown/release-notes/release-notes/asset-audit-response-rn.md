---
title: Asset Audit Response release notes
description: The ServiceNow Asset Audit Response application provides workspaces where asset managers can manage their regulatory audits, request evidence for these audits, respond to these requests through a guided experience, and access regulatory content data to help drive more efficient and accurate responses to these requests. Asset Audit Response was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# Asset Audit Response release notes

The ServiceNow® Asset Audit Response application provides workspaces where asset managers can manage their regulatory audits, request evidence for these audits, respond to these requests through a guided experience, and access regulatory content data to help drive more efficient and accurate responses to these requests. Asset Audit Response was enhanced and updated in the Australia release.

## Asset Audit Response highlights for the Australia release

[Australia Patch 1](../quality/australia-patch-1.md)

-   Automatically generate summaries of completed and in-progress evidence requests for your financial regulatory audits.
-   Track and manage impacted records that are associated with your remediation tasks.
-   Gain insight into the citations associated with your evidence requests.

See [Asset Audit Response](https://www.servicenow.com/docs/access?context=asset-audit-response&version=australia&pubname=australia-it-asset-management&ft:locale=en-US) for more information.

**Important:** Asset Audit Response is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Asset Audit Response to Australia

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://www.servicenow.com/docs/access?context=read-only-option&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## New in the Australia release

-   **[Automate the summarization of evidence requests](https://www.servicenow.com/docs/access?context=fulfill-evidence-requests-guided-experience&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

    Use generative AI to summarize completed and in-progress evidence requests for your ﬁnancial regulatory audits. Gain insight into the corresponding audit engagements, the associated financial regulations, and the evidence that was submitted for each request. In addition, view details about the remediation rules that were created for each request and the corresponding remediation tasks that were generated based on those rules. Use this information to help plan for and complete other in-progress evidence requests so that you can improve your operational efficiency.

-   **[Track impacted records that require remediation](https://www.servicenow.com/docs/access?context=fulfill-evidence-requests-guided-experience&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

    Use the Impacted Records related list in your remediation tasks to track and take any necessary actions on the impacted records, including asset and configuration item \(CI\) records, that are associated with each task. These remediation tasks are automatically generated based on the remediation rules that you define during evidence request fulfillment.

-   **[View citations for your evidence requests](https://www.servicenow.com/docs/access?context=fulfill-evidence-requests-guided-experience&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

    Gain insight into the citations that are associated with your evidence requests by using the Citation details fields in the Asset Response Guided Experience. Use these fields to identify the name, description, and supplemental guidance for any citation that is associated with a request.

-   **[Streamline the fulfillment of evidence requests by using financial regulatory context from the Digital Operational Resilience Act \(DORA\)](https://www.servicenow.com/docs/access?context=audit-workspace&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

    Associate your evidence requests with financial regulatory requirements and guidelines from the Digital Operational Resilience Act \(DORA\). By aligning the relevant requests with these requirements and guidelines, you can help your asset managers better understand the compliance obligations that are associated with each request. They can then use this information to fulfill each request more accurately and efficiently.

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


## Activation information

Install Asset Audit Response by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Software Asset Management](https://www.servicenow.com/docs/access?context=c_SoftwareAssetMgmt&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

    The ServiceNow® Software Asset Management application enables you to track, evaluate, and manage the compliance and optimization of your software products and SaaS applications. You can reclaim unused rights, purchase new rights, and manage allocations for your entitlements.

-   **[Hardware Asset Management](https://www.servicenow.com/docs/access?context=ham-landing-page&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

    The ServiceNow® Hardware Asset Management application provides advanced workflow, automation, and mobile capabilities to track and manage your technology asset environment.

-   **[Audit Management](https://www.servicenow.com/docs/access?context=c_GRCAudits&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

    The ServiceNow Audit Management application enables you to plan, execute, and report on your audit engagements so that you can mitigate risks and compliance issues before they lead to audit failures.


**Parent Topic:**[IT Asset Management release notes](it-asset-management-rn-landing.md)

