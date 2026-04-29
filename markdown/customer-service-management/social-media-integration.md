---
title: Social media integration
description: Support case resolution through social media communication channels.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Enable communication channels, Configure, Customer Service Management]
---

# Social media integration

Support case resolution through social media communication channels.

When working with customers or consumers to create and resolve cases, agents can select **Social** as the communication channel and add a social profile to the Case form. Any communication with customers or consumers that takes place through social media is recorded on the Case form in the **Social Logs** related list.

Customer service managers can create one or more social profiles for a user by recording a user's social profile information on a specific social media channel such as Twitter or Facebook. Managers can create social profiles for accounts, contacts, and consumers from the **Social Profiles** related list on the entity form. Agents have read-only access to these profiles.

## Integration with Customer Service Management

The social media communication channel is integrated with the following Customer Service Management forms: Case, Account, Contact, and Consumer.

On the Case form, the **Channel** field includes the **Social** option. Selecting this option adds the **Social Profile** field to the Case form, in which you can select a specific social media channel. The **Social Logs** related list captures the details of social media conversations.

The Account, Contact, and Consumer forms include the **Social Profiles** related list. Customer service managers can create one or more profiles for each of these entities.

## Plugins

The Customer Service Social Integration plugin \(com.sn\_cs\_social\) is activated as part of the Customer Service Management plugin.

## Tables

The Customer Service Social Media plugin adds the following tables.

|Table|Description|
|-----|-----------|
|Social Channels \(sn\_app\_cs\_social\_social\_channel\)|Stores the social channels, which are brought in by the social integration tool.|
|Social Profiles \(sn\_app\_cs\_social\_social\_profile\)|Stores the social profiles created for each customer contact or consumer.|
|Social Logs \(sn\_app\_cs\_social\_social\_log\)|Stores the details of social media conversations related to cases.|
|Customer Service integration with Social Media Store \(sn\_cs\_social\_host\)|The Customer Service integration with Social Media app allows agents to select Social as the communication channel and add a social profile to the Case form. Any communication with customers or consumers that takes place through social media is recorded on the Case form in the Social Logs related list.|

