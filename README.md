# multiple-webservice-wsdl-papi
multiple-webservice-wsdl-papi is created to handle multiple wsdl's in a single api 

# multiple-webservice-wsdl-papi

########Maven command for publishing app into an exchange:
mvn clean deploy 


#########Maven command for deploying an application from exchange to Runtime Manager:
mvn clean deploy -DmuleDeploy -Dserver=anypoint-connected-app -DappName=multiple-webservice-wsdl-papi -DmuleVersion=4.4.0 -DtargetName=Cloudhub-US-East-2 -Denvironment=Sandbox -Dreplicas=1 -DreplicasType=0.1 -Dbranch.name=dev -Ddecryption.key=goodluckDEV12345


#########Localhost Endpoints ::  Based on SOAPAction . So this can test only from SOAPUI using proper request
http://localhost:8081/api/v1/HelloWorldService/HelloWorldPort?wsdl
http://localhost:8081/api/v1/CalculatorService/CalculatorPort?wsdl
http://localhost:8081/api/v1/ContractSOAPQSService/ContractSOAPQSPort?wsdl
http://localhost:8081/api/v1/NDPEventOAGSvc/NDPEventOAGSvcBindingPort?wsdl

######Localhost Endpoints ::  Based on WSDL Service and WSDL Port . So this can test from SOAPUI using proper request and load wsdl in browser
http://localhost:8087/api/v2/HelloWorldService/HelloWorldPort?wsdl
http://localhost:8087/api/v2/CalculatorService/CalculatorPort
http://localhost:8087/api/v2/ContractSOAPQSService/ContractSOAPQSPort


########### Localhost Endpoints :: This is REST based Listener Can test from browser and POSTMAN
http://localhost:8088/api/v3/HelloWorldService/HelloWorldPort
http://localhost:8088/api/v3/CalculatorService/CalculatorPort
http://localhost:8088/api/v3/ContractSOAPQSService/ContractSOAPQSPort


############ API Deployed to CLOUDHUB2.0 This can be test from SOAPUI and WSDL can load in Browser .
	https://multiple-webservice-wsdl-papi-lewuz5.5sc6y6-4.usa-e2.cloudhub.io/api/HelloWorldService/HelloWorldPort?wsdl
	https://multiple-webservice-wsdl-papi-lewuz5.5sc6y6-4.usa-e2.cloudhub.io/api/CalculatorService/CalculatorPort?wsdl
	https://multiple-webservice-wsdl-papi-lewuz5.5sc6y6-4.usa-e2.cloudhub.io/api/ContractSOAPQSService/ContractSOAPQSPort?wsdl
	https://multiple-webservice-wsdl-papi-lewuz5.5sc6y6-4.usa-e2.cloudhub.io/api/NDPEventOAGSvc/NDPEventOAGSvcBindingPort?wsdl



########GIT Actions Secret Variables :

ANYPOINT_PLATFORM_KEY_DEV ---> goodluckDEV12345
ANYPOINT_PLATFORM_KEY_QA  ---> goodluckDEV12345
ANYPOINT_PLATFORM_KEY_UAT ----> goodluckDEV12345
ANYPOINT_PLATFORM_KEY_PROD --->> goodluckDEV12345
ANYPOINT_PLATFORM_PASSWORD  --->  ~~~Client~~~
ANYPOINT_PLATFORM_USERNAME  --->> 4ce6bfd5f2ed4ab1a667e19254d0054b~?~c930A975d6794F7982A18CEf23EdDc7E


