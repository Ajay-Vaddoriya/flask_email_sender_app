# Flask Email Sender Application

This is a simple Flask application that allows users to upload a CSV file containing email addresses, specify an email subject and message, and send emails to a specified range of addresses from the CSV file.

## Features
  1. Upload a CSV file containing email addresses.
  2. Specify the subject and message for the email.
  3. Send emails to a specified range of email addresses from the CSV file.
  4. Uses Flask-Mail for sending emails.
     
## Requirements
  1. Python 3.x
  2. Flask
  3. Flask-Mail
  4. Pandas
  
## Installation
  ### 1. Clone the repository:
          git clone https://github.com/your-repo/flask-email-sender.git
          cd flask-email-sender
  ### 2. Create and activate a virtual environment:
          python3 -m venv venv
          .\venv\Scripts\activate 
  ### 3. Install the required packages:
          pip install Flask Flask-Mail pandas
          
## Configuration
  ### 1. Set the sender email and app password:
          Edit the following lines in the code:
          
            sender_email = 'replace_with_sender_emailId'
            app_password = 'replace_with_app_password'
            
          Replace replace_with_sender_emailId with your email address and replace_with_app_password with your app password. Make sure to enable "Less secure app access" on your Google account or create an app-              specific password if using 2FA.

  ### 2. Configure the mail server settings:

          The application uses Gmail's SMTP server. If you need to use another email provider, change the following settings accordingly:
          
            app.config['MAIL_SERVER'] = 'smtp.gmail.com'
            app.config['MAIL_PORT'] = 465
            app.config['MAIL_USERNAME'] = sender_email   
            app.config['MAIL_PASSWORD'] = app_password 
            app.config['MAIL_USE_TLS'] = False
            app.config['MAIL_USE_SSL'] = True

            
## Running the Application
  ### 1. Start the Flask application:
          python app.py
  ### 2. Open your web browser and navigate to:
          http://127.0.0.1:5000/


## Usage
  ### 1. Upload a CSV file:
          The CSV file should have a column named email containing the email addresses.

  ### 2. Specify the email details:
          1. Subject: The subject of the email.
          2. Message: The message to be sent.
          3. From: The starting index (1-based) of the email list to send emails from.
          4. To: The ending index (1-based) of the email list to send emails to.

  ### 3. Send the emails:
          After uploading the file and specifying the email details, the application will send emails to the specified range of addresses.
