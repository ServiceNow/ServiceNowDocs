---
title: Upgrade the Discovery Console for OT
description: These are the instructions for upgrading the Discovery Console for OT. The scope of this document does not include how to upgrade the containerized version of the Console.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/upgrade-discovery-console.html
release: australia
topic_type: task
last_updated: "2026-06-17"
reading_time_minutes: 2
breadcrumb: [Discovery Console for OT, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Upgrade the Discovery Console for OT

These are the instructions for upgrading the Discovery Console for OT. The scope of this document does not include how to upgrade the containerized version of the Console.

## Before you begin

You must have the latest version of the Console already been installed on one of the supported Linux distributions.

**Note:** After the March 2026 GA release of the Console, the version of the .Net runtime has been changed from 8.x to 10.x since the 8.x version has an End of Support date of November 10, 2026.

The Console packages now require .Net 10.x. The console-upgrade.sh script included with `consoleinstaller` builds of 20260527.3 or later attempts to install this dependency before making any other changes to the system. This requires internet connectivity for the upgrade installation. If the script determines .Net 10 is not present on the system and is unable to install it, it exits before attempting to upgrade to the new set of Console packages.

Also, Rabbit 4.3 was released after the GA release. This script does not attempt to make any changes to accommodate a newer Rabbit version, because:

-   the system is still running the version installed at the time of the original Console installation, **OR**,
-   if Rabbit was upgraded after that, this was intentionally done by the end user, and this end user has already updated the Rabbit version.

Role required: admin

## Procedure

1.  Transfer the new `consoleinstaller` package over to the system hosting the Console.

2.  Unzip the package by typing `unzip [name of console installer package]`.

    **Note:** If you run this command in a directory where there is already a ConsoleInstaller folder present, you're prompted with: `replace ConsoleInstaller/docs/codeowners.md? [y]es, [n]o, [A]ll, [N]o, [r]ename:` Type A followed by Enter/Return to continue unzipping the files.

3.  Change directory to the ConsoleInstaller folder by typing `cd ConsoleInstaller`.

4.  Type `chmod +x console-upgrade.sh` to make sure the upgrade script is set to be executable.

5.  The Console upgrade script needs to run with root privileges.

    Include desired level of detail for using either `su` or `sudo` to do that.

6.  Run the upgrade script by typing the following command: `/bin/bash console-upgrade.sh`.

    Depending on the current state of the system, you may be prompted with a few questions to complete the upgrade process. The console upgrade script can run the latest migration scripts automatically with no user input needed. This requires Console installer program version 20260601.8 or later for `devslim`.


**Parent Topic:**[Discovery Console for Operational Technology \(OT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/ot-discovery-console-landing.md)

