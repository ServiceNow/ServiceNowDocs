---
title: Configure ServiceNow sudoers file
description: Configure the ServiceNow sudoers file to grant the servicenow user the necessary permissions to run specific commands with elevated privileges. This configuration uses a drop-in file in /etc/sudoers.d/ to maintain secure, isolated sudo rules for ServiceNow operations.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Installing DEX on your local machine, Configure, Digital End-User Experience, IT Service Management]
---

# Configure ServiceNow sudoers file

Configure the ServiceNow sudoers file to grant the servicenow user the necessary permissions to run specific commands with elevated privileges. This configuration uses a drop-in file in /etc/sudoers.d/ to maintain secure, isolated sudo rules for ServiceNow operations.

## Before you begin

Role required: admin

## Procedure

1.  Open Terminal with Root Access by running `sudo -i`.

2.  Create and edit the drop-in sudoers file by running `visudo -f /etc/sudoers.d/_servicenow`.

3.  Paste the following content into the editor:

    ```
    # ServiceNow Agent Collector - Sudoers Configuration for macOS
    
    # Command alias for ServiceNow allowed commands
    # These commands can be executed by the _servicenow user with sudo privileges
    Cmnd_Alias SN_ALLOWED = /usr/bin/powermetrics, \
                            /usr/bin/mdls, \
                            /usr/bin/log, \
                            /usr/bin/log show *, \
                            /bin/kill, \
                            /usr/bin/defaults, \
                            /usr/local/bin/jamf, \
                            /bin/rm, \
                            /bin/ls, \
                            /usr/bin/pgrep, \
                            /usr/bin/find, \
                            /usr/bin/pmset, \
                            /usr/bin/open, \
                            /Library/Application\ Support/servicenow/agent-client-collector/cache/acc-dex-modules/bin/scripts/sudo/app_freeze.sh, \
                            /Library/Application\ Support/servicenow/agent-client-collector/cache/acc-dex-modules/bin/scripts/sudo/zscaler_zpa_reconnect.sh, \
                            /Library/Application\ Support/servicenow/agent-client-collector/cache/acc-dex-modules/bin/scripts/sudo/clear_google_chrome_browsing_data.sh, \
                            /Library/Application\ Support/servicenow/agent-client-collector/cache/acc-dex-modules/bin/scripts/sudo/services.sh, \
                            /Library/Application\ Support/servicenow/agent-client-collector/cache/acc-dex-modules/bin/scripts/sudo/restart_service.sh *, \
                            /Applications/Zscaler/Zscaler.app/Contents/PlugIns/zscli, \
                            /Library/Application\ Support/servicenow/agent-client-collector/cache/acc-dex-modules/bin/scripts/sudo/elevate_temporary_admin.sh
    
    # ServiceNow user permissions
    # _servicenow user can run osqueryi and all SN_ALLOWED commands without password
    # SETENV allows environment variables to be preserved
    _servicenow ALL=NOPASSWD: SETENV: /Library/Application\ Support/servicenow/agent-client-collector/cache/osquery/bin/osqueryi *, SN_ALLOWED
    
    # Defaults for _servicenow user
    # !requiretty: Allow sudo without a TTY (required for automated scripts)
    Defaults:_servicenow !requiretty
    ```

4.  Save and exit.

5.  Validate the file syntax by running `visudo -c -f /etc/sudoers.d/_servicenow`.

    Expected output: `/etc/sudoers.d/_servicenow: parsed OK`.

6.  Set the file permissions:

    -   chown root:wheel /etc/sudoers.d/\_servicenow
    -   chmod 440 /etc/sudoers.d/\_servicenow
7.  Confirm the drop-in directory is included in the sudoers file by running `grep -i includedir /etc/sudoers`.

    Expected output: `#includedir /etc/sudoers.d`.

8.  Test permissions for the servicenow user by running `sudo -u _servicenow sudo -l`.

    List all allowed commands confirming the rules are active.


**Parent Topic:**[Installing DEX on your local machine](../concept/installing-dex-local.md)

