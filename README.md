# Static Website Project

This project is a simple static website hosted on AWS using S3 and CloudFront. The website showcases your portfolio and is optimized for performance and security through AWS services.

## Features

- **Fast Content Delivery**: The website is delivered via AWS CloudFront, ensuring low-latency and fast access for users worldwide.
- **Secure Hosting**: The website is hosted securely using Amazon S3, and the access is restricted to CloudFront, providing a secure and scalable solution.
- **Cross-Origin Resource Sharing (CORS)**: CORS is configured to allow secure access from different origins.
- **HTTPS**: CloudFront enforces HTTPS, ensuring secure connections.

## Technologies Used

- **AWS S3**: For hosting the static files (HTML, CSS, JS).
- **AWS CloudFront**: For content delivery network (CDN) to serve the website globally with improved speed and security.
- **GitHub**: For version control and source code management.
- **SSH**: Used for securely connecting to the GitHub repository.
  
## Installation and Setup

Follow the steps below to set up and deploy the website:

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/marufp10/Static-Website-Project.git
    cd Static-Website-Project
    ```

2. **Create an S3 Bucket**:
    - Go to the AWS Management Console.
    - Create an S3 bucket (make sure the bucket name is globally unique).
    - Upload your static files (HTML, CSS, JS) to the bucket.
  
3. **Configure S3 Bucket for Static Website Hosting**:
    - Enable static website hosting from the S3 bucket properties.
    - Set the index document and error document names.

4. **Set Bucket Permissions**:
    - Update the bucket policy to allow CloudFront to access the S3 bucket.
    - Add the necessary CORS configuration if required.
  
5. **Create a CloudFront Distribution**:
    - Use CloudFront to serve your website globally with low latency.
    - Create an Origin Access Identity (OAI) and restrict access to the S3 bucket.
    - Configure cache settings, SSL certificates, and other security settings.

6. **Update DNS Settings**:
    - Use Route 53 or another DNS provider to point your domain to the CloudFront distribution.
  
7. **Deploy and Test**:
    - After setting up the CloudFront distribution, open the provided CloudFront URL or your custom domain.
    - Your website should now be live!

## Project Structure
/Static-Website-Project ├── index.html # Main webpage (HTML) ├── style.css # Stylesheet for the website ├── script.js # JavaScript (optional) └── README.md # Project documentation


## Deployment

This website is deployed and accessible via CloudFront and S3. The website is live at the following URL:

- CloudFront URL: https://d1z96k1wrqfld6.cloudfront.net

### Accessing the Website

Once the CloudFront distribution is deployed, you can access the website through the CloudFront URL provided in the CloudFront management console. You can also set up a custom domain for the website.

## Troubleshooting

- If you encounter a **403 Access Denied** error, ensure that:
  - The CloudFront distribution has the correct permissions to access the S3 bucket.
  - The S3 bucket policy allows access from the CloudFront Origin Access Identity (OAI).
  - CORS is configured correctly in the S3 bucket.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


