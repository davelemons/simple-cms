# simple-cms
Cloudformation template to deploy an S3 bucket along with CloudFront Distribution to allow for simple hosting of images and attachments for Pinpoint emails or other uses.

WARNING! - ANY FILES UPLOADED TO THIS CMS WILL BE AVAILABLE TO THE PUBLIC.  DO NOT USE THIS TO STORE ANY THING YOU WOULDN'T WANT THE ENTIRE WORLD TO SEE.  THIS SHOULD ONLY BE USED TO HOST IMAGES/FILES YOU WOULD WANT TO INCLUDE IN EMAILS AND PUBLIC WEBSITES.

## Install
- Deploy CloudFormation Template.  There are no parameters.
- Once Deployment is complete open the Outputs tab of the Cloud Formation Stack
- Deploy files to the S3 bucket indicated on the Outputs tab
- Use the SimpleCMSURL to prefix any files uploaded to S3

## Notes
- The associated S3 bucket will have [S3 file versioning enabled](https://docs.aws.amazon.com/AmazonS3/latest/dev/manage-objects-versioned-bucket.html).  If you need to roll back or change versions you can easily do so via the S3 console.
- All S3 and CloudFront access will be logged to a separate S3 Logging Bucket for auditing purposes.
- [Custom Domain Name](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-to-cloudfront-distribution.html)