# Module 7 - Terraform Intialization

**Goal**: Initialize Terraform configuration to run on localstack

## Steps

1. Examine the following files, try to guess what the function and purpose of each file is:
    - `main.tf`
    - `variables.tf`
    - `versions.tf`
2. Initialize Terraform: `terraform init`
3. Preview the Terraform plan: `terraform plan`
4. If everything looks good, execute the plan: `terraform apply`
5. What new files are directories are created? Which of these files should never be checked in the Git repository?
6. A new S3 bucket should be running on localstack, you can check that it exists with: `aws --endpoint-url=http://localhost:4566 s3 ls`
7. Try copying a file into the bucket: `aws --endpoint-url=<http://localhost:4566> s3 cp README.md s3://my-test-bucket/
8. To list the files in the S3 bucket use: `aws --endpoint-url=http://localhost:4566 s3 ls s3://my-test-bucket`
9. Delete the file with: `aws --endpoint-url=http://localhost:4566 s3 rm s3://my-test-bucket/README.md`
10. Destroy the S3 bucket using `terraform destroy`

## Tips

- Check the `.gitignore` file at the root of the repository, maybe there is a hint there
