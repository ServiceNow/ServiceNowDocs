---
title: Run the Quick Start tests for Third-party Risk Management
description: Verify that TPRM still works after you make configuration changes such as applying an upgrade or developing an application. Copy and customize the quick-start tests to pass when using your instance-specific data.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Run the Quick Start tests for Third-party Risk Management

Verify that TPRM still works after you make configuration changes such as applying an upgrade or developing an application. Copy and customize the quick-start tests to pass when using your instance-specific data.

GRC: Vendor Manager Workspace and Third-party Risk Management quick start tests require activating the Vendor Manager Workspace and Third-party Risk Management plugin \(com.sn\_vdr\_risk\_asmt\) and loading demo data.

**Important:**

The Vendor Management Workspace for ITSM \(sn\_itsm\_vendor\) is deprecated as of the Australia release. It is hidden and no longer available for activation for new customers.

The GRC: Vendor Management Workspace quick start tests listed below require this plugin and are not applicable if your instance does not have it activated. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

|Test|Description|
|----|-----------|
|GRC: Create Engagement Risk Assessment|Creates and submits an engagement risk assessment to an engagement.|
|GRC: Vendor Risk Scoring - Cancel assessment for engagement|Verifies a request to recalculate a risk rating is automatically created on an Engagement and Third party after one assessment for the Engagement is cancelled.|
|GRC: Vendor Issue ATF|Creates and submits a third-party risk issue form and third-party risk task form.|
|GRC: Create Vendor Risk Assessment|Creates and submits a vendor risk assessment to a vendor.|
|GRC: Vendor Portal - Answer and Return Assessment|Vendor contact answers and submits assessment in the Service Vendor Portal.|
|GRC: Vendor Tiering Assessment|Selects and submits an assessment to respective assessors after changing the duration.|

**Related topics**  


[Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&version=australia&pubname=australia-application-development&ft:locale=en-US)

