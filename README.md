# google-authenticator
A pure Python script that produces the same TOTP codes as the Google Authenticator App

Expects a JSON file called 'secrets.json' in the current folder. The JSON file contains a dict mapping LABEL to SECRET.

If your machine doesn't have the right time, it won't show the right codes. You might have to do

    sudo ntpdate time.nist.gov

The included PNG is a QR code that encodes the following URL:

otpauth://totp/example.org:grahammitchell?secret=ABCDEFGHIJKLMNOP&issuer=example.org

(generated using [this tool](https://dan.hersam.com/tools/gen-qr-code.html).)

There's an "issuer" of example.org, a user of grahammitchell, and a "secret" of ABCDEFGHIJKLMNOP.

The matches the provided secrets.json, so if you scan this QR code into your Google Authenticator app, your app should then produce the same codes as the provided source code.

-Graham
