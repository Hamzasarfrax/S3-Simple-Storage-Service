# S3-Simple-Storage-Service
This project demonstrates my hands-on experience with Amazon S3, IAM, S3 Versioning, public hosting configuration, and AWS KMS encryption. I deployed a fully static HTML/CSS To-Do application using S3 as the storage and hosting solution. The goal of this project is to showcase my practical understanding of secure, scalable cloud storage and static web hosting.

I configured an S3 bucket to act as a public static website endpoint. Since S3 is region-specific, I carefully selected the region to optimize latency and follow AWS best practices. To make the site publicly accessible, I disabled Block All Public Access and applied a secure bucket policy that only allows public read access to website content. This demonstrates my understanding of IAM, access control, and S3 hosting requirements.

To ensure durability and safety of stored assets, I enabled S3 Versioning, which keeps multiple variants of objects inside the same bucket. Versioning makes it easy to preserve, retrieve, and restore object versions in case of unintended deletion, overwriting, or application failure. This setup proves my ability to maintain data integrity and prepare disaster-recovery-ready architectures.

For security, I enabled server-side encryption using AWS KMS keys (SSE-KMS), ensuring that every object uploaded to the bucket is encrypted at rest with AWS-managed keys. This highlights my understanding of encryption mechanisms, key management, and secure data lifecycle practices.

This project shows my ability to design, configure, and deploy real cloud infrastructure — from hosting and access control to encryption and version management. It reflects practical, production-like experience with AWS storage services and demonstrates my readiness for real-world Cloud or DevOps responsibilities.


{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::s3-simple-storage-service/*"
        }
    ]
}
