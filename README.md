/lightning/o/DocumentChecklistItem/new?defaultFieldValues=ParentRecordId={!BKU_Loan_Inquiry__c.Id},BKU_Loan_Inquiry__c={!BKU_Loan_Inquiry__c.Id}


-------------


/lightning/o/DocumentChecklistItem/new?defaultFieldValues=ParentRecordId={!IF(ISBLANK(BKU_Loan_Inquiry__c.Id), "", BKU_Loan_Inquiry__c.Id)},BKU_Loan_Inquiry__c={!IF(ISBLANK(BKU_Loan_Inquiry__c.Id), "", BKU_Loan_Inquiry__c.Id)}


--------------

Created lookup field "BKU Loan Inquiry" (BKU_Loan_Inquiry__c) on Document Checklist Item. ParentRecordId on Document Checklist Item is a polymorphic field, which doesn't give us a direct relationship or a dedicated related list on the Loan Inquiry record page. Adding a custom lookup lets us link checklist items directly to a Loan Inquiry and show them in a "Document Checklist Items" related list on the Loan Inquiry page.
Created a custom list button "New" on Document Checklist Item and added it to the related list on the Loan Inquiry record page. The standard New button on the related list doesn't pre-populate ParentRecordId. The custom button uses a URL with defaultFieldValues to pre-fill both ParentRecordId and BKU_Loan_Inquiry__c with the current Loan Inquiry Id, so users don't have to select the parent record manually.
