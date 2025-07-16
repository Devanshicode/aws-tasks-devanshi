# 🔐 Cloud Security Implementation on AWS

This project demonstrates how to implement cloud security best practices on Amazon Web Services (AWS), focusing on:

- IAM Policy Management (Least Privilege Access)
- Secure Amazon S3 Storage
- Data Encryption (SSE-S3)
- Bucket Policy Controls

> 🔗 **Live S3 Website (if hosted):**  
> http://my-multicloud-bucket01.s3-website.eu-north-1.amazonaws.com/

---

## 📌 Objectives

- Configure IAM user with restricted S3 access using custom policies.
- Secure S3 buckets by enabling server-side encryption and blocking public access.
- Test access using console and (optionally) CLI.
- Demonstrate understanding of cloud security controls.

---

## 📁 Bucket Details

| Bucket Name                 | Description                       | Security Applied     |
|----------------------------|-----------------------------------|----------------------|
| `devanshi-s3-demo-bucket`  | Test bucket for uploading files   | IAM + SSE-S3 + Block Public Access |
| `my-multicloud-bucket01`   | Static website hosting (index.html + syllabus PDF) | IAM + SSE-S3 + Block Public Access |

---

## 🔐 IAM Configuration

- **IAM User:** `secure-user`
- **Custom Policy:** `ReadOnlyAccessToMyBuckets`
- **Permissions Granted:**
  - List and read objects from both buckets
  - Denied from accessing other resources

```json
{
  "Effect": "Allow",
  "Action": ["s3:GetObject", "s3:ListBucket"],
  "Resource": [
    "arn:aws:s3:::devanshi-s3-demo-bucket",
    "arn:aws:s3:::devanshi-s3-demo-bucket/*",
    "arn:aws:s3:::my-multicloud-bucket01",
    "arn:aws:s3:::my-multicloud-bucket01/*"
  ]
}

