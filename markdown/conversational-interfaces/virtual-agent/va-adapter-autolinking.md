---
title: Account linking in pre-built messaging integrations
description: In Virtual Agent, account linking maps the users of a supported chat or messaging application to their ServiceNow user profile. Account auto-linking authenticates your messaging users, which enables users to automatically access Virtual Agent topics that involve ServiceNow records. If needed, users can also manually unlink from or link to their ServiceNow accounts.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Account linking in pre-built messaging integrations

In Virtual Agent, account linking maps the users of a supported chat or messaging application to their ServiceNow user profile. Account auto-linking authenticates your messaging users, which enables users to automatically access Virtual Agent topics that involve ServiceNow records. If needed, users can also manually unlink from or link to their ServiceNow accounts.

## How account auto-linking works

In the Conversational Integrations for Slack, Microsoft Teams, and Workplace from Facebook, you have the option to enable account auto-linking, which automatically links messaging users to their ServiceNow accounts. If you enable the account auto-linking feature on the Messaging Apps Integration page, your users are not prompted to link to their ServiceNow accounts when they engage with the virtual agent.

In earlier releases, messaging users were prompted to link to their ServiceNow accounts or continue as guests. However, for the Conversational Integrations for Slack, Microsoft Teams, and Workplace, if you enable account auto-linking, your users do not manually link their messaging accounts to their ServiceNow accounts, provided that they use the same email account for their messaging and ServiceNow accounts. During auto-linking, Virtual Agent maps the email accounts of messaging users to their email accounts defined in their profiles in the Users \[sys\_user\] table. When the email accounts match, the user is automatically linked \(authenticated\) and they do not see the **Link to ServiceNow** button when they begin a bot conversation.

In messaging integrations, your users can still use the **logout** command during bot conversations to unlink from their ServiceNow accounts. However, in all subsequent conversations after unlinking, Virtual Agent prompts them to link their accounts. When they engage with the virtual agent, they are prompted to link to their ServiceNow account or continue as a guest user.

## Account auto-linking

You can allow a user's 3rd party accounts to be auto-linked to their ServiceNow® profile.

You can enable account auto-linking in the sys\_cs\_provider.list. This feature bypasses the prompt for the users to link their accounts manually.

**Note:** Account linking is possible only for users who belong to the same domain that was used for installing Microsoft Teams on an instance. To auto-link users from other domains, ensure that Microsoft Teams installation is done using the global domain.

In the navigation filter type `sys_cs_provider.list`. Select the connection record you wish to link. Check the **Allow account linking** box, then check the **Auto link users' ServiceNow profiles** box that appears. Fill in the **Automatic link action** field with the corresponding account linking script.

Example: Account auto-linking script

```
var response_body = inputs['response_body'];
var status_code = inputs ['status_code'];
var email_id = '';
if(status_code>200 && status_code<=210){
    email_id = response_body && JSON.parse(response_body).userPrincipalName;
}
var sysUserId = null;

if(email_id){
    var gr = new GlideRecord("sys_user");
    gr.addQuery("email",email_id);
    gr.query();
    while(gr.next()){
        sysUserId = gr.getUniqueValue();
    }
}
if(sysUserId){
    outputs['status'} = 'Success';
    outputs['userid'] = sysUserId;
}
else{
    outputs['status'] = 'Failure';
}

})(inputs,outputs);
```

-   **[Unlink your ServiceNow user account from a messaging application for Virtual Agent conversations](../task/unlink-va-messaging.md)**  
If needed, you can unlink your ServiceNow user account from a messaging app used for the Now Virtual Agent.
-   **[Relink your ServiceNow user account to a messaging application for Virtual Agent conversations](../task/link-accounts-with-virtual-agent.md)**  
Relink your ServiceNow account to a third-party messaging application to access non-public Virtual Agent topics that use ServiceNow records.

**Parent Topic:**[Integrating Virtual Agent with messaging apps](va-integration-messaging-apps.md)

