# gcp-cloudrun-functions-qwikstart
A Qwik Start lab demonstrating how to create, deploy, and test Cloud Run functions using the Google Cloud console

# 🚀 Cloud Run Functions: Qwik Start - Console ☁️

## ✨ Overview ✨

This lab provides a hands-on introduction to Cloud Run functions, a serverless execution environment for event-driven services on Google Cloud. 💡 A Cloud Run function is a piece of code that runs in response to an event, such as an HTTP request, a message from a messaging service, or a file upload. Cloud events are things that happen in your cloud environment, like changes to data, file uploads, or VM creation.

Cloud Run functions are event-driven, so they only run when something happens. This makes them ideal for quick tasks or tasks that don't need to run constantly. ⏱️

For example, you can use a Cloud Run function to:

*   Automatically generate thumbnails for images uploaded to Cloud Storage. 🖼️
*   Send a notification to a user's phone when a new message is received in Pub/Sub. 📱
*   Process data from a Cloud Firestore database and generate a report. 📊

You can write your code in any language that supports Node.js, and deploy it with a few clicks. 💻 Once deployed, your Cloud Run function will automatically start running in response to events.

This lab shows you how to create, deploy, and test a Cloud Run function using the Google Cloud console. 👨‍💻

## 🎯 What you'll do 🎯

*   Create a Cloud Run function. ➕
*   Deploy and test the function. 🚀
*   View logs. 🪵

## ⚙️ Setup and Requirements ⚙️

Before starting the lab, ensure you have:

*   Access to a standard internet browser (Chrome browser recommended). 🌐
*   An Incognito or private browser window to avoid account conflicts. 👤
*   Sufficient time to complete the lab (approximately 20 minutes). ⏱️

**Important:** Use only the student account provided for this lab. Using your personal Google Cloud account may incur charges. ⚠️

## 👨‍💻 Lab Instructions 👨‍💻

### 1. Start the Lab and Sign in to the Google Cloud Console

1.  Click the **Start Lab** button. ▶️
2.  If prompted, select your payment method. 💳
3.  On the left, find the **Lab Details** pane. ℹ️
4.  Click **Open Google Cloud console** (or right-click and select **Open Link in Incognito Window**). 🖱️
5.  Copy the **Username** from the Lab Details pane and paste it into the Sign in dialog. Click **Next**. ➡️
6.  Copy the **Password** from the Lab Details pane and paste it into the Welcome dialog. Click **Next**. ➡️
7.  Accept the terms and conditions. 👍
8.  Do not add recovery options or two-factor authentication. 🚫
9.  Do not sign up for free trials. 🚫
10. The Google Cloud console will open in a new tab. ☁️

### **Task 1: Create a function**

In this step, you're going to create a Cloud Run function using the console.

1.  In the console, on the Navigation menu (Navigation Menu icon) click Cloud Run. ☁️
2.  Click **WRITE A FUNCTION**. 📝
3.  In the function dialog, enter the following values:

| Field                      | Value                         |
| -------------------------- | ----------------------------- |
| Service name               | `gcfunction`                  |
| Region                     | `REGION`                      |
| Authentication             | Allow unauthenticated invocations |
| Memory allocated           | Keep it default               |
| Execution environment      | Second generation             |
| Revision scaling           | Set Maximum instances to 5    |

4.  Click **Create**. ➕

**Note:** A helpful popup may appear to validate the required APIs are enabled in the project. Click the **ENABLE** button when requested.

### **Task 2: Deploy the function**

Still in the Create function dialog, in Source code for Inline editor use the default `helloHttp` function implementation already provided for `index.js`.

1.  Click **SAVE and REDEPLOY** to deploy the function. 💾

**Note:** While the function is being deployed, the icon next to it is a small spinner. When it's deployed, the spinner is a green check mark.

### **Task 3: Test the function**

Test the deployed function.

1.  On the function details dashboard, to test the function click **TEST**. ✅
2.  In the Triggering event field, enter the following text between the brackets `{}`:

```json
{
  "message":"Hello World!"
}

Copy the CLI test command and run it in the cloud shell. 💻

You will see the "Hello World!" message as the output. 💬

Task 4: View logs

View logs from the service details page.

On the Service Details Overview page click Logs tab. 🪵

Your application is deployed, tested, and you can view the logs.

Task 5: Test your understanding

Below are multiple-choice questions to reinforce your understanding of this lab's concepts. Answer them to the best of your abilities. 🤔

Cloud Run functions is a serverless execution environment for event driven services on Google Cloud.

✅ True

☐ False

Which type of trigger is used while creating Cloud Run functions in the lab?

☐ Pub/Sub

✅ HTTPS

☐ Cloud Storage

☐ Firebase

🎉 Congratulations! 🎉

You used the Google Cloud console to create, deploy, and test a Cloud Run function. 🏆 Keep exploring! 🚀
