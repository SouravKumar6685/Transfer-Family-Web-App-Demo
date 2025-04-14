# 🧹 **Task 5: Clean Up All AWS Resources**

---

## 🗂️ **Outline**
You’ll delete the following resources:
- AWS Transfer Family Web App
- S3 Access Grants instance
- S3 Access Grants Location
- (Optional) S3 Bucket

---

## 🧭 **Step-by-Step Cleanup Guide**

---

### 🔹 **Step 1: Delete Transfer Family Web App**



- Open **AWS Console**
- Go to **AWS Transfer Family**
- In the left panel, click **Web apps**
- Select your app: `AWS Transfer Family web app demo`
- Click **Actions** → **Delete**

![](https://i.postimg.cc/CxKGvhcK/01-clean-Up.png)

- In the confirmation prompt, **type** `delete`
- Click **Confirm**

---

### 🔹 **Step 2: Delete S3 Access Grants Instance**
- Open the **S3 Access Grants** console
- Click **View details** next to your instance
- Click **Delete** 

![](https://i.postimg.cc/hvgxVcJc/02-s3-grant.png)

  → Confirms deletion of your **Access Grants instance**

---

### 🔹 **Step 3: Deregister Location**
- Still inside **S3 Access Grants**
- Go to the **Locations** tab
- Select your registered **location** (S3 bucket path)
- Click **Deregister**

✅ This removes the association between your access grants instance and the S3 bucket

---

### 🔹 **Step 4: (Optional) Delete the S3 Bucket**
- Open **Amazon S3** console
- Search for your bucket name (e.g., `transfer-family-web-app-demo-yourname`)
- Click on the bucket
- Choose **Delete**
- Type the **bucket name** to confirm deletion

![](https://i.postimg.cc/TYdgw2Mc/03-Deregister.png)

![](https://i.postimg.cc/vH096RGw/04.png)

---

## ✅ **Conclusion**
You have successfully deleted:
- ✅ AWS Transfer Family web app
- ✅ S3 Access Grants instance
- ✅ Deregistered location
- ✅ (Optional) S3 bucket

---

## 📌 Pro Tip:
Always clean up unused AWS resources to avoid being charged. AWS bills are pay-as-you-go — anything active **can incur costs**.

