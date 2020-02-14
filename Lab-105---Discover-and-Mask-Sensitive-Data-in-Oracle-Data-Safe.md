# Lab 105 - Discover and Mask Sensitive Data in Oracle Data Safe



- <a href='#Lab105-DiscoverandMaskSensitiveDatainOracleDataSafe-BeforeYouBegin'>Before You Begin</a>

- <a href='#Lab105-DiscoverandMaskSensitiveDatainOracleDataSafe-STEP1:ViewsensitivedatainyourATPdatabase'>STEP 1: View sensitive data in your ATP database</a>

- <a href='#Lab105-DiscoverandMaskSensitiveDatainOracleDataSafe-STEP2:DiscoversensitivedatabyusingDataDiscovery'>STEP 2: Discover sensitive data by using Data Discovery</a>

- <a href='#Lab105-DiscoverandMaskSensitiveDatainOracleDataSafe-STEP3:MasksensitivedatabyusingDataMasking'>STEP 3: Mask sensitive data by using Data Masking</a>

- <a href='#Lab105-DiscoverandMaskSensitiveDatainOracleDataSafe-STEP4:ValidatethemaskeddatainyourATPdatabase'>STEP 4: Validate the masked data in your ATP database</a>





<h2 id="Lab105-DiscoverandMaskSensitiveDatainOracleDataSafe-BeforeYouBegin">Before You Begin


### Objectives

- View sensitive data in your Autonomous Transaction Processing (ATP) database
- Discover sensitive data by using Data Discovery
- Mask sensitive data by using Data Masking
- Validate the masked data in your ATP database



### Requirements

To complete this lab, you need to have the following:

- Login credentials for the Oracle Data Safe Console
- An Oracle Data Safe service enabled in a region of your tenancy
- A registered target database in Oracle Data Safe with sample audit data and the password for the <code>ADMIN</code> user account
<h2 id="Lab105-DiscoverandMaskSensitiveDatainOracleDataSafe-STEP1:ViewsensitivedatainyourATPdatabase">**STEP 1**: View sensitive data in your ATP database

In this step, you use SQL Developer Web to query sensitive data in your ATP database. You can access SQL Developer Web in the ATP Console.

- In a new browser window, enter the url to your region in the Oracle Cloud Infrastructure Console.


  To access the Ashburn region, enter the following url:<a href="https://console.us-ashburn-1.oraclecloud.com/a/tenancy" rel="nofollow" class="external-link"><code> https://console.us-ashburn-1.oraclecloud.com.</code></a>

  To access the Frankfurt region, enter the following url:<a rel="nofollow" href="https://console.eu-frankfurt-1.oraclecloud.com/a/tenancy" class="external-link"><code> https://console.eu-frankfurt-1.oraclecloud.com.</code></a>

  

- If prompted, in the **Cloud Tenant** field on the **SIGN IN** page, enter your tenancy name, and then click **Continue**. Under **Oracle Cloud Infrastructure**, enter your user credentials for Oracle Cloud Infrastructure, and then click **Sign In**.


  Note: If you are signed in to Oracle Cloud Infrastructure on another tab, then you are not prompted to enter a tenancy name and can continue to the next step.

  

- Make sure the correct region is selected in your tenancy, for example, **US East (Ashburn)** or **Germany Central (Frankfurt)**.


  <img class="confluence-embedded-image confluence-content-image-border" height="706" width="367" src="attachments/177047621/177413377.png" data-image-src="attachments/177047621/177413377.png" data-unresolved-comment-count="0" data-linked-resource-id="177413377" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-20-29.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- From the navigation menu, select **Autonomous Transaction Processing**.


  <img class="confluence-embedded-image confluence-content-image-border" height="400" src="attachments/177047621/177413380.png" data-image-src="attachments/177047621/177413380.png" data-unresolved-comment-count="0" data-linked-resource-id="177413380" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-21-34.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

- Under **COMPARTMENT**, make sure that your compartment is selected. For example, the <code>dsu100</code> user should be able to access the <code>dscrg100</code> compartment.


  <img class="confluence-embedded-image confluence-content-image-border" height="167" width="343" src="attachments/177047621/177413383.png" data-image-src="attachments/177047621/177413383.png" data-unresolved-comment-count="0" data-linked-resource-id="177413383" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-22-9.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- In the list of databases, click the name of your database, for example, **dsatp100**.


  <img class="confluence-embedded-image confluence-content-image-border" width="680" src="attachments/177047621/177413385.png" data-image-src="attachments/177047621/177413385.png" data-unresolved-comment-count="0" data-linked-resource-id="177413385" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-22-33.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- Click **Service Console** to navigate to the **Autonomous Transaction Processing Console**.


  A new browser tab is opened called **Autonomous Transaction Processing | Overview**.

  <img class="confluence-embedded-image confluence-content-image-border" width="680" src="attachments/177047621/177413387.png" data-image-src="attachments/177047621/177413387.png" data-unresolved-comment-count="0" data-linked-resource-id="177413387" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-23-5.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- If the browser prevents you from opening a pop-up window, click **Options**, and then select **Allow pop-ups for console.us-ashburn-1.oraclecloud.com**.


  

- On the **Overview** page, click **Development**.


  <img class="confluence-embedded-image confluence-content-image-border" height="400" src="attachments/177047621/177413390.png" data-image-src="attachments/177047621/177413390.png" data-unresolved-comment-count="0" data-linked-resource-id="177413390" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-23-32.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- Click **SQL Developer Web**.


  <img class="confluence-embedded-image confluence-content-image-border" width="680" src="attachments/177047621/177413391.png" data-image-src="attachments/177047621/177413391.png" data-unresolved-comment-count="0" data-linked-resource-id="177413391" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-24-4.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- On the **SIGN IN** page for SQL Developer Web, enter the database credentials for the <code>ADMIN</code> user, and then click **Sign In**.


  You are provided the password during the lab.

  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="558" src="attachments/177047621/177413392.png" data-image-src="attachments/177047621/177413392.png" data-unresolved-comment-count="0" data-linked-resource-id="177413392" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-24-37.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- If a help note is displayed, you can click the **X** to close it.


  <img class="confluence-embedded-image confluence-content-image-border" width="680" src="attachments/177047621/177413393.png" data-image-src="attachments/177047621/177413393.png" data-unresolved-comment-count="0" data-linked-resource-id="177413393" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-24-59.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- On the **Navigator** tab, select the <code>HCM1</code> schema from the first drop-down menu. In the second drop-down menu, ensure that **Tables** is selected.


  <img class="confluence-embedded-image confluence-content-image-border" width="680" src="attachments/177047621/177413395.png" data-image-src="attachments/177047621/177413395.png" data-unresolved-comment-count="0" data-linked-resource-id="177413395" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-26-6.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- Drag the <code>EMPLOYEES</code> table to the worksheet.


  <img class="confluence-embedded-image confluence-content-image-border" width="680" src="attachments/177047621/177413397.png" data-image-src="attachments/177047621/177413397.png" data-unresolved-comment-count="0" data-linked-resource-id="177413397" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-26-39.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- When prompted to choose an insertion type, click **Select**, and then click **Apply**.


  <img class="confluence-embedded-image confluence-content-image-border" height="344" width="383" src="attachments/177047621/177413398.png" data-image-src="attachments/177047621/177413398.png" data-unresolved-comment-count="0" data-linked-resource-id="177413398" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-27-8.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- View the SQL query on the worksheet.


  <img class="confluence-embedded-image confluence-content-image-border" width="680" src="attachments/177047621/177413399.png" data-image-src="attachments/177047621/177413399.png" data-unresolved-comment-count="0" data-linked-resource-id="177413399" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-27-31.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- On the toolbar, click the **Run Statement** button (green circle with a white arrow) to execute the query.


  <img class="confluence-embedded-image confluence-content-image-border" height="67" width="609" src="attachments/177047621/177413401.png" data-image-src="attachments/177047621/177413401.png" data-unresolved-comment-count="0" data-linked-resource-id="177413401" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-28-7.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- Review the query results.


  Data such as <code>employee_id</code>, <code>first_name</code>, <code>last_name</code>, <code>email</code>, <code>phone_number</code>, <code>hire_date</code>, <code>job_id</code>, <code>salary</code>, and <code>manager_id</code> are considered sensitive data and should be masked if shared for non-production use, such as development and analytics.

  Keep this tab open so that you can return to it later in step 4 when you view the masked data.

  <img class="confluence-embedded-image confluence-content-image-border" width="680" src="attachments/177047621/177413404.png" data-image-src="attachments/177047621/177413404.png" data-unresolved-comment-count="0" data-linked-resource-id="177413404" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-28-46.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  <h2 id="Lab105-DiscoverandMaskSensitiveDatainOracleDataSafe-STEP2:DiscoversensitivedatabyusingDataDiscovery">**STEP 2**: Discover sensitive data by using Data Discovery

The Data Discovery wizard generates a sensitive data model that contains sensitive columns in your target database. When working in the wizard, you select sensitive types that you want to discover in your target database.

- Open a new tab in your browser, and enter one of the following URLs to the Oracle Data Safe Console.


  The URL you use depends on your region. The url for the Ashburn region is <a rel="nofollow" href="https://datasafe.us-ashburn-1.oci.oraclecloud.com/ui/index.html" class="external-link"><code>https://datasafe.us-ashburn-1.oci.oraclecloud.com/ui/index.html.</code></a> The url for the Frankfurt region is <a rel="nofollow" href="https://datasafe.eu-frankfurt-1.oci.oraclecloud.com/ui/index.html" class="external-link"><code>https://datasafe.eu-frankfurt-1.oci.oraclecloud.com/ui/index.html.</code></a>

  

  Because you signed in to Oracle Cloud Infrastructure in step 1, you should automatically sign in. If not, sign in with your your tenancy name (if needed) and user credentials.

  

  The **Home** tab is displayed.

  

- Access the Data Discovery wizard by clicking the **Data Discovery** tab.


  <img class="confluence-embedded-image confluence-content-image-border" height="400" src="attachments/177047621/177413405.png" data-image-src="attachments/177047621/177413405.png" data-unresolved-comment-count="0" data-linked-resource-id="177413405" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-29-15.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- On the **Select Target for Sensitive Data Discovery** page, select your target database, and then click **Continue**.


  <img class="confluence-embedded-image confluence-content-image-border" width="680" src="attachments/177047621/177413415.png" data-image-src="attachments/177047621/177413415.png" data-unresolved-comment-count="0" data-linked-resource-id="177413415" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-32-39.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- On the **Select Sensitive Data Model** page, leave **Create** selected, enter **SDM1** for the name, enable **Show and save sample data**, select your resource group, and then click **Continue**.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047621/177413416.png" data-image-src="attachments/177047621/177413416.png" data-unresolved-comment-count="0" data-linked-resource-id="177413416" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-33-10.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- On the **Select Schemas for Sensitive Data Discovery** page, scroll down and select the **HCM1** schema, and then click **Continue**.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047621/177413420.png" data-image-src="attachments/177047621/177413420.png" data-unresolved-comment-count="0" data-linked-resource-id="177413420" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-33-44.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- On the **Select Sensitive Types for Sensitive Data Discovery** page, expand all of the categories by moving the slider to the right, and then scroll down the page and review the sensitive types. Notice that you can select individual sensitive types, sensitive categories, and all sensitive types.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047621/177413423.png" data-image-src="attachments/177047621/177413423.png" data-unresolved-comment-count="0" data-linked-resource-id="177413423" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-34-27.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- At the top of the page, select the **Select All** check box, and then click **Continue** to start the data discovery job.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047621/177413425.png" data-image-src="attachments/177047621/177413425.png" data-unresolved-comment-count="0" data-linked-resource-id="177413425" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-34-57.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- When the job is completed, ensure that the **Detail** column states <code>Data discovery job finished successfully</code>, and then click **Continue**.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047621/177413427.png" data-image-src="attachments/177047621/177413427.png" data-unresolved-comment-count="0" data-linked-resource-id="177413427" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-35-35.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- On the **Sensitive Data Discovery Result** page, examine the sensitive data model created by the Data Discovery wizard. To view all of the sensitive columns, move the **Expand All** slider to the right.


  Oracle Data Safe automatically saves your sensitive data model to the Oracle Data Safe Library.

  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047621/177413428.png" data-image-src="attachments/177047621/177413428.png" data-unresolved-comment-count="0" data-linked-resource-id="177413428" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-36-14.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">



- From the drop-down list, select **Schema View** to sort the sensitive columns by table.


  <img class="confluence-embedded-image confluence-content-image-border" height="400" src="attachments/177047621/177413429.png" data-image-src="attachments/177047621/177413429.png" data-unresolved-comment-count="0" data-linked-resource-id="177413429" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-36-53.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- Scroll down the page to view the sensitive columns.


  You can view sample data (if it's available for a sensitive column), column counts, and estimated data counts.

  In particular, take a look at the sensitive columns that Data Discovery found in the <code>EMPLOYEES</code> table. Columns that do not have a check mark are called referential relationships. They are included because they have a relationship to another sensitive column and that relationship is defined in the database's data dictionary.

  Also view the sample data provided to get an idea of what the sensitive data looks like. Your sample data may be different.

  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047621/177413430.png" data-image-src="attachments/177047621/177413430.png" data-unresolved-comment-count="0" data-linked-resource-id="177413430" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-37-38.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">



- Scroll to the bottom of the page, and then click **Report** to view the Data Discovery report.


  The chart compares sensitive categories. You can view totals of sensitive values, sensitive types, sensitive tables, and sensitive columns.

  The table displays individual sensitive column names, sample data for the sensitive columns, column counts based on sensitive categories, and estimated data counts.

  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047621/177413431.png" data-image-src="attachments/177047621/177413431.png" data-unresolved-comment-count="0" data-linked-resource-id="177413431" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-38-14.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">



- Click the chart's **Expand** button.


  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="378" src="attachments/177047621/177413432.png" data-image-src="attachments/177047621/177413432.png" data-unresolved-comment-count="0" data-linked-resource-id="177413432" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-38-42.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- Position your mouse over **Identification Info** to view statistics.


  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="302" src="attachments/177047621/177413435.png" data-image-src="attachments/177047621/177413435.png" data-unresolved-comment-count="0" data-linked-resource-id="177413435" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-39-10.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- With your mouse still over **Identification Info**, click the **Expand** button to drill down.


  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="303" src="attachments/177047621/177413438.png" data-image-src="attachments/177047621/177413438.png" data-unresolved-comment-count="0" data-linked-resource-id="177413438" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-39-39.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- Notice that the **Identification Info** category is divided into two smaller categories (**Personal IDs** and **Public IDs**). To drill-up, position your mouse over an expanded sensitive category, and then click the **Collapse** button.


  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="364" src="attachments/177047621/177413439.png" data-image-src="attachments/177047621/177413439.png" data-unresolved-comment-count="0" data-linked-resource-id="177413439" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-40-2.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- Click the **Close** button (**X**) to close the expanded chart. Continue to work in the wizard.


  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="304" src="attachments/177047621/177413441.png" data-image-src="attachments/177047621/177413441.png" data-unresolved-comment-count="0" data-linked-resource-id="177413441" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-40-25.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  <h2 id="Lab105-DiscoverandMaskSensitiveDatainOracleDataSafe-STEP3:MasksensitivedatabyusingDataMasking">**STEP 3**: Mask sensitive data by using Data Masking

The Data Masking wizard generates a masking policy for your target database based on a sensitive data model. In the wizard, you select the sensitive columns that you want to mask and the masking formats to use.

- Click **Continue to mask the data**. The Data Masking wizard is displayed.


  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="410" src="attachments/177047621/177413442.png" data-image-src="attachments/177047621/177413442.png" data-unresolved-comment-count="0" data-linked-resource-id="177413442" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-40-52.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- On the **Select Target for Data Masking** page, your target database is selected. Click **Continue**.


  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="584" src="attachments/177047621/177413443.png" data-image-src="attachments/177047621/177413443.png" data-unresolved-comment-count="0" data-linked-resource-id="177413443" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-41-16.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- On the **Masking Policy** page, move the **Expand All** slider to the right to view all of the sensitive columns. Scroll down the page to view the default masking format selected for each sensitive column.


  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="321" src="attachments/177047621/177413444.png" data-image-src="attachments/177047621/177413444.png" data-unresolved-comment-count="0" data-linked-resource-id="177413444" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-41-38.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- For the <code>HCM1.LOCATIONS.STREET_ADDRESS</code> column, click the arrow to the right of the masking format to view other masking formats.


  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="453" src="attachments/177047621/177413445.png" data-image-src="attachments/177047621/177413445.png" data-unresolved-comment-count="0" data-linked-resource-id="177413445" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-42-10.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- Next to the arrow, click the **Edit Format** button (pencil icon).


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047621/177413446.png" data-image-src="attachments/177047621/177413446.png" data-unresolved-comment-count="0" data-linked-resource-id="177413446" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-42-34.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- In the **Edit Format** dialog box, view the description, examples, and default configuration for the masking format.


  This is where you can modify a masking format. Click **Cancel**.

  <img class="confluence-embedded-image confluence-content-image-border" height="400" src="attachments/177047621/177413447.png" data-image-src="attachments/177047621/177413447.png" data-unresolved-comment-count="0" data-linked-resource-id="177413447" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-43-2.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- At the bottom of the page, click **Confirm Policy**, and then wait a moment while Data Masking creates the masking policy.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047621/177413448.png" data-image-src="attachments/177047621/177413448.png" data-unresolved-comment-count="0" data-linked-resource-id="177413448" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-43-35.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- On the **Schedule the Masking Job** page, leave **Right Now** selected, and then click **Review**.


  <img class="confluence-embedded-image confluence-content-image-border" height="400" src="attachments/177047621/177413449.png" data-image-src="attachments/177047621/177413449.png" data-unresolved-comment-count="0" data-linked-resource-id="177413449" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-44-1.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- On the **Review and Submit** page, review the information, and then click **Submit** to start the data masking job.


  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="429" src="attachments/177047621/177413450.png" data-image-src="attachments/177047621/177413450.png" data-unresolved-comment-count="0" data-linked-resource-id="177413450" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-44-26.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- Wait for the data masking job to finish. It takes a couple of minutes. You can follow the status of the job on the **Masking Jobs** page. When the job is finished, click **Report**.


  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="640" src="attachments/177047621/177413451.png" data-image-src="attachments/177047621/177413451.png" data-unresolved-comment-count="0" data-linked-resource-id="177413451" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-44-49.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- Examine the **Data Masking** report.


  At the top of the report, you can view the number of values, sensitive types, tables, and columns that were masked.

  The table shows you column counts for the sensitive categories and types. For each sensitive column, you can view the masking format used and the number of rows masked.

  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047621/177413453.png" data-image-src="attachments/177047621/177413453.png" data-unresolved-comment-count="0" data-linked-resource-id="177413453" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-45-24.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">



- Click **Generate Report**.


  <img class="confluence-embedded-image confluence-content-image-border" height="153" width="413" src="attachments/177047621/177413454.png" data-image-src="attachments/177047621/177413454.png" data-unresolved-comment-count="0" data-linked-resource-id="177413454" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-46-1.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- In the **Generate Report** dialog box, leave **PDF** selected, enter **Mask1_HCM1** for the description, ensure your resource group is selected, and then click **Generate Report**.


  <img class="confluence-embedded-image confluence-content-image-border" height="278" width="595" src="attachments/177047621/177413455.png" data-image-src="attachments/177047621/177413455.png" data-unresolved-comment-count="0" data-linked-resource-id="177413455" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-46-24.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- Wait for the report to generate. When it's generated, click **Download Report**.


  <img class="confluence-embedded-image confluence-content-image-border" height="198" width="386" src="attachments/177047621/177413457.png" data-image-src="attachments/177047621/177413457.png" data-unresolved-comment-count="0" data-linked-resource-id="177413457" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-46-56.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- Access the browser's downloads and open the report in Adobe Acrobat. Review the report, and then close it.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047621/177413459.png" data-image-src="attachments/177047621/177413459.png" data-unresolved-comment-count="0" data-linked-resource-id="177413459" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-47-20.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  <h2 id="Lab105-DiscoverandMaskSensitiveDatainOracleDataSafe-STEP4:ValidatethemaskeddatainyourATPdatabase">**STEP 4**: Validate the masked data in your ATP database

- Return to the browser tab for **SQL Developer Web**. You should still have your query results from STEP 1 in this lab. Take a moment to review the data.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047621/177413460.png" data-image-src="attachments/177047621/177413460.png" data-unresolved-comment-count="0" data-linked-resource-id="177413460" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-47-49.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- On the toolbar, click the **Run Statement** button (green circle with a white arrow) to execute the query.


  <img class="confluence-embedded-image confluence-content-image-border" height="67" width="609" src="attachments/177047621/177413461.png" data-image-src="attachments/177047621/177413461.png" data-unresolved-comment-count="0" data-linked-resource-id="177413461" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-48-16.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- If a dialog box is displayed stating that your session has expired, click **OK**, sign in again, and then click the **Run Statement** button.


  <img class="confluence-embedded-image confluence-content-image-border" width="650" src="attachments/177047621/177413464.png" data-image-src="attachments/177047621/177413464.png" data-unresolved-comment-count="0" data-linked-resource-id="177413464" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-48-39.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">

  

- Review the masked data.


  You can resize the panel to view more data, and you can scroll down and to the right.

  <img class="confluence-embedded-image confluence-content-image-border" height="194" width="650" src="attachments/177047621/177413466.png" data-image-src="attachments/177047621/177413466.png" data-unresolved-comment-count="0" data-linked-resource-id="177413466" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-3_6-49-8.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="177047621" data-linked-resource-container-version="20">




 



