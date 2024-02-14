# Python Twitch OAuth 
## A Python utility for handling Twitch OAuth tokens and refreshing them as needed.

## Overview
TwitchHandler is a Python class designed to simplify the process of obtaining and refreshing OAuth tokens for Twitch API integration. It provides methods to generate new tokens, save and load tokens from a file, check if a token needs refreshing, and refresh tokens when necessary.

# Getting Started
Clone the repository:
```
git clone https://github.com/PolishDogge/PythonTwitchOAuth.git
```
Install the required dependencies:
```
pip install requests
```
# Usage:
```
from twitchHandler import TwitchHandler
```

### Check if a token needs refreshing and refresh if necessary
```
TwitchHandler.token_needs_refreshing()
```

### Get the current OAuth token
``` 
token = TwitchHandler.get_oauth_token()
print(f"Current OAuth token: {token}")
```
### Configuration
Before using the TwitchHandler class, you need to set up a Twitch Developer application and obtain the client_id and client_secret. Update the client_id and client_secret in the TwitchHandler class with your own credentials.

```
client_id = "your_client_id"
client_secret = "your_client_secret"
```
### Generating New Tokens
To generate new OAuth tokens, run the following code. This will open a web browser to authorize your application and prompt you to enter the authorization code.

```
TwitchHandler.generate_new_tokens()
```
Follow the instructions in the terminal to complete the authorization process.

### Token Refreshing
If your token has expired, the TwitchHandler class will automatically attempt to refresh it when needed. If successful, the refreshed token will be saved for future use.

# License
This project is licensed under the MIT License - see the LICENSE file for details.

# Acknowledgments
Inspired by the need for a simple Twitch OAuth token handler in Python.

Special thanks to the Twitch API for providing a robust authentication system.

Feel free to contribute and make improvements!
