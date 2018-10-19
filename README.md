# calculator-web-service

This POC demonstrates how to consume a soap webservice and the best practices around that.

## Best Practices
   1. The wsdl and related xsd should be kept in local under src/main/resources/wsdl folder in stead of directly pointing to the URL.
      This helps in faster deployment and deployment failure incase the service is temporaily unavailable.
	    https://raw.githubusercontent.com/indiramallick1988/Demo2/master/Webservice/wsdl.png
	  
   2. Incase the webservice is unavailable temporarily, retry is added through until successful
      https://raw.githubusercontent.com/indiramallick1988/Demo2/master/Webservice/retry.png
      
	 3. The retry can be configured in runtime via propery files.
	    https://raw.githubusercontent.com/indiramallick1988/Demo2/master/Webservice/property.PNG

