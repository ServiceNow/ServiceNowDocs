---
title: Understanding PaCE
description: PaCE enables you to manage, administer, and audit policies from a centralized location.
locale: en-US
release: yokohama
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# Understanding PaCE

PaCE enables you to manage, administer, and audit policies from a centralized location.

A PaCE policy is a set of pre-defined rules and logic that determines the desired behavior of an application or a service. When invoked, the rules in the policy are applied on the provided input, and a decision is reached. This decision-making is the main function of PaCE and helps determine if a policy is compliant or non-compliant. The decision is then relayed to the software calling service or application, so that it can act on it to enforce a desired behavior.

PaCE provides the following capabilities:

-   Full life cycle management of policies
-   Policy reuse
-   Audit and compliance
-   Testing and validation of policies
-   Central automation of compliance and regulatory processes

PaCE can be used to:

-   Identify posture drifts from a desired state in the current application.
-   Make decisions \(compliant or non-compliant\) based on a change in the application or service and enforce the decision to prevent a drift.
-   Automate execution of policies and eliminate dependency on humans.
-   Standardize policies so that they can be shared and reused within a service and across services.
-   Increase change velocity while including guardrails with automated workflows to provide preventive controls.
-   Collect evidence and proof of compliance for audit purposes. This feature can be used by internal auditors to automate the process of collecting evidence for governance and risk requirements.
-   Provide business context to PaCE policies by using control objectives to connect PaCE with the Integrated Risk Management and Policy and Compliance Management workspace.

PaCE enables policy developers to view and understand an existing policy, make and assess changes, and decide if a policy can be used as a baseline for another policy. They can also use PaCE before debugging to understand how the policy should work and why it is not working as expected.

PaCE provides a centralized platform for storing, managing, and using policies. By using PaCE, policies can be:

-   Well documented and all the requirements clearly defined.
-   Reused across the organization.
-   Tracked and new versions can be created when a policy is changed.
-   Tested and validated before deployment.

Policies are also containers for all the elements that make up a policy. These elements include meta-data related to the policy, the policy versions \(including policy scripts and inputs\), mapping information, and policy execution history.

You can define any number of policies within PaCE.

