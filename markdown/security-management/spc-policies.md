---
title: Use cases, policy examples, and supported service graph connectors in Security Posture Control
description: Use cases are different scenarios that you configure to help you identify specific types of tool coverage gaps. Each use case requires a policy or policies to audit your assets for potential violations. You can also define your own policies to help you fulfill requirements for your specific internal security standards.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Security Posture Control, Security Operations]
---

# Use cases, policy examples, and supported service graph connectors in Security Posture Control

Use cases are different scenarios that you configure to help you identify specific types of tool coverage gaps. Each use case requires a policy or policies to audit your assets for potential violations. You can also define your own policies to help you fulfill requirements for your specific internal security standards.

## Use cases

The Security Posture Control application supports various use cases that are included with the application. Use cases help you identify specific types of tool coverage gaps in your assets, internet exposure of cloud assets, and combinations with vulnerabilities. The policies that you need for the supported use cases are also included with the product.

You can view the coverage status for some of the key use cases on the Home \(landing\) page in the Security Posture Control Workspace at **Workspaces** &gt; **Security Posture Control** &gt; **Home** on the Home module \(landing page\).

Alternatively, you can view the supported service graph connectors and coverage status for some of the key use cases on the 'Service graph connectors supported' and 'Key use case setup' tabs at **All** &gt; **Workspaces** &gt; **Security Posture Control** &gt; **Connectors and use cases setup** \(the gear icon\).

**Note:**

The Key use cases tab on the Home landing pages does not list all the possible use cases. It provides you with a few important use cases that you activate to help you get started with Security Posture Control product deployment.

Before you activate policies for the supported use cases provided with the application verify you have completed the following tasks.

-   You have installed and configured all the required applications described in [Install the supported applications for Security Posture Control](../task/spc-install.md).
-   You have met one or more of the following prerequisites for each use case. 

1.  You are currently using or you install and activate service graph connectors for various categories.

    Categories for the use cases include service graph connectors that you must activate to get initial insights, and  service graph connectors that you have the option to activate for improved coverage for the assets Security Posture Control  is monitoring.

2.  You are currently using or you install and activate the Vulnerability Response application.
3.  You are currently using or you configure the Cloud Account Scan for your AWS and Azure accounts under ‘Cloud Security Posture Management’.

Specific requirements for each supported use case are described in the following sections. Additionally, you must activate one or more of the policies shipped with Security Posture Control for a use case. This concept is also covered in the following sections.

## Examples of base, child, and cloned policies

See [Examples of base, child, and cloned policies for Security Posture Control](spc-policy-examples.md) and how you can reuse the conditions of a base policy when you create other policies. Create base, child policies and cloning existing policies in these examples. These examples also help you see how the policy builder works in the Policies and findings module.

## Supported service graph connectors

See tables of supported service graph connectors, their tool categories, and the types of data they import in [Supported hardware service graph connectors for Security Posture Control](../reference/scp-hw-connectors-ci-classes.md) and [Supported software service graph connectors for Security Posture Control](../reference/spc-connector-types-ci-classes.md).

