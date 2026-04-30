---
title: Credential affinity for Discovery and Orchestration
description: Credential affinity is an association between a set of credentials and a device on your network.
locale: en-US
release: yokohama
product: Connections and Credentials
classification: connections-and-credentials
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Getting started with credentials, Connections and Credentials, Access Management]
---

# Credential affinity for Discovery and Orchestration

Credential affinity is an association between a set of credentials and a device on your network.

When Discovery or Orchestration first attempts to access a device, they try all available credentials until they find the correct ones. After identifying the credentials for a device, Discovery and Orchestration create an affinity between the credentials and the device using the Credential Affinity `[dscy_credentials_affinity]` table. All subsequent discoveries or Orchestration activities attempt to match the credentials in this table with a device for which an affinity exists. If credentials for a device change, Discovery and Orchestration try all available credentials again until they create a new affinity.

![Lookup process for credential affinity](../image/CredentialsAffinityDiagram.png "Credential Affinity diagram")

**Note:** If Orchestration and Discovery are installed, and credential alias is enabled, multiple affinities can exist. In this case, the platform looks up credentials for each affinity and inserts the credential for the affinity with the lowest order into the probe.

