
# AWS Infrastructure with CloudFormation

Modular and reusable CloudFormation templates for:

- 🔐 S3 + CloudFront + ACM (static site + HTTPS)
- ⚙️ Lambda (basic & API Gateway)
- 🌐 VPC (custom networking setup)

---

## 🔧 Templates

| Module                 | Template Path                                |
|------------------------|----------------------------------------------|
| S3 + CloudFront + ACM | `templates/s3-cloudfront-domain/cloudfront-with-acm.yml` |

---

## 🚀 Deployment via AWS CLI

```bash
aws cloudformation deploy \
  --stack-name s3CloudfrontStack \
  --template-file templates/s3-cloudfront-domain/cloudfront-with-acm.yml \
  --capabilities CAPABILITY_NAMED_IAM \
  --parameter-overrides \
    DomainName=example.com \
    S3BucketDomain=your-bucket.s3.amazonaws.com
````

---

## 🧹 Cleanup

```bash
aws cloudformation delete-stack --stack-name s3CloudfrontStack
```

---

## 📂 Parameters

All parameters can be customized using JSON files under `/parameters`.

---

---

Let me know if you want:

- `deploy.sh` template to auto-deploy any module  
- GitHub Actions workflow for CI/CD  
- Combine or split outputs/logging  


```
