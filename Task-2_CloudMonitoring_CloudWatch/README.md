# Task 2: Cloud Monitoring with AWS CloudWatch

## 🎯 Objective
To set up monitoring for a cloud-based application using AWS CloudWatch, including metrics dashboard and alert configuration.

---

## 🛠️ Tools Used
- AWS EC2 (t2.micro)
- AWS CloudWatch (Monitoring + Alarm)
- SNS (for alert notification)

---

## ✅ Steps Performed

1. Launched a new EC2 instance (Amazon Linux 2, t2.micro)
2. Enabled CloudWatch default monitoring (5-minute intervals)
3. Created a new CloudWatch dashboard named `CloudAppMonitoring`
   - Added metrics: CPUUtilization, NetworkIn, NetworkOut
4. Created a CloudWatch alarm:
   - Metric: CPUUtilization
   - Condition: Greater than 70%
   - Notification: SNS Topic with my email
5. Confirmed SNS subscription via email

---

## 📸 Screenshots

| Screenshot | Description |
|------------|-------------|
| `ec2-instance.png` | Running EC2 instance |
| `cloudwatch-dashboard.png` | Custom dashboard showing metrics |
| `alarm-config.png` | Alarm threshold and SNS setup |

All screenshots are available in the `screenshots/` folder.

---

## 🧾 Outcome
- Successfully monitored the EC2 instance
- Created a working alarm and received email alert
- Dashboard shows real-time EC2 metrics

---

## 📂 Folder Structure


