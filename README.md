# google-authenticator
A pure Python script that produces the same TOTP codes as the Google Authenticator App

Expects a JSON file called 'secrets.json' in the current folder. The JSON file contains a dict mapping LABEL to SECRET.

If your machine doesn't have the right time, it won't show the right secrets. You might have to do

    sudo ntpdate time.nist.gov
