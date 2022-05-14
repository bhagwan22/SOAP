# SOAP
  - partner WSDL -> loosly typed
  - Enterprise WSDL -> strongly typed (specific to our org configuration, i.e if metadata changes then good practice to update WSDL)

* WSDL 
 - contain binding, protocol and object to make API call
 

# SF SOAP login
    with username & password+security Token
    ~ note: Since you’re making an API request from an IP address unknown to Salesforce, you need to append your security token to the end of your password

# SAMPLE 
    *Endpoint*
    https://login.salesforce.com/services/Soap/c/54.0/

    *BODY*
    <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:urn="urn:enterprise.soap.sforce.com">
       <soapenv:Header>
          <urn:LoginScopeHeader>
             <urn:organizationId>?</urn:organizationId>
             <!--Optional:-->
             <urn:portalId>?</urn:portalId>
          </urn:LoginScopeHeader>
       </soapenv:Header>
       <soapenv:Body>
          <urn:login>
             <urn:username>?</urn:username>
             <urn:password>?</urn:password>
          </urn:login>
       </soapenv:Body>
    </soapenv:Envelope>
