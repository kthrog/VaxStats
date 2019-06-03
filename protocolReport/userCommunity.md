## R<sup>3</sup> User Community
Though its practice only touches a small segment of the health sector, the vaccination of young, school-age children has far-reaching effects on the general population. Failure to vaccinate cannot only be grounds for denial of entry at many public schools, but failure to do so can endanger lives, and even cause premature death, when outbreaks of vaccine-preventable diseases rage out of control. Thus, vaccination and immunization information may be of interest to the following parties:
- Health officials and medical professionals
- Education administrators, teachers, students, and parents of students
- Policy analysts, legislators, and other citizen interest groups
- Researchers and nonprofit groups 
- Journalists
- General public

### Data Requirements
The VaxStats project anticipates these groups will have the following requirements from a vaccination data repository. 

| **User Group**| | **Data Access** | | **Data Format** | | **Data Analysis** |
| --- | --- | --- | --- |
| Department of Health | API, File download, GUI browsing | Plain text, non-encoded CSV |See full picture of vaccination data for their area |
| School Administrator | File download, GUI browsing | Open formats, not specific | Track school vaccination data over time, and compare data from surrounding districts |

Policy Analyst
API, File download, GUI browsing
Plain text, non-encoded CSV
View historical and multi-region data, as well as visualize it 
Journalist
File download, GUI browsing
Open formats, not specific 
Find data easily, read data descriptions, and visualize data
Epidemiologist 
API, File download, GUI browsing
Plain text, non-encoded CSV
Load data into statistical processing software and compare with other data
General Public
GUI browsing
Open formats, not specific 
Find and browse data quickly and easily

Data Repository
Additionally, because many of these user communities may already be accustomed to retrieving local data from an open government data portal, administered by their state, city, or county, we do not anticipate building a distinct repository for this data. Instead, VaxStats would contribute curated data to an already existing and available repository, such as data.wa.gov, which is built on Socrata. Not only does VaxStats believe this would contribute to better findability and accessibility for vaccination data, it would serve as secure hosting and storage for the data in the long term. Using a well-known repository with other types of data also has the added benefit of potentially displaying related datasets to those seeking vaccination data, increasing the likelihood of reuse and encouraging interoperability. 
User Community Context 
The user community of those interested in vaccination data can be complex, so it helps to begin with some context before detailing goal-oriented user stories. 
Legal Constraints
First, each U.S. state has differing vaccination requirements and public health administrative structures--plus, some use slightly different recommended vaccination schedules (Idaho’s, Oregon’s, and Washington’s), though many stick to the standardized schedules published by the Centers for Disease Control (CDC). The VaxStats project focuses on just the Pacific Northwest (PNW), defined as the states of Washington, Oregon, and Idaho, but even across these three states, laws vary. Additionally, some states currently have proposed changes pending to their immunization laws. For a brief overview of the PNW’s vaccination laws, see the legislative overview. 

Privacy Constraints
Second, because vaccination data is inextricably linked to medical data and because vaccination data is often collected by schools, many patient and student protections apply such as HIPAA and FERPA. These protections often result in already-aggregated data, as well as in inaccessible data formatting.

Interoperability Constraints
Third, due to the issues above, no state is producing or releasing vaccination in exactly the same way. VaxStats will cover this more thoroughly when describing cascading quality tiers of vaccination data. 

User Stories
User stories capture the the goals of the various user communities and stakeholders outlined above, as well as what potential depositors wish to accomplish when contributing data to VaxStats. These stories guide the repository’s documentation, policies, features, and curation efforts, setting the tone for what VaxStats hopes to achieve, and who it intends to serve. 

Users Seeking Data
Goal
User Story
Find data about vaccination exemptions 
“As a parent, I want to know what the vaccination exemption rate is in my county.”
Find data about vaccination requirements and recommendations
“As a policymaker, I want to better understand what other states in the PNW require for vaccination.”
Find data about multiple types of vaccines
“As a health official, I want to know which vaccines are waived most frequently.”
Download data in machine-readable formats
“As a journalist, I want to analyze a lot of data at once in order to tell a data-driven story about a recent measles outbreak in my area.”


Users Depositing Data
Goal
User Story
Transform data into an acceptable format for deposit
“As a public health official, I want to take aggregated data in PDF format, and produce a raw dataset appropriate for deposit.”
Protect sensitive data before placing in public repository
“As a local government employee, I want to ensure that any data released to the repository won’t compromise personally identifiable information of citizens.”
Know how datasets will be stored, secured, and accessed in the future
“As a researcher, I want to know if this data is secure, and if it will be available persistently in the future.”

