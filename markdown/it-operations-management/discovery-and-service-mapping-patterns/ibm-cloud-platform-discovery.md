---
title: IBM Cloud Platform discovery
description: The ServiceNow Discovery application finds IBM Cloud Platform components \(Softlayer API v3 and v3.1 and Bluemix API v2\) using the IBM Cloud Platform patterns. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 24
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# IBM Cloud Platform discovery

The ServiceNow Discovery application finds IBM Cloud Platform components \(Softlayer API v3 and v3.1 and Bluemix API v2\) using the IBM Cloud Platform patterns. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

You can use the patterns on the ServiceNow AI Platform using London Patch 7, Madrid Patch 2, or later releases.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **MID Server**

    Use a dedicated MID Server for cloud discovery. The MID Server must have 16 Cores, 8 GB with 4 GB Java Memory Model \(JVM\) memory allocation.

    Deploy and connect the dedicated MID Server with internet access.

-   **Credentials**

    The cloud resources are in an IBM cloud. Create the IBM Credentials for accessing your IBM account.

    1.  Navigate to **Discovery** &gt; **Credentials**.
    2.  Click **New**.
    3.  Click **IBM Credentials** and then fill in the form:

        |Field|Description|
        |-----|-----------|
        |Name|Credential name. An example is `ibm-cred`.|
        |Order|Order in which the platform tries this credential as it attempts to log on to devices. A smaller number indicates that the credential appears higher in the list. Establish the credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number, or none, the instance tries the credentials in a random order. The default value is 100.|
        |Softlayer API User|Username for the Softlayer API. Use the Softlayer API Username defined in the Softlayer console.|
        |Softlayer API Key|Key for the Softlayer API. Use the Softlayer API Key that is defined in the Softlayer console.|
        |Bluemix API Key|Key for the Bluemix API. Use the Bluemix API Key defined in the IBM Cloud console.|

    4.  Click **Submit**.
-   **Create an IBM cloud service account**

    Use the credentials defined in the preceding procedure to create the IBM cloud service account.


1.  Navigate to **Cloud Provisioning and Governance** &gt; **Service Accounts**.
2.  Click **New**.
3.  On the form, fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Name|Credential name. An example is `ibm-snow`|
    |Account Id|IBM account ID name. Enter the IBM Account ID.|
    |Discovery credentials|Discovery credentials that you defined earlier.|
    |Datacenter Type|Datacenter type. As an example, `IBM Datacenter [cmdb_ci_ibm_datacenter]`|

4.  Click **Submit**.

-   **Create a serverless Discovery schedule**

    Configure a serverless Discovery.

    1.  On the ServiceNow AI Platform, navigate to **Discovery** &gt; **Discovery Schedules**.
    2.  Click **New**.
    3.  On the form, fill in the fields:

        |Field|Description|
        |-----|-----------|
        |Name|Name for this Discovery schedule. As an example, `Serverless Pattern`|
        |Discover|Discover type. Select **Serverless**|
        |MID Server|Name of the MID Server. As an example, `Discovery_Server`|
        |Active|Option for enabling this schedule for Discovery. Select this check box to enable Discovery.|
        |Run|Specifies how frequently to run the Discovery schedule.|

    4.  Right-click the header of the Discovery Schedule form and select **Save**.

        ![Serverless execution pattern](../image/serverless-execution-pattern.png)

    5.  Click the **Serverless Execution Patterns** tab.
    6.  Click **New**.
    7.  On the form, fill in the fields:

<table id="table_k3d_bzy_fhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for this Serverless Execution Pattern. As an example, `IBM1`

</td></tr><tr><td>

Pattern

</td><td>

Name of the pattern that you want to run.![IBM patterns](../image/ibm-patterns.png)

 If you want to run multiple patterns, create multiple records.

</td></tr><tr><td>

Proxy Host

</td><td>

Fully qualified domain name of the machine on which you are installing the proxy server. Specify **Global**.

</td></tr><tr><td>

Active

</td><td>

Option for enabling this schedule for Discovery. Select this check box to enable Discovery.

</td></tr></tbody>
</table>    8.  Configure the parameters required by the IBM Cloud Platform pattern as follows:

        |Parameter|Description|
        |---------|-----------|
        |cloud\_cred\_id|The sys\_id of the IBM credentials specified into the configuration.|
        |cloud\_account\_id|The IBM account ID.|
        |cloud\_datacenter\_type|cmdb\_ci\_ibm\_datacenter|

    9.  **Update**.
    10. To start Discovery, navigate to the Serverless Discovery definition and click **Discover Now**.
-   **IBM flow - horizontal discovery**
    -   To perform a discovery using a serverless schedule, the IBM Cloud Platform patterns that were selected run and discover IBM Cloud Platform resources.
    -   To perform a discovery using a service account, a full IBM Cloud Platform discovery schedule runs, discovering all supported IBM Cloud Platform resources.
-   **Cloud custom operation**

    Cloud REST – Add Response to Context

    Operation for Cloud REST queries that supports large-scale responses and better memory usage.

    -   Specify all the fields with the same values as in the Cloud REST Query custom operation, except to specify the table for the response, which is set in the **Response Variable Name** field.

        ![Response field](../image/response-variable-name.png)

    -   Set **Define parsing** to None.
    Methods to retrieve data for the IBM account

    1.  Navigate to **Pattern Designer** &gt; **Custom Operations**.

        ![Cloud REST query](../image/cloud-rest-query.png)

    2.  Click **Cloud REST – add response to context**.
    Method: Get Call

    API URLs used to retrieve the data:

    -   Load Balancer **https://api.softlayer.com/rest&lt;api\_version&gt;/SoftLayer\_Network\_LBaaS\_LoadBalancer/getAllObjects?objectMask=mask\[listeners\[defaultPool\],members,healthMonitors\]**
    -   Network **https://api.softlayer.com/rest/&lt;API\_VERSION&gt;/SoftLayer\_Account/getNetworkVlans?objectMask=mask\[primaryRouter.datacenter,name,id,vlanNumber,networkSpace\]**
    -   Network **https://api.softlayer.com/rest/&lt;API\_VERSION&gt;/SoftLayer\_Account/getSubnets?objectMask=mask\[datacenter\]**
    -   Network**https://api.softlayer.com/rest/&lt;API\_VERSION&gt;/SoftLayer\_Account/getSecurityGroups?objectMask=mask\[rules\]**
    -   Organizations and Spaces **https://api.&lt;region&gt;.bluemix.net/v2/organizations**
    -   **https://api.&lt;region&gt;.bluemix.net/v2/spaces**
    -   SSH Key **https://api.softlayer.com/rest/v3/SoftLayer\_Account/SoftLayer\_Account/getSshKeys**
    -   Storage **https://api.softlayer.com/rest/&lt;api\_version&gt;/SoftLayer\_Account/getNetworkStorage**
    -   Virtual Server **https://api.softlayer.com/rest/v3.1/SoftLayer\_Account/getSecurityGroups**
    -   **http://api.softlayer.com/rest/v3.1/SoftLayer\_Account/getSecurityGroups?objectMask=mask\[id,name,networkComponentBindings\[networkComponentId,networkComponent\[networkId,guest\[fullyQualifiedDomainName,hostname,id,datacenter\[name\]\]\]\]\]**
    -   **https://api.softlayer.com/rest/v3.1/SoftLayer\_Account/getVirtualGuests?objectMask=mask\[hostname,domain,powerState,fullyQualifiedDomainName,notes,id,statusId,placementGroupId,sshKeys\[label,key,id,fingerprint,createDate,modifyDate,notes\],primaryBackendIpAddress,primaryIpAddress,networkVlans\[id,name,note,vlanNumber\],blockDeviceCount,blockDevices\[device,diskImageId,mountType,guestId,id,mountMode\],allowedNetworkStorage\[id,fileNetworkMountAddress,iscsiTargetIpAddresses,nasType,username,serviceResourceBackendIpAddress\],maxCpu,maxMemory,datacenter,networkComponentCount,regionalGroup,datacenter,location,operatingSystem\[id,softwareDescription\[id,name,longDescription,manufacturer,referenceCode,version\]\],networkComponents\[guestId,id,port,name,primarySubnet\[networkIdentifier,id,networkVlan\[id\]\],status,macAddress,primaryIpAddress\]\]**
-   **EVAL functions**

    Use the following EVAL function to transform the Load Balancer API response into a full JSON format. The default response is formatted as “\[&lt;resource objects&gt;\]”.

    ```
    var cloud_lb_response = ${cloud_lb_response};
    for (var i = 0; i < cloud_lb_response.size(); i++){
          cloud_lb_response.set(i, '{"result":[' + cloud_lb_response.get(i) + ']}');
    }
    CTX.setAttribute("cloud_lb_response", cloud_lb_response;
    
    ```

    Use the following EVAL function to transform the Network API response into a full JSON format. The default response is formatted as “\[&lt;resource objects&gt;\]”.

    ```
    var network_response = ${network_response};
    for (var i = 0; i < network_response.size(); i++){
          network_response.set(i, '{"result":[' + network_response.get(i) + ']}');
    }
    CTX.setAttribute("network_response", network_response);
    
    ```

    Use the following EVAL function to get the IBM region from the LB availability zone \(datacenter\). The same function is used for other resources inside the pattern.

    ```
    var res = "";
    res = IbmCloudDcToRegion.convertDctoRegion(${cloud_lb[].cloud_lb_az_short_name});
    
    
    ```

    Use the following EVAL function to select the required algorithm in the pattern.

    ```
    var rtrn
    var lb_algorithm = ${cloud_lb_pools[].lb_algorithm}.toString();
    switch (lb_algorithm){  
       case "ROUNDROBIN":
          lb_algorithm = "round-robin";
          break;    
       case "WEIGHTED_RR":
          lb_algorithm = "round-robin";
          break;          
       case "LEASTCONNECTION":
          lb_algorithm = "least-connections";
          break;     
       default: break;
    
    ```

    Use the following EVAL function to parse the unique region to the account that hosts the Organizations and the corresponding spaces.

    ```
    var tableWithoutDuplicates = '';
    tableWithoutDuplicates =  DuplicateRemover.removeDuplicates(${account_region},["region_name"]);
    CTX.setAttribute("account_region_unique",  tableWithoutDuplicates);
    
    ```

    Use the following EVAL function to get information for all the organizations that are assigned to the IBM cloud account, where iteration for getting the unique region is performed.

    ```
    var cloudcall = new CloudRestAPIClient();
    var resourceTable = ${account_region_unique[*].region_name};
    var tableSize = resourceTable.size();                                     
    var tmp_response = new Packages.java.util.ArrayList();
    var all_organizations_response = new Packages.java.util.ArrayList();
    for (var i = 0; i < tableSize ; i++){
       if  (!resourceTable.get(i)) continue;
       var url = "https://api."+resourceTable.get(i)+".bluemix.net/v2/organizations";
       tmp_response = cloudcall.arrayListExecute(${service_account}, null, url, null, 'GET', null, 'true', CTX);
       
       for (var j = 0; j < tmp_response.size(); j++){
          all_organizations_response.add('{"result":[' + tmp_response.get(j) + ']}');
       }
    }
    CTX.setAttribute("all_organizations_response", all_organizations_response);
    
    ```

    Use the following EVAL function to get information for all the IBM cloud account assigned spaces, where the iteration for getting the unique region is performed.

    ```
    var rtrn = '';
    var cloudcall = new CloudRestAPIClient();
    var resultList = new Packages.java.util.ArrayList();
    var rest = '';
    var resourceTable = ${account_region_unique[*].region_name};
    var result = new Packages.java.util.ArrayList();
    var all_organizations_response = ${all_organizations_response}
    for (var i = 0; i < resourceTable.size() ; i++){
       var url = "https://api."+resourceTable.get(i)+".bluemix.net/v2/spaces";
       result = cloudcall.arrayListExecute(${service_account}, null, url, null, 'GET', null, 'true', CTX);
       for (var z = 0; z < all_organizations_response.size(); z++){
          var jsonObj = JSON.parse(result.get(z));
          ms.log("length "+jsonObj.resources.length);
    for(var j=0;j<jsonObj.resources.length;j++){
             var guid = jsonObj.resources[j].metadata.guid;
             var url = jsonObj.resources[j].metadata.url;
             var name = jsonObj.resources[j].entity.name;
             var organization_guid = jsonObj.resources[j].entity.organization_guid;
             var allow_ssh = jsonObj.resources[j].entity.allow_ssh ? "true" : "false";
             var row = new Packages.java.util.HashMap();
     Packages.com.snc.sw.log.DiscoLog.getLogger("IBM Cloud Space and Org").debug(">>>>>>>>>>>>>||||||||||||>>>>>> region alias=" + resourceTable.get(i)); 
             Packages.com.snc.sw.log.DiscoLog.getLogger("IBM Cloud Space and Org").debug(">>>>>>>>>>>>>||||||||||||>>>>>> region full name=" + IbmCloudDcToRegion.regionNamebyAlias(resourceTable.get(i))); 
             row.put("region", IbmCloudDcToRegion.regionNamebyAlias(resourceTable.get(i)));
             row.put("space_guid",guid);
             row.put("space_url",url);
             row.put("space_name",name);
             row.put("space_organization_guid",organization_guid);
             row.put("space_allow_ssh",allow_ssh);
             row.put("rest", rest);
             resultList.add(row);
          }
       }
       CTX.setAttribute('spaces_table', resultList);
    }
         
    
    ```

    Use the following EVAL function to filter all the spaces by unique region.

    ```
    var space_region = ${spaces_table[].region};
    
    Packages.com.snc.sw.log.DiscoLog.getLogger("IBM Cloud Space and Org").debug("filtering space according to LDC. space_region=" + space_region);
    var regions = ${cmdb_ci_ibm_datacenter[*].region};
    Packages.com.snc.sw.log.DiscoLog.getLogger("IBM Cloud Space and Org").debug("input regions list=" + regions.toString());
    
    var rtrn = "false";
    if(regions.contains(space_region)) {
        rtrn = "true";
    }
    rtrn;
    
    ```

    Use the following EVAL function to filter all the spaces by storage discovery.

    ```
    var storage_response = ${storage_response};
    for (var i = 0; i < storage_response.size(); i++){
          storage_response.set(i, '{"result":[' + storage_response.get(i) + ']}');
    }
    CTX.setAttribute("storage_response", storage_response);
    
    
    ```

    Use the following EVAL function to transform the API response into full JSON format, as the untouched response is formatted as “\[&lt;resource objects&gt;\]”.

    ```
    var ssh_key = ${ssh_key_json};
    for(var i = 0; i < ssh_key.size(); i++){
       ssh_key.set(i,'{"result\" : ' + ssh_key.get(i) + "}");
    }
    CTX.setAttribute("ssh_key_json", ssh_key);
    
    ```

    Use the following EVAL function to populate the availability zone into the storage volume table.

    ```
    var rtrn;
    var resource_group = ${network_storage[].resource_name};
    var regex = /.*-(\w{3}\d{2}).*/;
    var az_name = regex.exec(resource_group);
    if (az_name) {
       rtrn = az_name[1];
    } else {
       rtrn;
    }
    
    ```

    Use the following EVAL function to populate the region into the storage volume table.

    ```
    var res = "";
    res = IbmCloudDcToRegion.convertDctoRegion(${network_storage[].availability_zone});
    
    
    ```

    Use the following EVAL function to transform the size of the storages to bytes from gigabytes.

    ```
    var rtrn = '';
    
    var size = ${network_storage[].size};
    
    rtrn = (parseInt(size) * 1073741824) + ‘’;
    
    ```

    Use the following EVAL function to transform the size of the storages to bytes from gigabytes.

    ```
    var cloudcall = new CloudRestAPIClient();
    var resourceTable = ${network_storage[*].storage_object_id};
    var tableSize = resourceTable.size();
    var allResources = new Packages.java.util.ArrayList();
    var response = new Packages.java.util.ArrayList();
    for (var i = 0; i < tableSize ; i++){
       if  (!resourceTable.get(i)) continue;
       var url = "https://api.softlayer.com/rest/"+${api_version}+"/SoftLayer_Network_Storage/"+resourceTable.get(i)+"/getObject?objectMask=mask[snapshots]";
       // the commented out code is to call the "Cloud Rest Call" API
       
       allResources = cloudcall.arrayListExecute(${service_account}, null, url, null, 'GET', null, 'true', CTX);
       for (var j = 0; j < allResources.size(); j++){
          response.add('{"result":[' + allResources.get(j) + ']}');
       }
    }
    CTX.setAttribute("all_snapshots_response", response);
    
    ```

    Use the following EVAL closure that transforms the JSON that is received from the API to a format that the JSON parser can work with. The default JSON is saved in `$vm_json_array`, the new JSON is in `$vm_json`.

    ```
    var vm_json = new Packages.java.util.ArrayList();
    vm_json.addAll(${vm_json_array});
    
    for (var i = 0 ; i < vm_json.size(); i++){
          vm_json.set(i, '{\"result\":[' + vm_json.get(i) + ']}');
    }
    
    CTX.setAttribute("vm_json", vm_json); 
    
    ```

    Use the following EVAL closure that returns ‘on’ if the power status is running. The value ‘off’ is returned if the power status is off.

    ```
    var power = ${cmdb_ci_vm_instance[].state};
    var rtrn = '';
    
    if (power == 'Running'){
       rtrn = "on";
    }
    else {
       rtrn = "off"
    } 
    
    ```

    Use the following EVAL closure that returns the region of the CI, based on provided availability zone name.

    ```
    var az = ${cmdb_ci_vm_instance[].avail_zone};
    var rtrn = '';
    rtrn = IbmCloudDcToRegion.convertDctoRegion(az);
    
    ```

    Use the following EVAL closure that builds a HashMap of HashSets, Connecting VMs with their network storages. The following key is used:

    -   P = page
    -   V = VM
    -   N = network storage
    ```
    var rtrn = '';
    var vmJson = ${vm_json_array};
    var VMtoStorageHashMap = new Packages.java.util.HashMap();
    
    for (var p = 0 ; p < vmJson.size(); p++){
       var page = JSON.parse(vmJson.get(p));
       for (var now_V in page){
          if (page[v].allowedNetworkStorage.length > 0){
             var vm_id = page[v].id + '';
             var storageSet = new Packages.java.util.HashSet();
             for (var n in page[v].allowedNetworkStorage){
                storageSet.add(page[v].allowedNetworkStorage[n].id + '');
             }
             VMtoStorageHashMap.put(vm_id,storageSet);
          }
       }
    }
    CTX.setAttribute("VMStorageCache", VMtoStorageHashMap); 
    
    ```

    Use the following EVAL closure to remove duplicate entries from tables.

    ```
    var tableWithoutDuplicates = '';
    tableWithoutDuplicates = DuplicateRemover.removeDuplicates(${cmdb_ci_os_template},["object_id"]);
    CTX.setAttribute("cmdb_ci_os_template", tableWithoutDuplicates);
    
    ```

    Use the following EVAL closure that builds a list of VM IDs that are related to the current security group ID.

    ```
    var rtrn = '';
    //get the Security Group ID of the current record in the table for comparison
    var current_table_id = ${security_groups[].sec_group_id};
    var current_table_id_string = current_table_id + '';
    
    // get the list of instance's ID that will be then added to Security Group table
    var needed_value_id_list = ${sec_group_network_components[*].vm_instance_id};
    //get the list of Security Group IDs in the Network Component table, which will then be compared one by one to the current record of the security_groups table
    var compare_id_list = ${sec_group_network_components[*].sec_group_id};
    
    var beforeReturn = '';
    var separator = '';
    for (var i = 0; i <  compare_id_list.size(); i++)   {
       
       if   (current_table_id_string == compare_id_list.get(i)){
          
          beforeReturn += separator + needed_value_id_list.get(i);
          separator = ',';
       }
    }
    rtrn = beforeReturn;
    
    ```

    Use the following EVAL closure that builds a HashMap of HashSet between security groups and the VMs that are configured to use them.

    ```
    rtrn = '';
    var secGroupTable = ${cmdb_ci_endpoint_comp_security};
    var secToVMHashSet = new Packages.java.util.HashMap();
    
    // this loop worst case O(N*M) M = security groups, N = VMs
    for(var i=0; i<secGroupTable.size(); i++){
       var securityTableId = secGroupTable.get(i).get('object_id');
       var vmListStr = secGroupTable.get(i).get('instance_list');
       var vmList = vmListStr.split(",");
    
       var vmSet = new Packages.java.util.HashSet();
       for (var j in vmList){
          vmSet.add(vmList[j]);
       }
    
       secToVMHashSet.put(securityTableId,vmSet);
    }
    CTX.setAttribute("securityVMCache",  secToVMHashSet);
    
    ```

    Use the following EVAL closure that returns ‘true’ if the current VM is using the current security group ID.

    ```
    var rtrn = '';
    var vm_id = ${cmdb_ci_vm_instance[].object_id};
    var vmHashSet = ${securityVMCache}.get(${cmdb_ci_endpoint_comp_security[].object_id});
    rtrn = vmHashSet.contains(vm_id);
    
    ```

    Use the following EVAL closure that returns ‘true’ if the current VM is using the current storage volume.

    ```
    var rtrn = '';
    var vm_id = ${cmdb_ci_vm_instance[].object_id};
    var vol_id = ${cmdb_ci_endpoint_iscsi[].object_id};
    var vmHashSet = ${VMStorageCache}.get(vm_id);
    if (vmHashSet){
       rtrn = vmHashSet.contains(vol_id);
    }
    else {
       rtrn = 'false'
    }
    
    ```

    Use the following EVAL function to transform the API response into full JSON format, as the untouched response is formatted as “\[&lt;resource objects&gt;\]”.

    ```
    var cloud_response = ${location_groups_response}
    for (var i = 0; i < cloud_response.size(); i++){
        cloud_response.set(I, '{"result":[' + cloud_response.get(i) + ']}');
    }
    CTX.setAttribute("location_groups_response", cloud_response);
    ```

    Parses the unique Location Groups in the “location\_groups\_az” table basdon the column “lg\_id” and creates a new table "location\_groups\_az\_unique“ that contains the result.

    ```
    var tableWithoutDuplicates= '';
    tableWithoutDuplicates = DuplicateRemover.removeDuplicates(${location_groups_az},["lg_id"]);
    CTX.setAttribute("location_groups_az_unique", tableWithoutDuplicates);
    ```

    Creates a list of Availability Zones per Location Group, that is stored in a column new column in the location\_groups\_az\_uniquetable. The list records are divided by commas purposely, so that unique relations could be made in consecutive step.

    ```
    var current_table_id= ${location_groups_az_unique[].lg_id};
    var current_table_id_string = current_table_id+ '';
    var needed_v alue_id_list = ${location_groups_az[*].lg_az_id};
    var compare_id_list= ${location_groups_az[*].lg_id};
    var beforeReturn= '';
    var separator = ',';
    for (var i= 0; i< compare_id_list.size(); i++)  {
        if (current_table_id_string == compare_id_list.get(i)){
        beforeReturn += separator + needed_v alue_id_list.get(i) + separator;
      }
    }
    rtrn = beforeReturn;
    ```

-   **Activate the cloud-related CI relationships**

    To include discovered components into application services, enable CI relationships used in tag-based discovery by Service Mapping. These CI relationships are available from the 1.0.68 release on the ServiceNow Store. For operational steps, see [Tag-based discovery configuration](../concept/tag_discovery_configuration.md).


## Data collected by Discovery during horizontal discovery

Data is collected using these patterns:

-   IBM Cloud Load Balancer
-   IBM Cloud Location Groups
-   IBM Cloud Network
-   IBM Cloud Organizations and Spaces
-   IBM Cloud Resource Groups
-   IBM Cloud SSH Key
-   IBM Cloud Storage
-   IBM Cloud Virtual Server

Data collected for IBM components:

-   **IBM Cloud Load Balancer discovered resources**

<table id="table_o21_dlv_2hb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Main CI: cmdb\_ci\_cloud\_load\_balancer

</td></tr><tr><td>

name

</td><td>

Load balancer name.

</td></tr><tr><td>

object\_id

</td><td>

Load balancer unique identifier.

</td></tr><tr><td>

fqdn

</td><td>

Load balancer address \(host name\).

</td></tr><tr><td>

dns\_name

</td><td>

Load balancer domain server name.

</td></tr><tr><td>

short\_description

</td><td>

Load balancer description that you provide for easy identification.

</td></tr><tr><td>

operational\_status

</td><td>

Load balancer status, one of either: -   ONLINE
-   OFFLINE


</td></tr><tr><td>

location

</td><td>

Datacenter location.

</td></tr><tr><td>

state

</td><td>

Load balancer provisioning status.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Related CI: cmdb\_ci\_lb\_service

</td></tr><tr><td>

name

</td><td>

Pattern created name, composed of:-   load balancer name
-   type of protocol
-   resource type listener


</td></tr><tr><td>

object\_id

</td><td>

Load balancer unique identifier.

</td></tr><tr><td>

port

</td><td>

Port number of the listener.

</td></tr><tr><td>

front\_end\_port

</td><td>

Protocol port number of the listener.

</td></tr><tr><td>

listener\_protocol

</td><td>

Protocol of the listener. One of the following protocols:-   TCP
-   HTTP
-   HTTPS


</td></tr><tr><td>

operational\_status

</td><td>

Provisioning status of the listener.

</td></tr><tr><td class="sub-head" colspan="2">

Related CI: cmdb\_ci\_lb\_pool

</td></tr><tr><td>

name

</td><td>

Pattern created name, composed of: -   load balancer name
-   type of protocol
-   port
-   resource type “pool”


</td></tr><tr><td>

object\_id

</td><td>

Load balancer pool unique identifier.

</td></tr><tr><td>

port

</td><td>

Protocol port of the backend.

</td></tr><tr><td>

pool\_status

</td><td>

Load balancer pool provisioning status.

</td></tr><tr><td>

load\_balancing\_method

</td><td>

Load balancing method. One of the following algorithms: -   "ROUNDROBIN"
-   "WEIGHTED\_RR"
-   "LEASTCONNECTION"


</td></tr><tr><td class="sub-head" colspan="2">

Related CI: cmdb\_ci\_lb\_pool\_member

</td></tr><tr><td>

name

</td><td>

Pattern created name, composed of:-   load balancer name
-   type of protocol
-   IP address of the Pool Member


</td></tr><tr><td>

object\_id

</td><td>

Load balancer pool member unique identifier, composed of:-   Member ID
-   Listener ID


</td></tr><tr><td>

ip\_address

</td><td>

IP address of a load balancer member.

</td></tr><tr><td>

server\_id

</td><td>

ID of the member in IBM cloud.

</td></tr><tr><td>

load\_balancer

</td><td>

Name of the related Load Balancer.

</td></tr><tr><td class="sub-head" colspan="2">

Related CI: cmdb\_ci\_lb\_health\_service

</td></tr><tr><td>

name

</td><td>

Pattern created name, composed of:-   load balancer name
-   type of protocol
-   resource type: **Health Check**
-   resource ID


</td></tr><tr><td>

object\_id

</td><td>

Unique identifier of the Health Service Check.

</td></tr><tr><td>

monitor\_type

</td><td>

Health check type. One of the following: -   TCP
-   HTTP
-   HTTPS


</td></tr><tr><td>

timeout\_sec

</td><td>

Timeout, in seconds, to wait for health check responses.

</td></tr><tr><td>

check\_interval\_sec

</td><td>

Interval, in seconds, to perform health check.

</td></tr></tbody>
</table>-   **IBM Cloud Location Groups discovered resources**

    |Field|Description|
    |-----|-----------|
    |Main CI: cmdb\_ci\_cloud\_location\_group|
    |name|A descriptive name used to identify a Location Group.|
    |object\_id|The ID of the Location Group record.|
    |locationGroupType Name|The name of the Location Group Type.|
    |short\_description|A small note about a Location Group to use at your discretion.|
    |locationGroup Type ID|The ID of the Location Group Type.|

-   **IBM Cloud Network discovered resources**

<table id="table_wlf_ybx_jhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Main CI: cmdb\_ci\_network

</td></tr><tr><td>

name

</td><td>

VLAN number.

</td></tr><tr><td>

object\_id

</td><td>

Network unique identifier.

</td></tr><tr><td>

access\_port\_vlan

</td><td>

VLAN number.

</td></tr><tr><td>

is\_external

</td><td>

Network space value. The value is either: -   true if the network\_space is “PUBLIC”
-   false if the network\_space is “PRIVATE”.


</td></tr><tr><td>

state

</td><td>

State has the value "available".

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Related CI: cmdb\_ci\_cloud\_subnet

</td></tr><tr><td>

name

</td><td>

Name, composed of: “network\_identifier/cidr”

</td></tr><tr><td>

object\_id

</td><td>

Subnet unique identifier.

</td></tr><tr><td>

subnet\_mask

</td><td>

Netmask of the subnet.

</td></tr><tr><td>

gateway

</td><td>

Gateway IP address.

</td></tr><tr><td>

cidr

</td><td>

Method for allocating IP addresses and IP routing: “network\_identifier/cidr”.

</td></tr><tr><td>

category

</td><td>

Subnet type.

</td></tr><tr><td>

broadcast\_address

</td><td>

Subnet broadcast address.

</td></tr><tr><td>

available\_ip\_count

</td><td>

Number of available IP addresses in the subnet.

</td></tr><tr><td class="sub-head" colspan="2">

Related CI: cmdb\_ci\_compute\_security\_group

</td></tr><tr><td>

name

</td><td>

Security Group name.

</td></tr><tr><td>

object\_id

</td><td>

Security Group unique identifier.

</td></tr><tr><td>

short\_description

</td><td>

Security Group description that you provide for easy identification.

</td></tr><tr><td class="sub-head" colspan="2">

Related CI: cmdb\_ci\_compute\_security\_group\_rule

</td></tr><tr><td>

name

</td><td>

Field with the same value as the Security Group Rule object\_id field.

</td></tr><tr><td>

object\_id

</td><td>

Security Group Rule unique identifier.

</td></tr><tr><td>

created

</td><td>

Date the CI was created.

</td></tr><tr><td>

direction

</td><td>

Direction of the information. One of the following: -   inbound
-   outbound


</td></tr><tr><td>

Ethertype

</td><td>

Ethertype. One of the following: -   IPv4
-   IPv6


</td></tr><tr><td>

port\_range\_min

</td><td>

The first port of the range that the rule applies to.

</td></tr><tr><td>

port\_range\_max

</td><td>

The last port of the range that the rule applies to.

</td></tr><tr><td>

protocol

</td><td>

Protocol that the rule is applied to.

</td></tr><tr><td>

remote\_group\_id

</td><td>

Security Group ID for the Source/Destination security group. It means that this rule applies on all IP addresses that were configured in this security group.

</td></tr></tbody>
</table>-   **IBM Cloud Organizations and Space discovered resources**

<table id="table_vbc_2cx_jhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Main CI: cmdb\_ci\_cloud\_org

</td></tr><tr><td>

name

</td><td>

Name of the cloud organization.

</td></tr><tr><td>

guid

</td><td>

Unique identifier of the organization.

</td></tr><tr><td>

url

</td><td>

Unique URL of the organization.

</td></tr><tr><td>

billing\_enabled

</td><td>

Billing method in use by the organization. One of either: -   Enabled / \(TRUE\)
-   Disabled / \(FALSE\)


</td></tr><tr><td>

quota\_definition\_url

</td><td>

Resources that are available to an organization.

</td></tr><tr><td>

spaces\_url

</td><td>

Unique URL of the space assigned to the organization.

</td></tr><tr><td>

operational\_status

</td><td>

Operational status of the organization.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Related CI: cmdb\_ci\_cloud\_space

</td></tr><tr><td>

name

</td><td>

Unique name of the space.

</td></tr><tr><td>

object\_id

</td><td>

Space unique identifier \(guid\).

</td></tr><tr><td>

alllow\_ssh

</td><td>

Access to the application over SSH is either allowed or not allowed. Boolean, one of either: -   TRUE
-   FALSE


</td></tr><tr><td>

URL

</td><td>

URL of the space from the metadata description.

</td></tr></tbody>
</table>-   **IBM Cloud Resource Groups discovered resources**

    |Field|Description|
    |-----|-----------|
    |Main CI: cmdb\_ci\_resource\_group|
    |name|Name of the resource group.|
    |object\_id|Unique identifier of the resource group.|
    |quota\_id|Value identifying the quota ID associated with the resource group.|

-   **IBM Cloud SSH Key discovered resources**

    |Field|Description|
    |-----|-----------|
    |Main CI: cmdb\_ci\_cloud\_key\_pair|
    |name|Name to identify an SSH key.|
    |object\_id|ID of the SSH key record.|
    |key|SSH Key record.|
    |finger\_print|Short sequence of bytes used to authenticate or lookup a longer SSH Key. This value is automatically generated when adding or modifying the SSH Key. Read only. Changes made are ignored.|
    |created \_date|Date when the SSH Key was added. Read only. Changes made are ignored.|
    |modify\_date|Date when the SSH Key was modified. Read only. Changes made are ignored.|
    |short\_description|SSH description that you provide for easy identification.|
    |Related CI: cmdb\_ci\_ibm\_datacenter|
    |name|Name of the datacenter.|
    |region|Region that the datacenter is in.|
    |discovery\_status|Status information about the IBM datacenter.|
    |sys\_class\_name|Class of the datacenter|
    |Related CI: cmdb\_ci\_cloud\_service\_account|
    |name|Name of the cloud service account.|
    |account\_id|Account ID for this cloud service account.|
    |discovery\_credentials|Credentials for this cloud service account.|
    |datacenter\_url|URL used to populate Logical Data Centers \(LDCs\).|
    |datacenter\_type|Type of datacenter. As an example, IBM Datacenter \[cmdb\_ci\_ibm\_datacenter\]|
    |datacenter\_discovery\_status|Status of last execution of Discover Datacenters.|

-   **IBM Cloud Storage discovered resources**

<table id="table_zd3_wdx_jhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Main CI: cmdb\_ci\_storage\_volume

</td></tr><tr><td>

name

</td><td>

Username used to:-   access a non-EVault Storage volume
-   register the EVault server agent with the vault backup system


</td></tr><tr><td>

object\_id

</td><td>

Storage account unique identifier.

</td></tr><tr><td>

size

</td><td>

Capacity of the storage account, measured in gigabytes.

</td></tr><tr><td>

size\_bytes

</td><td>

Capacity of the storage account, measured in bytes.

</td></tr><tr><td>

label

</td><td>

Name of the storage network resource.

</td></tr><tr><td>

storage\_type

</td><td>

Description of the storage type. As an example, NAS.

</td></tr><tr><td>

fqdn

</td><td>

IP address of a storage resource or fully qualified domain name.

</td></tr><tr><td>

device

</td><td>

Unique identification number of the device associated with a Storage volume.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Related CI: cmdb\_ci\_storage\_vol\_snapshot

</td></tr><tr><td>

name

</td><td>

Name of a storage network resource.

</td></tr><tr><td>

object\_id

</td><td>

Storage unique identifier.

</td></tr><tr><td>

capacity

</td><td>

Capacity of the snapshot volume in gigabytes.

</td></tr><tr><td>

fqdn

</td><td>

IP address of a storage resource or fully qualified domain name.

</td></tr><tr><td>

location

</td><td>

Unique availability zone where the storage volume is located.

</td></tr><tr><td class="sub-head" colspan="2">

Related CI: cmdb\_ci\_ibm\_datacenter

</td></tr><tr><td>

name

</td><td>

Name of the datacenter.

</td></tr><tr><td>

region

</td><td>

Region that the datacenter is in.

</td></tr><tr><td>

discovery\_status

</td><td>

Status information about the IBM datacenter.

</td></tr><tr><td>

sys\_class\_name

</td><td>

Class of the datacenter

</td></tr><tr><td class="sub-head" colspan="2">

Related CI: cmdb\_ci\_cloud\_service\_account

</td></tr><tr><td>

name

</td><td>

Name of the cloud service account.

</td></tr><tr><td>

account\_id

</td><td>

Account ID for this cloud service account.

</td></tr><tr><td>

discovery\_credentials

</td><td>

Credentials for this cloud service account.

</td></tr><tr><td>

datacenter\_url

</td><td>

URL used to populate LDCs.

</td></tr><tr><td>

datacenter\_type

</td><td>

Type of datacenter. As an example, IBM Datacenter \[cmdb\_ci\_ibm\_datacenter\]

</td></tr><tr><td>

datacenter\_discovery\_status

</td><td>

Status of last execution of Discover Datacenters.

</td></tr><tr><td class="sub-head" colspan="2">

Related CI: cmdb\_ci\_availability\_zone

</td></tr><tr><td>

name

</td><td>

Name of the availability zone \(AZ\).

</td></tr><tr><td>

object\_id

</td><td>

Unique identifier for this resource.

</td></tr><tr><td>

short\_description

</td><td>

Availability zone description that you provide.

</td></tr></tbody>
</table>-   **IBM Cloud Virtual Server discovered resources**

<table id="table_njj_ydx_jhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Main CI: cmdb\_ci\_vm\_instance

</td></tr><tr><td>

name

</td><td>

Name of the VM.

</td></tr><tr><td>

object\_id

</td><td>

Unique identifier of the VM.

</td></tr><tr><td>

dns\_domain

</td><td>

VM domain server name.

</td></tr><tr><td>

fqdn

</td><td>

VM IP address.

</td></tr><tr><td>

short\_description

</td><td>

Description in a note that is attached to the VM on the IBM console.

</td></tr><tr><td>

cpus

</td><td>

Number of CPU cores assigned to this VM.

</td></tr><tr><td>

memory

</td><td>

Memory size assigned to this VM.

</td></tr><tr><td>

disks

</td><td>

Number of disks assigned to this VM.

</td></tr><tr><td>

state

</td><td>

The running state of the VM.

 -   On – returned as ‘Running’ from the API.
-   Off – returned as ‘Halted’ from the API.


</td></tr><tr><td>

placement\_group\_id

</td><td>

Placement group ID.

</td></tr><tr><td>

nics

</td><td>

Number of NICs.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Related CI: cmdb\_ci\_nic

</td></tr><tr><td>

name

</td><td>

Name, composed of:-   load balancer name
-   Port


</td></tr><tr><td>

object\_id

</td><td>

Unique identifier of the NIC.

</td></tr><tr><td>

ip\_address

</td><td>

IP that is configured on the NIC.

</td></tr><tr><td>

mac\_address

</td><td>

NIC MAC details.

</td></tr><tr><td>

netmask

</td><td>

Mask used to divide the IP address into subnets and to specify the available hosts in the network.

</td></tr><tr><td>

status

</td><td>

State of the NIC.

</td></tr><tr><td class="sub-head" colspan="2">

Related CI: cmdb\_ci\_endpoint\_vnic

</td></tr><tr><td>

name

</td><td>

Name for the VNIC endpoint.

</td></tr><tr><td>

object\_id

</td><td>

Unique identifier of the VNIC endpoint.

</td></tr><tr><td>

host

</td><td>

Host identifier.

</td></tr><tr><td class="sub-head" colspan="2">

Related CI: cmdb\_ci\_storage\_volume

</td></tr><tr><td>

name

</td><td>

Username used to:-   access a non-EVault Storage volume
-   register the EVault server agent with the vault backup system


</td></tr><tr><td>

object\_id

</td><td>

Storage account unique identifier.

</td></tr><tr><td>

size

</td><td>

Capacity of the storage account, measured in gigabytes.

</td></tr><tr><td>

size\_bytes

</td><td>

Capacity of the storage account, measured in bytes.

</td></tr><tr><td>

label

</td><td>

Name of the storage network resource.

</td></tr><tr><td>

storage\_type

</td><td>

Description of the storage type. As an example, NAS.

</td></tr><tr><td>

fqdn

</td><td>

IP address of a storage resource or fully qualified domain name.

</td></tr><tr><td>

device

</td><td>

Unique identification number of the guest associated with a Storage volume.

</td></tr><tr><td class="sub-head" colspan="2">

Related CI: cmdb\_ci\_endpoint\_nfs

</td></tr><tr><td>

name

</td><td>

Name for the NFS endpoint.

</td></tr><tr><td>

host

</td><td>

Host identifier.

</td></tr><tr><td>

protocol

</td><td>

Protocol that was applied.

</td></tr><tr><td>

type

</td><td>

NFS endpoint type.

</td></tr><tr><td>

created

</td><td>

Date that the NFS endpoint was created.

</td></tr><tr><td>

updated

</td><td>

Date that the NFS endpoint was updated.

</td></tr><tr><td>

discovery\_source

</td><td>

Source of the discovery. As an example, ServiceWatch

</td></tr><tr><td>

host\_name

</td><td>

Host name of the NFS endpoint

</td></tr><tr><td class="sub-head" colspan="2">

Related CI: cmdb\_ci\_endpoint\_iscsi

</td></tr><tr><td>

host

</td><td>

Host identifier for the ISCSI endpoint.

</td></tr><tr><td>

port

</td><td>

Port to determine how GCP iscsi contact to the VMs.

</td></tr><tr><td>

protocol

</td><td>

Protocol that was applied.

</td></tr><tr><td>

type

</td><td>

ISCSI endpoint type

</td></tr><tr><td>

created

</td><td>

Date that the ISCSI endpoint was created.

</td></tr><tr><td>

updated

</td><td>

Date that the ISCSI endpoint was updated.

</td></tr><tr><td>

discovery\_source

</td><td>

Source of the discovery. As an example, ImportSet

</td></tr><tr><td>

host\_name

</td><td>

Host name of the ISCSI endpoint

</td></tr><tr><td class="sub-head" colspan="2">

Related CI: cmdb\_ci\_endpoint\_block

</td></tr><tr><td>

name

</td><td>

Name for the block endpoint.

</td></tr><tr><td>

object\_id

</td><td>

Unique identifier of the block endpoint.

</td></tr><tr><td>

host

</td><td>

Host identifier.

</td></tr><tr><td class="sub-head" colspan="2">

Related CI: cmdb\_ci\_os\_template

</td></tr><tr><td>

name

</td><td>

Name of the image. For example, ‘CentOS 7.0-64 Minimal for VSI’.

</td></tr><tr><td>

object\_id

</td><td>

Unique identifier of the image.

</td></tr><tr><td>

guest\_os

</td><td>

OS used by the image. As an example, Linux.

</td></tr><tr><td>

root\_device\_type

</td><td>

Type of device used by root.

</td></tr><tr><td>

image\_source

</td><td>

Source of the image.

</td></tr><tr><td>

image\_type

</td><td>

Image type.

</td></tr><tr><td>

infuse\_key

</td><td>

Key used to infuse the image.

</td></tr><tr><td>

update\_host\_name

</td><td>

Update host name for the image.

</td></tr><tr><td>

credentials

</td><td>

Credentials for the image.

</td></tr><tr><td>

version

</td><td>

OS version. For example, ‘7.0-64 Minimal for VSI’.

</td></tr><tr><td class="sub-head" colspan="2">

Related CI: cmdb\_ci\_cloud\_key\_pair

</td></tr><tr><td>

name

</td><td>

Name to identify a key \(key label\).

</td></tr><tr><td>

object\_id

</td><td>

ID of the key record.

</td></tr><tr><td>

key

</td><td>

Key record.

</td></tr><tr><td>

finger\_print

</td><td>

Short sequence of bytes used to authenticate or look up a Key. This value is automatically generated when adding or modifying the Key. Read only. Changes made are ignored.

</td></tr><tr><td>

created \_date

</td><td>

Date when the Key was added. Read only. Changes made are ignored.

</td></tr><tr><td>

modify\_date

</td><td>

Date when the Key was modified. Read only. Changes made are ignored.

</td></tr><tr><td>

short\_description

</td><td>

Description that you provide for easy identification.

</td></tr><tr><td class="sub-head" colspan="2">

Related CI: cmdb\_ci\_compute\_security\_group

</td></tr><tr><td>

name

</td><td>

Security Group name.

</td></tr><tr><td>

object\_id

</td><td>

Security Group unique identifier.

</td></tr><tr><td>

short\_description

</td><td>

Security Group description that you provide for easy identification.

</td></tr><tr><td class="sub-head" colspan="2">

Related CI: cmdb\_ci\_endpoint\_comp\_security

</td></tr><tr><td>

host

</td><td>

Host identifier of the compute security endpoint.

</td></tr><tr><td>

port

</td><td>

Unique identifier of the compute security endpoint.

</td></tr><tr><td>

protocol

</td><td>

Protocol that was applied.

</td></tr><tr><td>

type

</td><td>

Type of compute security endpoint.

</td></tr><tr><td>

created

</td><td>

Date when the compute security endpoint was added. Read only. Changes made are ignored.

</td></tr><tr><td>

updated

</td><td>

Date when the compute security endpoint was modified. Read only. Changes made are ignored.

</td></tr><tr><td>

discovery\_source

</td><td>

Source of the discovery. As an example, Manual Entry.

</td></tr><tr><td>

host\_name

</td><td>

Host name of the compute security endpoint.

</td></tr><tr><td class="sub-head" colspan="2">

Related CI: cmdb\_ci\_ibm\_datacenter

</td></tr><tr><td>

name

</td><td>

Name of the datacenter.

</td></tr><tr><td>

region

</td><td>

Region that the datacenter is in.

</td></tr><tr><td>

discovery\_status

</td><td>

Status information about the IBM datacenter.

</td></tr><tr><td>

sys\_class\_name

</td><td>

Class of the datacenter

</td></tr><tr><td class="sub-head" colspan="2">

Related CI: cmdb\_ci\_availability\_zone

</td></tr><tr><td>

name

</td><td>

Name of the availability zone \(AZ\).

</td></tr><tr><td>

object\_id

</td><td>

Unique identifier for this resource.

</td></tr><tr><td>

short\_description

</td><td>

Availability zone description that you provide.

</td></tr><tr><td class="sub-head" colspan="2">

Related CI: cmdb\_ci\_cloud\_service\_account

</td></tr><tr><td>

name

</td><td>

Name of the cloud service account.

</td></tr><tr><td>

account\_id

</td><td>

Account ID for this cloud service account.

</td></tr><tr><td>

discovery\_credentials

</td><td>

Credentials for this cloud service account.

</td></tr><tr><td>

datacenter\_url

</td><td>

URL used to populate LDCs.

</td></tr><tr><td>

datacenter\_type

</td><td>

Type of datacenter. As an example, IBM Datacenter \[cmdb\_ci\_ibm\_datacenter\]

</td></tr><tr><td>

datacenter\_discovery\_status

</td><td>

Status of last execution of Discover Datacenters.

</td></tr></tbody>
</table>-   **IBM Cloud Virtual Server – Related Items view**

    ![IBM Cloud Virtual Server – Related Items view](../image/ibm-vserver-related-items-1.png)


## CI Relationships

These relationships are created to support IBM Cloud Platform discovery.

-   **Relationships for IBM Cloud Load Balancer discovered resources**

    |CI|Relationship|CI|
    |---|------------|---|
    |Related CI: cmdb\_ci\_ibm\_datacenter|
    |cmdb\_ci\_ibm\_datacenter|Hosted on::Hosts|cmdb\_ci\_cloud\_service\_account|
    |cmdb\_ci\_ibm\_datacenter|Contains::Contained by|cmdb\_ci\_availability\_zone|
    |Related CI: cmdb\_ci\_cloud\_load\_balancer|
    |cmdb\_ci\_cloud\_load\_balancer|Hosted on::Hosts|cmdb\_ci\_ibm\_datacenter|
    |cmdb\_ci\_cloud\_load\_balancer|Contains::Contained by|cmdb\_ci\_lb\_health\_service|
    |Related CI: cmdb\_ci\_availability\_zone|
    |cmdb\_ci\_availability\_zone|Hosted on::Hosts|cmdb\_ci\_cloud\_load\_balancer|
    |cmdb\_ci\_availability\_zone|Contains::Contained by|cmdb\_ci\_lb\_service|
    |Related CI: cmdb\_ci\_lb\_service|
    |cmdb\_ci\_lb\_service|Hosted on::Hosts|cmdb\_ci\_cloud\_load\_balancer|
    |cmdb\_ci\_lb\_service|Contains::Contained by|cmdb\_ci\_lb\_pool|
    |Related CI: cmdb\_ci\_lb\_pool|
    |cmdb\_ci\_lb\_pool|Hosted on::Hosts|cmdb\_ci\_cloud\_load\_balancer|
    |cmdb\_ci\_lb\_pool|Owns::Owned by|cmdb\_ci\_lb\_pool\_member|
    |Related CI: cmdb\_ci\_lb\_health\_service|
    |cmdb\_ci\_lb\_health\_service|Contains::Contained by|cmdb\_ci\_cloud\_load\_balancer|

-   **Relationships for IBM Cloud Location Groups discovered resources**

    |CI|Relationship|CI|
    |---|------------|---|
    |Related CI: cmdb\_ci\_ibm\_datacenter|
    |cmdb\_ci\_ibm\_datacenter|Hosted on::Hosts|cmdb\_ci\_cloud\_service\_account|
    |cmdb\_ci\_ibm\_datacenter|Contains::Contained by|cmdb\_ci\_availability\_zone|
    |Related CI: cmdb\_ci\_cloud\_location\_group|
    |cmdb\_ci\_cloud\_location\_group|Hosted on::Hosts|cmdb\_ci\_cloud\_service\_account|
    |cmdb\_ci\_cloud\_location\_group|Contains::Contained by|cmdb\_ci\_availability\_zone|

-   **Relationships for IBM Cloud Network discovered resources**

    |CI|Relationship|CI|
    |---|------------|---|
    |Related CI: cmdb\_ci\_ibm\_datacenter|
    |cmdb\_ci\_ibm\_datacenter|Hosted on::Hosts|cmdb\_ci\_cloud\_service\_account|
    |cmdb\_ci\_ibm\_datacenter|Contains::Contained by|cmdb\_ci\_availability\_zone|
    |Related CI: cmdb\_ci\_network|
    |cmdb\_ci\_network|Hosted on::Hosts|cmdb\_ci\_ibm\_datacenter|
    |cmdb\_ci\_network|Contains::Contained by|cmdb\_ci\_cloud\_subnet|
    |Related CI: cmdb\_ci\_compute\_security\_group|
    |cmdb\_ci\_compute\_security\_group|Hosted on::Hosts|cmdb\_ci\_cloud\_service\_account|
    |cmdb\_ci\_compute\_security\_group|Contains::Contained by|cmdb\_ci\_compute\_security\_group\_rule|

-   **Relationships for IBM Cloud Resource Groups discovered resources**

    |CI|Relationship|CI|
    |---|------------|---|
    |Related CI: cmdb\_ci\_resource\_group|
    |cmdb\_ci\_resource\_group|Hosted on::Hosts|cmdb\_ci\_cloud\_service\_account|

-   **Relationships for IBM Cloud SSH Key discovered resources**

    |CI|Relationship|CI|
    |---|------------|---|
    |Related CI: cmdb\_ci\_ibm\_datacenter|
    |cmdb\_ci\_ibm\_datacenter|Hosted on::Hosts|cmdb\_ci\_cloud\_service\_account|
    |cmdb\_ci\_ibm\_datacenter|Contains::Contained by|cmdb\_ci\_availability\_zone|
    |Related CI: cmdb\_ci\_cloud\_key\_pair|
    |cmdb\_ci\_cloud\_key\_pair|Hosted on::Hosts|cmdb\_ci\_cloud\_service\_account|

-   **Relationships for IBM Cloud Storage discovered resources**

    |CI|Relationship|CI|
    |---|------------|---|
    |Related CI: cmdb\_ci\_ibm\_datacenter|
    |cmdb\_ci\_ibm\_datacenter|Hosted on::Hosts|cmdb\_ci\_cloud\_service\_account|
    |cmdb\_ci\_ibm\_datacenter|Contains::Contained by|cmdb\_ci\_availability\_zone|
    |Related CI: cmdb\_ci\_storage\_volume|
    |cmdb\_ci\_storage\_volume|Hosted on::Hosts|cmdb\_ci\_ibm\_datacenter|
    |cmdb\_ci\_storage\_volume|Provisioned::Provisioned From|cmdb\_ci\_storage\_vol\_snapshot|
    |Related CI: cmdb\_ci\_storage\_vol\_snapshot|
    |cmdb\_ci\_storage\_vol\_snapshot|Hosted on::Hosts|cmdb\_ci\_ibm\_datacenter|
    |cmdb\_ci\_storage\_vol\_snapshot|Located in Zone::Zone contains|cmdb\_ci\_availability\_zone|
    |Related CI: cmdb\_ci\_availability\_zone|
    |cmdb\_ci\_availability\_zone|Contains::Contained by|cmdb\_ci\_storage\_volume|

-   **Relationships for IBM Cloud Virtual Server discovered resources**

    |CI|Relationship|CI|
    |---|------------|---|
    |Related CI: cmdb\_ci\_ibm\_datacenter|
    |cmdb\_ci\_ibm\_datacenter|Hosted on::Hosts|cmdb\_ci\_cloud\_service\_account|
    |cmdb\_ci\_ibm\_datacenter|Contains::Contained by|cmdb\_ci\_availability\_zone|
    |cmdb\_ci\_ibm\_datacenter|Hosted on::Hosts|cmdb\_ci\_vm\_instance|
    |Related CI: cmdb\_ci\_vm\_instance|
    |cmdb\_ci\_vm\_instance|Hosted on::Hosts|cmdb\_ci\_ibm\_datacenter|
    |cmdb\_ci\_vm\_instance|Located in:Houses|cmdb\_ci\_availability\_zone|
    |cmdb\_ci\_vm\_instance|Uses:Used By|cmdb\_ci\_cloud\_key\_pair|
    |cmdb\_ci\_vm\_instance|Contains:Contained By|cmdb\_ci\_nic|
    |cmdb\_ci\_vm\_instance|endpoint|cmdb\_ci\_nic|
    |Related CI: cmdb\_ci\_availability\_zone|
    |cmdb\_ci\_availability\_zone|Hosted on::Hosts|cmdb\_ci\_vm\_instance|
    |Related CI: cmdb\_ci\_nic|
    |cmdb\_ci\_nic|Hosted on::Hosts|cmdb\_ci\_vm\_instance|
    |Related CI: cmdb\_ci\_os\_template|
    |cmdb\_ci\_os\_template|Hosted on::Hosts|cmdb\_ci\_cloud\_service\_account|
    |cmdb\_ci\_os\_template|Provisioned::Provisioned by|cmdb\_ci\_vm\_instance|
    |Related CI: cmdb\_ci\_compute\_security\_group|
    |cmdb\_ci\_compute\_security\_group|Hosted on::Hosts|cmdb\_ci\_cloud\_service\_account|
    |cmdb\_ci\_compute\_security\_group|Implement::Implemented from|cmdb\_ci\_vm\_instance|
    |Related CI: cmdb\_ci\_storage\_volume|
    |cmdb\_ci\_storage\_volume|Hosted on::Hosts|cmdb\_ci\_ibm\_datacenter|
    |cmdb\_ci\_storage\_volume|Implement::Implemented from|cmdb\_ci\_vm\_instance|
    |Related CI: cmdb\_ci\_cloud\_key\_pair|
    |cmdb\_ci\_cloud\_key\_pair|Hosted On:Hosts|cmdb\_ci\_cloud\_service\_account|

-   **Relationships discovered for the virtual machine \(VM\) instance**

    |CI|Relationship|CI|
    |---|------------|---|
    |Servers \[cmdb\_ci\_server\]|Virtualized by:: Virtualizes|Virtual Machine Instance \[cmdb\_ci\_instance\]|


## Data collected by Service Mapping during tag-based discovery

Service Mapping uses tag-based discovery to create service instance maps including the Cloud components. The Service Mapping application comes with the following preconfigured CI relationships used for tag-based discovery. These CI relationships are available from the 1.0.68 release on the ServiceNow Store.

|CI|Relationship|CI|
|---|------------|---|
|Configuration Item \[cmdb\_ci\]|Hosted on::Hosts|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|
|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

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
</table>**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

