# railway-booking-portal

# 🚆 Railway Info Portal Using AWS

This is a cloud-based **Railway Information Portal** that uses Amazon Web Services (AWS) to deliver a fully serverless web application. The system provides users with an interactive interface to view train schedules and book train tickets. The backend is powered by AWS Lambda, API Gateway, and DynamoDB, while the frontend is hosted on Amazon S3.

---

## 📁 Project Files

### 1. `index.html`
- The landing page of the Railway Info Portal.
- Features a professional design with call-to-action buttons: **Book Tickets** and **View Schedule**.
- Styled with modern CSS for responsiveness and visual appeal.

### 2. `schedule.html`
- Displays train schedules in a clean tabular format.
- Includes train numbers, departure/arrival cities, and times.
- Easy to update for dynamic content integration.

### 3. `book.html`
- A booking form where users can enter passenger name, train number, and travel date.
- Sends form data to the backend via API Gateway.
- Triggers a Lambda function to store data in DynamoDB.

---

## ☁️ AWS Services Used

### ✅ Amazon S3
- Hosts the frontend files (`index.html`, `schedule.html`, `book.html`).
- Configured for static website hosting with public read access.

### ✅ AWS Lambda
- Contains logic to process booking submissions.
- Uses Python and Boto3 to interact with DynamoDB.
- Triggered by API Gateway POST requests.

### ✅ API Gateway
- REST API endpoint exposed to frontend to handle booking requests.
- Integrated with Lambda for secure and scalable data flow.

### ✅ DynamoDB
- Stores booking records with attributes such as `PassengerName`, `TrainNumber`, and `TravelDate`.
- NoSQL design ensures high performance and scalability.

---

## 🚀 Deployment Instructions

### 1. Host Frontend on S3
- Upload all HTML files to an S3 bucket.
- Enable static website hosting.
- Make the files public and note the endpoint URL.

### 2. Setup Lambda
- Write the Lambda function in Python to save data to DynamoDB.
- Assign the required IAM role with `AmazonDynamoDBFullAccess` and `AWSLambdaBasicExecutionRole`.

### 3. Create API Gateway Endpoint
- Use POST method for booking requests.
- Link to your Lambda function.
- Deploy the API and update the form in `book.html` with the invoke URL.

---

## ✅ Example Flow

1. User visits `index.html`.
2. Clicks "Book Tickets" to access `book.html`.
3. Fills form and submits.
4. Data sent to API Gateway, processed by Lambda, and saved in DynamoDB.
5. User is redirected to output showing 'ticket booking is successful'.

---

## 📚 References

- [Amazon S3 Documentation](https://docs.aws.amazon.com/s3)
- [AWS Lambda Documentation](https://docs.aws.amazon.com/lambda)
- [Amazon API Gateway Docs](https://docs.aws.amazon.com/apigateway)
- [DynamoDB Developer Guide](https://docs.aws.amazon.com/amazondynamodb)
- [AWS IAM Best Practices](https://docs.aws.amazon.com/iam)

---

## 👨‍💻 Author
This Railway Info Portal project was developed to demonstrate the use of AWS cloud services in building scalable, serverless web applications with real-world utility.
