# Lab 103 - Analyze Alerts and Audit Reports in Oracle Data Safe



- <a href='#Lab103-AnalyzeAlertsandAuditReportsinOracleDataSafe-BeforeYouBegin'>Before You Begin</a>

- <a href='#Lab103-AnalyzeAlertsandAuditReportsinOracleDataSafe-STEP1:Viewandclosealerts'>STEP 1: View and close alerts</a>

- <a href='#Lab103-AnalyzeAlertsandAuditReportsinOracleDataSafe-STEP2:Analyzeopenalertsfromthedashboard'>STEP 2: Analyze open alerts from the dashboard</a>

- <a href='#Lab103-AnalyzeAlertsandAuditReportsinOracleDataSafe-STEP3:Viewallauditrecordsforthepastweek'>STEP 3: View all audit records for the past week</a>

- <a href='#Lab103-AnalyzeAlertsandAuditReportsinOracleDataSafe-STEP4:Viewasummaryofauditeventscollectedandalertsraised'>STEP 4: View a summary of audit events collected and alerts raised</a>

- <a href='#Lab103-AnalyzeAlertsandAuditReportsinOracleDataSafe-STEP5:Createafailedloginsreport'>STEP 5: Create a failed logins report</a>





<h2 id="Lab103-AnalyzeAlertsandAuditReportsinOracleDataSafe-BeforeYouBegin">Before You Begin


### Objectives

In this lab, you learn how to do the following:

- View and close alerts
- Analyze open alerts from the dashboard
- View all audit records for the past week
- View a summary of audit events collected and alerts raised
- Create a failed logins report



### Requirements

To complete this lab, you need to have the following:

- Login credentials for the Oracle Data Safe Console
- An Oracle Data Safe service enabled in a region of your tenancy
- A registered target database in Oracle Data Safe with sample data
- Audit collection started on your target database in Oracle Data Safe. If not, see <a href="Lab-102---Provision-Audit-and-Alert-Policies-in-Oracle-Data-Safe.md">Lab 102 - Provision Audit and Alert Policies in Oracle Data Safe</a>.



### Assumptions

This lab assumes that you are signed in to the Oracle Data Safe Console. If not, see <a href="Lab-101---View-a-Registered-Target-Database-in-Oracle-Data-Safe.md">Lab 101 - View a Registered Target Database in Oracle Data Safe</a>, step 1 or 2.

Your data values may be different than those shown in the screenshots in this lab.<h2 id="Lab103-AnalyzeAlertsandAuditReportsinOracleDataSafe-STEP1:Viewandclosealerts">**STEP 1**: View and close alerts

- In Oracle Data Safe Console, click the **Alerts** tab.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177413545.png" data-image-src="attachments/177047606/177413545.png" data-unresolved-comment-count="0" data-linked-resource-id="177413545" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-13-25.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- At the top of the **All Alerts** page, click **Summary**.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177413549.png" data-image-src="attachments/177047606/177413549.png" data-unresolved-comment-count="0" data-linked-resource-id="177413549" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-13-48.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- View the total number of target databases, critical alerts, high risk alerts, medium risk alerts, and open alerts.


  At a glance, you can better understand whether the security of your database is in jeopardy and how you should prioritize your work.

  The totals in your report may be different.

  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177425111.png" data-image-src="attachments/177047606/177425111.png" data-unresolved-comment-count="0" data-linked-resource-id="177425111" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-4_15-36-26.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- Scroll down to review the alerts in the table.


  The **DB User** column identifies who is doing the action.

  The **Operation** column identifies the action.

  The **Alert Severity** column indicates how serious the action is.

  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177425122.png" data-image-src="attachments/177047606/177425122.png" data-unresolved-comment-count="0" data-linked-resource-id="177425122" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-4_15-37-50.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">



- At the bottom of the page, click the page numbers to view other pages of alerts.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177413552.png" data-image-src="attachments/177047606/177413552.png" data-unresolved-comment-count="0" data-linked-resource-id="177413552" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-14-59.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">



- To filter the report to show only critical alerts, at the top of the report, click **Filters**. Click **+ Filter**, and then set the filter to be: **Alert Severity = Critical**. Click **Apply**.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177425079.png" data-image-src="attachments/177047606/177425079.png" data-unresolved-comment-count="0" data-linked-resource-id="177425079" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-4_15-32-36.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- Position the cursor over the **DB User** column and click the up arrow button to sort the column.


  <img class="confluence-embedded-image confluence-content-image-border" height="76" width="426" src="attachments/177047606/177413555.png" data-image-src="attachments/177047606/177413555.png" data-unresolved-comment-count="0" data-linked-resource-id="177413555" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-16-31.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- The table shows you the open critical alerts. 


  The number of open alerts may be different for you.

  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177425142.png" data-image-src="attachments/177047606/177425142.png" data-unresolved-comment-count="0" data-linked-resource-id="177425142" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-4_15-39-18.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- Click one of the **Alert IDs** to view more detail.


  <img class="confluence-embedded-image confluence-content-image-border" height="144" width="326" src="attachments/177047606/177425153.png" data-image-src="attachments/177047606/177425153.png" data-unresolved-comment-count="0" data-linked-resource-id="177425153" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-4_15-40-14.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

- Review the information in the **Alert Details** dialog box, and then click **X** to close it.


  You can view the **OS User**, **Client Host**, **Client Program**, **Client IP**, **Operation Time**, and much more.

  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177425160.png" data-image-src="attachments/177047606/177425160.png" data-unresolved-comment-count="0" data-linked-resource-id="177425160" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-4_15-40-57.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

- Click the **X** next to each filter to remove them.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177425173.png" data-image-src="attachments/177047606/177425173.png" data-unresolved-comment-count="0" data-linked-resource-id="177425173" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-4_15-42-49.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- Create two filters to find out if the user <code>EVIL_RICH</code> is making any user entitlement changes.


  To create the first filter, click **+ Filter** and set the filter to be: **Alert = User Entitlement Changes**.

  To create the second filter, click **+Filter**, and set the filter to be: **DB User = EVIL_RICH**. Click **Apply**.

  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177425186.png" data-image-src="attachments/177047606/177425186.png" data-unresolved-comment-count="0" data-linked-resource-id="177425186" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-4_15-44-21.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- Notice that there are several alerts for <code>EVIL_RICH</code>. Note that the number of alerts that you see may be different. Click the **Alert ID** for the first alert. 


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177425201.png" data-image-src="attachments/177047606/177425201.png" data-unresolved-comment-count="0" data-linked-resource-id="177425201" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-4_15-45-52.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- Scroll down in the **Alert Details** dialog box.


  Notice that <code>EVIL_RICH</code> tried to execute the SQL command: <code>grant PDB_DBA to ATILLA</code>, but failed. Close the dialog box.

  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177425210.png" data-image-src="attachments/177047606/177425210.png" data-unresolved-comment-count="0" data-linked-resource-id="177425210" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-4_15-46-53.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- Open the other **Alert IDs** for <code>EVIL_RICH</code>. Notice that the SQL text is similar in that the failed grants are for the <code>ATILLA</code> user.




- Suppose you take appropriate action. Now you can close the alerts. To do so, select the check box in the top left corner of the table to select all of the alerts displayed. From the **Mark As** menu, select **Closed**.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177425240.png" data-image-src="attachments/177047606/177425240.png" data-unresolved-comment-count="0" data-linked-resource-id="177425240" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-4_15-51-7.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- To hide closed alerts, move the **Open Alerts only** slider to the right.


  <img class="confluence-embedded-image confluence-content-image-border" height="58" width="224" src="attachments/177047606/177413562.png" data-image-src="attachments/177047606/177413562.png" data-unresolved-comment-count="0" data-linked-resource-id="177413562" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-18-42.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  <h2 id="Lab103-AnalyzeAlertsandAuditReportsinOracleDataSafe-STEP2:Analyzeopenalertsfromthedashboard">**STEP 2**: Analyze open alerts from the dashboard

- Click the **Home** tab.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177413563.png" data-image-src="attachments/177047606/177413563.png" data-unresolved-comment-count="0" data-linked-resource-id="177413563" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-19-10.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- Review the information in the charts on the dashboard.


  Note: There is no data for Data Discovery and Data Masking because you have not yet used those features.

  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177408455.png" data-image-src="attachments/177047606/177408455.png" data-unresolved-comment-count="0" data-linked-resource-id="177408455" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-2_16-1-26.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- In the **Open Alerts** chart, notice that the chart shows the number of open alerts for the last 7 days. Click the last node in the chart.


  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="469" src="attachments/177047606/177408465.png" data-image-src="attachments/177047606/177408465.png" data-unresolved-comment-count="0" data-linked-resource-id="177408465" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-2_16-2-33.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">



- In the **Open Alerts** dialog box, view the number of open alerts for the last 7 days.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177408484.png" data-image-src="attachments/177047606/177408484.png" data-unresolved-comment-count="0" data-linked-resource-id="177408484" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-2_16-3-55.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">



- Hover over the counts to view the number of **Critical**, **High**, and **Medium** alerts for each day.


  

- Click the name of your target database to open the **All Alerts** report.


  <img class="confluence-embedded-image confluence-content-image-border" height="127" width="235" src="attachments/177047606/177413566.png" data-image-src="attachments/177047606/177413566.png" data-unresolved-comment-count="0" data-linked-resource-id="177413566" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-20-8.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- Notice that the **All Alerts** report is filtered to show only the open alerts for your target database for the past 7 days.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177408562.png" data-image-src="attachments/177047606/177408562.png" data-unresolved-comment-count="0" data-linked-resource-id="177408562" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-2_16-8-57.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  <h2 id="Lab103-AnalyzeAlertsandAuditReportsinOracleDataSafe-STEP3:Viewallauditrecordsforthepastweek">**STEP 3**: View all audit records for the past week

- Click the **Reports** tab.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177413569.png" data-image-src="attachments/177047606/177413569.png" data-unresolved-comment-count="0" data-linked-resource-id="177413569" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-20-51.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- On the left, expand **Audit Reports** (if needed), and then click the **All Activity** report.


  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="162" src="attachments/177047606/177413571.png" data-image-src="attachments/177047606/177413571.png" data-unresolved-comment-count="0" data-linked-resource-id="177413571" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-21-14.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- At the top of the report, view the totals for **Targets**, **DB Users**, **Client Hosts**, **Login Success**, **Login Failures**, **User Changes**, **Privilege Changes**, **DDLs**, and **DMLs**.


  <img class="confluence-embedded-image confluence-content-image-border" width="680" src="attachments/177047606/177408585.png" data-image-src="attachments/177047606/177408585.png" data-unresolved-comment-count="0" data-linked-resource-id="177408585" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-2_16-11-14.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- If the filters are not displayed, click **Filters**.




- Notice that the report is automatically filtered to show one week's worth of audit data for your target database.


  <img class="confluence-embedded-image confluence-content-image-border" width="680" src="attachments/177047606/177408600.png" data-image-src="attachments/177047606/177408600.png" data-unresolved-comment-count="0" data-linked-resource-id="177408600" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-2_16-13-49.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28"><h2 id="Lab103-AnalyzeAlertsandAuditReportsinOracleDataSafe-STEP4:Viewasummaryofauditeventscollectedandalertsraised">**STEP 4**: View a summary of audit events collected and alerts raised

- On the left, click **Summary Reports**, and then click **Audit Summary**.


  The **Audit Summary** report helps you to gain an understanding of the activity trends of your target databases. By default, the report shows you data for all of your target databases for the past week.

  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="236" src="attachments/177047606/177413579.png" data-image-src="attachments/177047606/177413579.png" data-unresolved-comment-count="0" data-linked-resource-id="177413579" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-21-53.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- View the totals to learn how many target databases are represented in the charts, how many users are audited, and how many client hosts have connected to your target database.


  The report is filtered to show data for the last week.

  Your data may be different.

  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177408621.png" data-image-src="attachments/177047606/177408621.png" data-unresolved-comment-count="0" data-linked-resource-id="177408621" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-2_16-15-37.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">



- View the charts.


  The **Open Alerts** chart compares the number of critical, high, and medium open alerts for the past week.

  The **Admin Activity** chart compares the number of logins, database schema changes, audit setting changes, and entitlement changes for the past week.

  The **Login Activity** chart compares the number of failed and successful logins for the past week.

  The **All Activity** chart compares the total number of events for the past week.

  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177408629.png" data-image-src="attachments/177047606/177408629.png" data-unresolved-comment-count="0" data-linked-resource-id="177408629" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-2_16-16-28.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">



- To filter the time period for the report, at the top, select **Last 1 Month** and click **Apply**.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177408636.png" data-image-src="attachments/177047606/177408636.png" data-unresolved-comment-count="0" data-linked-resource-id="177408636" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-2_16-17-36.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- To filter the target database for the report, click **All Targets**.


  <img class="confluence-embedded-image confluence-content-image-border" height="169" width="575" src="attachments/177047606/177413580.png" data-image-src="attachments/177047606/177413580.png" data-unresolved-comment-count="0" data-linked-resource-id="177413580" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-22-32.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- In the **Select Targets** dialog box, deselect the check box for **All Targets**, click the field and select your target database, and then click **Done**.


  <img class="confluence-embedded-image confluence-content-image-border" width="680" src="attachments/177047606/177408650.png" data-image-src="attachments/177047606/177408650.png" data-unresolved-comment-count="0" data-linked-resource-id="177408650" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-2_16-19-3.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- Notice that your target database is set as a filter.


  <img class="confluence-embedded-image confluence-content-image-border" height="141" width="330" src="attachments/177047606/177408657.png" data-image-src="attachments/177047606/177408657.png" data-unresolved-comment-count="0" data-linked-resource-id="177408657" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-2_16-19-52.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28"><h2 id="Lab103-AnalyzeAlertsandAuditReportsinOracleDataSafe-STEP5:Createafailedloginsreport">**STEP 5**: Create a failed logins report

- Click the **Reports** tab.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177413582.png" data-image-src="attachments/177047606/177413582.png" data-unresolved-comment-count="0" data-linked-resource-id="177413582" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-23-11.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- In the list under **Audit Reports**, click **Login Activity**.


  <img class="confluence-embedded-image confluence-content-image-border" src="attachments/177047606/177413585.png" data-image-src="attachments/177047606/177413585.png" data-unresolved-comment-count="0" data-linked-resource-id="177413585" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-23-35.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- In the **Login Activity** report, set a filter by selecting **Operation Status = FAILURE** (no quotes). Click **Apply**.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177413592.png" data-image-src="attachments/177047606/177413592.png" data-unresolved-comment-count="0" data-linked-resource-id="177413592" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-24-10.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- Notice that the report shows only failed logins. Your data may be different than what is shown below.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177413920.png" data-image-src="attachments/177047606/177413920.png" data-unresolved-comment-count="0" data-linked-resource-id="177413920" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_8-58-31.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- From the **Report Definition** menu, select **Save As New**.


  <img class="confluence-embedded-image confluence-content-image-border" height="162" width="516" src="attachments/177047606/177426047.png" data-image-src="attachments/177047606/177426047.png" data-unresolved-comment-count="0" data-linked-resource-id="177426047" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-4_16-54-39.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

- In the **Save As** dialog box, enter the report name **<user name> Failed Logins** (for example, **dsu100 Failed Logins**), enter **Failed logins report** for the description, select your resource group, and then click **Save As**. A confirmation message states &quot;Successfully created the report.&quot;


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177426111.png" data-image-src="attachments/177047606/177426111.png" data-unresolved-comment-count="0" data-linked-resource-id="177426111" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-4_16-59-32.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- Click the **Reports** tab.




- At the top of the list under **Custom Reports**, click your failed logins report (**<user name> Failed Logins)**.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177427052.png" data-image-src="attachments/177047606/177427052.png" data-unresolved-comment-count="0" data-linked-resource-id="177427052" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-4_17-58-9.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- Click **Generate Report**.


  <img class="confluence-embedded-image confluence-content-image-border" height="71" width="467" src="attachments/177047606/177413598.png" data-image-src="attachments/177047606/177413598.png" data-unresolved-comment-count="0" data-linked-resource-id="177413598" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-25-47.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- In the **Generate Report** dialog box, leave **PDF** selected, select your resource group, and then click **Generate Report**.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047606/177427064.png" data-image-src="attachments/177047606/177427064.png" data-unresolved-comment-count="0" data-linked-resource-id="177427064" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-4_17-59-50.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

- Wait for a confirmation message that states that the report was generated successfully.




- Click **Download Report**.


  The PDF is downloaded to your browser.

  <img class="confluence-embedded-image confluence-content-image-border" height="76" width="640" src="attachments/177047606/177413602.png" data-image-src="attachments/177047606/177413602.png" data-unresolved-comment-count="0" data-linked-resource-id="177413602" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_7-26-21.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

  

- Click the downloaded **Failed Logins.pdf** file to view it in Adobe Acrobat.


  <img class="confluence-embedded-image confluence-content-image-border" height="400" src="attachments/177047606/177427077.png" data-image-src="attachments/177047606/177427077.png" data-unresolved-comment-count="0" data-linked-resource-id="177427077" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-4_18-1-20.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047606" data-linked-resource-container-version="28">

- View the report, and then close it.







 



