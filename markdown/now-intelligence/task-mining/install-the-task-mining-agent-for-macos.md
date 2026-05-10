---
title: Install the Task Mining agent for macOS
description: Install the Task Mining desktop agent on macOS workstations and deploy the Task Mining agent to managed macOS devices using JAMF. This procedure creates the package, scripts, policies, and configuration profile required for enterprise deployment.
locale: en-US
release: australia
product: Task Mining
classification: task-mining
topic_type: task
last_updated: "2026-04-27"
reading_time_minutes: 5
breadcrumb: [Install the Task Mining agent, Configure, Task Mining, Platform Analytics]
---

# Install the Task Mining agent for macOS

Install the Task Mining desktop agent on macOS workstations and deploy the Task Mining agent to managed macOS devices using JAMF. This procedure creates the package, scripts, policies, and configuration profile required for enterprise deployment.

## Before you begin

Role required: Task Mining Agent Install

**Note:** You must be a part of the Task Mining Agent Install group with roles itil, sn\_tm\_core.service\_user, and agent\_client\_collector\_admin to install the Task Mining agent. If the group doesn't exist, create a group with that name and those roles manually. For more information, see [Assign a role to a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_AssignRoleToGroup.md).

## About this task

The Task Mining agent for macOS is delivered as a `.pkg` archive. It can be installed using a one-line Terminal script, which handles the entire download and configuration automatically, or by downloading and configuring the installer package manually.

The JAMF deployment creates two scripts, two policies, and a configuration profile. The first script generates the JSON configuration file the installer needs. The second script checks whether the agent is installed and triggers a reinstall if not. The first policy combines the package and the configuration script and runs on a custom trigger. The second policy runs the provisioning script on a recurring schedule. The configuration profile grants the accessibility permissions the agent requires for data capture.

## Procedure

1.  Obtain the **Instance URL** and **Registration key**.

    The instance URL and registration key values are the same for Windows and macOS agents.

    1.  Navigate to **All** &gt; **Task Mining** &gt; **Agent Installation**.

    2.  Select an existing key or create one.

        ![Screenshot of registration key selection.](../image/tm-agent-3.png)

    3.  Copy the **Instance URL** and **Registration key** on the Agent Installation page.

    ![Screenshot of instance URL and registration key.](../image/tm-agent-4.png)

2.  Install the macOS agent by running the terminal script.

    1.  Select the **macOS** tab on the **Agent Installation** page.

    2.  Select **Copy** next to **Download and Install** to collect the one-line macOS command line script.

        ![Screenshot of macOS command line.](../image/tm-agent-2.png)

    3.  Open the macOS **Terminal** application.

    4.  Paste the script and press **Enter**.

    The script downloads the installer package, generates the required configuration file using your instance URL and registration key, and runs the installer automatically.

    **Note:** For a manual install, download the Intel &amp; Apple Silicon and JSON files. Place both files in the same folder. Do not rename the JSON file. Double-click \(or use the keyboard shortcut\) the .pkg file to launch the installer, and follow the on-screen instructions.

    ![Screenshot of JSON and Intel & Apple Silicon.](../image/tm-agent-1.png)

3.  Add the agent package to JAMF.

    1.  In JAMF Settings, search for **Packages**.

    2.  Select **New**.

    3.  Enter the package name, upload the agent `.pkg` archive, and save the package.

4.  Create the configuration script.

    1.  In JAMF Settings, search for **Scripts**.

    2.  Select **New**.

    3.  Name the script `Task Mining Script`.

    4.  Select the **Script** tab, choose the appropriate script type, and enter the following script:

        ```
        #!/bin/bash
        #set these variables in the param sections 4 and 5
        REGAPIURL=$4
        REGKEY=$5
        TARGET="/Library/Application Support/JAMF/Downloads/"
        JSON="tm-macos-agent_installer.json"
        
        if [[ -z "REGAPIURL" || -z "REGKEY" ]]; then
            echo "reg api url and reg key must be set as 4 and 5 arguments"
            exit 1
        fi
        
        cd "$TARGET" || {
            echo "failed to change dir"
            exit 2
        }
        
        cat <<EOF > "$JSON"
        {
            "agent": {
                "reg-api-url": "$REGAPIURL",
                "reg-key": "$REGKEY"
            }
        }
        EOF
        ```

    5.  Select **Save**.

5.  Create the provisioning script.

    1.  Select **New** to add another script.

    2.  Name the script `Task Mining Provisioning`.

    3.  Select the **Script** tab and enter the following script:

        ```
        #!/bin/bash
        APP_PATH="/Applications/Task Mining Agent.app"
        
        if [ ! -d "$APP_PATH" ]; then
            echo "taskmining is not installed -> triggering install via Jamf policy"
            if ! jamf policy -event taskmining_provisioning; then
                echo "error triggering jamf policy"
                exit
            fi
        else
            echo "taskmining app already installed"
        fi
        ```

    4.  Select **Save**.

6.  Create the installer policy.

    1.  In the JAMF **Computers** category, navigate to **Content Management** &gt; **Policies** and select **New**.

    2.  Name the policy `Task Mining Installer`.

    3.  Under **Trigger**, select **Custom** and enter `taskmining_provisioning` in the **Custom Event** field.

    4.  Set **Execution Frequency** to **Ongoing**.

    5.  Select **Save**.

    6.  Under the **Scope** tab, select **Add**, select the target computers or groups, and select **Done**.

    7.  In the sidebar, select **Options** &gt; **Packages** &gt; **Configure**.

    8.  Select **Add** next to the Task Mining Agent package.

    9.  In the sidebar, **Scripts** and **Configure**.

    10. Find **Task Mining Script** \(not Task Mining Provisioning\), and select **Add**.

    11. Under **Priority**, select **Before**.

    12. Paste the Instance URL into **Parameter 4** and the Registration key into **Parameter 5**.

    13. Select **Save**.

7.  Create the provisioning policy.

    1.  Navigate to **Content Management** &gt; **Policies** and select **New**.

    2.  Name the policy `Task Mining Provisioning`.

    3.  Under **Trigger**, select **Startup**, **Login**, and **Recurring Check-in**.

    4.  Set **Execution Frequency** to **Ongoing**.

    5.  In the **Scope** tab, add the same deployment targets as the installer policy.

    6.  In the sidebar, select **Scripts** and **Configure**.

    7.  Find **Task Mining Provisioning** \(not Task Mining Script\), and select **Add**.

        No parameters are needed.

    8.  Do not add any package to this policy.

    9.  Select **Save**.

8.  Create the configuration profile.

    1.  In the JAMF **Computers** category, navigate to **Content Management** &gt; **Configuration Profiles** and select **New**.

    2.  Name the profile `Task Mining`.

    3.  In the sidebar, select **Privacy Preferences Policy Control** and select **Configure**.

    4.  Enter the following values and select **Bundle ID** from the **Identifier Type** list:

        -   **Identifier**: `com.servicenow.taskmining.agent`
        -   **Code requirement**:

            ```
            identifier "com.servicenow.taskmining.agent" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = AS2BZHDV7Q
            ```

        **Note:** The code requirement is a static value. To obtain it, run the following Terminal command: `codesign -dr - ./Task\ Mining\ Agent.app`

    5.  Select **Add**.

    6.  Under **App or Service**, select **Accessibility**.

    7.  Under **Access**, select **Allow**.

    8.  Select **Save** for the accessibility permission, then select **Save** again at the bottom of the page for the entire profile.

9.  Mark the daemon as a managed login item.

    1.  In the configuration profile, select **Managed Login Items**.

    2.  Add a rule with the following values:

        -   **Rule Label**: `com.servicenowtaskmining.daemon`
        -   **Team Identifier**: `AS2BZHDV7Q`
        **Note:** The Team Identifier is the same value as the `subject.OU` in the code requirement from the previous step.

    3.  Select **Save**.


## What to do next

To debug policies on a macOS device, you can trigger them manually from Terminal. The policy identifier is the ID value in the JAMF URL when editing that policy.

```
sudo jamf policy -id *policy-id*
```

