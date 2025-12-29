# Deploying a Node.js Application on AWS

Deploy a Node.js application on **Amazon Web Services (AWS)**. AWS is a leading cloud computing platform offering scalable computing power, storage, databases, and other services, making it ideal for hosting web applications.  

The goal is to successfully deploy the provided Node.js application and make it accessible via a public URL.

---

A Node.js application that responds with a simple success message.

1. Deploy this application on the **AWS platform** (using EC2, Elastic Beanstalk, or any other suitable service).
2. Obtain the **base URL** of the deployed application.
3. Insert this URL into the `AWS_LINK` constant in the `solution.js` file in the format:

AWS_LINK="http://your-aws-public-ip:port"

Verify the deployment by sending a GET request to the deployed URL. The expected response is:


Status Code: 200
Response: "Hurray! I have successfully deployed this application on AWS."
Steps to Deploy
Set up an AWS account if you don’t already have one.

Launch an EC2 instance (or use Elastic Beanstalk for easier deployment).

Install Node.js and npm on the instance.

Upload your Node.js application to the instance.

Install dependencies using:

npm install
Run the application on a public port (e.g., 5000):

node index.js
Configure the security group to allow inbound traffic on the port used by your app.

Test the deployment by accessing the public IP and port via a browser or curl:

curl http://your-aws-public-ip:5000
Update solution.js with your base URL:

const AWS_LINK = "http://your-aws-public-ip:5000";
Verification
Access the AWS URL in a browser or use a GET request.

You should receive the following response:

Hurray! I have successfully deployed this application on AWS.
Ensure the HTTP status code is 200.

Make sure the port used by the Node.js app is open in the AWS security group.

Use a static IP or Elastic IP if you want a persistent endpoint.

You can use PM2 or screen to keep the Node.js app running in the background.
