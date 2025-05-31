# Serverless EC2 Instance Scheduler for Company Working Hours

## Scenario
In certain organizations, running EC2 instances all the day isn't necessary—they're only needed during specific hours, such as standard business hours from 8:00 AM to 5:00 PM. To optimize resource usage in this case, I’ll set up two AWS Lambda functions: one to start the instances in the morning and another to stop them in the evening. These functions will be triggered automatically by CloudWatch Events scheduled at the appropriate times. This approach provides a fully serverless and automated solution.

![image](https://github.com/user-attachments/assets/b3f209a0-5a9e-4869-b5c3-885389d7ba78)

## Steps 
### Step 1
### Creating the instance


