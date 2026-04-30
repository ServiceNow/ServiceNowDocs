---
title: Test connectivity to the ServiceNow instance
description: Test the ServiceNow DEX instance network connectivity.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Getting started, Configure, Digital End-User Experience, IT Service Management]
---

# Test connectivity to the ServiceNow instance

Test the ServiceNow DEX instance network connectivity.

## Before you begin

-   On Windows, download the curl utility with the latest binaries to support mutual Transport Layer Security \(mTLS\) authentication.

    1.  From [https://curl.se/windows/](https://curl.se/windows/), download the latest curl zip file and extract it to your local drive.
    2.  Open a command prompt and set the path to the downloaded curl binary.

        For example, `SET PATH=C:\curl-8.12.1_1-win64-mingw\bin;%PATH%`.

    **Note:** The curl utility downloaded from the website doesn't replace the existing utility version on your local machine. The new version is applicable to the current CMD session only.

-   On macOS, use the curl utility version already installed.

Role required: agent\_client\_collector\_admin

## Procedure

1.  From the command line, download the `install_script.sh` by running one of the following curl commands:

    -   Without a proxy: `curl –verbose -L https://<servicenow instance>/api/sn_agent/agents/install_agent -o install_script.sh`
    -   With a proxy: `curl --verbose –-proxy <HOST_NAME>:<PORT> -L https://<servicenow instance>/api/sn_agent/agents/install_agent -o install_script.sh`
    The command downloads a script written into install\_script.sh.

2.  From the All menu, navigate to the Agent scripts table \(sn\_agent\_script\).

3.  Select the install\_script record and confirm that its content matches the content of the install\_script.sh file.


## Result

The match confirms that the connection is established with the ServiceNow® instance.

If there’s no match, fix your network connection issues.

