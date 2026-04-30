---
title: Set the proxy server initial memory limit and upper bound memory limit
description: Set the initial memory limit and upper bound memory limit to specify how much memory the proxy server can consume. Set these limits to avoid performance issues in your Edge Encryption implementation.
locale: en-US
release: xanadu
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Install the Edge Encryption proxy server using the command line installer, Installing Edge Encryption, Edge Encryption, Encryption]
---

# Set the proxy server initial memory limit and upper bound memory limit

Set the initial memory limit and upper bound memory limit to specify how much memory the proxy server can consume. Set these limits to avoid performance issues in your Edge Encryption implementation.

## Before you begin

Role required: admin

## About this task

As a guideline, set both the initial memory limit and the upper bound memory limit to the same value. On any machine, allocate 2 GB of the physical memory to the operating system \(OS\). Then allocate the rest of the physical memory to the heap using the initial memory limit and upper bound memory limit properties. For example, on a machine with 8 GB of memory, allocate 2 GB to the OS, and allocate the remaining 6 GB \(6144 m\) to the initial and upper bound memory.

**Important:** If your Edge Encryption proxy server is running, you must stop and restart the proxy server after updating these properties.

## Procedure

1.  In your proxy server directory, open `<install dir>/conf/wrapper.conf`.

2.  To set the initial memory limit, add the following line at the end of the file:

    ```
    wrapper.java.additional.<number>=-Xms<min_memory_in_MB>m
    ```

    Set `<number>` to the next available `<number>` in the sequence of `wrapper.java.additional.<number>` properties defined in the `wrapper.conf` file.

    For example, you have the following list of `wrapper.java.additional.<number>` properties:

    ```
    wrapper.java.additional.1=
    wrapper.java.additional.2=
    ```

    The maximum `<number>` in the above list is **2**. When you add the `wrapper.java.additional.<number>=-Xms<min_memory_in_MB>m` line, set `<number>` to **3**, the next available number.

    **Important:** Do not leave gaps in the numbering sequence.

    Set `<min_memory_in_MB>` to the number of megabytes of memory remaining after allocating 2 GB of memory to the OS.

3.  Set the upper bound memory limit.

    Because an upper bound memory limit is not set in the base system, the proxy server can use all available memory. If other services are running on the server, you may want to set the upper bound memory limit.

    Add the following line at the end of the file:

    `wrapper.java.additional.<number>=-Xmx<max_memory_in_MB>m`

    Set `<number>` to the next available `<number>` in the sequence of `wrapper.java.additional.<number>` properties defined in the `wrapper.conf` file.

    For example, you have the following list of `wrapper.java.additional.<number>` properties:

    ```
    wrapper.java.additional.1=
    wrapper.java.additional.2=
    ```

    The maximum `<number>` in the above list is **2**. When you add the `wrapper.java.additional.<number>=-Xmx<max_memory_in_MB>m` line, set `<number>` to **3**, the next available number.

    **Note:** Do not leave gaps in the numbering sequence.

    Set `<max_memory_in_MB>` to the number of megabytes of memory remaining after allocating 2 GB of memory to the OS.

4.  Save and close the file.


## Example: Setting proxy server initial and upper bound memory limits

```
wrapper.java.additional.1 = -Djava.io.tmpdir=../tmp
wrapper.java.additional.2 = -Dcloudedge.home.dist=..
# must ensure UTF8 encoding when running on Windows
wrapper.java.additional.3 = -Dfile.encoding=UTF8
# additional properties for heap settings
wrapper.java.additional.4 = -Xms6144m
wrapper.java.additional.5 = -Xmx6144m
```

## What to do next

[Start the Edge Encryption proxy](t_RuntheProxy.md).

**Parent Topic:**[Install the Edge Encryption proxy server using the command line installer](manual-proxy-install.md)

**Previous topic:**[Configure a web proxy](t_SetUpWebProxyProperties.md)

**Next topic:**[Start the Edge Encryption proxy](t_RuntheProxy.md)

