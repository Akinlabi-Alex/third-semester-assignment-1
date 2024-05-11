# HOSTING A STATIC WEBSITE USING AWS S3 BUCKET AND CLOUDFRONT

 ![images](./images/Web%20Hosting.png)
 
## Overview
This guide outlines the steps to host a static website on AWS S3 bucket and accelerate its delivery using Amazon CloudFront content delivery network (CDN).
## Prerequisites
Before getting started, ensure you have the following:

     -An AWS account
     -The AWS CLI configured on your local machine
     -A static website ready to be hosted
 
## Steps

 ## Creating S3 Bucket  
![images](./images/s3bu%20copy.PNG)

     -On the search menu, type S3 
     -Enter any bucket name of your choice e.g alex-buc 

![images](./images/s3bu%20ii.PNG)

     -Click create bucket  
     -Open the bucket you created

 ## Uploading Files and Folders
 ![images](./images/upl%20copy.PNG)

     -Go to your file manager and upload your file and folder or wherever you saved your files and folders


## Enabling static website hosting
     -Open the bucket you created 
     -Click on properties

![images](./images/por.PNG) 

     -Scroll down and edit static webite hosting
     -At first, it will be disabled

![images](./images/dis.PNG)

     -Enable it

![images](./images/ena.PNG)   

     -Save and exit

## Creating CloudFront Distribution
![images](./images/s3bu%20copy.PNG)
    
     -On the search menu type in cloudfront and create a new distribution

![images](./images/cre%20clou.PNG)

     -Enter your bucket details in the origin      

![images](./images/ori%20cloud.PNG)
    
     -Edit the origin access from public 
     -Click on origin access control settings
     -Create a new origin access control, leave it as default

![images](./images/clou%20access.PNG)  

     -Scroll down and Enable security protection

![images](./images/waf.PNG)     

     -Type index.html under the index document

  ![images](./images/in.ht.PNG)   

    -Click on create distribution (It will take few seconds to deploy)

![images](./images/copy%20policy%20-.PNG) 

     -Copy this policy and paste it inside the bucket policy. To do these;
         -click on bucket you created after copying the policy, 
         -go to your file permission 

![images](./images/per.PNG) 


         -edit the bucket policy and paste 

     -Paste it here and save click save

![images](./images/bucpoli.PNG)

     -Go back to your cloudFront and copy the distribution domain name

![images](./images/domain%20-.PNG)


## Testing

     -Paste the distribution domain name on a new webpage
     -Here is the result after running it successfully

![images](./images/test.PNG)

   
     With the following steps, I have successfully hosted a static website on AWS S3 bucket and accelerated its delivery using Amazon CloudFront. This website is now highly available and scalable.
