---
title: Module access policy debugger
description: Use the module access policy debugger to review logging information and understand why your users are or aren’t granted access to an encryption context.
locale: en-US
release: australia
product: Platform Encryption
classification: platform-encryption
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Key Management Framework Reference, Key Management Framework, Encryption]
---

# Module access policy debugger

Use the module access policy debugger to review logging information and understand why your users are or aren’t granted access to an encryption context.

Module access policies \(MAPs\) define instance-level controls for access to cryptographic modules. Callers \(for example, a user or script\) require explicit access to use a cryptographic module for encryption and decryption. Use the debugger to see which policies are evaluated when a caller attempts to access a cryptographic module. You can also use the debugger and learn why access is or isn’t being granted.

This flowchart shows how your instance evaluates requests for access to a cryptographic module.

![Flowchart showing the how access to cryptographic modules are evaluated](../image/map-eval-flowchart.png)

## Control access to the debug logs

Access to the module access debug logs is determined by role. Users with the **sn\_kmf.admin** and **sn\_kmf.cryptographic\_manager** roles have access to the debugger. Grant access to other roles using the **glide.kmf.module\_access\_policies.debugger.authorized.roles** system property. The value of this property is a comma-separated list of roles that access the debug logs.

## Enable or disable the debugger

To enable debug logging messages for module access policies, navigate to **All** &gt; **Diagnostics** &gt; **Session Debug** &gt; **Debug Module Access Policies** &gt; **.**

When you’re finished debugging, you can disable the logging messages by navigating to **All** &gt; **Diagnostics** &gt; **Session Debug** &gt; **Disable All** &gt; **.**

## Access the logs

After enabling debugging, navigate to a page that triggers a MAP evaluation to view the MAP debug logs. Debug messages appear at the bottom of the page.

**Tip:** You can use impersonation to troubleshoot access for other users. For details on impersonation, see [Impersonating users](https://www.servicenow.com/docs/access?context=c_ImpersonateAUser&version=australia&pubname=australia-platform-administration&ft:locale=en-US). To view the debug logs from the perspective of another user, make sure that your module access policies with the **role** type have the **Impersonation** field set as **true**.

![Example debug output](../image/map-debug-logging-1.png)

In this example, a caller invokes two access requests to the `global.fuji` cryptographic module. A symmetric encryption, which is granted, and a symmetric decryption, which was denied.

## Understanding log entries

Debugging information is structured using this format.

1.  This first line displays the cryptographic module receiving the access request.
2.  The lines between the first and last line displays the evaluated MAPs in the order that they were evaluated, and includes their name, type, target, granular operation, and result.
3.  The last line displays the Policy Decision \(if applicable\) and the net access result for the caller \(whether the caller is granted access\).

Each line starts with an icon that indicates its message type.

|Icon|Message type|
|----|------------|
|![Informational icon](../image/map-vis-icon-1.png)|Informational message|
|![MAP grant access icon](../image/map-vis-icon-2.png)|Module access policy grants access|
|![MAP deny access icon](../image/map-vis-icon-3.png)|Module access policy denies access|
|![Caller grant access icon](../image/map-vis-icon-4.png)|Caller is granted access|
|![Caller deny access icon](../image/map-vis-icon-5.png)|Caller is denied access|
|![No MAP icon](../image/map-vis-icon-6.png)|No module access policy to evaluate|

## Debug log examples

-   **Access granted message**

    ![Debugging output for granted access](../image/map-vis-example-1.png)

-   **Access denied message**

    ![Debugging output for denied access](../image/map-vis-example-2.png)

-   **Access denied \(No module access policies to evaluate**

    ![Debugging output for denied access due to no MAP policies](../image/map-vis-example-3.png)

-   **Access denied \(insufficient privileges\)**

    ![Debugging output for denied access due to insufficient privileges](../image/map-vis-example-4.png)


**Parent Topic:**[Key Management Framework Reference](understanding-kmf.md)

**Related topics**  


[Key Management Framework key life-cycle states](../reference/key-life-cycle-states.md)

[Roles installed with Key Management Framework](../reference/kmf-roles.md#)

[Module access policy visualization](map-vis-concept.md)

[Encryption and Key Management subscription bundle](../../encryption/reference/encryption-sku.md)

