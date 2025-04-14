

# ✅ **Task 2: Create S3 Bucket & Set Up CORS for Transfer Family Web App**

---

## 🗂️ **Outline**
Create a new S3 bucket to store user data and configure CORS so that your web app can interact with this bucket securely across domains.

---

## ❓ **Objective**
- Create a unique Amazon S3 bucket  
- Add CORS policy using your web app's **Instance ARN**

---

## 🧭 **Step-by-Step Navigation**

---

### 🔹 **Step 1: Go to Amazon S3 Console**
- Open **AWS Console**
- In the **Search bar**, type: `S3`
- Click on **Amazon S3**

---

### 🔹 **Step 2: Create Bucket**

![](https://i.postimg.cc/C5WBM0jj/01-Bucket-Creation.png)

- Click **Create bucket**
- For **Bucket name**, use a globally unique name like:  
  `transfer-family-web-app-demo-<your-username>`

  ![](https://i.postimg.cc/RFTxVLKG/02-bucker.png)

- Leave remaining settings as default
- Scroll to bottom → Click **Create bucket**

---

### 🔹 **Step 3: Open Bucket Permissions**
- After creation:
  - Go to **General purpose buckets**
  - Search and click your **bucket name**
- Navigate to the **Permissions tab**

---

### 🔹 **Step 4: Configure CORS Policy**
- Scroll to the **Cross-origin resource sharing (CORS)** section
- Click **Edit**
- Paste the following JSON config 👇

#### 🔧 Replace `"AccessEndpoint"` with your actual **Instance ARN**
```json
[
  {
    "AllowedHeaders": [
      "*"
    ],
    "AllowedMethods": [
      "GET",
      "PUT",
      "POST",
      "DELETE",
      "HEAD"
    ],
    "AllowedOrigins": [
      "https://webapp-<your-instance-id>.transfer-webapp.<region>.on.aws"
    ],
    "ExposeHeaders": [
      "last-modified",
      "content-length",
      "etag",
      "x-amz-version-id",
      "content-type",
      "x-amz-request-id",
      "x-amz-id-2",
      "date",
      "x-amz-cf-id",
      "x-amz-storage-class",
      "access-control-expose-headers"
    ],
    "MaxAgeSeconds": 3000
  }
]
```


![](https://i.postimg.cc/yYxCs9dX/04-CORS.png)

> ⚠️ **Important**:  
> ❌ Don’t use a trailing slash at the end of your URL.  
> ✅ Correct: `https://webapp-xxxx.transfer-webapp.us-west-2.on.aws`  
> ❌ Wrong: `https://webapp-xxxx.transfer-webapp.us-west-2.on.aws/`

---

### 🔹 **Step 5: Save the CORS Policy**
- After editing, click **Save changes**

---

## 🏁 **Conclusion**
You’ve successfully:
- ✅ Created an S3 bucket  
- ✅ Set up a CORS policy with your web app's access endpoint (Instance ARN)

---



