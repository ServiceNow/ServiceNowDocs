---
title: Map with explicit transform map scripts
description: Explicitly define mapping relationships in the Transform Map record itself.
locale: en-US
release: zurich
product: System Import Sets
classification: system-import-sets
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Transform maps, Import sets, Imports, Workflow Data Fabric]
---

# Map with explicit transform map scripts

Explicitly define mapping relationships in the Transform Map record itself.

An explicit Transform Map script explicitly defines mapping relationships in the Transform Map record itself. It runs after the source field values have been copied over to the target record, and before they are written to the database.

## CMDB software import facilitated by explicit mapping script

An example demonstrating how explicit map scripting can be used to facilitate an import of software instances to the CMDB where it is necessary to have the count in the software packages table reflect the number of instances.

In the CMDB there exist tables for software packages and software instances. A software package refers to a one individual software title, such as Mozilla Firefox. A software instance refers to an individual instance of a software title such as Mozilla Firefox on Jared\_T60\_Laptop.

In more technical terms a software instance is a many-to-many relationship with a software package and a configuration item. This script imports software instances. In doing so it checks to see if a software package for the instance exists. If the software package doesn't exist then it is created and the sys\_id for the newly created package is associated with the instance via the instance record's **Software** field.

```
//First we will initialize some temporary variables, 
//referencing values from the Import Set table source that will be used to 
//reference software package records and create them if necessary. 
 
var name= source.u_name;
var version = source.u_version;
var sid =""; 
 
//Next we will perform a glide query on the software package table (Note: The target table 
//for the import is software instances) 
var sgr =new GlideRecord("cmdb_ci_spkg");
 
//Here we are building our query to search for software packages where the name and 
//version of the package matches the name and version of the instance being imported 
sgr.addQuery("name",name);
sgr.addQuery("version", version);
sgr.query();
 
//Now if a software package with the correct name and version are found then we record 
//the sys_id of the package record otherwise we create the package and then record the sys_id
if(sgr.next()){
   sid = sgr.sys_id;}else{// create it
   sgr.initialize();
   sgr.newRecord();
   sgr.name=name;
   sgr.version= version;
   sid = sgr.insert();
   
   //Here we make an entry in System Import Set Log saying that we had to create a software package  
   log.info("Created new spkg: "+name+" - "+ version);
}
//Finally we set the reference field on our software instance record to the sys_id we have 
//recorded for the software package. In doing so we are also relating the 
//software package with the instance and so the count, which keeps track of
//the number of instances associated with a package, will automatically be incremented.
target.software= sid;
```

## Populating child tables by setting class names in an import to the CMDB

An example demonstrating how to import servers into the configuration management database.

The destination table for the import is the cmdb\_ci\_servers table.

```
var operating_system = source.u_operating_system.toString();
 
 
//This if statement uses JavaScript regular expressions to search the operating system
if( operating_system.match(/linux/i)!=null){
   target.sys_class_name="cmdb_ci_linux_server";
};
 
if( operating_system.match(/win/i)!=null){
   target.sys_class_name="cmdb_ci_win_server";
};
```

## User import data sanitation

An example script demonstrating how to sanitize user data before import.

```
//Note: The field names referenced from an import set are 
//prefixed with an "u_", also note that it is necessary  to use the java method
// toString() to so that we can use JavaScript functions to 
//manipulate the data.
var name= source.u_name.toString();
 
//Use native JavaScript function split to create an array for each word in the name "splitting" it 
//anywhere that there is a space
var split_names =name.split(" ");
 
//Find the number of of names (i.e., first and last name only, or first middle and last name, etc.)
var num_names = split_names.length;
 
// If there is only one name then map it to the last name field in the user table
if(num_names ==1){
   target.last_name= split_names[0];
}
 
//if there are two names then map the first one to first name and the last one to last name
if(num_names ==2){
   target.first_name= split_names[0]; 
   target.last_name= split_names[1];
}
 
//if there are more than 3 names then all middle names get combined into one middle name this is done 
//by shifting off the first name (array element 0 ) and mapping to first name and popping off the last
// name and returning it to the last name field
if(num_names >=3){
   target.first_name= split_names.shift();
   target.last_name= split_names.pop();
   target.middle_name= split_names.join(" ");
}
```

