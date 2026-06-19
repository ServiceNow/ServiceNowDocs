---
title: Troubleshooting and accessing logs
description: Access various logs to troubleshoot and identify the failure reasons.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/servicenow-ai-platform-security/cs-logs.html
release: zurich
product: ServiceNow AI Platform Security
classification: servicenow-ai-platform-security
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administer and Troubleshoot, Code Signing, Platform Security]
---

# Troubleshooting and accessing logs

Access various logs to troubleshoot and identify the failure reasons.

## Code Signing logs

If any of the ECC queue records is not signed by the Code Signing Tracker API, the unsigned messages and the required details are displayed in the Code Signing module. Navigate to **System Logs** &gt; **System Log** &gt; **Code Signing** to access the list of records that are not trusted.

For additional debug node logs, enable **com.glide.codesigning.tracking.debug** and set its value to `true`.

## REST message signature validation failure on MID Server

Access the error message regarding to the signature validation failure, by navigating to **System Web Services** &gt; **Outbound** &gt; **REST Message** and opening the required REST message record.

\[Omitted image "CS-REST-logs.png"\] Alt text: REST message signature validation failure.

**Note:** Error messages related to the ECC firewall rejections start with `ECC message execution denied`.

\[Omitted image "CS-ECC.png"\] Alt text: ECC queue input when signature validation fails.

\[Omitted image "CS-ECC2.png"\] Alt text: Error message when the ECC message is blocked.

## JDBC probe

When a JDBC data source with an invalid or missing signature is executed on a MID Server, an error message with the required details is displayed.

\[Omitted image "CS-JDBC.png"\] Alt text: JDBC probe error message.

**Source** also displays the details of the error message.

\[Omitted image "CS-JDBC2.png"\] Alt text: Error details in Source.

## MID Server logs

To enable the detailed ECC firewall logging, increase the log level by setting the value of the MID Server configuration parameter, **mid.log.level**, to `TRACE`. The detailed logs provide information about:

-   Rules that the MID Server loaded from the boot configuration file.
-   Granular execution trace of rules.
-   Specific rule due to which an ECC message is to be accepted or rejected.

**Note:** If `boot-config.xml` is invalid, the MID Server fails to start and the failure details are logged in the MID agent logs.

