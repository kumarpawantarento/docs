# **Niramaya**


# **Platform Core PRD**

**Registries & Masters**

**Entity & Role Management**

September 2022


## Glossary/ Acronyms_


<table>
  <tr>
   <td>CB
   </td>
   <td>Capacity building 
   </td>
  </tr>
  <tr>
   <td>FRAC
   </td>
   <td>Framework of Roles, Activities and Competencies 
   </td>
  </tr>
  <tr>
   <td>iGOT
   </td>
   <td>Integrated Government Online Training 
   </td>
  </tr>
  <tr>
   <td>MCQ
   </td>
   <td>Multiple choice questions
   </td>
  </tr>
  <tr>
   <td>PIAA
   </td>
   <td>Proctored independent, authorised assessment
   </td>
  </tr>
  <tr>
   <td>PRD
   </td>
   <td>Product requirement document 
   </td>
  </tr>
  <tr>
   <td>QR
   </td>
   <td>Questions repository 
   </td>
  </tr>
  <tr>
   <td>QR_C
   </td>
   <td>Questions repository contributor
   </td>
  </tr>
  <tr>
   <td>QR_M
   </td>
   <td>Questions repository manager
   </td>
  </tr>
  <tr>
   <td>SOP
   </td>
   <td>Standard operating procedure 
   </td>
  </tr>
  <tr>
   <td>UPTSU
   </td>
   <td>Uttar Pradesh technical support unit
   </td>
  </tr>
  <tr>
   <td>UP SMF
   </td>
   <td>Uttar Pradesh State Medical Faculty
   </td>
  </tr>
  <tr>
   <td>NIC
   </td>
   <td>National Informatics Centre
   </td>
  </tr>
  <tr>
   <td>CASA
   </td>
   <td>Council Automation Smart Application
   </td>
  </tr>
</table>



## Platform Overview


1. Overall Objective and Users

The Uttar Pradesh State Medical Faculty (UPSMF) wants to set up an online platform to manage multiple functions regarding educational training, assessments, and job placement of allied healthcare professionals (AHPs) such as nurses, paramedical staff, lab technicians etc. The overall objective of the platform is to improve the quality of AHP medical education in the state, and eventually, improve the overall quality of healthcare delivery. 

Following entities will need to be onboarded onto the platform to achieve the platform’s objective:



1. Candidates - Students enrolled in GNM/ANM courses & professionals 
2. Institutes - All government & private medical institutes offering GNM/ANM courses
3. Workplace - Hospitals or healthcare centres where the graduating students are or can be employed
4. Regulatory Body - UP SMF, UP-TSU and other allied departments
5. QR_C
6. QR_M
7. PIAA Setter
8. PIAA Nodal
9. Medical & Non Medical Assessors (for institute verification and ratings)
1. Modules and Functionalities

Functionalities for the current roadmap of the platform have been identified, bucketed into 5 functional modules:



1. **Rating and Affiliation** for regular verification and grading of institutes and enable transparent decision-making for prospective students during the admission process
2. **Centralised Admissions** for prospective candidates looking to enrol in medical institutes for AHP courses (diploma / degree programs) to reduce the burden of institute-specific application process and remove discretion from the admissions process. 
3. **Competency based Assessments **of medical students and experienced professionals to enable tracking of role and function wise core competencies required by professionals to perform at their workplace
4. **Verifiable Resume** to enable ease of access and verification of a professional’s education and work history when applying for jobs in hospitals and health centres
5. **Aspirational Profession **module encompasses two key functionalities - (1) a job discovery and tracking platform to enable institute graduates to search for and apply for jobs, and (2) a learning management system (LMS) to enable access to online skilling courses to bridge the competency gaps identified as part of the competency based assessments


## Platform Architecture

A layered architecture is envisioned for building the platform with a **_Core Layer _**including the registries, credentials and masters as per defined standards and specifications. Above that is the **_Transaction Layer _**with transactional event data storage, intelligence engine, and communication engine. The **_Application Layer_** includes the five functional modules (described in the previous section) and platform UI. An open API layer connects the core with the application layer. 



<p id="gdcalert1" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image1.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert2">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image1.png "image_tooltip")


The platform will be built leveraging open-source [Sunbird](https://www.sunbird.org/) building blocks, which form the base of Ministry of Education’s (MoE) DIKSHA platform and Department of Personnel and Training’s (DoPT) human resource management platform, iGOT. Having Sunbird form the base of the UP HRH platform, will allow it to be contributed back to Sunbird repository for use by any other government entity in the country. 

The diagram below highlights the Sunbird building blocks that will be used to build different components of the platform. 



<p id="gdcalert2" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image2.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert3">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image2.png "image_tooltip")



## Platform Building Blocks

The following table summarises the different blocks that will form part of the platform and their status of readiness along with the work required to integrate them into the platform. 


<table>
  <tr>
   <td><strong>#</strong>
   </td>
   <td><strong>Layer</strong>
   </td>
   <td><strong>##</strong>
   </td>
   <td><strong>Block</strong>
   </td>
   <td><strong>Readiness</strong>
   </td>
   <td><strong>Work Required</strong>
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>Open Data Standards
   </td>
   <td>1.1
   </td>
   <td>Schemas
   </td>
   <td>To be Built
   </td>
   <td>- To be defined in a generic manner for DPG abstraction
   </td>
  </tr>
  <tr>
   <td rowspan="3" >2
   </td>
   <td rowspan="3" >Registries and Masters
   </td>
   <td>2.1
   </td>
   <td>Sunbird Lern
   </td>
   <td>Modification Needed
   </td>
   <td>- Enable OIDC / SSO based authentication
<p>
- Modify authorization instance to manage custom roles
   </td>
  </tr>
  <tr>
   <td>2.2
   </td>
   <td>Sunbird RC
   </td>
   <td>Modification Needed
   </td>
   <td>- To be deployed as per specified schema
<p>
- Brownfield approach to insert existing data
   </td>
  </tr>
  <tr>
   <td>2.3
   </td>
   <td>Sunbird Knowlg
   </td>
   <td>Ready for Use
   </td>
   <td>- Integrating functions, roles, activities and competencies (FRAC) framework
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td>Telemetry Events
   </td>
   <td>3.1
   </td>
   <td>Sunbird Obsrv
   </td>
   <td>Ready for Use
   </td>
   <td>- Designing telemetry objects
<p>
- Creating data products for dashboarding
   </td>
  </tr>
  <tr>
   <td>4
   </td>
   <td>Transactional Data
   </td>
   <td>4.1
   </td>
   <td><em>Backend</em>
   </td>
   <td>To be Built
   </td>
   <td>- Backend to be setup and managed
   </td>
  </tr>
  <tr>
   <td>4
   </td>
   <td>Intelligence
   </td>
   <td>4.1
   </td>
   <td>Drools
   </td>
   <td>Modification Needed
   </td>
   <td>- Needs to be implemented in UP context <em>(defining rules and triggers)</em>
<p>
- UI to be modified (Drools UI needs fixing)
<p>
- Needs to be integrated with Sunbird Obsrv
   </td>
  </tr>
  <tr>
   <td>5
   </td>
   <td>Communication
   </td>
   <td>5.1
   </td>
   <td>Sunbird UCI
   </td>
   <td>Modification Needed
   </td>
   <td>- Admin UI / functionalities will need to be added <em>(manage notifications)</em>
   </td>
  </tr>
  <tr>
   <td>6
   </td>
   <td>Unified Capacity Building APIs
   </td>
   <td>6.1
   </td>
   <td>Open APIs
   </td>
   <td>To be Built
   </td>
   <td>- Sunbird APIs can be leveraged <em>(will need to be selected and defined)</em>
<p>
- Some additional APIs will need to be written
   </td>
  </tr>
  <tr>
   <td>7
   </td>
   <td>Existing Systems
<p>
<em>(admissions, attendance, etc.)</em>
   </td>
   <td>7.1
   </td>
   <td>Data Transfer
   </td>
   <td>To be Built
   </td>
   <td>- Scaling for admissions / attendance data transfer (ongoing)
<p>
- Legacy data transfer for affiliation, exam results (one-time)
   </td>
  </tr>
  <tr>
   <td rowspan="2" >8
   </td>
   <td rowspan="2" >Reform Modules
<p>
<em>(accreditation, assessments)</em>
   </td>
   <td>8.1
   </td>
   <td>Sunbird inQuiry
   </td>
   <td>Ready for Use
   </td>
   <td>- Building a mobile app / container for deploying forms
   </td>
  </tr>
  <tr>
   <td>8.2
   </td>
   <td>Sunbird CoKreat
   </td>
   <td>Ready for Use
   </td>
   <td>- Adding question types: DocInput and DatePicker
<p>
- Creating workflows out of data-collection forms
   </td>
  </tr>
  <tr>
   <td>9
   </td>
   <td>Reform Modules
<p>
<em>(verifiable resume)</em>
   </td>
   <td>9.1
   </td>
   <td>Sunbird RC
   </td>
   <td>Modification Needed
   </td>
   <td>- <strong><em>Verifiable Resume</em></strong>: To be implemented in Sunbird RC
   </td>
  </tr>
  <tr>
   <td rowspan="3" >10
   </td>
   <td rowspan="3" >Reform Modules
<p>
<em>(aspirational profession)</em>
   </td>
   <td>10.1
   </td>
   <td>Sunbird RC
   </td>
   <td>Ready for Use
   </td>
   <td>- <strong><em>Jobs</em></strong>: Data to be pushed back to Sunbird RC
   </td>
  </tr>
  <tr>
   <td>10.2
   </td>
   <td>Sunbird Lern
   </td>
   <td>Modification Needed
   </td>
   <td>- <strong><em>LMS</em></strong>: Content marketplace to be setup, courses searchable by FRAC elements
   </td>
  </tr>
  <tr>
   <td>10.3
   </td>
   <td>Sunbird Knowlg
   </td>
   <td>Modification Needed
   </td>
   <td>- <strong><em>Jobs</em></strong>: Needs to be contextualised for job discovery & lifecycle management
   </td>
  </tr>
  <tr>
   <td>11
   </td>
   <td>Platform Interface
   </td>
   <td>11.1
   </td>
   <td>Sunbird Ed
   </td>
   <td>Modification Needed
   </td>
   <td>- Frontend to be developed contextualised for UP leveraging SunbirdEd UI framework
   </td>
  </tr>
</table>



## User Registries


1. Registry Entities

All user entities will be registry compliant to ensure privacy of users’ personal information. Registries allow each user to be in control of their data and can customise which applications (including the frontend of the platform) can access their personal details. A registry-compliant construct ensures that registry specific functionalities can be activated for all modules of the platform. 

 

Sunbird RC will form the base that houses all user entity information to enable secure and privacy-enabled user management. 

Currently, a UPSMF portal - CASA, ([https://upsmfac.org/](https://upsmfac.org/)) is being used for several functionalities, additional to the modules mentioned in the previous section. The [database](https://drive.google.com/file/d/19NDRjx3mmn9MO3S70dhoNwQwCPCLIBac/view?usp=sharing) is powered by MS SQL which houses details of these entities. 

Each user on the platform will be part of a registry and will have a unique process of getting onboarded (access & authentication) to the platform. Different workflows have been defined to enable this onboarding process.

The following [approach](https://app.diagrams.net/#G12h9tK-OHANrqlMFefe2mpg0cVStRokC6) will be followed to ensure a **_single source of truth _**for1, 2,entity information and **_registry compliance _**for the platform overall. 


<table>
  <tr>
   <td><strong>#</strong>
   </td>
   <td><strong>Scenario</strong>
   </td>
   <td><strong>Approach</strong>
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>Functionalities on CASA being used in parallel to the new UP HRH platform
   </td>
   <td>- CASA to remain as the single source of truth for core entities - students, institutes and faculty
<p>
- A copy of these entities to be created as registries on Sunbird RC, with the ability to update entries as changes occur in the CASA databases
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>CASA functionalities fully migrated to UP HRH platform and the old platform is sunset
   </td>
   <td>- Set up registries to function as the sole source of truth with full CRUD capabilities (no parallel database maintained on CASA)
   </td>
  </tr>
</table>


Below are the key registry entities with a link to their proposed schema, functions & onboarding workflow:

 


<table>
  <tr>
   <td><strong>#</strong>
   </td>
   <td><strong>Entity</strong>
   </td>
   <td><strong><a href="https://drive.google.com/file/d/19NDRjx3mmn9MO3S70dhoNwQwCPCLIBac/view?usp=sharing">Current DB</a><span style="text-decoration:underline;"> (CASA)</span></strong>
   </td>
   <td><strong>Proposed Schema</strong>
   </td>
   <td><strong>Functions to be Performed</strong>
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td><strong>Regulatory Body</strong>
   </td>
   <td>Currently does not exist
   </td>
   <td>TBD
   </td>
   <td><strong>Create: </strong>
<p>
- Entities in the Assessments Module : QR_C, QR_M, PIAA Setter, PIAA Nodal
<p>
- Issue certificates to candidates who have successfully passed assessments
<p>
<strong>Read:</strong>
<p>
- State/District level analytics
<p>
- Telemetry events as defined
<p>
<strong>Update:</strong>
<p>
- Entity - Role Mapping - This control will be with the regulatory body
<p>
<strong>Delete:</strong>
<p>
- Cannot delete but can mark an entity - role inactive
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td><strong>Candidate <em>(Part of User DB)</em></strong>
   </td>
   <td><em>Master_Student</em>
<p>
<em>Details</em>
   </td>
   <td><a href="https://docs.google.com/spreadsheets/d/13i7V7Az2D9mg2_se0j8QzQPXEKuYMpO1ARGMKH0ur6o/edit#gid=332080994">Link</a>
   </td>
   <td><strong>Create</strong>: new entity can come from two sources:
<p>
- students admitted to courses on CASA/ NIC’s admissions portal (once made)
<p>
- professionals self-register as part of the jobs discovery module (R5)
<p>
 \
<strong>Read</strong>: Allow admin (state dept.) to view all details through search or filter options (attributes indicated in schema)
<p>
<strong>Update</strong>: Only the admin is able to update certain attributes in the schema. These are:
<p>
- residential address (district, block etc.)
<p>
- contact details: email, mobile number
<p>
<strong>Delete</strong>: Cannot delete - only assign ‘inactive’  status (e.g., dropout student, terminated professional)
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td><strong>Institute</strong>
   </td>
   <td><em>Master_College</em>
<p>
<em>Registration_</em>
<p>
<em>Dental_Medical</em>
   </td>
   <td><a href="https://docs.google.com/spreadsheets/d/13i7V7Az2D9mg2_se0j8QzQPXEKuYMpO1ARGMKH0ur6o/edit#gid=1301957135">Link</a>
   </td>
   <td><strong>Create</strong>: The information of existing institutes will be fetched from CASA. 
<p>
<strong>Read</strong>: Allow admin (state dept.) to view all details through search or filter options (attributes indicated in schema)
<p>
<strong>Update</strong>: Only the admin is able to update certain attributes in the schema. These are:
<p>
- contact details: email, mobile number
<p>
- Institute head details
<p>
- Location details
<p>
<strong>Delete</strong>: Cannot delete - only assign ‘closed’ status 
   </td>
  </tr>
  <tr>
   <td>4
   </td>
   <td><strong>Faculty <em>(Part of User DB)</em></strong>
   </td>
   <td>- Details of institute faculty exist in table <em>Master_Institute</em>
<p>
<em>Tutor</em>
   </td>
   <td><a href="https://docs.google.com/spreadsheets/d/13i7V7Az2D9mg2_se0j8QzQPXEKuYMpO1ARGMKH0ur6o/edit#gid=1283869895">Link</a>
   </td>
   <td><strong>Create</strong>: No creation allowed, data pulled in fromCASA
<p>
<strong>Read</strong>: Allow admin (state dept.) to view all details through search or filter options (attributes indicated in schema)
<p>
<strong>Update</strong>: Only the admin is able to update certain attributes in the schema. These are:
<p>
- contact details: email, mobile number
<p>
- Location details
<p>
<strong>Delete</strong>: Cannot delete - only assign ‘inactive’ status
   </td>
  </tr>
  <tr>
   <td>5
   </td>
   <td><strong>Workplace</strong>
   </td>
   <td>Records exist - but not complete
   </td>
   <td><a href="https://docs.google.com/spreadsheets/d/13i7V7Az2D9mg2_se0j8QzQPXEKuYMpO1ARGMKH0ur6o/edit#gid=1414995340">Link</a>
   </td>
   <td><strong>Create</strong>: Workplaces can <strong><em>self-register</em></strong> to provide job listings (R5), update employee work history and access verifiable resumes (R4)
<p>
<strong>Read</strong>: Allow admin (state dept.) to view all details through search or filter options (attributes indicated in schema)
<p>
<strong>Update</strong>: Only the admin is able to update certain attributes in the schema. These are:
<p>
- contact details: email, mobile number
<p>
- Location details
<p>
<strong>Delete</strong>: Cannot delete - only assign ‘inactive’ status
   </td>
  </tr>
  <tr>
   <td>6
   </td>
   <td><strong>QR_C</strong>
   </td>
   <td>Currently does not exist
   </td>
   <td>TBD
   </td>
   <td><strong>Create: </strong>
<p>
- Questions in the Assessments module
<p>
- Bulk upload questions through a csv
<p>
<strong>Read</strong>:
<p>
- Questions that he has created
<p>
- Edits made by QR_M
<p>
- Summary of submitted, approved & rejected questions
<p>
<strong>Update</strong>: 
<p>
- Questions based on review suggestions provided by QR_M
<p>
<strong>Delete</strong>: 
<p>
- Self created questions before submitting them for review
   </td>
  </tr>
  <tr>
   <td>7
   </td>
   <td><strong>QR_M</strong>
   </td>
   <td>Currently does not exist 
   </td>
   <td>TBD
   </td>
   <td><strong>Create: </strong>
<p>
- Does not create anything
<p>
<strong>Read</strong>:
<p>
- Questions that QR_C  has created
<p>
- Edits made by QR_C
<p>
- Summary of submitted, approved & rejected questions
<p>
<strong>Update</strong>: 
<p>
- Edit questions submitted by QR_C
<p>
- Reject questions submitted by QR_C
<p>
- Adds comments for rejected questions
<p>
<strong>Delete</strong>: 
<p>
- Cannot delete - can only reject 
   </td>
  </tr>
  <tr>
   <td>8
   </td>
   <td><strong>PIAA Setter</strong>
   </td>
   <td>Currently does not exist
   </td>
   <td>TBD
   </td>
   <td><strong>Create: </strong>
<p>
- Create blueprint of assessments by defining the competency, competency levels to be tested
<p>
<strong>Read</strong>:
<p>
- View the assessments that have been created
<p>
<strong>Update</strong>: 
<p>
- Edit the blueprint of assessments
<p>
<strong>Delete</strong>: 
<p>
- Cannot delete
   </td>
  </tr>
  <tr>
   <td>9
   </td>
   <td><strong>PIAA Nodal</strong>
   </td>
   <td>Currently does not exist
   </td>
   <td>TBD
   </td>
   <td><strong>Create: </strong>
<p>
- Begin the assessment for a candidate
<p>
- Certificates for the candidates
<p>
<strong>Read</strong>:
<p>
- View the available assessments
<p>
<strong>Update</strong>: 
<p>
- Cannot edit
<p>
<strong>Delete</strong>: 
<p>
- Cannot delete
   </td>
  </tr>
  <tr>
   <td>10
   </td>
   <td><strong>Medical Assessor</strong>
   </td>
   <td>Currently does not exist
   </td>
   <td>TBD
   </td>
   <td rowspan="2" ><strong>Update:</strong>
<p>
- Can view and administer assessments
<p>
- Can enter student performance in the assessment
   </td>
  </tr>
  <tr>
   <td>11
   </td>
   <td><strong>Non Medical Assessor</strong>
   </td>
   <td>Currently does not exist
   </td>
   <td>TBD
   </td>
  </tr>
</table>



## Entity Role Management 

An ** entity **is any individual or organisation that will be using the platform.

**Permission** is an action that an entity will be entitled to perform.

**Role **is a group of permissions bunched together. **Roles **can be global or module specific.

An **entity **will be mapped to one or more **roles **and each role will have a set of one or more **permissions **within it.

This list of permissions, roles & their mapping to entities only covers the Assessments & Ratings modules currently and will expand as we scope out more modules.

**Dictionary of roles & permissions:**

 


<table>
  <tr>
   <td><strong>Roles</strong>
   </td>
   <td><strong>Permission</strong>
   </td>
   <td><strong>Module</strong>
   </td>
  </tr>
  <tr>
   <td>Super Admin
   </td>
   <td>1. Can view state level analytics
<p>
2. Can view telemetry of the platform
<p>
3. Can set/reset role level permissions at a module level
<p>
4. View all transactional data
<p>
5. Perform entity - role management
<p>
6. Can issue certificates to candidates undertaking assessments
   </td>
   <td>Across modules
   </td>
  </tr>
  <tr>
   <td>Admin_E Cred
   </td>
   <td>1. Can enter work experience / educational details for a candidate
   </td>
   <td>E credentials
   </td>
  </tr>
  <tr>
   <td>Admin_Assessments
   </td>
   <td>1. Can issue certificates to candidates undertaking assessments
   </td>
   <td>Assessments
   </td>
  </tr>
  <tr>
   <td>Admin_LMS
   </td>
   <td>1. Can view courses curated by content providers
<p>
2. Can review course and approve for publishing
<p>
3. Can return / reject course in case of improper tagging / content
   </td>
   <td>Aspirational Profession (LMS)
   </td>
  </tr>
  <tr>
   <td>Admin_Ratings
   </td>
   <td>1. Can create data entry forms
<p>
2. Can assign data entry forms
<p>
3. Can view / edit data entry forms  
<p>
4. Can schedule on-ground visits
<p>
5. Can reject / request for update of forms
   </td>
   <td>Ratings & Affiliation
   </td>
  </tr>
  <tr>
   <td>Repository Contributor
   </td>
   <td>1. Can create new question-sets for assessment
<p>
2. Can bulk upload new questions in laid out format
<p>
3. View reason of rejection if a QR_M rejects a question
<p>
4. Tag a question to competency level
   </td>
   <td rowspan="5" >Assessments
   </td>
  </tr>
  <tr>
   <td>Repository Manager
   </td>
   <td>1. Can view questions submitted by QR_C
<p>
2. Can accept or reject a question
<p>
3. Can write a reason for rejection for a question
<p>
4. Can edit mapping of a question to a competency
   </td>
  </tr>
  <tr>
   <td>Question Paper Setter
   </td>
   <td>1. Can set the blueprint of assessment
<p>
2. Can compose assessments packages from questions in directory
   </td>
  </tr>
  <tr>
   <td>Test centre Nodal
   </td>
   <td>1. Can start an assessment for a candidate
<p>
2. Can pause/ stop the assessment of a candidate
   </td>
  </tr>
  <tr>
   <td>Test Taker
   </td>
   <td>1. Can start a self assessment by entering defined parameters (Eg. roll number/ DOB)
<p>
2. Can view questions in assigned set
<p>
3. Can view the correct answers to assessments
<p>
4. Can view the marks awarded for each assessment
<p>
5. Can view/Download a report card for self assessment & a certificate for proctored assessment at the PIAA centre
<p>
6. Can report discrepancy in marks
   </td>
  </tr>
  <tr>
   <td>E cred verifier
   </td>
   <td>1. Can enter candidates’ workplace & institute details
<p>
2. Can view details contained in the verified resume of a candidate
   </td>
   <td rowspan="3" >E Credentials
   </td>
  </tr>
  <tr>
   <td>Job curator
   </td>
   <td>1. Can post job vacancies on the portal
<p>
2. Can view candidate profiles and notify interested candidates
   </td>
  </tr>
  <tr>
   <td>Placement verifier
   </td>
   <td>1. Can provide details of batch placement 
   </td>
  </tr>
  <tr>
   <td>Job Seeker
   </td>
   <td>1. Can search for posted jobs
<p>
2. Can apply to posted jobs
<p>
3. Can report status of successful employment
   </td>
   <td rowspan="3" >Aspirational Profession (LMS)
   </td>
  </tr>
  <tr>
   <td>Content Provider
   </td>
   <td>1. Can upload content pieces and organise into courses
<p>
2. Can tag courses to elements of the FRAC framework
   </td>
  </tr>
  <tr>
   <td>Learner
   </td>
   <td>1. Can register on the platform and add their Position (FRAC)
<p>
2. Can attempt a self-assessment to identify weak competencies
<p>
3. Can view recommended courses (as per identified competencies)
<p>
4. Can save courses to attempt later
<p>
5. Can view content under a course (video, text)
<p>
6. Can attempt assessment post course completion
<p>
7. Can receive and save a badge to profile on course completion
   </td>
  </tr>
</table>


**Entity - Role Mapping at a Module Level**


<table>
  <tr>
   <td><strong>Roles</strong>
   </td>
   <td><strong>Entity</strong>
   </td>
   <td><strong>Module</strong>
   </td>
  </tr>
  <tr>
   <td>Super Admin
   </td>
   <td>Regulatory body
   </td>
   <td>Across Modules
   </td>
  </tr>
  <tr>
   <td>Admin_E Cred
   </td>
   <td>Regulatory body
   </td>
   <td>E Credentials
   </td>
  </tr>
  <tr>
   <td>Admin_Assessments
   </td>
   <td>Regulatory body
   </td>
   <td>Assessments
   </td>
  </tr>
  <tr>
   <td>Admin_LMS
   </td>
   <td>Regulatory body
   </td>
   <td>Aspiration Profession 
   </td>
  </tr>
  <tr>
   <td>Admin_Ratings
   </td>
   <td>Regulatory body
   </td>
   <td>Ratings & Affiliation
   </td>
  </tr>
  <tr>
   <td>Repository Contributor
   </td>
   <td>QR_C
   </td>
   <td rowspan="5" >Assessments
   </td>
  </tr>
  <tr>
   <td>Repository Manager
   </td>
   <td>QR_M
   </td>
  </tr>
  <tr>
   <td>Question Paper Setter
   </td>
   <td>PIAA Setter
   </td>
  </tr>
  <tr>
   <td>Test centre Nodal
   </td>
   <td>PIAA Nodal
   </td>
  </tr>
  <tr>
   <td>Test Taker
   </td>
   <td>Candidate
   </td>
  </tr>
  <tr>
   <td rowspan="2" >E Cred Verifier
   </td>
   <td>Institute
   </td>
   <td rowspan="4" >E credentials
   </td>
  </tr>
  <tr>
   <td>Workplace
   </td>
  </tr>
  <tr>
   <td>Job Curator
   </td>
   <td>Workplace
   </td>
  </tr>
  <tr>
   <td>Placement Verifier
   </td>
   <td>Institute
   </td>
  </tr>
  <tr>
   <td>Job Seeker
   </td>
   <td>Candidate
   </td>
   <td rowspan="3" >Aspirational Profession (LMS)
   </td>
  </tr>
  <tr>
   <td>Content Provider
   </td>
   <td>Regulatory Body
   </td>
  </tr>
  <tr>
   <td>Learner
   </td>
   <td>Candidate
   </td>
  </tr>
</table>


The focus in the Core Module for Entity - Role - Permission mapping is on the Assessments module that is in scope for Q1. The other mappings will get fleshed out more when the PRDs and workflows for the other modules are taken up.


## Masters

Masters of different types will need to be established to enable consistency in attributes being stored across tables in the database. The table below lists the masters to be created. 


<table>
  <tr>
   <td><strong>Bucket</strong>
   </td>
   <td><strong>#</strong>
   </td>
   <td><strong>Master</strong>
   </td>
   <td><strong>Link</strong>
   </td>
  </tr>
  <tr>
   <td rowspan="5" ><strong>1. Location Masters</strong>
   </td>
   <td>1.1
   </td>
   <td>State
   </td>
   <td><a href="https://docs.google.com/spreadsheets/d/1l1mnePdfrSRlM5CINdQxrU0AGxYZJ5GEwxPlkAHLVKI/edit#gid=1192863714">link</a>
   </td>
  </tr>
  <tr>
   <td>1.2
   </td>
   <td>District
   </td>
   <td><a href="https://docs.google.com/spreadsheets/d/1l1mnePdfrSRlM5CINdQxrU0AGxYZJ5GEwxPlkAHLVKI/edit#gid=1147012189">link</a>
   </td>
  </tr>
  <tr>
   <td>1.3
   </td>
   <td>Block
   </td>
   <td><a href="https://docs.google.com/spreadsheets/d/1l1mnePdfrSRlM5CINdQxrU0AGxYZJ5GEwxPlkAHLVKI/edit#gid=1381024779">link</a>
   </td>
  </tr>
  <tr>
   <td>1.4
   </td>
   <td>Constituency
   </td>
   <td><a href="https://docs.google.com/spreadsheets/d/1l1mnePdfrSRlM5CINdQxrU0AGxYZJ5GEwxPlkAHLVKI/edit#gid=1431403349">link</a>
   </td>
  </tr>
  <tr>
   <td>1.5
   </td>
   <td>Village
   </td>
   <td><a href="https://docs.google.com/spreadsheets/d/1l1mnePdfrSRlM5CINdQxrU0AGxYZJ5GEwxPlkAHLVKI/edit#gid=126826487">link</a>
   </td>
  </tr>
  <tr>
   <td rowspan="4" ><strong>2. Competency Masters</strong>
<p>
<em>(see subsequent section)</em>
   </td>
   <td>2.1
   </td>
   <td>Positions
   </td>
   <td>-
   </td>
  </tr>
  <tr>
   <td>2.2
   </td>
   <td>Roles
   </td>
   <td>-
   </td>
  </tr>
  <tr>
   <td>2.3
   </td>
   <td>Activities
   </td>
   <td>-
   </td>
  </tr>
  <tr>
   <td>2.4
   </td>
   <td>Competencies
   </td>
   <td>-
   </td>
  </tr>
  <tr>
   <td rowspan="3" ><strong>3. Course Masters</strong>
   </td>
   <td>3.1
   </td>
   <td>Regulator
   </td>
   <td>TBD
   </td>
  </tr>
  <tr>
   <td>3.2
   </td>
   <td>Session
   </td>
   <td>TBD
   </td>
  </tr>
  <tr>
   <td>3.3
   </td>
   <td>Course
   </td>
   <td>TBD
   </td>
  </tr>
</table>



## Competency Management



1. Understanding FRAC[^1] framework
Professional competence of each AHP student / faculty / professional will be tracked against a FRAC framework (incorporated in DOPT’s iGOT platform) which stands for functions, roles, activities and competencies. 

**_Positions_** or functions refer to the job role of an individual, e.g., for a lecturer of the nursing degree course, the function is that of a _‘nursing faculty’. _The function of a student hired to administer anaesthesia in a district hospital, the function is that of an an _‘anaesthesia nurse’_

**_Roles_** refer to bucketing, abstraction of activities that are to be performed by the individual in a particular position. E.g., a general nurse midwife (GNM) will have the following roles - _manage normal delivery, caring for normal newborn_ etc.  

**_Activities_** offer a higher level of detail and specificity over roles pertaining to a specific position. E.g., the activities for a GNM under the role ‘manage normal delivery’ can be - _describe all markers of a normal delivery, describe all steps under normal delivery, perform all steps for normal delivery_ etc. 

**Competencies **refer to the specific behavioural, domain and functional understanding / competence that the individual must possess to be able to successfully perform the activities mentioned above, Examples of competencies for a GNM include - _understands components of normal delivery and second stage of labour_, _understands complications in PW and it’s management,_ etc. Each competency will have 3 to 5 levels which indicate the level of difficulty or proficiency for that competency. 



2. Rules for Competency Management



<p id="gdcalert3" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image3.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert4">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image3.png "image_tooltip")




* Each user (candidate / faculty) will get mapped to a single position i.e., _no user will be mapped to 2 or more positions_
* Each position will map to a set of roles
* A role can be mapped to one or more positions i.e., _mapping of roles to positions is not in a strict hierarchy_
* Roles are essentially logical aggregation / bucketing of activities
* An activity can map to more than 1 role - _activity to role mapping is not unique_
* An activity can map to two roles from either the same positions or two roles from different positions
* Every competency has 3 to 5 levels (L1, L2 and so on)
* Levels of a competency are progressive - _i.e., L2 is more complex / difficult than L1, if a candidate is at CXL3, they will be proficient in CXL2 and CXL1_
* Competency levels (CXLX) and not competencies (CX) map to activities
* Each activity should map to at least one competency level (CXLX)
* Every competency level should map to at least one activity
* Levels of the same competency can map to different activities (e.g., C1L1 to A1 and C1L2 to A2)
* One competency level (CXLX) can map to two or more activities (same or different role, same or different position)
3. Schemas of Competency Masters

The following table lists down the masters which will store all competency data for use in several modules of the platform. 


<table>
  <tr>
   <td><strong>#</strong>
   </td>
   <td><strong>Master</strong>
   </td>
   <td><strong>Description</strong>
   </td>
   <td><strong>Link</strong>
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>Position
   </td>
   <td><strong><em>Pre-service</em></strong>: course (e.g., ANM / GNM)
<p>
<strong><em>Post-service</em></strong>: specific job role
   </td>
   <td><a href="https://docs.google.com/spreadsheets/d/1l1mnePdfrSRlM5CINdQxrU0AGxYZJ5GEwxPlkAHLVKI/edit#gid=1580063997">link</a>
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>Role
   </td>
   <td><strong><em>Pre-service</em></strong>: specific subjects under the course
<p>
<strong><em>Post-service</em></strong>: bucketing of major activities covered under the function
   </td>
   <td><a href="https://docs.google.com/spreadsheets/d/1l1mnePdfrSRlM5CINdQxrU0AGxYZJ5GEwxPlkAHLVKI/edit#gid=587966324">link</a>
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td>Activity
   </td>
   <td>Learning outcomes or specific activities to be covered under a position
   </td>
   <td><a href="https://docs.google.com/spreadsheets/d/1l1mnePdfrSRlM5CINdQxrU0AGxYZJ5GEwxPlkAHLVKI/edit#gid=1752212325">link</a>
   </td>
  </tr>
  <tr>
   <td>4
   </td>
   <td>Competency
   </td>
   <td>Covers a specific competency / demonstrable outcome (pre or post service). Each competency is tagged to a competency type and competency area. Competencies also have 3-5 levels which denote difficulty of that competency
   </td>
   <td><a href="https://docs.google.com/spreadsheets/d/1l1mnePdfrSRlM5CINdQxrU0AGxYZJ5GEwxPlkAHLVKI/edit#gid=1998702533">link</a>
   </td>
  </tr>
</table>



## Milestone Phasing


<table>
  <tr>
   <td>#
   </td>
   <td>Category
   </td>
   <td>Phase
   </td>
   <td>Milestones
   </td>
   <td>Sep
   </td>
   <td>Oct
   </td>
   <td>Nov
   </td>
  </tr>
  <tr>
   <td rowspan="7" >1
   </td>
   <td rowspan="7" ><strong>Platform Core</strong>
   </td>
   <td rowspan="3" >Requirements
   </td>
   <td>Define Core PRD
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Define schema of registries and databases
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Define competency framework
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td rowspan="4" >Setup
   </td>
   <td>Setup Sunbird Ed (all building blocks)
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Setup registries on Sunbird RC
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Setup databases for common masters (location etc.)
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Sunbird Knowlg configured for tiered competency framework
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
</table>


In the Q1 scope of assessments, the competency masters will be uploaded in the backend by the engineering team.


<!-- Footnotes themselves at the bottom. -->
## Notes

[^1]:

     FRAC framework was developed as part of DOPT’s iGoT framework - [link](https://indianrailways.gov.in/railwayboard/uploads/directorate/mgt_ser/2021/Ann-A3.pdf)
