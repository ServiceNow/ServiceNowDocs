---
title: Configure skills in a domain for Now Assist for Customer Service Management \(CSM\)
description: Activate the skills with different skill configurations in each domain in the Now Assist for Customer Service Management \(CSM\) application.
locale: en-US
release: yokohama
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Domain separation in Now Assist for Customer Service Management \(CSM\), Configure, Now Assist for Customer Service Management \(CSM\), Customer Service Management]
---

# Configure skills in a domain for Now Assist for Customer Service Management \(CSM\)

Activate the skills with different skill configurations in each domain in the Now Assist for Customer Service Management \(CSM\) application.

## Before you begin

Role required: admin

## About this task

By default, the skill configurations in the domains inherit the settings from the global domain unless they’re overridden by the new configurations in that domain.

## Procedure

1.  Change the current domain to the domain that you want to activate the skills in by selecting the new domain.

    ![Different domains that are created under the global scope.](../image/domain-separation-change-domain.png "Domain scope")

    For example, if you want to configure the skill in ParentDomain, change the domain scope to ParentDomain.

2.  Navigate to **All** &gt; **Now Assist Admin Console** &gt; **Features** &gt; **Features**.

3.  In the Now Assist Admin console, select the global skill configuration to activate it within the current domain and to set up its own unique skill configuration.

    As shown in the following example, a modal pop-up window confirms that the skill configuration is being edited in the current domain. This action creates a skill configuration that overrides the existing global configuration. The active skill configuration in use is derived from the global domain and shares the same name as the global skill configuration.

    ![Confirmation modal pop-up window that indicates the skill configuration is being edited in the current domain.](../image/domain-separation-modal.png "Edit skill in a domain")

4.  Proceed to the guided setup by selecting **Yes, edit**.

    The configuration setup applies to the current domain and is inherited by its child domain. The name of the skill changes to &lt;Skill Name&gt; for &lt;Domain Name&gt;. For example, if the skill configuration - Case summarization for ParentDomain is activated, it overrides the global setting and applies to both the ParentDomain and ChildDomain. However, if the skill configuration Case summarization for ChildDomain is activated in ChildDomain, it only applies to ChildDomain.

    **Note:** The activation order must follow Global &gt; Parent domain &gt; Child domain to ensure a proper inheritance and overrides. If the child skill configuration in the child domain is activated before the parent domain, the parent skill configuration can't override the existing skill configuration in the child domain. Consequently, both the parent skill and the child skill remain active in the child domain and the result is a misconfiguration.

    ![Configuration setup that will be applicable to the current domain and name of the skill changes to <Skill Name> for <Domain Name>.](../image/domain-separation-changed-skill-name.png "New skill configuration name")

    More information about domain separation for CSM can be found in [Domain separation and Customer Service Management](https://servicenow.com/docs/csh?topicname=domain-separation-customer-service.html&version=latest)


