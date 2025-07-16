# Task 1 – AWS S3 Cloud Storage Setup

## ✅ Bucket Details
- **Bucket Name**: `devanshi-s3-demo-bucket`
- **Region**: `Europe (Stockholm)` (`eu-north-1`)
- **Storage Class**: General Purpose
- **Versioning**: Disabled
- **Encryption**: SSE-S3 (Default)
- **Block Public Access**: Disabled

## 📂 Files Uploaded
- `unit1.pptx'

## 🔓 Access Configuration
- **Bucket Policy**:
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadForAllObjects",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::devanshi-s3-demo-bucket/*"
    }
  ]
}
