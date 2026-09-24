---
title: Kubernetes discovery using patterns
description: The ServiceNow ITOM Visibility finds Kubernetes and OpenShift components using patterns and creates application services containing them. Discovery also finds Kubernetes events and frequently updates the CMDB to reflect the dynamic Kubernetes environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/kubernetes-discovery.html
release: brazil
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 36
keywords: [azure kubernetes, kubernetes cluster, get kubernetes config file, kubernetes mid server]
breadcrumb: [Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Kubernetes discovery using patterns

The ServiceNow ITOM Visibility finds Kubernetes and OpenShift components using patterns and creates application services containing them. Discovery also finds Kubernetes events and frequently updates the CMDB to reflect the dynamic Kubernetes environment.

Discovery uses the Kubernetes pattern and its extension sections to discover Kubernetes components:

-   The **Collect OpenShift info** extension section of the Kubernetes pattern discovers the OpenShift components of the Kubernetes deployment. The OpenShift Build Config extension section is available from Store version 1.0.53.
-   The **Service Mesh** extension discovers service mesh details. This information enables the pattern to create service-to-service relations, shown as Connects to::Connected. Service mesh discovery requires deploying Istio on your K8s \(Kubernetes\) cluster. The Service Mesh extension section is available from [Kubernetes extension classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/cmdb-ci-class-models-kubernetes.md). It’s supported on the ServiceNow AI Platform using the Madrid release or later.
-   The **Collect Container Repository** and extension section finds container registries and images in these registries.

Starting from Discovery and Service Mapping Patterns version 1.35.0, the Kubernetes Cluster - Per-Namespace LP pattern is available for large cluster discovery. For more information, see the **Large-payload Kubernetes discovery** section.

In addition, Discovery uses the Kubernetes Event pattern to discover events for Kubernetes components.

Starting from the 1.0.68 release on ServiceNow Store, Service Mapping can use CI relationships to add the Kubernetes components to application services during tag-based discovery.

Discovery uses the following patterns to discover the entire Kubernetes infrastructure deployed on GCP, AWS, and Azure:

-   Google Cloud Platform \(GCP\) – Get Kubernetes Clusters.
-   Amazon AWS Cloud - Get Kubernetes Clusters.
-   Microsoft Azure - Get Kubernetes Clusters.

These patterns query the Cloud, collect data on all Kubernetes clusters, and create a serverless schedule for each cluster. When the cluster is deleted, the schedule is marked as inactive. This feature eliminates the overhead of creating and managing multiple credentials and serverless discovery schedules per cluster. The Cloud infrastructure patterns are triggered through standard Cloud discovery.

Starting with Discovery and Service Mapping Patterns version 1.31.0, you can choose to discover Docker image CIs only, without discovering Docker container CIs. Check your entitlements to determine whether you have access to 2026 Packaging SKU. For more information, see [Disable Docker container CI discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/disable-docker-container-discovery.md).

## Supported versions

For the list of Kubernetes distribution versions validated against the Kubernetes and Kubernetes Event patterns, see [Kubernetes Versions Tested with ServiceNow Discovery \[KB3145280\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3145280).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Large-payload Kubernetes discovery

By default, Discovery uses the Kubernetes pattern to discover an entire cluster in a single execution. On large clusters, this can result in incomplete discovery data in the CMDB. The Kubernetes Cluster - Per-Namespace LP pattern is available as an alternative for large cluster environments, starting from Discovery and Service Mapping Patterns version 1.35.0.

The Kubernetes Cluster - Per-Namespace LP pattern identifies the cluster and then discovers each namespace separately, improving reliability on large clusters. The data collected and the CIs populated in the CMDB are identical between the two patterns. For configuration on on-premises clusters, see the **Prerequisites for on-premises Kubernetes discovery** section. For cloud clusters, see the prerequisites section for your cloud provider.

## General prerequisites for Kubernetes discovery

**Note:** For additional prerequisites for Kubernetes Cloud infrastructure discovery, see [below](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/kubernetes-discovery.md).

**Note:** Running automatic serverless Kubernetes schedules fetches the Bearer token. Adding credentials is unnecessary.

Perform the following steps so that Discovery can use the pattern to successfully find Kubernetes.

1.  Deploy the latest Discovery and Service Mapping Patterns application from ServiceNow Store.
2.  On the Kubernetes platform, find the parameters to set up Kubernetes discovery:
    -   Find the URL of the kubeapi server:
        1.  On the Kubernetes platform, run the following command:

            `kubectl cluster-info`

        2.  In the output, find the line that states the URL of the kubeapi server. For example, Kubernetes control plane is running at

            `https://10.154.144.146:443`

    -   Find the namespaces of the kubeapi server:
        1.  On the Kubernetes platform, run this command:

            `kubectl get namespaces`

        2.  In the output, find the line that states the namespaces. For example, `kube-system`.
    -   Find the Kubernetes username and password:
        1.  On the Kubernetes platform, run this command:

            `kubectl config view`

        2.  In the output, find the username and password.\[Omitted image "kubernetes-username-password.png"\] Alt text: Locate the lines that contain information on password and username.

            **Note:** If in a certain environment, `kubectl config view` command is not showing the expected details, use the `supported` command from the Kubernetes admin to fetch the user name and password details.

    -   Find the valid Bearer token with the proper permissions:
        -   If you know the default token name, use the command in the following format: `kubectl describe secret <default-token-token name>`.

            For example: `kubectl describe secret default-token-g6pwc`.

        -   If you don't know the default token name, use the command: `kubectl describe secret`.
3.  Verify that the API Server is reachable from the MID Server for successful Kubernetes discovery.
4.  Verify that the user configured on the Kubernetes platform has **GET** permissions to run the following /api/v1 elements:

    -   https://&lt;url&gt;/api/v1/namespaces/
    -   https://&lt;url&gt;/api/v1/namespaces/&lt;namespace&gt;
    -   https://&lt;url&gt;/api/v1/namespaces/kube-system/endpoints/kube-controller-manager
    -   https://&lt;url&gt;/api/v1/services
    -   https://&lt;url&gt;/api/v1/pods
    -   https://&lt;url&gt;/api/v1/nodes
    -   https://&lt;url&gt;/api/v1/replicationcontrollers
    -   https://&lt;url&gt;/apis/networking.k8s.io/v1/ingresses
    -   https://&lt;url&gt;/apis/apps/v1/deployments
    -   https://&lt;url&gt;/apis/apps/v1/statefulsets
    -   https://&lt;url&gt;/apis/apps/v1/daemonsets
    -   https://&lt;url&gt;/apis/apps/v1/replicasets
    -   https://&lt;url&gt;/apis/batch/v1/cronjobs
    -   https://&lt;url&gt;/apis/batch/v1/jobs
    **Note:** When using the **Kubernetes Cluster - Per-Namespace LP** pattern, verify your RBAC setup before switching. The LP pattern requires the same permissions listed above, but lists resources per namespace instead of cluster-wide. A ClusterRole with a ClusterRoleBinding covers all namespaces automatically and requires no changes. If you use namespace-scoped Role and RoleBinding objects, verify that a binding exists in each namespace that discovery will enumerate, because missing bindings could cause incomplete discovery for that namespace.

5.  To discover the OpenShift components of the Kubernetes deployment, verify that the user configured on the Kubernetes platform has **GET** permissions to run the following /api/v1 elements:

    -   /apis/apps.openshift.io/v1/deploymentconfigs
    -   ​/apis/build.openshift.io/v1/buildconfigs​
    -   /apis/route.openshift.io/v1/routes​
    -   /apis/user.openshift.io/v1/groups​
    -   /apis/user.openshift.io/v1/users​
    -   /apis/project.openshift.io/v1/projects​
    -   /apis/image.openshift.io/v1/images​
    -   /apis/image.openshift.io/v1/imagestreams
    To discover service mesh information:

    -   Deploy Istio on your K8s cluster.
    -   Provide the Prometheus URL.
    -   Configure Prometheus to scrape metrics from Istio.
6.  Activate **Get Kubernetes Config Files** extension to:

    -   Discover configuration files.
    -   Create tracked configuration files.
    -   Map the configuration files workloads and services with a relationship.
    **Note:** Tracked files content is in the JSON format from version 1.0.92. Tracked files content is in YAML format in version 1.0.91 and earlier.

7.  Create the Kubernetes credentials on the ServiceNow platform:
    1.  On the ServiceNow AI Platform, navigate to **All** &gt; **Discovery** &gt; **Credentials**.
    2.  Select **New**.
    3.  Select **Kubernetes Credentials**.
    4.  On the form, fill in the fields.

<table id="table_udg_p4h_hdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique and descriptive name for this credential.

</td></tr><tr><td>

User name

</td><td>

User name associated with this credential. Leading or trailing spaces should be avoided; if any are detected, a warning will appear. Only one authentication method should be used: either a user name and password or a Bearer token. Don't use both.

</td></tr><tr><td>

Password

</td><td>

Password associated with this credential. Only one authentication method should be used: either a user name and password or a Bearer token. Don't use both.

</td></tr><tr><td>

Bearer Token Authentication

</td><td>

This option enables advanced authentication using a Bearer token. When the check box is selected, the Bearer Token field is displayed.

</td></tr><tr><td>

Bearer Token

</td><td>

Discovery uses the Bearer token for advanced authentication when accessing Kubernetes. The Bearer token should be in BASE64 encoded format, using the character sequence as the token. For example: 31ada4fd-adec-460c-809a-9e56ceb75269.

Only one authentication method should be used: either a user name and password or a Bearer token. Don't use both.

</td></tr><tr><td>

Credential alias

</td><td>

An alias is configured to use the Kubernetes credential for devices and applications other than Kubernetes. This alias is also used when defining a serverless discovery schedule for discovering the Kubernetes deployment.1.  Select the padlock icon, and then select the search icon.
2.  On the Connection &amp; Credential Aliases form, select **New**.
3.  Specify a name for the credential alias record.
4.  Define attributes for the alias. Set the **Type** to `Credential`.
5.  Select and hold \(or right-click\) the form header and select **Save**, then select **Update**.
6.  On the Connection &amp; Credential Aliases form, select the newly added alias.

The alias appears in the Credential alias field.

</td></tr></tbody>
</table>    5.  On the Kubernetes credentials form, select **Update**.
8.  Create a serverless discovery schedule for the Kubernetes pattern.
    1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Schedules** and select **New**.
    2.  On the form, fill in the fields.

<table id="table_k8s_schedule_form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for this discovery schedule.

</td></tr><tr><td>

Discover

</td><td>

Scan type, which should be **Serverless**.

</td></tr><tr><td>

MID Server selection method

</td><td>

Select the method that Discovery uses to select a MID Server:-   `Specific MID Cluster`: Use a preconfigured cluster of MID Servers. The MID Server can’t be part of multiple clusters
-   `Specific MID Server`: Use only one MID Server. If that MID Server is part of a cluster, only that MID Server is used. The cluster isn’t used.


</td></tr><tr><td>

MID server

</td><td>

Name of the MID Server to use for this schedule. This field is available if **MID Server selection method** is set to `Specific MID Server`.

</td></tr><tr><td>

MID Server cluster

</td><td>

Name of the MID Server cluster to use for this schedule. This field is available if **MID Server selection method** is set to `Specific MID Cluster`.

</td></tr></tbody>
</table>    3.  Select **Submit**.
    4.  In the **Execution Patterns** related list, select **New**.
    5.  On the form, fill in the fields.

<table id="table_k8s_execution_pattern_form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name for this record.

</td></tr><tr><td>

Pattern

</td><td>

Pattern to use for this schedule: -   **Kubernetes**
-   **Kubernetes Cluster - Per-Namespace LP** \(starting from Discovery and Service Mapping Patterns version 1.35.0\)


</td></tr><tr><td>

Run Child Patterns

</td><td>

Enable this option if you selected **Kubernetes Cluster - Per-Namespace LP** as the pattern.

</td></tr></tbody>
</table>    6.  Select **Submit**.
    7.  In the **Pattern Launcher Parameters** related list, configure the parameters.

<table id="table_obc_k2z_3db"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

url

</td><td>

The identifier for the hostname, IP, or FQDN and the port of the Kubernetes apiserver. Use the following format: example\_hostname:example\_port or example\_ip:example\_port. Provide the correct protocol \(HTTP or HTTPS\) in the URL.

</td></tr><tr><td>

namespace

</td><td>

The namespaces that the system passes in the Kubernetes Discovery Configuration. Enter one of the following values:-   Individual namespace: enter the namespace and then "kube-system". For example: `dev,kube-system`
-   The default value: enter `default, kube-system`
-   Multiple namespaces: enter the namespaces, use a comma \(,\) to separate the values, and then enter "kube-system". For example: `automation,application,test,kube-system`
-   All namespaces: Use an asterisk \(\*\) to enter all namespaces


</td></tr><tr><td>

credentials alias

</td><td>

The alias associated with the previously created Kubernetes credentials.

</td></tr><tr><td>

cluster name

</td><td>

The name of the Kubernetes cluster, in the following format: &lt;serviceaccountid&gt;&lt;space&gt;&lt;clustername&gt;.

</td></tr><tr><td>

provider

</td><td>

The cloud provider or deployment type: -   For cloud hosted clusters: GCP, AWS, or Azure
-   For on-premises clusters: `OnPrem`


</td></tr><tr><td>

cluster\_resource\_id

</td><td>

Cluster resource ID example:-   Azure Kubernetes clusters - Resource ID.
-   AWS - cluster ARN.
-   GCP - cluster global name.


</td></tr><tr><td>

cluster\_uid\_cache

</td><td>

Internal parameter used by the **Kubernetes Cluster - Per-Namespace LP** pattern. Leave this value empty.

</td></tr></tbody>
</table>9.  Create a serverless discovery schedule for the Kubernetes Event pattern. Configure the schedule to run every 5 or 10 minutes.

    **Note:** When the pattern is run for the first time, it stores an event\_timestamp. Later on it collects only the delta events based on the timestamp. The more often the pattern is run, the fewer updates to the CMDB IRE are needed.

    Create a serverless execution pattern for the discovery schedule and assign it to the Kubernetes Events pattern. Configure the parameters required by the Kubernetes pattern as described in [Configuring execution pattern attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/kubernetes-discovery.md).

10. To include discovered components into service instances, enable CI relationships used in tag-based discovery by Service Mapping. These CI relationships are available from the 1.0.68 release on the ServiceNow Store. For operational steps, see [Tag-based discovery configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/service-mapping/tag_discovery_configuration.md).

## Additional prerequisites for Kubernetes Cloud infrastructure discovery

For the Google Cloud Platform \(GCP\) – Get Kubernetes Clusters pattern, perform the following:

1.  In the ServiceNow instance, set up a Google Cloud Platform \(GCP\) service account with valid credentials and permissions.
2.  On the GCP infrastructure, set up the MID Server with full access to all Cloud APIs: Set Cloud API access scopes to "Allow full access to all Cloud APIs". The MID Server instance can access only the Clusters specific to the project.
3.  Navigate to `sys_properties.list` and, using the admin role, configure the following properties:
    -   **sn\_itom\_pattern.k8s\_midserver**: Specify a valid MID Server or MID Server cluster name \(MID Server cluster support starting with Discovery and Service Mapping Patterns version 1.35.0\).

        **Note:** To target a specific service account or cluster, you can configure the **sn\_itom\_pattern.k8s\_&lt;service\_account\_id&gt;\_midserver** and the **sn\_itom\_pattern.k8s\_&lt;service\_account\_id&gt;\_&lt;clustername&gt;\_midserver** properties. The most specific property takes precedence.

    -   **sn\_itom\_pattern.k8s\_create\_schedule\_enabled**: Set the value to **true**.

        **Note:** Enabling the **sn\_itom\_pattern.k8s\_create\_schedule\_enabled** property automatically creates a serverless schedule for your cloud clusters, eliminating the need for manual scheduling. If you have an existing manual schedule and want to convert it to an automatic one, enable the property. Your manual schedule will be updated; no additional schedule will be created. An automatically created schedule has no "Max run time" defined.

    -   **sn\_itom\_pattern.k8s\_entry\_pattern**: To use the per-namespace large-payload \(LP\) discovery pattern, set the value to **Kubernetes Cluster - Per-Namespace LP** \(starting from Discovery and Service Mapping Patterns version 1.35.0\).
4.  Create and run Google Cloud Discovery

    **Note:**

    To fetch the Bearer token, while running GKE Kubernetes schedule, use the gcloud command:

    `gcloud config config-helper --format="value(credential.access_token)"`

    Configuring gcloud in the MID Server instance grants access to the GKE cluster to fetch the token.


For the Amazon Elastic Kubernetes Service \(EKS\) cluster discovery, perform the following:

1.  In the ServiceNow instance, set an AWS service account with valid management account credentials and permissions.
    1.  Verify that the Amazon Elastic Kubernetes Service \(EKS\) Cluster has a cluster role with the read-only access to all resources.
    2.  Create cluster role binding between the cluster role and a Kubernetes user. For example, read-onlyuser.
    3.  Create an AWS IAM role with the policy EKSReadOnly.
    4.  Associate the IAM role with the Kubernetes user in one of the following ways:
        -   In the cluster, edit the aws-auth ConfigMap.
        -   Run the command:

            `eksctl create iamidentitymapping --cluster yourClusterName --arnarn:aws:iam::yourAccountID:role/yourIAMRoleName --username read-only-user`

2.  Run Amazon Elastic Kubernetes Service \(EKS\) cluster discovery in one of two ways: Using the AWS Command Line Interface \(CLI\) or without using the AWS CLI. First, set the system property **sn\_itom\_pattern.k8s\_aws\_cli\_to\_generate\_token** to use the model you choose. This system property is set to **true** by default.

    -   Set this system property to **true** to use AWS CLI to generate a token.

    -   Set this system property to **false** to use Assume Roles to generate a token.

    1.  Run Amazon Elastic Kubernetes Service \(EKS\) cluster discovery using AWS CLI:

        1.  Set up the MID Server with the AWS CLI configured. Configuring AWS CLI credentials grants access to the Amazon Elastic Kubernetes Service \(EKS\) cluster.

            **Note:** The user logged in to the system must be the same as the MID Server user.

        2.  To generate the Bearer token, While running the Amazon Elastic Kubernetes Service \(EKS\) schedule, use the AWS CLI command:`aws eks get-token --cluster-name <cluster_name>`.

            Configuring the AWS CLI user/role in the MID Server instance grants access to the Amazon Elastic Kubernetes Service \(EKS\) cluster to generate the token.

    2.  Run Amazon Elastic Kubernetes Service \(EKS\) cluster discovery without using AWS CLI:

        **Note:**

        This feature is supported from Discovery and Service Mapping Patterns version 1.0.96 - December 2022.

        Refer to the following KB for detailed instructions: [KB1182188: EKS cluster discovery using STS AssumeRoles \(Without AWS CLI\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1182188)

3.  Navigate to `sys_properties.list` and, using the admin role, configure the following properties:
    -   **sn\_itom\_pattern.k8s\_midserver**: Specify a valid MID Server or MID Server cluster name \(MID Server cluster support starting with Discovery and Service Mapping Patterns version 1.35.0\).

        **Note:** To target a specific service account or cluster, you can configure the **sn\_itom\_pattern.k8s\_&lt;service\_account\_id&gt;\_midserver** and the **sn\_itom\_pattern.k8s\_&lt;service\_account\_id&gt;\_&lt;clustername&gt;\_midserver** properties. The most specific property takes precedence.

    -   **sn\_itom\_pattern.k8s\_create\_schedule\_enabled**: Set the value to **true**.

        **Note:** Enabling the **sn\_itom\_pattern.k8s\_create\_schedule\_enabled** property automatically creates a serverless schedule for your cloud clusters, eliminating the need for manual scheduling. If you have an existing manual schedule and want to convert it to an automatic one, enable the property. Your manual schedule will be updated; no additional schedule will be created. An automatically created schedule has no "Max run time" defined.

    -   **sn\_itom\_pattern.k8s\_entry\_pattern**: To use the per-namespace large-payload \(LP\) discovery pattern, set the value to **Kubernetes Cluster - Per-Namespace LP** \(starting from Discovery and Service Mapping Patterns version 1.35.0\).
4.  Create and run an AWS Cloud Discovery schedule.


For Microsoft Azure Kubernetes Services \(AKS\)- Kubernetes cluster discovery, perform the following:

1.  Update to the latest Discovery and Service Mapping Patterns version.
2.  In the ServiceNow instance, configure the Azure Service Account with valid Azure credentials and permission.
3.  Navigate to `sys_properties.list` and, using the admin role, configure the following properties:
    -   **sn\_itom\_pattern.k8s\_midserver**: Specify a valid MID Server or MID Server cluster name \(MID Server cluster support starting with Discovery and Service Mapping Patterns version 1.35.0\).

        **Note:** To target a specific service account or cluster, you can configure the **sn\_itom\_pattern.k8s\_&lt;service\_account\_id&gt;\_midserver** and the **sn\_itom\_pattern.k8s\_&lt;service\_account\_id&gt;\_&lt;clustername&gt;\_midserver** properties. The most specific property takes precedence.

    -   **sn\_itom\_pattern.k8s\_create\_schedule\_enabled**: Set the value to **true**.

        **Note:** Enabling the **sn\_itom\_pattern.k8s\_create\_schedule\_enabled** property automatically creates a serverless schedule for your cloud clusters, eliminating the need for manual scheduling. If you have an existing manual schedule and want to convert it to an automatic one, enable the property. Your manual schedule will be updated; no additional schedule will be created. An automatically created schedule has no "Max run time" defined.

        .

    -   **sn\_itom\_pattern.k8s\_entry\_pattern**: To use the per-namespace large-payload \(LP\) discovery pattern, set the value to **Kubernetes Cluster - Per-Namespace LP** \(starting from Discovery and Service Mapping Patterns version 1.35.0\).
4.  If you don't have local accounts with Kubernetes RBAC and want to improve pattern efficiency, navigate to **MID Server** &gt; **Properties** and set the **sn\_itom\_pattern.aks\_fetch\_local\_ad\_token** property to **false**.
5.  Run an Azure cloud discovery schedule.
6.  Configure the MID Server in the Discovery schedules according to the cluster account type. If you don't have Local accounts with RBAC, you can ignore this step.

<table id="table_pbp_dwy_zbc"><thead><tr><th>

Cluster account type

</th><th>

Discovery schedule MID Server

</th></tr></thead><tbody><tr><td>

MS Entra ID auth with Kubernetes RBAC.

</td><td>

Any MID Server.

</td></tr><tr><td>

MS Entra ID authentication with Azure RBAC.

</td><td>

Any MID Server.

</td></tr><tr><td>

Local accounts with Kubernetes RBAC.

</td><td>

Select the MID Server with the Azure Command Line Interface \(CLI\) configured. Configuring the Azure CLI credentials grants access to the AKS cluster.

 To fetch the Bearer token while running the AKS Kubernetes schedule, use the Azure CLI command: `az aks get-credentials --name <cluster_name> --overwrite-existing --resource-group <resourceGroup_name> --file -`.

</td></tr></tbody>
</table>    **Note:**

    -   The user logged in to the system must be the same as the MID Server user.
    -   For detailed information about AKS Cluster Discovery configuration, see the [AKS Cluster Discovery Configuration Details \[KB1220553\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1220553) article in the Now Support Knowledge Base.

<table id="table_qhn_ztd_x5b"><thead><tr><th>

 

</th><th>

Property name

</th><th>

Property description

</th><th>

Type

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

 

</td><td>

sn\_itom\_pattern.manifest\_digest\_image\_id

</td><td>

 

</td><td>

Boolean

</td><td>

false

 **Note:** Before setting this property to **true** and running discovery: avoid duplicate records from being created by deleting all Docker image records.

</td></tr><tr><td>

 

</td><td>

sn\_itom\_pattern.k8s\_create\_schedule\_enabled

</td><td>

The feature flag that can be enabled/disabled under the system properties, which is responsible to control the pattern execution. When enabled, it creates discovery schedules despite the new property value. An automatically created schedule has no "Max run time" defined.

</td><td>

Boolean

</td><td>

false

</td></tr><tr><td>

 

</td><td>

sn\_itom\_k8s\_run\_cloud\_discovery

</td><td>

When enabled, this property executes cloud Kubernetes patterns, discovering Kubernetes clusters without creating auto schedules.

</td><td>

Boolean

</td><td>

false

</td></tr><tr><td rowspan="5">

MID Server

</td><td>

sn\_itom\_pattern.k8s\_midserver\*

</td><td>

\[Default\]

 Example- Valid MID Server or MID Server cluster name \(MID Server cluster support starting with Discovery and Service Mapping Patterns version 1.35.0\). Applies to newly created discovery schedules only; existing schedules aren't updated.

</td><td>

String

</td><td>

 

</td></tr><tr><td>

sn\_itom\_pattern.k8s\_&lt;service\_account\_id&gt;\_midserver\*

</td><td>

\[Based on Service Account Level\]

 Example- Valid MID Server or MID Server cluster name \(MID Server cluster support starting with Discovery and Service Mapping Patterns version 1.35.0\).

</td><td>

String

</td><td>

 

</td></tr><tr><td>

sn\_itom\_pattern.k8s\_&lt;service\_account\_id&gt;\_&lt;clustername&gt;\_midserver\*

</td><td>

\[Based on Cluster name\]

 Example- Valid MID Server or MID Server cluster name \(MID Server cluster support starting with Discovery and Service Mapping Patterns version 1.35.0\).

</td><td>

String

</td><td>

 

</td></tr><tr><td>

sn\_itom\_pattern.kubernetes\_collect\_volume

</td><td>

When the property is set to **True**, the data for Kubernetes Volume \[cmdb\_ci\_kubernetes\_volume\] gets populated.

</td><td>

String

</td><td>

false

</td></tr><tr><td>

sn\_itom\_pattern.k8s\_add\_workload\_to\_image\_relation

</td><td>

Starting from Discovery and Service Mapping Patterns version 1.30.2, the Kubernetes patterns create an indirect-only relationship between Docker Image and workload CIs through Kubernetes Pods. Setting the property to true also creates direct relationships between Docker Image and the following workload CI types: Deployment, DaemonSet, ReplicaSet, StatefulSet, and ReplicationController.

</td><td>

Boolean

</td><td>

false

</td></tr><tr><td rowspan="3">

Credential Alias

</td><td>

sn\_itom\_pattern.k8s\_ cred\_alias

</td><td>

\[Default\]

 Example- credential alias name

</td><td>

String

</td><td>

 

</td></tr><tr><td>

sn\_itom\_pattern.k8s\_&lt;service\_account\_id&gt;\_alias

</td><td>

\[Based on Service Account Level\]

 Example- Valid credential alias name.

</td><td>

String

</td><td>

 

</td></tr><tr><td>

sn\_itom\_pattern.k8s\_&lt;service\_account\_id&gt;\_&lt;clustername&gt;\_alias

</td><td>

\[Based on Cluster name\]

 Example- Valid credential alias name.

</td><td>

String

</td><td>

 

</td></tr><tr><td rowspan="3">

Prometheus Url

</td><td>

sn\_itom\_pattern.k8s\_ prometheusUrl

</td><td>

\[Default\]

 Example- Valid Prometheus Url

</td><td>

String

</td><td>

 

</td></tr><tr><td>

sn\_itom\_pattern.k8s\_&lt;service\_account\_id&gt;\_prometheusUrl

</td><td>

\[Based on Service Account Level\]

 Example- Valid Prometheus Url

</td><td>

String

</td><td>

 

</td></tr><tr><td>

sn\_itom\_pattern.k8s\_&lt;service\_account\_id&gt;\_&lt;clustername&gt;\_prometheusUrl

</td><td>

\[Based on Cluster name\]

 Example- Valid Prometheus URL

</td><td>

String

</td><td>

 

</td></tr><tr><td>

 

</td><td>

sn\_itom\_pattern.k8s\_ run

</td><td>

\[Supported Discovery Schedule run- Daily, On Demand, Weekdays, Weekends, Month Last Day, Calendar Quarter End\]

 Example- Daily

</td><td>

String

</td><td>

 

</td></tr><tr><td>

 

</td><td>

sn\_itom\_pattern.k8s\_batch\_count

</td><td>

\[Refers how many schedules to run in batch – default set to 5\]

 Example- 5 \(Number of schedules to run in on batch\)

</td><td>

Integer

</td><td>

5

</td></tr><tr><td>

 

</td><td>

sn\_itom\_pattern.k8s\_schedule\_batch\_delay

</td><td>

\[keeps tracks of the time difference between two batches value contains in sec\]

 Example- 300 \(in seconds\)

</td><td>

Integer

</td><td>

 

</td></tr><tr><td>

 

</td><td>

sn\_itom\_pattern.k8s\_run\_time

</td><td>

\[keeps tracks of the current time for a batch\]

 If this property is set, then you can use the same or you can use the dynamic timing, which will be 5 min after the system current timing. Values contains in HH:MM:SS format

 Example- 10:11:12 \(HH:MM:SS \)

</td><td>

String

</td><td>

 

</td></tr><tr><td>

 

</td><td>

sn\_itom\_pattern.bring\_discovery\_container

</td><td>

Available starting with Discovery and Service Mapping Patterns version 1.31.0. This property controls whether the Kubernetes, Kubernetes Event, Docker Pattern, and Amazon AWS - ECS patterns discover both Docker container and Docker image CIs, or only Docker image CIs. Check your entitlements to determine whether you have access to 2026 Packaging SKU.

</td><td>

Boolean

</td><td>

true

</td></tr><tr><td>

 

</td><td>

sn\_itom\_pattern.k8s\_entry\_pattern

</td><td>

Controls which entry pattern Kubernetes cloud discovery uses. When set to **Kubernetes Cluster - Per-Namespace LP**, discovery identifies the cluster and then discovers each namespace separately, improving reliability on large clusters. The Kubernetes Cluster - Per-Namespace LP pattern is available starting from Discovery and Service Mapping Patterns version 1.35.0.

</td><td>

String

</td><td>

Kubernetes

</td></tr></tbody>
</table>\* If a MID Server and a MID Server cluster share the same name, the MID Server cluster takes precedence. **sn\_itom\_pattern.k8s\_&lt;service\_account\_id&gt;\_midserver** takes precedence over **sn\_itom\_pattern.k8s\_midserver** for that account. **sn\_itom\_pattern.k8s\_&lt;service\_account\_id&gt;\_&lt;clustername&gt;\_midserver** takes precedence over both for that account and cluster.

**Note:** `<service_account_id>` is the account ID name under Cloud Service Accounts. For more information, see: [Create Discovery schedules for cloud resources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/discovery-manager.md)

## Kubernetes Credential-less or mid-in-cluster discovery

Prerequisites for Kubernetes Credentials-less discovery:

Deploy the containerized MID Server to the Kubernetes cluster. Configuring Kubernetes credentials is unnecessary since the MID Server in Kubernetes cluster automatically discovers the API server and authenticate.

<table id="table_d3s_55j_x5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

URL

</td><td>

Enter any one the of following value in URL field:

 https://cluster

 Or

 https://kubernetes.default.svc

</td></tr><tr><td>

namespace

</td><td>

The namespaces that the system passes in the Kubernetes Discovery Configuration. Enter one of the following values:

 -   Individual namespace: enter the namespace and then "kube-system". For example: `dev,kube-system`
-   The default value. Enter:`default,kube-system`
-   Multipile namespaces: enter the namespaces, use a comma \(,\) to separate the values, and then enter "kube-system". For example: `automation,application,test,kube-system`
-   All namespaces: Use an asterisk \(\*\) to enter all namespaces.

</td></tr><tr><td>

cluster\_name

</td><td>

Enter Unique name.

</td></tr></tbody>
</table>## Data collected by Discovery during horizontal discovery

-   **Kubernetes pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the kube-controller-manager leader.|
    |Kubernetes UID \[k8s\_uid\]|The kube-system namespace UID \[supported versions: 1.0.92 and later\]|
    |IP Address \[ip\_address\]|The identifier for the host IP of the Kubernetes apiserver.|
    |Port \[port\]|The identifier for the Kubernetes apiserver port.|
    |Namespace \[namespace\]|This value shows the namespaces the system passed in the Kubernetes Discovery Configuration.|
    |Event Timestamp \[event\_timestamp\]|The timestamp of the latest event created on this Kubernetes cluster at the time of the discovery.|

    |Field|Description|
    |-----|-----------|
    |The virtual aspect of the Kubernetes node. Data relating to the physical aspect of the Kubernetes node is stored under Linux server.|
    |Name \[name\]|The name of the Kubernetes node. The format can be only the name of the machine or the full name consisting of the name and the hostname: `<name>.<hostname>`.|
    |Kubernetes UID \[k8s\_uid\]|The identifier for the Kubernetes node UUID.|
    |Kubernetes Cluster \[cluster\]|References the Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\] table.|
    |Operational status \[operational\_status\]|The operational status of the Kubernetes node.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the Kubernetes service.|
    |Selector \[selector\]|A comma delimited list of the label selectors specified in the Kubernetes configuration that are used to select target pods.|
    |Namespace \[namespace\]|The Kubernetes namespace to which this Kubernetes service belongs.|
    |Kubernetes UID \[k8s\_uid\]|The Kubernetes service UUID.|
    |Kubernetes Cluster \[cluster\]|References the Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\] table.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the Kubernetes pod.|
    |Kubernetes UID \[k8s\_uid\]|The Kubernetes pod UUID.|
    |Resource version \[resource\_version\]|The resource version of the Kubernetes pod.|
    |Namespace \[namespace\]|The Kubernetes namespace to which this Kubernetes pod belongs.|
    |Kubernetes Cluster \[cluster\]|References the Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\] table.|
    |State \[state\]|The Kubernetes pod status: Pending, Running, Succeeded, Failed, and Unknown.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the Kubernetes cronjob.|
    |Namespace \[namespace\]|The Kubernetes namespace to which this Kubernetes cronjob belongs.|
    |Kubernetes UID \[k8s\_uid\]|The Kubernetes cronjob UUID.|
    |Kubernetes Cluster \[cluster\]|References the Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\] table.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the Kubernetes job.|
    |Namespace \[namespace\]|The Kubernetes namespace to which this Kubernetes job belongs.|
    |Kubernetes UID \[k8s\_uid\]|The Kubernetes job UUID.|
    |Kubernetes Cluster \[cluster\]|References the Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\] table.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the Kubernetes daemonset.|
    |Namespace \[namespace\]|The Kubernetes namespace to which this Kubernetes daemonset belongs.|
    |Kubernetes UID \[k8s\_uid\]|The Kubernetes daemonset UUID.|
    |Kubernetes Cluster \[cluster\]|References the Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\] table.|
    |Pods Available \[pods\_avail\]|The number of available pods.|
    |Pods Failed \[pods\_failed\]|The number of pods in the Failed phase.|
    |Pods Running \[pods\_running\]|The number of pods in the Running phase.|
    |Pods Succeeded \[pods\_succeeded\]|The number of pods in the Succeeded phase.|
    |Pods Waiting \[pods\_waiting\]|The number of pods in the Waiting phase.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the Kubernetes ingress.|
    |Namespace \[namespace\]|The Kubernetes namespace to which this Kubernetes ingress belongs.|
    |Kubernetes UID \[k8s\_uid\]|The Kubernetes ingress UID.|
    |Kubernetes Cluster \[cluster\]|References the Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\] table.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the Kubernetes deployment.|
    |Namespace \[namespace\]|The Kubernetes namespace to which this Kubernetes deployment belongs.|
    |Kubernetes UID \[k8s\_uid\]|The Kubernetes deployment UID.|
    |Kubernetes Cluster \[cluster\]|References the Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\] table.|
    |Total Replicas \[total\_replicas\]|The number of replicas in this deployment.|
    |Desired Replicas \[desired\_replicas\]|The number of replicas in the desired phase.|
    |Available Replicas \[available\_replicas\]|The number of available replicas.|
    |Unavailable Replicas \[unavailable\_replicas\]|The number of replicas in the unavailable phase.|
    |Updated Replicas \[updated\_replicas\]|The number of updated replicas.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the Kubernetes replicaset.|
    |Namespace \[namespace\]|The Kubernetes namespace to which this Kubernetes replicaset belongs.|
    |Kubernetes UID \[k8s\_uid\]|The Kubernetes replicaset UID.|
    |Kubernetes Cluster \[cluster\]|References the Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\] table.|
    |Total Replicas \[total\_replicas\]|The number of replicas in this replicaset.|
    |Desired Replicas \[desired\_replicas\]|The number of replicas in the desired phase.|
    |Available Replicas \[available\_replicas\]|The number of available replicas.|
    |Unavailable Replicas \[unavailable\_replicas\]|The number of replicas in the unavailable phase.|
    |Updated Replicas \[updated\_replicas\]|The number of updated replicas.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the Kubernetes replication controller.|
    |Namespace \[namespace\]|The Kubernetes namespace to which this Kubernetes replication controller belongs.|
    |Kubernetes UID \[k8s\_uid\]|The Kubernetes replication controller UID.|
    |Kubernetes Cluster \[cluster\]|References the Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\] table.|
    |Total Replicas \[total\_replicas\]|The number of replicas in this replication controller.|
    |Desired Replicas \[desired\_replicas\]|The number of replicas in the desired phase.|
    |Available Replicas \[available\_replicas\]|The number of available replicas.|
    |Unavailable Replicas \[unavailable\_replicas\]|The number of replicas in the unavailable phase.|
    |Updated Replicas \[updated\_replicas\]|The number of updated replicas.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the Kubernetes statefulset.|
    |Namespace \[namespace\]|The Kubernetes namespace to which this Kubernetes statefulset belongs.|
    |Kubernetes UID \[k8s\_uid\]|The Kubernetes statefulset UID.|
    |Kubernetes Cluster \[cluster\]|References the Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\] table.|
    |Total Replicas \[total\_replicas\]|The number of replicas in this statefulset.|
    |Desired Replicas \[desired\_replicas\]|The number of replicas in the desired phase.|
    |Available Replicas \[available\_replicas\]|The number of available replicas.|
    |Unavailable Replicas \[unavailable\_replicas\]|The number of replicas in the unavailable phase.|
    |Updated Replicas \[updated\_replicas\]|The number of updated replicas.|

<table id="table_docker_container"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

The component that runs the docker image.

</td></tr><tr><td>

Container id \[container\_id\]

</td><td>

The unique identifier for the Kubernetes docker container.In cases where duplicate records are created, deduplication tasks appear once discovery runs. For information on how to resolve these tasks, see the [Making docker container identifier independent \[KB1443042\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1443042) article in the ServiceNow® Knowledge Base.

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |An executable package of an application and its related software that can be instantiated by a docker container.|
    |Image id \[image\_id\]|The identifier for the Kubernetes docker image.|
    |Name \[name\]|The name of the Kubernetes docker image.|

    |Field|Description|
    |-----|-----------|
    |The server that hosts the Kubernetes node.|
    |Name \[name\]|The name of the Linux server powering the Kubernetes node.|
    |Host name \[host\_name\]|The hostname of the Linux server.|
    |Operating System \[os\]|The operating system deployed on this Linux server.|
    |Kernel Release \[kernel\_release\]|The version of the Linux kernel operating system deployed on this Linux server.|
    |RAM \(MB\) \[ram\]|The size of RAM installed on this Linux server.|
    |IP Address \[ip\_address\]|The IP address of the Linux server.|
    |CPU type \[cpu\_type\]|The CPU architecture of the Linux server hosting the Kubernetes node.|
    |CPU count \[cpu\_count\]|The number of CPUs on the Linux server hosting the Kubernetes node.|
    |Serial number \[serial\_number\]|The serial number of the Linux server hosting the Kubernetes node.|

<table id="table_key_value"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

This configuration item contains Kubernetes labels. Labels are key/value pairs that are attached to objects, such as pods.

</td></tr><tr><td>

Key \[key\]

</td><td>

The key of the Kubernetes pod or Kubernetes service **Key Value** parameter.

</td></tr><tr><td>

Value \[value\]

</td><td>

The value of the Kubernetes pod or Kubernetes service **Key Value** parameter.

</td></tr><tr><td>

Configuration item \[configuration\_item\]

</td><td>

References one of the following CI tables, based on the key-value pair: -   Kubernetes DaemonSet \[cmdb\_ci\_kubernetes\_daemonset\]
-   Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]
-   Kubernetes Ingress \[cmdb\_ci\_kubernetes\_ingress\]
-   Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]
-   Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]
-   Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]
-   Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]
-   Kubernetes ReplicationController \[cmdb\_ci\_kubernetes\_replicationcontroller\]
-   Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]
-   Kubernetes StatefulSet \[cmdb\_ci\_kubernetes\_statefulset\]


</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Kubernetes UID \[k8s\_uid\]|The Kubernetes volume UUID.|
    |Mount Path \[mount\_path\]|The path for accessing this Kubernetes volume.|
    |Name \[name\]|The name of the Kubernetes volume.|
    |Namespace \[namespace\]|The Kubernetes namespace to which this Kubernetes volume belongs.|
    |Kubernetes Cluster \[cluster\]|The name of the cluster that contains this resource.|
    |Volume ID \[volume\_id\]|The ID of the Kubernetes volume.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the Kubernetes namespace.|
    |Kubernetes Cluster \[cluster\]|References the Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\] table.|
    |State \[state\]|The Kubernetes namespace phase: Active or Terminating.|

-   **Collect OpenShift info pattern extension**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the OpenShift deployment configuration.|
    |Namespace \[namespace\]|The name of the namespace containing the deployment configuration.|
    |Kubernetes UID \[k8s\_uid\]|The Kubernetes UID of this resource.|
    |Kubernetes Cluster \[cluster\]|References the Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\] table.|
    |Url \[url\]|The URL of the OpenShift deployed configuration, available only for Kubernetes versions earlier than 1.16.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the OpenShift build configuration.|
    |Namespace \[namespace\]|The name of the OpenShift namespace containing the build configuration.|
    |Kubernetes UID \[k8s\_uid\]|The Kubernetes UID of this resource.|
    |Url \[url\]|The URL of the OpenShift build configuration, available only for Kubernetes versions earlier than 1.16.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the OpenShift source image.|
    |To \[to\]|Related image.|
    |Parent ID \[parent\_id\]|The ID of the OpenShift source image.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the OpenShift route.|
    |Namespace \[namespace\]|The name of the namespace containing the OpenShift route.|
    |Kubernetes UID \[k8s\_uid\]|The Kubernetes UID of this resource.|
    |Kubernetes Cluster \[cluster\]|References the Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\] table.|
    |Url \[url\]|The URL of the OpenShift route, available only for Kubernetes versions earlier than 1.16.|
    |Host \[host\]|The target host of the OpenShift route.|
    |Port \[port\]|The target port of the OpenShift route.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the OpenShift group.|
    |Kubernetes UID \[k8s\_uid\]|The Kubernetes UID of this resource.|
    |Url \[url\]|The URL of the OpenShift group, available only for Kubernetes versions earlier than 1.16.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the OpenShift user.|
    |Kubernetes UID \[k8s\_uid\]|The Kubernetes UID of this resource.|
    |Url \[url\]|The URL of the OpenShift user, available only for Kubernetes versions earlier than 1.16.|
    |Full Name \[full\_name\]|The full name of the OpenShift user.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the OpenShift project.|
    |Kubernetes UID \[k8s\_uid\]|The Kubernetes UID of this resource.|
    |Url \[url\]|The URL of the OpenShift project, available only for Kubernetes versions earlier than 1.16.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the OpenShift image.|
    |Kubernetes UID \[k8s\_uid\]|The Kubernetes UID of this resource.|
    |Url \[url\]|The URL of the OpenShift image, available only for Kubernetes versions earlier than 1.16.|
    |Docker Image Metadata ID \[docker\_image\_metadata\_id\]|The ID of the docker image.|
    |Docker Image Metadata Parent ID \[docker\_image\_metadata\_parent\_id\]|The ID of the image parent.|
    |Architecture \[arch\]|The architecture of the image.|
    |Size \[size\]|The image size.|
    |Hostname \[hostname\]|The hostname related to the image.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the OpenShift image stream.|
    |Kubernetes UID \[k8s\_uid\]|The Kubernetes UID of this resource.|
    |Url \[url\]|The URL of the OpenShift image stream, available only for Kubernetes versions earlier than 1.16.|
    |Namespace \[namespace\]|The name of the namespace containing the OpenShift image stream.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the OpenShift docker image repository.|
    |Parent ID \[parent\_id\]|The ID of the parent system.|

<table id="table_openshift_key_value"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

This configuration item contains OpenShift labels. Labels are key/value pairs that are attached to objects, such as deployed configurations and routes.

</td></tr><tr><td>

Key \[key\]

</td><td>

The key of the OpenShift deployed configuration or route **Key Value** parameter.

</td></tr><tr><td>

Value \[value\]

</td><td>

The value of the OpenShift deployed configuration or route **Key Value** parameter.

</td></tr><tr><td>

Configuration item \[configuration\_item\]

</td><td>

References one of the following CI tables, based on the key-value pair: -   OpenShift Deployed Config \[cmdb\_ci\_openshift\_dep\_conf\]
-   OpenShift Route \[cmdb\_ci\_openshift\_route\]


</td></tr></tbody>
</table>-   **Collect Container Repository pattern extension**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the container repository.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the container repository entry.|
    |Category \[category\]|The category of the container repository entry.|


## Kubernetes deployment diagrams

The graphic illustrates CIs that are part of Kubernetes discovery.

**Note:** This Dependency Views map was simplified for clarity. Your Kubernetes deployments may contain many more CIs.

\[Omitted image "kubernetes-diagram.png"\] Alt text: Relationships between Kubernetes configuration items and Kubernetes workload tables

\[Omitted image "openshift-diagram.png"\] Alt text: Namespace contains OpenShift configuration items

## CI relationships and references created by the Kubernetes pattern

These relationships and references are created by the Kubernetes pattern. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Docker Container \[cmdb\_ci\_docker\_container\]|Runs on::Runs|Linux Server \[cmdb\_ci\_linux\_server\]\*|
|Docker Image \[cmdb\_ci\_docker\_image\]|Instantiates::Instantiated by|Docker Container \[cmdb\_ci\_docker\_container\]\*|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Ingress \[cmdb\_ci\_kubernetes\_ingress\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Cluster of::Cluster|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]\*|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]\*|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]\*|
|Kubernetes Cronjob \[cmdb\_ci\_kubernetes\_cronjob\]|Hosted on::Hosts|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes Cronjob \[cmdb\_ci\_kubernetes\_cronjob\]|Owns::Owned by|Kubernetes Job \[cmdb\_ci\_kubernetes\_job\]|
|Kubernetes DaemonSet \[cmdb\_ci\_kubernetes\_daemonset\]|Hosted on::Hosts|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes DaemonSet \[cmdb\_ci\_kubernetes\_daemonset\]|Instantiates::Instantiated by|Docker Image \[cmdb\_ci\_docker\_image\]|
|Kubernetes DaemonSet \[cmdb\_ci\_kubernetes\_daemonset\]|Instantiates::Instantiated by|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|
|Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]|Hosted on::Hosts|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]|Instantiates::Instantiated by|Docker Image \[cmdb\_ci\_docker\_image\]|
|Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]|Instantiates::Instantiated by|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|
|Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]|Owns::Owned by|Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]|
|Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]|Owns::Owned by|Kubernetes ReplicationController \[cmdb\_ci\_kubernetes\_replicationcontroller\]|
|Kubernetes Ingress \[cmdb\_ci\_kubernetes\_ingress\]|Instantiates::Instantiated by|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|
|Kubernetes Job \[cmdb\_ci\_kubernetes\_job\]|Hosted on::Hosts|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes Job \[cmdb\_ci\_kubernetes\_job\]|Instantiates::Instantiated by|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Contains::Contained by|Kubernetes Cronjob \[cmdb\_ci\_kubernetes\_cronjob\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Contains::Contained by|Kubernetes DaemonSet \[cmdb\_ci\_kubernetes\_daemonset\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Contains::Contained by|Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Contains::Contained by|Kubernetes Ingress \[cmdb\_ci\_kubernetes\_ingress\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Contains::Contained by|Kubernetes Job \[cmdb\_ci\_kubernetes\_job\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Contains::Contained by|Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Contains::Contained by|Kubernetes ReplicationController \[cmdb\_ci\_kubernetes\_replicationcontroller\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Contains::Contained by|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Contains::Contained by|Kubernetes StatefulSet \[cmdb\_ci\_kubernetes\_statefulset\]|
|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]|Hosted on::Hosts|Linux Server \[cmdb\_ci\_linux\_server\]\*|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Contains::Contained by|Docker Container \[cmdb\_ci\_docker\_container\]\*|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Contains::Contained by|Docker Image \[cmdb\_ci\_docker\_image\]\*|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Contains::Contained by|Kubernetes Volume \[cmdb\_ci\_kubernetes\_volume\]\*|
|Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]|Hosted on::Hosts|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]|Instantiates::Instantiated by|Docker Image \[cmdb\_ci\_docker\_image\]|
|Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]|Instantiates::Instantiated by|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|
|Kubernetes ReplicationController \[cmdb\_ci\_kubernetes\_replicationcontroller\]|Hosted on::Hosts|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes ReplicationController \[cmdb\_ci\_kubernetes\_replicationcontroller\]|Instantiates::Instantiated by|Docker Image \[cmdb\_ci\_docker\_image\]|
|Kubernetes ReplicationController \[cmdb\_ci\_kubernetes\_replicationcontroller\]|Instantiates::Instantiated by|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|
|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|Provided By::Provides|Kubernetes DaemonSet \[cmdb\_ci\_kubernetes\_daemonset\]|
|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|Provided By::Provides|Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]|
|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|Provided By::Provides|Kubernetes StatefulSet \[cmdb\_ci\_kubernetes\_statefulset\]|
|Kubernetes StatefulSet \[cmdb\_ci\_kubernetes\_statefulset\]|Hosted on::Hosts|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes StatefulSet \[cmdb\_ci\_kubernetes\_statefulset\]|Instantiates::Instantiated by|Docker Image \[cmdb\_ci\_docker\_image\]|
|Kubernetes StatefulSet \[cmdb\_ci\_kubernetes\_statefulset\]|Instantiates::Instantiated by|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|
|Linux Server \[cmdb\_ci\_linux\_server\]|Contains::Contained by|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]\*|
|Linux Server \[cmdb\_ci\_linux\_server\]|Managed by::Manages|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]\*|

\* These relationships are also created by the Kubernetes Event pattern.

<table id="table_ci_references_k8s"><thead><tr><th>

CI

</th><th>

Field

</th><th>

Referenced CI

</th></tr></thead><tbody><tr><td>

Container Environment Variables \[cmdb\_container\_environment\_variables\]

</td><td>

Configuration item \[configuration\_item\]

</td><td>

Docker Container \[cmdb\_ci\_docker\_container\]

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

Configuration item \[configuration\_item\]

</td><td>

References one of the following CI tables, based on the key-value pair:

 -   Kubernetes DaemonSet \[cmdb\_ci\_kubernetes\_daemonset\]
-   Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]
-   Kubernetes Ingress \[cmdb\_ci\_kubernetes\_ingress\]
-   Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]
-   Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]
-   Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]
-   Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]
-   Kubernetes ReplicationController \[cmdb\_ci\_kubernetes\_replicationcontroller\]
-   Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]
-   Kubernetes StatefulSet \[cmdb\_ci\_kubernetes\_statefulset\]

</td></tr><tr><td>

Kubernetes Cronjob \[cmdb\_ci\_kubernetes\_cronjob\]

</td><td>

Kubernetes Cluster \[cluster\]

</td><td>

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

</td></tr><tr><td>

Kubernetes DaemonSet \[cmdb\_ci\_kubernetes\_daemonset\]

</td><td>

Kubernetes Cluster \[cluster\]

</td><td>

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

</td></tr><tr><td>

Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]

</td><td>

Kubernetes Cluster \[cluster\]

</td><td>

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

</td></tr><tr><td>

Kubernetes Ingress \[cmdb\_ci\_kubernetes\_ingress\]

</td><td>

Kubernetes Cluster \[cluster\]

</td><td>

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

</td></tr><tr><td>

Kubernetes Job \[cmdb\_ci\_kubernetes\_job\]

</td><td>

Kubernetes Cluster \[cluster\]

</td><td>

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

</td></tr><tr><td>

Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]

</td><td>

Kubernetes Cluster \[cluster\]

</td><td>

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

</td></tr><tr><td>

Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]

</td><td>

Kubernetes Cluster \[cluster\]

</td><td>

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

</td></tr><tr><td>

Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]

</td><td>

Kubernetes Cluster \[cluster\]

</td><td>

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

</td></tr><tr><td>

Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]

</td><td>

Kubernetes Cluster \[cluster\]

</td><td>

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

</td></tr><tr><td>

Kubernetes ReplicationController \[cmdb\_ci\_kubernetes\_replicationcontroller\]

</td><td>

Kubernetes Cluster \[cluster\]

</td><td>

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

</td></tr><tr><td>

Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]

</td><td>

Kubernetes Cluster \[cluster\]

</td><td>

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

</td></tr><tr><td>

Kubernetes StatefulSet \[cmdb\_ci\_kubernetes\_statefulset\]

</td><td>

Kubernetes Cluster \[cluster\]

</td><td>

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

</td></tr><tr><td>

Kubernetes Volume \[cmdb\_ci\_kubernetes\_volume\]

</td><td>

Kubernetes Cluster \[cluster\]

</td><td>

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

</td></tr><tr><td>

Serial Number \[cmdb\_serial\_number\]

</td><td>

Configuration Item \[cmdb\_ci\]

</td><td>

Linux Server \[cmdb\_ci\_linux\_server\]

</td></tr></tbody>
</table>## CI relationships created by the Kubernetes cloud patterns

These additional relationships are created by the Google Cloud Platform \(GCP\) – Get Kubernetes Clusters, Amazon AWS Cloud - Get Kubernetes Clusters, and Microsoft Azure - Get Kubernetes Clusters patterns.

|CI|Relationship|CI|
|---|------------|---|
|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|

## CI relationships and references created by the Kubernetes extension sections

The following extension sections of the Kubernetes pattern identify additional relationships and references. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

-   **Collect OpenShift info**

    |CI|Relationship|CI|
    |---|------------|---|
    |Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|OpenShift Docker Image Repository \[cmdb\_ci\_openshift\_docker\_images\_repository\]|
    |Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|OpenShift Group \[cmdb\_ci\_openshift\_group\]|
    |Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|OpenShift Image \[cmdb\_ci\_openshift\_images\]|
    |Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|OpenShift Project \[cmdb\_ci\_openshift\_project\]|
    |Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|OpenShift Source2Image \[cmdb\_ci\_openshift\_source\_2\_image\]|
    |Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|OpenShift User \[cmdb\_ci\_openshift\_user\]|
    |Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Contains::Contained by|OpenShift Build Config \[cmdb\_ci\_openshift\_build\_conf\]|
    |Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Contains::Contained by|OpenShift Deployed Config \[cmdb\_ci\_openshift\_dep\_conf\]|
    |Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Contains::Contained by|OpenShift Image Stream \[cmdb\_ci\_openshift\_images\_stream\]|
    |Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Contains::Contained by|OpenShift Route \[cmdb\_ci\_openshift\_route\]|
    |Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|Provided By::Provides|OpenShift Deployed Config \[cmdb\_ci\_openshift\_dep\_conf\]|
    |OpenShift Build Config \[cmdb\_ci\_openshift\_build\_conf\]|Contains::Contained by|Tracked Configuration file \[cmdb\_ci\_config\_file\_tracked\]|
    |OpenShift Deployed Config \[cmdb\_ci\_openshift\_dep\_conf\]|Contains::Contained by|Tracked Configuration file \[cmdb\_ci\_config\_file\_tracked\]|
    |OpenShift Deployed Config \[cmdb\_ci\_openshift\_dep\_conf\]|Owns::Owned by|Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]|
    |OpenShift Deployed Config \[cmdb\_ci\_openshift\_dep\_conf\]|Owns::Owned by|Kubernetes ReplicationController \[cmdb\_ci\_kubernetes\_replicationcontroller\]|

<table id="table_sjm_vyf_pkc"><thead><tr><th>

CI

</th><th>

Field

</th><th>

Referenced CI

</th></tr></thead><tbody><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

Configuration item \[configuration\_item\]

</td><td>

References one of the following CI tables, based on the key-value pair:-   OpenShift Deployed Config \[cmdb\_ci\_openshift\_dep\_conf\]
-   OpenShift Route \[cmdb\_ci\_openshift\_route\]


</td></tr><tr><td>

OpenShift Deployed Config \[cmdb\_ci\_openshift\_dep\_conf\]

</td><td>

Kubernetes Cluster \[cluster\]

</td><td>

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

</td></tr><tr><td>

OpenShift Route \[cmdb\_ci\_openshift\_route\]

</td><td>

Kubernetes Cluster \[cluster\]

</td><td>

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

</td></tr></tbody>
</table>-   **Collect Container Repository**

    |CI|Relationship|CI|
    |---|------------|---|
    |Docker Image \[cmdb\_ci\_docker\_image\]|Provisioned From::Provisioned|Container Repository Entry \[cmdb\_ci\_container\_repository\_entry\]|
    |Container Repository Entry \[cmdb\_ci\_container\_repository\_entry\]|Hosted on::Hosts|Container Repository \[cmdb\_ci\_container\_repository\]|

-   **Istio Service Mesh**

    Prerequisites for Istio Service Mesh extension:

    -   Verify that Istio Service Mesh and Prometheus components are configured on the Kubernetes cluster.
    -   Verify that Prometheus discovers the service connection information using the `queryistio_requests_total` command.
    -   Verify that the application services are connected, and verify service-to-service traffic flow in Kiali graph.
    For more information on the Bookinfo application, see: [https://istio.io/latest/docs/examples/bookinfo/](https://istio.io/latest/docs/examples/bookinfo/)

    |CI|Relationship|CI|
    |---|------------|---|
    |Kubernetes Service \[cmdb\_ci\_kubernetes\_servi ce\]|Connects to::Connected by|Kubernetes Service \[cmdb\_ci\_kubernetes\_servi ce\]|


## Data collected by Service Mapping during tag-based discovery

Service Mapping uses tag-based discovery to create application service maps including the Kubernetes components. Service Mapping comes with the following preconfigured CI relationships used for tag-based discovery. These CI relationships are available from the 1.0.68 release on ServiceNow Store.

|CI|Relationship|CI|
|---|------------|---|
|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|Contained By::Contains|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|OpenShift Project \[cmdb\_ci\_openshift\_project\]|Contained by::Contains|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Contained by::Contains|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Cluster::Cluster of|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]​|Contains::Contained By|OpenShift Deployed Config \[cmdb\_ci\_openshift\_dep\_conf​\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]​|Contains::Contained By|OpenShift Build Config \[cmdb\_ci\_openshift\_build\_conf\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]​|Contains::Contained By|OpenShift Route \[cmdb\_ci\_openshift\_route\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]​|Contains::Contained By|OpenShift Image Stream \[cmdb\_ci\_openshift\_images\_stream\]|

## Kubernetes dashboard

After Discovery finishes discovering components of the Kubernetes deployment, you can navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Insights** and use the Kubernetes Explorer dashboard to view the Kubernetes environments and resources of your organization. To use the enhanced Kubernetes dashboard, verify you have Discovery Admin Workspace starting from version 1.3.1 \(August 2024 Store\). For more information about Kubernetes Explorer, see [Kubernetes Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-discovery-workspace/cloud-operations-workspace-kubernetes-dashboard.md).

## Troubleshooting

If the mapping process does not proceed as you expected, follow the following suggestions.

<table id="table_ggn_ypj_yhb"><thead><tr><th>

Symptom

</th><th>

Cause

</th><th>

Solution

</th></tr></thead><tbody><tr><td>

Discovery fails. The discovery message contains the information about an error caused by the REST timeout.

</td><td>

There are many CIs sending the REST call response in the deployment. The MID Server cannot process the REST call response without exceeding the time limit controlled by the **mid.sa.cloud.request\_timeout** parameter.

</td><td>

By default, the **mid.sa.cloud.request\_timeout** parameter is set to 30000 milliseconds. Increase the value of this parameter on the relevant MID Server and run discovery again.

**Note:** If the **Configuration Parameters** related list for the relevant MID Server does not show this parameter, you may need to add it.

</td></tr><tr><td>

Pattern Designer fails during a debug session. The Pattern Designer message contains information about an error caused by a timeout.

</td><td>

The Pattern Designer fails because of a timeout during pattern debugging \(and not during discovery\).

</td><td>

By default, the **sa.debugger.max\_timeout**parameter is set to 240 seconds.Increase the value of this parameter on the relevant MID Server.

</td></tr></tbody>
</table>To run the Kubernetes pattern in Debug mode, refer to [KB0832567](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0832567) for operational information.

-   **[Container image scanning for software decomposition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/container-image-concept.md)**  
The ITOM Visibility apps, Discovery and Service Mapping Patterns and Kubernetes Visibility Agent integrate with Aqua Trivy to collect data on container images and OS packages. You can increase your control over container deployment by having visibility to the container components.
-   **[Disable Docker container CI discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/disable-docker-container-discovery.md)**  
Configure Docker discovery to collect image CIs only, instead of both image and container CIs.

**Parent Topic:**[Discovery for containerized resources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/container-discovery.md)

