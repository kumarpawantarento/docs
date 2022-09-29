# **Assessments Module**

**V1.0**

Last Updated: 9th Sept 2022


### Glossary/ Acronyms


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
</table>




### 1. **Overall Purpose and Vision**

    The scope of the document is to define the purpose and functionality of the knowledge based assessment tool for assessing the competency proficiency levels of individual candidates, specifically in knowledge. It lays out detailed users, functional requirements with flows. It also defines the desired outputs of each functionality. The document also details out how the self practice assessment and proctored assessment modules will interact and communicate with other digital systems. The assessment is part of PIAA (proctored, independent, authorised assessment) which is used for identifying the competency proficiency levels of candidates for all competencies that the participants require. 


    The document is designed by the UPTSU team for technical partners, and vendors to clearly understand the requirements of the knowledge based assessment tool. 


### 2. **Project scope **

    The module will enable creation and conduction of written and objective competency linked assessments in two setups:

1. <span style="text-decoration:underline;">self practice assessment</span> for the candidate to practice and gauge whether they have attained the competencies mapped to their roles or position
2. Proactored, independent, authorised assessment (PIAA) in a designated PIAA centre to maintain credible competency attainment records for candidates and to provide inputs to the verifiable resume / competency passbook of each individual

_Assumptions and dependencies_

1. A competency directory, mapped with each position, role and activity is ready to refer for Assessment composition
2. Databases like list of PIAA centres ; PIAA setter; mapping of assessment process owners  and other system users is available when setup starts
3. **Overview of use case and interface requirements**

The MCQ based assessment tool will have 6 roles namely; 


<table>
  <tr>
   <td><strong>#</strong>
   </td>
   <td><strong>Entity</strong>
   </td>
   <td><strong>Roles</strong>
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>Faculty 
   </td>
   <td>Question repository contributor (QR_C)
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>UPTSU
   </td>
   <td>Question repository manager (QR_M)
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td>PIAA setter
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>4
   </td>
   <td>PIAA nodal
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>5
   </td>
   <td>Candidate
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>6
   </td>
   <td>Admin
   </td>
   <td>
   </td>
  </tr>
</table>



### **Noun verbs**

1. Questions - Create (QR C), Review (QR M)
2. Blueprint for Question paper - Create (PIAA setter)
3. PIAA papers - Create (PIAA setter), Review (PIAA Nodal)
4. Practice papers - Create (candidate), Submit (candidate)
5. PIAA paper submissions - Create (candidate), Update (PIAA Nodal), Review (?), View (?)
6. Verifiable credentials - Create (?), Issue (?), View (candidate)

### **Use case overview**

Based on the requirements, some of the use cases for users are listed below. 

<table>
  <tr>
   <td><strong>S.No</strong>
   </td>
   <td><strong>Use Case</strong>
   </td>
   <td><strong>Description</strong>
   </td>
   <td><strong>User Role</strong>
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>Proposes competency wise questions to questions repository
   </td>
   <td>As a QR contributor, I am able to record and propose various types of questions in the questions repository linked to competency levels.
   </td>
   <td>Question Repository Contributor
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>Review questions: Edit, approve or reject questions
   </td>
   <td>As a QR manager, I can view proposed questions, make edits and reject or accept the questions proposed. 
<p>
I can also edit the mapping of the questions to the mapped competency level. 
   </td>
   <td>Question Repository Manager
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td>Manages and maintains question repository
   </td>
   <td>As a QR manager, I am able to approve previously rejected questions or disapprove previously approved questions
   </td>
   <td>Question Repository Manager
   </td>
  </tr>
  <tr>
   <td>4
   </td>
   <td>Compose assessment blueprints for various roles and cadres in public health
   </td>
   <td>As a PIAA setter, I am able to select relevant competencies from the directory and set the assessments blueprint for various roles.
   </td>
   <td>PIAA Setter
   </td>
  </tr>
  <tr>
   <td>5
   </td>
   <td>Initiate assessment session for candidates and facilitate
   </td>
   <td>As a PIAA Nodal, I am able to set up assessment blueprints on systems for different candidates and begin / pause / stop assessments for them
   </td>
   <td>PIAA Nodal
   </td>
  </tr>
  <tr>
   <td>6
   </td>
   <td>Take a practice self practice assessment
   </td>
   <td>As a candidate, I am able to select any of the available question papers from the directory and conduct a self practice assessment and submit my responses in a timed manner. I am also able to get the results and feedback.
   </td>
   <td>candidate
   </td>
  </tr>
  <tr>
   <td>7
   </td>
   <td>View and download certificate 
   </td>
   <td>As a candidate, I am able to view and download certificates for the PIAA assessments I have taken so far
   </td>
   <td>candidate
   </td>
  </tr>
  <tr>
   <td>8
   </td>
   <td>Review assessments, approving / aborting assessment blueprints for the evaluation of results
   </td>
   <td>As an admin, I am able to review assessment sessions and approve or abort them to decide if they can be sent for evaluation or not
   </td>
   <td>Admin
   </td>
  </tr>
  <tr>
   <td>9
   </td>
   <td>View results and issue certificates to assessment takers
   </td>
   <td>As an admin, I am able to view results and issue certificates to the assessment takers
   </td>
   <td>Admin
   </td>
  </tr>
</table>



### **Versioning**


<table>
  <tr>
   <td><strong>Use case #</strong>
   </td>
   <td><strong>Description</strong>
   </td>
   <td><strong>Version</strong>
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>
<h3>Proposes competency wise questions to questions repository</h3>

Question type: Single select 
<p>
Question type: Multiple choice questions – Single/Multi MCQ type , One-word answers, Fill in the blanks, Short/long answers, Case study-based questions, Match the following
   </td>
   <td>v1
<p>
v2
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>
<h3>Review questions: Edit, Approve or Reject questions</h3>


   </td>
   <td>v1
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td>
<h3>Manages and maintains questions repository</h3>


   </td>
   <td>v1
   </td>
  </tr>
  <tr>
   <td>4
   </td>
   <td>
<h3>Compose assessment blueprints for various roles and cadres in public health</h3>

# of questions by competency levels 
<p>
# of questions by question type
   </td>
   <td>v1
<p>
v2
   </td>
  </tr>
  <tr>
   <td>5
   </td>
   <td>
<h3>Initiate assessment session for candidates and facilitate</h3>

Individual - PIAA nodal opens the assessment blueprint on a desktop computer and maps it to a candidate and starts the assessment 
<p>
Batch start
   </td>
   <td>v1
<p>
v2
   </td>
  </tr>
  <tr>
   <td>6
   </td>
   <td>
<h3>Take a self practice assessment</h3>

Untimed
<p>
Timed
   </td>
   <td>v1
<p>
v2
   </td>
  </tr>
  <tr>
   <td>7
   </td>
   <td>
<h3>View and download certificate</h3>


   </td>
   <td>v1
   </td>
  </tr>
  <tr>
   <td>8
   </td>
   <td>
<h3>Review assessments, approving / aborting assessment blueprints for the evaluation of results</h3>


   </td>
   <td>v1
   </td>
  </tr>
  <tr>
   <td>9
   </td>
   <td>
<h3>View results and issue certificates to assessment takers</h3>

PDF generator enabled certificate
<p>
Verifiable credentials
   </td>
   <td>v1
<p>
v2
   </td>
  </tr>
</table>



#### **Use case details**

#### Use case 1: Proposes competency wise questions to questions repository

1. QR contributors logs in with Unique user id and password
2. The home page will include two tabs namely ‘Create questions’ and ‘View questions’
3. The home page will display the following metrics
1. Number of questions created
2. Number of questions approved
3. Number of questions rejected
4. Number of questions pending review
4. When QR contributors click on ‘Create questions’, a dropdown of position and competency directory will be shown to select competency level (Position-Competency-Competency level). Once the competency level is selected, a window to record the question body, options and correct answer input will be provided. Question body may contain pure text, text and image or only image also. This can be the method for adding one question at a time. For the v1, only single-select MCQ type questions can be added. 
5. For a set of questions, a QR contributor is able to upload a set of questions in the repository in a speciﬁc format (csv) deﬁned by system admin by clicking on ‘Upload questions’ CTA in the ‘Create questions’ page
6. The QR_C can see the questions created in the ‘View questions’ tab
7. On adding questions (single or bulk upload), the QR_C gets options to either ‘Save’ or ‘Submit for Review’
8. The questions will be displayed along with any one of the following status
1. Approved
2. Approved with edits
3. Sent for review
4. Pending review
5. Rejected
9. The questions will also have CTAs to send for review, edit or delete the questions
10. The user will be able to edit and delete only those questions which have their status as “Pending review”
11. The QR_C cannot resubmit questions which have been rejected
12. QR_C can click on the ‘Send for review’ CTA against a question to send it for review. QR_C can also multi-select the questions and submit them for review.

**Types of Assessment questions (v2) :**

The written assessments for competencies may use various types of items. A pop-up will be displayed while the QR_C is creating questions where they can select the type of questions. These types of items in the assessment item bank can be:


1. Multiple choice questions – Single/Multi select: using text/ images
2. One-word answers, Fill in the blanks
3. Short/long answers
4. Case study-based questions
5. Match the following

The selection of a particular/ mix of question types for an assessment blueprint is a choice of the PIAA setter. The question repository will have all types of questions mapped to each competency and competency level. For the ﬁrst two types of questions ( MCQs and one word/ ﬁll in the blanks) the mapping to a particular competency and competency level will be 1:1. For the others, it might be 1:many


#### Use case 2: Review questions: Edit, Approve or Reject questions

1. QR manager logs in with Unique user ID and password. On successful login, the user would be able to see the home page with the following tabs; ‘Review questions’ and ‘Manage reviewed questions’
2. The home page will display the following metrics
1. Number of approved questions
2. Number of questions pending review
3. Number of rejected questions
3. Once the QR_M clicks on ‘Review questions’, all the questions appear for review. This list will have multiple options to filter/sort based on position, roles, competency and competency levels, and question type. 
4. If QR_M wants to edit the question, a button will be available next to each question. On clicking this, a new window will open with the option to edit the body of the question, the body of the alternatives and the mapping of the question to competency level. On clicking ‘Save and Update’, question will be tagged as “approved with edits”


#### Use case 3: Manages and maintains questions repository

1. On clicking on the ‘Manage reviewed questions’ tab, the list of questions which have been approved and rejected by the specific QR_M will be displayed
2. QR_M will have the option to multi-select questions and edit their status - i.e., previously approved questions can be rejected and vice versa

<table>
  <tr>
   <td>
<strong>S. No</strong>
   </td>
   <td><strong>Functionality </strong>
   </td>
   <td><strong>User</strong>
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>Propose competency wise questions to questions repository
   </td>
   <td>QR contributor 
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>Review questions : Edit, Approve or Reject questions 
   </td>
   <td>QR Manager
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td>Manage and maintain question repository
   </td>
   <td>QR Manager
   </td>
  </tr>
</table>


#### Use case 4: Compose assessment blueprints for various roles and cadres in public health

1. PIAA setter logs in using unique user id based login and password
2. The PIAA setter creates an assessment blueprint by tagging target audience (positions)
3. The PIAA setter adds attributes and tags to the assessment blueprint
    1. Name of assessment
    2. Description
    3. Mode - practice question papers vs PIAA only vs both
4. Further, the PIAA setter adds additional tags to the assessment blueprint by selecting a set of competencies (dropdown) from the competency directory. The competency directory will only reflect those competencies which are applicable to the position selected by the PIAA Setter in the previous step
5. The platform will list all the questions applicable to the competencies of a position
6. The PIAA Setter will have an option to multi-select the questions and lock them for PIAA. These questions will not display in the practice question papers for candidates
7. The PIAA setter will define the assessments blueprint: 
    4. Blueprint will include - # of questions by competency levels (version 2 to also include # of questions by question type)
    5. System will pick randomly during conduction of the assessment from locked questions only as per the defined blueprint
8. Preview and finalise the assessment blueprints and has the option to make them go-live
9. Once an assessment blueprint is finalised and made live, it will be visible to the relevant positions for self practice assessment and to the PIAA Nodal for those positions 
10. Homepage will have all assessment blueprints – draft-in-process, finalised but not live and currently live. PIAA setters will be able to remove assessment blueprints from live, edit assessment blueprints and delete existing blueprints at any stage. 


### Use case 5: Initiate assessment session for candidates and facilitate

1. PIAA nodal logins in with unique ID and password based login - Authentication of candidate will be handled offline.
2. The PIAA nodal is able to see all live and PIAA tagged assessment blueprints on the home screen with positions and competency levels tagged for each blueprint
3. The same login should work simultaneously such that the PIAA nodal can be logged in with all desktop computers at the PIAA centre
4. The assessment blueprint can be started as follows:
    1. Individual - PIAA nodal opens the assessment blueprint on a desktop computer and maps it to a candidate and starts the assessment 
    2. Batch start can be part of Version 2
5. Once the assessment goes live, the assessment taker is shown an instructions page and the timer for the assessment starts once the assessment taker presses ‘Okay’
6. The assessment should allow moving from one question to another, to edit responses and to move back to earlier questions to review / update answers. 
7. The PIAA nodal can pause, resume, stop assessment for any assessment taker on the system
8. The PIAA nodal should be able to submit a feedback / issues form after every assessment to be able to submit the data to the admin
9. The assessment taker can provide feedback for the assessment sessions (This would be optional. After completion of each assessment, a mail with the feedback form would be sent where the feedback can be raised)


#### Use case 6: Take a self practice assessment 

1. candidate logs in with unique ID and password
2. Once successfully logged in, the candidate has the following tabs/sections on the home page – User profile (editable data fields for the individual. Mandatory on first login) ‘self practice assessment’ and ‘View Certificate’
3. By clicking on the self practice assessment tab, the list of available assessment blueprints for that position are displayed, by clicking on the blueprint, the competency lists being assessed in the blueprint can be viewed. 
4. The candidate selects ‘take the self practice assessment’ for any of the available blueprints and starts the self practice assessment after an instructions screen. 
5. Each time the self practice assessment is triggered for any assessment blueprint, based on the pre-defined composition algorithm, random questions are selected from the question bank and displayed in a random order to the candidate. The questions locked in PIAA assessment blueprints won’t be displayed in self practice assessment
6. An option for timed or untimed assessment may be given to the candidate (version 1 can be untimed with version 2 having both options)
7. candidate submits their responses to all the questions in the self practice assessment and submits. Option to review answers, move back and forward on the questions and end test without answering all questions may be provided. 
8. candidates are shown the score achieved and have the option to scroll through the questions with the answer given by them and the correct answer indicated against each question. 


#### Use Case 7: View and download certificate


1. Candidate logs in with unique ID and password
2. Once successfully logged in, the candidate has the following tabs/sections on the home page – User profile (editable data fields for the individual. Mandatory on first login) ‘self practice assessment’ and ‘View Certificate’
3. By clicking on the view certificate tab, the candidate will be able to see a list view of the certificates for the assessments they’ve taken so far

<table>
  <tr>
   <td>
<strong>#</strong>
   </td>
   <td><strong>Assessment Code</strong>
   </td>
   <td><strong>Date taken</strong>
   </td>
   <td><strong>Status of issuance</strong>
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>GNM064
   </td>
   <td>01/09/2022
   </td>
   <td><strong>VIEW CERTIFICATE </strong>(download icon)
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>GNM098
   </td>
   <td>09/09/2022
   </td>
   <td>In process
   </td>
  </tr>
</table>




4. By clicking on the ‘View Certificate’ CTA, they will be able to view their certificate
5. Additionally, there would be an option to download the certificate through a download icon across the particular assessment taken

<table>
  <tr>
   <td>
<strong>S. No</strong>
   </td>
   <td><strong>Functionality </strong>
   </td>
   <td><strong>User</strong>
   </td>
  </tr>
  <tr>
   <td>4
   </td>
   <td>Compose assessment blueprints
   </td>
   <td>PIAA setter
   </td>
  </tr>
  <tr>
   <td>5
   </td>
   <td>Initiates a PIAA session
   </td>
   <td>PIAA Nodal
   </td>
  </tr>
  <tr>
   <td>6
   </td>
   <td>Generate and initiate a practice question paper
   </td>
   <td>candidate
   </td>
  </tr>
  <tr>
   <td>7
   </td>
   <td>View and download certificate
   </td>
   <td>candidate
   </td>
  </tr>
</table>


#### Use case 8: Review assessments, approving / aborting assessment blueprints for the evaluation of results


1. Admin logs in with unique ID and password
2. Admin’s home page will have the following tabs: ‘Review assessment sessions’ and  ‘Issue certificates’
3. The Admin selects the ‘Review assessment sessions’ tab
4. Admin reviews all assessment sessions from issues / comments shared by the PIAA nodal  and takes a decision to approve/ abort an assessment session based on the SOPs. Only approved assessments will be sent for calculation of results by the UPTSU


#### Use Case 9: View results and issue certificates to assessment takers

1. Admin logs in with unique ID and password
2. Admin’s home page will have the following tabs: ‘Review assessment sessions’ and  ‘Issue certificates’
3. The Admin selects the ‘Issue certificates’ tab
4. This tab will reflect a list view of candidates whose results have been evaluated and generated by UPTSU along with the status of certificate issuance

<table>
  <tr>
   <td>
<strong>#</strong>
   </td>
   <td><strong>Name of the candidate/ Assessment Taker</strong>
   </td>
   <td><strong>Assessment Code</strong>
   </td>
   <td><strong>Status of Issuance</strong>
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>Sagari
   </td>
   <td>GNM063
   </td>
   <td><em>Certificate issued</em>
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>Rinkle
   </td>
   <td>ANM023
   </td>
   <td><strong>ISSUE CERTIFICATE</strong>
   </td>
  </tr>
</table>




5. The admin can find a CTA to issue certificates across the name of each candidate. By clicking the same, a certificate will be generated and issued to the candidate
6. The admin will also have an option to multi select/ select all candidates and issue them the certificates upon which the certificate will be issued to the candidates

<table>
  <tr>
   <td>
<strong>S. No</strong>
   </td>
   <td><strong>Functionality </strong>
   </td>
   <td><strong>User</strong>
   </td>
  </tr>
  <tr>
   <td>8
   </td>
   <td>Review assessments, approving / aborting assessment blueprints for the evaluation of results
   </td>
   <td>Admin
   </td>
  </tr>
  <tr>
   <td>9
   </td>
   <td>View results and issue certificates to assessment takers
   </td>
   <td>Admin
   </td>
  </tr>
</table>

