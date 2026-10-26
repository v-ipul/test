1. Why (the business problem)

Today RMs price deals in PrecisionLender, which creates a Deal in Salesforce. CPOs don’t use that Deal; they do underwriting in eCAM and re-enter the data by hand.
The future state moves CAM into Salesforce, so the Deal has to become the central workspace for the whole lending lifecycle, handing off from RM to CPO to LCO.
Loan Inquiry is the first building block. It lets a loan request be tracked on its own, separately from the Opportunity and the Deal.

2. What this story delivers

A new custom object, Loan Inquiry (BKU_Loan_Inquiry__c), with reports enabled.
8 fields: an auto number (LI-000000), Name, Origination Source (OnePath/OPX/Commercial Cards), Loan Stage (11 stages from Inquiry Submitted to Paid off), and Amount as a formula from the Opportunity.
3 relationships:
Master-detail to Opportunity, so Opportunity is the parent.
Lookup to Relationship (Account).
Lookup to PL Deal.

Hi, thanks for checking in! It’s been resolved now. Abh created a new user for me and I’m able to log in.
