---
title: Set MID Server thread use
description: Change the number of threads used by the MID Server according to performance requirements. MID Servers which compete with other programs for CPU time can use fewer threads than the default. MID Servers which need more speed, and have a host computer powerful enough, can use more threads.
locale: en-US
release: xanadu
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Set MID Server thread use

Change the number of threads used by the MID Server according to performance requirements. MID Servers which compete with other programs for CPU time can use fewer threads than the default. MID Servers which need more speed, and have a host computer powerful enough, can use more threads.

## Before you begin

Role required: admin

<table id="table_ckr_vs4_nhb"><tbody><tr><td>

![Setup indicator for configuration phase](../image/ProgressBarConfig.png)

</td></tr></tbody>
</table>## About this task

The three parameters define the maximum numbers of worker threads that can run simultaneously in each pool: **threads.interactive.max**, **threads.expedited.max**, and **threads.max**. Changing the thread parameters can affect the MID Server performance.

The interactive thread pool is designed for executing interactive messages including system commands and heartbeats. They are typically lightweight, so usually there is no need to change the default value. The expedited thread pool is designed for executing messages that have higher priority than the standard ones but less than interactive ones. Unless you have applications that produce a lot of expedited messages, there is no need to change the default value for **threads.expedited.max**.

The standard thread pool is the busiest pool. Most probes are using it and they can take a lot of system resources such as CPU, memory, and so on. You can set the MID Server to use as few as five threads without issue. To increase the speed of the MID Server if the host is powerful enough or lightly loaded with other programs, you can increase the threads setting.

The threads setting depends on the limitation of the CPU speed, memory, and operating system of the host machine. You might have to experiment to find the optimal threads count that works best when the MID Server is busy so it does not exhaust the host machine’s hardware limitations. This means you may have to refine the thread count to best meet your situation. The following general observations may be useful:

-   PowerShell is resource intensive and threads may not scale linearly.
-   Most MID Server tasks require file handles to do their job.
    -   Windows: On the Windows operating system, file handles are available in a fixed quantity. If you configure too many MID Server threads on a Windows host, the MID Server can consume all the file handles before approaching maximum CPU usage. This situation appears as an Out of file handles error in the MID Server log and indicates that the MID Server is trying to use too many threads.
    -   UNIX and Linux: UNIX and Linux hosts have a much different scheme for allocating file handles. Generally, you can increase MID Server thread use on these operating systems until the CPU of the host is overloaded. See your OS documentation for monitoring CPU usage.
-   Each thread on the MID Server requires some memory. Exactly how much memory varies considerably from task to task and depends on the equipment being discovered. To increase the number of threads, you might have to [increase the amount of memory](t_MIDServerOptionalConfiguration.md) that Java uses. If you configure insufficient memory, an Out of memory error appears in the MID Server log.
-   You can set threads.max as high as 200, however, this setting may need to be changed depending on the OS. For example, Windows-based MID Servers running Discovery uses Powershell which is resource intensive. In this case, you may exhaust the CPU power of the host machine with just 50 threads count.

Follow the steps below to change the `config.XML` file. Alternatively, use the `threads.max` connection parameter. See [MID Server Connection parameters](../reference/mid-server-parameters.md#) for more details.

## Procedure

1.  Open the **\\agent\\config.xml** file using any text editor.

2.  Locate the following lines:

    ```
    <!-- MID Server Threads --><parameter name="threads.max" value="25"/>
    ```

3.  Edit the value.

    Keep in mind the cautions described above.

4.  Save the record.

5.  Restart the MID Server service.


**Parent Topic:**[Configuring MID Servers](../concept/c_MIDServerConfiguration.md)

