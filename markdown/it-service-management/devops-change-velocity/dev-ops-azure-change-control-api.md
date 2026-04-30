---
title: Configuring change control using the Azure Invoke REST API
description: You can use the Azure Invoke REST API in your YAML or Classic Azure pipeline to configure change control for DevOps.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring the Azure pipeline for DevOps, Azure DevOps, Integrate, DevOps Change Velocity, IT Service Management]
---

# Configuring change control using the Azure Invoke REST API

You can use the Azure Invoke REST API in your YAML or Classic Azure pipeline to configure change control for DevOps.

You must enable the **This property decides whether to create a Generic Connection on configure operation for Azure DevOps** property to use Invoke REST API.

For Azure Invoke REST API details, visit the [Microsoft documentation site](http://docs.microsoft.com) and search for [`Invoke HTTP REST API task- Azure Pipelines`](https://learn.microsoft.com/en-us/azure/devops/pipelines/tasks/reference/invoke-rest-api-v1?view=azure-pipelines&tabs=yaml).

**Important:**

If you have duplicate or reused job names in your pipeline execution steps, ensure that the stageName attribute contains azurestageName/jobName in it’s value, i.e. `stageName = azureStageName/jobName`. The artifact registration tasks send both stage and job names to associate the artifact version to the correct task execution.

## Generic service connection

Using the Azure Invoke REST API requires the creation of a generic service connection in Azure DevOps.

![Azure YAML REST API change control connection](../image/dev-ops-azure-api-change-conn.png)

## YAML Azure pipeline

In Azure DevOps, a server task must be created with the service connection as the change control endpoint.

<table id="table_yjj_5mp_wmb"><thead><tr><th>

Azure pipeline type

</th><th>

Values

</th></tr></thead><tbody><tr><td>

Build

</td><td>

-   buildNumber
-   isMultiBranch
-   branchName

</td></tr><tr><td>

Release

</td><td>

-   releaseNumber
-   projectName

</td></tr></tbody>
</table>**Note:** For release pipelines, set the **Pre-deployment conditions** &gt; **Advanced** &gt; **Completion event** field to Callback.

Build pipeline:

```

- task: InvokeRESTAPI@1
      inputs:
        connectionType: 'connectedServiceName'
        serviceConnection: 'change1'
        method: 'POST'
        body: |
         {
            "buildNumber": "$(build.buildId)",
            "isMultiBranch": "true",
            "branchName": "$(build.sourceBranchName)"
         }
        waitForCompletion: 'true'
```

Release pipeline:

```

- task: InvokeRESTAPI@1
      inputs:
        connectionType: 'connectedServiceName'
        serviceConnection: 'change1'
        method: 'POST'
        body: |
         {
            "releaseNumber": "$(Release.ReleaseId)",
            "projectName": "$(System.TeamProject)"
         }
        waitForCompletion: 'true'
```

## Classic Azure pipeline

For a Classic Azure pipeline, an Invoke REST API server task must be added.

![Azure Pipeline Invoke REST API change control](../image/dev-ops-azure-api-change-classic.png "Classic Azure build pipeline example")

![DevOps Azure classic release pipeline](../image/dev-ops-azure-api-chg-rel-classic.png "Classic Azure release pipeline example")

**Parent Topic:**[Azure DevOps integration with DevOps Change Velocity](azure-devops-integration-dev-ops.md)

