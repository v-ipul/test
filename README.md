BKU_Loan_Inquiry__c li = [SELECT Id, Name FROM BKU_Loan_Inquiry__c LIMIT 1];

DocumentChecklistItem dci = new DocumentChecklistItem(
    Name = 'Test DCI - Loan Inquiry',
    ParentRecordId = li.Id,
    Status = 'New'
);
insert dci;

System.debug('Created DCI: ' + dci.Id + ' on Loan Inquiry: ' + li.Name);



SELECT Id, Name, Status, ParentRecordId FROM DocumentChecklistItem WHERE Name = 'Test DCI - Loan Inquiry'

Manual step (SFWB-94): give Create access on Document Checklist Item

Go to Setup → Quick Find → Permission Sets → open BKU WB RM.
Click Object Settings → Document Checklist Items → Edit.
Under Object Permissions, tick Read and Create.
Under Field Permissions, tick Read Access for Name, Status, Required, Received Document and Owner.
Click Save.
Repeat steps 1–5 for BKU WB CPO.
