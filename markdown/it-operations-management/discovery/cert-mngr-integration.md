---
title: Certificate generation through Cert-Manager Integration
description: Request a certificate through Kubernetes cert-manager using the ServiceNow External Issuer \(sn-external-issuer\) and save the certificate and its related information securely within the Kubernetes cluster as a secret. In Kubernetes, a secret is an object that allows you to store and manage sensitive information, such as passwords, API keys, and certificates.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-10-29"
reading_time_minutes: 2
breadcrumb: [Configuring Certificate Inventory and Management, Certificate Inventory and Management, Discovery, ITOM Visibility, IT Operations Management]
---

# Certificate generation through Cert-Manager Integration

Request a certificate through Kubernetes cert-manager using the ServiceNow External Issuer \(sn-external-issuer\) and save the certificate and its related information securely within the Kubernetes cluster as a secret. In Kubernetes, a secret is an object that allows you to store and manage sensitive information, such as passwords, API keys, and certificates.

For information on building an external issuer, see [Building and Deploying External Issuer For Certificate Management \[KB1435392\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1435392).

## Deployment Requirements

-   Deploy cert-manager in your Kubernetes environment. Update **manager.yaml** with Instance URL, Certificate Owner Group, Certificate Owner, Environment, and Renewal Tracking.
-   Deploy the ServiceNow External Issuer \(sn-external-issuer\) in your Kubernetes environment. Create a Kubernetes secret **clusterissuer-servicenow-credentials** with the instance username and password, ensuring the user has the necessary roles to request a certificate.
-   The ServiceNow External Issuer supports amd64 architecture along with the latest version of Kubernetes, 1.33.3.

## ServiceNow External Issuer \(sn-external-issuer\)

-   External issuers expand cert-manager functionality to issue certificates through non-core APIs and services.
-   The ServiceNow External Issuer is a ServiceNow-specific implementation of an External Issuer.
-   When a new certificate task is created, its Certificate Request UID and Certificate Task Sys Id are stored in the local JSON cache and the Certificate Request UID to Task Map table on the instance.
-   The ServiceNow External Issuer polls the instance to monitor the status of the certificate task.
-   If the certificate task is in the **Work in progress** state, its Certificate Request UID and Certificate Task Sys Id are added to the External Issuer UID Map table on the instance and the local JSON cache. During this time, Cert-manager automatically attempts to request the certificate.
-   Upon receiving a certificate request, Cert-manager checks for a matching task in the local JSON cache. If found, it polls the same task; otherwise, it queries the instance for records from the External Issuer UID Map table and populates the local JSON cache.
-   Once the task is marked as complete and the certificate is generated, the ServiceNow External Issuer sends another request to the instance, downloads the certificate attachment, and updates the certificate resource and corresponding secret in Kubernetes.

## Deploying the ServiceNow External Issuer in Kubernetes

Deploying the ServiceNow External Issuer in Kubernetes involves the following steps:

1.  From the ServiceNow instance download page, obtain the Helm Chart or YAML zip package.
2.  Customize the `manager.yaml` or `values.yaml` files as needed for your specific use case. These files may include essential information such as the Instance URL and Certificate Owner Group.
3.  Create a Kubernetes secret named `clusterissuer-servicenow-credentials` with the instance username and password.

    Example command:

    -   Create a Kubernetes secret named `clusterissuer-servicenow-credentials` with the instance username and password. Example command:

        ```
        kubectl create secret generic clusterissuer-servicenow-credentials
                      --from-literal=user=<user_name> --from-literal=password=<password> -n
                    system
        ```

    -   Ensure that the user has the necessary roles to request certificates.
4.  Execute the following commands for deployment.

    ```
    kubectl create ns system
    kubectl apply -f crd
    kubectl apply -f rbac
    kubectl apply -f issuers
    kubectl apply -f manager/manager.yaml
    ```

5.  \(Optional\) Customize any additional configurations in the files to suit your specific requirements.
6.  Ensure that the deployment is successful and the ServiceNow External Issuer is up and running.

## Request new certificate flow

After deployment, submit a certificate resource with the following information in a file named `certificate_clusterissuer.yaml`.

-   issuerRef : clusterissuer-servicenow
-   issuer : issuer-servicenow
-   kind : ClusterIssuer
-   issuerRef : servicenow-issuer.servicenow.com

Here's a sample Certificate Resource:

```
apiVersion: cert-manager.io/v1
kind: Certificate
metadata:
name: certificate-by-clusterissuer
spec:
commonName: certificate-by-clusterissuer.servicenow.com
secretName: certificate-by-clusterissuer
dnsNames:
- servicenow.com
- foo.servicenow.com
issuerRef:
name: clusterissuer-servicenow
group: servicenow-issuer.servicenow.com
kind: ClusterIssuer
```

Apply the certificate resource using `kubectl apply -f certificate_clusterissuer.yaml`

