# AWS Static Web Hosting S3
This project demonstrates how to host a static website using AWS S3.

## Steps

- Login to your AWS account
- Search S3 in search bar > Click on Services > Buckets

![Step 1](https://github.com/Zayan9484/AWS-Projects/blob/main/AWS%20Static%20Web%20Hosting/images/AWS-1.png?raw=true)

- Create a bucket.
- Give it a name, scroll down and click on Create bucket. The bucket will be created.
- Click on your bucket & upload files i.e., web file
 
- After upload, click on the uploaded file name and it will open a page like this where you can see the URL of your web under Object URL.
 
When you copy and paste this URL in your browser, it will give your error message like this.
 
*To resolve this, we have to enable Static Web Hosting and some permissions*

- Go to your bucket and click on Properties.
- Scroll and enable Static Web Hosting by clicking on Edit.
- Enable it, write the name of your web file (like index.html) & save changes.
- Now to make it publicly accessible, go to the Permissions tab of your bucket.
- Click on edit Block Public Access and “uncheck block all public access”
- Now, we need to make it public via ACL (Access Control List).
- Scroll after saving changes and edit Object Ownership.
- Save changes.

- Now open your **bucket > Select it > Actions > Make public using ACL > Make Public**
 
- Now refresh that web URL that was giving error.

- Your website will be loaded.
 


