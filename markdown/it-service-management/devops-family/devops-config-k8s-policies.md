---
title: Kubernetes policies in DevOps Config
description: By default, the DevOps Config Policy content pack contains a set of policies to validate your Kubernetes configuration.
locale: en-US
release: zurich
product: DevOps \(Family\)
classification: devops-family
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [PaCE content, PaCE policies, PaCE content policies, DevOps Config policies, Default DevOps Config policies, PaCE default policies, DevOps Config Policy content pack]
breadcrumb: [Default DevOps Config policies, Reference, DevOps Config, IT Service Management]
---

# Kubernetes policies in DevOps Config

By default, the DevOps Config Policy content pack contains a set of policies to validate your Kubernetes configuration.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

You can use or customize these default DevOps Config policies to validate that your configuration data content is conformable, or [administrate the full life cycle of PaCE policies](https://www.servicenow.com/docs/access?context=pace-managing-policies&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

**Note:** You can’t modify the default policies. However, you can make a copy of the policy and customize your copy.

<table id="table_gsp_4vm_nzb"><tbody><tr><td>

[A](devops-config-k8s-policies.md#a) \| [B](devops-config-k8s-policies.md#b) \| [C](devops-config-k8s-policies.md#c) \| [D](devops-config-k8s-policies.md#d) \| [I](devops-config-k8s-policies.md#i) \| [K](devops-config-k8s-policies.md#k) \| [M](devops-config-k8s-policies.md#m) \| [N](devops-config-k8s-policies.md#n) \| [P](devops-config-k8s-policies.md#p) \| [R](devops-config-k8s-policies.md#r) \| [S](devops-config-k8s-policies.md#s) \| [T](devops-config-k8s-policies.md#t)

</td></tr></tbody>
</table>## Always Pull Images Admission Control Plugin Is Enabled \(container\_always\_pull\_images\_plugin\_is\_enabled\)

Checks whether the `AlwaysPullImages` admission controller plugin is enabled for the Kubernetes API server.

Results into a non-compliant status when the `AlwaysPullImages` plugin is not specified with the `--enable-admission-plugins` argument when using the `kube-apiserver` command.

## Basic Auth File Isn't Set \(container\_basic\_auth\_file\_is not\_set\)

Checks whether the Kubernetes API server is not using the basic user authentication mechanism.

Results into a non-compliant status when the `--basic-auth-file` argument is specified for a container when using the `kube-apiserver` command.

## Bind Address Isn't Set \(container\_bind\_address\_not\_set\_to\_localhost\)

Checks whether the bind address of the Kubernetes scheduler or Kubernetes controller manager is not `127.0.0.1`.

Results into a non-compliant status when the `--bind-address` argument is set to `127.0.0.1` for a container when using the `kube-controller-manager` or `kube-scheduler` command.

## Containers Don't Run With Low UID \(container\_uid\_minimum\_limit\)

Checks whether the UID of each container within a Kubernetes pod is greater than or equal to the specified minimum UID value.

Results into a non-compliant status if the UID defined for a container is less than the minimum UID value. If the UID is not defined for a container, the UID of the associated pod is validated.

-   **Input argument**

    min\_uid

    -   The minimum UID value required for the containers in a pod.
    -   Default value: `10000`
    -   Type: Integer
    -   Mandatory: False

## Containers Require Drop Capabilities \(container\_requires\_drop\_capabilities\)

Checks whether the drop capabilities are defined for containers within a Kubernetes pod.

Results into a non-compliant status when the drop capabilities for a container are not defined.

## Containers Run as a Non-Root User \(container\_run\_as\_nonroot\_user\)

Checks whether the containers within a Kubernetes pod run only as a non-root user to limit the exploitability of security misconfiguration and to restrict an attacker's possibilities in case of compromise.

Results into a non-compliant status when the `runAsNonRoot` key for a container is set to `false` or the user ID \(UID\) of a container is zero.

## Containers Run Without Privilege Access \(container\_is\_not\_privileged\)

Checks whether the containers within a Kubernetes pod are run without privileged access.

Results into a non-compliant status when the privileged field for a container is set to `true`.

## Containers Run Without Sys Admin Capability \(container\_is\_without\_sys\_admin\_capability\)

Checks whether the containers within a Kubernetes pod are run without the SYS\_ADMIN capability.

Results into a non-compliant status when the SYS\_ADMIN privileges are assigned to a container.

## CPU Requests Are Within Limits \(container\_cpu\_request\_within \_limits\)

Checks whether the containers within a Kubernetes pod are requesting the central processing unit \(CPU\) resources within the specified CPU limit.

Results into a non-compliant status when either the `limits.cpu` key is not defined or when the value of the `requests.cpu` key exceeds the value of the `limits.cpu` key.

## Docker Daemon Socket Isn't Exposed \(docker\_daemon\_socket\_not\_exposed\)

Checks whether the Docker daemon socket is not exposed to containers.

Results into a non-compliant status when the `hostPath.path` key for a volume is set to `/var/run/docker.sock`.

## Image Pull Policy Is Always \(container\_imagePullPolicy\_is\_always\)

Checks whether the `imagePullPolicy` field for each container within a Kubernetes pod is set to `Always`.

Results into a non-compliant status if the `imagePullPolicy` field is not defined or the `Always` criterion is not met.

## Insecure Bind Address Isn't Set \(container\_insecure\_bind\_address\_is\_not\_set\)

Checks whether the Kubernetes API server does not bind to an insecure address that otherwise could enable attackers to connect to the server over the insecure port and potentially read sensitive data in transit.

Results into a non-compliant status when the `insecure-bind-address` argument is specified when using the `kube-apiserver` command.

## Kubelet HTTPS Is True \(container\_kubelet\_https\_is\_true\)

Checks whether the connections between the Kubernetes API server and the kubelet use the HTTPS protocol to secure data transfer.

Results into a non-compliant status when the `-kubelet-https` argument is set to false when using the `kube-apiserver` command.

## Memory Requests Are Within Limits \(container\_memory\_request\_within \_limits\)

Checks whether the containers within a Kubernetes pod are consuming resources within the specified memory limit.

Results into a non-compliant status when either the `limits.memory` key is not defined or when the value of the `requests.memory` key exceeds the value of the `limits.memory` key.

## No Wildcard in the RBAC Rule \(rbac\_no\_wildcard\_in\_rule\)

Checks whether the Role and ClusterRole resources are not using wildcards to refer to objects or actions for role-based access control \(RBAC\) rule.

Returns into a non-compliant status when the wildcards are used in `apiGroups`, `resources`, or `verbs` for the RBAC rule.

## Privilege Escalation Not Allowed \(container\_privilege\_escalation\_not\_allowed\)

Checks whether the containers within a Kubernetes pod have less privileges than their parent process.

Results into a non-compliant status when the `allowPrivilegeEscalation` key for a container is either set to `true` or not defined.

## Root Containers Admitted \(container\_read\_only\_root\_file\_system\)

Checks whether the containers within a Kubernetes pod have the root file system set to read only.

Returns into a non-compliant status when the `readOnlyRootFilesystem` key for a container is not defined or set to `false`.

## Seccomp Profile Is Configured \(container\_seccomp\_profile\_is\_configured \)

Checks whether the containers within a Kubernetes pod are configured with a secure computing mode \(seccomp\) profile to restrict potentially dangerous system calls \(syscalls\).

Results into a non-compliant status when the `seccompProfile.type` key for a container is either not defined or set to a value other than `Localhost` or `RuntimeDefault`.

## Service Account Private Key File Is Specified \(container\_service\_account\_private\_key\_file\_is\_specified\)

Checks whether the `--service-account-private-key-file` argument is specified with the `kube-controller-manager` command for a container.

Results into a non-compliant status when the `--service-account-private-key-file` argument is not specified for a container when using the `kube-controller-manager` command.

## Secure Port Isn't Set to Zero \(container\_secure\_port\_not\_set\_to\_zero\)

Checks whether the Kubernetes API server is not using port `0` for the HTTPS authentication and authorization.

Results into a non-compliant status when the `--secure-port` argument is set to `0` for a container when using the `kube-apiserver` command.

## Token Auth File Isn't Set \(token\_auth\_file\_is\_not\_set\)

Checks whether the Kubernetes API server is not using a static token file for user authentication.

Results into a non-compliant status when the `token-auth-file` argument is specified when using the `kube-apiserver` command.

