

# 🚀 **Task 1: Create AWS Transfer Family Web App & Assign User**

---

## 🗂️ **Outline**
In this task, you will:
- Create a **Transfer Family Web App**
- Connect it with **IAM Identity Center**
- Assign a **user** to the web app

---

## 🕐 **Time to Complete**
~ 5 minutes

---

## 📋 **Pre-requisites**
- ✅ AWS Account
- ✅ IAM Identity Center already set up (Instance ARN noted)
- ✅ IAM Identity Center user already created (from previous setup)

---

## 🧭 **Step-by-Step Navigation**

---

### 🔹 **Step 1: Go to IAM Identity Center**
- Open **AWS Console**
- Search for `IAM Identity Center`
- ✅ Make sure you’re in the correct AWS **Region**

![](https://i.postimg.cc/gkHm2dqm/01.png)

![](https://i.postimg.cc/Vk7wXRVh/02-AWS-Region.png)


- Go to **Settings**  
  → **Note down the `Instance ARN`** (you’ll need this later)

![](https://i.postimg.cc/VLmPTpyT/03-ARN-IAM.png)

---

### 🔹 **Step 2: Create Web App in AWS Transfer Family**
- In AWS Console, search **“AWS Transfer Family”**
- In the left panel, select **Web apps**
- Click **Create web app**

![](https://i.postimg.cc/LsqcLMfq/04-AWS-Transfer-Family.png)

---

### 🔹 **Step 3: Configure Web App Settings**

- ✅ **Authentication Access**  
  - Make sure **IAM Identity Center** is selected

  ![](https://i.postimg.cc/85MxXBZN/06-Config-Web-App.png)

    ![](https://i.postimg.cc/RZnFC2FR/07-Created.png)

  - For **Permission type**: select `Create and use a new service role`  
  - For **Web app units**: set `1` (this allows up to 250 concurrent sessions)

---

### 🔹 **Step 4: Add Tags (Optional but Recommended)**
- Click **Add tag**
  - Key: `Name`  
  - Value: `Transfer Family web app demo`

Click **Next**

---

### 🔹 **Step 5: Design Web App**
- **Page title**: `AWS Transfer Family Web App Demo`
- (Optional) Upload your logo
- Click **Next**

---

### 🔹 **Step 6: Review & Create**
- Review the settings
- Click **Create web app**

---

### 🔹 **Step 7: Assign User to Web App**
- Once the web app is created, click **Add user**

- Choose **Assign users and groups**
- Select **Assign existing users and groups**
- Click **Next**

![](https://i.postimg.cc/GmfNcSNb/01-Assign.png)

---

### 🔹 **Step 8: Select Your IAM Identity Center User**
- A pop-up will open
- Search for your **IAM Identity Center user**
- Select the user → Click **Assign**

![](https://i.postimg.cc/G2xqsMM8/02-user.png)

📌 To confirm the correct user:
- Go to **IAM Identity Center**
- Click **Users** tab → Verify username

---

### 🔹 **Step 9: Copy Important Values**
- After assigning user:
  - Go to **Web app details** pane
  - ✅ Copy the `Instance ARN` (you’ll need it for CORS setup)
  - ✅ Go to **Users** tab → Copy the **User ID**

![](https://i.postimg.cc/YSc3DcZL/03-Data.png)

---

## ✅ **Conclusion**
You’ve successfully:
- Created an AWS Transfer Family Web App
- Integrated with IAM Identity Center
- Assigned your Identity Center user to the app
- Collected `Instance ARN` and `User ID` for next steps
