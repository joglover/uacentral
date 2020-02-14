# Lab 101 - View a Registered Target Database in Oracle Data Safe



- <a href='#Lab101-ViewaRegisteredTargetDatabaseinOracleDataSafe-BeforeYouBegin'>Before You Begin</a>

- <a href='#Lab101-ViewaRegisteredTargetDatabaseinOracleDataSafe-STEP1:SignintotheOracleDataSafeConsoleDirectly'>STEP 1: Sign in to the Oracle Data Safe Console Directly</a>

- <a href='#Lab101-ViewaRegisteredTargetDatabaseinOracleDataSafe-STEP2(Optional):SignintotheOracleDataSafeConsolethroughtheOracleCloudInfrastructureConsole'>STEP 2 (Optional): Sign in to the Oracle Data Safe Console through the Oracle Cloud Infrastructure Console</a>

- <a href='#Lab101-ViewaRegisteredTargetDatabaseinOracleDataSafe-STEP3:ViewtheOracleDataSafeDashboard'>STEP 3: View the Oracle Data Safe Dashboard</a>

- <a href='#Lab101-ViewaRegisteredTargetDatabaseinOracleDataSafe-STEP4:ViewdetailsforaregisteredtargetdatabaseinOracleDataSafe'>STEP 4: View details for a registered target database in Oracle Data Safe</a>





<h2 id="Lab101-ViewaRegisteredTargetDatabaseinOracleDataSafe-BeforeYouBegin">Before You Begin


### Objectives

In this lab, you learn how to do the following:

- Sign in to the Oracle Data Safe Console either directly or through the Oracle Cloud Infrastructure Console
- View the Oracle Data Safe dashboard
- View details for a registered target database in Oracle Data Safe



### Requirements

To complete this lab, you need to have the following:

- Login credentials for your tenancy in Oracle Cloud Infrastructure
- An Oracle Data Safe service enabled in a region of your tenancy
- A registered target database in Oracle Data Safe
<h2 id="Lab101-ViewaRegisteredTargetDatabaseinOracleDataSafe-STEP1:SignintotheOracleDataSafeConsoleDirectly">**STEP 1**: Sign in to the Oracle Data Safe Console Directly

This step shows you how to access the Oracle Data Safe Console directly without having to go through the Oracle Cloud Infrastructure Console. Alternatively, you can follow step 2 below to access the Oracle Data Safe Console through the Oracle Cloud Infrastructure Console.

- From any browser, enter the url to the Oracle Data Safe Console for your region.


   The url for the Ashburn region is as follows:<a href="https://datasafe.us-ashburn-1.oci.oraclecloud.com/ui/index.html" class="external-link" rel="nofollow"> https://datasafe.us-ashburn-1.oci.oraclecloud.com/ui/index.html</a>.

  The url for the Frankfurt region is as follows:<a href="https://datasafe.eu-frankfurt-1.oci.oraclecloud.com/ui/index.html" class="external-link" rel="nofollow"> https://datasafe.eu-frankfurt-1.oci.oraclecloud.com/ui/index.html.</a>

  

- In the Cloud Tenant field on the **SIGN IN** page, enter your tenancy name, and then click **Continue**.


  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="421" src="attachments/175001807/177407918.png" data-image-src="attachments/175001807/177407918.png" data-unresolved-comment-count="0" data-linked-resource-id="177407918" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-2_14-57-46.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="175001807" data-linked-resource-container-version="82">



- Under Oracle Cloud Infrastructure, enter your user credentials for Oracle Cloud Infrastructure, and then click **Sign In**. Be sure to use the correct user name, which is similar to <code>dsu100</code>. Please do not change your password.


  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="516" src="attachments/175001807/177407946.png" data-image-src="attachments/175001807/177407946.png" data-unresolved-comment-count="0" data-linked-resource-id="177407946" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-2_15-0-57.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="175001807" data-linked-resource-container-version="82"><h2 id="Lab101-ViewaRegisteredTargetDatabaseinOracleDataSafe-STEP2(Optional):SignintotheOracleDataSafeConsolethroughtheOracleCloudInfrastructureConsole">**STEP 2 (Optional)**: Sign in to the Oracle Data Safe Console through the Oracle Cloud Infrastructure Console

This step shows you how to access the Oracle Data Safe Console by starting in the Oracle Cloud Infrastructure Console. If you completed step 1, you can skip this step and continue on to step 3.

- In a browser window, enter the url to the Oracle Cloud Infrastructure Console.


  For example, the url for the Ashburn region is as follows: <a href="https://console.us-ashburn-1.oraclecloud.com/a/tenancy" class="external-link" rel="nofollow">https://console.us-ashburn-1.oraclecloud.com</a>.

  The url for the Frankfurt region is as follows: <a href="https://console.eu-frankfurt-1.oraclecloud.com/a/tenancy" class="external-link" rel="nofollow">https://console.eu-frankfurt-1.oraclecloud.com</a><a href="https://datasafe.eu-frankfurt-1.oci.oraclecloud.com/ui/index.html" class="external-link" rel="nofollow">.</a>

  

- In the Cloud Tenant field on the **SIGN IN** page, enter your tenancy name, and then click **Continue**.


  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="421" src="attachments/175001807/177407918.png" data-image-src="attachments/175001807/177407918.png" data-unresolved-comment-count="0" data-linked-resource-id="177407918" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-2_14-57-46.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="175001807" data-linked-resource-container-version="82">

  

- Under **Oracle Cloud Infrastructure**, enter your user credentials for Oracle Cloud Infrastructure, and then click **Sign In**.


  Be sure to use the correct user name, which is similar to <code>dsu100</code>.

  Please do not change your password.

  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="516" src="attachments/175001807/177407946.png" data-image-src="attachments/175001807/177407946.png" data-unresolved-comment-count="0" data-linked-resource-id="177407946" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-2_15-0-57.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="175001807" data-linked-resource-container-version="82">

  

- From the navigation menu in Oracle Cloud Infrastructure, select **Data Safe**.


  <img class="confluence-embedded-image confluence-content-image-border" height="400" src="attachments/175001807/177407990.png" data-image-src="attachments/175001807/177407990.png" data-unresolved-comment-count="0" data-linked-resource-id="177407990" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-2_15-7-12.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="175001807" data-linked-resource-container-version="82">

  

- On the **Data Safe** page, view the list of databases that are registered with Oracle Data Safe.


  <img class="confluence-embedded-image confluence-content-image-border" height="150" src="attachments/175001807/177407984.png" data-image-src="attachments/175001807/177407984.png" data-unresolved-comment-count="0" data-linked-resource-id="177407984" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-2_15-6-38.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="175001807" data-linked-resource-container-version="82">



- Click **Service Console** to access the Oracle Data Safe Console.


  Each student uses his or her own database.

  Your database corresponds to your user name. For example, user <code>dsu01</code> uses the ATP database named <code>dsatp01</code>.

  

- On the **SIGN IN** page under Oracle Cloud Infrastructure, enter your user name and password again, and then click **Sign In**.


  Be sure to use the correct user name, which is similar to <code>dsu<number></code> (for example, <code>dsu01</code>), and do not use the Single Sign-On (SSO) option.

  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="516" src="attachments/175001807/177407946.png" data-image-src="attachments/175001807/177407946.png" data-unresolved-comment-count="0" data-linked-resource-id="177407946" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-2_15-0-57.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="175001807" data-linked-resource-container-version="82">

  

- Bookmark the page so that if you need to sign in again, you can navigate directly to the Oracle Data Safe **SIGN IN** page.


<h2 id="Lab101-ViewaRegisteredTargetDatabaseinOracleDataSafe-STEP3:ViewtheOracleDataSafeDashboard">**STEP 3**: View the Oracle Data Safe Dashboard

- Notice that when you sign in to Oracle Data Safe, you are presented with a dashboard on the **Home** tab.


  The dashboard lets you monitor several activities at once.

  When you first sign in, the charts in your dashboard may not contain data because you have not yet used the features.

  <img class="confluence-embedded-image confluence-content-image-border" height="400" width="595" src="attachments/175001807/175010698.png" data-image-src="attachments/175001807/175010698.png" data-unresolved-comment-count="0" data-linked-resource-id="175010698" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-11-27_13-8-32.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="175001807" data-linked-resource-container-version="82">

  

- View the top tabs.


  They provide quick access to the dashboard (**Home** tab), registered target databases (**Targets** tab), the Oracle Data Safe Library (**Library** tab), reports for all Oracle Data Safe features (**Reports** tab), all of the alerts (**Alerts** tab), and all of the current and scheduled jobs (**Jobs** tab).

  <img class="confluence-embedded-image confluence-content-image-border" height="150" width="630" src="attachments/175001807/175010721.png" data-image-src="attachments/175001807/175010721.png" data-unresolved-comment-count="0" data-linked-resource-id="175010721" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-11-27_13-9-30.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="175001807" data-linked-resource-container-version="82">

  

- View the side tabs. They provide quick access to Oracle Data Safe's main features, including **Security Assessment**, **User Assessment**, **Data Discovery**, **Data Masking**, and **Activity Auditing**.


  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="242" src="attachments/175001807/175010733.png" data-image-src="attachments/175001807/175010733.png" data-unresolved-comment-count="0" data-linked-resource-id="175010733" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-11-27_13-10-10.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="175001807" data-linked-resource-container-version="82">

  <h2 id="Lab101-ViewaRegisteredTargetDatabaseinOracleDataSafe-STEP4:ViewdetailsforaregisteredtargetdatabaseinOracleDataSafe">**STEP 4**: View details for a registered target database in Oracle Data Safe

- Click the **Targets** tab.


  Notice that there is only one target database to which you have access.

  An Oracle Data Safe administrator configured an authorization policy in Oracle Data Safe to grant you access to the resource group that contains your database.

  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="649" src="attachments/175001807/175010785.png" data-image-src="attachments/175001807/175010785.png" data-unresolved-comment-count="0" data-linked-resource-id="175010785" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-11-27_13-12-46.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="175001807" data-linked-resource-container-version="82">

  

- Click the name of your target database.


  <img class="confluence-embedded-image confluence-content-image-border" height="250" width="751" src="attachments/175001807/177408050.png" data-image-src="attachments/175001807/177408050.png" data-unresolved-comment-count="0" data-linked-resource-id="177408050" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-2_15-15-31.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="175001807" data-linked-resource-container-version="82">

  

- Review the details for your target database.


  Your database is an Autonomous Transaction Processing (ATP) database. It was automatically added to the <code>dscrg01</code> resource group during target registration.

  An Oracle Data Safe administrator registered your Autonomous Database through the Autonomous Transaction Processing (ATP) Console.

  <img class="confluence-embedded-image confluence-content-image-border" height="400" width="299" src="attachments/175001807/177408053.png" data-image-src="attachments/175001807/177408053.png" data-unresolved-comment-count="0" data-linked-resource-id="177408053" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2019-12-2_15-16-8.png" data-base-url="https://confluence.oci.oraclecorp.com" data-linked-resource-content-type="image/png" data-linked-resource-container-id="175001807" data-linked-resource-container-version="82">

  

- Click **Cancel** to close the **Target Details** dialog box.







 



