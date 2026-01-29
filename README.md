# GCP Static Website Architecture

This project presents a design-focused cloud architecture for hosting a scalable and secure static website on Google Cloud Platform (GCP).

The goal of this project is to demonstrate how core GCP services can be combined to deliver high-performance static content with custom domain support, HTTPS, and global scalability.

---

## Project Overview

The architecture is designed to host a static website (HTML, CSS, JavaScript) using managed Google Cloud services, eliminating the need for servers while ensuring performance, security, and reliability.

This repository focuses on **architecture design and service integration**, not live infrastructure deployment.

---

## Architecture Components

### Cloud Storage
- Stores static website assets (HTML, CSS, JS, images)
- Configured as a static website backend

### Global HTTP(S) Load Balancer
- Acts as the single entry point for user traffic
- Routes requests to the backend storage bucket

### Cloud CDN
- Caches static content at edge locations
- Improves latency and reduces backend load

### Cloud DNS
- Manages the custom domain (e.g. example.com)
- Routes domain traffic to the load balancer

### Managed SSL Certificates
- Provides HTTPS encryption
- Automatically managed by Google Cloud

---

## Request Flow

1. User accesses the website via a custom domain
2. DNS resolves the domain to the Google Cloud Load Balancer
3. Cloud CDN serves cached content when available
4. Requests are forwarded to Cloud Storage if cache is missed
5. Static assets are delivered securely over HTTPS

---

## Key Benefits

- Serverless static hosting
- Global scalability
- Built-in security with HTTPS
- Optimized performance using CDN
- Minimal operational overhead

---

## Use Cases

- Portfolio websites
- Company landing pages
- Documentation sites
- Marketing and product pages

---

## Project Scope

This project is intended for **learning, architectural design, and portfolio demonstration purposes**.  
It does not include live deployment or billing-enabled infrastructure.

---

## Author

Bandar Alhujayri
