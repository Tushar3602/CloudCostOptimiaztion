# CloudCostOptimiaztion

If we delete an EC2 instance, its attached volume will automatically get deleted, but it won't delete the snapshot linked with that volume. Therefore, I have created a Lambda function to delete EBS snapshots whenever an EC2 instance is deleted, and it will send you a notification email confirming that the snapshot has been successfully deleted.
