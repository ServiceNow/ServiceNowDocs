---
title: Red Hat OpenShift policies in DevOps Config
description: By default, the DevOps Config Policy content pack contains a set of policies to validate your Red Hat OpenShift configuration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/devops-family/devops-config-os-policies.html
release: zurich
product: DevOps \(Family\)
classification: devops-family
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [PaCE content, PaCE policies, PaCE content policies, DevOps Config policies, Default DevOps Config policies, PaCE default policies, DevOps Config Policy content pack]
breadcrumb: [Default DevOps Config policies, DevOps Config reference, DevOps Config, IT Service Management]
---

# Red Hat OpenShift policies in DevOps Config

By default, the DevOps Config Policy content pack contains a set of policies to validate your Red Hat OpenShift configuration.

**Important:** Starting with the Washington D.C. release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

You can use or customize these default DevOps Config policies to validate that your configuration data content is conformable, or administrate the full life cycle of PaCE policies.

**Note:** You can’t modify the default policies. However, you can make a copy of the policy and customize your copy.

<table id="table_gsp_4vm_nzb"><tbody><tr><td>

[A](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-family/devops-config-os-policies.md) \| [B](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-family/devops-config-os-policies.md) \| [C](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-family/devops-config-os-policies.md) \| [H](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-family/devops-config-os-policies.md) \| [N](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-family/devops-config-os-policies.md) \| [R](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-family/devops-config-os-policies.md) \| [S](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-family/devops-config-os-policies.md) \| [T](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-family/devops-config-os-policies.md)

</td></tr></tbody>
</table>## Audit Log Maximum Backup Is Set \(openshift\_audit\_log\_maxbackup\_is\_set\)

Checks whether the maximum number of old audit log files to be retained for API servers is set.

Results into a non-compliant status when the `--audit-log-maxbackup` argument is either not set or not within the specified limits.

-   **Input arguments**
    -   lowerLimit
        -   The lower limit of the `--audit-log-maxbackup` argument.
        -   Type: Integer
        -   Mandatory: False
    -   upperLimit
        -   The upper limit of the `--audit-log-maxbackup` argument.
        -   Type: Integer
        -   Mandatory: False

## Audit Log Maximum File Size Is Set \(openshift\_audit\_log\_maxsize\_is\_set\)

Checks whether the maximum file size specified as the rollover threshold for audit log files is set. After an audit log file reaches the maximum file size, the original audit log file is renamed and a new log file with the original name is created.

Results into a non-compliant status when the `--audit-log-maxsize` argument is either not set or not within the specified limits.

-   **Input arguments**
    -   lowerLimit
        -   The lower memory limit of the `--audit-log-maxsize` argument.
        -   Type: Integer
        -   Mandatory: True
    -   upperLimit
        -   The upper memory limit of the `--audit-log-maxsize` argument.
        -   Type: Integer
        -   Mandatory: True

## Audit Log Path Isn't Set \(openshift\_audit\_log\_path\_is\_not\_set\)

Checks whether the auditing is enabled in OpenShift and the audit log file path is set.

Results into a non-compliant status when either the `--audit-log-path` argument for openshift-kube-apiserver isn’t set to `/var/log/kube-apiserver/audit.log` or the `--audit-log-path` argument for openshift-apiserver isn’t set to `/var/log/openshift-apiserver/audit.log`.

## Basic Auth File Isn’t Set \(openshift\_basic\_auth\_file\_is\_not\_set\)

Checks whether OpenShift doesn’t use the basic authentication mechanism to authenticate requests to the API server.

Results into a non-compliant status when the `--basic-auth-file` argument is set.

## Containers Run Without Privilege Access \(openshift\_container\_is\_not\_privileged\)

Checks whether the containers within an OpenShift pod are run without privileged access.

Results into a non-compliant status when the privileged field for a container is set to `true`.

## Host PID Namespace Is Disabled \(openshift\_scc\_with\_hostPID\_namespace\_disabled\)

Checks whether there is at least one security context constraint \(SCC\) is defined that doesn’t allow containers to share the host PID namespace.

Results into a warning when there’s an SCC defined with the **allowHostPID** field set to `true`.

## NamespaceLifecycle Plugin Is Enabled \(openshift\_namespacelifecycle\_plugin\_is\_enabled\)

Checks whether the admission control plugin NamespaceLifecycle is enabled.

Results into a non-compliant status when the NamespaceLifecycle plugin is disabled.

## Read-Only Port Is Disabled \(openshift\_read\_only\_port\_disabled\)

Checks whether the Kubelet API server isn’t using the read-only port or the read-only port is set to `0`.

Results into a non-compliant status when the `kubelet-read-only-port` argument isn’t set to `0`.

## Request Timeout Is Set \(openshift\_request\_timeout\_is\_set\)

Checks whether the global request timeout for API servers is set.

Results into a non-compliant status when the `--min-request-timeout` argument is either not set or not within the specified limits.

-   **Input arguments**
    -   lowerLimit
        -   The lower limit of the `--min-request-timeout` argument.
        -   Type: Integer
        -   Mandatory: False
    -   upperLimit
        -   The upper limit of the `--min-request-timeout` argument.
        -   Type: Integer
        -   Mandatory: False

## Streaming Connections Timeout Isn't Disabled \(openshift\_streaming\_connections\_timeout\_not\_disabled\)

Checks whether the timeouts are set on streaming connections to ensure protection against denial-of-service attacks, inactive connections, and ephemeral ports exhaustion.

Results into a non-compliant status when the `streamingConnectionIdleTimeout` argument is set to `0` in the `Kubelet config` file.

## Token Auth File Isn’t Set \(openshift\_token\_auth\_file\_is\_not\_set\)

Checks whether OpenShift doesn't use a static token file to authenticate requests to the API server.

Results into a non-compliant status when the `--token-auth-file` argument is set.

