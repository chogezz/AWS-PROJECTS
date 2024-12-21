**HOSTING A STATIC WEBSITE ON AWS S3**
---

*Intro*
---
In this project,I host a Static Website on AWS S3.AWS S3 offers high availability and cost-effectiveness and to add on it since its a simple project,the use of AWS Free Tier is also an option

---

*Steps*
---
1.Launch AWS Console

Launch the AWS Console and search for "S3" and open when it appears

2.Create a Bucket

Click on "Create bucket." 

Provide a unique "Bucket name" for your website.

3.Configure Bucket Settings

Unselect "Block all public access" to allow internet users to access your website.

Click on "Create bucket" at the bottom.

4.Select Your Bucket

Once created, select your bucket from the list.

5.Configure Static Web Hosting

Under the "Properties" tab, scroll down to "Static web hosting" and click on "Edit."

Click on "Enable" and select "Host a static website." Choose the default home page (index document) for your site.

6.Set Up Error Handling (Optional)

Enter the names of the index document and error document (if needed), then click "Save changes."

7.Endpoint Creation

When "Static website hosting" is enabled, the bucket endpoint is created.

8.Bucket Policy for File Access

Create a bucket policy to enable access to the files.
Navigate to the "Permissions" tab and under the "Bucket policy" section, enter the provided policy, ensuring to change the Resource to your bucket's ARN followed by "/*".

9.Upload Your Website

Create and upload your website files, including the "index.html" file as specified in step 8.

10.Final Configuration

Navigate to the "Properties" tab and load the bucket's endpoint. The "index.html" file will serve as the home page.
In case of an error (e.g., the index file is not available), the "error.html" page will be returned at the endpoint.

---
