SELECT Id, Name, CreatedBy.Name, CreatedDate
FROM DocumentDecisionRequirement
ORDER BY Name


3. Story 93: Decision table

Deploy: DecisionTable Document_Decision_Requirement.
Manual: open Lookup Tables → Document Decision Requirement → Activate, then Refresh after story 91’s data is loaded.
Check: Status Active and Refresh Status Completed.

4. Story 87: Decision matrix

Deploy:
DecisionMatrixDefinition Document_Type_Settings
DecisionMatrixDefinitionVersion Document_Type_Settings_V1, with its 7 columns
Manual: open version V1 → Upload CSV File (Decision Matrix 1.csv) → Save. The rows don’t deploy as metadata.
Manual: Activate version V1.
If built for AC5: deploy ExpressionSetDefinition [name] and its version, then Activate it in INT.
Check: the version shows Active with the right row count, and Simulate on the Expression Set returns the outputs.

Object: DocumentType (Setup → Document Checklist → Document Types)
Records: [X] Document Types loaded in DEVWB
Fields: MasterLabel, DeveloperName, Description, IsActive


Grants the MuleSoft integration user API access to Salesforce files and related records (Relationship, Opportunity, Loan Inquiry, Deal), and edit access to Document Checklist Item sync fields for the SharePoint integration.

ContentDocument, ContentVersion and ContentDocumentLink don’t have object permissions in a permission set, so access to them is given through the Query All Files app permission, which I’ve enabled in BKU_SF_MuleSoft_SharePoint.

Access to the other objects (Document Checklist Item, Relationship, Opportunity, Loan Inquiry and Deal) is given through object permissions, as defined in the story


Hi team, please move the following from DEVWB to INT. They’re listed in the order they need to go in.

1. SFWB-90: Document Types (data)

Object: DocumentType
Records: 191 Document Types loaded in DEVWB
Fields: MasterLabel, DeveloperName, Description, IsActive
These need to go in first, because stories 87 and 93 reference the Document Type developer names. If Copado can’t move DocumentType as metadata or with Data Deploy, let me know and I’ll load them manually.

2. SFWB-93: Document Decision Requirement

DecisionTable: Document_Decision_Requirement
Expression Set: Document_Decision_Requirement

3. SFWB-87: Document Type Settings

Decision Matrix: Document_Type_Settings, with version Document_Type_Settings_V1
Expression Set: Document_Type_Settings

4. SFWB-101: MuleSoft SharePoint integration

PermissionSet: BKU_SF_MuleSoft_SharePoint
Dependencies: Loan Inquiry object BKU_Loan_Inquiry__c (SFWB-71) and the four sync fields on Document Checklist Item
