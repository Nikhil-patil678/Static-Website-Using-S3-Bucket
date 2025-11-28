#  Deploying a Static Webebsite Using Amazon S3

### This guide will help you deploy a static website ( HTML , CSS , JS ) using **Amazon S3** . Follow the steps carefully to host your website publicly .
---
## Prerequisites 
Before you begin , ensure you have :
- An **AWS Account** 
- AWS **IAM user** with S3 permissions
- Website files (HTML, CSS, js, images)
---
## Steps To Deploy

### Step 1 : Create An S3 Bucket 

1. Go to **AWS Console** -> **S3**

2. Click **Create Bucket**

3. Enter a unique bucket name (example : `static-22-b-bucket-s3`)

4. Choose your AWS Region

5. Click **Create Bucket**

![my image](./images/Screenshot%202025-11-28%20205430.png)

---

### Step 2 : Make The Bucket Public 

1.  **Disabled "Block Public Access"** 
    
    - Navigate to **Permissions** -> **Block Public Access** -> **Edit**

    - **Uncheck** all the ckeckbox to allow public access 

    - **Save Changes**

![my image](./images/Screenshot%202025-11-28%20210148.png)

2. **Enable ACLs**
 
     - Navigate to **Permissions** -> **Object Ownership** -> **Edit** 

     - Choose **ACLs enabled ( Access Control List )**

     - **Save Changes**  

![my image](./images/Screenshot%202025-11-28%20211250.png)

---

### Step 3 : Upload Website Files 

1. Open your bucket 

2. Click **Upload**

3. Add your files (`index.html` , CSS , images , etc.)

4. Click **Upload** 

![my image](./images/Screenshot%202025-11-28%20213010.png)

5.  After uploading , **select all objects -> Actions -> Make public using ACLs**

![my image](./images/Screenshot%202025-11-28%20213512.png)

---

### Step 4 : Enable Static Website Hosting 

1. Go to **Properties** Tab 

2. Scroll to **Static Website Hosting**

3. Click **Edit**

4. Enable Static Website Hosting 

5. Enter : 
    - **Index document** : `index.html`

6. Save Changes 

![my image](./images/Screenshot%202025-11-28%20214439.png)

---
### Step 5 : Access the Website 

- After enabling static hosting , an **endpoint URL** will be provided .

bash 

    http://static-22-b-bucket-s3.s3-website-us-east-1.amazonaws.com

- Copy that UPL 

- Open it any browser 

![my image](./images/Screenshot%202025-11-28%20215304.png)

![my image](./images/Screenshot%202025-11-28%20215321.png)

![my image](./images/Screenshot%202025-11-28%20215338.png)

---
---