---
title: vSphere metrics
description: The following table lists the metrics that are gathered as output from vSphere checks. Entries indicated as Featured metrics are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 15
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# vSphere metrics

The following table lists the metrics that are gathered as output from vSphere checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|net.broadcastRx.summation|network adapter|packets|Number of broadcast packets received.|
|net.broadcastTx.summation|network adapter|packets|Number of broadcast packets transmitted.|
|net.bytesRx.average|network adapter|KiB|Average amount of data received per second.|
|net.bytesTx.average|network adapter|KiB|Average amount of data transmitted per second.|
|net.droppedRx.summation|network adapter|packets|Number of received packets dropped.|
|net.droppedTx.summation|network adapter|packets|Number of transmitted packets dropped.|
|net.multicastRx.summation|network adapter|packets|Number of multicast packets received.|
|net.multicastTx.summation|network adapter|packets|Number of multicast packets transmitted.|
|net.packetsRx.summation|network adapter|packets|Number of packets received.|
|net.packetsTx.summation|network adapter|packets|Number of packets transmitted.|
|net.received.average|network adapter|KiB|Average rate at which data was received during the interval. This represents the bandwidth of the network.|
|net.transmitted.average|network adapter|KiB|Average rate at which data was transmitted during the interval. This represents the bandwidth of the network.|
|net.usage.average \(featured metric\)|network adapter|KiB|Network utilization \(combined transmit- and receive-rates\).|
|disk.maxTotalLatency.latest \(featured metric\)|drive|millisecond|Highest latency value across all disks used by the host.|
|disk.read.average|drive|KiB|Average number of kilobytes read from the disk each second.|
|disk.usage.average \(featured metric\)|drive|KiB|Aggregated disk I/O rate.|
|disk.usage.maximum|drive|KiB|Maximum disk I/O rate.|
|disk.usage.minimum|drive|KiB|Minimum disk I/O rate.|
|disk.write.average|drive|KiB|Average number of kilobytes written to the disk each second.|
|cpu.costop.summation|cpu-core|millisecond|Time the virtual machine is ready to run, but is unable to run due to co-scheduling constraints.|
|cpu.demand.average|cpu-core|megahertz|The amount of CPU resources a virtual machine would use if there were no CPU contention or CPU limit.|
|cpu.demandEntitlementRatio.latest|cpu-core|percent|CPU resource entitlement to CPU demand ratio.|
|cpu.entitlement.latest|cpu-core|megahertz|CPU resources devoted by the ESXi scheduler.|
|cpu.idle.summation|cpu-core|millisecond|Total time that the CPU spent in an idle state.|
|cpu.latency.average|cpu-core|percent|Percent of time the virtual machine is unable to run because it is contending for access to the physical CPU\(s\).|
|cpu.maxlimited.summation|cpu-core|millisecond|Time the virtual machine is ready to run, but is not running because it has reached its maximum CPU limit setting.|
|cpu.overlap.summation|cpu-core|millisecond|Time the virtual machine was interrupted to perform system services on behalf of itself or other virtual machines.|
|cpu.readiness.average|cpu-core|percent|Percentage of time that the virtual machine was ready, but could not get scheduled to run on the physical CPU.|
|cpu.ready.summation|cpu-core|millisecond|Milliseconds of CPU time spent in ready state.|
|cpu.run.summation|cpu-core|millisecond|Time the virtual machine is scheduled to run.|
|cpu.swapwait.summation|cpu-core|millisecond|CPU time spent waiting for swap-in.|
|cpu.system.summation|cpu-core|millisecond|Amount of time spent on system processes on each virtual CPU in the virtual machine.|
|cpu.usage.average \(featured metric\)|cpu-core|percent|Percentage of CPU capacity being used.|
|cpu.usagemhz.average|cpu-core|megahertz|CPU usage, as measured in megahertz.|
|cpu.used.summation|cpu-core|millisecond|Time accounted to the virtual machine. If a system service runs on behalf of this virtual machine, the time spent by that service \(represented by cpu.system\) should be charged to this virtual machine. If not, the time spent \(represented by cpu.overlap\) should not be charged against this virtual machine.|
|cpu.wait.summation \(featured metric\)|cpu-core|millisecond|Total CPU time spent in wait state.The wait total includes time spent the CPU Idle, CPU Swap Wait, and CPU I/O Wait states.|
|cpu.usage.vcpus.average|cpu-core|percent|Percentage of vcpus capacity being used.|
|cpu.utilization.average|cpu-core|percent|Percentage of CPU capacity being used.|
|mem.active.average|memory|KiB|Amount of memory that is actively used, as estimated by VMkernel based on recently touched memory pages.|
|mem.activewrite.average|memory|KiB|Estimate for the amount of memory actively being written to by the virtual machine.|
|mem.compressed.average|memory|KiB|Kilobytes of memory that have been compressed.|
|mem.compressionRate.average|memory|KiB|Rate of memory compression for the virtual machine.|
|mem.consumed.average|memory|KiB|Amount of host physical memory consumed by a virtual machine, host, or cluster.|
|mem.decompressionRate.average|memory|KiB|Rate of memory decompression for the virtual machine.|
|mem.entitlement.average|memory|KiB|Amount of host physical memory the virtual machine is entitled to, as determined by the ESX scheduler.|
|mem.granted.average|memory|KiB|Amount of host physical memory or physical memory that is mapped for a virtual machine or a host.|
|mem.latency.average|memory|KiB|Percentage of time the virtual machine is waiting to access swapped or compressed memory.|
|mem.llSwapInRate.average|memory|KiB|Rate at which memory is being swapped from host cache into active memory.|
|mem.llSwapOutRate.average|memory|KiB|Rate at which memory is being swapped from active memory to host cache.|
|mem.llSwapUsed.average|memory|KiB|Space used for caching swapped pages in the host cache.|
|mem.overhead.average|memory|KiB|Host physical memory consumed by the virtualization infrastructure for running the virtual machine.|
|mem.overheadMax.average|memory|KiB|Host physical memory reserved for use as the virtualization overhead for the virtual machine.|
|mem.overheadTouched.average|memory|KiB|Actively touched overhead host physical memory \(KB\) reserved for use as the virtualization overhead for the virtual machine.|
|mem.shared.average|memory|KiB|Amount of guest physical memory that is shared with other virtual machines, relative to a single virtual machine or to all powered-on virtual machines on a host.|
|mem.usage.average \(featured metric\)|memory|percent|Memory usage as percent of total configured or available memory.|
|mem.vmmemctl.average|memory|KiB|Amount of memory allocated by the virtual machine memory control driver.|
|mem.vmmemctltarget.average|memory|KiB|Target value set by VMkernal for the virtual machine's memory balloon size. In conjunction with vmmemctl metric, this metric is used by VMkernel to inflate and deflate the balloon for a virtual machine.|
|mem.zero.average|memory|KiB|Memory that contains 0s only. Included in shared amount. Through transparent page sharing, zero memory pages can be shared among virtual machines that run the same operating system.|
|power.energy.summation|power|joule|Total energy \(in joule\) used since last stats reset.|
|power.power.average|power|watt|Current power usage.|
|sys.heartbeat.latest|system|number|Number of heartbeats issued per virtual machine.|
|sys.osUptime.latest|system|seconds|Total time elapsed, in seconds, since last operating system boot-up.|
|sys.uptime.latest|system|seconds|Total time elapsed since last system startup.|
|virtualDisk.read.average|virtual disk|KiB|Average number of kilobytes read from the virtual disk each second.|
|virtualDisk.write.average|virtual disk|KiB|Average number of kilobytes written to the virtual disk each second.|
|rescpu.actav1.latest|rescpu|percent|CPU active average over 1 minute.|
|rescpu.actav15.latest|rescpu|percent|CPU active average over 15 minutes.|
|rescpu.actav5.latest|rescpu|percent|CPU active average over 5 minutes.|
|rescpu.actpk1.latest|rescpu|percent|CPU active peak over 1 minute.|
|rescpu.actpk15.latest|rescpu|percent|CPU active peak over 15 minutes.|
|rescpu.actpk5.latest|rescpu|percent|CPU active peak over 5 minutes.|
|rescpu.runav1.latest|rescpu|percent|CPU running average over 1 minute.|
|rescpu.runav15.latest|rescpu|percent|CPU running average over 15 minutes.|
|rescpu.runav5.latest|rescpu|percent|CPU running average over 5 minutes.|
|rescpu.runpk1.latest|rescpu|percent|CPU running peak over 1 minute.|
|rescpu.runpk15.latest|rescpu|percent|CPU running peak over 15 minutes.|
|rescpu.runpk5.latest|rescpu|percent|CPU running peak over 5 minutes.|
|rescpu.sampleCount.latest|rescpu|millisecond|Group CPU sample count.|
|rescpu.samplePeriod.latest|rescpu|millisecond|Group CPU sample period.|

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|vmop.numChangeDS.latest|Virtual Machine Operations Counters|Number|Number of datastore change operations for powered-off and suspended virtual machines.|
|vmop.numChangeHost.latest|Virtual Machine Operations Counters|Number|Number of host change operations for powered-off and suspended virtual machines.|
|vmop.numChangeHostDS.latest|Virtual Machine Operations Counters|Number|Number of host and datastore change operations for powered-off and suspended virtual machines.|
|vmop.numClone.latest|Virtual Machine Operations Counters|Number|Number of virtual machine clone operations.|
|vmop.numCreate.latest \(featured metric\)|Virtual Machine Operations Counters|Number|Number of virtual machine create operations.|
|vmop.numDeploy.latest|Virtual Machine Operations Counters|Number|Number of virtual machine template deploy operations.|
|vmop.numDestroy.latest \(featured metric\)|Virtual Machine Operations Counters|Number|Number of virtual machine delete operations.|
|vmop.numPoweroff.latest|Virtual Machine Operations Counters|Number|Number of virtual machine power off operations.|
|vmop.numPoweron.latest|Virtual Machine Operations Counters|Number|Number of virtual machine power on operations.|
|vmop.numRebootGuest.latest \(featured metric\)|Virtual Machine Operations Counters|Number|Number of virtual machine guest reboot operations.|
|vmop.numReconfigure.latest|Virtual Machine Operations Counters|Number|Number of virtual machine reconfigure operations.|
|vmop.numRegister.latest|Virtual Machine Operations Counters|Number|Number of virtual machine register operations.|
|vmop.numReset.latest|Virtual Machine Operations Counters|Number|Number of virtual machine reset operations.|
|vmop.numSVMotion.latest|Virtual Machine Operations Counters|Number|Number of migrations with Storage vMotion \(datastore change operations for powered-on VMs\).|
|vmop.numShutdownGuest.latest|Virtual Machine Operations Counters|Number|Number of virtual machine guest shutdown operations.|
|vmop.numStandbyGuest.latest|Virtual Machine Operations Counters|Number|Number of virtual machine standby guest operations.|
|vmop.numSuspend.latest|Virtual Machine Operations Counters|Number|Number of virtual machine suspend operations.|
|vmop.numUnregister.latest|Virtual Machine Operations Counters|Number|Number of virtual machine unregister operations.|
|vmop.numVMotion.latest \(featured metric\)|Virtual Machine Operations Counters|Number|Number of migrations with vMotion \(host change operations for powered-on VMs\).|
|vmop.numXVMotion.latest|Virtual Machine Operations Counters|Number|Number of host and datastore change operations for powered-on and suspended virtual machines.|

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|datastore.busResets.summation|Datastore|Number|Number of SCSI-bus reset commands issued.|
|datastore.commandsAborted.summation|Datastore|Number|Number of SCSI commands aborted.|
|datastore.datastoreIops.average|Datastore|Number|Storage I/O Control aggregated IOPS.|
|datastore.datastoreMaxQueueDepth.latest|Datastore|Number|Storage I/O Control datastore maximum queue depth.|
|datastore.datastoreNormalReadLatency.latest|Datastore|millisecond|Storage DRS datastore normalized read latency.|
|datastore.datastoreNormalWriteLatency.latest|Datastore|millisecond|Storage DRS datastore normalized write latency.|
|datastore.datastoreReadBytes.latest|Datastore|millisecond|Storage DRS datastore bytes read.|
|datastore.datastoreReadIops.latest|Datastore|Number|Storage DRS datastore read I/O rate.|
|datastore.datastoreReadLoadMetric.latest|Datastore|Number|Storage DRS datastore metric for read workload model.|
|datastore.datastoreReadOIO.latest|Datastore|Number|Storage DRS datastore outstanding read requests.|
|datastore.datastoreVMObservedLatency.latest|Datastore|microsecond|The average datastore latency as seen by virtual machines.|
|datastore.datastoreWriteBytes.latest|Datastore|millisecond|Storage DRS datastore bytes written.|
|datastore.datastoreWriteIops.latest|Datastore|Number|Storage DRS datastore write I/O rate.|
|datastore.datastoreWriteLoadMetric.latest|Datastore|Number|Storage DRS datastore metric for write workload model.|
|datastore.datastoreWriteOIO.latest|Datastore|Number|Storage DRS datastore outstanding write requests.|
|datastore.maxTotalLatency.latest|Datastore|millisecond|Highest latency value across all datastores used by the host.|
|datastore.numberReadAveraged.average|Datastore|Number|Average number of read commands issued per second to the datastore.|
|datastore.numberWriteAveraged.average|Datastore|Number|Average number of write commands issued per second to the datastore during the collection interval.|
|datastore.read.average \(featured metric\)|Datastore|KiB|Rate of reading data from the datastore.|
|datastore.siocActiveTimePercentage.average \(featured metric\)|Datastore|percent|Percentage of time Storage I/O Control actively controlled datastore latency.|
|datastore.sizeNormalizedDatastoreLatency.average|Datastore|microsecond|Storage I/O Control size-normalized I/O latency.|
|datastore.throughput.contention.average|Datastore|millisecond|Average amount of time for an I/O operation to the datastore or LUN across all ESX hosts accessing it.|
|datastore.throughput.usage.average|Datastore|KiB|The current bandwidth usage for the datastore or LUN.|
|datastore.totalReadLatency.average|Datastore|millisecond|Average amount of time for a read operation from the datastore.|
|datastore.totalWriteLatency.average|Datastore|millisecond|Average amount of time for a write operation from the datastore.|
|datastore.unmapIOs.summation|Datastore|Number|Number of Unmap operations.|
|datastore.unmapSize.summation|Datastore|Number|Total UnMap size.|
|datastore.write.average \(featured metric\)|Datastore|KiB|Rate of writing data to the datastore.|
|disk.busResets.summation|disk|Number|Number of SCSI-bus reset commands issued.|
|disk.capacity.latest|disk|KiB|Configured size of the datastore.|
|disk.capacity.contention.average|disk|KiB|The amount of storage capacity overcommitment for the entity, measured in percent.|
|disk.capacity.provisioned.average|disk|KiB|Provisioned size of the entity.|
|disk.capacity.usage.average|disk|KiB|The amount of storage capacity currently being consumed by or on the entity.|
|disk.commands.summation|disk|Number|Number of SCSI commands issued.|
|disk.commandsAborted.summation|disk|Number|Number of SCSI commands aborted.|
|disk.commandsAveraged.average|disk|Number|Average number of SCSI commands issued per second.|
|disk.deltaused.latest|disk|KiB|Storage overhead of a virtual machine or a datastore due to delta disk backings.|
|disk.deviceLatency.average|disk|millisecond|Average amount of time it takes to complete an SCSI command from physical device.|
|disk.deviceReadLatency.average|disk|millisecond|Average amount of time it takes to complete read from physical device.|
|disk.deviceWriteLatency.average|disk|millisecond|Average amount of time to write from the physical device.|
|disk.kernelLatency.average|disk|millisecond|Average amount of time spent by VMkernel to process each SCSI command.|
|disk.kernelReadLatency.average|disk|millisecond|Average amount of time spent by VMkernel to process each SCSI read command.|
|disk.kernelWriteLatency.average|disk|millisecond|Average amount of time spent by VMkernel to process each SCSI write command.|
|disk.maxQueueDepth.average \(featured metric\)|disk|Number|Maximum queue depth.|
|disk.maxTotalLatency.latest|disk|millisecond|Highest latency value across all disks used by the host.|
|disk.numberRead.summation|disk|Number|Number of disk reads during the collection interval.|
|disk.numberReadAveraged.average|disk|Number|Average number of read commands issued per second to the datastore.|
|disk.numberWrite.summation|disk|Number|Number of disk writes during the collection.|
|disk.numberWriteAveraged.average|disk|Number|Average number of write commands issued per second to the datastore.|
|disk.provisioned.latest|disk|KiB|Amount of storage set aside for use by a datastore or a virtual machine. Files on the datastore and the virtual machine can expand to this size but not beyond it.|
|disk.queueLatency.average|disk|millisecond|Average amount of time spent in VMkernel queue \(per SCSI command\).|
|disk.queueReadLatency.average \(featured metric\)|disk|millisecond|Average amount of time spent in the VMkernel queue per SCSI read command.|
|disk.queueWriteLatency.average|disk|millisecond|Average amount of time spent in the VMkernel queue per SCSI write command.|
|disk.read.average|disk|KiB|Average number of kilobytes read from the disk each second.|
|disk.scsiReservationCnflctsPct.average|disk|Number|Number of SCSI reservation conflicts for the LUN as a percent of total commands during the collection interval.|
|disk.scsiReservationConflicts.summation|disk|Number|Number of SCSI reservation conflicts for the LUN during the collection interval.|
|disk.throughput.contention.average|disk|millisecond|Average amount of time for an I/O operation to the datastore or LUN across all ESX hosts accessing it.|
|disk.throughput.usage.average|disk|KiB|The current bandwidth usage for the datastore or LUN.|
|disk.totalLatency.average \(featured metric\)|disk|millisecond|Average amount of time taken during the collection interval to process a SCSI command issued by the guest OS to the virtual machine.|
|disk.totalReadLatency.average|disk|millisecond|Average amount of time taken to process a SCSI read command issued from the guest OS to the virtual machine.|
|disk.totalWriteLatency.average|disk|millisecond|Average amount of time taken to process a SCSI write command issued by the guest OS to the virtual machine.|
|disk.unshared.latest|disk|KiB|Amount of space associated exclusively with a virtual machine.|
|disk.usage.average \(featured metric\)|disk|KiB|Aggregated disk I/O rate.|
|disk.used.latest|disk|KiB|Amount of space actually used by the virtual machine or the datastore. May be less than the amount provisioned at any given time, depending on whether the virtual machine is powered-off, whether snapshots have been created or not, and other such factors.|
|disk.write.average|disk|KiB|Average number of kilobytes written to the disk each second.|

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|cpu.coreUtilization.average  \(featured metric\)|cpu-core|percent|CPU utilization of the corresponding core \(if hyper-threading is enabled\) as a percentage.|
|cpu.reservedCapacity.average|cpu-core|megahertz|Total CPU capacity reserved by virtual machines.|
|cpu.totalCapacity.average|cpu-core|megahertz|Total CPU capacity reserved by and available for virtual machines.|
|datastore.maxTotalLatency.latest|datastore|millisecond|Highest latency value across all datastores used by the host.|
|hbr.hbrDiskReadLatency.average|host-based replication|millisecond|Average Disk read latency.|
|hbr.hbrDiskStallLatency.average|host-based replication|millisecond|Average Disk stall latency.|
|hbr.hbrNetRx.average|host-based replication|KiB|Average amount of data received per second.|
|hbr.hbrNetTx.average|host-based replication|KiB|Average amount of data transmitted per second.|
|hbr.hbrNumVms.average|host-based replication|Number|Number of powered-on virtual machines running on this host that currently have host-based replication protection enabled.|
|mem.heap.average|memory|KiB|VMkernel virtual address space dedicated to VMkernel main heap and related data.|
|mem.heapfree.average|memory|KiB|Free address space in the VMkernel main heap.Varies based on number of physical devices and configuration options.|
|mem.llSwapIn.average|memory|KiB|Amount of memory swapped-in from host cache.|
|mem.llSwapOut.average|memory|KiB|Amount of memory swapped-out to host cache.|
|mem.lowfreethreshold.average|memory|KiB|Threshold of free host physical memory below which ESX/ESXi will begin reclaiming memory from virtual machines through ballooning and swapping.|
|mem.reservedCapacity.average|memory|MiB|Total amount of memory reservation used by powered-on virtual machines and vSphere services on the host.|
|mem.sharedcommon.average|memory|KiB|Amount of machine memory that is shared by all powered-on virtual machines and vSphere services on the host.|
|mem.state.latest|memory|KiB|One of four threshold levels representing the percentage of free memory on the host.|
|mem.swapin.average|memory|KiB|Amount of memory swapped-in from disk.|
|mem.swapinRate.average|memory|KiB|Rate at which memory is swapped from disk into active memory.|
|mem.swapout.average|memory|KiB|Amount of memory swapped-out to disk.|
|mem.swapoutRate.average|memory|KiB|Rate at which memory is being swapped from active memory to disk.|
|mem.swapused.average|memory|KiB|Amount of memory that is used by swap. Sum of memory swapped of all powered on VMs and vSphere services on the host.|
|mem.sysUsage.average|memory|KiB|Amount of host physical memory used by VMkernel for core functionality, such as device drivers and other internal uses. Does not include memory used by virtual machines or vSphere services.|
|mem.totalCapacity.average|memory|KiB|Total amount of memory reservation used by and available for powered-on virtual machines and vSphere services on the host.|
|mem.unreserved.average|memory|KiB|Amount of memory that is unreserved. Memory reservation not used by the Service Console, VMkernel, vSphere services and other powered on VMs user-specified memory reservations and overhead memory.|
|mem.vmfs.pbc.capMissRatio.latest  \(featured metric\)|memory|percent|Trailing average of the ratio of capacity misses to compulsory misses for the VMFS PB Cache.|
|mem.vmfs.pbc.overhead.latest|memory|KiB|Amount of VMFS heap used by the VMFS PB Cache.|
|mem.vmfs.pbc.size.latest|memory|MiB|Space used for holding VMFS Pointer Blocks in memory.|
|mem.vmfs.pbc.sizeMax.latest|memory|MiB|Maximum size the VMFS Pointer Block Cache can grow to.|
|mem.vmfs.pbc.workingSet.latest|memory|TiB|Amount of file blocks whose addresses are cached in the VMFS PB Cache.|
|mem.vmfs.pbc.workingSetMax.latest|memory|TiB|Maximum amount of file blocks whose addresses are cached in the VMFS PB Cache.|
|net.errorsRx.summation  \(featured metric\)|network adapter|Number|Number of packets with errors received.|
|net.errorsTx.summation  \(featured metric\)|network adapter|Number|Number of packets with errors transmitted.|
|net.unknownProtos.summation|network adapter|KiB|Number of frames with unknown protocol received.|
|power.powerCap.average|power|watt|Maximum allowed power usage.|
|rescpu.maxLimited1.latest|rescpu|percent|Amount of CPU resources over the limit that were refused, average over 1 minute.|
|rescpu.maxLimited15.latest|rescpu|percent|Amount of CPU resources over the limit that were refused, average over 15 minutes.|
|rescpu.maxLimited5.latest|rescpu|percent|Amount of CPU resources over the limit that were refused, average over 5 minutes.|
|storageAdapter.maxTotalLatency.latest  \(featured metric\)|storage adapter|millisecond|Highest latency value across all storage adapters used by the host.|
|storagePath.maxTotalLatency.latest  \(featured metric\)|storage adapter|millisecond|Highest latency value across all storage paths used by the host.|

**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

