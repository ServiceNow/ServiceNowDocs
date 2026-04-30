---
title: Web service import sets security requirements
description: Web Service Import Sets use the same security mechanisms as SOAP Web Services.
locale: en-US
release: yokohama
product: System Import Sets
classification: system-import-sets
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Web service import sets, Import sets, Imports, Data and Automation]
---

# Web service import sets security requirements

Web Service Import Sets use the same security mechanisms as SOAP Web Services.

-   Basic authentication requires a Web Service user provide a valid user name and password.
-   Contextual security requires a Web Service user meet the access control rule of the queried table.

If your instance uses high security settings, the Web Service user may also need the soap role.

## Web service import sets related links

When displaying a mapped web service table, you have the following related links.

-   Import Sets — The import sets related to this web service import set.
-   Transform Maps — A list of transform maps related to this web service.
-   Transform History — The transformation history.
-   Edit Web Service — Edit the web service.

The following image shows a record that was inserted into the web service import set Notification. The target record is the resulting creation or modification to the Incident table record as a result of the transform.

![](../image/SoapNotification.jpg "Soap Notification")

## Web service import sets example

This example demonstrates the WSDL, SOAP envelope and response, Perl invocation, and result of a SOAP web service import.

## Sample WSDL

```
<?xmlversion="1.0"encoding="UTF-8"?><wsdl:definitions targetNamespace="http://www.service-now.com"  xmlns:tns="http://www.service-now.com/imp_notification"  xmlns:sncns="http://www.service-now.com"  xmlns:mime="http://schemas.xmlsoap.org/wsdl/mime/"  xmlns:http="http://schemas.xmlsoap.org/wsdl/http/"  xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/"  xmlns:xsd="http://www.w3.org/2001/XMLSchema"  xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/"  xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/"><wsdl:types><xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema"      elementFormDefault="unqualified"      targetNamespace="http://www.service-now.com/imp_notification"><xsd:element name="insert"><xsd:complexType><xsd:sequence><xsd:element maxOccurs="1" minOccurs="0" name="corrective_message" type="xsd:string"/><xsd:element maxOccurs="1" minOccurs="0" name="duration" type="xsd:string"/><xsd:element maxOccurs="1" minOccurs="0" name="expires_on" type="xsd:string"/><xsd:element maxOccurs="1" minOccurs="0" name="message" type="xsd:string"/><xsd:element maxOccurs="1" minOccurs="0" name="severity" type="xsd:string"/><xsd:element maxOccurs="1" minOccurs="0" name="source" type="xsd:string"/><xsd:element maxOccurs="1" minOccurs="0" name="timestamp" type="xsd:string"/><xsd:element maxOccurs="1" minOccurs="0" name="type" type="xsd:string"/><xsd:element maxOccurs="1" minOccurs="1" name="uuid" type="xsd:string"/></xsd:sequence></xsd:complexType></xsd:element><xsd:element name="insertResponse"><xsd:complexType><xsd:sequence><xsd:element maxOccurs="1" minOccurs="1" name="sys_id" type="xsd:string"/><xsd:element maxOccurs="1" minOccurs="1" name="table" type="xsd:string"/><xsd:element maxOccurs="1" minOccurs="1" name="display_name" type="xsd:string"/><xsd:element maxOccurs="1" minOccurs="1" name="display_value" type="xsd:string"/><xsd:element maxOccurs="1" minOccurs="1" name="status" type="xsd:string"/><xsd:element maxOccurs="1" minOccurs="0" name="status_message" type="xsd:string"/><xsd:element maxOccurs="1" minOccurs="0" name="error_message" type="xsd:string"/></xsd:sequence></xsd:complexType></xsd:element></xsd:schema></wsdl:types><wsdl:message name="insertSoapOut"><wsdl:part name="imp_notification" element="tns:insertResponse"/></wsdl:message><wsdl:message name="insertSoapIn"><wsdl:part name="imp_notification" element="tns:insert"/></wsdl:message><wsdl:portType name="ServiceNowSoap"><wsdl:operation name="insert"><wsdl:input message="sncns:insertSoapIn"/><wsdl:output message="sncns:insertSoapOut"/></wsdl:operation></wsdl:portType><wsdl:binding name="ServiceNowSoap" type="sncns:ServiceNowSoap"><soap:binding style="document" transport="http://schemas.xmlsoap.org/soap/http"/><wsdl:operation name="insert"><soap:operation soapAction="http://www.service-now.com/imp_notification/insert" style="document"/><wsdl:input><soap:body use="literal"/></wsdl:input><wsdl:output><soap:body use="literal"/></wsdl:output></wsdl:operation></wsdl:binding><wsdl:service name="ServiceNow"><wsdl:port name="ServiceNowSoap" binding="sncns:ServiceNowSoap"><soap:address location="http://Macintosh-7.local:8080/glide/imp_notification.do?SOAP"/></wsdl:port></wsdl:service></wsdl:definitions>
```

## Sample SOAP Envelope

```
<?xmlversion="1.0"encoding="UTF-8"?><SOAP-ENV:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:SOAP-ENC="http://schemas.xmlsoap.org/soap/encoding/" SOAP-ENV:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/" xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/"><SOAP-ENV:Body><insert xmlns="http://www.service-now.com"><message xsi:type="xsd:string">Host 198.10.10.210 is down</message><uuid xsi:type="xsd:string">HGAF76251HGF1</uuid></insert></SOAP-ENV:Body></SOAP-ENV:Envelope>
```

## Sample SOAP Response

```
<?xmlversion="1.0"encoding="UTF-8"?><SOAP-ENV:Envelope  SOAP-ENV:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/"  xmlns:SOAP-ENC="http://schemas.xmlsoap.org/soap/encoding/"  xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/"  xmlns:xsd="http://www.w3.org/2001/XMLSchema"  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"><SOAP-ENV:Body><insertResponse><sys_id>b54aafbfc0a8006f0058db95daa5b88d</sys_id><table>incident</table><display_name>number</display_name><display_value>INC10008</display_value><status>ignored</status><status_message>No field values changed</status_message></insertResponse></SOAP-ENV:Body></SOAP-ENV:Envelope>
```

## Example Invocation using Perl

The following example script uses the Notification web service to create an Incident as the itil user. It uses the Perl language and the SOAP::Lite package.

```
#!/usr/bin/perl -w
 
#use SOAP::Lite ( +trace => all, maptype => {} );use SOAP::Lite;
 
sub SOAP::Transport::HTTP::Client::get_basic_credentials{return'itil'=>'itil';// set basic auth credentials for the itil user
}
 
my$soap= SOAP::Lite->proxy('http://localhost:8080/glide/imp_notification.do?SOAP');
 
my$method= SOAP::Data->name('insert')->;attr({xmlns =>'http://www.service-now.com/'});
 
# insert into the web servicemy@params=( SOAP::Data->name(message =>'problem detected for database DB12DG'));push(@params, SOAP::Data->name(source =>'DB12DG'));push(@params, SOAP::Data->name(uuid =>'HGAF76251HGF2'));
 
my$result=$soap->call($method=>@params);
 
print_fault($result);//print any SOAP faults
print_result($result);//print any results
 
sub print_result {my($result)=@_;if($result->body&&$result->body->{'insertResponse'}){my%keyHash=%{$result->body->{'insertResponse'}};foreachmy$k(keys%keyHash){print"name=$k   value=$keyHash{$k}\n";}}}
 
sub print_fault {my($result)=@_;if($result->fault){print"faultcode=".$result->fault->{'faultcode'}."\n";print"faultstring=".$result->fault->{'faultstring'}."\n";print"detail=".$result->fault->{'detail'}."\n";}}
```

The following is the result printed by the Perl script on the console.

```
name=display_value   value=INC10011
name=status   value=inserted
name=table   value=incident
name=display_name   value=number
name=sys_id   value=cd45649c0a0a0b2b00e6f27649d6bd2c
```

The following image shows the resultant row created for the import set table Notification \(imp\_notification\).

![](../image/WsIsetPerl.png "WS Iset Perl")

**Parent Topic:**[Web service import sets](c_WebServiceImportSets.md)

