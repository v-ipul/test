Hi team, please move the following from DEVWB to INT:

SFWB-94: Document Checklist Item related list on Relationships

Layout: Account-[Business Relationship layout name], e.g. Account-BKU - Business
Layout: PersonAccount-[Individual Relationship layout name]

SFWB-96: Document Checklist Item related list on Opportunity

Layout: Opportunity-BKU - Loan OnePATHE Opportunity Layout
Layout: Opportunity-BKU - Loan - OnePATHE (Pay-Down, Pay-Off or Advance)
Layout: Opportunity-[Renewal, Mod or Extension layout name], if it's a separate layout

Change in both stories: added the Document Checklist Items related list with these columns: Name, Status, Required, Received Document, Last Modified Date, Last Modified By, Owner Name.

Dependency: SFWB-115 (Document Checklist Item Status values) should go together with these, so the Status column shows the right values.

Manual steps: none.

Thanks!"
