---
title: Linux metrics
description: The following table lists the metrics that are gathered as output from Linux checks. Entries indicated as Featured metrics are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 10
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Linux metrics

The following table lists the metrics that are gathered as output from Linux checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|proc.acc.running| | |Number of processes running with this name \(acc\).|
|proc.acc.cpuPercent| | |Percentage of CPU taken by the process.|
|proc.acc.memPercent| | |Percentage of memory taken by the process.|

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|reboot.count.today| | |Number of reboots today.|

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|cpu.total.user| | |Normal processes executing in user mode; **cpu.total.user** is the total of the **cpuN.user** metrics.|
|cpu.total.nice| | |Niced processes executing in user mode; **cpu.total.nice** is the total of the **cpuN.nice** metrics.|
|cpu.total.system| | |Time the CPU spent running the kernel; **cpu.total.system** is the total of the **cpuN.system** metrics.|
|cpu.total.idle| | |Total time the CPU spent in an idle state; **cpu.total.idle** is the total of the **cpuN.idle** metrics.|
|cpu.total.iowait| | |Total time the CPU spent waiting for IO operations to complete; **cpu.total.iowait** is the total of the **cpuN.iowait** metrics.|
|cpu.total.irq| | |Total time that the processor is spending on Interrupts; **cpu.total.irq** is the total of the **cpuN.irq** metrics.|
|cpu.total.softirq| | |Time spent servicing soft interrupt requests; **cpu.total.softirq** is the total of the **cpuN.softirq** metrics.|
|cpu.total.steal| | |Total time the virtual CPU spent waiting for the Hypervisor to service another virtual CPU. Applies only to virtual machines.|
|cpu.total.guest| | |Total time the CPU spent running the virtual processor. Applies only to Hypervisors.|
|cpu.total.guest\_nice| | |Total time the CPU spent running as nice guest OS; **cpu.total.guset\_nice** is the total of the **cpuN.guest\_nice** metrics|
|cpu.&lt;cpu-core&gt;.user| | |Time spent with normal processing in user mode.|
|cpu.&lt;cpu-core&gt;.nice| | |Time spent with niced processing in user mode.|
|cpu.&lt;cpu-core&gt;.system| | |Time spent running in kernel mode.|
|cpu.&lt;cpu-core&gt;.idle| | |Time spent idle.|
|cpu.&lt;cpu-core&gt;.iowait| | |Time spent waiting for I/O to complete. Also considered idle time.|
|cpu.&lt;cpu-core&gt;.irq| | |Time spent serving hardware interrupts.|
|cpu.&lt;cpu-core&gt;.softirq| | |Time spent serving software interrupts.|
|cpu.&lt;cpu-core&gt;.steal| | |Time stolen by other operating systems running in a virtual environment.|
|cpu.&lt;cpu-core&gt;.guest| | |Time spent running a virtual CPU or guest OS under the control of the kernel.|
|cpu.&lt;cpu-core&gt;.guest\_nice| | |Total time the CPU spent running as nice guest OS.|
|cpu.intr| | |Interrupts serviced since boot time.|
|cpu.ctxt| | |Total number of context switches across all CPUs.|
|cpu.btime| | |Boot time.|
|cpu.processes| | |The number of processes and threads created, which includes \(but is not limited to\) those created by calls to the fork\(\) and clone\(\) system calls.|
|cpu.procs\_running| | |The total number of processes running on all CPUs.|
|cpu.procs\_blocked| | |The number of processes currently blocked and waiting for I/O to complete.|
|cpu.cpu\_count| | |The number of CPUs on the system.|
|cpu.&lt;cpu-core&gt;.cores| | |The number of CPU cores.|

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|load\_avg.one \(featured metric\)| | |The average system load over one minute.|
|load\_avg.five \(featured metric\)| | |The average system load over five minutes.|
|load\_avg.fifteen \(featured metric\)| | |The average system load over fifteen minutes.|
|load\_avg.norm.one| | |The average system load over one minute normalized by the number of CPUs.|
|load\_avg.norm.five| | |The average system load over five minutes normalized by the number of CPUs.|
|load\_avg.norm.fifteen| | |The average system load over fifteen minutes normalized by the number of CPUs.|

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|cpu.avgutilization\_percentage| | |The average percentage of CPU used.|
|cpu.user\_percentage \(featured metric\)| | |Percentage of time total CPU was used by normal processes in user mode.|
|cpu.nice\_percentage \(featured metric\)| | |Percentage of time all CPUs used by niced processes in user mode.|
|cpu.system\_percentage \(featured metric\)| | |Percentage of time the CPU spent running the kernel.|
|cpu.idle\_percentage \(featured metric\)| | |Percentage of time all CPIUs were idle.|
|cpu.iowait\_percentage \(featured metric\)| | |Percentage of time all CPUs waited for I/O to complete.|
|cpu.irq\_percentage \(featured metric\)| | |Percentage of time all CPUs serviced interrupts.|
|cpu.softirq\_percentage \(featured metric\)| | |Percentage of time all CPIs serviced software interrupts.|
|cpu.steal\_percentage \(featured metric\)| | |Percentage of time all CPUs serviced virtual-host operating systems.|
|cpu.guest\_percentage \(featured metric\)| | |Percentage of time all CPUs serviced guest operating systems.|

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|disk.&lt;disk-name&gt;.reads \(featured metric\)| | |Total number of reads completed successfully.|
|disk.&lt;disk-name&gt;.readsMerged| | |Total number of reads merged.|
|disk.&lt;disk-name&gt;.sectorsRead| | |Total number of sectors read successfully.|
|disk.&lt;disk-name&gt;.readTime| |milliseconds|Total number of milliseconds spent by all reads.|
|disk.&lt;disk-name&gt;.writes \(featured metric\)| | |Total number of writes completed successfully.|
|disk.&lt;disk-name&gt;.writesMerged| | |Total number of writes merged.|
|disk.&lt;disk-name&gt;.sectorsWritten| | |Total number of sectors written successfully.|
|disk.&lt;disk-name&gt;.writeTime| |milliseconds|Total number of milliseconds spent by all writes.|
|disk.&lt;disk-name&gt;.ioInProgress| | |Total number of I/Os currently in progress.|
|disk.&lt;disk-name&gt;.ioTime \(featured metric\)| | |Total time spent on I/Os.|
|disk.&lt;disk-name&gt;.ioTimeWeighted| | |Total time spent on I/Os. This can provide a measure of both I/O completion time and the backlog that might be accumulating.|

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|disk.&lt;file-system-name&gt;.total| | |The total size of the file system.|
|disk.&lt;file-system-name&gt;.used| | |The total amount of space allocated to existing files in the file system.|
|disk.&lt;file-system-name&gt;.avail| | |The total amount of space available within the file system.|
|disk.&lt;file-system-name&gt;.used\_percentage| | |The percentage of the available space that is currently allocated to all files on the file system.|
|disk.&lt;file-system-name&gt;.itotal| | |The total number of **inodes** on the file system.|
|disk.&lt;file-system-name&gt;.iused| | |The number of used **inodes**.|
|disk.&lt;file-system-name&gt;.iavail| | |The number of free \(unused\) **inodes**.|
|disk.&lt;file-system-name&gt;.iused\_percentage| | |The percentage of used **inodes**.|

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|disk\_usage.&lt;disk&gt;.total| | |Total amount of space available on the disk.|
|disk\_usage.&lt;disk&gt;.used| | |Total amount of space used in the disk.|
|disk\_usage.&lt;disk&gt;.avail| | |Total amount of space available on the disk.|
|disk\_usage.&lt;disk&gt;.used\_percentage \(featured metric\)| | |The percentage of space used on the disk.|

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|memory.total| | |Total usable RAM.|
|memory.free| | |Total free RAM.|
|memory.available| | |An estimate of how much memory is available for starting new applications without swapping.|
|memory.buffers| | |Temporary storage used for raw disk blocks.|
|memory.cached| | |In-memory cache for files read from disk \(the page cache\). Does not include **mem\_swapcached**.|
|memory.swapTotal \(featured metric\)| | |Total amount of swap space available.|
|memory.swapFree \(featured metric\)| | |Amount of swap space that is currently unused.|
|memory.dirty| | |Memory which is waiting to be written back to the disk.|
|memory.swapUsed \(featured metric\)| | |The amount of swap space in use.|
|memory.used| | |The amount of RAM in use.|
|memory.usedWOBuffersCaches| | |The amount of memory in use.|
|memory.freeWOBuffersCaches| | |Value of **MemAvailable** from **/proc/meminfo**if present, but falls back to free + buffered + cached memory if not.|
|memory.swapUsedPercentage| | |Percent of swap space used.|

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|memory\_percent.free \(featured metric\)| | |Percentage of free RAM.|
|memory\_percent.available \(featured metric\)| | |Percentage of memory available|
|memory\_percent.buffers \(featured metric\)| | |Percentage of memory used for raw disk blocks.|
|memory\_percent.cached \(featured metric\)| | |Percentage of memory used with in-memory cache for files read from disk.|
|memory\_percent.dirty \(featured metric\)| | |Percentage of memory waiting to be written back to the disk.|
|memory\_percent.swapUsed \(featured metric\)| | |Percentage of swap space used.|
|memory\_percent.usedWOBuffersCaches \(featured metric\)| | |Percentage of memory used.|
|memory\_percent.freeWOBuffersCaches \(featured metric\)| | |Percentage of memory available.|

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|system.uptime\(sec\)| | |The amount of time the system has been working and available.|

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|vmstat.nr\_free\_pages| | |Pages that are currently unused by the system.|
|vmstat.nr\_alloc\_batch| | |Pages allocated to other domains due to insufficient memory in each domain of each non-uniform memory access \(NUMA\) node.|
|vmstat.nr\_inactive\_anon| | |Memory pages in each domain of each NUMA node that have not been accessed.|
|vmstat.nr\_active\_anon| | |Anonymous virtual memory pages that have been recently used.|
|vmstat.nr\_inactive\_file| | |The memory page corresponding to the file that has not been accessed in each domain of each NUMA.|
|vmstat.nr\_active\_file| | |The memory page corresponding to the file that has been recently accessed.|
|vmstat.nr\_unevictable| | |The number of pages in the unevictable \(non-\)LRU list.|
|vmstat.nr\_mlock| | |Pages mapped into a VM\_LOCKED VMA that are a class of unevictable pages.|
|vmstat.nr\_anon\_pages| | |Memory mapped pages that are not part of a file.|
|vmstat.nr\_mapped| | |The number of memory mapped pages.|
|vmstat.nr\_file\_pages| | | |
|vmstat.nr\_dirty| | |Pages waiting to be written to disk.|
|vmstat.nr\_writeback| | |Pages currently being written to disk.|
|vmstat.nr\_slab\_reclaimable| | |Pages from the kernel slab memory usage that can be reclaimed.|
|vmstat.nr\_slab\_unreclaimable| | |Pages from the kernel slab memory usage that cannot be reclaimed.|
|vmstat.nr\_page\_table\_pages| | |Pages allocated to page tables.|
|vmstat.nr\_kernel\_stack| | |Amount of memory allocated to kernel stacks.|
|vmstat.nr\_unstable| | |The number of unstable pages in each domain of each NUMA node.|
|vmstat.nr\_bounce| | | |
|vmstat.nr\_vmscan\_write| | |The number of dirty pages written back during a scan of LRUs.|
|vmstat.nr\_vmscan\_immediate\_reclaim| | | |
|vmstat.nr\_writeback\_temp| | | |
|vmstat.nr\_isolated\_anon| | |The number of anonymous memory pages isolated in each domain of each NUMA node.|
|vmstat.nr\_isolated\_file| | |The number of file storage pages isolated in each domain of each NUMA node.|
|vmstat.nr\_shmem| | |The number of shared memory pages.|
|vmstat.nr\_dirtied| | |The number of dirty pages in each domain of each NUMA node.|
|vmstat.nr\_written| | | |
|vmstat.numa\_hit| | |The number of pages that were successfully allocated to this node.|
|vmstat.numa\_miss| | |The number of pages that were allocated to this node because of low memory on the intended node.|
|vmstat.numa\_foreign| | |The number of pages initially intended for this node that were allocated to another node.|
|vmstat.numa\_interleave| | |The number of interleave policy pages successfully allocated to this node.|
|vmstat.numa\_local| | |The number of pages successfully allocated on this node by a process on this node.|
|vmstat.numa\_other| | |The number of pages allocated on this node by a process on another node.|
|vmstat.workingset\_refault| | | |
|vmstat.workingset\_activate| | | |
|vmstat.workingset\_nodereclaim| | | |
|vmstat.nr\_anon\_transparent\_hugepages| | | |
|vmstat.nr\_free\_cma| | |Free continuous memory allocator pages in each domain of each NUMA.|
|vmstat.nr\_dirty\_threshold| | | |
|vmstat.nr\_dirty\_background\_threshold| | | |
|vmstat.pgpgin| | |The number of pages brought in from disk.|
|vmstat.pgpgout| | |The number of pages written out to disk.|
|vmstat.pswpin| | |The number of pages brought in from swap space.|
|vmstat.pswpout| | |The number of pages swapped out into swap space.|
|vmstat.pgalloc\_dma| | | |
|vmstat.pgalloc\_dma32| | | |
|vmstat.pgalloc\_normal| | | |
|vmstat.pgalloc\_movable| | | |
|vmstat.pgfree| | |The number of pages free since the last boot.|
|vmstat.pgactivate| | |Number of page activations since the last boot.|
|vmstat.pgdeactivate| | |Number of page deactivations since the last boot.|
|vmstat.pgfault| | |Minor faults since the last boot.|
|vmstat.pgmajfault| | |Major faults since the last boot.|
|vmstat.pglazyfreed| | | |
|vmstat.pgrefill\_dma| | | |
|vmstat.pgrefill\_dma32| | | |
|vmstat.pgrefill\_normal| | |Number of page refills since the last boot.|
|vmstat.pgrefill\_movable| | | |
|vmstat.pgsteal\_kswapd\_dma| | | |
|vmstat.pgsteal\_kswapd\_dma32| | | |
|vmstat.pgsteal\_kswapd\_normal| | | |
|vmstat.pgsteal\_kswapd\_movable| | | |
|vmstat.pgsteal\_direct\_dma| | | |
|vmstat.pgsteal\_direct\_dma32| | | |
|vmstat.pgsteal\_direct\_normal| | | |
|vmstat.pgsteal\_direct\_movable| | | |
|vmstat.pgscan\_kswapd\_dma| | | |
|vmstat.pgscan\_kswapd\_dma32| | | |
|vmstat.pgscan\_kswapd\_normal| | |Number of pages scanned by **kswapd** since boot.|
|vmstat.pgscan\_kswapd\_movable| | | |
|vmstat.pgscan\_direct\_dma| | | |
|vmstat.pgscan\_direct\_dma32| | | |
|vmstat.pgscan\_direct\_normal| | |Number of pages reclaimed since boot.|
|vmstat.pgscan\_direct\_movable| | | |
|vmstat.pgscan\_direct\_throttle| | | |
|vmstat.zone\_reclaim\_failed| | | |
|vmstat.pginodesteal| | | |
|vmstat.slabs\_scanned| | | |
|vmstat.kswapd\_inodesteal| | | |
|vmstat.kswapd\_low\_wmark\_hit\_quickly| | | |
|vmstat.kswapd\_high\_wmark\_hit\_quickly| | | |
|vmstat.pageoutrun| | |Number of times **kswapd** called page reclaim.|
|vmstat.allocstall| | |Number of times page reclaim was called directly \(low memory\).|
|vmstat.pgrotated| | | |
|vmstat.drop\_pagecache| | | |
|vmstat.drop\_slab| | | |
|vmstat.numa\_pte\_updates| | | |
|vmstat.numa\_huge\_pte\_updates| | | |
|vmstat.numa\_hint\_faults| | | |
|vmstat.numa\_hint\_faults\_local| | | |
|vmstat.numa\_pages\_migrated| | | |
|vmstat.pgmigrate\_success| | | |
|vmstat.pgmigrate\_fail| | | |
|vmstat.compact\_migrate\_scanned| | | |
|vmstat.compact\_free\_scanned| | | |
|vmstat.compact\_isolated| | | |
|vmstat.compact\_stall| | |The number of times a process stalls when running memory compaction so that a huge page is free for use.|
|vmstat.compact\_fail| | |The number of times the system attempted to compact memory but failed.|
|vmstat.compact\_success| | |The number of times the system compacted memory and freed a huge page for use.|
|vmstat.htlb\_buddy\_alloc\_success| | | |
|vmstat.htlb\_buddy\_alloc\_fail| | | |
|vmstat.unevictable\_pgs\_culled| | | |
|vmstat.unevictable\_pgs\_scanned| | | |
|vmstat.unevictable\_pgs\_rescued| | | |
|vmstat.unevictable\_pgs\_mlocked| | | |
|vmstat.unevictable\_pgs\_munlocked| | | |
|vmstat.unevictable\_pgs\_cleared| | | |
|vmstat.unevictable\_pgs\_stranded| | | |
|vmstat.thp\_fault\_alloc| | |The number of huge pages successfully allocated to handle a page fault.|
|vmstat.thp\_fault\_fallback| | |The number of page fault fails to allocate a huge page before falling back to using small pages.|
|vmstat.thp\_collapse\_alloc| | |The number of pages collapsed into one huge page with the successful allocation of a new huge page to store the data.|
|vmstat.thp\_collapse\_alloc\_failed| | |The number of pages collapsed into one huge page but failed allocation.|
|vmstat.thp\_split| | |The number of base pages to split from a huge page.|
|vmstat.thp\_zero\_page\_alloc| | |The number of successful allocations of huge zero pages.|
|vmstat.thp\_zero\_page\_alloc\_failed| | |The number of times the kernel failed to allocate a huge zero page and falls back to using small pages.|
|vmstat.balloon\_inflate| | | |
|vmstat.balloon\_deflate| | | |
|vmstat.balloon\_migrate| | | |

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|proc.&lt;process&gt;.VmSize| | |The total amount of virtual memory used by the process.|
|proc.&lt;process&gt;.VmRSS| | |The non-swapped physical memory used by a process.|
|proc.&lt;process&gt;.VmSwap| | |The total amount of swap space used.|

**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

