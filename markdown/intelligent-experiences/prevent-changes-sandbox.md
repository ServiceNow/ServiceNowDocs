---
title: Prevent changes to sandbox files
description: Add a filesystem deny rule to your sandbox policy so that agent actions can't modify files in the sandbox runtime directory on user devices.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/prevent-changes-sandbox.html
release: brazil
topic_type: task
last_updated: "2026-09-29"
reading_time_minutes: 2
keywords: [sandbox rules, sandbox runtime directory, filesystem deny rule, known issue]
breadcrumb: [Reference, ServiceNow Cowork, Extending AI with external systems and providers, Enable AI Experiences]
---

# Prevent changes to sandbox files

Add a filesystem deny rule to your sandbox policy so that agent actions can't modify files in the sandbox runtime directory on user devices.

## Before you begin

Role required: sn\_app\_cowork.admin

## About this task

Cowork runs agent commands in an isolated sandbox. The sandbox reaches permitted files on the device through an authenticated file bridge, which is how tasks such as reading and saving documents work.

In affected releases, the file bridge doesn't prevent writes to the sandbox runtime directory. Cowork launches sandbox components from this directory when it creates a sandbox, so a replaced file there can run on the device with the privileges of the user running Cowork, outside the sandbox restrictions. The deny rule blocks these writes until you deploy a release that contains the permanent fix.

## Procedure

1.  Navigate to **All** &gt; **ServiceNow Cowork** &gt; **Policies** &gt; **Cowork Agent Policy**.

2.  Open the policy assigned to your affected Cowork users.

3.  Select the **Policy Sandbox Rules** tab, and then select **New**.

4.  In the **Sandbox Rule** field, select a sandbox rule.

5.  In the **Domain** field, select the domain.

6.  Select **Submit**.

7.  In the **Policy Sandbox Rules** tab, select the rule you created.

8.  Configure the rule.

    1.  From the **Rule type** list, select **filesystem**.

    2.  From the **Access mode** list, select **deny**.

    3.  In the **Path** field, enter `.local/share/openshell/vm-runtime`.

        Enter the path exactly as shown. The path is relative to the user's home directory. Don't add `~/`, environment variables, or wildcard characters. Apply the rule to the directory itself, not to a version folder or a file, because each new version creates its own subfolder.

9.  Select **Update**.

10. Sync the policy to your Cowork clients.

11. Verify the rule.

    1.  Confirm the rule is active and linked to the correct policy.

    2.  Confirm each affected client received the rule.

    3.  In a test environment, confirm that writes to the protected directory are denied.

    4.  Confirm that normal file tasks outside that directory still work.

    A device is protected only after it receives and applies the policy. If verification fails, resolve the policy or sync issue before you treat the device as protected.

    **Important:** Don't test the rule by overwriting, renaming, deleting, or running a real sandbox runtime file, because this can break the sandbox on that device. Use a separate test file in a test environment.

    If your deployment uses a custom sandbox runtime location, add a separate deny rule for that location. Contact ServiceNow Support to confirm the path.


## Result

Agent actions can't write to the sandbox runtime directory. Typical tasks are unaffected: users can open permitted documents, process them in the sandbox, and save results to permitted locations. Before wide deployment, validate your business critical workflows and any custom skills in a test environment.

**Note:**

The rule protects the configured path for operations that the sandbox policy controls. It doesn't cover:

-   Custom runtime locations, unless you add rules for them
-   Other processes that run on the device under the same user account
-   Runtime files that were modified before you applied the rule

Approval prompts add oversight but don't replace this rule.

## What to do next

Keep the rule in place until a release that contains the permanent fix is deployed to all affected devices and you verify protection on them. Remove the rule only through your normal change approval process.

If you suspect a runtime file on a device was already modified, follow your organization's security incident process and reinstall Cowork from a trusted source on that device.

**Parent Topic:**[ServiceNow Cowork reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/servicenow-cowork-reference.md)

