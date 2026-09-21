# test
demo test
 update 1

 sf project deploy start --source-dir force-app/main/default/lwc

 HttpRequest req = new HttpRequest();
req.setEndpoint('callout:Sharepoint_Named_Credential/sites/bankunited.sharepoint.com:/sites/WB:/drives');
req.setMethod('GET');
System.debug(new Http().send(req).getBody());
