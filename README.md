## Distributed Systems - Event-Driven Architecture.

__Name:__ ....Wentao Lin .....

__Demo__: ....https://youtu.be/kbiSLOZd790......

This repository contains the implementation of a skeleton design for an application that manages a photo gallery, illustrated below. The app uses an event-driven architecture and is deployed on the AWS platform using the CDK framework for infrastructure provisioning.

![](./images/arch.png)

### Code Status.

[Advice: In this section, state the status of your submission for each feature listed below. The status options are: (1) Completed & Tested; (2) Attempted (i.e. partially works); (3) Not Attempted. Option (1) implies the feature performs the required action (e.g. updates the table) __only when appropriate__, as dictated by the relevant filtering policy described in the specification.]

__Feature:__
Photographer:

Log new Images - ✅ Completed and Tested

Implemented in processImage.ts using event-driven logic and S3 trigger.

Metadata updating - ✅ Completed and Tested

Handled in add_data.ts and update_data.ts to enrich and modify image records.

Invalid image removal - ✅ Completed and Tested

Implemented in delate_img.ts, which filters and deletes unwanted/invalid images.

Status Update Mailer - 🟡 Attempted

Email logic present in notify_info.ts, but may need full verification/test of SES integration.

Moderator:

Status updating - ✅ Completed and Tested

Status modification logic included in update_data.ts.



### Notes (Optional)
All infrastructure (e.g. S3 buckets, Lambda functions, DynamoDB tables) is provisioned using AWS CDK in photo-library-app.ts and photo-library-app-stack.ts.

The code uses an event-driven pattern where S3 and DynamoDB events trigger corresponding Lambda functions.

File processImage.ts is the entry point for new image uploads, validating and emitting metadata.



