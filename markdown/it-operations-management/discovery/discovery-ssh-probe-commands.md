---
title: SSH commands not requiring a privileged user during probe-based discovery
description: These tables display the SSH commands run by Discovery probes on target devices during horizontal discovery. These SSH commands don’t require elevated privileges to run.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
keywords: [SSH commands, probe commands, SSH probe commands, no elevated privileges]
breadcrumb: [SSHCommand probe, List of Discovery probes, Discovery probes and sensors, Discovery, ITOM Visibility, IT Operations Management]
---

# SSH commands not requiring a privileged user during probe-based discovery

These tables display the SSH commands run by Discovery probes on target devices during horizontal discovery. These SSH commands don’t require elevated privileges to run.

## Operating systems

For information on commands used by Service Mapping during the top-down discovery, see [Service Mapping commands requiring a privileged user](../../service-mapping/reference/r_CommandsnCredentials.md) and [Service Mapping commands not requiring a privileged user](../../service-mapping/reference/r_NonSudoCommands.md).

<table id="table_zzv_4md_11b"><thead><tr><th>

Command \(ECC queue name\)

</th><th>

Parameters

</th></tr></thead><tbody><tr><td>

`sh`

</td><td>

**variable**

</td></tr><tr><td>

`lsattr`

</td><td>

**-El sys0 -a modelname -F value**

</td></tr><tr><td>

`lslpp`

</td><td>

**-Lc**

</td></tr><tr><td>

`/etc/ifconfig`

</td><td>

**-au; netstat -in**

</td></tr><tr><td>

`instfix`

</td><td>

**-i \| grep AIX\_ML**

</td></tr><tr><td>

`oslevel`

</td><td>

**-r**

</td></tr><tr><td>

`echo `lsattr`

</td><td>

**-El sys0 -a systemid \| cut ...**

</td></tr><tr><td>

`rmsock`

</td><td>

 

</td></tr><tr><td>

`lsdev`

</td><td>

-   **-C -F 'name,status' -c memory\|grep '^mem'**
-   **-C -F 'name,status' -c processor -S a**

</td></tr><tr><td>

`ps`

</td><td>

**-aef -o "pid,ppid,args"**

</td></tr></tbody>
</table><table id="table_vs2_nqd_11b"><thead><tr><th>

Command \(ECC queue name\)

</th><th>

Parameters

</th></tr></thead><tbody><tr><td>

`arp`

</td><td>

**-n**

</td></tr><tr><td>

`bash`

</td><td>

**variable**

</td></tr><tr><td>

`cat`

</td><td>

-   **/sys/hypervisor/compilation/compiled\_by**
-   **/sys/devices/virtual/dmi/id/product\_uuid**
-   **/etc/\*release**
-   **/proc/cpuinfo**
-   **/var/lib/dpkg/status**
-   **/proc/mounts**
-   **/proc/scsi/scsi**
-   **/etc/iscsi/initiatorname.iscsi**
-   **/sys/hypervisor/compilation/compiled\_by**

</td></tr><tr><td>

`grep MemTotal`

</td><td>

**/proc/meminfo**

</td></tr><tr><td>

`ifconfig`

</td><td>

**-a &amp;&amp; route -n**

</td></tr><tr><td>

`sh`

</td><td>

**variable**

</td></tr><tr><td>

`rpm`

</td><td>

**-q -a --qf**

</td></tr><tr><td>

`ls`

</td><td>

-   **-d /sys/block/\* \| grep '^/sys/block/\\\(dm-\|sd\|sr\\\)'**
-   **/sys/class/scsi\_host/host\*/protocol 2&gt; /dev/null**
-   **/sys/class/scsi\_host/host\*/info 2&gt; /dev/null**
-   **-d /sys/class/fc\_host/host\***

</td></tr><tr><td>

`shopt`

</td><td>

**-s extglob**

</td></tr><tr><td>

`findmnt`

</td><td>

`-l -n -o SOURCE,TARGET 2>/dev/null`

</td></tr><tr><td>

`find`

</td><td>

**/sys/class/iscsi\_session -maxdepth 1 -type l**

</td></tr><tr><td>

`fcoeadm`

</td><td>

**-i**

</td></tr><tr><td>

`ip`

</td><td>

-   **neighbor 2&gt; /dev/null**
-   **address show &amp;&amp; ip route**

</td></tr><tr><td>

`hostname`

</td><td>

**-f 2&gt; /dev/null**

</td></tr><tr><td>

`dnsdomainname`

</td><td>

**2&gt; /dev/null**

</td></tr><tr><td>

`grep`

</td><td>

-   **^\[\[:space:\]\]\*domain /etc/resolv.conf**
-   **^\[\[:space:\]\]\*search /etc/resolv.conf**

</td></tr><tr><td>

`wget`

</td><td>

-   **--spider -t 1 -T 1**
-   **-qO-**

</td></tr><tr><td>

`curl`

</td><td>

**--connect-timeout 1**

</td></tr><tr><td>

`python`

</td><td>

**-c**

</td></tr><tr><td>

`sudo cat`

</td><td>

**/sys/devices/virtual/dmi/id/product\_uuid**

</td></tr></tbody>
</table><table id="table_q4l_hh3_11b"><thead><tr><th>

Command \(ECC queue name\)

</th><th>

Parameters

</th></tr></thead><tbody><tr><td>

`ps`

</td><td>

**-elx**

</td></tr><tr><td>

`echo itick_per_usec/D`

</td><td>

**\| adb -k /stand/vm...**

</td></tr><tr><td>

`sh`

</td><td>

**variable**

</td></tr><tr><td>

`model`

</td><td>

 

</td></tr><tr><td>

`uname`

</td><td>

-   **-i**
-   **-r**

</td></tr><tr><td>

`swlist`

</td><td>

**-l product \| grep -v 'PH..\_'**

</td></tr><tr><td>

`echo 'memory_installed_in_machine/D'`

</td><td>

**\| a...**

</td></tr><tr><td>

`netstat`

</td><td>

**-in \| grep -v Name**

</td></tr><tr><td>

`lanscan`

</td><td>

**-ia**

</td></tr><tr><td>

`typeset`

</td><td>

**-i2**

</td></tr><tr><td>

`ioscan`

</td><td>

**-fnkC processor \| grep PROCESSOR \| wc -l**

</td></tr></tbody>
</table><table id="table_ahg_yn3_11b"><thead><tr><th>

Command \(ECC queue name\)

</th><th>

Parameters

</th></tr></thead><tbody><tr><td>

`sh`

</td><td>

**variable**

</td></tr><tr><td>

`kstat`

</td><td>

**cpu\_info**

</td></tr><tr><td>

`pkginfo`

</td><td>

**-l \| egrep 'PKGINST\|NAME\|CATEGO...**

</td></tr><tr><td>

`prtconf`

</td><td>

-   **\| grep Memory**
-   **\| grep 'System Configuration:'**
-   **-pv 2&gt;/dev/null**

</td></tr><tr><td>

`ifconfig`

</td><td>

**-a; netstat -pnr -f inet**

</td></tr><tr><td>

`arp`

</td><td>

**-an**

</td></tr><tr><td>

`showrev`

</td><td>

**-p**

</td></tr><tr><td>

`sneep`

</td><td>

**-T**

</td></tr><tr><td>

`bash`

</td><td>

**variable**

</td></tr><tr><td>

`pkg`

</td><td>

**list**

</td></tr><tr><td>

`iostat`

</td><td>

**-En \| awk '/^c/'**

</td></tr><tr><td>

`zpool`

</td><td>

-   **list**
-   **status \| awk '$1 == "NAME", $1 == ""'**

</td></tr><tr><td>

`df`

</td><td>

**-k**

</td></tr><tr><td>

`fcinfo`

</td><td>

**hba-port**

</td></tr><tr><td>

`zonename`

</td><td>

 

</td></tr><tr><td>

`zoneadm`

</td><td>

 

</td></tr><tr><td>

`zonecfg`

</td><td>

**-z**

</td></tr><tr><td>

`hostid`

</td><td>

 

</td></tr><tr><td>

`uname`

</td><td>

**-r**

</td></tr><tr><td>

`nawk`

</td><td>

 

</td></tr><tr><td>

`ps`

</td><td>

-   **-o pid,ppid**
-   **-awwx**

</td></tr><tr><td>

`pfiles`

</td><td>

 

</td></tr></tbody>
</table><table id="table_t53_wbj_11b"><thead><tr><th>

Command \(ECC queue name\)

</th><th>

Parameters

</th></tr></thead><tbody><tr><td>

`system_profiler`

</td><td>

-   **SPHardwareDataType SPMemoryDataType -xml**
-   **SPSerialATADataType SPSASDataType SPFireWireDataType -xml**
-   **SPNetworkDataType -xml;ifconfig \| grep '\\Winet6\\W'**
-   **SPSoftwareDataType -xml**
-   **SPHardwareDataType -xml**
-   **SPApplicationsDataType -xml**

</td></tr><tr><td>

`last`

</td><td>

**\| grep -m 1 console**

</td></tr><tr><td>

`hostname`

</td><td>

**2&gt; /dev/null**

</td></tr><tr><td>

`grep`

</td><td>

-   **'^\[\\s\]\*domain' /etc/resolv.conf**
-   **'^\[\\s\]\*search' /etc/resolv.conf**

</td></tr></tbody>
</table><table id="table_wcv_11k_11b"><thead><tr><th>

Command \(ECC queue name\)

</th><th>

Parameters

</th></tr></thead><tbody><tr><td>

`ps`

</td><td>

-   **awwxo pid,ppid,command \| sed -n '/&lt;defunct&gt;/!p'**
-   **-ef**

</td></tr><tr><td>

`sh`

</td><td>

**variable**

</td></tr><tr><td>

`cat`

</td><td>

**variable**

</td></tr><tr><td>

`variable`

</td><td>

**-version**

</td></tr><tr><td>

`uname`

</td><td>

**-a**

</td></tr><tr><td>

`df`

</td><td>

**-kP**

</td></tr><tr><td>

`uptime;env`

</td><td>

**LC\_ALL=C date '+%a %b %e %H:%M %Z %Y'**

</td></tr><tr><td>

`echo`

</td><td>

**\\echo \`uname -I\` \`hostname\` \`uname -Iv\`.\`uname -Ir\` 2&gt;&amp;1\`\`**

</td></tr><tr><td>

`awk`

</td><td>

 

</td></tr><tr><td>

`grep`

</td><td>

 

</td></tr><tr><td>

`find`

</td><td>

 

</td></tr><tr><td>

`uuencode`

</td><td>

**-m**

</td></tr><tr><td>

`base64`

</td><td>

**-w 0**

</td></tr><tr><td>

`wc`

</td><td>

**-c**

</td></tr><tr><td>

`nohup`

</td><td>

 

</td></tr><tr><td>

`vmware`

</td><td>

**-v 2&gt;&amp;1**

</td></tr><tr><td>

`systemctl`

</td><td>

**status cloudian-s3 2&gt;&amp;1**

</td></tr></tbody>
</table>|Command \(ECC queue name\)|Parameters|
|--------------------------|----------|
|`echo`|**\\lshmc -V 2&gt;&amp;1\`\`**|

## Web servers

|Command \(ECC queue name\)|Parameters|
|--------------------------|----------|
|`sh`|**variable**|
|`httpd_command`|**-V**|

|Command \(ECC queue name\)|Parameters|
|--------------------------|----------|
|`sh`|**variable**|
|`cat`|**variable**|
|`find -L ${dirname}`|**-name web.xml -print 2&gt;/dev/null**|

<table id="table_czl_23j_11b"><thead><tr><th>

Command \(ECC queue name\)

</th><th>

Parameters

</th></tr></thead><tbody><tr><td>

`sh`

</td><td>

-   **get-nginxcfg**
-   **get-nginx-ver**

</td></tr></tbody>
</table>## Databases

|Command \(ECC queue name\)|Parameters|
|--------------------------|----------|
|`sh`|**variable**|
|`lsnrctl`|**status**|

|Command \(ECC queue name\)|Parameters|
|--------------------------|----------|
|`cat`|**variable**|
|`variable`|**-V**|

|Command \(ECC queue name\)|Parameters|
|--------------------------|----------|
|`cat`|**variable**|
|`sh`|**variable**|
|`variable`|**-lv \| grep ^$\{processID\}**|
|`echo`|**"version" \| hbase shell**|

## Applications

|Command \(ECC queue name\)|Parameters|
|--------------------------|----------|
|`sh`|**variable**|

|Command \(ECC queue name\)|Parameters|
|--------------------------|----------|
|`sh`|**variable**|
|`tmsh`|**show sys version 2&gt;&amp;1**|

|Command \(ECC queue name\)|Parameters|
|--------------------------|----------|
|`sh`|**variable**|
|`variable`|**-v**|

|Command \(ECC queue name\)|Parameters|
|--------------------------|----------|
|`find`|**-name web.xml -print**|
|`cat`|**variable**|

|Command \(ECC queue name\)|Parameters|
|--------------------------|----------|
|`sh`|**variable**|
|`virsh`|**Various capabilities**|

<table id="table_clg_bmn_s2c"><thead><tr><th>

Command \(ECC queue name\)

</th><th>

Parameters

</th></tr></thead><tbody><tr><td>

`puppet`

</td><td>

-   **--version**
-   **config print**

</td></tr><tr><td>

`hostname`

</td><td>

**--fqdn**

</td></tr></tbody>
</table>## Storage

|Command \(ECC queue name\)|Parameters|
|--------------------------|----------|
|`purehw`|**list --all --nvp --type ch**|
|`vxprint`|**-AQmb**|
|`vxdisk`|**path**|
|`sudo vxdisk`|**list \| awk 'NR &gt; 1'**|
|`pureblade`|**list 2&gt;&amp;1**|

**Parent Topic:**[SSHCommand probe](../concept/c_SSHCommandProbe.md)

**Related topics**  


[Discovery commands for probes and patterns](../concept/discovery-command-probe-pattern.md)

