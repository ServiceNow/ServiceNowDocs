---
title: Queued Application Operations
description: CICD APIs that must obtain the update instance wide lock / mutex to perform the requested operations are queued instead of being rejected when the update instance wide lock / mutex is occupied by the other operations.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Application sharing, Administer your apps, Deploying applications, Building applications]
---

# Queued Application Operations

CICD APIs that must obtain the update **instance wide lock / mutex** to perform the requested operations are queued instead of being rejected when the update **instance wide lock / mutex** is occupied by the other operations.

Beginning in Tokyo, the CICD APIs that require to obtain the update **instance wide lock / mutex** to perform the requested operations will be queued instead of being rejected when the update **instance wide lock / mutex** is occupied by the other operations. When a CICD request is received, the corresponding CICD service constructs an application operation NowMQ \(Now Message Queue\) message and insert the message to the queue using NowMQ APIs. The queued messages are then polled by the scheduled job and handled one by one or in parallel if parallel processing is enabled and the operation satisfies necessary criteria.

## Application Operation NowMQ Message

The application operation NowMQ messages have a common subject that is "sys.applifecycle.operation”. The message body of the application operation NowMQ message contains a JSON object that includes the sys\_id of the Execution Tracker \(also refer to as the progress id returned in the CICD API response\), the operation type that can be one of the following: app\_install, plugin\_activation, batch\_install, rollback, import\_app and apply\_changes. It also contains the information like plugin id for plugin activation, app id or scope for application install.

## Execution Tracker for Application Operation

When the Application Operation NowMQ message is constructed and inserted, the Execution Tracker record for the corresponding CICD request is created and its sys\_id is added into the body of the NowMQ message. The Execution Tracker is in Pending state initially. The Execution Tracker’s “Details” column contains the information about the type of operation, and the important input parameters for the CICD request. Its “Message” column contains the information about the queue position. When the queue is paused, the message is prefixed with “\[App Operation Queue is paused\]”.

Sample Application Operations Execution Trackers when queue is running. ![Sample application operation queue running.](../image/sample-app-operation-queue-running.png)

Sample Application Operation Execution Trackers when queue is paused.![Sample application operations execution trackers when queue is paused.](../image/sample-app-operation-queue-paused.png)

**Note:** Operations that are in a pending state will not display in recent history.

Sample Applications Operations Execution Trackers recent history. Recent history displays historical operations that were queued and processed in the past 24hrs.

![Recent history tracker shows executions](../image/applications-operations-exe-tracker-recent-history.png)

## Manage Application Operation Queue

While manually installing products from All Applications is queued, manually installing an application from UI like All Applications or Application Manager isn’t queued.

Sometimes, the instance may be receiving, queueing, and handling many CICD requests which may cause the manual install from UI starving for update **instance wide lock / mutex**. When this happens, admin can temporarily pause the Application Operation Queue.

Admin can manage the Application Operation Queue through System Diagnostics-&gt;Application Operation Queue UI page. On “Operation Queue Status” panel, the admin can pause or resume the queue. Admin can also cancel the pending execution tracker, this will eventually remove the corresponding queued message from NowMQ by the App Operation Queue Health Monitor job.

## Application Operation Queue UI page

Sample Application Operation Queue UI page. Admin can click the button in “Operation Queue Status” to pause or resume the queue.![Application operation queue ui page.](../image/app-operation-queue-ui-page.png)

Click the “Application Operations Execution Trackers” list item, it opens the Execution Tracker form. If the queued message is pending in the queue, update the execution tracker state to “Cancelled” and save the change will cancel the corresponding queued CICD request. Note: if the state of the execution tracker is “Running”, the CICD request can’t be cancelled.![Execution tracker form.](../image/execution-tracker-page.png)

## Application Operation Queue and Upgrade Window

By default, 2 hours \(can be customized through sys property “com.glide.update\_operation.queue\_upgrade\_window”\) before the scheduled upgrade, Application Operation Queue stop processing queued messages.

The Application Operation Queue status is changed to “Upgrade Paused”. During this upgrade window, new CICD requests continue to be queued.![Application operation queue and upgrade window.](../image/app-operation-queue-and-upgrade.png)

When upgrade completes, the Application Operation Queue resumes processing the queued messages automatically.

## Impact to CICD Pipeline

The existing request/response contracts for the CICD APIs aren’t changed. The operation failure due to update **instance wide lock / mutex** conflicts that are observed in a pre-Tokyo release won’t be seen. The request is queued and served one by one or in parallel depending on they job type.

## CICD APIs supporting queueing

The following CICD APIs are queued for processing.

-   api/sn\_cicd/app\_repo/install
-   api/sn\_cicd/v1/app\_repo/install
-   api/sn\_cicd/v2/app\_repo/install
-   api/sn\_cicd/app\_repo/rollback
-   api/sn\_cicd/v1/app\_repo/install
-   api/sn\_cicd/v2/app\_repo/rollback
-   api/sn\_cicd/sc/apply\_changes
-   api/sn\_cicd/v1/sc/apply\_changes
-   api/sn\_cicd/v2/sc/apply\_changes
-   api/sn\_cicd/app/batch/install
-   api/sn\_cicd/sc/import
-   api/sn\_cicd/plugin/\{plugin\_id\}/activate
-   api/sn\_cicd/plugin/\{plugin\_id\}/rollback

## Parallelize Application Installs and Plugin Activations

Starting in Tokyo, the following operations can execute in parallel with other operations.

-   api/sn\_cicd/app\_repo/install
-   api/sn\_cicd/v1/app\_repo/install
-   api/sn\_cicd/v2/app\_repo/install
-   api/sn\_cicd/plugin/\{plugin\_id\}/activate

All queue processing takes an **instance wide lock / mutex** and holds this mutex until any queued operation is completed. This lock is called **UpdateMutex**, and its status can be viewed in the **sys\_mutex** table. During this time, operations that take this same lock \(app installs, plugin activations, source control operations\) are not performable via the UI. The queue can still be paused via the **Application Operation Queue** page to release the lock after currently running jobs have been completed.

Parallelization is enabled by default. It can be turned off by using the property `com.glide.update_operation.parallel_operation_enabled`, and all operations will run sequentially from the queue as in previous releases.

## Limits on Parallelization

The queue processor determines if an enqueued job can run. If a job can run, it is scheduled to be picked up by an instance node at first availability. If not, it is returned to the queue, and the processor evaluates the next job in the queue for processing.

There is a limit to the maximum number of jobs that can be executed in parallel, which defaults to 2. This property can be toggled via `glide.update.app_operation_queue.parallel.max` but keep in mind that there is an upper limit of available threads to perform the install and increased parallelization takes additional memory that can slow the instance for active users.

## Obtaining Resource Locks

The following plugins and applications can't be installed in parallel.

-   Any two operations that share the same scope including customizations.
-   Any two operations that cause schema changes.
-   Any two operations containing fix scripts.

Queue processing determines if these criteria are met for enqueued operations and defers not processable jobs if necessary. The Progress ID of the job is updated to reflect if the operation is waiting for appropriate resource locks to be obtained. An executing operation maintains a list of the resources \(scopes, schema, fix scripts present\) in the sys\_padlock table, and the insert and release of these locks can be observed in this table by the Progress ID. If a queued job is deferred due to inability to obtain necessary locks on resources, it is put on a cool-down to allow other messages to process. The cool-down period can be modified with property `com.glide.update_operation.job_cancel_timeout_minutes`. The job is still in the queue and is visible on the **Application Operation Queue** page.

If the queue is unable to download an application package or find a plugin to check for necessary resources to obtain, it logs an error against that queued operation. If the operation fails to preview its resources a determined number of times, the tracker fails, and the job is removed from the queue. The maximum number of times defaults to 3 and can be modified by the `com.glide.update_operation.max_failure_count` property.

**Note:** Failing to obtain necessary locks doesn't count as a failure attempt. Only errors encountered such as failing to download an application package from AppRepo count.

**Parent Topic:**[Application sharing](../concept/c_SharingApplications.md)

