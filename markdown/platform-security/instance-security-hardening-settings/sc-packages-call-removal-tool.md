---
title: Packages call removal tool
description: Activate and run the Packages Call Removal Tool \(com.glide.script.packages\_call\_removal\) plugin, and then consider whether each of the proposed changes should be completed or rejected.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Restrict allowed Java packages \[Updated in Security Center 1.3\], Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Packages call removal tool

Activate and run the Packages Call Removal Tool \(**com.glide.script.packages\_call\_removal**\) plugin, and then consider whether each of the proposed changes should be completed or rejected.

The Packages Call Removal Tool is a plugin that:

-   Scans scripts for package calls to ServiceNow AI Platform Java classes.
-   Proposes changes to replace them with preferred GlideScriptable names.
-   Facilitates the script changes.

**Note:** If this record is a base system record, using the recommendation from the tool causes the item to be marked as customer\_update. However, it may still be useful to use this tool because it flags Packages,xxx calls.

The Packages Call Removal Tool might report some package calls used in `sa_mapping_ext_commands` and `sa_custom_operation`. These package calls belong to the MID Server. As there are no classes, the code runs in MID Server. If you find any of the following listed package calls in the Errors section, mark them as Rejected \(Ignored\). The tool doesn't report that package call again.

-   `Packages.com.snc.sw.util.JSONUtil.toJSONPlain(file_content);`
-   `Packages.com.snc.sw.util.JSONUtil.toJSONPlain(file_name);`
-   `Packages.com.snc.sw.commands.HttpCallHandler;`
-   `Packages.com.snc.sw.dto.ProviderType.SSH`

## More information

|Attribute|Description|
|---------|-----------|
|Plugin Name|com.glide.script.packages\_call\_removal|
|Configuration type|System Definition &gt; Plugins|
|Purpose|To remove/replace unauthorized package/member calls with Glide Acceptable \(GlideScriptable\) names that only allow authorized access to data.|
|Recommended value|Active|
|Functional impact|This remediation would replace the package calls with GlideScriptable APIs, and can affect the customizations that include package calls. The tool doesn’t actually replace package calls automatically. Instead, it provides suggestions that are stored into the packages\_call\_item table. Your administrator can then decide whether to accept or reject the proposed change.|
|Security risk|\(Medium\) Client-side API calls that result in data retrieval or object access on server are deemed to be dangerous from a security standpoint. They should be validated for authorization and restriction for sensitive object access.|

## Steps to configure

1.  Navigate to **System Definition** &gt; **Plugins**

    ![Packages call removal tool 1](../../security/image/packages-call-removal-tool1.png)

2.  Search for the plugin ID = **com.glide.script.packages\_call\_removal**.

    ![Packages call removal tool 2](../../security/image/packages-call-removal-tool2.png)

3.  Click **Activate/Upgrade** to activate the plugin.

    ![Packages call removal tool 3](../../security/image/packages-call-removal-tool3.png)

4.  To check inclusion list package calls and inclusion list member calls, complete the actions outlined in the Steps to Configure sections in [Restrict allowed Java packages \[Updated in Security Center 1.3\]](sc-java-packages-allowlist.md).

**Parent Topic:**[Restrict allowed Java packages \[Updated in Security Center 1.3\]](sc-java-packages-allowlist.md)

