---
title: Use generative AI skills in Now Assist for Vault
description: The Now Assist for Vault application includes the generative AI skills and features that enable you to streamline your administrative workload.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow Vault]
---

# Use generative AI skills in Now Assist for Vault

The Now Assist for Vault application includes the generative AI skills and features that enable you to streamline your administrative workload.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

After you activate skills, they appear in the Ask Now Assist panel in ServiceNow Vault console.

![Vault console dashboard with the Ask Now Assist panel highlighted.](../image/vault-dashboard-now-assist.png)

By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the Now Assist Admin console](https://www.servicenow.com/docs/access?context=domain-separation-in-the-now-assist-admin-console&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://www.servicenow.com/docs/access?context=next-experience-pickers&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).\)

-   **[Generate a custom data pattern by using Now Assist for Vault](../task/generate-custom-data-pattern-now-assist-vault.md)**  
Use the generate custom data pattern skill to create a custom regular expression data pattern from your description and add it as an active data pattern to your instance.
-   **[Check role access for an encrypted column with Now Assist for Vault](../task/check-role-access-now-assist-vault.md)**  
Use the check role access for encrypted column skill to identify user roles that have access to encryption and decryption keys in your instance.
-   **[Schedule a Data Discovery job with Now Assist for Vault](../task/schedule-data-discovery-job-now-assist-vault.md)**  
Use the schedule data discovery job skill to schedule one-time or recurring Data Discovery jobs with Now Assist. Data Discovery jobs can detect sensitive data such as PII or PHI provided as input to the Now LLM.

**Parent Topic:**[ServiceNow Vault](../../vault/reference/servicenow-vault-landing.md)

