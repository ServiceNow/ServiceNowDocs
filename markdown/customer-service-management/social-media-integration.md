---
title: Social media communication channel
description: Use the social media communication channel to associate social profiles and social media conversations with cases.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customer service case types, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Social media communication channel

Use the social media communication channel to associate social profiles and social media conversations with cases.

## Overview

Agents can select **Social** as the communication channel on the Case form. Selecting the Social channel adds the Social Profile field, which lets agents associate a specific social media profile with the case. Social media conversations related to a case are captured in the Social Logs related list.

Customer service managers can create social profiles for accounts, contacts, and consumers from the **Social Profiles** related list on each entity form. A social profile records a user's profile information for a specific social media channel. Managers can create multiple profiles per entity. Agents have read-only access to these profiles.

## Supported forms

The social media communication channel adds the following functionality to CSM forms:

-   **Case:** The Channel field includes the Social option. Selecting it adds the **Social Profile** field and the **Social Logs** related list.
-   **Account, Contact, and Consumer:** Each form includes the **Social Profiles** related list for creating and managing profiles.

## Plugin

The Customer Service Social Integration plugin \(com.sn\_cs\_social\) is activated as part of the Customer Service Management plugin.

## Tables

The Customer Service Social Media plugin adds the following tables.

|Table|Description|
|-----|-----------|
|Social Channels \(sn\_app\_cs\_social\_social\_channel\)|Stores available social media channels.|
|Social Profiles \(sn\_app\_cs\_social\_social\_profile\)|Stores social profiles created for accounts, contacts, and consumers.|
|Social Logs \(sn\_app\_cs\_social\_social\_log\)|Stores social media conversation details related to cases.|

