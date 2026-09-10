---
title: Controlling what AI Desktop Actions can access
description: Control which desktop resources, such as files, folders, websites, and applications, AI Desktop Actions can access within your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/security\_policy\_governance\_concept.html
release: australia
topic_type: concept
last_updated: "2026-08-18"
reading_time_minutes: 6
keywords: [security policy, AI Desktop Actions, resource access control, governance, administrator configuration, policy management, desktop automation security]
breadcrumb: [Adaptive desktop actions for desktop and web, Configure, AI Desktop Actions, Enable AI experiences]
---

# Controlling what AI Desktop Actions can access

Control which desktop resources, such as files, folders, websites, and applications, AI Desktop Actions can access within your organization.

Create policies for defined user criteria and resource access rules to enforce consistent resource restrictions across your organization.

## Key concepts

-   **Policy**

    Collection of resource access rules that applies to a specific user group or set of users based on defined user criteria. Only active policies are enforced. For example, a "Finance Team Policy" restricts AI agents from accessing payroll documents.

-   **Resource access rule**

    A specific rule that controls access to one type of resource, such as a file, folder, website, or application. Each rule specifies the resource type, match pattern, access level \(allow or deny\), and permissions. Rules can be reused across multiple policies.

-   **Policy-rule mappings**

    Mappings that connect policies to the resource access rules they enforce. One policy can link to multiple rules, and one rule can be linked to multiple policies. When you update a rule, the change applies everywhere it is linked.

-   **User criteria**

    The condition that determines which users are subject to a policy. User criteria typically reference group membership, department, role, company, or other user attributes. For example, "members of the Finance group" or "users assigned to the Accounting role."

-   **Resource type**

    The category of resource being controlled: File, Folder, Website, or Application. Each resource type has specific field options, match types, and value formats.

<table id="table_rlc_23q_hkc"><thead><tr><th>

Resource type

</th><th>

Details

</th></tr></thead><tbody><tr><td>

File

</td><td>

-   **Match type**: Exact, Wildcard
-   **Value**: File path using forward slashes \(for example, `username/documents/report.pdf`\)
-   **Permissions**: Read, Create, Update, and Delete
-   Wildcard examples:
    -   `**/*.pdf` — All PDF files anywhere
    -   `**/*.log` — All log files anywhere
    -   `/documents/**/*.xlsx` — All Excel files in the documents folder and subfolders
    -   `/tmp/**` — All files in the tmp folder and subfolders


</td></tr><tr><td>

Folder

</td><td>

-   **Match type**: Exact, Wildcard
-   **Value**: Folder path using forward slashes \(for example, `/payroll`\)
-   **Permissions**: Read, Create, Update, and Delete
-   Wildcard examples:

`/private/**` — Private folders and all contents

</td></tr><tr><td>

Website

</td><td>

-   **Match type**: Exact, Wildcard
-   **Value**: Domain name \(for example, `github.com`, `*.internal.company.com`\)
-   **Permissions**: Not applicable
-   Wildcard examples:
    -   `*.servicenow.com` — All ServiceNow subdomains
    -   `github.com` — Exact domain match


</td></tr><tr><td>

Application

</td><td>

-   **Match type**: Not applicable
-   **Value**: Application name as seen in the Application folder \(for example, `chrome`, `python`, `Microsoft Excel`\)
-   **Permissions**: Not applicable


</td></tr></tbody>
</table>
## How it works

When a user begins a task, the system checks which active policies apply to that user based on user criteria, such as group membership. The system then uses the combined active resource access rules from all applicable policies to determine which resources the AI agent can access.

1.  When user logs in, the system identifies the user and their applicable policies based on user criteria.
2.  When the user provides a task, all active resource access rules from the user's applicable policies are retrieved.
3.  Before accessing any resource: file, folder, URL, application, the system checks whether the resource is permitted by the resource access rules.
4.  If a resource is restricted by any policy, the AI agent stops execution.
5.  If a resource is permitted by any policy, the AI agent automatically executes the task.

## Default policy and rules

The following policy and rules are available by default with installation of the AI Desktop Actions application.

|Name|Type|Description|
|----|----|-----------|
|Default Desktop Actions Policy|Policy|Default desktop actions policy with standard resource access rules|
|Allow ServiceNow|Rule|Allow access to ServiceNow websites|
|Allow Calculator|Rule|Allow access to Calculator application|
|Allow Text Files|Rule|Allow access to text files|
|Allow Downloads|Rule|Allow access to Downloads folder|
|Deny Terminal|Rule|Deny access to Terminal application|
|Deny Run Shell Script|Rule|Deny access to Run Shell Script application|
|Deny Automator|Rule|Deny access to Automator application|
|Deny Script Editor|Rule|Deny access to Script Editor application|

If you need AI Desktop Actions to access one of these apps for a specific task, you can update the resource access rules to allow these applications.

**Warning:** Restricted applications can execute system-level commands and scripts that aren't available through the graphical interface. If the AI agent proposes an alternate plan that involves restricted applications, review the plan carefully before granting access. After the task completes, revert access to Deny.

## Policy evaluation order

When AI Desktop Actions needs to access a resource, policies are evaluated in this order.

The system collects all active policies where the current user matches the user criteria, then gathers all active resource access rules linked to those policies. If any rule explicitly denies access to the resource, access is refused — Deny takes precedence. If any rule explicitly allows access, access is granted. If no rule matches, the user is prompted during execution to allow or deny access to the resource for that task. For security-sensitive resources, create explicit rules rather than relying on runtime prompts.

## Common use cases

-   **Protect sensitive files**

    Create a "Restricted Files" policy that denies AI agent access to payroll folders, HR documents, or financial records. Apply the policy to the Finance group.

-   **Limit external website access**

    Create a policy that allows access only to company-internal websites. Apply it to the IT Operations group.

-   **Control application access**

    Create a policy that restricts access to applications outside an approved developer toolset to avoid accidental launches of unknown or untrusted applications.

-   **Role-based automation**

    Create separate policies for different roles, such as HR, Finance, Operations, with resource restrictions appropriate to each role's responsibilities.

-   **Temporary restrictions**

    Temporarily deactivate a policy during maintenance, then reactivate it when complete. Deactivated policies aren't enforced.


## Known policy behaviors and limitations

-   **Multiple permission prompts for same resource**

    If a resource is not explicitly declared in a rule, the AI agent may ask for permission multiple times for the same resource during a single goal. This is expected behavior when no rule matches a resource.

    The system checks each resource access independently. For operations such as Read, Write, Update, and Delete on the same resource, each operation may trigger a prompt if no rule covers that specific operation.

    Create explicit Allow or Deny rules for resources your organization uses frequently. Use wildcard patterns to cover resource categories efficiently. For example, instead of creating separate rules for each URL, use a wildcard pattern like `*.internal.company.com` to allow all internal company subdomains in one rule.

-   **Denied applications take precedence**

    If any policy rule explicitly denies access to a resource, that Deny decision takes precedence over any Allow rules. The AI agent can't access the resource, regardless of other permissions.

    Verify that your Allow and Deny rules are carefully balanced. A broad Deny rule overrides more specific Allow rules.

-   **Default allow behavior when no rule matches**

    If no policy rule matches a resource, the AI agent prompts you for access during execution. This provides flexibility but may leave sensitive resources unprotected if not explicitly restricted.

    Use a default-deny approach: create explicit Allow rules for resources you want AI agents to access, rather than relying on implicit allow for unspecified resources.


-   **[Create a desktop action policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-da-policy.md)**  
Desktop action policies control which users are subject to resource access rules. Configure a policy to define the user criteria and link the rules that govern automated resource access.
-   **[Create a desktop action access rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-da-access-rule.md)**  
Configure rules to enforce security boundaries for AI agents in your organization. Resource access rules define which files, folders, websites, and applications AI Desktop Actions can access.

**Parent Topic:**[Configuring AI Desktop Actions for adaptive desktop actions for desktop and web](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ad-adaptive-path-desktop-da.md)

**Related topics**  


[Create a desktop action policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-da-policy.md)

[Create a desktop action access rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-da-access-rule.md)

[Known issues and limitations of adaptive desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/adaptive-desktop-actions-troubleshooting.md)

