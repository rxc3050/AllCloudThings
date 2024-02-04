Linux / MacOS Set-up

Option 1: Set your ‘OPENAI_API_KEY’ Environment Variable using zsh

 

1. Run the following command in your terminal, replacing yourkey with your API key. 

echo "export OPENAI_API_KEY='yourkey'" >> ~/.zshrc
 

2. Update the shell with the new variable:

source ~/.zshrc
 

3. Confirm that you have set your environment variable using the following command. 

echo $OPENAI_API_KEY
The value of your API key will be the resulting output.

 

Option 2: Set your ‘OPENAI_API_KEY’ Environment Variable using bash

Follow the directions in Option 1, replacing .zshrc with .bash_profile.

 

You’re all set! You can now reference the key in curl or load it in your Python:

import os
import openai
 
openai.api_key = os.environ["OPENAI_API_KEY"]
 

5. Use a Key Management Service
There are a variety of products available for safely managing secret API keys. These tools allow you to control access to your keys and improve your overall data security. In the event of a data breach to your application, your key(s) would not be compromised, as they would be encrypted and managed in a completely separate location.

 

For teams deploying their applications into production, we recommend you consider one of these services.

 

6. Monitor your account usage and rotate your keys when needed
A compromised API key allows a person to gain access to your account quota, without your consent. This can result in data loss, unexpected charges, a depletion of your monthly quota, and interruption in your API access.

 

Your teams’ Usage can be tracked via the Usage page. If you ever have concerns about misuse there are a few actions you can take to protect your account:

Review your usage to see if it aligns with your team’s work. For users belonging to multiple organizations (ex. corporate and personal), make sure the user has enabled tracking and set their default organization for usage and tracking.

If you believe your key has been leaked, rotate your key immediately from the API Keys page. For customers with applications in production, you will need to update your key values accordingly.

Contact us through help.openai.com for further investigating.

