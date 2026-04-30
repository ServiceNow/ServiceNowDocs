---
title: HTTP default checks and policies
description: Agent Client Collector provides the following policies for HTTP health monitoring. Policies come with the checks specified in the tables below.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# HTTP default checks and policies

Agent Client Collector provides the following policies for HTTP health monitoring. Policies come with the checks specified in the tables below.

<table id="table_x5c_gdf_ktb"><thead><tr><th>

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

util.check-http-follow-redirect

</td><td>

Verifies that redirection links can be followed in a set number of requests.

</td><td>

Usage check-head-redirect.rb \(options\):

-   -A, --auth-first-only: Use basic auth on first request only.
-   -aws-access-key-id: AWS Access Key. Either set ENV\["AWS\_ACCESS\_KEY\_ID"\] or provide it as an option on agent.
-   -r -aws-region: AWS Region \(defaults to us-east-1\).
-   --aws-secret-access-key: AWS Secret Access Key. Either set ENV\["AWS\_SECRET\_ACCESS\_KEY"\] or provide it as an option on agent.
-   -R --redirect: Follow first &lt;N&gt; redirects
-   -g --get-redirects: Follow first &lt;N&gt; redirects with GET requests.
-   -s, --s3-config-bucket: S3 config bucket to get configuration.
-   -k, --s3-config-key: S3 config key to get configuration.
-   -u, --url: URL needs to be updated in `Monitoring HTTP Entrypoint/cmdb_ci_endpoint_http_list.do` for the CI.

The Aws-region, aws-secret-key, aws-access-key ,s3-config, s3-config-key parameters are useful if you do not want to configure connection information in other check parameters. If a bucket and key have access to the environment in which the Sensu check executes in, provide an AWS key and token and the checks pull the specified JSON file from S3 and merge the JSON config into the current check configuration.

 Usage example: `command: check-head-redirect.rb -R 10 -u 'https://servicenow.com'`

</td><td>

Check Head Redirect OK

</td></tr><tr><td>

Event

</td><td>

util.check-http-response

</td><td>

Verifies URL response time and raises a CRITICAL/WARNING event if elapsed time exceeds provided CRITICAL/WARNING thresholds. Otherwise, it raises an OK event.

</td><td>

Usage: check-head-redirect.rb \(options\)

 -   -R, --redirect: Follow first &lt;N&gt; redirects.
-   -w --timeout\_warning: Set the timeout threshold for warning in milliseconds.
-   -c --timeout\_critical: Set the timeout threshold for critical in milliseconds.
-   -u, --url URL needs to be updated in `Monitoring HTTP Entrypoint/cmdb_ci_endpoint_http_list.do` for the CI.

 Usage example: `command: check-head-redirect.rb -R 10 -u 'https://servicenow.com' -w 3000 -c 5000`

</td><td>

Check Head Redirect OK

</td></tr></tbody>
</table><table id="table_gsx_r3f_ktb"><thead><tr><th>

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

Metric

</td><td>

util.metrics-http-curl

</td><td>

Retrieves metrics on HTTP endpoints using curl.This check requires a proxy agent.

</td><td>

Usage:

-   -a, --curl\_args "CURL ARGS": Additional arguments to pass to curl.
-   s, --scheme SCHEME: Metric naming scheme, text to append to metric \(Default: hostname\).
-   -u, --url: URL needs to be updated in `Monitoring HTTP Entrypoint/cmdb_ci_endpoint_http_list.do` for the CI.

 Usage example: `metrics-curl.rb -u myURL.com -a -Lk`

</td><td>

Check run successfully. Output: ws10.curl\_timings.time\_total 0.219622 1642749209

 ws10.curl\_timings.time\_namelookup 0.145494 1642749209

 ws10.curl\_timings.time\_connect 0.151103 1642749209

 ws10.curl\_timings.time\_pretransfer 0.168569 1642749209

 ws10.curl\_timings.time\_redirect 0.095899 1642749209

 ws10.curl\_timings.time\_starttransfer 0.219351 1642749209

 ws10.curl\_timings.http\_code 200 1642749209

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

