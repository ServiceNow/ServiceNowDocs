---
title: Guarded script evaluator
description: The guarded script evaluator enhances instance security by supporting only a restricted scripting language and detecting or rejecting untrusted scripts that use unsupported JavaScript features.
locale: en-US
release: australia
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2024-12-19"
reading_time_minutes: 8
breadcrumb: [Sandbox environment, Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# Guarded script evaluator

The guarded script evaluator enhances instance security by supporting only a restricted scripting language and detecting or rejecting untrusted scripts that use unsupported JavaScript features.

The guarded script evaluator uses a domain-specific language \(DSL\) that permits only a small set of JavaScript syntax, such as simple expressions and function calls, and certain APIs in server-side scripts that run in the script sandbox environment.

**Note:** Guarded script doesn't apply to script includes, which run in the application scope outside of the sandbox, or client-side scripts.

When a script that uses only supported features is evaluated by guarded script, it executes successfully. If a script contains unsupported features, guarded script handles it differently depending on the following factors:

-   The origin of the transaction: authenticated user or unauthenticated \(guest\) user.
-   The enforcement phase for authenticated traffic configured for an instance.

Scripts with a guarded-script exemption bypass guarded script restrictions and are routed to the script sandbox evaluator for execution instead. For more information about the script sandbox evaluator, see [Script sandbox evaluator](script-sandbox.md).

## Guarded script enforcement

Beginning with the Australia Patch 2 release, incompatible scripts sent to the server by guest users are rejected on all instances by default. Scripts sent by authenticated users are evaluated differently depending on the instance type.

<table id="tableID-guarded_script_default_enforcement"><thead><tr><th>

Transaction type

</th><th>

Default behavior

</th></tr></thead><tbody><tr><td>

Unauthenticated \(guest\)

</td><td>

Enforced immediately on all instances. Guarded script rejects incompatible scripts, adds them to the Incompatible Guarded Scripts list, and logs errors.

</td></tr><tr><td>

Authenticated

</td><td>

-   Upgraded cloud-based instances: Phased enforcement beginning with guarded script detecting but not rejecting incompatible scripts \(Phase 1: Detection\) and automatically advancing to each subsequent phase \(Phase 2: Syntax enforcement and Phase 3: Full enforcement\) after two weeks.
-   Upgraded on-premise instances: Not enforced, but guarded script detects and records incompatible scripts \(Phase 1: Detection\). Administrators can configure when to transition to the subsequent enforcement phases.
-   New instances: Enforced immediately. Guarded script rejects incompatible scripts, adds them to the Incompatible Guarded Scripts list, and logs errors \(Phase 3: Full enforcement\).

</td></tr></tbody>
</table>For authenticated traffic on upgraded instances, guarded script enforcement advances through the following phases to provide time to detect and review incompatible scripts before rejecting them. Before transitioning to Phase 2: Syntax enforcement and Phase 3: Full enforcement, the system creates exemptions for any incompatible scripts detected during each phase automatically. Those exempted scripts bypass guarded script restrictions and run in the script sandbox evaluator. To further secure your instance, you can still review any scripts that have an automatic exemption, update them to be compatible with guarded script, and then remove the exemption.

**Important:** Incompatible scripts are only detected and recorded when transactions calling them are sent to the server. You should test business-critical scripts that run infrequently, such as for quarterly or annual processes, before moving to Phase 3: Full enforcement and review the Incompatible Guarded Scripts list regularly to identify any scripts that may need remediation before they could be rejected. For more information, see [Review and update scripts incompatible with guarded script](../task/review-incompatible-guarded-scripts.md).

<table id="table_yt2_cc4_y3c"><thead><tr><th>

Phase

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Phase 1: Detection

</td><td>

-   Not enforced. Scripts execute regardless of guarded script restrictions.
-   Detects and records only scripts with incompatible syntax in the Incompatible Guarded Scripts list. Scripts with incompatible APIs aren't detected yet.
-   At the end of this phase, exemptions are created automatically for scripts with incompatible syntax, which routes them to the script sandbox evaluator for execution instead.

 Default duration: two weeks

</td></tr><tr><td>

Phase 2: Syntax enforcement

</td><td>

-   Enforces guarded script syntax restrictions only, rejecting scripts with incompatible syntax and logging errors, but doesn't reject scripts with incompatible APIs.
-   Detects and records scripts with any incompatibilities in the Incompatible Guarded Scripts list.
-   At the end of this phase, exemptions are created automatically for scripts that use incompatible APIs, which routes them to the script sandbox evaluator for execution instead.

 Default duration: two weeks

</td></tr><tr><td>

Phase 3: Full enforcement

</td><td>

-   Enforces both guarded script syntax and API restrictions. Guarded script rejects all incompatible scripts and logs errors.
-   Detects and records scripts with any incompatibilities in the Incompatible Guarded Scripts list.
-   In this phase, any additional exemptions must be created manually.

</td></tr></tbody>
</table>## Configuring guarded script

Beginning with the Australia Patch 2 release, administrators can configure the enforcement process for authenticated traffic using the following system properties and script include.

<table id="table_tzb_vzf_y3c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.glide.script.sandbox.ks.watchdog.phase

</td><td>

The current phase of enforcement that the guarded script evaluator applies to untrusted scripts.If the **com.glide.script.sandbox.ks.watchdog.auto.advance** property is set to true, the value of this property is automatically updated according to the duration specified with the **com.glide.script.sandbox.ks.watchdog.phase.duration.days** property.

-   Type: String
-   Default value:
    -   1 for upgraded instances
    -   3 for new \(or zBoot\) instances
-   Valid values:
    -   1: Enables Phase 1: Detection.
    -   2: Enables Phase 2: Syntax enforcement.
    -   3: Enables Phase 3: Full enforcement.

</td></tr><tr><td>

com.glide.script.sandbox.ks.watchdog.phase.duration.days

</td><td>

The duration, in days, that each of Phase 1: Detection and Phase 2: Syntax enforcement is in effect.To pause automatically advancing between each phase, set the value to `-1`.

-   Type: Integer
-   Default value: 14

</td></tr><tr><td>

com.glide.script.sandbox.ks.watchdog.auto.advance

</td><td>

An option to control automatically advancing between enforcement phases according to the duration configured with the **com.glide.script.sandbox.ks.watchdog.phase.duration.days** property.-   Type: Boolean
-   Default value:
    -   true for cloud-based instances
    -   false for on-premise instances

</td></tr><tr><td>

com.glide.script.sandbox.ks.watchdog.enabled

</td><td>

An option to turn off the guarded script evaluator and route all untrusted scripts to the script sandbox evaluator instead.**Warning:** Don't set this property to false on production instances. Setting this property to false removes the enhanced security protections provided by the guarded script evaluator.

-   Type: Boolean
-   Default value: true

</td></tr></tbody>
</table>For information about configuring system properties, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

The GlideGuardedScript script include supports methods for transitioning between enforcement phases and validates that the transition occurs sequentially. These methods are primarily useful for instances that aren't configured to advance automatically, such as upgraded, on-premise instances. From the Scripts - Background module, you can run the following methods to transition to each phase as needed.

|Method|Description|
|------|-----------|
|`new GlideGuardedScript().resetToPhase1()`|Resets the instance to Phase 1: Detection for authenticated transactions. Any automatic exemptions created previously remain.|
|`new GlideGuardedScript().advanceToPhase2()`|Validates that Phase 1: Detection is complete, creates exemptions for scripts with incompatible syntax, and advances the instance to Phase 2: Syntax enforcement for authenticated transactions.|
|`new GlideGuardedScript().advanceToPhase3()`|Validates that Phase 2: Syntax enforcement is complete, creates exemptions for scripts that use incompatible APIs, and advances the instance to Phase 3: Full enforcement for authenticated transactions.|

For information about running background scripts, see [Scripts - Background module](c_ScriptsBackground.md).

## JavaScript features supported by guarded script

Review the JavaScript features that guarded script supports to help you analyze scripts in the Incompatible Guarded Scripts list and either rewrite them or create an exemption for them.

Guarded script supports only a single, simple expression or function call using the following JavaScript syntax:

-   Primitive literals: number, string, boolean, null, undefined
-   Common operators: +, -, &lt;, !==, &amp;&amp;, instanceof, typeof
-   Ternary operator \(?:\)
-   Array literals \(\[1, 'x'\]\)
-   Property access using dot notation \(a.b\)
-   Indexed array access with constant numbers \(a\[0\]\)
-   Calling script includes that have the **Sandbox enabled** option selected

Other JavaScript syntax, including variable and function declarations, assignment operators \(=\), control flows, and multiple statements, aren't supported by guarded script. For example, guarded script rejects the following script because it contains a variable and control flow logic \(`if` statement\):

```javascript
javascript:var ret='customer=true';
if (current.relationship_type.to == 'partner')
  ret = 'partner=true';
ret + '^sys_id!=' + current.from_company;
```

If you move this logic to a script include and call the script include from the script instead, guarded script executes the updated script:

```javascript
javascript:new MyAppUtils().getAccountToFilter(current);
```

In addition, guarded script supports only a restricted list of ServiceNow server-side JavaScript APIs and built-in JavaScript APIs. For a list of supported APIs, see [JavaScript APIs supported by guarded script](../reference/guarded-script-allowed-apis.md).

You should review the Incompatible Guarded Scripts list regularly and either rewrite scripts to use supported features to further secure your instance or create exemptions for scripts that can't be rewritten. For more information, see [Review and update scripts incompatible with guarded script](../task/review-incompatible-guarded-scripts.md) and the [Server-Side Sandbox Runtime Replacement \[KB2944435\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2944435) article on the Now Support Knowledge Base.

-   **[Review and update scripts incompatible with guarded script](../task/review-incompatible-guarded-scripts.md)**  
Review scripts that are incompatible with guarded script and either rewrite them to use supported features or create an exemption for scripts that can't be rewritten.
-   **[JavaScript APIs supported by guarded script](../reference/guarded-script-allowed-apis.md)**  
Review the JavaScript APIs that guarded script supports to help you analyze scripts in the Incompatible Guarded Scripts list and either rewrite them or create an exemption for them.

**Parent Topic:**[Script sandbox environment](script-sandbox-environment.md)

**Related topics**  


[Script sandbox evaluator](script-sandbox.md)

