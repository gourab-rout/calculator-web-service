# calculator-web-service

This POC demonstrates how to consume a soap webservice and the best practices around that.

## Best Practices
   1. The wsdl and related xsd should be kept in local under src/main/resources/wsdl folder in stead of directly pointing to the URL.
      This makes the application deployment otherwise it takes time to download and fetch the related schemas.
      It also avoids the deployment failure incase the service is temporaily unavailable.
      
      ![ScreenShot](https://raw.githubusercontent.com/indiramallick1988/Demo2/master/Webservice/wsdl.png)
	  
   2. Incase the webservice is unavailable temporarily, retry is added through until successful.
   
      ![ScreenShot](https://raw.githubusercontent.com/indiramallick1988/Demo2/master/Webservice/retry.png)
      
   3. The retry can be configured in runtime via property files.
   
      ![ScreenShot](https://raw.githubusercontent.com/indiramallick1988/Demo2/master/Webservice/property.PNG)
      
## Testing
   1. Once the application is deployed locally it can be tested as below
   
   ### Sum
   URL: http://localhost:8081/sum
   METHOD: POST
   MIME TYPE: APPLICATION/JSON
   REQUEST: {
	"num1" : 10,
	"num2" : 20
   }
   ### Multiply
   URL: http://localhost:8081/multiply
   METHOD: POST
   MIME TYPE: APPLICATION/JSON
   REQUEST: {
	"num1" : 10,
	"num2" : 20
   }

