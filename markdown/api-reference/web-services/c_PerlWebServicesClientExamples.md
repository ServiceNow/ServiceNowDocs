---
title: Perl web services client examples
description: Examples demonstrating an integration with a Perl web services client.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Examples, Inbound, Web services, API implementation, API implementation and reference]
---

# Perl web services client examples

Examples demonstrating an integration with a Perl web services client.

**Note:** The following examples require the usage of the [Perl language](http://www.perl.com/) and the [SOAP::Lite package](http://soaplite.com/).

## System Requirements

Perl 5.8

-   SOAP::Lite \(prerequisites [http://soaplite.com/prereqs.html](http://soaplite.com/prereqs.html)\)
-   Crypt::SSLeay
-   IO::Socket::SSL

## insert

The following example will insert a record into the Incident table.

```
#!/usr/bin/perl -w
 
# declare usage of SOAP::Liteuse SOAP::Lite;
 
# specifying this subroutine, causes basic auth to use# its credentials when challengedsub SOAP::Transport::HTTP::Client::get_basic_credentials{# login as the itil userreturn'itil'=>'itil';}
 
# declare the SOAP endpoint heremy$soap= SOAP::Lite->proxy('https://myinstance.service-now.com/incident.do?SOAP');
 
# calling the insert functionmy$method= SOAP::Data->name('insert')->attr({xmlns =>'http://www.service-now.com/'});
 
# create a new incident with the following short_description and categorymy@params=( SOAP::Data->name(short_description =>'This is an example short description'));push(@params, SOAP::Data->name(category =>'Hardware'));
 
# invoke the SOAP callmy$result=$soap->call($method=>@params);
 
# print any SOAP faults that get returned
print_fault($result);# print the SOAP response that get return
print_result($result);
 
# convenient subroutine for printing all resultssub print_result {my($result)=@_;
 
  if($result->body&&$result->body->{'insertResponse'}){my%keyHash=%{$result->body->{'insertResponse'}};foreachmy$k(keys%keyHash){print"name=$k   value=$keyHash{$k}\n";}}}
 
# convenient subroutine for printing all SOAP faultssub print_fault {my($result)=@_;
 
  if($result->fault){print"faultcode=".$result->fault->{'faultcode'}."\n";print"faultstring=".$result->fault->{'faultstring'}."\n";print"detail=".$result->fault->{'detail'}."\n";}}
```

## insert \(With XML payload\)

The following is an example of inserting a record into the ecc\_queue table where the payload field is an XML document. This is done using the [Perl language](http://www.perl.com/) and the [SOAP::Lite](http://soaplite.com/) package, the XML document creation uses the [XML::Writer package](http://search.cpan.org/%7Ejosephw/XML-Writer-0.601/Writer.pm):

```
#!/usr/bin/perl -w#use SOAP::Lite ( +trace => all, maptype => {} );use SOAP::Lite;use XML::Writer;use XML::Writer::String;
 
## Get parameters passed by OVO notification#$OVMSG{id}=$ARGV[0];$OVMSG{node_name}=$ARGV[1];$OVMSG{node_type}=$ARGV[2];$OVMSG{date_created}=$ARGV[3];$OVMSG{time_created}=$ARGV[4];$OVMSG{date_received}=$ARGV[5];$OVMSG{time_received}=$ARGV[6];$OVMSG{application}=$ARGV[7];$OVMSG{msg_group}=$ARGV[8];$OVMSG{object}=$ARGV[9];$OVMSG{severity}=$ARGV[10];$OVMSG{operator_list}=$ARGV[11];$OVMSG{msg_text}=$ARGV[12];$OVMSG{instruction}=$ARGV[13];
 
sub SOAP::Transport::HTTP::Client::get_basic_credentials{return'itil'=>'itil';}
 
my$soap= SOAP::Lite->proxy('http://<instance name>.service-now.com/ecc_queue.do?SOAP');
 
my$method= SOAP::Data->name('insert')->attr({xmlns =>'http://www.service-now.com/'});
 
# get all incidents with category Networkmy@params=( SOAP::Data->name(agent =>'OVO_Notification'));push(@params, SOAP::Data->name(queue =>'input'));push(@params, SOAP::Data->name(name =>'HP Openview OVO Notification'));push(@params, SOAP::Data->name(source =>$OVMSG{id}));
 
my$s= XML::Writer::String->new();my$writer=new XML::Writer(OUTPUT =>$s);
 
#$writer->xmlDecl();$writer->startTag('notification');
 
write_element('id');
write_element('node_name');
write_element('node_type');
write_element('date_created');
write_element('time_created');
write_element('date_received');
write_element('time_received');
write_element('application');
write_element('msg_group');
write_element('object');
write_element('severity');
write_element('operator_list');
write_element('msg_text');
write_element('instruction');
 
$writer->endTag('notification');
 
$writer->end;
 
sub write_element {my$label=shift;my$value=$OVMSG{$label};$writer->startTag($label);if($value){$writer->characters($value);}$writer->endTag($label);}
 
push(@params, SOAP::Data->name(payload =>$s->value()));
 
print$soap->call($method=>@params)->result;</pre>
 
=== Response to the ''insert''===<source lang="xml"><?xml version="1.0" encoding="UTF-8"?><soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
    xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
    xmlns:xsi="http://www.w3.org/2001/XML Schema-instance"><soap:Body><insertResponse xmlns="http://www.service-now.com/ecc_queue"><sys_id>1a5ad50e0a0a021101bef2e07705f87a</sys_id><name>HP Openview OVO Notification</name></insertResponse></soap:Body></soap:Envelope>
```

## update

```
#!/usr/bin/perl -w
 
#use SOAP::Lite ( +trace => all, maptype => {} );use SOAP::Lite;
 
sub SOAP::Transport::HTTP::Client::get_basic_credentials{return'itil'=>'itil';}
 
my$soap= SOAP::Lite->proxy('http://localhost:8080/glide/incident.do?SOAP');
 
my$method= SOAP::Data->name('update')->attr({xmlns =>'http://www.service-now.com/'});
 
# update incident by sys_idmy@params=( SOAP::Data->name(sys_id =>'e8caedcbc0a80164017df472f39eaed1'));push(@params, SOAP::Data->name(short_description =>'this is a new description'));
 
my$result=$soap->call($method=>@params);
 
print_fault($result);
print_result($result);
 
sub print_result {my($result)=@_;
 
  if($result->body&&$result->body->{'updateResponse'}){my%keyHash=%{$result->body->{'updateResponse'}};foreachmy$k(keys%keyHash){print"name=$k   value=$keyHash{$k}\n";}}}
 
sub print_fault {my($result)=@_;
 
  if($result->fault){print"faultcode=".$result->fault->{'faultcode'}."\n";print"faultstring=".$result->fault->{'faultstring'}."\n";print"detail=".$result->fault->{'detail'}."\n";}}
```

## getKeys

The following is an example of retrieving a list of s for records of Incident where is Network.

```
#!/usr/bin/perl -w
 
#use SOAP::Lite ( +trace => all, maptype => {} );use SOAP::Lite;
 
sub SOAP::Transport::HTTP::Client::get_basic_credentials{return'itil'=>'itil';}
 
my$soap= SOAP::Lite->proxy('http://<instance name>.service-now.com/incident.do?SOAP');
 
my$method= SOAP::Data->name('getKeys')->attr({xmlns =>'http://www.service-now.com/'});
 
# get all incidents with category Networkmy@params=( SOAP::Data->name(category =>'Network')); 
 
print$soap->call($method=>@params)->result;
```

## get

The following is an example of retrieving an Incident record using its sys\_id value.

```
#!/usr/bin/perl -w#use SOAP::Lite ( +trace => all, maptype => {} );use SOAP::Lite;
 
sub SOAP::Transport::HTTP::Client::get_basic_credentials{return'itil'=>'itil';}
 
my$soap= SOAP::Lite->proxy('http://<instance name>.service-now.com/incident.do?SOAP');
 
my$method= SOAP::Data->name('get')->attr({xmlns =>'http://www.service-now.com/'});
 
# get incident by sys_idmy@params=( SOAP::Data->name(sys_id =>'9d385017c611228701d22104cc95c371'));
 
my%keyHash=%{$soap->call($method=>@params)->body->{'getResponse'}};
 
# iterate through all fields and print themforeachmy$k(keys%keyHash){print"$k=$keyHash{$k}\n";}
```

## getRecords

To query for an Incident using its incident number value:

```
#!/usr/bin/perl -w#use SOAP::Lite ( +trace => all, maptype => {} );use SOAP::Lite;
 
sub SOAP::Transport::HTTP::Client::get_basic_credentials{return'itil'=>'itil';}
 
my$soap= SOAP::Lite->proxy('http://<instance name>.service-now.com/incident.do?SOAP');
 
my$method= SOAP::Data->name('getRecords')->attr({xmlns =>'http://www.service-now.com/'});# get incident by numbermy@params=( SOAP::Data->name(number =>'INC10001'));
 
my%keyHash=%{$soap->call($method=>@params)->body->{'getRecordsResponse'}->{'getRecordsResult'}};
 
# iterate through all fields and print themforeachmy$k(keys%keyHash){print"$k=$keyHash{$k}\n";}
```

## getRecords \(Returning Multiple Results\)

The following is an example of retrieving and displaying an array of Incident records by querying all Incidents that have a of "Network"

```
#!/usr/bin/perl -w#use SOAP::Lite ( +trace => all, maptype => {} );use SOAP::Lite;
 
sub SOAP::Transport::HTTP::Client::get_basic_credentials{return'itil'=>'itil';}
 
my$soap= SOAP::Lite->proxy('http://<instance name>.service-now.com/incident.do?SOAP');
 
my$method= SOAP::Data->name('getRecords')->attr({xmlns =>'http://www.service-now.com/'});
 
# get incident by sys_idmy@params=( SOAP::Data->name(category =>'Network'));
 
my%keyHash=%{$soap->call($method=>@params)->body->{'getRecordsResponse'}};
 
my$i=0;my$size=@{$keyHash{'getRecordsResult'}};for($i=0;$i<$size;$i++){my%record=%{$keyHash{'getRecordsResult'}[$i]};print"------------------------------ $i ----------------------------\n";foreachmy$kk(keys%record){print"$kk=$record{$kk}\n";}}
```

## deleteRecord

```
#!/usr/bin/perl -w
 
#use SOAP::Lite ( +trace => all, maptype => {} );use SOAP::Lite;
 
sub SOAP::Transport::HTTP::Client::get_basic_credentials{return'itil'=>'itil';}
 
my$soap= SOAP::Lite->proxy('http://localhost:8080/glide/incident.do?SOAP');
 
my$method= SOAP::Data->name('deleteRecord')->attr({xmlns =>'http://www.service-now.com/'});
 
# delete incident by sys_idmy@params=( SOAP::Data->name(sys_id =>'46f67787a9fe198101e06dfcf3a78e99'));
 
my$result=$soap->call($method=>@params);
 
print_fault($result);
print_result($result);
 
sub print_result {my($result)=@_;
 
  if($result->body&&$result->body->{'deleteRecordResponse'}){my%keyHash=%{$result->body->{'deleteRecordResponse'}};foreachmy$k(keys%keyHash){print"name=$k   value=$keyHash{$k}\n";}}}
 
sub print_fault {my($result)=@_;
 
  if($result->fault){print"faultcode=".$result->fault->{'faultcode'}."\n";print"faultstring=".$result->fault->{'faultstring'}."\n";print"detail=".$result->fault->{'detail'}."\n";}}
```

**Parent Topic:**[Inbound web service examples](c_InboundWebServiceExamples.md)

