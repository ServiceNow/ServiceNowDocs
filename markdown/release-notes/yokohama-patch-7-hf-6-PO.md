---
title: Yokohama Patch 7 Hotfix 6
description: The Yokohama Patch 7 Hotfix 6 release contains fixes to these problems.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-12-05"
reading_time_minutes: 1
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 7 Hotfix 6

The Yokohama Patch 7 Hotfix 6 release contains fixes to these problems.

-   **Build information:**

    Build date: 12-01-2025\_2305

    Build tag: glide-yokohama-12-18-2024\_\_patch7-hotfix6-11-30-2025


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

## Fixed problem

<table id="all-other-fixes"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Authentication

 PRB1947882

</td><td>

After upgrading within Yokohama, the email MFA option is missing and only Authenticator App \(TOTP\) is shown

</td><td>

After upgrading, users are no longer able to see the email multi-factor authentication option during login. Only the Authenticator App \(TOTP\) is displayed, even after selecting 'Try another way to verify.'

</td><td>

1.  Make sure both email and the Authenticator App \(TOTP\) are configured.
2.  Log in.
3.  Notice that only TOTP appears as a multi-factor authentication option.
4.  Select **Try another way to verify**.

 Observe that only TOTP appears. The email option is still missing.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 7 Hotfix 5](https://downloads.docs.servicenow.com/enus/yokohama/rn/hotfix/yokohama-patch-7-hf-5.pdf)
-   [Yokohama Patch 6](yokohama-patch-6.md)
-   [Yokohama Patch 5](yokohama-patch-5.md)
-   [Yokohama Patch 4](yokohama-patch-4.md)
-   [Yokohama Patch 3](yokohama-patch-3.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

