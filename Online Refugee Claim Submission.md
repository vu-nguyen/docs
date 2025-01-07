# Online Refugee Claim Submission

## Background

Immigration, Refugees, and Citizenship Canada (IRCC) and the Canada Border Services Agency (CBSA) both process refugee claims and make eligibility determination. Immigration and Refugee Board (IRB) also makes a determination on the basis of claim.

The work is divided into CBSA processing refugee claims made the Port of Entry (PoE) and IRCC and CBSA processing inland refugee claims.

## Barriers

Current inland refugee claims are done through claimants filling out multiple forms and sending it to IRCC and CBSA (with IRB playing some role) for processing. This process is labor intensive and time consuming. The form itself is long and confusing as to what information is required.

Current list of forms used are:

- Document Checklist ([IMM 5745](https://www.canada.ca/content/dam/ircc/migration/ircc/english/pdf/kits/forms/imm5745e.pdf))
- Generic Application Form for Canada ([IMM 0008](https://www.canada.ca/content/dam/ircc/migration/ircc/english/pdf/kits/forms/imm0008enu_2d.pdf))
- Additional Dependents / Declaration ([IMM 0008DEP](https://www.canada.ca/content/dam/ircc/migration/ircc/english/pdf/kits/forms/imm0008depenu.pdf)), if you have more dependents than can be listed on the Generic Application Form for Canada
- Schedule A – Background / Declaration ([IMM 5669](https://www.canada.ca/content/dam/ircc/migration/ircc/english/pdf/kits/forms/imm5669e.pdf))
- Schedule 12 – Refugee Claimants Inside Canada ([IMM 0008 – Schedule 12](https://www.canada.ca/content/dam/ircc/migration/ircc/english/pdf/kits/forms/imm0008_12e.pdf))
- Use of a Representative ([IMM 5476](https://www.canada.ca/content/dam/ircc/migration/ircc/english/pdf/kits/forms/imm5476e.pdf)), if applicable
- [Basis of Claim](https://www.irb-cisr.gc.ca/en/pages/index.aspx) (IRB)

## Business Requirements

> To digitalize and streamline the refugee claim process to allow claimants or their authorized representatives to submit claims online and/or submit subsequent information after claim is made.

We want to design a client-friendly, streamline, accessible digital process that helps to cut down on processing time. The digitalization of the process will also help in reducing the administrative burden on IRCC and CBSA staff.

## User Journey

The user journey for submitting refugee claim is as follow. 

1. Answer short questionnaire to determine if user is eligible to make refugee claim
2. User download application package containing the various forms
3. From the forms, the following information are required:
   - Generic Application Form (IMM 0008) gathers
     - Application deatils
     - Personal details (IMM 0008)
     - Contact information (IMM 0008)
     - Passport information (IMM 0008)
     - National identity (IMM 0008)
     - Education (IMM 0008)
     - Language detail (IMM 0008)
     - Dependants details (including passport, national identity, education, and language) (IMM 0008 and IMM 0008DEP if needed)
   - Background information (IMM 5669 - Schedule A) gathers
     - Parent's information
     - Education/employment history (10 years)
     - Government employment
     - Military/government service
     - Organization affiliates
   - Additional information for claimants inside Canada (IMM 0008 - Schedule 12)
     - Travel to Canada details
     - Travel documents
     - Supporting documents to support refugee claim
   - Use of a representative (IMM 5476), if applicable
   - Basis of claim (IRB)
4. Send application package to [IRCC.RefugeeClaim-Demandedasile.IRCC@cic.gc.ca](mailto:IRCC.RefugeeClaim-Demandedasile.IRCC@cic.gc.ca) through [epost Connect](https://www.canadapost.ca/cpc/en/business/postal-services/digital-mail/epost-connect.page) for secure delivery
5. Wait for **acknowledgement of claim letter** along with instructions to complete a medical examination and schedule an interview
6. Following the interview, the user will be provided with various documents, such as
   - Notice of Seizure
   - Acknowledgement of Conditions
   - An A44 Report, outlining inadmissibilities
   - Refugee Protection Claimant Document
   - Removal Order
   - Confirmation of Referral to IRB, if eligible
   - And other forms
7. Wait for IRB's decision

This whole process can take months.

## Administrative User Journey

The user journey for the administrative side is as follow.

1. IRCC receives the refugee claim application
2. Review the submitted forms for completeness
3. Schedule an interview
4. Enter the information provided into GCMS
5. Package information for security screening and refugee 
