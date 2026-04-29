---
title: Linux default checks and policies
description: Agent Client Collector provides the following default checks and policies for Linux Metrics monitoring.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Agent Client Collector Monitoring default checks and policies, ACC-M reference, Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# Linux default checks and policies

Agent Client Collector provides the following default checks and policies for Linux Metrics monitoring.

## Linux monitoring metrics checks

<table id="table_ls1_pyn_v5b"><thead><tr><th>

Check

</th><th>

Metric Name

</th><th>

Resource

</th><th>

Description

</th><th>

Units

</th><th>

Featured Metric

</th><th>

Anomaly Detection

</th></tr></thead><tbody><tr><td rowspan="3">

os.linux.metrics-process-usage

</td><td>

proc.acc.running

</td><td>

process-name

</td><td>

Number of processes running with this name\(acc\)

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

proc.acc.cpuPercent

</td><td>

process-name

</td><td>

Percentage of cpu taken by the process.

</td><td>

percent

</td><td>

 

</td><td>

 

</td></tr><tr><td>

proc.acc.​memPercent

</td><td>

process-name

</td><td>

Percentage of memory taken by the process.

</td><td>

percent

</td><td>

 

</td><td>

 

</td></tr><tr><td>

os.linux.metrics-reboot-count-today

</td><td>

reboot.count.today

</td><td>

empty

</td><td>

Number of reboot done on today

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td rowspan="28">

os.linux.metrics-system-cpu

</td><td>

cpu.total.user

</td><td>

total

</td><td>

Normal processes executing in user mode; cpu.total.user is the total of the cpuN.user metrics.

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.total.nice

</td><td>

total

</td><td>

Niced processes executing in user mode; cpu.total.nice is the total of the cpuN.nice metrics.

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.total.system

</td><td>

total

</td><td>

Time the CPU spent running the kernel; cpu.total.system is the total of the cpuN.system metrics.

</td><td>

sec

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.total.idle

</td><td>

total

</td><td>

Total time the CPU spent in an idle state.; cpu.total.idle is the total of the cpuN.idle metrics.

</td><td>

sec

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.total.iowait

</td><td>

total

</td><td>

Total time the CPU spent waiting for IO operations to complete.; cpu.total.iowait is the total of the cpuN.iowait metrics.

</td><td>

sec

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.total.irq

</td><td>

total

</td><td>

Total time that the processor is spending on handling Interrupts.; cpu.total.irq is the total of the cpuN.irq metrics.

</td><td>

sec

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.total.softirq

</td><td>

total

</td><td>

Time spent on servicing soft interrupt requests; cpu.total.softirq is the total of the cpuN.softirq metrics.

</td><td>

sec

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.total.steal

</td><td>

total

</td><td>

Total time the virtual CPU spent waiting for the hypervisor to service another virtual CPU. Only applies to virtual machines.

</td><td>

sec

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.total.guest

</td><td>

total

</td><td>

Total time the CPU spent running the virtual processor. Only applies to hypervisors.

</td><td>

sec

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.total.guest\_nice

</td><td>

total

</td><td>

Total time the CPU spent running as nice guest OS. cpu.total.guset\_nice si the total of the cpuN.guest\_nice metrics

</td><td>

sec

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.&lt;cpu-core&gt;.user

</td><td>

cpu-core

</td><td>

Time spent with normal processing in user mode.

</td><td>

sec

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.&lt;cpu-core&gt;.nice

</td><td>

cpu-core

</td><td>

Time spent with niced processes in user mode.

</td><td>

sec

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.&lt;cpu-core&gt;.system

</td><td>

cpu-core

</td><td>

Time spent running in kernel mode.

</td><td>

sec

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.&lt;cpu-core&gt;.idle

</td><td>

cpu-core

</td><td>

Time spent in vacations twiddling thumbs.

</td><td>

sec

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.&lt;cpu-core&gt;.iowait

</td><td>

cpu-core

</td><td>

Time spent waiting for I/O to completed. This is considered idle time too.

</td><td>

sec

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.&lt;cpu-core&gt;.irq

</td><td>

cpu-core

</td><td>

Time spent serving hardware interrupts.

</td><td>

sec

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.&lt;cpu-core&gt;.softirq

</td><td>

cpu-core

</td><td>

Time spent serving software interrupts.

</td><td>

sec

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.&lt;cpu-core&gt;.steal

</td><td>

cpu-core

</td><td>

Time stolen by other operating systems running in a virtual environment.

</td><td>

sec

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.&lt;cpu-core&gt;.guest

</td><td>

cpu-core

</td><td>

Time spent for running a virtual CPU or guest OS under the control of the kernel.

</td><td>

sec

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.&lt;cpu-core&gt;.guest\_nice

</td><td>

cpu-core

</td><td>

Total time the CPU spent running as nice guest OS.

</td><td>

sec

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.intr

</td><td>

empty

</td><td>

Interrupts serviced since boot time.

</td><td>

sec

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.ctxt

</td><td>

empty

</td><td>

Total number of context switches across all CPUs.

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.btime

</td><td>

empty

</td><td>

The time the system booted

</td><td>

sec

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.processes

</td><td>

empty

</td><td>

The number of processes and threads created, which includes \(but is not limited to\) those created by calls to the fork\(\) and clone\(\) system calls.

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.procs\_running

</td><td>

empty

</td><td>

The total number of processes running on all CPUs.

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.procs\_blocked

</td><td>

empty

</td><td>

The number of processes currently blocked, waiting for I/O to complete.

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.cpu\_count

</td><td>

empty

</td><td>

Number of cpu on the system

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.&lt;cpu-core&gt;.cores

</td><td>

cpu-core

</td><td>

The number of CPU cores

</td><td>

core count

</td><td>

 

</td><td>

 

</td></tr><tr><td rowspan="6">

os.linux.metrics-system-cpu-load

</td><td>

load\_avg.one

</td><td>

empty

</td><td>

The average system load over one minute.

</td><td>

thread count

</td><td>

yes

</td><td>

yes

</td></tr><tr><td>

load\_avg.five

</td><td>

empty

</td><td>

The average system load over five minutes.

</td><td>

thread count

</td><td>

yes

</td><td>

yes

</td></tr><tr><td>

load\_avg.fifteen

</td><td>

empty

</td><td>

The average system load over fifteen minutes.

</td><td>

thread count

</td><td>

yes

</td><td>

yes

</td></tr><tr><td>

load\_avg.norm.one

</td><td>

empty

</td><td>

The average system load over one minute normalized by the number of CPUs.

</td><td>

thread count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

load\_avg.norm.five

</td><td>

empty

</td><td>

The average system load over five minutes normalized by the number of CPUs.

</td><td>

thread count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

load\_avg.norm.fifteen

</td><td>

empty

</td><td>

The average system load over fifteen minutes normalized by the number of CPUs.

</td><td>

thread count

</td><td>

 

</td><td>

 

</td></tr><tr><td rowspan="10">

os.linux.metrics-system-cpu-percentage

</td><td>

cpu.avgutilization\_​percentage

</td><td>

empty

</td><td>

Percent of cpu was used on average

</td><td>

percent

</td><td>

 

</td><td>

 

</td></tr><tr><td>

cpu.user\_​percentage

</td><td>

empty

</td><td>

Percent of time total cpu was used by normal processes in user mode

</td><td>

percent

</td><td>

yes

</td><td>

yes

</td></tr><tr><td>

cpu.nice\_​percentage

</td><td>

empty

</td><td>

Percent of time all cpus used by niced processes in user mode

</td><td>

percent

</td><td>

yes

</td><td>

yes

</td></tr><tr><td>

cpu.system\_​percentage

</td><td>

empty

</td><td>

The percent of time the CPU spent running the kernel.

</td><td>

percent

</td><td>

yes

</td><td>

yes

</td></tr><tr><td>

cpu.idle\_percentage

</td><td>

empty

</td><td>

Percent of time all cpus were idle

</td><td>

percent

</td><td>

yes

</td><td>

yes

</td></tr><tr><td>

cpu.iowait\_​percentage

</td><td>

empty

</td><td>

Percent of time all cpus waiting for I/O to complete

</td><td>

percent

</td><td>

yes

</td><td>

yes

</td></tr><tr><td>

cpu.irq\_percentage

</td><td>

empty

</td><td>

Percent of time all cpus servicing interrupts

</td><td>

percent

</td><td>

yes

</td><td>

yes

</td></tr><tr><td>

cpu.softirq\_​percentage

</td><td>

empty

</td><td>

Percent of time all cpus servicing software interrupts

</td><td>

percent

</td><td>

yes

</td><td>

yes

</td></tr><tr><td>

cpu.steal\_​percentage

</td><td>

empty

</td><td>

Percent of time all cpus serviced virtual hosts operating systems

</td><td>

percent

</td><td>

yes

</td><td>

yes

</td></tr><tr><td>

cpu.guest\_​percentage

</td><td>

empty

</td><td>

Percent of time all cpus serviced guest operating system

</td><td>

percent

</td><td>

yes

</td><td>

yes

</td></tr><tr><td rowspan="11">

os.linux.metrics-system-disk

</td><td>

disk.&lt;disk-name&gt;.reads

</td><td>

disk-name

</td><td>

Total number of reads completed successfully.

</td><td>

count

</td><td>

yes

</td><td>

yes

</td></tr><tr><td>

disk.&lt;disk-name&gt;.readsMerged

</td><td>

disk-name

</td><td>

Total number of reads merged

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

disk.&lt;disk-name&gt;.sectorsRead

</td><td>

disk-name

</td><td>

Total number of sectors read successfully.

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

disk.&lt;disk-name&gt;.readTime

</td><td>

disk-name

</td><td>

Total number of milliseconds spent by all reads.

</td><td>

millisec

</td><td>

 

</td><td>

 

</td></tr><tr><td>

disk.&lt;disk-name&gt;.writes

</td><td>

disk-name

</td><td>

Total number of writes completed successfully.

</td><td>

count

</td><td>

yes

</td><td>

yes

</td></tr><tr><td>

disk.&lt;disk-name&gt;.writesMerged

</td><td>

disk-name

</td><td>

Total number of writes merged

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

disk.&lt;disk-name&gt;.sectorsWritten

</td><td>

disk-name

</td><td>

Total number of sectors written successfully.

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

disk.&lt;disk-name&gt;.writeTime

</td><td>

disk-name

</td><td>

Total number of milliseconds spent by all writes.

</td><td>

misllisec

</td><td>

 

</td><td>

 

</td></tr><tr><td>

disk.&lt;disk-name&gt;.ioInProgress

</td><td>

disk-name

</td><td>

Total number of I/Os currently in progress

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

disk.&lt;disk-name&gt;.ioTime

</td><td>

 

</td><td>

Total time spent doing I/Os

</td><td>

millisec

</td><td>

yes

</td><td>

yes

</td></tr><tr><td>

disk.&lt;disk-name&gt;.ioTimeWeighted

</td><td>

disk-name

</td><td>

Total time spent doing I/Os. This can provide an easy measure of both I/O completion time and the backlog that may be accumulating.

</td><td>

millisec

</td><td>

 

</td><td>

 

</td></tr><tr><td rowspan="8">

os.linux.metrics-system-disk-capacity

</td><td>

disk.&lt;file-system-name&gt;.total

</td><td>

file-system-name

</td><td>

The total size of the file system.

</td><td>

byte

</td><td>

 

</td><td>

 

</td></tr><tr><td>

disk.&lt;file-system-name&gt;.used

</td><td>

file-system-name

</td><td>

The total amount of space allocated to existing files in the file system.

</td><td>

byte

</td><td>

 

</td><td>

 

</td></tr><tr><td>

disk.&lt;file-system-name&gt;.avail

</td><td>

file-system-name

</td><td>

The total amount of space available within the file system.

</td><td>

byte

</td><td>

 

</td><td>

 

</td></tr><tr><td>

disk.&lt;file-system-name&gt;.used\_percentage

</td><td>

file-system-name

</td><td>

The percentage of the available space that currently allocated to all files on the file system.

</td><td>

percent

</td><td>

 

</td><td>

 

</td></tr><tr><td>

disk.&lt;file-system-name&gt;.itotal

</td><td>

file-system-name

</td><td>

The total number of inodes on the file system.

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

disk.&lt;file-system-name&gt;.iused

</td><td>

file-system-name

</td><td>

The number of used inodes.

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

disk.&lt;file-system-name&gt;.iavail

</td><td>

file-system-name

</td><td>

The number of free \(unused\) inodes.

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

disk.&lt;file-system-name&gt;.iused\_percentage

</td><td>

file-system-name

</td><td>

The percentage of used inodes.

</td><td>

percent

</td><td>

 

</td><td>

 

</td></tr><tr><td rowspan="4">

os.linux.metrics-system-disk-usage

</td><td>

disk\_usage.&lt;disk&gt;.total

</td><td>

disk-name

</td><td>

Total amount of space available on this disk

</td><td>

bytes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

disk\_usage.&lt;disk&gt;.used

</td><td>

disk-name

</td><td>

Total amount of space used in this disk

</td><td>

bytes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

disk\_usage.&lt;disk&gt;.avail

</td><td>

disk-name

</td><td>

Total amount of space available on this disk

</td><td>

bytes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

disk\_usage.&lt;disk&gt;.used\_​percentage

</td><td>

disk-name

</td><td>

The percentage of space used on this disk

</td><td>

percent

</td><td>

yes

</td><td>

yes

</td></tr><tr><td rowspan="21">

os.linux.metrics-system-memoryos.​linux.metrics-system-​memory-percent

</td><td>

memory.total

</td><td>

empty

</td><td>

Total usable RAM.

</td><td>

KB

</td><td>

 

</td><td>

 

</td></tr><tr><td>

memory.free

</td><td>

empty

</td><td>

Total free RAM.

</td><td>

KB

</td><td>

 

</td><td>

 

</td></tr><tr><td>

memory.available

</td><td>

empty

</td><td>

An estimate of how much memory is available for starting new applications, without swapping.

</td><td>

KB

</td><td>

 

</td><td>

 

</td></tr><tr><td>

memory.buffers

</td><td>

empty

</td><td>

Temporary storage used for raw disk blocks.

</td><td>

KB

</td><td>

 

</td><td>

 

</td></tr><tr><td>

memory.cached

</td><td>

empty

</td><td>

In-memory cache for files read from disk \(the page cache\). Does not include mem\_swapcached.

</td><td>

KB

</td><td>

 

</td><td>

 

</td></tr><tr><td>

memory.swapTotal

</td><td>

empty

</td><td>

Total amount of swap space available.

</td><td>

KB

</td><td>

yes

</td><td>

yes

</td></tr><tr><td>

memory.swapFree

</td><td>

empty

</td><td>

Amount of swap space that is currently unused.

</td><td>

 

</td><td>

yes

</td><td>

yes

</td></tr><tr><td>

memory.dirty

</td><td>

empty

</td><td>

Memory which is waiting to get written back to the disk.

</td><td>

KB

</td><td>

 

</td><td>

 

</td></tr><tr><td>

memory.swapUsed

</td><td>

empty

</td><td>

The amount of swap space in use.

</td><td>

KB

</td><td>

yes

</td><td>

yes

</td></tr><tr><td>

memory.used

</td><td>

empty

</td><td>

The amount of RAM in use.

</td><td>

KB

</td><td>

 

</td><td>

 

</td></tr><tr><td>

memory.​usedWOBuffersCaches

</td><td>

empty

</td><td>

The amount of memory in use.

</td><td>

KB

</td><td>

 

</td><td>

 

</td></tr><tr><td>

memory.​freeWOBuffersCaches

</td><td>

empty

</td><td>

Value of MemAvailable from /proc/meminfo if present, but falls back to adding free + buffered + cached memory if not.

</td><td>

KB

</td><td>

 

</td><td>

 

</td></tr><tr><td>

memory.​swapUsedPercentage

</td><td>

empty

</td><td>

Percent of swap space used.

</td><td>

percent

</td><td>

 

</td><td>

 

</td></tr><tr><td>

memory\_percent.​free

</td><td>

empty

</td><td>

Percent of free RAM

</td><td>

percent

</td><td>

yes

</td><td>

yes

</td></tr><tr><td>

memory\_percent.​available

</td><td>

empty

</td><td>

Percent of Mem available

</td><td>

percent

</td><td>

yes

</td><td>

yes

</td></tr><tr><td>

memory\_percent.​buffers

</td><td>

empty

</td><td>

Precent of Memory used for raw disk blocks

</td><td>

percent

</td><td>

yes

</td><td>

yes

</td></tr><tr><td>

memory\_percent.​cached

</td><td>

empty

</td><td>

Percent of memory used for in-memory cache for files read from disk

</td><td>

percent

</td><td>

yes

</td><td>

yes

</td></tr><tr><td>

memory\_percent.​dirty

</td><td>

empty

</td><td>

Percent of memory waiting to get written back to the disk.

</td><td>

percent

</td><td>

yes

</td><td>

yes

</td></tr><tr><td>

memory\_percent.​swapUsed

</td><td>

empty

</td><td>

Percent of swap space used.

</td><td>

percent

</td><td>

yes

</td><td>

yes

</td></tr><tr><td>

memory\_percent.​usedWOBuffersCaches

</td><td>

empty

</td><td>

Percent of memory is being used

</td><td>

percent

</td><td>

yes

</td><td>

yes

</td></tr><tr><td>

memory\_percent.​freeWOBuffersCaches

</td><td>

empty

</td><td>

Percent of Memory available

</td><td>

percent

</td><td>

yes

</td><td>

yes

</td></tr><tr><td>

os.linux.metrics-​system-uptime

</td><td>

system.uptime\(sec\)

</td><td>

empty

</td><td>

The amount of time the system has been working and available.

</td><td>

sec

</td><td>

 

</td><td>

 

</td></tr><tr><td rowspan="118">

os.linux.metrics-​memory-vmstat

</td><td>

vmstat.nr\_free\_pages

</td><td>

empty

</td><td>

Pages that are currently unused by the system.

</td><td>

pages

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_alloc\_​batch

</td><td>

empty

</td><td>

pages allocated to other domains due to insufficient memory in each domain of each NUMA

</td><td>

pages

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_​inactive\_anon

</td><td>

empty

</td><td>

memory pages in each domain of each NUMA node that have not been accessed for a long time

</td><td>

pages

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_active\_​anon

</td><td>

empty

</td><td>

Anonymous virtual memory pages that have been recently used

</td><td>

KB

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_inactive\_​file

</td><td>

empty

</td><td>

The memory page corresponding to the file that has not been accessed for a long time in each domain of each NUMA.

</td><td>

KB

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_active\_​file

</td><td>

empty

</td><td>

The memory page corresponding to the file that has been accesseed recently .

</td><td>

pages

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_​unevictable

</td><td>

empty

</td><td>

The number of pages is in the unevictable \(non-\)LRU list

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_​mlock

</td><td>

empty

</td><td>

Pages mapped into a VM\_LOCKED VMA - are a class of unevictable pages.

</td><td>

pages

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_anon\_​pages

</td><td>

empty

</td><td>

Memory mapped pages that is not part of a file.

</td><td>

pages

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_​mapped

</td><td>

empty

</td><td>

The number of memory mapped pages.

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_file\_​pages

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_​dirty

</td><td>

empty

</td><td>

Pages waiting to be written to disk

</td><td>

pages

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_​writeback

</td><td>

empty

</td><td>

Pages currently being written to disk

</td><td>

pages

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_slab\_​reclaimable

</td><td>

empty

</td><td>

Pages from the kernel slab memory usage that can be reclaimed

</td><td>

pages

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_slab\_​unreclaimable

</td><td>

empty

</td><td>

Pages from the kernel slab memory usage that cannot be reclaimed

</td><td>

pages

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_page\_table\_​pages

</td><td>

empty

</td><td>

Pages allocated to page tables

</td><td>

pages

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_kernel\_​stack

</td><td>

empty

</td><td>

Amount of memory allocated to kernel stacks.

</td><td>

KB

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_unstable

</td><td>

empty

</td><td>

The number of unstable pages in each domain of each NUMA node

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_bounce

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_vmscan\_​write

</td><td>

empty

</td><td>

The number of dirty pages written back during a scan of LRU\(s\)

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_vmscan\_​immediate\_reclaim

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_writeback\_​temp

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_isolated\_​anon

</td><td>

empty

</td><td>

The number of anonymous memory pages isolated in each domain of each NUMA node

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_​isolated\_file

</td><td>

empty

</td><td>

The number of pages of file storage pages isolated in each domain of each NUMA node

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_shmem

</td><td>

empty

</td><td>

The number of shared memory pages

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_dirtied

</td><td>

empty

</td><td>

The number of dirty pages in each domain of each NUMA node

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_written

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.numa\_hit

</td><td>

empty

</td><td>

The number of pages that were successfully allocated to this node.

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.numa\_miss

</td><td>

empty

</td><td>

The number of pages that were allocated on this node because of low memory on the intended node.

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.numa\_​foreign

</td><td>

empty

</td><td>

The number of pages initially intended for this node that were allocated to another node instead.

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.numa\_​interleave

</td><td>

empty

</td><td>

The number of interleave policy pages successfully allocated to this node.

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.numa\_local

</td><td>

empty

</td><td>

The number of pages successfully allocated on this node, by a process on this node

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.numa\_other

</td><td>

empty

</td><td>

The number of pages allocated on this node, by a process on another node.

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.workingset\_​refault

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.workingset\_​activate

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.workingset\_​nodereclaim

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_anon\_transparent\_​hugepages

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_free\_cma

</td><td>

empty

</td><td>

Free continuous memory allocator pages in each domain of each NUMA

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_dirty\_​threshold

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.nr\_dirty\_​background\_threshold

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgpgin

</td><td>

empty

</td><td>

The number of pages brought in from disk

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgpgout

</td><td>

empty

</td><td>

The number of pages written out to disk

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pswpin

</td><td>

empty

</td><td>

The number of pages brought in from swap space

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pswpout

</td><td>

empty

</td><td>

The number of pages swapped out into swap space

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgalloc\_dma

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgalloc\_​dma32

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgalloc\_​normal

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgalloc\_​movable

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgfree

</td><td>

empty

</td><td>

The number of pages are free since last boot

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgactivat

</td><td>

empty

</td><td>

Number of page activations since last boot

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgdeactivate

</td><td>

empty

</td><td>

Number of page deactivations since last boot

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgfault

</td><td>

empty

</td><td>

Minor faults since last boot

</td><td>

pages

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgmajfault

</td><td>

empty

</td><td>

Major faults since last boot

</td><td>

pages

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pglazyfreed

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgrefill\_dma

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgrefill\_dma32

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgrefill\_normal

</td><td>

empty

</td><td>

Number of page refills since last boot

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgrefill\_​movable

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgsteal\_​kswapd\_dma

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgsteal\_​kswapd\_dma32

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgsteal\_​kswapd\_normal

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgsteal\_​kswapd\_movable

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgsteal\_​direct\_dma

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgsteal\_​direct\_dma32

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgsteal\_​direct\_normal

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgsteal\_​direct\_movable

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgscan\_​kswapd\_dma

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgscan\_​kswapd\_dma32

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgscan\_​kswapd\_normal

</td><td>

empty

</td><td>

Number of pages scanned by kswapd since boot

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgscan\_​kswapd\_movable

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgscan\_​direct\_dma

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgscan\_​direct\_dma32

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgscan\_​direct\_normal

</td><td>

empty

</td><td>

Number of pages reclaimed since boot

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgscan\_​direct\_movable

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgscan\_​direct\_throttle

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.zone\_​reclaim\_failed

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pginodesteal

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.slabs\_scanned

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.kswapd\_​inodesteal

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.kswapd\_low\_​wmark\_hit\_quickly

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.kswapd\_high\_​wmark\_hit\_quickly

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pageoutrun

</td><td>

empty

</td><td>

Number of times kswapd called page reclaim

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.allocstall

</td><td>

empty

</td><td>

Number of times page reclaim was called directly \(low memory\)

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgrotated

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.drop\_​pagecache

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.drop\_​slab

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.numa\_pte\_​updates

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.numa\_huge\_​pte\_updates

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.numa\_hint\_​faults

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.numa\_hint\_​faults\_local

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.numa\_pages\_​migrated

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgmigrate\_​success

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.pgmigrate\_fail

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.compact\_​migrate\_scanned

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.compact\_​free\_scanned

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.compact\_​isolated

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.compact\_​stall

</td><td>

empty

</td><td>

The number of times a process stalls to run memory compaction so that a huge page is free for use.

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.compact\_fail

</td><td>

empty

</td><td>

The number of times the system tries to compact memory but failed.

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.compact\_​success

</td><td>

empty

</td><td>

The number of times the system compacted memory and freed a huge page for use.

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.htlb\_buddy\_​alloc\_success

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.htlb\_buddy\_​alloc\_fail

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.unevictable\_​pgs\_culled

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.unevictable\_​pgs\_scanned

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.unevictable\_​pgs\_rescued

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.unevictable\_​pgs\_mlocked

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.unevictable\_​pgs\_munlocked

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.unevictable\_​pgs\_cleared

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.unevictable\_​pgs\_stranded

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.thp\_fault\_alloc

</td><td>

empty

</td><td>

The number of huge pages is successfully allocated to handle a page fault.

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.thp\_fault\_​fallback

</td><td>

empty

</td><td>

The number of page fault fails to allocate a huge page and instead falls back to using small pages.

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.thp\_collapse\_alloc

</td><td>

empty

</td><td>

The number of collapse of a range of pages into one huge page and then successfull allocation of a new huge page to store the data.

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.thp\_collapse\_​alloc\_failed

</td><td>

empty

</td><td>

The number of collapse of a range of pages into one huge page but failed the allocation.

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.thp\_split

</td><td>

empty

</td><td>

The number of split of a huge page into base pages

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.thp\_zero\_​page\_alloc

</td><td>

empty

</td><td>

The number of successful allocation of huge zero page

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.thp\_zero\_​page\_alloc\_failed

</td><td>

empty

</td><td>

The number of times the kernel failed to allocate huge zero page and falls back to using small pages.

</td><td>

count

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.balloon\_inflate

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.balloon\_​deflate

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

vmstat.balloon\_​migrate

</td><td>

empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td rowspan="3">

os.linux.metrics-process-status

</td><td>

proc.&lt;process&gt;.VmSize

</td><td>

process-name

</td><td>

The total amount of virtual memory used by the process

</td><td>

KB

</td><td>

 

</td><td>

 

</td></tr><tr><td>

proc.&lt;process&gt;.VmRSS

</td><td>

process-name

</td><td>

The non-swapped physical memory a process has used

</td><td>

KB

</td><td>

 

</td><td>

 

</td></tr><tr><td>

proc.&lt;process&gt;.VmSwap

</td><td>

process-name

</td><td>

The total amount of swap space used.

</td><td>

KB

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table>## Linux network monitoring checks

**Note:** When upgrading from an earlier version, manually add the checks in this table to the Linux metrics policy.

<table id="table_r45_msb_gvb"><thead><tr><th>

Type

</th><th>

Check

</th><th>

Description

</th><th>

Usage and usage example

</th><th>

Metrics collected

</th><th>

Featured Metric

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

os.linux.metrics-network-interface

</td><td>

Retrieves all network interface related metrics for Linux servers.

</td><td>

Usage:

-   -x, excludeinterface: List of interfaces to exclude \(comma separated\)
-   -i, includeinterface: List of interfaces to include \(comma separated\)
-   -I, includeinterfaceregex: Regex matching interfaces to include
-   -X, excludeinterfaceregex: Regex matching interfaces to exclude

 Usage example: `command: metrics-network-interface.rb`

</td><td>

-   rxBytes \(featured metric\)
-   rxPackets \(featured metric\)
-   rxErrors
-   rxDrops \(featured metric\)
-   rxFifo
-   rxFrame
-   rxCompressed
-   rxMulticast
-   rxBytes \(featured metric\)
-   rxPackets \(featured metric\)
-   rxErrors
-   rxDrops \(featured metric\)
-   rxFifo
-   rxColls
-   rxCarrier
-   rxCompressed

</td><td>

yes

</td></tr><tr><td>

Metric

</td><td>

os.linux.metrics-netstat-tcp

</td><td>

Retrieves metrics on TCP socket states from netstat. Useful on high-traffic web or proxy servers with large numbers of short-lived TCP connections coming and going.

</td><td>

Usage:

-   -p, port: The port from which you want to receive metrics. Value range = 1-65535.
-   -t, type: The port type from which to receive metrics. Values=local or remote. Default = local
-   -d, disabletcp6: Disables the tcp6 check. Enter a value to set disabletcp6 = true.

 Usage example: `metrics-netstat-tcp.rb`

</td><td>

-   tcp.UNKNOWN
-   tcp.ESTABLISHED
-   tcp.SYN\_SENT
-   tcp.SYN\_RECV
-   tcp.FIN\_WAIT1
-   tcp.FIN\_WAIT2
-   tcp.TIME\_WAIT
-   tcp.CLOSE
-   tcp.CLOSE\_WAIT
-   tcp.LAST\_ACK
-   tcp.LISTEN
-   tcp.CLOSING

</td><td>

no

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

