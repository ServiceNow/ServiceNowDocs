---
title: Bulk deploy Agent Client Collector on macOS using Jamf
description: Use Jamf to install Agent Client Collector \(ACC\) on multiple macOS devices at once, promoting consistent deployment across your organization.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2025-08-25"
reading_time_minutes: 3
breadcrumb: [Getting started, Configure, Digital End-User Experience, IT Service Management]
---

# Bulk deploy Agent Client Collector on macOS using Jamf

Use Jamf to install Agent Client Collector \(ACC\) on multiple macOS devices at once, promoting consistent deployment across your organization.

## Before you begin

-   Create an agent registration key and retrieve its value to use in the procedure. For more information, see [Create an ACC registration key](../../product/digital-end-user-experience/task/setup-acc.md).
-   Install ACC on your local machine. For more information, see [Install ACC for DEX on macOS](../../product/digital-end-user-experience/task/install-acc-for-dex-macos.md).

Role required: agent\_client\_collector\_admin

## About this task

The following procedure describes how to mass-deploy ACC using Jamf. Your organization might have a different method to accomplish this task.

## Procedure

1.  Download the installation package.

    1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Deployment** &gt; **Agent Downloads**.

    2.  Download the appropriate package from the macOS Downloads section, based on the chip type.

2.  Upload the installation package to Jamf Pro.

    1.  In the Jamf Pro instance, navigate to **Settings** &gt; **Packages**.

    2.  Select the **New** button.

    3.  Provide a display name for a package.

    4.  Select **browse for a file** under **Filename** and select the package.

    5.  Select **Save**.

3.  Update the `acc.yml` file.

    1.  Copy the `acc.yml` file generated during the local installation to your Desktop location.

    2.  Confirm **connect-without-mid** is set to `true`.

    3.  Confirm that the instance URL is accurate and insert the registration key.

    4.  Verify that **verify-plugin-signature** is set to `false`.

    5.  Save the `acc.yml`

4.  Using the Terminal command line, convert your `acc.yml` file into a deploy package.

    1.  Create a file named `yml_package_builder.sh` on your Desktop.

    2.  Copy the following script into the `yml_package_builder.sh` file and save it.

        ```
        #!/bin/bash
        # === CONFIGURATION ===
        PKG_NAME="acc-yml.pkg"
        INSTALL_PATH="/Library/Application Support/servicenow/agent-clientcollector"
        YML_SOURCE_PATH="$HOME/Desktop/acc.yml" # Assuming you have your yml
        file on the Desktop folder, change it if needed
        # === CREATE BUILD STRUCTURE ===
        BUILD_DIR="$HOME/pkgbuild-yml"
        PAYLOAD_DIR="$BUILD_DIR/payload$INSTALL_PATH"
        # Clean previous build
        rm -rf "$BUILD_DIR"
        mkdir -p "$PAYLOAD_DIR"
        # Copy YAML file into package payload
        cp "$YML_SOURCE_PATH" "$PAYLOAD_DIR/"
        # === BUILD THE PACKAGE ===
        pkgbuild \
        --identifier "com.servicenow.acc.yml" \
        --install-location "$INSTALL_PATH" \
        --root "$BUILD_DIR/payload" \
        "$HOME/Desktop/$PKG_NAME"
        echo "✅ .pkg created at: $HOME/Desktop/$PKG_NAME"
        ```

    3.  Run the `sh yml_package_builder.sh` command from the Terminal.

        **Note:** The modified `acc.yml` file and the `yml_package_builder.sh` file must be saved in the same location \(Desktop, for example\).

    The file `acc-yml.pkg` appears on your Desktop.

5.  Upload the yml package to Jamf Pro in the same way you uploaded the installation package.

6.  In the Jamf Pro instance, create a post-install script.

    1.  Navigate to **Settings** &gt; **Scripts**.

    2.  Select the **New** button.

    3.  Provide a display name and complete the form as needed.

    4.  In the **Script** tab, paste the following script.

        ```
        # === 1. Create sudoers file ===
        SUDOERS_FILE="/private/etc/sudoers.d/_servicenow"
        cat <<EOF > "$SUDOERS_FILE"
        _servicenow ALL=NOPASSWD: SETENV: /Library/Application
        Support/servicenow/agent-client-collector/cache/osquery/bin/osqueryi *,
        /usr/bin/mdls, /usr/bin/log, /bin/kill, /bin/launchctl
        Defaults:_servicenow !requiretty
        EOF
        chmod 440 "$SUDOERS_FILE"
        echo "[INFO] Sudoers file created at $SUDOERS_FILE"
        # === 2. Set permissions for the YAML file ===
        YML_PATH="/Library/Application Support/servicenow/agent-clientcollector/
        acc.yml"
        if [ -f "$YML_PATH" ]; then
        chmod 644 "$YML_PATH"
        echo "[INFO] Permissions set on acc.yml"
        else
        echo "[WARN] acc.yml not found at $YML_PATH"
        fi
        # === 3. Restart ACC service ===
        PLIST="/Library/LaunchDaemons/com.sn.acc.plist"
        if [ -f "$PLIST" ]; then
        echo "[INFO] Stopping ACC service..."
        launchctl unload -w "$PLIST" 2>/dev/null
        sleep 2
        echo "[INFO] Starting ACC service..."
        launchctl load -w "$PLIST"
        else
        echo "[ERROR] LaunchDaemon not found at $PLIST"
        fi
        ```

    5.  Select **Save**.

7.  Create a Jamf policy and add the created packages and script.

    1.  In the Jamf Pro instance, navigate to **Inventory** &gt; **Policies**.

    2.  Select the **New** button.

    3.  Enter an appropriate policy name, trigger, and frequency.

    4.  Under **Scope**, add all the target computers.

    5.  Navigate to **Packages** &gt; **Configure** and add the installation and `acc-yml` packages to the record.

        **Note:** Make sure **Install** is selected under **Action**.

    6.  Navigate to **Scripts** &gt; **Configure** and add the post-install script to the record.

        **Note:** Make sure **After** is selected under **Priority**.

    7.  Select **Save**.

    8.  On the Scope tab, add target computers and target users.

    9.  Select **Save**.

8.  To monitor the deployment status, do one of the following:

    -   Check the deployment status in the Jamf Pro instance Dashboard.
    -   Check the agent status by navigating to **All** &gt; **Agent Client Collector** &gt; **Agents**.
    -   Review the log file on the endpoint devices: `/Library/Application Support/servicenow/agent-client-collector/log/acc.log`.

