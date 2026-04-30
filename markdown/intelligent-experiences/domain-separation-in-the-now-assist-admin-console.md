---
title: Domain separation in the Now Assist Admin console
description: If any conkeyrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file.In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conkeyref at the end that describes domain separation.Domain separation is supported for the Now Assist Admin console. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [Domain Separation, Now Assist Admin, console, Generative AI, Gen AI]
breadcrumb: [Now Assist reference, Now Assist, Enable AI experiences]
---

# Domain separation in the Now Assist Admin console

Domain separation is supported for the Now Assist Admin console. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

In the Now Assist Admin console, generative AI capabilities are organized into skills. Each skill can be configured differently for each domain or you can create a variant of a skill for a domain. By default, all skills exist in the global domain.

## How domain separation works in the Now Assist Admin console

You must enable domain separation on your instance first before you can use it for Now Assist skills.

Now Assist works with domain separation. When you use Now Assist in a domain-separated environment, users are only able to access data within their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists within the user's domain when generating that summary. When a skill is domain separated, only users who are in that domain can use the skill that you have configured for that scope.

If you're a service provider that hosts multiple clients in the same instance, you can set up domain separation to separate tenant data, processes, and administrative tasks. However, Assist consumption is tracked according to instance without differentiating between tenants. You can track your Now Assist usage in the Subscription Management dashboard.

If you want a domain to have a different version of an existing skill, you can reconfigure and activate the skill or create a variant in the preferred domain. See the section on granting access to Now Assist skills to a domain.

## Use cases

You can configure the inputs, roles, triggers, and prompts when you’re activating or editing a skill or a later variant of the skill.

Some use cases include the following examples:

-   Use the **Activity** field as an input in the incident summarization in one domain but only use the **short description** and **description** fields in another domain.
-   Grant certain roles access to the Now Assist panel in one domain while another domain has no role restrictions.
-   Trigger the generative AI capabilities by using quick actions in Agent Chat in only one domain.
-   Create a variant of a skill to test one prompt in one domain while another domain uses the default prompt for the skill.

## Granting a domain access to Now Assist skills

Domain separation is possible at the skill level and at the individual configuration level. When using the guided setup in the Now Assist Admin console, each configuration option has its own record that you can separate by domain. To create a record in a different domain, you must set up the skill while in the scope of your preferred domain.

1.  Navigate to the Now Assist Skill Config \(sn\_nowassist\_skill\_config\) table.
2.  Add the Domain field to the list. If it isn't present, select the gear icon at the top of the list and add the Domain field into the Selected column, then select **OK**.
3.  Find the skill that you want to enable on a domain-by-domain basis. Set Active to false on the skill that is in the global scope. You might need to change the scope to edit the record.
4.  Change your current domain to the domain that you want to enable the skill in.
5.  Navigate to **All** &gt; **Now Assist Admin Console** &gt; **Features**.
6.  Navigate to the skill that you want to activate according to domain and select **Activate skill**.
7.  Configure the skill as usual. For more information, see [Activate a Now Assist skill](../task/configure-a-now-assist-skill.md).
8.  Return to the Now Assist Skill Config \(sn\_nowassist\_skill\_config\) table. There should be a new record in the current domain. Open the new record.
9.  In a different browser tab, return to the Now Assist Skill Config table and open the deactivated skill record in the global domain.
10. Compare the global skill record to the one created within your domain. Records on the related list may not be present in the domain-specific skill. If they are not there, you must recreate those records in your domain and attach them to the related list in your domain-specific skill.
11. Repeat the process for each skill and each domain where you want to have the skill available.

**Parent Topic:**[Now Assist reference](../reference/now-assist-reference-landing.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

