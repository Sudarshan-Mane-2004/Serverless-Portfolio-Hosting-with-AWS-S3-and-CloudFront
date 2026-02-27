# 🌐 Serverless Portfolio Hosting with AWS S3 and CloudFront

## 📌 Project Title

**Serverless Portfolio Hosting with AWS S3 and CloudFront**

---

## 🎯 Aim

Host a static website on AWS using a fully serverless, highly available, secure, and low-cost architecture.

---

## 🏁 Final Aim (Project Outcome)

By completing this project, we achieve:

* Deployment of a static website without managing servers
* Global content delivery with low latency
* HTTPS-enabled secure access
* Highly durable and scalable hosting
* Cost-optimized architecture using managed AWS services

This architecture demonstrates real-world cloud hosting best practices used in production environments.

---

## 🔄 Project Flow

**User → CloudFront (CDN) → S3 Bucket → Website Files**

### Flow Explanation

1. User opens the website URL
2. Request reaches nearest CloudFront edge location
3. CloudFront checks cache
4. If not cached, CloudFront fetches content from S3
5. Static files are returned to the user

---

## ❓ Why Each Service is Used

### 🪣 Amazon S3

* Stores static website files
* Highly durable and cost-effective
* Fully serverless storage
* Easy static website hosting

### 🚀 Amazon CloudFront

* Global Content Delivery Network (CDN)
* Reduces latency using edge locations
* Provides HTTPS support
* Enables caching for better performance
* Adds security layer in front of S3

### 🔐 AWS IAM Role

* Provides secure permission management
* Implements least-privilege access
* Demonstrates security best practices

---

## 🏗️ Architecture

User → CloudFront → S3 → Static Files

---

# 🧠 Key Learning From This Architecture

## 🔹 What Happens When Using S3 Website URL Directly

When users access the **S3 website endpoint**:

* Traffic goes directly to the S3 region
* No global edge caching
* Higher latency for distant users
* Basic HTTP (no automatic HTTPS unless configured separately)
* Bucket is publicly exposed
* Limited performance optimization

✅ Good for: testing and small demos
❌ Not ideal for production

---

## 🔹 What Happens When Using CloudFront URL

When users access via **CloudFront**:

* Request goes to nearest edge location
* Content is cached globally
* Much faster load times
* Built-in HTTPS support
* Better security posture
* Reduced load on S3
* Production-grade architecture

✅ Best for real-world deployments

---

## 🚀 Why This Architecture Matters

This project demonstrates:

* Serverless web hosting
* CDN integration
* Edge caching strategy
* Secure content delivery
* Cost optimization in AWS
* Real DevOps deployment thinking

These are core skills expected from AWS/DevOps engineers.

---

# 🛠️ Implementation Steps

## ✅ Step 1: Create S3 Bucket

* Create unique bucket
* Disable block public access

## ✅ Step 2: Enable Static Website Hosting

* Enable hosting
* Set index.html

## ✅ Step 3: Upload Website Files

Upload:

* index.html
* error.html
* css/
* js/
* images/

## ✅ Step 4: Add Bucket Policy

Allow public read access to objects.

## ✅ Step 5: Create IAM Role

Create role with least privilege (demo: AmazonS3ReadOnlyAccess).

## ✅ Step 6: Test S3 Website

Verify website endpoint works.

## ✅ Step 7: Create CloudFront Distribution

* Use S3 website endpoint
* Enable HTTPS redirect

## ✅ Step 8: Access via CloudFront

Use generated CloudFront domain.

---
## 🏗️ Architecture Diagram
<p align="center">
  <img src="https://github.com/user-attachments/assets/58554c8e-4427-4acb-815e-45ea8a7fbb0e" 
       alt="Serverless Portfolio Hosting with AWS S3 and CloudFront"
       width="900"/>
</p>

# 🧪 Testing Checklist

* ✅ S3 endpoint working
* ✅ CloudFront working
* ✅ HTTPS enabled
* ✅ Fast global loading
* ✅ No AccessDenied errors

---

# 📈 Outcome

Successfully built a **production-style serverless static website hosting architecture** using AWS S3 and CloudFront.

---

# 🔮 Future Enhancements

* Implement Origin Access Control (OAC)
* Add AWS WAF protection
* Enable CI/CD automation
* Add custom domain and SSL
* Enable advanced caching policies

---

## 👨‍💻 Author

**Sudarshan Mane**
Aspiring AWS & DevOps Engineer
