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
