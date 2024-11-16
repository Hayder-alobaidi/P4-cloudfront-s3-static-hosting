# Global Static Website Hosting with CloudFront

This project demonstrates how to host a static website on AWS using various AWS services like S3, CloudFront, Route 53, and AWS Certificate Manager (ACM). The result is a secure, highly available, and globally distributed website that benefits from AWS's caching, security, and scalability features.

The goal of this project is to ensure fast, reliable, and cost-efficient content delivery to users worldwide, with advanced caching strategies, access control mechanisms, multi-region setup, and continuous deployment.

---

## Technologies Used:
- **AWS S3**: For static website hosting.
- **AWS CloudFront**: For global content delivery via a CDN.
- **AWS Certificate Manager (ACM)**: For SSL/TLS encryption (HTTPS).
- **Route 53**: For DNS management and custom domain configuration.
- **CloudWatch**: For logging and monitoring website performance.
  
---

## Project Phases and Implementation

### Phase 1: Basic Static Website Hosting with S3 & CloudFront
- Set up an **S3 bucket** for static website hosting.
- Created a **CloudFront distribution** for globally distributed content delivery.
- Configured a custom domain and DNS via **Route 53**.
- Enabled **SSL/TLS** encryption using **AWS Certificate Manager (ACM)** to ensure secure content delivery (HTTPS).

### Phase 2: Cache Control & Caching Strategies with CloudFront
- Set Cache Expiration (TTL) based on file types (e.g., longer TTL for images, shorter TTL for HTML).
- Configured **Cache Invalidation** to purge outdated content from CloudFront when new content is deployed.
- Optimized caching with **Cache Behaviors** to apply different TTL settings to different content types.
- Used **asset versioning** by appending version numbers to filenames to ensure the delivery of updated content.

### Phase 3: Advanced Security with Signed URLs and Signed Cookies
- Created **Signed URLs** to restrict access to private content (e.g., videos, downloadable files).
- Implemented **Signed Cookies** to provide authenticated access to specific content areas.
- Optionally configured **IP whitelisting** to control access based on source IPs.

### Phase 4: Cross-Origin Resource Sharing (CORS) Configuration
- Configured **CORS** headers on specific resources (images, APIs) in **S3** to enable cross-domain resource sharing.
- Ensured that **CloudFront** propagated the appropriate CORS headers for all cross-origin requests.

### Phase 5: Logging and Monitoring with CloudFront and S3
- Enabled **CloudFront Access Logs** to track user requests served by the CDN.
- Set up **S3 Access Logs** to monitor who is accessing static content stored in the S3 bucket.
- Configured **CloudWatch** to track CloudFront performance metrics (e.g., latency, cache hit/miss ratios) and set alarms to alert on any potential issues.

### Phase 6: Global Content Delivery with Multi-Region Setup
- Created **multiple S3 buckets** in different AWS regions to store copies of the website content.
- Configured **CloudFront** for **multi-origin setup**, utilizing latency-based routing to serve content from the nearest S3 bucket.
- Implemented **Origin Failover** to ensure high availability and content redundancy in case one region's bucket becomes unavailable.

### Phase 7: Cost Optimization and Best Practices
- Used **S3 Storage Classes** (e.g., **Intelligent-Tiering**, **Glacier**) to optimize storage costs for infrequently accessed content.
- Optimized **CloudFront TTL** settings to reduce the frequency of data retrieval from S3 and reduce overall costs.
- Enabled **CloudFront Compression** to reduce content size and save bandwidth during content delivery.

### Phase 8: Content Versioning and Continuous Deployment
- Enabled **S3 Versioning** by appending version numbers to filenames (e.g., `index-v1.html`) to ensure the latest content is always served.
- Automated deployment from **GitHub** to **S3** using **GitHub Actions**, allowing for seamless and continuous updates to the website.
- Ensured **CloudFront** served the latest version of content after each deployment.

### Phase 9: Integrating Third-Party Services
- Integrated **Google Analytics** for website traffic and user behavior tracking.
- Added **SEO metadata** (structured data) to improve search engine visibility and rankings.
- Used **JavaScript/HTML Injection** (via third-party services) to dynamically inject content and personalize user experiences.

---

## Final Outcome

By completing this project, I now have a fully functional, globally distributed static website with the following key features:

- **Secure**: The website is served over HTTPS with SSL/TLS encryption, and private content is protected using signed URLs and cookies.
- **Optimized for Performance**: Content is cached globally using **CloudFront**, with multi-region setup for faster content delivery and reduced latency.
- **Scalable**: The infrastructure can handle large traffic spikes, with CloudFront ensuring efficient content delivery even under heavy load.
- **Cost-Effective**: I implemented best practices for reducing costs, such as using S3 storage classes and optimizing CloudFront TTLs and compression.
- **Monitored and Logged**: I have set up **CloudWatch** for monitoring and receiving alerts on any performance or availability issues, and enabled access logs to track user behavior and resource access.

---

## Skills Mastered

- **S3 Configuration**: Setting up and managing S3 buckets for static website hosting, access control, and versioning.
- **CloudFront Distribution**: Configuring CloudFront for caching, security (signed URLs and cookies), global delivery, and multi-region support.
- **Advanced Security**: Implementing signed URLs, signed cookies, and IP whitelisting for content access control.
- **Performance Optimization**: Configuring caching strategies, TTLs, asset versioning, and compression for faster content delivery.
- **Cost Optimization**: Using cost-effective storage solutions (e.g., Intelligent-Tiering, Glacier) and optimizing CloudFront settings to reduce bandwidth and retrieval costs.
- **Continuous Deployment**: Automating the deployment pipeline with GitHub Actions for seamless website updates.
- **Third-Party Integrations**: Adding Google Analytics, SEO metadata, and dynamic content injection to enhance user experience and site performance.

---

## Setup Instructions

### Prerequisites:
- AWS account
- AWS CLI or Console access
- Custom domain name (optional, if using Route 53 for DNS)
- GitHub repository (optional, for CI/CD integration)

### Steps to Deploy:

1. **Set up the S3 bucket** for static website hosting and upload your website content (HTML, CSS, JS).
2. **Create a CloudFront distribution**, linking it to the S3 bucket for global content delivery.
3. **Configure Route 53** (or any DNS provider) to point your domain to the CloudFront distribution.
4. **Enable logging** on both CloudFront and S3 for access tracking.
5. **Configure CloudWatch** to monitor CloudFront performance and set up alarms for issues like high latency or error rates.
6. **Set caching rules** (TTL) in CloudFront and enable content compression.
7. **Automate deployments** with GitHub Actions to push content updates to S3.
8. **Test the website** for security (HTTPS), performance (fast loading), and availability (global access).

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
