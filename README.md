# Burpsuite Sniper Attack

## Objective

Execute a sniper attack using Burp Suite on a vulnerable web application to identify security vulnerabilities and understand attack vectors through packet analysis.

### Skills Learned

- Penetration Testing: Conducted targeted attacks using Burp Suite's sniper mode to pinpoint vulnerabilities in web applications.
- Traffic Analysis: Analyzed HTTP history and captured web packets to gain insights into data flow and potential security breaches.
- Security Best Practices: Developed a deeper understanding of web application security and the importance of regular vulnerability assessments.

### Tools Used

- Burp Suite: Utilized for executing sniper attacks and for detailed analysis of web traffic.
- Kali Linux: Used to support and enhance the penetration testing process with a range of integrated tools for security testing.

### Outcome
Successfully identified and documented critical security issues in the target web application, leading to improved security measures and enhanced protection against potential cyber threats.
                                 
## Steps

Start up Vulnerable VM and check IP/ set up proxy foxy to work with Burpsuite. Then go to vulenerable VM web application where testing will be held.

![Screenshot 2024-08-15 212944](https://github.com/user-attachments/assets/e7412ffa-e8e2-4760-9e6c-dcefb76b83f4)

![Screenshot 2024-08-15 213220](https://github.com/user-attachments/assets/7a23b870-8ff4-486b-b6b3-1848f8eebedc)

![Screenshot 2024-08-15 213259](https://github.com/user-attachments/assets/f80c27d9-9de6-48db-a6b3-906311356157)

-------------------------------------------------------------------------------

Log into the vulnerable web applicaiton

![Screenshot 2024-08-15 213413](https://github.com/user-attachments/assets/e04f9946-a1a2-47ce-87fe-9097dc44a287)

-------------------------------------------------------------------------------

On Burpsuite go to Proxy -> HTTP History to view the traffic hisotry. Fidn the (POST) for the method which means we are sending information to the web app (Login info)

![Screenshot 2024-08-15 213426](https://github.com/user-attachments/assets/7e7a7648-1d70-4e4d-9c95-852065ed962d)

-------------------------------------------------------------------------------

We can see the username and password info that was sent to the web app. Send to Intruder tab to perform the brute force attack to steal login information.

![Screenshot 2024-08-15 213458](https://github.com/user-attachments/assets/3619e547-044b-41fc-a236-bf484a09383b)

-------------------------------------------------------------------------------

Add the brackets to the password field and then navigate to (Payloads) to then insert our word lists to try against this web app. In this step we can try lots of different methods (SQL injection) for either the username or password if we want to do a spray attack however in this lab we are under the assumtion that we know the username and we want to find a password.

![Screenshot 2024-08-15 213706](https://github.com/user-attachments/assets/737f8efa-0dfa-45e6-a085-a46f840321e0)

-------------------------------------------------------------------------------

Try the list of passwords and review the feedback Hint: Look at the length, if there is a successful login the (Length) column will tend to be more a higher number. If successful return to the login and copy and paste successful password for that username.

![Screenshot 2024-08-15 213851](https://github.com/user-attachments/assets/eb4a0f24-1f19-41d0-af7e-e98b1a81fcfb)

-------------------------------------------------------------------------------






