---
title: Create a SOAP message from a WSDL that references an external XSD file
description: Create a SOAP message from a WSDL and external XSD file.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Messages, SOAP, Outbound, Web services, API implementation, API implementation and reference]
---

# Create a SOAP message from a WSDL that references an external XSD file

Create a SOAP message from a WSDL and external XSD file.

## Before you begin

Role required: web\_service\_admin

## About this task

This task includes example WSDL and XSD files for a weather forecast SOAP message. Your WSDL and XSD file will vary.

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **SOAP Message** and create a new record.

2.  Clear the **Download WSDL** check box.

3.  Paste the content of the WSDL into the **WSDL XML** field.

4.  Save the record.

5.  In the **SOAP Message Imports** related list, click **New**.

6.  Paste the content of the XSD file into the **External Document** field.

7.  Set the **Schema Location** field to `db://<name of the referenced XSD file>.xsd`.

    Specifying the schema location allows the instance to know the location of the referenced XSD file.

8.  Click **Submit.**

9.  Click **Generate sample SOAP messages**.


## Example WSDL and XSD files

```
<?xml version="1.0" encoding="utf-8"?>
<wsdl:definitions xmlns:tm="http://microsoft.com/wsdl/mime/textMatching/" xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/" xmlns:mime="http://schemas.xmlsoap.org/wsdl/mime/" xmlns:tns="http://www.webservicex.net" xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:s="http://www.w3.org/2001/XMLSchema" xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" xmlns:http="http://schemas.xmlsoap.org/wsdl/http/" targetNamespace="http://www.webservicex.net" xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
  <wsdl:documentation xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">Get one week weather forecast for valid zip code or Place name in USA</wsdl:documentation>
  <wsdl:types>
    <s:schema elementFormDefault="qualified" targetNamespace="http://www.webservicex.net">
       <s:include schemaLocation="WeatherForecast.xsd" />
    </s:schema>
  </wsdl:types>
  <wsdl:message name="GetWeatherByZipCodeSoapIn">
    <wsdl:part name="parameters" element="tns:GetWeatherByZipCode" />
  </wsdl:message>
  <wsdl:message name="GetWeatherByZipCodeSoapOut">
    <wsdl:part name="parameters" element="tns:GetWeatherByZipCodeResponse" />
  </wsdl:message>
  <wsdl:message name="GetWeatherByPlaceNameSoapIn">
    <wsdl:part name="parameters" element="tns:GetWeatherByPlaceName" />
  </wsdl:message>
  <wsdl:message name="GetWeatherByPlaceNameSoapOut">
    <wsdl:part name="parameters" element="tns:GetWeatherByPlaceNameResponse" />
  </wsdl:message>
  <wsdl:message name="GetWeatherByZipCodeHttpGetIn">
    <wsdl:part name="ZipCode" type="s:string" />
  </wsdl:message>
  <wsdl:message name="GetWeatherByZipCodeHttpGetOut">
    <wsdl:part name="Body" element="tns:WeatherForecasts" />
  </wsdl:message>
  <wsdl:message name="GetWeatherByPlaceNameHttpGetIn">
    <wsdl:part name="PlaceName" type="s:string" />
  </wsdl:message>
  <wsdl:message name="GetWeatherByPlaceNameHttpGetOut">
    <wsdl:part name="Body" element="tns:WeatherForecasts" />
  </wsdl:message>
  <wsdl:message name="GetWeatherByZipCodeHttpPostIn">
    <wsdl:part name="ZipCode" type="s:string" />
  </wsdl:message>
  <wsdl:message name="GetWeatherByZipCodeHttpPostOut">
    <wsdl:part name="Body" element="tns:WeatherForecasts" />
  </wsdl:message>
  <wsdl:message name="GetWeatherByPlaceNameHttpPostIn">
    <wsdl:part name="PlaceName" type="s:string" />
  </wsdl:message>
  <wsdl:message name="GetWeatherByPlaceNameHttpPostOut">
    <wsdl:part name="Body" element="tns:WeatherForecasts" />
  </wsdl:message>
  <wsdl:portType name="WeatherForecastSoap">
    <wsdl:operation name="GetWeatherByZipCode">
      <wsdl:documentation xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">Get one week weather forecast for a valid Zip Code(USA)</wsdl:documentation>
      <wsdl:input message="tns:GetWeatherByZipCodeSoapIn" />
      <wsdl:output message="tns:GetWeatherByZipCodeSoapOut" />
    </wsdl:operation>
    <wsdl:operation name="GetWeatherByPlaceName">
      <wsdl:documentation xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">Get one week  weather forecast for a place name(USA)</wsdl:documentation>
      <wsdl:input message="tns:GetWeatherByPlaceNameSoapIn" />
      <wsdl:output message="tns:GetWeatherByPlaceNameSoapOut" />
    </wsdl:operation>
  </wsdl:portType>
  <wsdl:portType name="WeatherForecastHttpGet">
    <wsdl:operation name="GetWeatherByZipCode">
      <wsdl:documentation xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">Get one week weather forecast for a valid Zip Code(USA)</wsdl:documentation>
      <wsdl:input message="tns:GetWeatherByZipCodeHttpGetIn" />
      <wsdl:output message="tns:GetWeatherByZipCodeHttpGetOut" />
    </wsdl:operation>
    <wsdl:operation name="GetWeatherByPlaceName">
      <wsdl:documentation xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">Get one week  weather forecast for a place name(USA)</wsdl:documentation>
      <wsdl:input message="tns:GetWeatherByPlaceNameHttpGetIn" />
      <wsdl:output message="tns:GetWeatherByPlaceNameHttpGetOut" />
    </wsdl:operation>
  </wsdl:portType>
  <wsdl:portType name="WeatherForecastHttpPost">
    <wsdl:operation name="GetWeatherByZipCode">
      <wsdl:documentation xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">Get one week weather forecast for a valid Zip Code(USA)</wsdl:documentation>
      <wsdl:input message="tns:GetWeatherByZipCodeHttpPostIn" />
      <wsdl:output message="tns:GetWeatherByZipCodeHttpPostOut" />
    </wsdl:operation>
    <wsdl:operation name="GetWeatherByPlaceName">
      <wsdl:documentation xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">Get one week  weather forecast for a place name(USA)</wsdl:documentation>
      <wsdl:input message="tns:GetWeatherByPlaceNameHttpPostIn" />
      <wsdl:output message="tns:GetWeatherByPlaceNameHttpPostOut" />
    </wsdl:operation>
  </wsdl:portType>
  <wsdl:binding name="WeatherForecastSoap" type="tns:WeatherForecastSoap">
    <soap:binding transport="http://schemas.xmlsoap.org/soap/http" />
    <wsdl:operation name="GetWeatherByZipCode">
      <soap:operation soapAction="http://www.webservicex.net/GetWeatherByZipCode" style="document" />
      <wsdl:input>
        <soap:body use="literal" />
      </wsdl:input>
      <wsdl:output>
        <soap:body use="literal" />
      </wsdl:output>
    </wsdl:operation>
    <wsdl:operation name="GetWeatherByPlaceName">
      <soap:operation soapAction="http://www.webservicex.net/GetWeatherByPlaceName" style="document" />
      <wsdl:input>
        <soap:body use="literal" />
      </wsdl:input>
      <wsdl:output>
        <soap:body use="literal" />
      </wsdl:output>
    </wsdl:operation>
  </wsdl:binding>
  <wsdl:binding name="WeatherForecastSoap12" type="tns:WeatherForecastSoap">
    <soap12:binding transport="http://schemas.xmlsoap.org/soap/http" />
    <wsdl:operation name="GetWeatherByZipCode">
      <soap12:operation soapAction="http://www.webservicex.net/GetWeatherByZipCode" style="document" />
      <wsdl:input>
        <soap12:body use="literal" />
      </wsdl:input>
      <wsdl:output>
        <soap12:body use="literal" />
      </wsdl:output>
    </wsdl:operation>
    <wsdl:operation name="GetWeatherByPlaceName">
      <soap12:operation soapAction="http://www.webservicex.net/GetWeatherByPlaceName" style="document" />
      <wsdl:input>
        <soap12:body use="literal" />
      </wsdl:input>
      <wsdl:output>
        <soap12:body use="literal" />
      </wsdl:output>
    </wsdl:operation>
  </wsdl:binding>
  <wsdl:binding name="WeatherForecastHttpGet" type="tns:WeatherForecastHttpGet">
    <http:binding verb="GET" />
    <wsdl:operation name="GetWeatherByZipCode">
      <http:operation location="/GetWeatherByZipCode" />
      <wsdl:input>
        <http:urlEncoded />
      </wsdl:input>
      <wsdl:output>
        <mime:mimeXml part="Body" />
      </wsdl:output>
    </wsdl:operation>
    <wsdl:operation name="GetWeatherByPlaceName">
      <http:operation location="/GetWeatherByPlaceName" />
      <wsdl:input>
        <http:urlEncoded />
      </wsdl:input>
      <wsdl:output>
        <mime:mimeXml part="Body" />
      </wsdl:output>
    </wsdl:operation>
  </wsdl:binding>
  <wsdl:binding name="WeatherForecastHttpPost" type="tns:WeatherForecastHttpPost">
    <http:binding verb="POST" />
    <wsdl:operation name="GetWeatherByZipCode">
      <http:operation location="/GetWeatherByZipCode" />
      <wsdl:input>
        <mime:content type="application/x-www-form-urlencoded" />
      </wsdl:input>
      <wsdl:output>
        <mime:mimeXml part="Body" />
      </wsdl:output>
    </wsdl:operation>
    <wsdl:operation name="GetWeatherByPlaceName">
      <http:operation location="/GetWeatherByPlaceName" />
      <wsdl:input>
        <mime:content type="application/x-www-form-urlencoded" />
      </wsdl:input>
      <wsdl:output>
        <mime:mimeXml part="Body" />
      </wsdl:output>
    </wsdl:operation>
  </wsdl:binding>
  <wsdl:service name="WeatherForecast">
    <wsdl:documentation xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">Get one week weather forecast for valid zip code or Place name in USA</wsdl:documentation>
    <wsdl:port name="WeatherForecastSoap" binding="tns:WeatherForecastSoap">
      <soap:address location="http://www.webservicex.net/WeatherForecast.asmx" />
    </wsdl:port>
    <wsdl:port name="WeatherForecastSoap12" binding="tns:WeatherForecastSoap12">
      <soap12:address location="http://www.webservicex.net/WeatherForecast.asmx" />
    </wsdl:port>
    <wsdl:port name="WeatherForecastHttpGet" binding="tns:WeatherForecastHttpGet">
      <http:address location="http://www.webservicex.net/WeatherForecast.asmx" />
    </wsdl:port>
    <wsdl:port name="WeatherForecastHttpPost" binding="tns:WeatherForecastHttpPost">
      <http:address location="http://www.webservicex.net/WeatherForecast.asmx" />
    </wsdl:port>
  </wsdl:service>
</wsdl:definitions>

```

```
<s:schema elementFormDefault="qualified" targetNamespace="http://www.webservicex.net" xmlns:s="http://www.w3.org/2001/XMLSchema" xmlns:tns="http://www.webservicex.net" >
      <s:element name="GetWeatherByZipCode">
        <s:complexType>
          <s:sequence>
            <s:element minOccurs="0" maxOccurs="1" name="ZipCode" type="s:string" />
          </s:sequence>
        </s:complexType>
      </s:element>
      <s:element name="GetWeatherByZipCodeResponse">
        <s:complexType>
          <s:sequence>
            <s:element minOccurs="1" maxOccurs="1" name="GetWeatherByZipCodeResult" type="tns:WeatherForecasts" />
          </s:sequence>
        </s:complexType>
      </s:element>
      <s:complexType name="WeatherForecasts">
        <s:sequence>
          <s:element minOccurs="1" maxOccurs="1" name="Latitude" type="s:float" />
          <s:element minOccurs="1" maxOccurs="1" name="Longitude" type="s:float" />
          <s:element minOccurs="1" maxOccurs="1" name="AllocationFactor" type="s:float" />
          <s:element minOccurs="0" maxOccurs="1" name="FipsCode" type="s:string" />
          <s:element minOccurs="0" maxOccurs="1" name="PlaceName" type="s:string" />
          <s:element minOccurs="0" maxOccurs="1" name="StateCode" type="s:string" />
          <s:element minOccurs="0" maxOccurs="1" name="Status" type="s:string" />
          <s:element minOccurs="0" maxOccurs="1" name="Details" type="tns:ArrayOfWeatherData" />
        </s:sequence>
      </s:complexType>
      <s:complexType name="ArrayOfWeatherData">
        <s:sequence>
          <s:element minOccurs="0" maxOccurs="unbounded" name="WeatherData" type="tns:WeatherData" />
        </s:sequence>
      </s:complexType>
      <s:complexType name="WeatherData">
        <s:sequence>
          <s:element minOccurs="0" maxOccurs="1" name="Day" type="s:string" />
          <s:element minOccurs="0" maxOccurs="1" name="WeatherImage" type="s:string" />
          <s:element minOccurs="0" maxOccurs="1" name="MaxTemperatureF" type="s:string" />
          <s:element minOccurs="0" maxOccurs="1" name="MinTemperatureF" type="s:string" />
          <s:element minOccurs="0" maxOccurs="1" name="MaxTemperatureC" type="s:string" />
          <s:element minOccurs="0" maxOccurs="1" name="MinTemperatureC" type="s:string" />
        </s:sequence>
      </s:complexType>
      <s:element name="GetWeatherByPlaceName">
        <s:complexType>
          <s:sequence>
            <s:element minOccurs="0" maxOccurs="1" name="PlaceName" type="s:string" />
          </s:sequence>
        </s:complexType>
      </s:element>
      <s:element name="GetWeatherByPlaceNameResponse">
        <s:complexType>
          <s:sequence>
            <s:element minOccurs="1" maxOccurs="1" name="GetWeatherByPlaceNameResult" type="tns:WeatherForecasts" />
          </s:sequence>
        </s:complexType>
      </s:element>
      <s:element name="WeatherForecasts" type="tns:WeatherForecasts" />
    </s:schema>


```

**Parent Topic:**[SOAP message](../concept/c_SOAPMessage.md)

