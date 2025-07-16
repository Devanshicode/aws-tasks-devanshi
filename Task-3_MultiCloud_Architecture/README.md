# 🌐 Multi-Cloud Architecture Project

This project demonstrates a **Multi-Cloud Architecture** where services and files are distributed across two cloud providers: **AWS (Amazon Web Services)** and **Google Cloud (via Google Drive)**.

> ✅ Live Site:  
> **[http://my-multicloud-bucket01.s3-website.eu-north-1.amazonaws.com/](http://my-multicloud-bucket01.s3-website.eu-north-1.amazonaws.com/)**

---

## 📄 Project Description

This is a static HTML-based website hosted on an **AWS S3 bucket**. It includes:

- A public **PDF file** hosted on S3: `CYBER SECURITY SYLLABUS.pdf`
- A secondary link to the same file hosted on **Google Drive**
- Clean, minimal HTML for easy access and demonstration

---

## 🔗 Resources Linked in the Project

### 🟦 1. AWS S3-hosted File
- [📄 CYBER SECURITY SYLLABUS (S3)](http://my-multicloud-bucket01.s3-website.eu-north-1.amazonaws.com/CYBER%20SECURITY%20SYLLABUS.pdf)

### 🟨 2. Google Drive-hosted File
- [🔗 CYBER SECURITY SYLLABUS (Google Drive)](https://drive.google.com/file/d/10ycESTh2aV3fziISBCoaJhNH71Q2NCAS/view?usp=sharing)

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| **AWS S3** | Hosting static HTML website and PDF |
| **HTML**   | Markup for the static site |
| **Google Drive** | External cloud file hosting |
| **Public Bucket Policy** | To enable file access via URL |

---

## 🌍 Deployment Steps (AWS S3)

1. **Create S3 Bucket**
   - Name: `my-multicloud-bucket01`
   - Region: `eu-north-1`
   - Disable block public access

2. **Upload Files**
   - `index.html`
   - `CYBER SECURITY SYLLABUS.pdf`

3. **Enable Static Website Hosting**
   - Index document: `index.html`

4. **Set Permissions**
   - Make both files public
   - Add bucket policy:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadAccess",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::my-multicloud-bucket01/*"
    }
  ]
}

