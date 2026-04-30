---
title: Linux log monitoring default checks and policies
description: Agent Client Collector provides the following policy for Linux log monitoring.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Linux log monitoring default checks and policies

Agent Client Collector provides the following policy for Linux log monitoring.

<table id="table_nrb_dv1_ktb"><thead><tr><th>

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

util.check-logs

</td><td>

Enables monitoring log files owned by a regular user.

</td><td>

Usage:-   -i --icase: Run a case insensitive match.
-   -c, --crit N: Critical level \(if pattern has a group\).
-   --encode-utf16u: Encode line with utf16 before matching.
-   -e, --encoding ENCODING-PAGE: Specific encoding page to read log file with.
-   -E, --exclude PAT: Pattern to exclude from matching.
-   -F, --filepattern FILE: Check a pattern of files, instead of one file. For REGEX, first test it on `https://rubular.com/` to get the expected outcomes and then pass it inside quotes as a parameter. For example, to get all **.log** extension files, pass `"(.)*\.log$"` as REGEX.

-   -f, --log-file FILE: Path to log file.
-   -l, --log-pattern PAT: Log format of each log entry:
-   -o, --warn-only Warn instead of critical on match.
-   -q, --pattern PAT Pattern to search for.To search for multiple patterns, separate each pattern with pipe\(\|\) and put inside quotes \(For example: "SEVERE\|404"\).
-   -r, --return: Return matched line.
-   -L, --return-length N: Matched line length.
-   -M, --return-error-limit N: Max number of returned matched lines\(log entries\).
-   -n, --name NAME Set state file dir automatically using name.
-   -s, --state\_dir DIR Dir to keep state files under.
-   -w, --warn N: Warning level if pattern has a groupWarning level if pattern has a group.

 Usage example: `command: check-log.rb -c 2 -w 1 -q "SEVERE|Exception" -s /tmp/cache/check-log -f /var/log/servicenow/agent-client-collector/acc.log`

</td><td>

CheckLog CRITICAL: 0 warnings, 8 criticals for pattern SEVERE\|Exception in log file /var/log/servicenow/agent-client-collector/acc.log

</td></tr><tr><td>

Event

</td><td>

util.check-logs-sudo

</td><td>

Enables monitoring log files owned by a root user.

</td><td>

Usage:-   -i --icase: Run a case insensitive match
-   -c, --crit N: Critical level \(if pattern has a group\)
-   --encode-utf16u: Encode line with utf16 before matching
-   -e, --encoding ENCODING-PAGE: Specific encoding page to read log file with.
-   -E, --exclude PAT Pattern to exclude from matching
-   -F, --filepattern FILE: Check a pattern of files, instead of one file. For REGEX, first test it on `https://rubular.com/` to get the expected outcomes and then pass it inside quotes as a parameter. For example, to get all **.log** extension files, pass `"(.)*\.log$"` as REGEX.

-   -f, --log-file FILE: Path to log file.
-   -l, --log-pattern PAT: Log format of each log entry:
-   -o, --warn-only Warn instead of critical on match
-   -q, --pattern PAT Pattern to search for.To search for multiple patterns, separate each pattern with pipe\(\|\) and put inside quotes \(for example: "SEVERE\|404"\)
-   -r, --return: Return matched line.
-   -L, --return-length N: Matched line length.
-   -M, --return-error-limit N: Max number of returned matched lines\(log entries\).
-   -n, --name NAME: Set state file dir automatically using name.
-   -s, --state\_dir DIR: Dir to keep state files under
-   -w, --warn N: Warning level if pattern has a groupWarning level if pattern has a group.

 Usage example: `command: check-log.rb -c 2 -w 1 -q "SEVERE|Exception" -s /tmp/cache/check-log -f /var/log/servicenow/agent-client-collector/acc.log`

</td><td>

CheckLog CRITICAL: 0 warnings, 8 criticals for pattern SEVERE\|Exception in log file /var/log/servicenow/agent-client-collector/acc.log

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

