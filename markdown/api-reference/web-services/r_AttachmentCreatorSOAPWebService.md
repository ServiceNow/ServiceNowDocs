---
title: AttachmentCreator SOAP web service
description: Attach documents to records in ServiceNow by sending a SOAP message targeting the ecc\_queue table.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [SOAP web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# AttachmentCreator SOAP web service

Attach documents to records in ServiceNow by sending a SOAP message targeting the ecc\_queue table.

**Important:** The AttachmentCreator SOAP web service is not recommended. Instead, use the REST [Attachment API](../../inbound-rest/concept/c_AttachmentAPI.md#) to manage attachments with web services.

Using the AttachmentCreator SOAP web service, you can attach a single document to a message that is a maximum of 5 MB. The following is an example of a URL or target end point: `https://instance_name.service-now.com/ecc_queue.do?WSDL`

|Field Name|Description|Value|
|----------|-----------|-----|
|agent|The name of the agent sending in the request, this can be any value since it is not used for processing.|AttachmentCreator|
|topic|The topic of the queue record, this value must be set to "AttachmentCreator" to trigger the attachment creation|AttachmentCreator|
|name|This field must contain a ":" delimited value of the file name, and its content-type|file\_name.xls:application/vnd.ms-excel|
|source|This field must contain a ":" delimited value of the target table and its sys\_id|incident:dd90c5d70a0a0b39000aac5aee704ae8|
|payload|This field must contain the Base 64 encoded string representing the object to be attached|the base 64 encoded string|

Sending in the values described in the table above will attach an Excel file to the incident table for the record located by the sys\_id `dd90c5d70a0a0b39000aac5aee704ae8`

## Security

Like all other HTTP based web services available on the platform, the AttachementCreator SOAP web service is required to authenticate using basic authentication by default. The user ID that is used for authentication will be subjected to access control in the same way as an interactive user.

To create attachments, the SOAP user must have any roles required to create Attachment \[sys\_attachment\] records, as well as the soap\_create role, and any roles required to read and write records on the target table, such as the itil role to add attachments to incident records. By default there is no single role allowing you to add attachments. You can create a role to explicitly allow adding attachments, then assign this role to the SOAP user.

## File type security

You can control what file types users can attach by setting the **glide.attachment.extensions** and **glide.security.file.mime\_type.validation** properties.

For these properties to apply to the AttachmentCreator web service, the property **glide.attachment.enforce\_security\_validation** must be set to true. This property is true by default.

## Example SOAP Message

The following is an example of a SOAP message that would take a text file "john1.txt" of mime-type: text/plain and attach it to an Incident with a GUID of: e6eed6950a0a3c59006f32c8e3ff3cf9. Note the payload is the base64 encoding of the file itself.

```
<?xml version="1.0" encoding="UTF-8"?>
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:ecc="http://www.service-now.com/ecc_queue">
    <soapenv:Header />
    <soapenv:Body>
        <ecc:insert>
            <agent>AttachmentCreator</agent>
            <topic>AttachmentCreator</topic>
            <name>john1.txt:text/plain</name>
            <source>incident:e6eed6950a0a3c59006f32c8e3ff3cf9</source>
            <payload>SSB3b25kZXIgaWYgc2hlIGtub3ducyB3aGF0IHNoZSdzIGRvaW5nIG5vdy4K</payload>
        </ecc:insert>
    </soapenv:Body>
</soapenv:Envelope>
```

## Example Node.js Script

The following example Node.js script adds an attachment to an incident record. Run this script from a client computer, not an instance.

```
/**
 * 
 * Node.js to ServiceNow attachment upload via SOAP
 * 
 * Andrew Venables andrew.venables@servicenow.com
 * July 2014
 * 
 * Version 1.0
 * 
 */

var soap = require('soap'), // https://github.com/vpulim/node-soap
	mime = require('mime'), // https://github.com/broofa/node-mime
	fs = require("fs");

var WSDL_FILENAME = 'ecc_queue.xml'; // Goto https://instancename.service-now.com/ecc_queue.do?WSDL and save a copy of the WSDL locally for simplicity
var DIRECTORY_CONTAINING_FILES = '/Users/andrew.venables/Documents/Uploads'; // Local path to the directory containing all the files we want to upload
var USERNAME = 'andy.venables'; // An admin user account on the instance
var PASSWORD = 'MY_PASSWORD'; // Password for above account
var TARGET_TABLE = 'incident'; // Target table to attach the files to
var TARGET_SYS_ID = '9d385017c611228701d22104cc95c371'; // Target record / sys_id to attach the files to. OOTB INC0000002

var files_to_upload; // Global that will contain our list of files to be uploaded
var pos = 0; // Global pointer for our position in the files_to_upload list

// Create a SOAP client to use to post to the instance
soap.createClient(WSDL_FILENAME, function(err, client) { // Node uses callbacks
	if (err) console.error(err);
	
	// Set the username and password
	client.setSecurity(new soap.BasicAuthSecurity(USERNAME, PASSWORD));
	
	// Read all the files in our source directory, will include . and ..
	files_to_upload = fs.readdirSync(DIRECTORY_CONTAINING_FILES);
	
	console.log('Files to upload: ' + files_to_upload.length + '\n');
	
	// Start iterating through the list of files to upload
	next(client);
		
});

// Process the next file in the files_to_upload array
// This is a neat way of dealing with Node and its expectation of callbacks
function next(client) {
	
	// Check we haven't reached the end
	if (pos >= files_to_upload.length) return;
	
	// Get the next file to upload
	var file_name = files_to_upload[pos];
	
	// Increment the pointer to the next file
	pos++;
	
	console.log(pos + '/'+ files_to_upload.length+ ' - Uploading file: ' + file_name);

	// A blank file is the end of the list
	if (file_name == '') return;
	
	// Skip to the next file as this one is invalid
	if (file_name == '.' || file_name == '..' || file_name.indexOf('.') == 0) 
		next(client);
	
	// Get the file type using an module called mime
	var file_type = mime.lookup(file_name);
	console.log('   of type: ' + file_type);
	
	var file_payload;
	// Load the file into a buffer
	fs.readFile(DIRECTORY_CONTAINING_FILES + '/' + file_name, function(err, the_data) {
		if (err) console.error(err);
		
		// Encode the buffer to base64
		file_payload = new Buffer(the_data, 'binary').toString('base64');
		
		// Set the parameters before we call the Web Service
		var parameters = {
			'agent': 	'AttachmentCreator',
	        'topic': 	'AttachmentCreator',
	        'name': 	file_name+':'+file_type,
	        'source': 	TARGET_TABLE+':'+TARGET_SYS_ID,
	        'payload': 	file_payload
		};
		
		console.log('      sending...')
		// Make the Web Service call, remember node likes callbacks
		client.insert(parameters, function(err, result) {
			if (err) console.error(err);
			
			console.log(result);
			
			// This file is done, next!
			next(client);
		});
	});
}
```

## Example Perl Script

The following example Perl script will create an attachment to an incident record.

```
use MIME::Base64;
use strict;
use SOAP::Lite;
 
# the ServiceNow instance
my $SNC_HOST = "https://instance_name.service-now.com";
my $base64;
my $buf;
 
# upload and attach a file on the local disk, base 64 encode it into a string first
open(FILE, "/Users/davidloo/Desktop/test_files/number_test.xls") or die "$!";
binmode FILE; #preserves file formatting on Windows
while (read(FILE, $buf, 60*57)) {
  $base64 .= encode_base64($buf);
}
 
# call the sub routine to attach
attach_incident();
 
sub attach_incident {
  # target the ecc_queue table
  my $soap = SOAP::Lite->proxy("$SNC_HOST/ecc_queue.do?SOAP");
  $soap->{_transport}->{_proxy}->{ssl_opts}->{verify_hostname} = 0;
  my $method = SOAP::Data->name('insert')->attr({xmlns => 'http://www.service-now.com/'});
 
  # set the ecc_queue parameters
  my @params = (SOAP::Data->name(agent => 'AttachmentCreator'));
  push(@params, SOAP::Data->name(topic => 'AttachmentCreator') );
 
  # identify the file name and its mime type
  push(@params, SOAP::Data->name(name => 'number_test.xls:application/vnd.ms-excel') );
 
  # attach to the incident, specifying its sys_id
  push(@params, SOAP::Data->name(source => 'incident:dd90c5d70a0a0b39000aac5aee704ae8') );
 
  # set the payload to be the base 64 encoded string representation of the file
  push(@params, SOAP::Data->name(payload => $base64) );
 
  # invoke the web service
  my $result = $soap->call($method => @params);
 
  print_fault($result);
 
  print_result($result);
}
 
sub print_result {
  my ($result) = @_;
 
  if ($result->body && $result->body->{'insertResponse'}) {
    my %keyHash = %{ $result->body->{'insertResponse'} };
    foreach my $k (keys %keyHash) {
        print "name=$k   value=$keyHash{$k}\n";
    }
  }
}
 
sub print_fault {
  my ($result) = @_;
 
  if ($result->fault) {
    print "faultcode=" . $result->fault->{'faultcode'} . "\n";
    print "faultstring=" . $result->fault->{'faultstring'} . "\n";
    print "detail=" . $result->fault->{'detail'} . "\n";
  }
}
 
# use the itil user for basic auth credentials
sub SOAP::Transport::HTTP::Client::get_basic_credentials {
   return 'itil' => 'itil';
}
```

**Parent Topic:**[SOAP web service](../concept/c_SOAPWebService.md)

