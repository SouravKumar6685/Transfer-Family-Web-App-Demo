# 🚀 AWS Transfer Family Web App Demo

## 📌 Project Definition

This project demonstrates how to build a **secure, user-authenticated file transfer portal** using **AWS Transfer Family**, **Amazon S3**, **IAM Identity Center**, and **S3 Access Grants**. 

It provides an end-to-end flow for:
- Creating a branded file transfer web application
- Managing user access securely via AWS IAM Identity Center
- Allowing users to upload/download files from S3 buckets
- Ensuring fine-grained access control with S3 Access Grants
- Enabling safe cross-origin resource sharing (CORS)

---

## ✅ Why Use AWS Transfer Family Web App?

- **No infrastructure management**: Fully managed by AWS — no need to build, deploy, or host custom file transfer servers.
- **Secure authentication**: Integrated with IAM Identity Center for enterprise-grade security.
- **Granular data access**: Uses S3 Access Grants for precise control over what users can access.
- **Branded experience**: Allows customization of web interface and logo.
- **Seamless S3 integration**: Direct access to S3 buckets for file storage, access, and management.

---

## 🌍 Real-World Use Cases

- 📁 **Enterprise file exchange portals**  
  Share files securely with clients or internal teams without writing custom backend code.

- 🏥 **Healthcare or Legal data sharing**  
  Where fine-grained access control and audit logging are critical.

- 🧑‍💼 **User-based onboarding**  
  Let partners, vendors, or employees upload documents securely through a web app.

- 🏢 **SaaS Platforms**  
  Offering file hosting as part of larger workflow or management applications.

---

## 🛠️ Project Phases

### Phase 1: Create Web App and Assign User
- Configure AWS Transfer Family Web App
- Connect with IAM Identity Center
- Assign a user to the app

### Phase 2: Create Amazon S3 Bucket and Setup CORS
- Create a globally unique S3 bucket
- Set CORS rules with the correct access endpoint

### Phase 3: Configure S3 Access Grants
- Create an S3 Access Grants instance
- Register S3 bucket location
- Grant access to the IAM Identity Center user

### Phase 4: Upload Files from Web App
- Login to Transfer Web App
- Create folder and upload files
- Verify upload in S3

### Phase 5: Cleanup Resources
- Delete web app
- Remove S3 Access Grants
- (Optional) Delete S3 bucket

---

## 📎 Notes

- Bucket names must be **globally unique**
- Use **correct Instance ARN** (from IAM Identity Center, not Web App ARN) for CORS
- Web App supports up to **250 concurrent sessions**


