# test
demo test
 update 1

Two new metadata fields — Grant_Owner_Folder_Access__c (Checkbox), Owner_Access_Role__c (Text 20)
   =IF(TRIM(F2)="","",IF(RIGHT(TRIM(F2),8)=".invalid",TRIM(F2),TRIM(F2)&".invalid"))
   SELECT FIELDS(ALL) FROM Lead WHERE IsConverted = false LIMIT 200


SELECT Id, Name, Status, CreatedBy.Name, CreatedDate, LastModifiedBy.Name, LastModifiedDate
FROM ApexClass
ORDER BY Name


One required Setup step

Setup → CSP Trusted Sites → New:

Trusted Site Name: SharePoint_Upload
URL: https://bankunited.sharepoint.com
Active: checked
Context: All
Under "CSP Directives", tick connect-src

SELECT Title, ContentUrl, ContentSize, SharePoint_Sync_Status__c
FROM ContentVersion
WHERE Title LIKE '50mb%' AND IsLatest = true

https://bankunited--devopx.sandbox.lightning.force.com


Authorize Endpoint URL-



Opportunity o = [SELECT StageName, RecordTypeId, RecordType.DeveloperName
                 FROM Opportunity WHERE Id = 'PASTE_OPP_ID'];
System.debug('Stage:      "' + o.StageName + '"');
System.debug('RecordType: "' + o.RecordType.DeveloperName + '"');
https://login.microsoftonline.com/common/oauth2/authorize?resource=https://zl2zb.sharepoint.com&prompt=login I

Token Endpoint URL-

https:/login.microsoftonline.com/common/oauth2/tokenoauth2%2Ftoken&v=NgKZHXPqS6w)


Issue: My user was created with .invalid at the end of my email, which is standard after a sandbox refresh. Because of this, the password setup email never reached me.
Blocker: To fix the email, Salesforce asks me to log in first, but I don’t have a password, so I can’t fix it myself.
Fix needed (admin of that org):
Correct the email on my user record (remove .invalid).
Set a temporary password for me using System.setPassword() in the Developer Console, or use Reset Password once the email is corrected.
