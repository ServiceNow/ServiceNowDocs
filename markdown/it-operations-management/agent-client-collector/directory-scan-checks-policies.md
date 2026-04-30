---
title: Directory Scan monitoring default checks and policies
description: The Agent Client Collector provides the following default checks and policies for Directory Scan monitoring.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Directory Scan monitoring default checks and policies

The Agent Client Collector provides the following default checks and policies for Directory Scan monitoring.

<table id="table_x53_1mq_12c"><thead><tr><th>

Type

</th><th>

Check

</th><th>

Description

</th><th>

Usage and Usage Example

</th><th>

Output

</th></tr></thead><tbody><tr><td>

Event

</td><td>

check-directory-file-count

</td><td>

Checks the number of files present in a given directory and compares it to the provided warning and critical thresholds. Returns a CRITICAL, WARNING, or OK event based on the critical and warning thresholds.

**Note:**

-   Counts the number of files inside the directory, not including files in subdirectories.
-   The agent requires read and execute permissions on the directory being monitored.

</td><td>

check-directory-file-count.rb \(options\)

-d, --dir Absolute path to the directory to count the files \(required\)

-w, --warning Warning threshold \(required\)

-c, --critical Critical threshold \(required\)

-H, include\_hidden\_files Set active to **true** to include hidden files while counting \(default is **false**\)

**Usage Example:**

`check-directory-file-count.rb -d /path/to/directory -w 50 -c 100`

</td><td>

DirectoryFileCount CRITICAL: &lt;path to dir&gt; has 165 files.

</td></tr><tr><td>

Event

</td><td>

check-directory-integrity

</td><td>

Compares the last modified time of the directory with the current time to determine if any updates have occurred within a defined time interval. Based on this comparison, the check returns a CRITICAL or OK event.

**Note:** The agent requires read and execute permissions on the directory being monitored.

</td><td>

commonchecks check-directory-integrity \(options\)

 -d, --dirpath DIRPATH: Absolute path to the directory to check \(required\).

 -i, --interval INTERVAL: Time interval in seconds to check for recent updates \(required\). Default value can be set to 180 seconds.

 **Usage example:**

 `commonchecks check-directory-update -d /path/to/directory -i 180`

</td><td>

Common Checks CRITICAL: Directory Integrity: CHANGES DETECTED for &lt;path to file&gt; within the last 180 seconds \(Last Modified: Wed, 04 Dec 2024 12:18:55 EST\).

</td></tr><tr><td>

Event

</td><td>

check-file-age

</td><td>

Evaluates the age of a specified file by comparing its last modification time with the current time. Raises an alert if the file exceeds the defined critical or warning age thresholds.

 **Note:** The agent requires read and execute permissions on the file being monitored.

</td><td>

commonchecks check-file-age \(options\)-f, --filepath FILEPATH: Absolute path to the file to check \(required\).

-c, --critical CRITICAL: Critical age threshold in minutes for the file \(required\).

-w, --warning WARNING: Warning age threshold in minutes for the file \(required\).

**Usage example:**`commonchecks check-file-age -f /path/to/file.txt -c 120 -w 60`

</td><td>

Common Checks OK: File &lt;path to file&gt; age: 30 minutes.

</td></tr><tr><td>

Event

</td><td>

check-file-response-time

</td><td>

Compares the time needed to read a specified file and compares it with the critical and warning thresholds. Based on this comparison, the check returns a CRITICAL or OK event.

**Note:** The agent requires read and execute permissions on the file being monitored.

</td><td>

commonchecks check-file-response-time \(options\)-f, --filepath FILEPATH: Absolute path to the file to check \(required\).

-c, --critical CRITICAL: Critical threshold in seconds for file response time \(required\).

-w, --warning WARNING: Warning threshold in seconds for file response time \(required\).

-t, --timeout TIMEOUT: Maximum time allowed for reading the file content, specified in seconds. Time out value must be greater than the critical threshold value.

**Usage example:**`commonchecks check-file-response-time -f /var/log/servicenow/agent-client-collector/acc.log -c 10 -w 5 -t 20`

</td><td>

Common Checks OK: File read response time: 0.0020 seconds for the file\_name: /var/log/servicenow/agent-client-collector/acc.log.

</td></tr><tr><td>

Event

</td><td>

check-file-size

</td><td>

Measures the size of a file \(the actual amount of data it contains\) and compares it against specified thresholds. Returns a CRITICAL, WARNING, or OK event based on the comparison of the file size and the thresholds.

 **Note:** The agent requires read and execute permissions on the file being monitored.

</td><td>

commonchecks check-file-size \(options\)-f, --filepath FILEPATH Absolute path to the required file \(required\).

-c, --critical CRITICAL. Critical threshold in kilobytes. Provide as a number without units \(for example, 1000 for 1000 KB\) \(required\)

-w, --warning WARNING. Warning threshold in kilobytes. Provide as a number without units \(for example, 500 for 500 KB\) \(required\)

**Usage example:**`commonchecks check-file-size -f C:\ProgramData\ServiceNow\agent-client-collector\config\acc.yml`

</td><td>

Common Checks OK: For File &lt;path to file&gt; size: 4.72 KB is within thresholds

</td></tr><tr><td>

Event

</td><td>

check-file-space

</td><td>

Measures the size of a file on disk against specified thresholds, returning a CRITICAL, WARNING, or OK event based on the thresholds.

 **Note:** The agent requires read and execute permissions on the file being monitored.

</td><td>

commonchecks check-file-space \(options\)-f, --filepath FILEPATH: Absolute path to the relevant file \(required\).

-c, --critical CRITICAL: Critical threshold in kilobytes. Provided as a number without units \(for example, 1000 for 1000 KB\) \(required\)

-w, --warning WARNING: Warning threshold in kilobytes. Provided as a number without units \(for example, 500 for 500 KB\) \(required\)

-b, --blocksize BLOCKSIZE: Block size in bytes \(Default = 4096\) \(required\)

**Usage example:**

`commonchecks check-file-space -f C:\ProgramData\ServiceNow\agent-client-collector\config\acc.yml`

</td><td>

Common Checks OK: File &lt;path to file&gt; space: 8.00 KB is within threshold

</td></tr><tr><td>

Event

</td><td>

os.windows.check-directory-space

</td><td>

Verifies the disk space occupied by a directory's content. Returns a CRITICAL, WARNING, or OK event, based on the comparison with the given critical and warning event severity thresholds.**Note:** The agent requires read and execute permissions on the directory being monitored.

</td><td>

winchecks check-dir-space \(options\)-d, --dirpath DIRPATH: Absolute path to the directory being checked \(required\).

-c, --critical CRITICAL: Critical disk space threshold in kilobytes \(required\).

-w, --warning WARNING: Warning disk space threshold in kilobytes \(required\).

-t, --timeout TIMEOUT: Maximum time allowed for directory size calculation, specified in seconds \(required\).

**Usage example:**`winchecks check-dir-space -d /path/to/directory -c 1000 -w 500 -t 120`

</td><td>

Windows Checks OK: Directory &lt;path to file&gt; space: 369.25 KB is within thresholds

</td></tr></tbody>
</table><table id="table_uky_x3w_12c"><thead><tr><th>

Type

</th><th>

Check

</th><th>

Description

</th><th>

Usage and Usage Example

</th><th>

Output

</th></tr></thead><tbody><tr><td>

Event

</td><td>

check-directory-file-count

</td><td>

Checks the number of files present in a given directory and compares it to the provided warning and critical thresholds. Returns a CRITICAL, WARNING, or OK event based on the critical and warning thresholds.

**Note:**

-   Counts the number of files inside the directory, not including files in subdirectories.
-   The agent requires read and execute permissions on the directory being monitored.

</td><td>

check-directory-file-count.rb \(options\)

-d, --dir Absolute path to the directory to count the files \(required\)

-w, --warning Warning threshold \(required\)

-c, --critical Critical threshold \(required\)

-H, include\_hidden\_files Set active to **true** to include hidden files while counting \(default is **false**\)

**Usage Example:**

`check-directory-file-count.rb -d /path/to/directory -w 50 -c 100`

</td><td>

DirectoryFileCount CRITICAL: &lt;path to dir&gt; has 165 files.

</td></tr><tr><td>

Event

</td><td>

check-directory-integrity

</td><td>

Compares the last modified time of the directory with the current time to determine if any updates have occurred within a defined time interval. Based on this comparison, the check returns a CRITICAL or OK event.

**Note:** The agent requires read and execute permissions on the directory being monitored.

</td><td>

commonchecks check-directory-integrity \(options\)

 -d, --dirpath DIRPATH: Absolute path to the directory to check \(required\).

 -i, --interval INTERVAL: Time interval in seconds to check for recent updates \(required\). Default value can be set to 180 seconds.

 **Usage example:**

 `commonchecks check-directory-update -d /path/to/directory -i 180`

</td><td>

Common Checks CRITICAL: Directory Integrity: CHANGES DETECTED for &lt;path to file&gt; within the last 180 seconds \(Last Modified: Wed, 04 Dec 2024 12:18:55 EST\).

</td></tr><tr><td>

Event

</td><td>

check-file-age

</td><td>

Evaluates the age of a specified file by comparing its last modification time with the current time. Raises an alert if the file exceeds the defined critical or warning age thresholds.

 **Note:** The agent requires read and execute permissions on the file being monitored.

</td><td>

commonchecks check-file-age \(options\)-f, --filepath FILEPATH: Absolute path to the file to check \(required\).

-c, --critical CRITICAL: Critical age threshold in minutes for the file \(required\).

-w, --warning WARNING: Warning age threshold in minutes for the file \(required\).

**Usage example:**`commonchecks check-file-age -f /path/to/file.txt -c 120 -w 60`

</td><td>

Common Checks OK: File &lt;path to file&gt; age: 30 minutes.

</td></tr><tr><td>

Event

</td><td>

check-file-response-time

</td><td>

Compares the time needed to read a specified file and compares it with the critical and warning thresholds. Based on this comparison, the check returns a CRITICAL or OK event.

**Note:** The agent requires read and execute permissions on the file being monitored.

</td><td>

commonchecks check-file-response-time \(options\)-f, --filepath FILEPATH: Absolute path to the file to check \(required\).

-c, --critical CRITICAL: Critical threshold in seconds for file response time \(required\).

-w, --warning WARNING: Warning threshold in seconds for file response time \(required\).

-t, --timeout TIMEOUT: Maximum time allowed for reading the file content, specified in seconds. Time out value must be greater than the critical threshold value.

**Usage example:**`commonchecks check-file-response-time -f /var/log/servicenow/agent-client-collector/acc.log -c 10 -w 5 -t 20`

</td><td>

Common Checks OK: File read response time: 0.0020 seconds for the file\_name: /var/log/servicenow/agent-client-collector/acc.log.

</td></tr><tr><td>

Event

</td><td>

check-file-size

</td><td>

Measures the size of a file \(the actual amount of data it contains\) and compares it against specified thresholds. Returns a CRITICAL, WARNING, or OK event based on the comparison of the file size and the thresholds.

 **Note:** The agent requires read and execute permissions on the file being monitored.

</td><td>

commonchecks check-file-size \(options\)-f, --filepath FILEPATH Absolute path to the required file \(required\).

-c, --critical CRITICAL. Critical threshold in kilobytes. Provide as a number without units \(for example, 1000 for 1000 KB\) \(required\)

-w, --warning WARNING. Warning threshold in kilobytes. Provide as a number without units \(for example, 500 for 500 KB\) \(required\)

**Usage example:**`commonchecks check-file-size -f C:\ProgramData\ServiceNow\agent-client-collector\config\acc.yml`

</td><td>

Common Checks OK: For File &lt;path to file&gt; size: 4.72 KB is within thresholds

</td></tr><tr><td>

Event

</td><td>

check-file-space

</td><td>

Measures the size of a file on disk against specified thresholds, returning a CRITICAL, WARNING, or OK event based on the thresholds.

 **Note:** The agent requires read and execute permissions on the file being monitored.

</td><td>

commonchecks check-file-space \(options\)-f, --filepath FILEPATH: Absolute path to the relevant file \(required\).

-c, --critical CRITICAL: Critical threshold in kilobytes. Provided as a number without units \(for example, 1000 for 1000 KB\) \(required\)

-w, --warning WARNING: Warning threshold in kilobytes. Provided as a number without units \(for example, 500 for 500 KB\) \(required\)

-b, --blocksize BLOCKSIZE: Block size in bytes \(Default = 4096\) \(required\)

**Usage example:**

`commonchecks check-file-space -f C:\ProgramData\ServiceNow\agent-client-collector\config\acc.yml`

</td><td>

Common Checks OK: File &lt;path to file&gt; space: 8.00 KB is within threshold

</td></tr><tr><td>

Event

</td><td>

os.linux.check-directory-size

</td><td>

Verifies the space allocated for a disk's directory and compares it against specified critical and warning thresholds.**Note:** The agent requires read and execute permissions on the directory being monitored.

</td><td>

linuxchecks check-directory-size \(options\)-d, --dirpath DIRPATH: Absolute path to the directory being checked \(required\).

-c, --critical CRITICAL: Critical disk space threshold in kilobytes \(required\).

-w, --warning WARNING: Warning disk space threshold in kilobytes \(required\).

-t, --timeout TIMEOUT: Maximum time allowed for directory size calculation, specified in seconds \(required\).

**Usage example:**`linuxchecks check-directory-size -d path/to/directory -c 100 -w 50 -t 30`

</td><td>

Linux Checks CRITICAL: Directory &lt;path to file&gt; size: 500.00 KB exceeds critical threshold 10.00 KB

</td></tr><tr><td>

Event

</td><td>

os.linux.check-directory-space

</td><td>

Verifies the disk space occupied by directory content. Returns a CRITICAL, WARNING, or OK event based on the comparison with the critical and warning thresholds.**Note:** The agent requires read and execute permissions on the directory being monitored.

</td><td>

linuxchecks check-directory-space \(options\)-d, --dirpath DIRPATH: Absolute path to the directory being checked \(required\).

-c, --critical CRITICAL: Critical disk space threshold in kilobytes \(required\).

-w, --warning WARNING: Warning disk space threshold in kilobytes \(required\).

-t, --timeout TIMEOUT: Maximum time allowed for directory size calculation, specified in seconds \(required\).

**Usage example:**`linuxchecks check-directory-space -d /path/to/directory -c 10 -w 5 -t 30`

</td><td>

Linux Checks CRITICAL: Directory &lt;path to file&gt; space: 374.00 KB exceeds critical threshold 10.00 KB

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

