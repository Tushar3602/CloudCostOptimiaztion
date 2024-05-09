# CloudCostOptimiaztion

If we delete an EC2 instance, its attached volume will automatically get deleted, but it won't delete the snapshot linked with that volume. Therefore, I have created a Lambda function to delete EBS snapshots whenever an EC2 instance is deleted, and it will send you a notification email confirming that the snapshot has been successfully deleted.

Replace 'your_ses_verified_sender_email' with the email address you have verified in SES for sending emails. Replace 'recipient_email' with the email address where you want to receive notifications. Make sure that the sender email address is verified in SES to avoid any sending limitations.

References :-
for deletion of snapshot:-
https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2/client/delete_snapshot.html#delete-snapshot

for notification:-
https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ses/client/send_email.html
