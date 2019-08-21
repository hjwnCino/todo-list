# Platform (Functional) AKA FunLess

FunLess influences many areas of the product. FunLess spends a significant amount of time
developing customer facing features that impact many different areas of the nCino product (DocMan, Smart Checklist, FormsGen etc).

FunLess features are often used in multiple business domains that nCino provides solutions
for (Commercial, Retail, etc), and are tools that can provide value to those domains.

FunLess provides a great opportunity to work on features that use lots of different technologies and
affect a wide variety of business applications.


## Example Application - Smart Checklist:
Smart Checklist is a FunLess feature that is used to track work efforts (requirements) needed in the context of
a given record. Smart Checklist is built to support building requirements on any SObject. Smart Checklist
has implications for many different areas of the nCino product and will be leveraged differently by 
the different teams.

#### Client:
- Visualforce
- TypeScript
- Angular
- ngRX (**[Reducer](https://github.com/ncino/force-LLC_BI/blob/release/src/LLC_BI/checklist/dynamicresources/checklist/src/app/reducers/requirement.ts)**) 
- Types (**[Interface](https://github.com/ncino/force-LLC_BI/blob/release/src/LLC_BI/checklist/dynamicresources/checklist/src/app/interfaces/Requirement.interface.ts)**) 

#### Server:
- SOA (**[Checklist Entity](https://github.com/ncino/force-LLC_BI/blob/release/src/LLC_BI/checklist/classes/Checklist.cls)**)
- Generator/Scheduler (**[Scheduler](https://github.com/ncino/force-LLC_BI/blob/release/src/LLC_BI/checklist-generation/classes/ScheduledChecklistGenerator.cls)**)

