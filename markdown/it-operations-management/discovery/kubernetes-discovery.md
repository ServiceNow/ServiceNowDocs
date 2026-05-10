---
title: Kubernetes discovery using patterns
description: The ServiceNow ITOM Visibility finds Kubernetes and OpenShift components using patterns and creates application services containing them. Discovery also finds Kubernetes events and frequently updates the CMDB to reflect the dynamic Kubernetes environment.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-23"
reading_time_minutes: 25
keywords: [azure kubernetes, kubernetes cluster, get kubernetes config file, kubernetes mid server]
breadcrumb: [Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Kubernetes discovery using patterns

The ServiceNow ITOM Visibility finds Kubernetes and OpenShift components using patterns and creates application services containing them. Discovery also finds Kubernetes events and frequently updates the CMDB to reflect the dynamic Kubernetes environment.

Discovery uses the Kubernetes pattern and its extension sections to discover Kubernetes components:

-   The **Collect OpenShift info** extension section of the Kubernetes pattern discovers the OpenShift components of the Kubernetes deployment. The OpenShift Build Config extension section is available from Store version 1.0.53.
-   The **Service Mesh** extension discovers service mesh details. This information enables the pattern to create service-to-service relations, shown as Connects to::Connected. Service mesh discovery requires deploying Istio on your K8s \(Kubernetes\) cluster. The Service Mesh extension section is available from [Kubernetes extension classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/cmdb-ci-class-models/cmdb-ci-class-models-kubernetes.md). It’s supported on the ServiceNow AI Platform using the Madrid release or later.
-   The **Collect Container Repository** and extension section finds container registries and images in these registries.

In addition, Discovery uses the Kubernetes Event pattern to discover events for Kubernetes components.

From the 1.0.68 release on ServiceNow Store, Service Mapping can use CI relationships to add the Kubernetes components to application services during tag-based discovery.

Discovery uses the following patterns to discover the entire Kubernetes infrastructure deployed on GCP, AWS, and Azure:

-   Google Cloud Platform \(GCP\) – Get Kubernetes Clusters.
-   Amazon AWS Cloud - Get Kubernetes Clusters.
-   Microsoft Azure - Get Kubernetes Clusters.

These patterns query the Cloud, collect data on all Kubernetes clusters, and create a serverless schedule for each cluster. When the cluster is deleted, the schedule is marked as inactive. This feature eliminates the overhead of creating and managing multiple credentials and serverless discovery schedules per cluster. The Cloud infrastructure patterns are triggered through standard Cloud discovery.

## Supported versions

The patterns have been validated with the following Kubernetes and Red Hat OpenShift versions:

|Platform/pattern|Validated version|
|----------------|-----------------|
|On-Premises Kubernetes|1.34|
|Google Kubernetes Engine \(GKE\)|1.34|
|Azure Kubernetes Engine \(AKS\)|1.34|
|Amazon Elastic Kubernetes Service \(EKS\)|1.34|
|Kubernetes Event patterns|1.34|
|OpenShift|4.19.20|

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

**Note:** For prerequisites for Kubernetes Cloud infrastructure discovery, see [below](kubernetes-discovery.md#section_qgk_lbh_dtb).

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

        2.  In the output, find the username and password.![Locate the lines that contain information on password and username.](../image/kubernetes-username-password.png)

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

    Create and define the serverless execution pattern as described in the product documentation. Configure the parameters required by the Kubernetes pattern as follows:

<table id="table_obc_k2z_3db"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

url

</td><td>

The identifier for the hostname, IP, or FQDN and the port of the Kubernetes apiserver. Use the following format: example\_hostname:example\_port or xample\_ip:example\_port. Provide the correct protocol \(HTTP or HTTPS\) in the URL.

</td></tr><tr><td>

namespace

</td><td>

The namespaces that the system passes in the Kubernetes Discovery Configuration. Enter one of the following values:-   Individual namespace: enter the namespace and then "kube-system". For example: `dev,kube-system`
-   The default value: enter `default, kube-system`
-   Multipile namespaces: enter the namespaces, use a comma \(,\) to separate the values, and then enter "kube-system". For example: `automation,application,test,kube-system`
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

The cloud provider: GCP or AWS or Azure.

</td></tr><tr><td>

cluster\_resource\_id

</td><td>

Cluster resource ID example:-   Azure Kubernetes clusters- Resource ID.
-   AWS- cluster ARN.
-   GCP- cluster global name.


</td></tr></tbody>
</table>9.  Create a serverless discovery schedule for the Kubernetes Event pattern. Configure the schedule to run every 5 or 10 minutes.

    **Note:** When the pattern is run for the first time, it stores an event\_timestamp. Later on it collects only the delta events based on the timestamp. The more often the pattern is run, the fewer updates to the CMDB IRE are needed.

    Create a serverless execution pattern for the discovery schedule and assign it to the Kubernetes Events pattern. Configure the parameters required by the Kubernetes pattern as described in [Configuring execution pattern attributes](kubernetes-discovery.md#table_obc_k2z_3db).

10. To include discovered components into service instances, enable CI relationships used in tag-based discovery by Service Mapping. These CI relationships are available from the 1.0.68 release on the ServiceNow Store. For operational steps, see [Tag-based discovery configuration](tag_discovery_configuration.md).

## Prerequisites for Kubernetes Cloud infrastructure discovery

For the Google Cloud Platform \(GCP\) – Get Kubernetes Clusters pattern, perform the following:

1.  In the ServiceNow instance, set up a Google Cloud Platform \(GCP\) service account with valid credentials and permissions.
2.  On the GCP infrastructure, set up the MID Server with full access to all Cloud APIs: Set Cloud API access scopes to "Allow full access to all Cloud APIs". The MID Server instance can access only the Clusters specific to the project.
3.  Navigate to `sys_properties.list` and configure the following properties:
    -   **sn\_itom\_pattern.k8s\_midserver**: Specify a valid MID Server name.
    -   **sn\_itom\_pattern.k8s\_create\_schedule\_enabled**: Set the value to **true**.

        **Note:** Enabling the **sn\_itom\_pattern.k8s\_create\_schedule\_enabled** property automatically creates a serverless schedule for your cloud clusters, eliminating the need for manual scheduling. If you have an existing manual schedule and want to convert it to an automatic one, enable the property. Your manual schedule will be updated; no additional schedule will be created.

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

3.  Navigate to `sys_properties.list` and configure the following properties:
    -   **sn\_itom\_pattern.k8s\_midserver**: Specify a valid MID Server name.
    -   **sn\_itom\_pattern.k8s\_create\_schedule\_enabled**: Set the value to **true**.

        **Note:** Enabling the **sn\_itom\_pattern.k8s\_create\_schedule\_enabled** property automatically creates a serverless schedule for your cloud clusters, eliminating the need for manual scheduling. If you have an existing manual schedule and want to convert it to an automatic one, enable the property. Your manual schedule will be updated; no additional schedule will be created.

4.  Create and run an AWS Cloud Discovery schedule.


For Microsoft Azure Kubernetes Services \(AKS\)- Kubernetes cluster discovery, perform the following:

1.  Update to the latest Discovery and Service Mapping Patterns version.
2.  In the ServiceNow instance, configure the Azure Service Account with valid Azure credentials and permission.
3.  Navigate to `sys_properties.list` and configure the following properties:
    -   **sn\_itom\_pattern.k8s\_midserver**: Specify a valid MID Server name.
    -   **sn\_itom\_pattern.k8s\_create\_schedule\_enabled**: Set the value to **true**.

        **Note:** Enabling the **sn\_itom\_pattern.k8s\_create\_schedule\_enabled** property automatically creates a serverless schedule for your cloud clusters, eliminating the need for manual scheduling. If you have an existing manual schedule and want to convert it to an automatic one, enable the property. Your manual schedule will be updated; no additional schedule will be created.

        .

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

The feature flag that can be enabled/disabled under the system properties, which is responsible to control the pattern execution. When enabled, it creates discovery schedules despite the new property value.

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

sn\_itom\_pattern.k8s\_midserver

</td><td>

\[Default\]

 Example- Valid MID Server name

</td><td>

String

</td><td>

 

</td></tr><tr><td>

sn\_itom\_pattern.k8s\_&lt;service\_account\_id&gt;\_midserver

</td><td>

\[Based on Service Account Level\]

 Example- Valid MID Server name

</td><td>

String

</td><td>

 

</td></tr><tr><td>

sn\_itom\_pattern.k8s\_&lt;service\_account\_id&gt;\_&lt;clustername&gt;\_midserver

</td><td>

\[Based on Cluster name\]

 Example- Valid MID Server name

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

 

</td></tr></tbody>
</table>**Note:** `<service_account_id>` is the account ID name under Cloud Service Accounts. For more information, see: [Create Discovery schedules for cloud resources](../../discovery/concept/discovery-manager.md#)

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

<table id="table_olk_1pq_f56b"><thead><tr><th>

Table and field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

</td></tr><tr><td>

Name

</td><td>

The name of the kube-controller-manager leader.

</td></tr><tr><td>

K8s\_uid

</td><td>

The kube-system namespace UID \[supported versions: 1.0.92 and later\]

</td></tr><tr><td>

ip\_address

</td><td>

The identifier for the host\_ip of the Kubernetes apiserver.

</td></tr><tr><td>

port

</td><td>

The identifier for the Kubernetes apiserver port.

</td></tr><tr><td>

namespace

</td><td>

This value shows the namespaces the system passed in the Kubernetes Discovery Configuration.

</td></tr><tr><td>

event\_timestamp

</td><td>

The timestamp of the latest event created on this Kubernetes cluster at the time of the discovery.

</td></tr><tr><td>

Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]

</td><td>

The virtual aspect of the Kubernetes node. Data relating to the physical aspect of the Kubernetes node is stored under Linux server.

</td></tr><tr><td>

name

</td><td>

The name of the Kubernetes node. The format can be only the name of the machine or the full name consisting of the name and the hostname: `<name>.<hostname>`.

</td></tr><tr><td>

k8s\_uid

</td><td>

The identifier for the Kubernetes node UUID.

</td></tr><tr><td>

cluster

</td><td>

The name of the cluster that contains this resource.

</td></tr><tr><td>

operational\_status

</td><td>

The operational status of the Kubernetes node.

</td></tr><tr><td colspan="2">

Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]

</td></tr><tr><td>

name

</td><td>

The name of the Kubernetes service.

</td></tr><tr><td>

selector

</td><td>

A comma delimited list of the label selectors specified in the Kubernetes configuration that are used to select target pods.

</td></tr><tr><td>

namespace

</td><td>

The Kubernetes namespace to which this Kubernetes service belongs.

</td></tr><tr><td>

k8s\_uid

</td><td>

The Kubernetes service UUID.

</td></tr><tr><td>

cluster

</td><td>

The name of the cluster that contains this resource.

</td></tr><tr><td colspan="2">

Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]

</td></tr><tr><td>

name

</td><td>

The name of the Kubernetes pod.

</td></tr><tr><td>

k8s\_uid

</td><td>

The Kubernetes pod UUID.

</td></tr><tr><td>

resourceVersion

</td><td>

The resource version of the Kubernetes pod.

</td></tr><tr><td>

namespace

</td><td>

The Kubernetes namespace to which this Kubernetes pod belongs.

</td></tr><tr><td>

cluster

</td><td>

The name of the cluster that contains this resource.

</td></tr><tr><td>

state

</td><td>

The Kubernetes pod status: Pending, Running, Succeeded, Failed, and Unknown.

</td></tr><tr><td colspan="2">

Kubernetes Cronjob \[cmdb\_ci\_kubernetes\_cronjob\]

</td></tr><tr><td>

name

</td><td>

The name of the Kubernetes cronjob

</td></tr><tr><td>

namespace

</td><td>

The Kubernetes namespace to which this Kubernetes pod belongs.

</td></tr><tr><td>

k8s\_uid

</td><td>

The Kubernetes cronjob UUID.

</td></tr><tr><td>

cluster

</td><td>

The name of the cluster that contains this resource.

</td></tr><tr><td colspan="2">

Kubernetes Job \[cmdb\_ci\_kubernetes\_job\]

</td></tr><tr><td>

name

</td><td>

The name of the Kubernetes Job

</td></tr><tr><td>

namespace

</td><td>

The Kubernetes namespace to which this Kubernetes job belongs.

</td></tr><tr><td>

k8s\_uid

</td><td>

The Kubernetes job UUID

</td></tr><tr><td>

cluster

</td><td>

The name of the cluster that contains Kubernetes job.

</td></tr><tr><td colspan="2">

Kubernetes Daemonset \[cmdb\_ci\_kubernetes\_daemonset\]

</td></tr><tr><td>

name

</td><td>

The name of the Kubernetes daemonset.

</td></tr><tr><td>

namespace

</td><td>

The Kubernetes namespace to which this Kubernetes daemonset belongs.

</td></tr><tr><td>

k8s\_uid

</td><td>

The Kubernetes daemonset UUID.

</td></tr><tr><td>

cluster

</td><td>

The name of the cluster that contains this resource.

</td></tr><tr><td>

pods\_avail

</td><td>

The number of pods Available.

</td></tr><tr><td>

pods\_failed

</td><td>

The number of pods in Failed phase.

</td></tr><tr><td>

pods\_running

</td><td>

The Number of pods in the Running phase.

</td></tr><tr><td>

pods\_succeeded

</td><td>

The number of pods in the Succeeded phase.

</td></tr><tr><td>

pods\_waiting

</td><td>

The number of pods in the Waiting phase.

</td></tr><tr><td colspan="2">

Kubernetes Ingress \[cmdb\_ci\_kubernetes\_ingress\]

</td></tr><tr><td>

name

</td><td>

The name of the Kubernetes ingress

</td></tr><tr><td>

namespace

</td><td>

The Kubernetes namespace to which this Kubernetes ingress belongs.

</td></tr><tr><td>

k8s\_uid

</td><td>

The Kubernetes ingress UID

</td></tr><tr><td>

cluster

</td><td>

The name of the cluster that contains this resource.

</td></tr><tr><td colspan="2">

Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]

 Kubernetes Replicaset \[cmdb\_ci\_kubernetes\_replicaset\]

 Kubernetes Replication controller \[cmdb\_ci\_kubernetes\_replicationcontroller\]

 Kubernetes Statefulset \[cmdb\_ci\_kubernetes\_statefulset\]

</td></tr><tr><td>

name

</td><td>

The name of this resource

</td></tr><tr><td>

namespace

</td><td>

The Kubernetes namespace to which this resource belongs.

</td></tr><tr><td>

K8s\_uid

</td><td>

The Kubernetes UID of this resource

</td></tr><tr><td>

cluster

</td><td>

The name of the cluster that contains this resource.

</td></tr><tr><td>

total\_replicas

</td><td>

Number of replicas in this resource

</td></tr><tr><td>

desired\_replicas

</td><td>

The number of replicas in desired phase

</td></tr><tr><td>

available\_replicas

</td><td>

Number of replicas available

</td></tr><tr><td>

unavailable\_replicas

</td><td>

Number of replicas in unavailable phase

</td></tr><tr><td>

updated\_replicas

</td><td>

Number of replicas updated

</td></tr><tr><td>

Docker Container \[cmdb\_ci\_docker\_container\]

</td><td>

The component that runs the docker image.

</td></tr><tr><td>

container\_id

</td><td>

The unique identifier for the Kubernetes docker containerIn cases where duplicate records are created, deduplication tasks appear once discovery runs. For information on how to resolve these tasks, see the [Making docker container identifier independent \[KB1443042\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1443042) article in the ServiceNow® Knowledge Base.

</td></tr><tr><td>

namespace

</td><td>

The Kubernetes namespace to which this Kubernetes docker container belongs

</td></tr><tr><td>

Docker Image \[cmdb\_ci\_docker\_image\]

</td><td>

An executable package of an application and its related software that can be instantiated by a docker container

</td></tr><tr><td>

image\_id

</td><td>

The identifier for the Kubernetes docker image

</td></tr><tr><td>

name

</td><td>

The name of the Kubernetes docker image.

</td></tr><tr><td>

image\_url

</td><td>

The URL for downloading the docker image.

</td></tr><tr><td>

namespace

</td><td>

The Kubernetes namespace to which this Kubernetes docker image belongs.

</td></tr><tr><td>

Linux Server \[cmdb\_ci\_linux\_server\]

</td><td>

The server that hosts the Kubernetes node.

</td></tr><tr><td>

name

</td><td>

The name of the Linux server powering the Kubernetes node.

</td></tr><tr><td>

hostname

</td><td>

The hostname of the Linux server.

</td></tr><tr><td>

os

</td><td>

The operating system deployed on this Linux server.

</td></tr><tr><td>

kernel\_release

</td><td>

The version of the Linux kernel operating system deployed on this Linux server.

</td></tr><tr><td>

ram

</td><td>

The size of RAM installed on this Linux server.

</td></tr><tr><td>

ip\_address

</td><td>

The IP address of the Linux server.

</td></tr><tr><td>

cpu\_type

</td><td>

The CPU architecture of the Linux server hosting the Kubernetes node.

</td></tr><tr><td>

cpu\_count

</td><td>

The number of CPUs on the Linux server hosting the Kubernetes node.

</td></tr><tr><td>

serial\_number

</td><td>

The serial number of the Linux server hosting the Kubernetes node.

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

This configuration item contains Kubernetes labels. Labels are key/value pairs that are attached to objects, such as pods.

</td></tr><tr><td>

key

</td><td>

The key of the Kubernetes pod or Kubernetes service **Key Value** parameter.

</td></tr><tr><td>

value

</td><td>

The value of the Kubernetes pod or Kubernetes service **Key Value** parameter.

</td></tr><tr><td colspan="2">

Kubernetes Volume \[cmdb\_ci\_kubernetes\_volume\]

</td></tr><tr><td>

k8s\_uid

</td><td>

The Kubernetes volume UUID.

</td></tr><tr><td>

mount\_path

</td><td>

The path for accessing this Kubernetes volume.

</td></tr><tr><td>

name

</td><td>

The name of the Kubernetes volume.

</td></tr><tr><td>

namespace

</td><td>

The Kubernetes namespace to which this Kubernetes volume belongs.

</td></tr><tr><td>

cluster

</td><td>

The name of the cluster that contains this resource.

</td></tr><tr><td>

volume\_id

</td><td>

The ID of the Kubernetes volume.

</td></tr><tr><td colspan="2">

OpenShift Deployed Configuration \[cmdb\_ci\_openshift\_dep\_conf\]​

</td></tr><tr><td>

name

</td><td>

The name of the OpenShift Deployment configuration.

</td></tr><tr><td>

namespace

</td><td>

The name of the namespace containing the deployment configuration.

</td></tr><tr><td>

k8s\_uid

</td><td>

The Kubernetes volume UUID.

</td></tr><tr><td>

url

</td><td>

The URL of the OpenShift deployed configuration, available only for Kubernetes versions earlier than 1.16.

</td></tr><tr><td colspan="2">

OpenShift Build Config \[cmdb\_ci\_openshift\_build\_conf\]

</td></tr><tr><td>

name

</td><td>

The name of the OpenShift build configuration.

</td></tr><tr><td>

namespace

</td><td>

The name of the OpenShift namespace containing the build configuration.

</td></tr><tr><td>

k8s

</td><td>

The Kubernetes volume UUID.

</td></tr><tr><td>

url

</td><td>

The URL of the OpenShift build configuration, available only for Kubernetes versions earlier than 1.16.

</td></tr><tr><td colspan="2">

OpenShift Source2Image \[cmdb\_ci\_openshift\_source\_2\_image\]

</td></tr><tr><td>

name

</td><td>

The name of the OpenShift source image.

</td></tr><tr><td>

to

</td><td>

Related image.

</td></tr><tr><td>

parent\_id

</td><td>

The ID of the OpenShift source image.

</td></tr><tr><td colspan="2">

OpenShift Route \[cmdb\_ci\_openshift\_route\]

</td></tr><tr><td>

name

</td><td>

The name of the OpenShift route.

</td></tr><tr><td>

namespace

</td><td>

The name of the namespace containing the OpenShift route.

</td></tr><tr><td>

k8s\_uid

</td><td>

The Kubernetes volume UUID.

</td></tr><tr><td>

url

</td><td>

The URL of the OpenShift Route, available only for Kubernetes versions earlier than 1.16.

</td></tr><tr><td>

host

</td><td>

The target host of the OpenShift route.

</td></tr><tr><td>

port

</td><td>

The target port of the OpenShift route.

</td></tr><tr><td colspan="2">

OpenShift Group \[cmdb\_ci\_openshift\_group\]

</td></tr><tr><td>

name

</td><td>

The name of the OpenShift Group.

</td></tr><tr><td>

k8s\_uid

</td><td>

The Kubernetes volume UUID.

</td></tr><tr><td>

url

</td><td>

The URL of the OpenShift Group, available only for Kubernetes versions earlier than 1.16.

</td></tr><tr><td colspan="2">

OpenShift User \[cmdb\_ci\_openshift\_user\]

</td></tr><tr><td>

name

</td><td>

The name of the OpenShift user.

</td></tr><tr><td>

k8s\_uid

</td><td>

The Kubernetes volume UUID.

</td></tr><tr><td>

url

</td><td>

The URL of the OpenShift user, available only for Kubernetes versions earlier than 1.16.

</td></tr><tr><td>

full\_name

</td><td>

The full name of the OpenShift user.

</td></tr><tr><td colspan="2">

OpenShift Project \[cmdb\_ci\_openshift\_project\]

</td></tr><tr><td>

name

</td><td>

The name of the OpenShift project.

</td></tr><tr><td>

k8s\_uid

</td><td>

The Kubernetes volume UUID.

</td></tr><tr><td>

url

</td><td>

The URL of the OpenShift Project, available only for Kubernetes versions earlier than 1.16.

</td></tr><tr><td colspan="2">

OpenShift Image \[cmdb\_ci\_openshift\_images\]

</td></tr><tr><td>

name

</td><td>

The name of the OpenShift Image.

</td></tr><tr><td>

k8s\_uid

</td><td>

The Kubernetes volume UUID.

</td></tr><tr><td>

url

</td><td>

The URL of the OpenShift Image, available only for Kubernetes versions earlier than 1.16.

</td></tr><tr><td>

docker\_image\_metadata\_id

</td><td>

The ID of the docker image.

</td></tr><tr><td>

docker\_image\_metadata\_parent\_id

</td><td>

The ID of the image parent ID.

</td></tr><tr><td>

arch

</td><td>

Architecture of the image.

</td></tr><tr><td>

size

</td><td>

The image size.

</td></tr><tr><td>

hostname

</td><td>

The hostname related to the image.

</td></tr><tr><td colspan="2">

OpenShift Image Stream \[cmdb\_ci\_openshift\_images\_stream\]

</td></tr><tr><td>

name

</td><td>

The name of the OpenShift Image Stream.

</td></tr><tr><td>

k8s\_uid

</td><td>

The Kubernetes volume UUID.

</td></tr><tr><td>

url

</td><td>

The URL of the OpenShift Image Stream, available only for Kubernetes versions earlier than 1.16.

</td></tr><tr><td>

namespace

</td><td>

The name of the namespace containing the OpenShift image stream.

</td></tr><tr><td colspan="2">

OpenShift Docker Image Repository \[cmdb\_ci\_openshift\_docker\_images\_repository\]

</td></tr><tr><td>

name

</td><td>

The name of the OpenShift docker image repository.

</td></tr><tr><td>

parent\_ID

</td><td>

The ID of the parent system.

</td></tr><tr><td colspan="2">

Namespace \[cmdb\_ci\_kubernetes\_namespace\]

</td></tr><tr><td>

name

</td><td>

The name of the Kubernetes Namespace.

</td></tr><tr><td>

state

</td><td>

The Kubernetes namespace phases: Active or Terminating.

</td></tr></tbody>
</table>This data is collected by the **Collect Container Repository** extension section.

|Table and field|Description|
|---------------|-----------|
|Container Repository \[cmdb\_ci\_container\_repository\]|
|Name \[name\]|The name of the container repository.|
|Container Repository Entry \[cmdb\_ci\_container\_repository\_entry\]|
|Name \[name\]|The name of the container repository entry.|
|Category \[category\]|The category of the container repository entry.|

The graphic illustrates CIs that are part of Kubernetes discovery.

**Note:** This Dependency Views map was simplified for clarity. Your Kubernetes deployments may contain many more CIs.

![Relationships between Kubernetes configuration items and Kubernetes workload tables](../../it-operations-management/image/kubernetes-diagram.png "Components of the Kubernetes deployment")

![Namespace contains OpenShift configuration items](../../it-operations-management/image/openshift-diagram.png "Components of the Kubernetes deployment including OpenShift")

## CI relationships collected by the Kubernetes pattern

These relationships are created by Kubernetes pattern:

<table id="table_ysf_fpq_f987b"><thead><tr><th>

CI

</th><th>

Relationship

</th><th>

CI

</th></tr></thead><tbody><tr><td rowspan="13">

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

</td><td>

Contains::Contained By

</td><td>

Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]

</td></tr><tr><td>

Contains::Contained By

</td><td>

Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]

</td></tr><tr><td>

Contains::Contained By

</td><td>

Kubernetes Ingress \[cmdb\_ci\_kubernetes\_ingress\]

</td></tr><tr><td>

Contains::Contained By

</td><td>

Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]

</td></tr><tr><td>

Contains::Contained By

</td><td>

\[cmdb\_ci\_openshift\_source\_2\_image\]

</td></tr><tr><td>

Contains::Contained By

</td><td>

OpenShift Group \[cmdb\_ci\_openshift\_group\]

</td></tr><tr><td>

Contains::Contained By

</td><td>

OpenShift User \[cmdb\_ci\_openshift\_user\]

</td></tr><tr><td>

Contains::Contained By

</td><td>

OpenShift Project \[cmdb\_ci\_openshift\_project\]

</td></tr><tr><td>

Contains::Contained By

</td><td>

OpenShift Image \[cmdb\_ci\_openshift\_images\]

</td></tr><tr><td>

Contains::Contained By

</td><td>

OpenShift Docker Image Repository \[cmdb\_ci\_openshift\_docker\_images\_repository\]

</td></tr><tr><td>

Cluster of::Cluster

</td><td>

Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]

</td></tr><tr><td>

Manages::Managed by

</td><td>

Linux Server \[cmdb\_ci\_linux\_server\]

</td></tr><tr><td>

Contained by::Contains

</td><td>

Resource Group \[cmdb\_ci\_resource\_group\]

</td></tr><tr><td rowspan="3">

Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]

</td><td>

Contains::Contained By

</td><td>

Docker Container \[cmdb\_ci\_docker\_container\]

</td></tr><tr><td>

Contains::Contained By

</td><td>

Docker Image \[cmdb\_ci\_docker\_image\]

</td></tr><tr><td>

Contains::Contained By

</td><td>

Kubernetes Volume \[cmdb\_ci\_kubernetes\_volume\]

</td></tr><tr><td>

Kubernetes Workload \[cmdb\_ci\_kubernetes\_workload\]

</td><td>

Hosted on::Hosts

</td><td>

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

</td></tr><tr><td>

Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]

</td><td>

Provides::Provided By

</td><td>

Kubernetes Workload \[cmdb\_ci\_kubernetes\_workload\]

</td></tr><tr><td>

Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]

</td><td>

Owns::Owned By

</td><td>

Kubernetes Replicaset \[cmdb\_ci\_kubernetes\_replicaset\]

</td></tr><tr><td>

Kubernetes Replicaset \[cmdb\_ci\_kubernetes\_replicaset\]

</td><td>

iInstantiates:: Instantiated By

</td><td>

Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]

</td></tr><tr><td>

Kubernetes Workload \[cmdb\_ci\_kubernetes\_workload\]

</td><td>

Provided By::Provides To

</td><td>

Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]

</td></tr><tr><td>

Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]

</td><td>

Hosted on::Hosts

</td><td>

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

</td></tr><tr><td>

Kubernetes Daemonset \[cmdb\_ci\_kubernetes\_daemonset\]

</td><td>

Hosted on::Hosts

</td><td>

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

</td></tr><tr><td>

Kubernetes Statefulset \[cmdb\_ci\_kubernetes\_statefulset\]

</td><td>

Hosted on::Hosts

</td><td>

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

</td></tr><tr><td rowspan="4">

Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]​

</td><td>

Contains::Contained By

</td><td>

OpenShift Deployed Config \[cmdb\_ci\_openshift\_dep\_conf​\]

</td></tr><tr><td>

Contains::Contained By

</td><td>

OpenShift Build Config \[cmdb\_ci\_openshift\_build\_conf\]

</td></tr><tr><td>

Contains::Contained By

</td><td>

OpenShift Route \[cmdb\_ci\_openshift\_route\]

</td></tr><tr><td>

Contains::Contained By

</td><td>

OpenShift Image Stream \[cmdb\_ci\_openshift\_images\_stream\]

</td></tr><tr><td>

Docker Image \[cmdb\_ci\_docker\_image\]

</td><td>

Instantiates::Instantiated by

</td><td>

Docker Container \[cmdb\_ci\_docker\_container\]

</td></tr><tr><td rowspan="3">

Linux Server \[cmdb\_ci\_linux\_server\]

</td><td>

Contains::Contained By

</td><td>

Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]

</td></tr><tr><td>

Runs::Runs on

</td><td>

Docker Container \[cmdb\_ci\_docker\_container\]

</td></tr><tr><td>

Hosts::Hosted on

</td><td>

Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]

</td></tr><tr><td>

OpenShift Deploy Config \[cmdb\_ci\_openshift\_dep\_conf​\]

</td><td>

Contains::Contained By

</td><td>

\[cmdb\_ci\_config\_file\_tracked​\]

</td></tr></tbody>
</table>The **Collect Container Repository** extension section of the Kubernetes pattern identifies these relationships.

|CI|Relationship|CI|
|---|------------|---|
|Docker Image \[cmdb\_ci\_docker\_image\]|Provisioned From::Provisioned|Container Repository Entry \[cmdb\_ci\_container\_repository\_entry\]|
|Container Repository Entry \[cmdb\_ci\_container\_repository\_entry\]|Hosted on::Hosts|Container Repository \[cmdb\_ci\_container\_repository\]|

## CI relationships collected by the Istio Service Mesh extension

Prerequisites for Istio Service Mesh extension:

-   Ensure that Istio Service Mesh and Prometheus components are configured on the Kubernetes cluster.
-   Ensure that Prometheus discovers the service connection information using the `queryistio_requests_total` command.
-   Ensure that the application services are connected, and verify service-to-service traffic flow in Kiali graph.

For more information on the Bookinfo application, see: [https://istio.io/latest/docs/examples/bookinfo/](https://istio.io/latest/docs/examples/bookinfo/)

|CI|Relationship|CI|
|---|------------|---|
|Kubernetes Service \[cmdb\_ci\_kubernetes\_servi ce\]|Connects to::Connected by|Kubernetes Service \[cmdb\_ci\_kubernetes\_servi ce\]|

## CI relationships collected by the Kubernetes Event pattern

These relationships are created to support the Kubernetes event discovery:

<table id="table_ysf_fpq_f9k393"><thead><tr><th>

CI

</th><th>

Relationship

</th><th>

CI

</th></tr></thead><tbody><tr><td rowspan="4">

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

</td><td>

Contains::Contained By

</td><td>

Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]

</td></tr><tr><td>

Contains::Contained By

</td><td>

Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]

</td></tr><tr><td>

Cluster of::Cluster

</td><td>

Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]

</td></tr><tr><td>

Manages::Managed by

</td><td>

\[cmdb\_ci\_linux\_server\]

</td></tr><tr><td rowspan="3">

Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]

</td><td>

Contains::Contained By

</td><td>

Docker Container \[cmdb\_ci\_docker\_container\]

</td></tr><tr><td>

Contains::Contained By

</td><td>

Docker Image \[cmdb\_ci\_docker\_image\]

</td></tr><tr><td>

Contains::Contained By

</td><td>

Kubernetes Volume \[cmdb\_ci\_kubernetes\_volume\]

</td></tr><tr><td>

Docker Image \[cmdb\_ci\_docker\_image\]

</td><td>

Instantiates::Instantiated by

</td><td>

Docker Container \[cmdb\_ci\_docker\_container\]

</td></tr><tr><td rowspan="3">

Linux Server \[cmdb\_ci\_linux\_server\]

</td><td>

Contains::Contained By

</td><td>

Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]

</td></tr><tr><td>

Runs::Runs on

</td><td>

Docker Container \[cmdb\_ci\_docker\_container\]

</td></tr><tr><td>

Hosts::Hosted on

</td><td>

Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]

</td></tr></tbody>
</table>## Data collected by Service Mapping during tag-based discovery

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

After Discovery finishes discovering components of the Kubernetes deployment, you can navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Insights** and use the Kubernetes Explorer dashboard to view the Kubernetes environments and resources of your organization. To use the enhanced Kubernetes dashboard, verify you have Discovery Admin Workspace starting from version 1.3.1 \(August 2024 Store\). For more information about Kubernetes Explorer, see [Kubernetes Explorer](../../../use/dashboards/application-content-packs/cloud-operations-workspace-kubernetes-dashboard.md).

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

-   **[Container image scanning for software decomposition](container-image-concept.md)**  
The ITOM Visibility apps, Discovery and Service Mapping Patterns and Kubernetes Visibility Agent integrate with Aqua Trivy to collect data on container images and OS packages. You can increase your control over container deployment by having visibility to the container components.

**Parent Topic:**[Discovery for containerized resources](../../discovery/concept/container-discovery.md)

