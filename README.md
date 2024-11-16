# 🌍 Global Static Website Hosting with CloudFront

This project demonstrates how to host a **static website** on AWS using services like **S3**, **CloudFront**, **Route 53**, and **AWS Certificate Manager (ACM)**. The goal is to ensure **secure**, **scalable**, and **high-performance** content delivery to users worldwide.

With features like **advanced caching**, **security control**, **global distribution**, and **CI/CD deployment**, this website is optimized for both speed and cost-efficiency. 

---

## 🛠️ Technologies Used

- **AWS S3** 🗂️: Static website hosting.
- **AWS CloudFront** 🌐: Global content delivery via CDN.
- **AWS Certificate Manager (ACM)** 🔒: SSL/TLS for HTTPS.
- **Route 53** 🌍: DNS management and custom domains.
- **CloudWatch** 📊: Monitoring, logging, and alarms.

---

## 📋 Project Phases & Implementation

### Phase 1: Basic Static Website Hosting with S3 & CloudFront
- Set up **S3 bucket** for hosting static content (HTML, CSS, JS).
- Created a **CloudFront distribution** for fast, global delivery.
- Configured **Route 53** for DNS and custom domain.
- Enabled **SSL/TLS encryption** with **ACM** for HTTPS.

---

### Phase 2: ⚡ Cache Control & Performance Optimization
- Set **TTL** (Time-to-Live) for different file types (images, HTML, JS).
- Configured **Cache Invalidation** for fresh content updates.
- Applied **Cache Behaviors** for optimized content delivery.
- Enabled **asset versioning** to ensure correct content versions are served.

---

### Phase 3: 🔐 Advanced Security with Signed URLs and Signed Cookies
- Created **Signed URLs** for private content (e.g., videos, downloads).
- Implemented **Signed Cookies** for secure access to authenticated users.
- Optional: **IP whitelisting** for access control.

---

### Phase 4: 🌍 Cross-Origin Resource Sharing (CORS)
- Configured **CORS headers** on S3 resources to allow cross-domain sharing.
- Set up **CloudFront CORS settings** to propagate headers correctly.

---

### Phase 5: 📈 Logging and Monitoring with CloudWatch & S3
- Enabled **CloudFront and S3 access logs** to track requests.
- Set up **CloudWatch** for real-time monitoring (latency, cache hit/miss ratios).
- Configured **CloudWatch alarms** to alert on performance issues.

---

### Phase 6: 🌎 Global Content Delivery with Multi-Region Setup
- Created **S3 buckets in multiple AWS regions** for replicated content.
- Configured **CloudFront** for **latency-based routing** to serve content from the nearest region.
- Set up **Origin Failover** to ensure high availability.

---

### Phase 7: 💸 Cost Optimization & Best Practices
- Used **S3 Storage Classes** like **Intelligent-Tiering** and **Glacier** to reduce costs.
- Optimized **CloudFront TTLs** and **data compression** to save on bandwidth.
- Applied **CloudFront cache policies** to improve cache hit ratio and minimize S3 requests.

---

### Phase 8: 🔄 Content Versioning and Continuous Deployment
- Implemented **S3 versioning** (e.g., `index-v1.html`) for updated content.
- Automated **CI/CD** pipeline using **GitHub Actions** to push content to S3.
- Ensured **CloudFront** serves the latest content after each deployment.

---

### Phase 9: 📊 Integrating Third-Party Services
- Integrated **Google Analytics** for website traffic tracking.
- Added **SEO metadata** to improve search engine ranking.
- Dynamically injected content using **JavaScript** for personalization.

---

## 🎯 Final Outcome

By completing this project, I now have a fully functional **global static website** with:

- ✅ **Secure delivery** (SSL/TLS, signed URLs, signed cookies)
- ⚡ **Optimized performance** (CloudFront caching, multi-region delivery)
- 🌍 **Scalability** (handles global traffic spikes)
- 💰 **Cost-efficiency** (optimized storage, bandwidth, and caching)
- 📊 **Real-time monitoring** (via CloudWatch, access logs, and alarms)

---

## 💡 Skills Mastered

- **S3 Configuration**: Setting up static website hosting, permissions, and versioning.
- **CloudFront**: Configuring caching, security, and global distribution.
- **Advanced Security**: Implementing signed URLs/cookies, IP whitelisting, and access control.
- **Performance Optimization**: Caching strategies, asset versioning, compression.
- **Cost Optimization**: Using S3 Storage Classes, CloudFront pricing optimization.
- **CI/CD Deployment**: Automating deployments with GitHub Actions.
- **Third-Party Integrations**: Google Analytics, SEO metadata, dynamic content injection.

---

## 🚀 Setup Instructions

### 📝 Prerequisites:
- AWS account
- AWS CLI or Console access
- Custom domain (optional, for Route 53 DNS management)
- GitHub repository (optional, for CI/CD)

### 🔧 Steps to Deploy:

1. **Set up the S3 bucket**: Create and configure an S3 bucket for static hosting.
2. **Configure CloudFront**: Link your CloudFront distribution to the S3 bucket for global delivery.
3. **Set up Route 53** (optional): Configure DNS for your custom domain to point to CloudFront.
4. **Enable logging**: Set up access logs for both CloudFront and S3.
5. **Configure CloudWatch**: Monitor CloudFront metrics and set alarms for performance issues.
6. **Implement caching and versioning**: Adjust TTLs, enable compression, and version assets.
7. **Deploy and test**: Automate deployments with GitHub Actions and ensure the website is live with HTTPS.

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
