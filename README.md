# google-authenticator
A pure Python script that produces the same TOTP codes as the Google Authenticator App

Expects a JSON file called 'secrets.json' in the current folder. The JSON file contains a dict mapping LABEL to SECRET.

If your machine doesn't have the right time, it won't show the right codes. You might have to do

    sudo ntpdate time.nist.gov

The included PNG is a QR code that encodes the following URL:

    otpauth://totp/example.org:grahammitchell?secret=ABCDEFGHIJKLMNOP&issuer=example.org

(I generated the QR code using Dan Hersam's [QR Codes for Google Authenticator](https://dan.hersam.com/tools/gen-qr-code.html) generator thingy. Super helpful.)

There's an "issuer" of example.org, a user of grahammitchell, and a "secret" of ABCDEFGHIJKLMNOP.

![QR code for secret](https://raw.githubusercontent.com/grahammitchell/google-authenticator/master/sample-secret-qr.png "sample secret")

This matches the provided `secrets.json`, so if you scan this QR code into your Google Authenticator app, your app should then produce the same codes as the python script here!

-Graham
