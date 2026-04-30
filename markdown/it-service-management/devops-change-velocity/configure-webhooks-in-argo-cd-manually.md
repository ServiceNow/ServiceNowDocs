---
title: Configure webhooks in Argo CD manually
description: Configure webhooks in Argo CD to send sync notifications to the DevOps Change Velocity application.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Argo CD, Integrate, DevOps Change Velocity, IT Service Management]
---

# Configure webhooks in Argo CD manually

Configure webhooks in Argo CD to send sync notifications to the DevOps Change Velocity application.

## Before you begin

Role required: Argo CD admin

## About this task

The subscription to Argo CD application events can be defined using the `notifications.argoproj.io/subscribe.<trigger>.<service>: <recipient>` annotation.

## Procedure

1.  In Argo CD, update the `ConfigMap: argocd-notifications-cm.yaml` to set up the notifications that are send to DevOps Change Velocity.

    ```
    apiVersion: v1 
    kind: configMap 
    metadata: 
      name: argocd-notifications-cm 
      namespace: default 
    data: 
      context: | 
        argocdUrl: "https://<argocdURL>" 
      service.webhook.sn_devops_argocd: | 
        url: https://<instance>.service-now.com/api/sn_devops/v2/devops/tool/orchestration?toolId=<toolId> 
        basicAuth: #optional username password 
          username: "" 
          password: "" 
      template.app-sync-succeeded: | 
        webhook: 
          sn_devops_argocd: 
            method: POST 
            body: | 
              {  
              "titleLink" : "http://<argocdURL>/applications/{{.app.metadata.name}}", 
              "syncStatus" : "{{.app.status.sync.status}}", 
              "repo" : "{{.app.spec.source.repoURL}}", 
              "revision": "{{.app.status.sync.revision}}", 
              "path": "/repos/{{call .repo.FullNameByRepoURL .app.spec.source.repoURL}}/statuses/{{.app.status.operationState.operation.sync.revision}}", 
              "commitAuthor" : "{{(call .repo.GetCommitMetadata .app.status.sync.revision).Author}}", 
              "commitMessage" : "{{(call .repo.GetCommitMetadata .app.status.sync.revision).Message}}", 
              "commitTags" : "{{(call .repo.GetCommitMetadata .app.status.sync.revision).Tags}}", 
              "startedAt" : "{{.app.status.operationState.startedAt}}", 
              "finishedAt" : "{{.app.status.operationState.finishedAt}}", 
              "message": "{{.app.metadata.name}} app is synced" 
              } 
      trigger.on-sync-status-unknown: | 
        - description: Application status is 'Unknown' 
          send: 
          - app-sync-status-unknown 
          when: app.status.sync.status == 'Unknown' 
      trigger.on-sync-succeeded: | 
        - description: Application syncing has succeeded 
          send: 
          - app-sync-succeeded 
          when: app.status.operationState.phase in ['Succeeded'] 
      subscriptions: | 
        - recipients: 
          - sn_devops_argocd 
          triggers: 
          - on-sync-succeeded 
          - on-sync-status-unknown
    ```

2.  Open the Argo CD app for which you are configuring webhooks.

3.  Navigate to **APP DETAILS &gt; SUMMARY**.

4.  Add the **notifications.argoproj.io/subscribe.&lt;trigger&gt;.&lt;service&gt;: &lt;recipient&gt;** annotation with the trigger condition to sync the change status for your instance.

    For example, `notifications.argoproj.io/subscribe.on-sync-succeeded.sn_devops_argocd`.![Notification subscription.](../image/argocd-9.png)


**Parent Topic:**[Argo CD integration with DevOps Change Velocity](../concept/argo-cd-integration-with-devops-change-velocity.md)

