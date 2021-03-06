# Welcome to Radium LIS
Radium LIS is a customizable and secure laboratory information system, built from the ground up
for clinical toxicology laboratories doing high-complexity lab testing. Radium LIS helps manage
patients, providers, outcomes (results & reports), test instruments (including panels, methods, worklists, and result exports), and everything a laboratory needs to do testing on samples for patients.

### Key Features
The key features of Radium LIS are:
* A secure datastore for patient demographics, provider information, test rules, reports, etc.
* Client Portal for providers to login, edit patients, create orders, and view reports.
* Laboratory Access to maintain clients, providers, tests, patients, and other system settings.
* Electronic Requisition Generator to automatically fill and file requisitions for orders.
* Electronic Signatures for Providers and Patients.
* Worklist Generator for LCMS instruments
* Quality Control Levey-Jennings charts generator for LCMS instruments

---
### Our Vision
The healthcare system in the United States is a giant conglomoration of different systems and software. 
We want to be a part of that. Laboratory Information Systems could and should be used in conjunction with other Lab Systems 
through cross communication to standardize patient medical records, allowing patients to access their medical testing
history with a secure storage platform.

### Software
The backend is written using [Perl Dancer](https://perldancer.org) with a [PostgreSQL](https://www.postgresql.org/) database, 
while the frontend is mostly [jQuery](jquery.com) and custom JS.
These technologies are simple, flexible, well documented, and I happened to know how to use them when starting Radium LIS.
I also found that Web-based technologies are on the rise, so it makes sense to integrate any new product with the existing 
infrastructure of the web. People like to work remotely.

### Security
The database is protected with a secure, encrypted password, known only to the server.
The server is protected by an encrypted login and dh-4096 key-only access.

Each user has configurable permissions to allow them to access only certain parts of the LIS, and every user action
is logged in a searchable auditlog. 

Every user password is encrypted in the database using chkpass so that the password is never in plain text.

As with any patient records, the hardware should be kept in a secure location which is under lock and key to prevent
data from being lost and/or stolen. Stolen patient health information is a serious concern and there
are necessary steps to take to prevent such things from happening.

### Suggestions
We would love your feedback! Email Rob with any suggestions: [rob.w3@pm.me](mailto:rob.w3@pm.me)

### Getting Involved
If you would like to get involved in helping this great product to grow, we have **some** work to be done:
* Developer with knowledge in Perl/Python, and Javascript. Remote applicants welcome.
* Sales Representatives with experience in the clinical laboratory industry.


If you would like to get involved but don't really like to get your hands dirty, please feel free to Donate.
(Donate button coming soon).

### Frequently Asked Questions:

<details><summary>How do I use the LIS?</summary>
<p markdown="1">
!!!! If you are a provider or work at a provider office, please see <a href="../providers">Getting Started For Providers</a>.

!!! If you are working in the lab, please see <a href="../labusers">Getting Started For Lab Personnel</a>
</p>
</details>
<br>
<details><summary>I need help with a specific problem in Radium LIS...</summary>
<p markdown="1">
! Please send a detailed summary of your problem to <a href="mailto:support@walls.solutions">support</a>
</p>
</details>
<br>
<details><summary>How do I get Radium LIS for my lab?</summary>
<p markdown="1">
!!! Please contact <a href="mailto:support@walls.solutions">support</a>. We discuss your laboratory's specific needs and 
!!! customize a quote so you only pay for what you need.
</p>
</details>