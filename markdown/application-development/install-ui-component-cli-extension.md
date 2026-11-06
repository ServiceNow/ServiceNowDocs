---
title: Install the UI component CLI extension
description: Install the UI component extension to develop Next Experience UI Framework components with the ServiceNow CLI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/install-ui-component-cli-extension.html
release: australia
topic_type: task
last_updated: "2026-10-24"
reading_time_minutes: 1
breadcrumb: [Configure, UI component CLI extension, Building pro-code applications, Developing your application, Classic app development, Building applications]
---

# Install the UI component CLI extension

Install the UI component extension to develop Next Experience UI Framework components with the ServiceNow CLI.

## Before you begin

-   The ServiceNow CLI must be installed. See [Install the ServiceNow CLI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cli/download-cli.md). To confirm installation, run the following command:

    ```
    $ snc --help
    ```

-   Configure a default profile to enable the ServiceNow CLI to communicate with an instance. See [Create a default profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cli/create-default-profile.md).

Role required: admin

## About this task

The UI component CLI extension provides the commands for developing Next Experience UI Framework components. Commands that connect to a ServiceNow instance use the default ServiceNow CLI profile.

**Note:**

If you use ServiceNow CLI version 1.1.0, you must pass the connection details with each command instead of using a profile.

```
snc ui-component develop --loginHost <INSTANCE_URL> --username <USERNAME> --password <PASSWORD>
```

## Procedure

1.  Install the extension by running the following command:

    ```
    snc extension add --name ui-component
    ```

2.  View the commands that the extension supports by running the following command:

    ```
    snc ui-component --help
    ```

3.  Update the extension when a new version is available by running the following command:

    ```
    $ snc extension update --name ui-component
    ```

4.  Remove the extension by running the following command:

    ```
    $ snc extension remove --name ui-component
    ```


