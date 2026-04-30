---
title: Build MID Server Docker Image for Linux
description: Deploy Containerized MID Servers on Linux by creating a Docker image with the provided recipes. Containerized MID Server uses a Docker image of the MID Server that allows you to quickly deploy MID Servers at scale.Containerized MID Server uses a Docker image of the MID Server that allows you to quickly deploy MID Servers at scale. MID Servers are deployed using orchestration tools like Docker Swarm.You can configure containerized MID Servers with configuration parameters passed through environment variables or secret files.You can configure containerized MID Servers with configuration parameters passed through environment variables or secret files.You can configure containerized MID Servers with configuration parameters passed through environment variables or secret files.You can configure containerized MID Servers with configuration parameters passed through environment variables or secret files.
locale: en-US
release: zurich
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 14
breadcrumb: [Containerized MID Server, Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Build MID Server Docker Image for Linux

Deploy Containerized MID Servers on Linux by creating a Docker image with the provided recipes. Containerized MID Server uses a Docker image of the MID Server that allows you to quickly deploy MID Servers at scale.

## Before you begin

Role required: admin

<table id="table_p53_ms4_nhb"><tbody><tr><td>

![Setup indicator for configuration phase](../image/ProgressBarConfig.png)

</td></tr></tbody>
</table>Prerequisites:

The host must use [Docker engine and command-line interface \(CLI\) 20.10.4 or later](https://docs.docker.com/desktop/install/linux-install/).

Update the library to the newest version available, or at least the highest version with a security fix. If issues identified are part of a transitive dependency, find a version of the dependent library which includes a newer transitive version. If the transitive dependency cannot be upgraded by upgrading the dependent library, consider excluding the dependency and directly including a secure version.

**Note:** Check docker availability by running the docker version command as administrator. See the [the docker version command documentation](https://docs.docker.com/engine/reference/commandline/version/) for more information.

## Procedure

1.  Download the Linux Docker recipe ZIP file from the MID Server download page and verify its signature.

    For more information about the MID Server download page and signature verification, see [Download MID Server files](t_DownloadMIDServerFiles.md#postreq_znq_nzd_mgb).

2.  Unzip the ZIP file to a folder.

3.  You can change the current directory to the new folder.

4.  To build an image, run the build command: `> docker build <path-to-docker-recipe> [ --tag <docker-tag> ]`

    For more information on the command, see [the Docker build command documentation](https://docs.docker.com/engine/reference/commandline/build/). The path to the Docker file can be a relative path or the current directory if the file is in the Docker recipe directory.

    The default image tag is provided out-of-the box in the .env file with the **DOCKER\_TAG** parameter. You can export this parameter before executing any docker command by running the command: `> export $(grep DOCKER_TAG .env)`. You can replace `<docker-tag>` with the **DOCKER\_TAG** value in all the following commands.

    The build command takes the following build arguments:

<table id="id_exp_hmz_z5b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

MID\_INSTALLATION\_URL

</td><td>

The link to download the MID Server installation file. By default, it is set to the download link for the Linux 64 bit Installation ZIP file provided on the MID Server download page.

</td></tr><tr><td>

MID\_INSTALLATION\_FILE

</td><td>

The name of a local MID Server installation file. The default value is empty. If this parameter is not empty, the recipe uses the local file instead of downloading from the installation server. This parameter uses the file name only, not the full path. Before the build, the local file must be copied to the `asset/` sub-folder of the recipe directory. MID Server releases prior to Rome are not supported.For example: `> docker build <path-to-dockerfile> --build-arg MID_INSTALLATION_FILE=<mid.installation.file.name>) --tag <docker-tag>`

</td></tr><tr><td>

MID\_SIGNATURE\_VERIFICATION

</td><td>

The signature of the MID Server installation file must be verified. The default value is TRUE. If it is TRUE, the build process always verifies the digital signature of the MID Server installation file whether it is downloaded from the remote server or a local file. Otherwise, the signature verification is skipped.For example: `> docker build <path-to-dockerfile> --build-arg MID_SIGNATURE_VERIFICATION=false --tag <docker-tag>`

</td></tr><tr><td>

USER\_ID and GROUP\_ID

</td><td>

By default, when not specified, Docker creates a   MID Server user with user id = 1001 and group id = 1001. You may pass a custom user id and group id into container by using the USER\_ID and GROUP\_ID build arguments. Docker creates an user for the  MID Server  with the provided user id and group id. Inside the container image, all files under the MID Server installation folder are owned by this user and the root group \(id=0\).

 When the image is deployed on Kubernetes platform, this MID Server user becomes the container user who runs the MID Server.

 When the image is deployed on an OpenShift platform, OpenShift may assign an arbitrary non-admin user id as the container user who runs the MID Server. However, that user always belongs to the root group.

 In both cases, the container user has full access to the MID Server files. That way, the same image can be deployed on Kubernetes as well as on OpenShift.

</td></tr></tbody>
</table>5.  After the image is built successfully, you can list the image built with command: `> docker image ls`


## What to do next

To save disk space, if there are unused or intermediate images, run the following commands to remove those dangling images:

```
$ docker rmi $(docker images --filter "dangling=true" -q --no-trunc)
```

For example, before removing dangling images, the command `docker image ls` may show something similar to the following:

```
REPOSITORY                                TAG                                           IMAGE ID       CREATED              SIZE
mid                                       trackdiscocopper-10-09-2020_10-14-2021_2200   4542b6ab34af   21 seconds ago       1.01GB
<none>                                    <none>                                        1cdae087a970   About a minute ago   1.38GB

```

After removing the dangling images, the command `docker image ls` shows the following:

```
REPOSITORY                                TAG                                           IMAGE ID       CREATED              SIZE
mid                                       trackdiscocopper-10-09-2020_10-14-2021_2200   4542b6ab34af   About a minute ago   1.01GB

```

## Launch Containerized MID Server

Containerized MID Server uses a Docker image of the MID Server that allows you to quickly deploy MID Servers at scale. MID Servers are deployed using orchestration tools like Docker Swarm.

### Before you begin

Role required: admin

Prerequisites:

-   Linux hosts must use AlmaLinux distribution 64 bit architecture, and AlmaLinux distro is recommended.

-   The host must use [Docker engine and command-line interface \(CLI\) 20.10.4 or later](https://docs.microsoft.com/en-us/virtualization/windowscontainers/quick-start/set-up-environment?tabs=Windows-Server).

    **Note:** Check docker availability by running the docker version command as administrator. See the [the docker version command documentation](https://docs.docker.com/engine/reference/commandline/version/) for more information.


### Procedure

1.  Once the image is available, launch the new MID Server using the docker run command and specify an env file or env variable options: `docker run --env-file <env_file_name_here> <docker_tag or image_id>`

    **Note:** Do not pass sensitive data using this command, as there may be security vulnerabilities. To pass sensitive data, use the procedures [Pass sensitive data to a containerized MID Server with Docker Secrets](mid-build-docker-linux.md#) and [Pass sensitive data to a containerized MID Server with Kubernetes Secrets](mid-build-docker-linux.md#).

    For more information, see the Docker documentation pages for [the docker image ls command](https://docs.docker.com/engine/reference/commandline/image_ls/), [the docker run command](https://docs.docker.com/engine/reference/commandline/run/), and [specifying an env file or env variable options](https://docs.docker.com/engine/reference/commandline/run/#set-environment-variables--e---env---env-file). The env file is a simple text file using the name=value format. If a variable is specified in both env file and in the `--env` option, the variable defined in the command line takes precedence.

    While deployment requests are the recommended method to launch containerized MID Servers, they can be alternatively configured with environmental variables. When the container is first started, the initialization script will take the environment variables and configure the MID Server application using the following environment variables:

    -   **MID\_INSTANCE\_URL**

        This variable sets the ‘url’ config parameter.

    -   **MID\_INSTANCE\_USERNAME**

        This variable sets the ‘mid.instance.username’ config parameter.

    -   **MID\_INSTANCE\_PASSWORD**

        This variable sets the ‘mid.instance.password’ config parameter.

    -   **MID\_SERVER\_NAME**

        This variable sets the ‘name’ config parameter.

    -   **MID\_PROXY\_HOST**

        This variable sets the ‘mid.proxy.host’ config parameter. This variable is not mandatory and is only necessary when a proxy is set up.

    -   **MID\_PROXY\_PORT**

        This variable sets the ‘mid.proxy.port’ config parameter.

    -   **MID\_PROXY\_USERNAME**

        This variable sets the ‘mid.proxy.username’ config parameter.

    -   **MID\_PROXY\_PASSWORD**

        This variable sets the ‘mid.proxy.password’ config parameter.

    -   **MID\_SECRETS\_FILE**

        This variable specifies the full secret filename that contains sensitive data like passwords or certificate.

    -   **MID\_MUTUAL\_AUTH\_PEM\_FILE**

        This variable specifies the full filename of the client certificate file used for auto validation setup.

2.  To see a list of containers, run the docker container ls command: `docker container ls [-a]`


## Pass sensitive data to a containerized MID Server with Docker Secrets

You can configure containerized MID Servers with configuration parameters passed through environment variables or secret files.

### Before you begin

Role required: Docker Swarm admin

### About this task

You can pass sensitive data, such passwords or certificates, into a containerized MID Server using [Docker Secret](https://docs.docker.com/engine/swarm/secrets/). Setup and start [Docker Swarm](https://docs.docker.com/engine/swarm/) before using this procedure.

When creating deployments, ensure that the replicas are kept to 1.

### Procedure

1.  Place the sensitive data in `mid-secrets.properties`

2.  Create a docker secret using the docker secret create command: `docker secret create mid-secrets mid-secrets.properties`

    The first `mid-secrets` represents the secret in docker swarm, while the second `mid-secrets.properties` parameter represents the file path to read the secret on the host machine’s filesystem. You can list all created secrets by running the command `docker secret ls`.

    For more information on the docker secret command, see [the docker secret documentation](https://docs.docker.com/engine/reference/commandline/secret_create/).

3.  Update the **MID\_SECRETS\_FILE** environment variable with the path to the secret file inside the container.

    The default path for Docker Swarm secrets on Linux is `/run/secrets/mid-secrets.properties`.

4.  Deploy the MID Server Image Container to Swarm using the docker service create command: `docker service create --name mid-service --secret mid-secrets.properties --env-file mid.env <docker-tag or image-id>`

    Make sure that the `--secret flag` is provided for the container service to associate with the specified secrets.


## Pass sensitive data to a mutual authenticated containerized MID Server with Docker Secrets

You can configure containerized MID Servers with configuration parameters passed through environment variables or secret files.

### Before you begin

Role required: admin

Role required: Docker Swarm admin

### About this task

If [certificate based authentication](https://www.servicenow.com/docs/access?context=set-up-mutual-auth&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) is enabled on the instance, the MID Server can be configured to [auto-validate using a mutual authentication client certificate](install-mid-mutual-auth.md) \(PEM file\). This can be done via setting the full path to the PEM certificate file inside container with the *MID\_MUTUAL\_AUTH\_PEM\_FILE* environment variable. For example, you can update variable to *MID\_MUTUAL\_AUTH\_PEM\_FILE= /run/secrets/certificate.pem* in the `mid.env` file.

You can pass the PEM certificate file into a container using Docker or Kubernetes secret. The following is an example command to pass the PEM certificate file into a container: `docker service create --name mid-service --secret mid-secrets.properties --secret <certificate-secret-name> --env-file mid.env <docker-tag or image-id>`

The mutual PEM certificate is installed on the MID Server during initialization. MID Server then connects to the instance and auto-validates. When the MID Server connects to the instance with mutual authentication successfully enabled, you might observe some of the following entries in the MID agent log:

-   Installed custom certificate into the MID keystore
-   Configured MID to use mutual authentication

### Procedure

1.  Prepare the mutual authentication PEM bundle.

2.  Create a docker secret using the docker secret create command: `docker secret create mutual-auth-secret <mutual-auth-pem-file-on-local-filesystem> .`

    You can list all created secrets by running the command `docker secret ls`.

3.  Update the **MID\_MUTUAL\_AUTH\_PEM\_FILE** environment variable with the path to the secret file inside the container.

    The default path for Docker Swarm secrets on Linux is `/run/secrets/<mutual-auth-pem-file-name>`.

4.  Deploy the MID Server Image Container to Swarm using the docker service create command: d`ocker service create --name mid-service --secret mutual-auth-secret --env-file mid.env <docker-tag or image-id>`

    Ensure the `--secret` flag is provided for the container service to associate with the specified secrets.

5.  Deploy the containerized MID Server to the pod with the **deployment.yml** and run the command: `kubectl create -f deployment.yml`


## Pass sensitive data to a containerized MID Server with Kubernetes Secrets

You can configure containerized MID Servers with configuration parameters passed through environment variables or secret files.

### Before you begin

Role required: Kubernetest admin

Setup and start [Kubernertes cluster](https://kubernetes.io/docs/setup/) before using this procedure. For more information on Kubernetes Secrets, see the [Kubernertes secrets documentation](https://kubernetes.io/docs/concepts/configuration/secret/).

**Note:** Kubernetes doesn’t work directly with a local image. Upload the MID Server image to a public registry or setup a local registry. See [the official Docker instruction](https://docs.docker.com/registry/) on building a docker registry.

When creating deployments, ensure that the replicas are kept to 1.

### Procedure

1.  Place the sensitive data in mid-secrets.properties accordingly.

2.  Create a Kubernetes secret with the command: `kubectl create secret generic mid-secret --from-file=mid-secrets.properties`

3.  You can list all created secrets by running the command: `kubectl get secrets`

4.  Update the **MID\_SECRETS\_FILE** environment variable with the path to the secret file inside container.

    The path is defined in [data field when creating a configuration file for a Secret](https://kubernetes.io/docs/concepts/configuration/secret/).

5.  Create a deployment with the following sample YML content:

    ```
    apiVersion: apps/v1
    kind: Deployment
    metadata:
      name: basic-example
    spec:
      selector:
        matchLabels:
          app: MIDServerManagement
          provider: ServiceNow
      replicas: 1
      template:
        metadata:
          labels:
            app: MIDServerManagement
            provider: ServiceNow
        spec:
          containers:
            - name: basic-example-container
              imagePullPolicy: IfNotPresent
              image: "mid:imageTag"
              env:
                - name: MID_INSTANCE_URL
                  value: " https://exampleinstance.service-now.com/"
                - name: MID_INSTANCE_USERNAME
                  value: "mid_server_user_name”
                - name: MID_SECRETS_FILE
                  value: "/opt/snc_mid_server/secrets/mid-secrets.properties“
                - name: MID_SERVER_NAME
                  value: "Basic-Example-MID"
              volumeMounts:
                - mountPath: "/opt/snc_mid_server/secrets"
                  name: "mid-mount-secret"
                  readOnly: true
          volumes:
          - name: "mid-mount-secret"
            secret:
              secretName: "mid-secret"
    
    ```

    **Note:** There are many ways to create a deployment or pod. For more information, see the [Kubernetes deployment instructions](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/).  

6.  Deploy the containerized MID Server to the pod with the deployment.yml and run the command: `kubectl create -f deployment.yml`


## Pass sensitive data to a mutual authenticated containerized MID Server with Kubernetes Secrets

You can configure containerized MID Servers with configuration parameters passed through environment variables or secret files.

### Before you begin

Role required: Kubernetest admin

Prerequisites:

If [certificate based authentication](https://www.servicenow.com/docs/access?context=set-up-mutual-auth&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) is enabled on the instance, the MID Server can be configured to [auto-validate using a mutual authentication client certificate](install-mid-mutual-auth.md) \(PEM file\). This can be done via setting the full path to the PEM certificate file inside container with the *MID\_MUTUAL\_AUTH\_PEM\_FILE* environment variable. You can pass the PEM certificate file into a container using Kubernetes secret.

The mutual PEM certificate is installed on the MID Server during initialization. MID Server then connects to the instance and auto-validates. When the MID Server connects to the instance with mutual authentication successfully enabled, you might observe some of the following entries in the MID agent log:

-   Installed custom certificate into the MID keystore
-   Configured MID to use mutual authentication

### Procedure

1.  Prepare the mutual authentication PEM bundle.

2.  Create a Kubernetes secret with the command: `kubectl create secret generic mutual-auth-secret --from-file=<mutual-auth-pem-file>`

3.  You can check all created secrets by running the command: `kubectl get secrets`

4.  Update the **MID\_MUTUAL\_AUTH\_PEM\_FILE** environment variable with the path to the secret file inside container.

5.  Create a deployment with the following sample YML content:

    ```
    6.	apiVersion: apps/v1
    7.	kind: Deployment
    8.	metadata:
    9.	  name: mutual-auth-example
    10.	spec:
    11.	  selector:
    12.	    matchLabels:
    13.	      app: MIDServerManagement
    14.	      provider: ServiceNow
    15.	  replicas: 1
    16.	  template:
    17.	    metadata:
    18.	      labels:
    19.	        app: MIDServerManagement
    20.	        provider: ServiceNow
    21.	    spec:
    22.	      containers:
    23.	        - name: mutual-auth -container
    24.	          imagePullPolicy: IfNotPresent
    25.	          image: "mid:imageTag”
    26.	          env:
    27.	            - name: MID_INSTANCE_URL
    28.	              value: "https://exampleinstance.service-now.com/"
    29.	            - name: MID_INSTANCE_USERNAME
    30.	              value: "mid_server_user_name”
    31.	            - name: MID_SERVER_NAME
    32.	              value: "Mutual-Auth-Deployment-MID"
    33.	            - name: MID_MUTUAL_AUTH_PEM_FILE
    34.	              value: "/opt/snc_mid_server/mutual-auth/yourpemfile.pem"
    35.	          volumeMounts:
    36.	            - mountPath: "/opt/snc_mid_server/mutual-auth"
    37.	              name: "mid-mount-mutual-auth"
    38.	              readOnly: true
    39.	      volumes:
    40.	      - name: "mid-mount-mutual-auth"
    41.	        secret:
    42.	          secretName: "mid-mutual-auth-secret"
    
    ```

6.  Deploy the containerized MID Server to the pod with the **deployment.yml** and run the command: `kubectl create -f deployment.yml`


