---
title: GitHub pipeline actions
description: Use these actions in your GitHub pipeline to interact with the DevOps Config data model.
locale: en-US
release: zurich
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Integrate, DevOps Config, IT Service Management]
---

# GitHub pipeline actions

Use these actions in your GitHub pipeline to interact with the DevOps Config data model.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

GitHub scripted and declarative pipelines are supported.

The ServiceNow DevOps Config Validate \(servicenow-devops-config-validate\) and DevOps Config Export \(servicenow-devops-config-export\) GitHub Actions are provided to create a specific pipeline definition.

## DevOps Config Validate \(servicenow-devops-config-validate\)

Upload and validate configuration data in a ServiceNow instance.

-   **Input arguments**

<table id="table_k3q_bf4_tzb"><thead><tr><th>

Argument

</th><th>

Description

</th></tr></thead><tbody><tr><td>

instance-url

</td><td>

ServiceNow instance URL.

</td></tr><tr><td>

devops-integration-username

</td><td>

DevOps Config integration username.

</td></tr><tr><td>

devops-integration-user-password

</td><td>

DevOps Config integration user password.

</td></tr><tr><td>

application-name

</td><td>

DevOps Config application name.

</td></tr><tr><td>

target

</td><td>

Data model target where configuration files are uploaded. Example data model targets are:

-   `component`
-   `collection`
-   `deployable`


</td></tr><tr><td>

deployable-name

</td><td>

Deployable name in the DevOps Config data model.

</td></tr><tr><td>

collection-name

</td><td>

\(Optional\) Collection name in the data model. Required when target is collection.

</td></tr><tr><td>

name-path

</td><td>

\(Optional\) Name path of the node in the data model where the configuration files are uploaded.

</td></tr><tr><td>

config-file-path

</td><td>

File path when uploading a single file or file path pattern based on the Ant-style pattern when uploading multiple files to the data model. See [Directory-based Tasks](https://ant.apache.org/manual/dirtasks.html) for information on Ant-style patterns in the Apache Ant.1.10.14 Manual documentation.

</td></tr><tr><td>

data-format

</td><td>

Data format of the configuration files. Example data formats are:

-   `CSV`
-   `INI`
-   `JSON`
-   `Properties`
-   `RAW`
-   `XML`
-   `YAML`


</td></tr><tr><td>

data-format-attribute

</td><td>

\(Optional\) Extended data format attributes for parsing configuration data.

</td></tr><tr><td>

auto-commit

</td><td>

Boolean \(true or false\) input to commit configuration data after successful upload.Default value: `true`

</td></tr><tr><td>

auto-validate

</td><td>

Boolean \(true or false\) input to validate configuration data after successful commit.Default value: `true`

</td></tr><tr><td>

auto-publish

</td><td>

Boolean \(true or false\) input to publish configuration data after successful validation.Default value: `true`

</td></tr><tr><td>

changeset

</td><td>

\(Optional\) Open changeset associated with the upload action. If not provided, a new changeset is created.

</td></tr><tr><td>

snapshot-validation-timeout

</td><td>

\(Optional\) Maximum time in minutes for validation to complete before failing the action.Default value: `60`

</td></tr><tr><td>

terminate-on-policy-validation-failures

</td><td>

\(Optional\) Boolean \(true or false\) input to terminate the GitHub workflow after policy validation failures.Default value: `false`

</td></tr></tbody>
</table>-   **Outputs**
    -   **changeset-number**

        Changeset number associated with the upload action.

    -   **snapshot-name**

        Name of the latest snapshot of the deployable.

    -   **validation-status**

        Validation status of the snapshot. Example: `passed`, `passed_with_exception`, `failed`, `execution_error`, `not_validated`

    -   **validation-results**

        Validation results in the JSON format for the snapshot.

-   **Example — Uploading config files to a deployable**

    ```
    upload_and_validate_job:
        name: Upload and validate
        needs: <upstream job>
        runs-on: ubuntu-latest
        steps:     
          - name: ServiceNow Devops Config Validate
            uses: ServiceNow/servicenow-devops-config-validate@v1.0.0-beta
            with:
              instance-url: ${{ secrets.SN_INSTANCE_URL }}
              devops-integration-username: ${{ secrets.SN_DEVOPS_CONFIG_USERNAME }}
              devops-integration-user-password: ${{ secrets.SN_DEVOPS_CONFIG_PASSWORD }}
              application-name: PaymentDemo
              target: deployable
              deployable-name: Production
              name-path: web-api-v1.0
              auto-commit: true
              auto-validate: true
              auto-publish: true
              config-file-path: data/k8s/helm/*.yml
              data-format: yaml
              snapshot-validation-timeout: 60
              terminate-on-policy-validation-failures: true
    ```

-   **Example — Uploading config files to a collection**

    ```
    upload_and_validate_job:
        name: Upload and validate
        needs: <upstream job>
        runs-on: ubuntu-latest
        steps:     
          - name: ServiceNow Devops Config Validate
            uses: ServiceNow/servicenow-devops-config-validate@v1.0.0-beta
            with:
              instance-url: ${{ secrets.SN_INSTANCE_URL }}
              devops-integration-username: ${{ secrets.SN_DEVOPS_CONFIG_USERNAME }}
              devops-integration-user-password: ${{ secrets.SN_DEVOPS_CONFIG_PASSWORD }}
              application-name: PaymentDemo
              target: collection
              deployable-name: Production
              collection-name: release-1.0
              name-path: web-api-v1.0
              auto-commit: true
              auto-validate: true
              auto-publish: true
              config-file-path: data/k8s/helm/*.yml
              data-format: yaml
              snapshot-validation-timeout: 60
              terminate-on-policy-validation-failures: true
    ```

-   **Example — Uploading config files to a component**

    ```
    upload_and_validate_job:
        name: Upload and validate
        needs: <upstream job>
        runs-on: ubuntu-latest
        steps:     
          - name: ServiceNow Devops Config Validate
            uses: ServiceNow/servicenow-devops-config-validate@v1.0.0-beta
            with:
              instance-url: ${{ secrets.SN_INSTANCE_URL }}
              devops-integration-username: ${{ secrets.SN_DEVOPS_CONFIG_USERNAME }}
              devops-integration-user-password: ${{ secrets.SN_DEVOPS_CONFIG_PASSWORD }}
              application-name: PaymentDemo
              target: component
              deployable-name: Production
              name-path: web-api-v1.0
              auto-commit: true
              auto-validate: true
              auto-publish: true
              config-file-path: data/k8s/helm/*.yml
              data-format: yaml
              snapshot-validation-timeout: 60
              terminate-on-policy-validation-failures: true
    ```

-   **Example — Uploading multiple config files in a single commit**

    ```
    upload_and_validate_job:
        name: Upload and validate
        
        needs: <upstream job>
        runs-on: ubuntu-latest
        # Upload an XML file to a component
        steps:     
          - name: ServiceNow Devops Config Validate
            id: upload_and_validate_xml
            uses: ServiceNow/servicenow-devops-config-validate@v1.0.0-beta
            with:
              instance-url: ${{ secrets.SN_INSTANCE_URL }}
              devops-integration-username: ${{ secrets.SN_DEVOPS_CONFIG_USERNAME }}
              devops-integration-user-password: ${{ secrets.SN_DEVOPS_CONFIG_PASSWORD }}
              application-name: PaymentDemo
              target: component
              deployable-name: Production
              name-path: web-api-v1.0
              auto-commit: false
              auto-validate: true
              auto-publish: true
              config-file-path: data/infra/v1/*.xml
              data-format: xml
              snapshot-validation-timeout: 60
              terminate-on-policy-validation-failures: true
    
        # Upload a JSON file to the vars folder of a deployable
        steps:     
          - name: ServiceNow Devops Config Validate
            id: upload_and_validate_json
            uses: ServiceNow/servicenow-devops-config-validate@v1.0.0-beta
            with:
              instance-url: ${{ secrets.SN_INSTANCE_URL }}
              devops-integration-username: ${{ secrets.SN_DEVOPS_CONFIG_USERNAME }}
              devops-integration-user-password: ${{ secrets.SN_DEVOPS_CONFIG_PASSWORD }}
              application-name: PaymentDemo
              target: component
              deployable-name: Production
              name-path: web-api-v1.0
              auto-commit: true
              auto-validate: true
              auto-publish: true
              config-file-path: data/infra/prod/*.json
              data-format: json
              snapshot-validation-timeout: 60
              terminate-on-policy-validation-failures: true
              changeset : ${{ steps.upload_and_validate_xml.outputs.changeset-number }}
    ```


## DevOps Config Export \(servicenow-devops-config-export\)

Export configuration data using ServiceNow DevOps Config.

-   **Input arguments**

<table id="table_znh_3nq_11c"><thead><tr><th>

Argument

</th><th>

Description

</th></tr></thead><tbody><tr><td>

instance-url

</td><td>

ServiceNow instance URL.

</td></tr><tr><td>

devops-integration-username

</td><td>

DevOps Config integration username.

</td></tr><tr><td>

devops-integration-user-password

</td><td>

DevOps Config integration user password.

</td></tr><tr><td>

application-name

</td><td>

DevOps Config application name.

</td></tr><tr><td>

deployable-name

</td><td>

Deployable name in the DevOps Config data model.

</td></tr><tr><td>

exporter-name

</td><td>

Exporter name that exports configuration data from the DevOps Config data model.

</td></tr><tr><td>

snapshot-name

</td><td>

\(Optional\) Snapshot from which to export data. If a snapshot is not specified, the latest snapshot for the deployable is used.

</td></tr><tr><td>

exporter-data-format

</td><td>

\(Optional\) Format to export the snapshot data. Example data formats are:

-   `CSV`
-   `INI`
-   `JSON`
-   `Properties`
-   `RAW`
-   `XML`
-   `YAML`


</td></tr><tr><td>

exporter-arguments

</td><td>

\(Optional\) Arguments to be used along with the exporter. The value must be a JSON object represented as a string.

</td></tr></tbody>
</table>-   **Output**
    -   **exporter-content**

        Configuration data that the exporter exports.

-   **Example — Export specific snapshot**

    ```
    export:
        name: Export config
        needs: <upstream job>
        runs-on: ubuntu-latest
        steps:
        - name: ServiceNow DevOps Config Export
          uses: ServiceNow/servicenow-devops-config-export@v1.0.0-beta
          with:
            instance-url: ${{ secrets.SN_INSTANCE_URL }}
            devops-integration-username: ${{ secrets.SN_DEVOPS_CONFIG_USERNAME }}
            devops-integration-password: ${{ secrets.SN_DEVOPS_CONFIG_PASSWORD }}
            application-name: PaymentDemo
            deployable-name: Production
            exporter-name: returnDataforNodeName-now
            snapshot-name: Production-v1.dpl
            exporter-arguments: '{ "nodeName": "node1" }'
    ```

-   **Example — Export the latest deployed snapshot with additional parameters**

    ```
    export:
        name: Export config
        needs: <upstream job>
        runs-on: ubuntu-latest
        steps:
        - name: ServiceNow DevOps Config Export
          uses: ServiceNow/servicenow-devops-config-export@v1.0.0-beta
          with:
            instance-url: ${{ secrets.SN_INSTANCE_URL }}
            devops-integration-username: ${{ secrets.SN_DEVOPS_CONFIG_USERNAME }}
            devops-integration-password: ${{ secrets.SN_DEVOPS_CONFIG_PASSWORD }}
            application-name: PaymentDemo
            deployable-name: Production
            exporter-name: returnDataforNodeName-now
            exporter-arguments: '{ "nodeName": "node1" }'
            exporter-data-format: XML
    ```


