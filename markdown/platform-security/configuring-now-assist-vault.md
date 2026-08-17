---
title: Install ServiceNow Otto for Vault
description: Install the ServiceNow Otto for Vault application from the ServiceNow Store to get AI capabilities within Vault.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/configuring-now-assist-vault.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring ServiceNow Vault, ServiceNow Vault]
---

# Install ServiceNow Otto for Vault

Install the ServiceNow Otto for Vault application from the ServiceNow® Store to get AI capabilities within Vault.

## Before you begin

Review the ServiceNow Otto for Vault application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## Procedure

1.  From the ServiceNow Otto for Vault application page on the ServiceNow Store, select **Buy**.

2.  After approval has been granted, on your instance, navigate to **All &gt; System Applications &gt; All Available Applications &gt; All**.

3.  Using the search bar, search for the ServiceNow Otto for Vault application \(sn\_vault\_gen\_ai\).

4.  Select **Install**.

5.  Verify that the ServiceNow Otto for Vault skills are active:

    1.  Navigate to **All &gt;Admin &gt; AI Admin Hub &gt; AI Skills**.

    2.  In the workflow list, select **Vault**.

    3.  Verify that the skills are active.

    \[Omitted image "ai-admin-hub-vault-skills.png"\] Alt text: AI Admin Hub showing skills from ServiceNow Otto for Vault.

6.  Verify that ServiceNow Otto for Vault agentic workflows are activated by following the steps in [Activate an agentic workflow template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-aia-use-case.md).

    By default, the workflows are active when you install ServiceNow Otto for Vault. This step is in case a user deactivated them after installation.


