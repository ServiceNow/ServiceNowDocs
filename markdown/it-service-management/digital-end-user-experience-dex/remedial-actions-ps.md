---
title: Creating and executing a PowerShell script-based remedial action
description: A custom remedial action can be created using a PowerShell script packaged in an Agent Client Collector \(ACC\) plugin and executed on endpoint devices through a check definition.
locale: en-US
release: yokohama
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [DEX remedial actions, Configure, Digital End-User Experience, IT Service Management]
---

# Creating and executing a PowerShell script-based remedial action

A custom remedial action can be created using a PowerShell script packaged in an Agent Client Collector \(ACC\) plugin and executed on endpoint devices through a check definition.

The ACC plugin contains the PowerShell script that defines the remedial action using commands and a Ruby script that calls the PowerShell script from the ServiceNow instance. When the signed ACC plugin is uploaded to a ServiceNow instance, the ACC agent downloads the plugin and executes the remedial action through a check definition you create.

Creating and executing a PowerShell script-based custom remedial action includes the following tasks.

1.  Creating an ACC plugin package that includes the PowerShell script, Ruby script, and allowlist. For more information, see [Create an ACC plugin package](../task/create-acc-plugin-structure.md).
2.  Generating a self-signed certificate, signing the plugin package, and verifying the signature to enable the remedial action to be executed securely on endpoint devices. For more information, see [Sign and verify an ACC plugin](../task/sign-verify-plugin.md).
3.  Uploading the signed plugin package to the ServiceNow instance. For more information, see [Create and edit Agent Client Collector plugins](https://www.servicenow.com/docs/access?context=create-edit-assets&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).
4.  Creating a check definition and linking it to the ACC plugin to enable the ACC agent to download it and execute the remedial action on the endpoint device. For more information, see [Create a check definition for a custom remedial action](../task/create-check-def-remedial-actions.md).
5.  Testing the check definition to verify if the ACC plugin is linked and the remedial action runs successfully. For more information, see [Test a check definition](../task/test-check-def.md).

