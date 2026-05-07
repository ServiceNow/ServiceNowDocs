---
title: Copy HCLS Script Includes to Global Scope
description: Copy the MultiSSO\_OIDC\_CTO and OAuthUtilEpic script includes to the global scope so they are available for later configuration steps.
locale: en-US
release: australia
product: Healthcare Operations Core
classification: healthcare-operations-core
topic_type: task
last_updated: "2026-04-30"
reading_time_minutes: 1
breadcrumb: [Embed Care Team Portal in Epic, Configure, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Copy HCLS Script Includes to Global Scope

Copy the MultiSSO\_OIDC\_CTO and OAuthUtilEpic script includes to the global scope so they are available for later configuration steps.

## Before you begin

Role required: admin

## Procedure

1.  Set the application scope to Global.

2.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

3.  In the Name field, search for **MultiSSO\_OIDC\_CTO**.

4.  In the results list, confirm that the Application column shows Healthcare and Life Sciences Service Management Core, then open the record.

5.  Right-click the form toolbar and select **Insert and Stay**.

6.  Confirm that the Application field now shows **Global**.

7.  In the Name field, change the value to **MultiSSO\_OIDC\_CTO\_global**.

8.  Select **Update**.

9.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

10. In the Name field, search for **OAuthUtilEpic**.

11. In the results list, confirm that the Application column shows **Healthcare and Life Sciences Service Management Core**, then open the record.

12. Right-click the form toolbar and select **Insert and Stay**.

13. Confirm that the Application field now shows **Global**.

14. In the Name field, change the value to **OAuthUtilEpic\_global**.

15. Select **Update**.


## Result

The MultiSSO\_OIDC\_CTO\_global and OAuthUtilEpic\_global script includes are now available in the global scope for later configuration steps.

