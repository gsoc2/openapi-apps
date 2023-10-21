# Cisco Nexus APIs
Gsoc2 integration for Cisco Nexus 3000 and 9000 series switches.
##### In order to use REST APIs on switch following steps are required. 
**Step 1:** We'll have to enable REST API on switch which we'll allow switch to communicate through http calls.
To enable NX-API, enter the following CLI command on the switch:
``` 
feature nxapi
```
By default, the NX-API REST feature is enabled for HTTP listen on port 80 and HTTPS listen on port 443.
**Step 2:** Now we'll need to authenticate API with Gsoc2. 
- Go to workflows in gsoc2. Create a new workflow.
- Drag in the http app inside workflow. Issue a POST request to https://[IP of Nexus switch]/api/mo/aaaLogin.json with the below example payload.
 ```json
{"aaaUser" : {"attributes" : {"name": "USERNAME","pwd": "PASSWORD"}}
```
This call returns a cookie value that the Gsoc2 uses for the subsequent API calls.
