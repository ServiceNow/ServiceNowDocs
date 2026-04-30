---
title: Upgrade the ServiceNow SDK
description: Upgrade to the latest version of the ServiceNow SDK for use with instances beginning with the Washington DC release.
locale: en-US
release: xanadu
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Upgrade the ServiceNow SDK

Upgrade to the latest version of the ServiceNow SDK for use with instances beginning with the Washington DC release.

## Before you begin

Your system must meet the following minimum requirements to use the latest version of the ServiceNow SDK:

-   Node.jsv20.18.0
-   npm v8.19.3

To install or upgrade Node.js or npm, see the [installation instructions](https://docs.npmjs.com/cli/v8/configuring-npm/install) on the npm website.

Role required: admin

## Procedure

1.  Complete the following steps depending on whether you're updating a global installation of the ServiceNow SDK or the version used by an application.

<table id="choicetable_q2z_4ms_mgc"><thead><tr><th align="left" id="d286149e86">

Option

</th><th align="left" id="d286149e89">

Steps

</th></tr></thead><tbody><tr><td id="d286149e95">

**Application package**

</td><td>

1.  Open the `package.json` file for your application.
2.  In the `devDependencies` object, update the versions of the `@servicenow/sdk` and `@servicenow/eslint-plugin-sdk-app-plugin` packages. For example:

    ```json
"devDependencies": {
        "@servicenow/sdk": "<version>",
        "@servicenow/glide": "26.0.1",
        "eslint": "8.50.0",
        "@servicenow/eslint-plugin-sdk-app-plugin": "<version>"
}
    ```

3.  Open a command-line tool on your system.
4.  Change directories into the directory for your application using the `cd` command:

    ```cmd
cd <path/to/directory>
    ```

5.  Enter the following command to verify the version of the ServiceNow SDK:

    ```cmd
now-sdk -v
    ```

</td></tr><tr><td id="d286149e146">

**Global package**

</td><td>

1.  Open a command-line tool on your system.
2.  Change directories into the directory for your application using the `cd` command:

    ```cmd
cd <path/to/directory>
    ```

3.  Enter the following command to upgrade to the latest version of the ServiceNow SDK:

    ```cmd
npm update -g @servicenow/sdk
    ```

4.  Enter the following command to verify the version of the ServiceNow SDK:

    ```cmd
now-sdk -v
    ```

</td></tr></tbody>
</table>
## What to do next

Install the ServiceNow Fluent Language server to get language processing and validation for ServiceNow Fluent in Visual Studio Code. For more information, see [Install the ServiceNow Fluent Language server in Visual Studio Code](install-fluent-language-extension-vs-code.md).

Use the ServiceNow SDK to authenticate to a ServiceNow instance. For more information, see [Authenticating to a ServiceNow instance with the ServiceNow SDK](../concept/authenticate-instance-now-sdk.md).

**Parent Topic:**[Configuring the ServiceNow SDK](../concept/configuring-servicenow-sdk.md)

**Related topics**  


[Install the ServiceNow SDK in an application](install-servicenow-sdk.md)

[Install the ServiceNow Fluent Language server in Visual Studio Code](install-fluent-language-extension-vs-code.md)

