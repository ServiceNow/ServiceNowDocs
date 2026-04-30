---
title: Exploring Conversational Interfaces Diagnostic Tool
description: The Conversational Interfaces Diagnostic Tool lets admins search for, identify, and resolve issues with conversational interfaces.
locale: en-US
release: zurich
product: Conversational Interfaces Diagnostics Tool
classification: conversational-interfaces-diagnostics-tool
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [exploring, Diagnostic Tool, Conversational Interfaces]
breadcrumb: [Conversational Interfaces Diagnostic Tool, Conversational Interfaces]
---

# Exploring Conversational Interfaces Diagnostic Tool

The Conversational Interfaces Diagnostic Tool lets admins search for, identify, and resolve issues with conversational interfaces.

The Conversational Interfaces Diagnostic Tool lets admins search for, identify, and resolve issues with conversational interfaces.

Technical support engineers set up the Conversational Interfaces Diagnostic Tool on the server. Technical support engineers create and manage the Conversational Interfaces diagnostic category records and content that the Conversational Interfaces Diagnostic Tool uses.

After the technical support engineers create the diagnostic categories and content, admins can start using the Conversational Interfaces Diagnostic Tool on the chat widget. Admins must have the admin or virtual\_agent\_admin role.

The Conversational Interfaces Diagnostic Tool is available for both Virtual Agent and Virtual Agent Lite.

**Note:** Before using the Conversational Interfaces Diagnostic Tool, admins must activate the Conversational Interfaces - Diagnostics plugin \(sn\_ci\_diagnostics\) available on the ServiceNow® Store store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Conversational Interfaces Diagnostic Tool workflow

After you've described the issue you want to solve, the Conversational Interfaces Diagnostic Tool workflow begins using the relevant diagnostic topics and topic blocks. These topics and topic blocks are used for identifying, diagnosing, solving, and collecting data for the issue described.

For example, the diagnostic workflow does the following:

-   Prompts you for the required data, based on the issue you want to solve.
-   Includes a list of Knowledge Base \(KB\) articles where you can find more information, as applicable. If you aren't finding the information you need, you can also search for additional KB articles.
-   Gives you the option of downloading diagnostic support information.
-   Lets you select another issue to solve.

The diagnostic workflow and the options and prompts you see correspond to the issue you are trying to diagnose and solve. The diagnostic workflow uses an AI Search filter as part of the diagnosis. For more information about AI Search and how to configure it, see [Configuring AI Search](https://www.servicenow.com/docs/access?context=configuring-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

The diagnostic topic block workflow also includes solutions for messaging integrations, such as Microsoft Teams. It also helps with Advanced Work Assignment configuration issues.

In the workflow, the admin describes the issue. The tool runs a health check and returns available troubleshooting information, as well as contact information for Now Support if the problem was not solved.

## Conversational Interfaces Diagnostic Tool benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Diagnose general errors, such as error messages and system property issues.|[Diagnose Conversational Interfaces errors](../task/diagnose-general-error.md)|Admins|
|Identify and solve Microsoft Teams configuration issues.|[Diagnose Microsoft Teams configuration issues](../task/diagnose_ci_plugin_issues.md)|Admins|
|Identify and resolve common Advanced Work Assignment \(AWA\) configuration issues.|[Diagnose Advanced Work Assignment configuration issues](../task/diagnose-awa-no-agents-avail.md)|Admins|

