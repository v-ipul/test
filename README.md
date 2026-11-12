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
