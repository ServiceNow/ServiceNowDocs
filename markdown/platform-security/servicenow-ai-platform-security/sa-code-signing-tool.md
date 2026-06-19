---
title: Standalone signing tool
description: Use the standalone Signing Tool to sign supported records in ServiceNow applications using your own private key.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/servicenow-ai-platform-security/sa-code-signing-tool.html
release: zurich
product: ServiceNow AI Platform Security
classification: servicenow-ai-platform-security
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Code Signing, Code Signing, Platform Security]
---

# Standalone signing tool

Use the standalone Signing Tool to sign supported records in ServiceNow applications using your own private key.

Use the Signing Tool to sign records in ServiceNow apps. The tool generates signatures for records in your local environment using your own private key.

## Signing tool workflow

\[Omitted image "code-signing-tool.png"\] Alt text: Signing tool workflow

1.  Create or select an existing ServiceNow application with records to be signed, such as business rules or script includes.
2.  Push the application into your Git repository, which resides in your environment.

    **Note:** Applications can be synced between a Git repository and your instance using the Source Control Integration. For details on configuring and using this integration, see .

3.  Clone the application in your local environment.
4.  Use the Signing Tool \(also in your local environment\) to sign the supported records from the cloned ServiceNow application using your private key. The Signing Tool creates signature records and X.509 Certificate \[sys\_certificate\] records. For details on using the Signing Tool, see [Using the Signing Tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/servicenow-ai-platform-security/use-sa-signing-tool.md).
5.  Push the updated application to your Git repository.
6.  In your instance, import the updated application by applying remote changes.

-   **[Using the Signing Tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/servicenow-ai-platform-security/use-sa-signing-tool.md)**  
Learn how to use the Signing Tool to sign supported records in ServiceNow applications.
-   **[Signing Tool arguments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/servicenow-ai-platform-security/sa-signing-tool-reference.md)**  
Learn about the available arguments for the Signing Tool.

**Parent Topic:**[Using Code Signing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/servicenow-ai-platform-security/using-code-signing.md)

