# Lab 104 - Assess Database Configurations and Users with Oracle Data Safe



- <a href='#Lab104-AssessDatabaseConfigurationsandUserswithOracleDataSafe-BeforeYouBegin'>Before You Begin</a>

- <a href='#Lab104-AssessDatabaseConfigurationsandUserswithOracleDataSafe-STEP1:RunaSecurityAssessmentjobagainstatargetdatabase'>STEP 1: Run a Security Assessment job against a target database</a>

- <a href='#Lab104-AssessDatabaseConfigurationsandUserswithOracleDataSafe-STEP2:RunaUserAssessmentjobagainstatargetdatabase'>STEP 2: Run a User Assessment job against a target database</a>

- <a href='#Lab104-AssessDatabaseConfigurationsandUserswithOracleDataSafe-STEP3:Analyzetheuserassessmentresults'>STEP 3: Analyze the user assessment results</a>

- <a href='#Lab104-AssessDatabaseConfigurationsandUserswithOracleDataSafe-STEP4:Analyzethesecurityassessmentresults'>STEP 4: Analyze the security assessment results</a>





<h2 id="Lab104-AssessDatabaseConfigurationsandUserswithOracleDataSafe-BeforeYouBegin">Before You Begin


### Objectives

- Run a Security Assessment job against a target database
- Run a User Assessment job against a target database
- Analyze the user assessment results
- Analyze the security assessment results



### Requirements

To complete this lab, you need to have the following:

- Login credentials for the Oracle Data Safe Console
- An Oracle Data Safe service enabled in a region of your tenancy
- A registered target database in Oracle Data Safe with sample audit data
- Audit collection started on your target database in Oracle Data Safe. If not, see <a href="Lab-102---Provision-Audit-and-Alert-Policies-in-Oracle-Data-Safe.md">Lab 102 - Provision Audit and Alert Policies in Oracle Data Safe</a>.



### Assumptions

This lab assumes that you are signed in to the Oracle Data Safe Console. If not, see <a href="Lab-101---View-a-Registered-Target-Database-in-Oracle-Data-Safe.md">Lab 101 - View a Registered Target Database in Oracle Data Safe</a>, steps 1 or 2.<h2 id="Lab104-AssessDatabaseConfigurationsandUserswithOracleDataSafe-STEP1:RunaSecurityAssessmentjobagainstatargetdatabase">**STEP 1**: Run a Security Assessment job against a target database

You can use Security Assessment to evaluate the current security state of your target databases and receive recommendations on how to mitigate the identified risks.

- In the Oracle Data Safe Console, click the **Home** tab, and then click the **Security Assessment** tab.


  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="133" src="attachments/177047600/177413495.png" data-image-src="attachments/177047600/177413495.png" data-unresolved-comment-count="0" data-linked-resource-id="177413495" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-59-36.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  

- On the **Security Assessment** page, select the check box for your target database, and then click **Assess**.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047600/177413497.png" data-image-src="attachments/177047600/177413497.png" data-unresolved-comment-count="0" data-linked-resource-id="177413497" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-0-2.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  

- While the assessment is running, continue to the next step.


  The assessment takes approximately 2-3 minutes to complete.

  <h2 id="Lab104-AssessDatabaseConfigurationsandUserswithOracleDataSafe-STEP2:RunaUserAssessmentjobagainstatargetdatabase">**STEP 2**: Run a User Assessment job against a target database

You can use User Assessment to identify user settings and risks on your target databases.

- Click the **User Assessment** tab.


  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="135" src="attachments/177047600/177413500.png" data-image-src="attachments/177047600/177413500.png" data-unresolved-comment-count="0" data-linked-resource-id="177413500" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-0-37.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  

- On the **User Assessment** page, select the check box for your target database, and then click **Assess**.


  The assessment takes approximately 10 seconds.

  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047600/177413502.png" data-image-src="attachments/177047600/177413502.png" data-unresolved-comment-count="0" data-linked-resource-id="177413502" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-0-58.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  <h2 id="Lab104-AssessDatabaseConfigurationsandUserswithOracleDataSafe-STEP3:Analyzetheuserassessmentresults">**STEP 3**: Analyze the user assessment results

- When the user assessment is completed, notice the following on the **User Assessment** page:


  A green check mark is displayed in the **Last Generated Report** column.

  You can view the number of **Critical Risk**, **High Risk**, **Medium Risk**, and **Low Risk** users.

  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047600/177413503.png" data-image-src="attachments/177047600/177413503.png" data-unresolved-comment-count="0" data-linked-resource-id="177413503" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-1-31.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">



- In the **Last Generated Report** column, click **View Report**.


  <img class="confluence-embedded-image confluence-content-image-border" height="113" width="222" src="attachments/177047600/177413505.png" data-image-src="attachments/177047600/177413505.png" data-unresolved-comment-count="0" data-linked-resource-id="177413505" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-1-54.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  

- On the **Users** page, review the 4 charts. You can click the small circles below the charts to navigate between the charts.


  The **User Risk** chart shows you the percent of users who are **Critical Risk**, **High Risk**, **Medium Risk**, and **Low Risk**.

  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="342" src="attachments/177047600/177413506.png" data-image-src="attachments/177047600/177413506.png" data-unresolved-comment-count="0" data-linked-resource-id="177413506" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-2-18.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  

  The **User Roles** chart shows you the number of users with the **DBA**, **DV Admin**, and **Audit Admin** roles.

  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="338" src="attachments/177047600/177413508.png" data-image-src="attachments/177047600/177413508.png" data-unresolved-comment-count="0" data-linked-resource-id="177413508" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-2-44.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  

  The **Last Password Change** chart shows you the number of users who have changed their passwords in the last 30 days, the last 30-90 days, and 90 days ago or more.

  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="340" src="attachments/177047600/177413509.png" data-image-src="attachments/177047600/177413509.png" data-unresolved-comment-count="0" data-linked-resource-id="177413509" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-3-3.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  

  The **Last Login** chart shows you the number of users that signed in to the database within the last 24 hours, within the last week, within the current month, within the current year, and a year ago or more.

  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="343" src="attachments/177047600/177413511.png" data-image-src="attachments/177047600/177413511.png" data-unresolved-comment-count="0" data-linked-resource-id="177413511" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-3-19.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  

- Review the table below the charts.


  This table lets you quickly identify critical and high risk users. It identifies users who are DBAs, DV Admins, and Audit Admins.

  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047600/177413512.png" data-image-src="attachments/177047600/177413512.png" data-unresolved-comment-count="0" data-linked-resource-id="177413512" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-3-41.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  

- Scroll to the right. In the **Audit Records** column, click **View Activity** for the <code>ADMIN</code> user.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047600/177413513.png" data-image-src="attachments/177047600/177413513.png" data-unresolved-comment-count="0" data-linked-resource-id="177413513" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-4-16.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  

- View the **All Activity** report.


  This report is automatically filtered to show you the audit records for the <code>ADMIN</code> user, for the past week, and for your target database.

  At the top of the report, you can view totals for **Targets**, **DB Users**, **Client Hosts**, **Login Success**, **Login Failures**, **User Changes**, **Privilege Changes**, **DDLs**, and **DMLs**.

  The **Event** column shows you the activites performed by this user.

  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047600/177413514.png" data-image-src="attachments/177047600/177413514.png" data-unresolved-comment-count="0" data-linked-resource-id="177413514" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-4-42.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  

- At the bottom of the page, click the page numbers to view more audit records.


  <img class="confluence-embedded-image confluence-content-image-border" height="42" width="560" src="attachments/177047600/177413515.png" data-image-src="attachments/177047600/177413515.png" data-unresolved-comment-count="0" data-linked-resource-id="177413515" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-5-8.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  

- At the top of the report, click **Back to User Assessment report**.


  <img class="confluence-embedded-image confluence-content-image-border" src="attachments/177047600/177413517.png" data-image-src="attachments/177047600/177413517.png" data-unresolved-comment-count="0" data-linked-resource-id="177413517" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-5-28.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  

- At the bottom of the **User Assessment** page, click **2** to view page 2.


  <img class="confluence-embedded-image confluence-content-image-border" height="42" width="436" src="attachments/177047600/177413519.png" data-image-src="attachments/177047600/177413519.png" data-unresolved-comment-count="0" data-linked-resource-id="177413519" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-5-52.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  

- Notice that the privileged user <code>VOLDEMORT</code> is expired. Click **View Activity** to view the audit records for the <code>VOLDEMORT</code> user.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047600/177413520.png" data-image-src="attachments/177047600/177413520.png" data-unresolved-comment-count="0" data-linked-resource-id="177413520" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-6-10.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  

- Notice that <code>VOLDEMORT</code> has no activity on the target database.


  Here is a case where you might consider removing this user from the target database.

  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047600/177413522.png" data-image-src="attachments/177047600/177413522.png" data-unresolved-comment-count="0" data-linked-resource-id="177413522" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-6-32.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  <h2 id="Lab104-AssessDatabaseConfigurationsandUserswithOracleDataSafe-STEP4:Analyzethesecurityassessmentresults">**STEP 4**: Analyze the security assessment results

- Click the **Home** tab, and then click the **Security Assessment** tab.


  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="133" src="attachments/177047600/177413525.png" data-image-src="attachments/177047600/177413525.png" data-unresolved-comment-count="0" data-linked-resource-id="177413525" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-6-52.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  

- On the **Security Assessment** page, view when you last assessed the security of your target database, and the number of **High Risk**, **Medium Risk**, and **Low Risk** users. In the **Last Generated Report** column, click **View Report** to view the **Comprehensive Assessment** report.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047600/177413527.png" data-image-src="attachments/177047600/177413527.png" data-unresolved-comment-count="0" data-linked-resource-id="177413527" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-7-11.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  

- At the top of the **Comprehensive Assessment** report, you can view the target database name, when the database was assessed, and the database version.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047600/177413531.png" data-image-src="attachments/177047600/177413531.png" data-unresolved-comment-count="0" data-linked-resource-id="177413531" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-7-36.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  

- Also at the top of the report, you can view totals for the following:


  Risk levels (**High Risk**, **Medium Risk**, **Low Risk**, **Advisory**, **Evaluate**, and **Pass**). These totals give you an idea of how secure your database is. Notice that the risk levels are color coded**.**

  **Security Controls**, **User Security**, and **Security Configurations**. These totals show you the number of findings for each high-level category in the report.

  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047600/177413533.png" data-image-src="attachments/177047600/177413533.png" data-unresolved-comment-count="0" data-linked-resource-id="177413533" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-8-0.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  

- In the **Summary** category, you can view a table that compares the number of findings for each category and counts the number of findings per risk level. These values help you to identify areas that need attention.


  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="606" src="attachments/177047600/177413534.png" data-image-src="attachments/177047600/177413534.png" data-unresolved-comment-count="0" data-linked-resource-id="177413534" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-8-21.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  

- Expand **User Accounts** to view a list of all the user accounts in the target database. You can view each user's status, profile, and tablespace; whether the user is Oracle defined; and the authentication type for the user.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047600/177413535.png" data-image-src="attachments/177047600/177413535.png" data-unresolved-comment-count="0" data-linked-resource-id="177413535" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-8-41.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  

- Expand **User Profiles** to view a list of profile names, parameters, and values.


  <img class="confluence-embedded-image confluence-content-image-border" src="attachments/177047600/177413536.png" data-image-src="attachments/177047600/177413536.png" data-unresolved-comment-count="0" data-linked-resource-id="177413536" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-9-6.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  

- Scroll down and expand categories. Each category lists related findings about your database and how you can make changes to improve its security.


  On the right, indicators show whether a finding is recommended by the Center for Internet Security (**CIS**), European Union's General Data Protection Regulation (**GDPR**), and/or Security Technical Implementation Guide (**STIG**). These indications make it easy for you to identify the recommended security controls.

  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047600/177413537.png" data-image-src="attachments/177047600/177413537.png" data-unresolved-comment-count="0" data-linked-resource-id="177413537" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-9-35.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  

- Scroll to the top of the report, and then click **Medium Risk** to filter the report to show only medium risk findings.


  It's a toggle so if you click it again, the filter is removed.

  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047600/177413538.png" data-image-src="attachments/177047600/177413538.png" data-unresolved-comment-count="0" data-linked-resource-id="177413538" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-9-55.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">

  

- Scroll down to the **Account Locking after Failed Login Attempts** category and view the information.


  Notice that there are many users with unlimited failed login attempts.

  Oracle recommends that you use the <code>FAILED_LOGIN_ATTEMPTS</code> and <code>PASSWORD_LOCK_TIME</code> profile resources to lock user accounts for a specified time when there are multiple failed login attempts without a successful login.

  <img class="confluence-embedded-image confluence-content-image-border" height="211" width="650" src="attachments/177047600/177413539.png" data-image-src="attachments/177047600/177413539.png" data-unresolved-comment-count="0" data-linked-resource-id="177413539" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-10-21.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047600" data-linked-resource-container-version="16">




 



