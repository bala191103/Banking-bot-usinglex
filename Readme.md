📌 Project Overview
The Banking Bot is an AI-powered virtual assistant developed using AWS Lex, enabling users to:
✅ Check account balances
✅ Transfer funds securely
✅ Retrieve account details
✅ Access banking-related information

It is integrated with AWS Lambda for backend logic and DynamoDB for storing user transactions.

🚀 Features
Conversational AI powered by AWS Lex
Secure banking transactions with AWS Lambda
Multi-account support (Savings & Current)
Seamless chatbot integration via Kommunicate API
Real-time responses and secure database storage
🛠️ Technologies Used
Technology	Purpose
AWS Lex	Chatbot framework
AWS Lambda	Backend logic for processing user requests
DynamoDB	Stores user balances and transaction history
Kommunicate API	Provides chat interface on the website/app
AWS S3	Hosts static assets & logs interactions
📸 Screenshots
Below are key chatbot interaction screenshots:

1️⃣ Banking Bot Welcome Screen
👉 Images/Welcome.png

2️⃣ Balance Inquiry Response
👉 Images/Balance.png

3️⃣ Fund Transfer Confirmation
👉 Images/FundTransfer.png

4️⃣ Account Summary Screen
👉 Images/AccountSummary.png

📂 Folder Structure
graphql
Copy
Edit
BankingBot/
│── images/                 # Folder for screenshots
│   ├── Welcome.png
│   ├── Balance.png
│   ├── FundTransfer.png
│   ├── AccountSummary.png
│── lambda_function.py       # AWS Lambda backend logic
│── README.md                # Project Documentation
🛠 3️⃣ Set Up AWS Lambda Function
1️⃣ Create Lambda Function
Login to AWS Console → Navigate to AWS Lambda.
Click Create Function → Select Author from Scratch.
Set Function Name as BankingBotHandler.
Choose Runtime as Python 3.x.
Under Permissions, create a new IAM Role with necessary policies.
Click Create Function.
2️⃣ Upload Lambda Code
Open the lambda_function.py file.
Copy and paste the code into the AWS Lambda code editor.
Click Deploy.
✅ Lambda Function Created Successfully! 🎉

🤖 4️⃣ Configure AWS Lex Bot
1️⃣ Create the Bot
Open AWS Lex Console → Click Create Bot.
Set Bot Name as BankingBot → Select Create a new IAM Role.
Click Next → Configure the following intents:
Intent Name	Function
CheckBalance	Fetch and display account balance
TransferFunds	Process money transfers
AccountSummary	Show recent transactions
Under Fulfillment, select AWS Lambda Function and choose BankingBotHandler.
Click Save & Build → Test the Bot in AWS Lex Console.
✅ Lex Bot is Ready to Use! 🎉

🌍 5️⃣ Deploy the Chatbot on a Website (Kommunicate API)
1️⃣ Integrate Kommunicate API
Sign up on Kommunicate → Get your API Key.
Add the following script to your HTML file:
html
Copy
Edit
<script type="text/javascript">
(function(d, m){
    var kommunicateSettings = {
        "appId": "YOUR_APP_ID",
        "popupWidget": true,
        "automaticChatOpenOnNavigation": true
    };
    var s = document.createElement("script"); 
    s.type = "text/javascript"; s.async = true;
    s.src = "https://widget.kommunicate.io/v2/kommunicate.app";
    var h = document.getElementsByTagName("head")[0]; 
    h.appendChild(s);
    window.kommunicate = m; m._globals = kommunicateSettings;
})(document, window.kommunicate || {});
</script>
Replace "YOUR_APP_ID" with your Kommunicate API Key.
Save the file and open it in a browser.
✅ Chatbot is Live on the Website! 🎉

📝 Additional Notes
AWS Lex chatbot automatically improves responses using Machine Learning.
Ensure IAM permissions allow AWS Lex to invoke Lambda functions.
DynamoDB auto-scaling ensures faster performance.
📬 Contact & Support
📧 Email: balaji629262@gmail.com

