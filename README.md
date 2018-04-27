# Barry_Assignment
Lambda Functions

Task:  

Barry Danmark APS - backend developer assignment
For the purpose of this assignment an account of AWS is required. In the case you do not have an account, you may create one here:  https://aws.amazon.com/free/
The  Serverless  framework is required for building and deploying the lambda functions/api gateway resources.
Create an api with Serverless that will accept a json of two values (full-name and telephone number), which will trigger a lambda function to manipulate the incoming values. The lambda function should split the full-name into first name and last name, and prepend the danish phone prefix (+45) if that does not already exist as part of the phone number, while removing all spaces. The lambda function should then save those three new values to a DynamoDB table. Create another lambda function that will read the DynamoDB stream and will publish a message to an SNS topic, for example: “User John Doe with phone +4570101122 has just signed up!”. For the lambda functions you may choose any programming language you prefer.
The response of the api should be those three new fields (first name, last name and the phone number with the prefix) in json format with a 200 HTTP status code.
In the case that the json found in the request does not contain any of the two elements we need, the api will return a plain error message with a 400 HTTP status code.
Create a private git repository on  bitbucket  to host your code, and afterwards give access to user getbarry-evan (Evan Cohylakis) to that repository.

Example of a valid incoming json: {
"fullname": "John Doe",
"phone": "70 10 11 22" }
Example of the response json: {
"first_name": "John", "last_name": "Doe", "phone": "+4570101122"
}
For all inquiries please contact  evan@getbarry.co
    
