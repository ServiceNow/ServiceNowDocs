---
title: Configure the application repository on an air-gapped instance
description: After installing the application repository, you must configure it using the following procedure.
locale: en-US
release: australia
product: Application Repository \(Self-Hosted\)
classification: application-repository-self-hosted
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Application Repository for self-hosted, air-gapped customers, ServiceNow application repository, Application sharing, Administer your apps, Deploying applications, Building applications]
---

# Configure the application repository on an air-gapped instance

After installing the application repository, you must configure it using the following procedure.

## Before you begin

Role required: You’ll need the maint role to install and configure, and then only the admin role after the configuration is complete.

## Procedure

1.  Pair an instance with the application repository.

    1.  Log in to the instance you want to connect to the application repository.

    2.  Set the system property **sn\_appclient.repository\_base\_url** to the URL of your application repository instance.

        For example, `http://localhost:8080/`.

    3.  Clear the values of the **sn\_appclient.upload\_base\_url** and **sn\_appauthor.upload\_base\_url** properties.

    4.  Set the value of the **sn\_apprepo.credential** property in a Global scope to any non-null value, such as "secret."

        1.  SSH into the instance.
        2.  Change the directory to `/root/instance/instance_<portno>/conf/overrides.d` using `cd /root/instance/instance_<portno>/conf/overrides.d`.
        3.  Open / Create the `glide.properties` file.
        4.  Add the credential property to the end and save the file `[sn_apprepo.credential=<value>]`.
        5.  \(Shutdown.sh/Startup.sh\) Restart the glide, or run `Packages.com.glide.util.GlideProperties.loadPropertyFile(new Packages.java.io.File(gs.getProperty("glide.home.dist")+"/conf/overrides.d/glide.properties"));` in background scripts to dynamically load the properties file at runtime without restarting the instance.
        6.  Verify by printing the property in a background script `gs.info(gs.getProperty("sn_apprepo.credential"));`.
    5.  Add **sn\_appclient.repo\_auth\_name** with **sn\_repo.AppRepo** as its value.

    6.  Set the **glide.test\_instance** property to **False** on both the application repository instance and the client instance.

    7.  Set the **sn\_appclient.client\_calls\_allowed** property to **True**.

        **Note:** A scheduled job might set this property to **False** when not connected.

    8.  Set the **sn\_appclient.app.install.offline** property to **False** on the client instance.

    9.  Select **Submit**.

2.  Log in to the instance where the application repository is installed and complete the following steps.

    1.  Navigate to the **core\_company.list** table and ensure there is a record with the **Primary** field set to **True** or create one with any user-defined name.

        **Note:** The details of this record are not important.

    2.  Access the **sn\_repo\_instance.do** screen and create a new instance record for the client instance that you want to connect.

        1.  Ensure that **State** is set to Pairing.
        2.  Enter the name of the instance that you want to connect \(on the **stats.do** screen on that instance\) in the **Name** field.
        3.  Leave all other fields empty. They’re populated automatically.
    3.  Repeat the previous step for any additional instances that you want to connect.

3.  Log back in to the instance you used in Step 1 \(the instance that you want to pair with the application repository\) and navigate to the **Scripts - Background** module.

    1.  Select **sn\_appauthor scope** from the drop-down list.

    2.  Run the following script: `new ConfigChecker().checkForChanges()`.

4.  To remove the instance, navigate to the Instance record \(sn\_repo\_instance table\) and change the State to **Blocked**, which temporarily restricts access to the instance, or delete the instance.

    If you need the instance again, you can change the State to **Paired** again.

    **Warning:** If the instance name, instance ID, or credential of a paired instance changes, it must be paired again. Manually updating any of these values on the instance record isn’t recommended.


## What to do next

After an instance is paired, it’s fully set up to use the application repository. You can test your configuration by publishing a scoped application as described in [Publish an application to the application repository](t_PublishAppsToTheAppRepository.md). After publishing, you can verify that the app was successfully published by locating it in **All** &gt; **Application Repository** &gt; **Artifacts** &gt; **Internal Apps**.

