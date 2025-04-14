# ✅ **Task 4: Access Web App, Create Folder & Upload Sample File**

---

## 🗂️ **Outline**
Use your **IAM Identity Center user** to log into the **AWS Transfer Family Web App**, create a folder, and upload a sample file.

---

## 🧭 **Step-by-Step Navigation**

---

### 🔹 **Step 1: Open AWS Transfer Family Console**
- Go to AWS Console
- In the **left panel**, choose **Web apps**
- Find your app → `Transfer Family web app demo`
- Click on the **Access endpoint**  
  → URL format: `https://webapp-xxxxx.transfer-webapp.<region>.on.aws`


  ![](https://i.postimg.cc/prDCtsjX/01.png)

---

### 🔹 **Step 2: Sign In with Your IAM Identity Center User**

![](https://i.postimg.cc/3JF1Sb7t/02.png)

- Username: Enter your **user name**  
  (Same one you created in IAM Identity Center)
- Click **Next**
- Password: Enter your **user password**
- Click **Sign in**

➡️ You should now land on your **web app’s home page** 🎉

![](https://i.postimg.cc/Z5fcZBW3/03-Main.png)

---

## 📁 **Folder Creation and File Upload**

---

### 🔹 **Step 3: Create Folder**
- In the **web app interface**, find the option to **Create folder**
- Enter any name for the folder (e.g., `demo-folder`)
- Click **Create folder**

![](https://i.postimg.cc/DzHPJ9dw/04-Create-Folder.png)

---

### 🔹 **Step 4: Upload File**
- Enter the folder you just created
- Click on **Add files**
- Select a sample file from your local machine (e.g., `.txt`, `.jpg`, etc.)
- Click **Upload**

![](https://i.postimg.cc/T1XjQns8/07.png)

---

### 🔹 **Step 5: Verify in S3 Bucket**
- Go to AWS Console → Open **Amazon S3**
- Search for your bucket: `transfer-family-web-app-demo-<your-username>`
- Navigate to the folder you created → confirm the file is uploaded

![](https://i.postimg.cc/ZnF8QCkW/08.png)

✅ You’ll see the file with correct timestamp and metadata

---

## 🏁 **Conclusion**
You have:
- ✅ Logged in to AWS Transfer Family Web App as your Identity Center user
- ✅ Created a folder inside the web interface
- ✅ Uploaded a sample file
- ✅ Verified file upload in S3 bucket

