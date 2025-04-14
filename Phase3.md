# ✅ **Task 3: Create S3 Access Grants Instance & Set Up Bucket Access**

---

## 🗂️ **Outline**
You’ll create an **S3 Access Grants instance**, register your S3 bucket, and grant **your IAM Identity Center user** read/write access.

---

## ❓ **Objective**
- Create Access Grants instance
- Register S3 bucket location
- Grant access to Identity Center user

---

## 🧭 **Step-by-Step Navigation**

---

### 🔹 **Step 1: Open S3 Access Grants Console**
- Go to AWS Console
- Search for **S3 Access Grants**
- Click on **Create S3 Access Grants instance**


![](https://i.postimg.cc/sDvqtr6T/01-Access-Grant.png)

---

### 🔹 **Step 2: Add IAM Identity Center ARN**
- Click **Add IAM Identity Center instance**
- Paste the **Instance ARN** from Task 1:  
  (Looks like `arn:aws:sso:::8`)
- Click **Next**

![](https://i.postimg.cc/ydLpbQFq/03-Blur-it.png)

![](https://i.postimg.cc/xTJp6P87/04-Blur-it.png)

➡️ This creates an **Access Grants Instance** behind the scenes

- Click **Cancel** afterward to simplify creation process  
  (✅ Instance has been created already)

---

## 🪣 **Register the S3 Bucket Location**

---

### 🔹 **Step 3: Go to "Locations" Tab**
- Click on the **Locations** tab
- Click **Register location**

![](https://i.postimg.cc/1t3JwGbv/05-Location.png)


---

### 🔹 **Step 4: Configure Location**

![](https://i.postimg.cc/VvSgHYfM/06-Scope.png)

- **Scope**: Click **Browse**, select your **S3 bucket**  
  → This fills in something like: `s3://transfer-family-web-app-demo-xyz`
- **IAM Role**: Click **Create new role**  
  → This lets S3 Access Grants access this location


- Click **Register location**

---

## 🎯 **Create Access Grant for the User**

---

![](https://i.postimg.cc/59HDrJkn/Create-Grants.png)

### 🔹 **Step 5: Create Grant**
- Click **Create Grant**

#### Grant Form:

| Field                       | Value                                                                 |
|----------------------------|-----------------------------------------------------------------------|
| **Location**               | Click **Browse locations** → Select the one you just registered      |
| **Path > Subprefix**       | `*` (This gives access to entire bucket)                             |
| **Permissions**            | Select: ✅ Read and ✅ Write                                           |
| **Grantee type**           | `Directory identity from IAM Identity Center`                        |
| **Directory identity type**| `User`                                                                |
| **IAM Identity Center user ID** | Paste the **User ID** copied from Task 1                         |


![](  ![](https://i.postimg.cc/kXbwQXhP/07-Permi.png)

  ![](https://i.postimg.cc/qqCcxjwx/10-gg.png)
)

- Click **Create Grant**

