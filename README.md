BKU_Loan_Inquiry__c li = [SELECT Id, Name FROM BKU_Loan_Inquiry__c LIMIT 1];

DocumentChecklistItem dci = new DocumentChecklistItem(
    Name = 'Test DCI - Loan Inquiry',
    ParentRecordId = li.Id,
    Status = 'New'
);
insert dci;

System.debug('Created DCI: ' + dci.Id + ' on Loan Inquiry: ' + li.Name);



SELECT Id, Name, Status, ParentRecordId FROM DocumentChecklistItem WHERE Name = 'Test DCI - Loan Inquiry'
