---
title: Allow policy exception requests from other applications
description: Starting with Version 10.1, you can leverage new policy exception capabilities in Policy and Compliance Management from within other applications.
locale: en-US
release: xanadu
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Policy and Compliance Management enhancement steps, Implementing Policy and Compliance Management, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Allow policy exception requests from other applications

Starting with Version 10.1, you can leverage new policy exception capabilities in Policy and Compliance Management from within other applications.

Requests are routed through multiple approvals based on risk rating, policy, and control objective associated with an exception. Compliance and risk teams obtain better visibility with respect to exceptions raised for vulnerabilities.

**Note:** Starting with Version 10.1, if you have installed Version 10.3 of the Vulnerability Response application, you can request policy exceptions using the GRC policy exception management capability inherent in the Policy and Compliance Management application. For details, see [Policy Exception Integration with Vulnerability Response](../reference/request-pe-from-vr.md).

Before allowing other applications to leverage the policy exception capabilities of Policy and Compliance Management, you must first add the application to the Integration Registry and then perform some preliminary setup.

-   **[Configure policy exceptions from other applications](../task/configure_policy_except_from_app.md)**  
Before you can request policy exceptions from applications other than Policy and Compliance Management, you must add a UI action for making the request and, optionally, create a new list view to see policy exception target records on the Policy Exception form.
-   **[Register other applications to request policy exceptions](../task/enable-other-apps-to-request-policy-exceptions.md)**  
Enable other applications to request policy exception from any table such as Problem or Incident and so on. The applications must be added and configured in the Integration Registry.
-   **[Define policy exception reason choices](../task/define-reason-choices.md)**  
You can define reason choices to be available to any user who requests an exception.
-   **[Define policy categories](../task/define-policy-categories.md)**  
You can filter policies by specific criteria to limit the number of policies displayed when you are creating policy exceptions.
-   **[Create an exception questionnaire](../task/create-except-quest.md)**  
When you are setting up the Policy Exception Integration Registry, you can define configurable questions that can be included in risk assessments created from templates. The Policy Exception Integration Registry can be associated with one template at a time.
-   **[Define policy exception verification rules](../task/define-verification-rules.md)**  
The verification rule is used to verify the accuracy and completeness of a policy exception request prior to sending it out for approvals. You can define multiple levels of approvers for an application.
-   **[Define policy exception approval rules](../task/define-approval-rules.md)**  
Approval rules define the criteria \(risk rating, policy or control objective\) that is used for sending approval requests for an exception. Rules can be configured for an application and you can identify multiple levels of approvers, as needed.

**Parent Topic:**[Policy and Compliance Management enhancement steps](../../grc-policy-compliance-implementation/concept/policy-compliance-optional-steps.md)

