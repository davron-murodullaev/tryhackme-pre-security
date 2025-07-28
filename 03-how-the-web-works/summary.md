# SECTION 3: How The Web Works

## 1. Objectives
In this section you will learn:
- **DNS in Detail:** how domain names resolve to IP addresses
- **HTTP in Detail:** structure of requests and responses, common methods
- **How Websites Work:** the client-server model and page rendering
- **Putting it All Together:** full flow from DNS lookup to HTTP response

## 2. Key Commands & Concepts

| Command / Concept       | Description                                          |
|-------------------------|------------------------------------------------------|
| `dig example.com +short`| Quickly query DNS records (A, CNAME, MX, etc.)       |
| `curl -I http://URL`    | Fetch only HTTP headers from a web resource          |
| HTTP Methods            | GET, POST, PUT, DELETE                               |
| Status Codes            | 200 OK, 301 Redirect, 404 Not Found, 500 Server Error|

## 3. Hands-On Example

1. **Task:** Resolve a domain and fetch its headers  
2. **Steps:**  
   ```bash
   # 1. DNS lookup for tryhackme.com
   dig tryhackme.com +short

   # 2. Get HTTP headers from the site
   curl -I https://tryhackme.com
