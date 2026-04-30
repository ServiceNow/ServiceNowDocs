---
title: External credential storage configuration
description: Configure your instance to obtain credentials from a remote repository.Create a JAR file to resolve credential identifiers sent from the MID Server into actual credentials from the repository.Import a JAR file created to resolve credential identifiers sent from the MID Server into actual credentials from the repository.Configure the credential identifier in the instance.Configure your instance to obtain credentials from a remote repository.
locale: en-US
release: zurich
product: Connections and Credentials
classification: connections-and-credentials
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [External credential storage, Get started with credentials, Connections and Credentials, Access Management]
---

# External credential storage configuration

Configure your instance to obtain credentials from a remote repository.

These procedures assume that you already have an external repository configured with the credentials you want to protect. The credential identifier configured in the ServiceNow instance must be mapped to the actual credential in the repository through the JAR file.

**Note:** ServiceNow supports two external vaults at a time: one default CyberArk credential resolver, and one custom external credential resolver. Creating a custom CyberArk credential resolver still uses the second, custom external vault, and no additional custom external vaults can be used.

To configure External Credential Storage, complete the following tasks in order.

**Parent Topic:**[External credential storage](c_ExternalCredentialStorage.md)

## Create a JAR file to resolve credentials

Create a JAR file to resolve credential identifiers sent from the MID Server into actual credentials from the repository.

### Before you begin

Role required: agent\_admin or admin

Make sure to include all the credential elements that the instance expects, such as the private key.

To create a JAR file to resolve credentials:

### Procedure

1.  Use either the templates provided on the ServiceNow github or the sample Java file.

    **Caution:**

    These samples are intended as a template only. Do **NOT** use this code in production without modifying it for your environment.

    1.  Download the open source JAR files with instructions from the ServiceNow github:

        -   [HashiCorp External Credential Resolver](http://github.com/ServiceNow/mid-hashicorp-external-credential-resolver)
        -   [CyberArk External Credential Resolver](http://github.com/ServiceNow/mid-cyberark-external-credential-resolver)
    2.  Use the following sample Java file as a template and modify it to suit your environment:

        ```
        
        package com.snc.discovery;
        
        import java.util.*;
        import java.io.*;
        
        /**
         * Basic implementation of a CredentialResolver that uses a properties file.
         */
        
        public class CredentialResolver {
        
        	private static String ENV_VAR = "CREDENTIAL_RESOLVER_FILE";
        	private static String DEFAULT_PROP_FILE_PATH = "C:\\dummycredentials.properties";
        
        	// These are the permissible names of arguments passed INTO the resolve()
        	// method.
        
        	// the string identifier as configured on the ServiceNow instance...
        	public static final String ARG_ID = "id";
        
        	// a dotted-form string IPv4 address (like "10.22.231.12") of the target
        	// system...
        	public static final String ARG_IP = "ip";
        
        	// the string type (ssh, snmp, etc.) of credential as configured on the
        	// instance...
        	public static final String ARG_TYPE = "type";
        
        	// the string MID server making the request, as configured on the
        	// instance...
        	public static final String ARG_MID = "mid";
        
        	// These are the permissible names of values returned FROM the resolve()
        	// method.
        
        	// the string user name for the credential, if needed...
        	public static final String VAL_USER = "user";
        
        	// the string password for the credential, if needed...
        	public static final String VAL_PSWD = "pswd";
        
        	// the string pass phrase for the credential if needed:
        	public static final String VAL_PASSPHRASE = "passphrase";
        
        	// the string private key for the credential, if needed...
        	public static final String VAL_PKEY = "pkey";
        
        	// the string authentication protocol for the credential, if needed...
        	public static final String VAL_AUTHPROTO = "authprotocol";
        
        	// the string authentication key for the credential, if needed...
        	public static final String VAL_AUTHKEY = "authkey";
        
        	// the string privacy protocol for the credential, if needed...
        	public static final String VAL_PRIVPROTO = "privprotocol";
        
        	// the string privacy key for the credential, if needed...
        	public static final String VAL_PRIVKEY = "privkey";
        
        
        	private Properties fProps;
        
        	public CredentialResolver() {
        	}
        
        	private void loadProps() {
        		if(fProps == null)
        			fProps = new Properties();
        
        		try {
        			String propFilePath = System.getenv(ENV_VAR);
        			if(propFilePath == null) {
        				System.err.println("Environment var "+ENV_VAR+" not found. Using default file: "+DEFAULT_PROP_FILE_PATH);
        				propFilePath = DEFAULT_PROP_FILE_PATH;
        			}
        
        			File propFile = new File(propFilePath);
        			if(!propFile.exists() || !propFile.canRead()) {
        				System.err.println("Can't open "+propFile.getAbsolutePath());
        			}
        			else {
        				InputStream propsIn = new FileInputStream(propFile);
        				fProps.load(propsIn);
        			}
        			//fProps.load(CredentialResolver.class.getClassLoader().getResourceAsStream("dummycredentials.properties"));
        		} catch (IOException e) {
        			System.err.println("Problem loading credentials file:");
        			e.printStackTrace();
        		}
        	}
        
        	/**
        	 * Resolve a credential.
        	 */
        	public Map resolve(Map args) {
        		loadProps();
        		String id = (String) args.get(ARG_ID);
        		String type = (String) args.get(ARG_TYPE);
        		String keyPrefix = id+"."+type+".";
        
        		if(id.equalsIgnoreCase("misbehave"))
        			throw new RuntimeException("I've been a baaaaaaaaad CredentialResolver!");
        
        		// the resolved credential is returned in a HashMap...
        		Map result = new HashMap();
        		result.put(VAL_USER, fProps.get(keyPrefix + VAL_USER));
        		result.put(VAL_PSWD, fProps.get(keyPrefix + VAL_PSWD));
        		result.put(VAL_PKEY, fProps.get(keyPrefix + VAL_PKEY));
        		result.put(VAL_PASSPHRASE, fProps.get(keyPrefix + VAL_PASSPHRASE));
        		result.put(VAL_AUTHPROTO, fProps.get(keyPrefix + VAL_AUTHPROTO));
        		result.put(VAL_AUTHKEY, fProps.get(keyPrefix + VAL_AUTHKEY));
        		result.put(VAL_PRIVPROTO, fProps.get(keyPrefix + VAL_PRIVPROTO));
        		result.put(VAL_PRIVKEY, fProps.get(keyPrefix + VAL_PRIVKEY));
        
        		System.err.println("Error while resolving credential id/type["+id+"/"+type+"]");
        
        		return result;
        	}
        
        
        	/**
        	 * Return the API version supported by this class.
        	 */
        	public String getVersion() {
        		return "1.0";
        	}
        
        	public static void main(String[] args) {
        		CredentialResolver obj = new CredentialResolver();
        		obj.loadProps();
        
        		System.err.println("I spy the following credentials: ");
        		for(Object key: obj.fProps.keySet()) {
        			System.err.println(key+": "+obj.fProps.get(key));
        		}
        
        	}
        }
        ```


## Import a JAR file to resolve credentials

Import a JAR file created to resolve credential identifiers sent from the MID Server into actual credentials from the repository.

### Before you begin

Role required: agent\_admin or admin

After you [create the JAR file](external_cred_storage_configuration.md#), import it into the instance, where it becomes accessible to the MID Server.

### Procedure

1.  After creating the JAR and properties files, copy the properties file to the MID Server.

2.  Navigate to **MID Server** &gt; **JAR Files**.

3.  Click **New**.

4.  Complete the following fields:

    |Field|Description|
    |-----|-----------|
    |Name|A unique and descriptive name for identifying the file in the instance.|
    |Version|A version number for the file, if one is available.|
    |Source|Location of the JAR file for reference purposes. Source information is not used by the system.|
    |Description|Short description of the JAR file and its purpose in the instance.|

5.  Click the paper clip icon in the banner and attach the JAR file to the record.

    ![The paper clip icon appears next to the Submit button.](../image/AttachingAJARFile.png "Attaching a JAR file")

6.  Click **Submit**.

7.  Restart the MID Server service.

    The platform makes the JAR file available to any MID Server configured to communicate with the instance.


## Configure the credential identifier

Configure the credential identifier in the instance.

### Before you begin

Role required: admin

Verify the following items:

-   The [External Credential Storage](../task/t_ActivateExtrnlCredStoragePlugIn.md) plugin must be active.
-   The [Enable External Credential Storage](c_ExternalCredentialStorage.md) Discovery property is enabled.

### Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Credentials** or **Orchestration** &gt; **Credentials**.

2.  Click **New**.

3.  Select a credential type.

4.  Select the **External credential store** check box.

    The **User name** and **Password** fields disappear, and the **Credential ID** field and **Credential storage vault** menu appear.

5.  From the **Credential storage vault** menu, select either None, the CyberArk vault, or a custom external credential storage vault.

    **Note:**

    If CyberArk vault is selected, the **Lookup key** menu appears with four lookup key choices: Credential ID, IP Address, FQDN, All of the above. Selecting All of the above can degrade performance because it requires accessing the vault multiple times.

    1.  To use a custom external credential storage vault, navigate to Vault Configurations \[vault\_configuration.list\] in the instance.

    2.  Create a new record using a name associated an imported JAR file for a custom credential resolver.

        See the procedures [Create a JAR file to resolve credentials](external_cred_storage_configuration.md#) and [Import a JAR file to resolve credentials](external_cred_storage_configuration.md#) for information on creating a custom external credential storage vault.

6.  Complete the Credentials form using the fields from the following table.

<table id="table_xhq_3lc_rw"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique and descriptive name for this credential.

</td></tr><tr><td>

Active

</td><td>

Enable or disable these credentials for use.

</td></tr><tr><td>

Credential ID

</td><td>

Enter the unique key configured for external credentials in the JAR file uploaded to the MID Server for an external credential system. This is the ID passed to the Java class in the parameter map:```
public static final String ARG_ID   = "id";
```

The MID Server uses this identifier to resolve the actual credentials on the repository.**Note:** This field is only visible when the **External credential store** check box is selected.

</td></tr><tr><td>

Tag

</td><td>

Allow workflow creators to assign individual credentials to any activity in an Orchestration workflow or assign different credentials to each occurrence of the same activity type in an Orchestration workflow.

</td></tr><tr><td>

External credential store

</td><td>

Select this check box to use an external credential storage system. When you select this option the **User name** and **Password** fields are replaced with the **Credential ID** field. External credential storage is only available when the [External Credential Storage plugin](../task/t_ActivateExtrnlCredStoragePlugIn.md) in activated.

</td></tr><tr><td>

Credential storage vault

</td><td>

Choose the external credential storage vault from a list of available vaults. The menu is composed of records from the Vault Configurations \[vault\_configuration.list\]. New records can be added and use names associated with custom credential resolver JAR files. See the procedures [Create a JAR file to resolve credentials](external_cred_storage_configuration.md#) and [Import a JAR file to resolve credentials](external_cred_storage_configuration.md#) for information on creating a custom external credential storage vault.

</td></tr><tr><td>

Applies to

</td><td>

Select whether to apply these credentials to **All MID servers** in your network, or to one or more **Specific MID servers**. Specify the MID Servers that should use these credentials in the **MID servers** field.

</td></tr><tr><td>

MID servers

</td><td>

Select one or more MID Servers from the list of available MID Servers. The credentials configured in this record are available to the MID Servers in this list. This field is available only when you select **Specific MID servers** from the **Applies to** field.

</td></tr><tr><td>

Order

</td><td>

Enter the order \(sequence\) in which the platform tries this credential as it attempts to log onto devices. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), Discovery or Orchestration tries the credentials in a random order.

</td></tr></tbody>
</table>7.  Click **Submit**.


## Configure the credential identifier for AWS

Configure your instance to obtain credentials from a remote repository.

### Before you begin

Role required: cloud\_admin

Verify that these plugins are active, and the MID Server has been installed:

-   Discovery \[com.snc.discovery\]
-   Cloud Provisioning and Governance \[com.snc.cloud.mgmt\]
-   External Credential Storage \[com.snc.discovery.external\_credentials\]

### About this task

These procedures assume that you already have an external repository configured with the credentials you want to protect. The credential identifier configured in the ServiceNow instance must be mapped to the actual credential in the repository through the JAR file.

### Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Credentials**.

2.  Select a credential that your external credential storage provider supports.

3.  Complete the form, using the fields from the table.

    |Field|Description|
    |-----|-----------|
    |Name|A unique and descriptive name for this credential. For example, Amazon Web Services.|
    |Active|Check box to enable or disable the credential.|
    |Credential ID|Enter the Name under which this credential is stored in the external credential storage provider.|
    |MID Servers|Select one or more MID Servers that can use these credentials.|
    |External credential store|Select this check box to use an external credential storage system. When external storage is enabled, the **Credential ID** field appears. If this check box is not visible, click the menu icon in the header bar and select **View** &gt; **External Storage** from the context menu.|
    |Credential storage vault|Select **CyberArk**.|

4.  Click **Submit**.


