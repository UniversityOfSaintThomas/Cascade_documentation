# Cascade LPs/RFIs
Documentation for the current state of RFIs and Landing pages within CascadeCMS
## Data Definition/Shared Field values
- | Orion - RFI<br>(Shared Field) | Capricorn - RFI Form<br>(Shared Field) | Salesforce API Name | Notes
- |------ | ------ | ------ | ------
1 | - | Background Color (Radio) | -
2 | Heading (Text)   | Heading (Text) | -
3 | - | Short Description (Text) | -
4 | **Domain (Dropdown) | *Confirmation Page Host (Dropdown) | -
5 | *Confirmation Page (Link) | *Confirmation Page (Link) | retURL
6 | *Submit Button Text (Text) | *Submit Button Text (Text) | -
7 | *Program Catalog (Dropdown) | *Program Catalog (Dropdown) | Program_Catalog__c
8 | College (Dropdown) | Fields -> <br>Graduate College/Programs -><br>College (Dropdown) | School__c
9 | Programs (Multi-select) | Fields -> <br>Graduate College/Programs -><br>Programs (Multi-select) | Major_Code__c <br> Program_Offered_Code__c
10 | Filter Programs (Multi-select) | - | -
11 | Program Offered Code (Multi-select) | - | Program_Offered_Code
12 | Degree Types (Dropdown List) | Fields -> <br>Graduate College/Programs -><br>Degree Types (Dropdown List) | - | Prioritized sorting in the Programs field by Degree Type
13 | *Environment (Dropdown) | *Environment (Dropdown) | oid
14 | Lead Source (Dropdown) | Lead Source (Dropdown) | lead_source
15 | Campaign ID (Text) | - | Campaign_ID
16 | Debug (Checkbox) | Debug (Checkbox) | debug
17 | ReCaptcha | ReCaptcha | -
18 | Pardot | Pardot | - | Not within "Landing page two" format
19 | UTM -> <br> Campaign (Text) | UTM -> <br> Campaign (Text) | utm_campaign__c
20 | UTM -> <br> Medium (Text) | UTM -> <br> Medium (Text) | utm_medium__c
21 | UTM -> <br> Source (Text) | UTM -> <br> Source (Text) | utm_source__c
22 | UTM -> <br> Content (Text) | UTM -> <br> Content (Text) | utm_content__c
23 | UTM -> <br> Term (Text) | UTM -> <br> Term (Text) | utm_term__c
24 | Fields -><br>Apply As [Enable, Required, Enable & Hidden (Dropdown)] | Fields -><br>Apply As [Enable, Required] | Inquiry_Applicant_Type__c
25 | Fields -><br>Citizenship [Enable, Required] | Fields -><br>Citizenship [Enable, Required] |Inquiry_Citizenship__c
26 | Fields -><br>Graduate College/Programs [Enable, Required, Format (Dropdown)] | Fields -><br>Graduate College/Programs [Enable, Required, College (Dropdown), Degree Types (Dropdown List), Programs (Multi-select)] | - | Capricorn: Same as fields above 8, 9, 12
27 | Fields -> <br>Name [Enable, Required] | Fields -> <br>Name [Enable, Required] | first_name<br>last_name
28 | Fields -> <br>Gender [Enable, Required] | Fields -> <br>Gender [Enable, Required] | Gender__c
29 | Fields -> <br>Email [Enable, Required] | Fields -> <br>Email [Enable, Required] | email
30 | Fields -><br>Address [Enable, Required] | Fields -><br>Address [Enable, Required] | StreetLine1__c<br>StreetLine2__c<br>MailingStreetLine3__c<br>MailingCity__c<br>MailingState__c<br>MailingZip__c<br>MailingCountry__c<br>MailingCounty__c
31 | Fields -> <br>Mobile Phone [Enable, Required] | Fields -> <br>Mobile Phone [Enable, Required] | mobile
32 | Fields -> <br>Home Phone [Enable, Required] | Fields -> <br>Home Phone [Enable, Required] | Home_Phone__c
33 | Fields -> <br>Text Message Opt-in [Enable, Required] | Fields -> <br>Text Me [Enable] | Receive_Texts__c | Auto Checked
34 | Fields -> <br>Birthday [Enable, Required] | Fields -> <br>Birthday [Enable, Required] | Birth_Month_Day__c
35 | Fields -> <br>How did you hear about us [Enable, Required] | Fields -> <br>How did you hear about us [Enable, Required] | How_did_you_hear_about_us__c
36 | Fields -> <br>Start Term Season [Enable, Required] | Fields -> <br>Start Term Season [Enable, Required] | Timeline__c
37 | Fields -> <br>Start Term Year [Enable, Required] | Fields -> <br>Start Term Year [Enable, Required] | Start_Term__c
38 | Fields -> <br>Employer [Enable, Required] | Fields -> <br>Employer [Enable, Required] | Company_Employer__c
39 | Fields -> <br>High School/College [Enable, Required] | Fields -> <br>High School/College [Enable, Required] | High_School__c<br>School_Organization_Code__c
40 | Fields -> <br>High School Graduation [Enable, Required] | Fields -> <br>High School Graduation [Enable, Required] | Expected_Graduation_Date__c
41 | Fields -> <br>Clubs [Enable, Required] | Fields -> <br>Clubs [Enable, Required] | Activity_Clubs__c
42 | Fields -> <br>Music [Enable, Required] | Fields -> <br>Music [Enable, Required] | Activity_Music__c
43 | Fields -> <br>Club Sports [Enable, Required] | Fields -> <br>Club Sports [Enable, Required] | Activity_Intramural_Sports__c
44 | Fields -> <br>Varsity Sports [Enable, Required] | Fields -> <br>Varsity Sports [Enable, Required] | Activity_Varsity_Sports__c
45 | Fields -> <br>Questions/Comments [Enable] | Fields -> <br>Questions/Comments [Enable] | I_Have_a_Question__c<br>description
46 | Fields -> <br>Mail Opt-in [Enable] | Fields -> <br>Email Me [Enable] | Send_Printed_Info__c | Capricon: Incorrect name (Email Me)
47 | Fields -> <br>ZNUR More Info [Enable] | Fields -> <br>Nursing Checkbox [Enable] | - | Temporary functionality

 *Required
 **Required for RFI v2 only