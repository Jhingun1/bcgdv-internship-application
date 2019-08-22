# BCGDV Internship Application Instructions

Thank you for your interest in Boston Consulting Group Digital Ventures!

To proceed with your application, do two of the following steps:

  - Generate an API key using the instructions below
  - Submit a POST request with your name and email address
  
Also please keep your code / how you did it on a public repo handy for the next interview process.

## 1. Get an API Key

In order to submit the application, you will need this key.

Endpoint: `GET <base URI>/api/v1/key`

Returns: json object: 

```json
{
  "key": "C8EC22A4-02D0-485F-ACEB-8D806CAF9E75",
  "expires": "2019-07-29T14:28:33.508041"	
}
```

HTTP Status: 201 Created


## 2. Application Submission

A name and email address are payloads to be submitted using the generated API key above as an application/json request.

Endpoint: `POST <base URI>/api/v1/submit?apiKey=<API_KEY>`

Example Body: json object: 

```json
{
  "name": "Katrina Verma",
  "email": "k.verma@gmail.com"	
}
```

Replace the name and email with yours.

HTTP Status: 202 Accepted 

Once you receive the HTTP status ACCEPTED, you should see an echo of your json object in the body. This means that your application has been successfully submitted.

Bad Request: Bad key or invalid parameters

Not Found: If API Key doesn’t exist

Submissions must be made by the end of September 8th.