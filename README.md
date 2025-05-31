# Serverless EC2 Instance Scheduler for Company Working Hours

## Scenario :
In certain organizations, running EC2 instances all the day isn't necessary—they're only needed during specific hours, such as standard business hours from 8:00 AM to 5:00 PM. To optimize resource usage in this case, I’ll set up two AWS Lambda functions: one to start the instances in the morning and another to stop them in the evening. These functions will be triggered automatically by CloudWatch Events scheduled at the appropriate times. This approach provides a fully serverless and automated solution.

![image](https://github.com/user-attachments/assets/b3f209a0-5a9e-4869-b5c3-885389d7ba78)

## Steps :
### Step 1:
### Creating the instance
![image](https://github.com/Ahmed1337a/Automate-start-stop-EC2/blob/d6c96770526bd27d0b883d0d20930e8c68e51510/Images/1.png)

![image](https://github.com/Ahmed1337a/Automate-start-stop-EC2/blob/d0346bb1ef70746d51de95ad384143c63d8d425f/Images/2.png)

![image](https://github.com/Ahmed1337a/Automate-start-stop-EC2/blob/d0346bb1ef70746d51de95ad384143c63d8d425f/Images/3.png)

### Step 2 :
### Creating the Policy :

1. Navigate to the IAM Console.
2. Click on "Policies" and then Click on "Create policy"
   
![image](https://github.com/Ahmed1337a/Automate-start-stop-EC2/blob/d0346bb1ef70746d51de95ad384143c63d8d425f/Images/4.png)

3. Select services as EC2.
4. And Actions are StartInstances and Stop Instance
   
![image](https://github.com/Ahmed1337a/Automate-start-stop-EC2/blob/d0346bb1ef70746d51de95ad384143c63d8d425f/Images/5.png)

![image](https://github.com/Ahmed1337a/Automate-start-stop-EC2/blob/d0346bb1ef70746d51de95ad384143c63d8d425f/Images/6.png)

![image](https://github.com/Ahmed1337a/Automate-start-stop-EC2/blob/d0346bb1ef70746d51de95ad384143c63d8d425f/Images/7.png)

![image](https://github.com/Ahmed1337a/Automate-start-stop-EC2/blob/d0346bb1ef70746d51de95ad384143c63d8d425f/Images/8.png)

5. Now Creating Role for Start Instance

![image](https://github.com/Ahmed1337a/Automate-start-stop-EC2/blob/d0346bb1ef70746d51de95ad384143c63d8d425f/Images/10.png)

![image](https://github.com/Ahmed1337a/Automate-start-stop-EC2/blob/d0346bb1ef70746d51de95ad384143c63d8d425f/Images/12.png)

![image](https://github.com/Ahmed1337a/Automate-start-stop-EC2/blob/d0346bb1ef70746d51de95ad384143c63d8d425f/Images/12.png)

6. Doing the same for Stop instance
   
![image](https://github.com/Ahmed1337a/Automate-start-stop-EC2/blob/d0346bb1ef70746d51de95ad384143c63d8d425f/Images/13.png)

## Step 3 :
## Creating the Lambda functions :
    Now we create two lambda functions one for start and other for stop and attach to each existing Role

 ![image](https://github.com/Ahmed1337a/Automate-start-stop-EC2/blob/d0346bb1ef70746d51de95ad384143c63d8d425f/Images/14.png)
 
 ![image](https://github.com/Ahmed1337a/Automate-start-stop-EC2/blob/d0346bb1ef70746d51de95ad384143c63d8d425f/Images/15.png)

  now we make a deploy and test to make sure that the code and all things is right
  
  ![image](https://github.com/Ahmed1337a/Automate-start-stop-EC2/blob/d0346bb1ef70746d51de95ad384143c63d8d425f/Images/16.png)

  ### Step 4 :
### Creating the Schedules Using Cloud Watch :

  ![image](https://github.com/Ahmed1337a/Automate-start-stop-EC2/blob/d0346bb1ef70746d51de95ad384143c63d8d425f/Images/17.png)
  
  Now we create two Rules one for Start and one for Stop

  ![image](https://github.com/Ahmed1337a/Automate-start-stop-EC2/blob/d0346bb1ef70746d51de95ad384143c63d8d425f/Images/18*.png)


  Now, we have successfully created two schedules: one to start the instance every day at 8:00 AM and the other to stop the instance every day at 5:00 PM.
  

  
  
  




  


 

    


   







   
 















