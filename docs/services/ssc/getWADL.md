# Get WADL
This service provides the [Web Application Description Language (WADL)](https://en.wikipedia.org/wiki/Web_Application_Description_Language) for these Web services.

## Example Response
Below is an example client request to this service, along with the result.

```bash
$ curl https://sscweb.gsfc.nasa.gov/WS/sscr/2/application.wadl | xmllint --format -
```

### Response
```xml  
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<application xmlns="http://wadl.dev.java.net/2009/02">
  <doc xmlns:jersey="http://jersey.java.net/" jersey:generatedBy="Jersey: 2.34.payara-p1 2021-08-18 10:17:28"/>
  <doc xmlns:jersey="http://jersey.java.net/" jersey:hint="This is simplified WADL with user and core resources only. To get full WADL with extended resources use the query parameter detail. Link: https://sscweb.gsfc.nasa.gov/WS/sscr/2/application.wadl?detail=true"/>
  <grammars>
    <include href="application.wadl/xsd0.xsd">
      <doc title="Generated" xml:lang="en"/>
    </include>
  </grammars>
  <resources base="https://sscweb.gsfc.nasa.gov/WS/sscr/2/">
    <resource path="/">
      <resource path="/conjunctions">
        <method id="getConjunctions" name="POST">
          <request>
            <param xmlns:xs="http://www.w3.org/2001/XMLSchema" name="javax.ws.rs.container.Suspended" type="xs:string"/>
            <representation xmlns:ns2="http://sscweb.gsfc.nasa.gov/schema" element="ns2:QueryRequest" mediaType="application/xml"/>
            <representation xmlns:ns2="http://sscweb.gsfc.nasa.gov/schema" element="ns2:QueryRequest" mediaType="application/json"/>
          </request>
        </method>
      </resource>
      <resource path="/graphs">
        <method id="getGraphs" name="POST">
          <request>
            <param xmlns:xs="http://www.w3.org/2001/XMLSchema" name="javax.ws.rs.container.Suspended" type="xs:string"/>
            <representation xmlns:ns2="http://sscweb.gsfc.nasa.gov/schema" element="ns2:GraphRequest" mediaType="application/xml"/>
            <representation xmlns:ns2="http://sscweb.gsfc.nasa.gov/schema" element="ns2:GraphRequest" mediaType="application/json"/>
          </request>
        </method>
      </resource>
      <resource path="/observatories/{object: [a-z][a-z0-1]*}/clientLibraryExample/{library : (?:(sscws)([Pp]y|[Ii]dl))?(?:,(?:(sscws)([Pp]y|[Ii]dl)))?}">
        <param xmlns:xs="http://www.w3.org/2001/XMLSchema" name="library" style="template" type="xs:string"/>
        <param xmlns:xs="http://www.w3.org/2001/XMLSchema" name="object" style="template" type="xs:string"/>
        <method id="getClientLibraryExample" name="GET">
          <request>
            <param xmlns:xs="http://www.w3.org/2001/XMLSchema" name="mediaType" style="query" type="xs:string"/>
          </request>
          <response>
            <representation mediaType="text/plain"/>
            <representation mediaType="text/x-python"/>
            <representation mediaType="text/x-idl"/>
            <representation mediaType="application/octet-stream"/>
            <representation mediaType="application/xhtml+xml"/>
          </response>
        </method>
      </resource>
      <resource path="/observatories">
        <method id="getAllObservatories" name="GET">
          <response>
            <representation mediaType="application/xml"/>
            <representation mediaType="application/json"/>
          </response>
        </method>
      </resource>
      <resource path="/kml">
        <method id="getKmlFiles" name="POST">
          <request>
            <param xmlns:xs="http://www.w3.org/2001/XMLSchema" name="javax.ws.rs.container.Suspended" type="xs:string"/>
            <representation xmlns:ns2="http://sscweb.gsfc.nasa.gov/schema" element="ns2:KmlRequest" mediaType="application/xml"/>
            <representation xmlns:ns2="http://sscweb.gsfc.nasa.gov/schema" element="ns2:KmlRequest" mediaType="application/json"/>
          </request>
        </method>
      </resource>
      <resource path="/locations">
        <method id="getData" name="POST">
          <request>
            <param xmlns:xs="http://www.w3.org/2001/XMLSchema" name="javax.ws.rs.container.Suspended" type="xs:string"/>
            <representation xmlns:ns2="http://sscweb.gsfc.nasa.gov/schema" element="ns2:DataRequest" mediaType="application/xml"/>
            <representation xmlns:ns2="http://sscweb.gsfc.nasa.gov/schema" element="ns2:DataRequest" mediaType="application/json"/>
          </request>
        </method>
      </resource>
      <resource path="/spaseObservatories">
        <method id="getAllSpaseObservatories" name="GET">
          <response>
            <representation mediaType="application/xml"/>
            <representation mediaType="application/json"/>
          </response>
        </method>
      </resource>
      <resource path="/status">
        <method id="getStatus" name="POST">
          <request>
            <representation mediaType="application/x-www-form-urlencoded">
              <param xmlns:xs="http://www.w3.org/2001/XMLSchema" name="refresh" style="query" type="xs:int"/>
              <param xmlns:xs="http://www.w3.org/2001/XMLSchema" name="emailUpdate" style="query" type="xs:string"/>
              <param xmlns:xs="http://www.w3.org/2001/XMLSchema" name="emailNotifications" style="query" type="xs:boolean"/>
            </representation>
          </request>
          <response>
            <representation mediaType="application/xml"/>
            <representation mediaType="application/json"/>
          </response>
        </method>
        <method id="getStatus" name="GET">
          <request>
            <param xmlns:xs="http://www.w3.org/2001/XMLSchema" name="refresh" style="query" type="xs:int"/>
          </request>
          <response>
            <representation mediaType="application/xml"/>
            <representation mediaType="application/json"/>
          </response>
        </method>
      </resource>
      <resource path="/groundStations">
        <method id="getAllGroundStations" name="GET">
          <response>
            <representation mediaType="application/xml"/>
            <representation mediaType="application/json"/>
          </response>
        </method>
      </resource>
      <resource path="/echoGraphRequest">
        <method id="echoRequest" name="POST">
          <request>
            <representation xmlns:ns2="http://sscweb.gsfc.nasa.gov/schema" element="ns2:GraphRequest" mediaType="application/xml"/>
            <representation xmlns:ns2="http://sscweb.gsfc.nasa.gov/schema" element="ns2:GraphRequest" mediaType="application/json"/>
          </request>
          <response>
            <representation mediaType="application/xml"/>
            <representation mediaType="application/json"/>
          </response>
        </method>
      </resource>
      <resource path="/locations/{objects: ([a-z][a-z0-9]*)(,[a-z][a-z0-9]*)*}/{time: [0-9]{4}(((0[1-9])|(1[0-2]))(([0-2][0-9])|(3[0-1]))?)?T((([0-1][0-9])|(2[0-4]))(([0-5][0-9])(([0-5][0-9])|(60))?)?)?Z,[0-9]{4}(((0[1-9])|(1[0-2]))(([0-2][0-9])|(3[0-1]))?)?T((([0-1][0-9])|(2[0-4]))(([0-5][0-9])(([0-5][0-9])|(60))?)?)?Z}/{coordSystems: ([a-z][a-z0-9]+)?(,[a-z][a-z0-9]*)*}">
        <param xmlns:xs="http://www.w3.org/2001/XMLSchema" name="coordSystems" style="template" type="xs:string"/>
        <param xmlns:xs="http://www.w3.org/2001/XMLSchema" name="objects" style="template" type="xs:string"/>
        <param xmlns:xs="http://www.w3.org/2001/XMLSchema" name="time" style="template" type="xs:string"/>
        <method id="getData" name="GET">
          <request>
            <param xmlns:xs="http://www.w3.org/2001/XMLSchema" name="output" style="query" type="xs:string"/>
            <param xmlns:xs="http://www.w3.org/2001/XMLSchema" name="javax.ws.rs.container.Suspended" type="xs:string"/>
          </request>
        </method>
      </resource>
      <resource path="/echoQueryRequest">
        <method id="echoRequest" name="POST">
          <request>
            <representation xmlns:ns2="http://sscweb.gsfc.nasa.gov/schema" element="ns2:QueryRequest" mediaType="application/xml"/>
            <representation xmlns:ns2="http://sscweb.gsfc.nasa.gov/schema" element="ns2:QueryRequest" mediaType="application/json"/>
          </request>
          <response>
            <representation mediaType="application/xml"/>
            <representation mediaType="application/json"/>
          </response>
        </method>
      </resource>
      <resource path="/echoDataRequest">
        <method id="echoRequest" name="POST">
          <request>
            <representation xmlns:ns2="http://sscweb.gsfc.nasa.gov/schema" element="ns2:DataRequest" mediaType="application/xml"/>
            <representation xmlns:ns2="http://sscweb.gsfc.nasa.gov/schema" element="ns2:DataRequest" mediaType="application/json"/>
          </request>
          <response>
            <representation mediaType="application/xml"/>
            <representation mediaType="application/json"/>
          </response>
        </method>
      </resource>
    </resource>
  </resources>
</application>
```