---
title: Install the ServiceNow SDK in an application
description: Install the ServiceNow software development kit \(SDK\) in a local application using Node Package Manager \(npm\).
locale: en-US
release: zurich
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Install the ServiceNow SDK in an application

Install the ServiceNow software development kit \(SDK\) in a local application using Node Package Manager \(npm\).

## Before you begin

Your system must meet the following minimum requirements to use the latest version of the ServiceNow SDK:

-   Node.jsv20.18.0
-   npm v8.19.3

To install or upgrade Node.js or npm, see the [installation instructions](https://docs.npmjs.com/cli/v8/configuring-npm/install) on the npm website.

Role required: admin

## About this task

The ServiceNow SDK is available as an npm package from the [public npm registry](https://www.npmjs.com/package/@servicenow/sdk). The ServiceNow SDK supports integrating with ServiceNow instances beginning with the Washington DC release.

In the following procedure, you install the ServiceNow SDK within a new application using `npx` rather than globally. To install the ServiceNow SDK globally, use the `npm install --global @servicenow/sdk` command.

**Note:** If you use `npx` to install the ServiceNow SDK in application rather than globally, you must use `npx @servicenow/sdk [command]` rather than `now-sdk [command]` with the ServiceNow SDK CLI.

## Procedure

1.  Open a command-line tool on your system.

2.  Verify that your system meets the requirements.

    1.  Enter `node -v​` to check if you have Node.js installed and which version.

    2.  Enter `npm -v` to check if you have npm installed and which version.

3.  Create a local directory for your application.

4.  Change directories into the directory for your application using the `cd` command.

    ```cmd
    cd <path/to/directory>
    ```

5.  Create an application with the ServiceNow SDK.

<table id="choicetable_bpj_k5p_s2c"><thead><tr><th align="left" id="d221675e200">

State

</th><th align="left" id="d221675e203">

Steps

</th></tr></thead><tbody><tr><td id="d221675e209">

**Authentication hasn't been configured**

</td><td>

If you haven't added authentication credentials and an alias on your system yet, install the ServiceNow SDK with the `auth` command before creating an application with the `init` command. For example:

```cmd
npx @servicenow/sdk auth --add <instance>
```

 For more information, see [Authenticating to a ServiceNow instance with the ServiceNow SDK](../concept/authenticate-instance-now-sdk.md).

</td></tr><tr><td id="d221675e248">

**Authentication has been configured**

</td><td>

If you have added authentication credentials, install the ServiceNow SDK in new applications with the `init` command. For example:

```cmd
npx @servicenow/sdk init
```

 For more information, see [Create an application with the ServiceNow SDK](create-application-now-sdk.md) or [Convert an application with the ServiceNow SDK](convert-application-now-sdk.md).

</td></tr></tbody>
</table>
## What to do next

Install the ServiceNow Fluent Language server to get language processing and validation for ServiceNow Fluent in Visual Studio Code. For more information, see [Install the ServiceNow Fluent Language server in Visual Studio Code](install-fluent-language-extension-vs-code.md).

**Parent Topic:**[Configuring the ServiceNow SDK](../concept/configuring-servicenow-sdk.md)

**Related topics**  


[Upgrade the ServiceNow SDK](upgrade-servicenow-sdk.md)

[Install the ServiceNow Fluent Language server in Visual Studio Code](install-fluent-language-extension-vs-code.md)

