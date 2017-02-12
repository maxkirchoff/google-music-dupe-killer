Google Music Dupe Killer
========================

Really small script designed to remove pesky duplicates from Google Music.

** The duplicates must have all correct meta data as this evaluates their title and album for detection.

Thanks to [simon weber](https://github.com/simon-weber) for a GREAT client library that made this super easy to code.

## Usage
This is a incredibly simple script, but does require a few small configurations.

### Install [Unofficial Google Music Api](https://github.com/simon-weber/Unofficial-Google-Music-API)
* For most environments with Python 3 already installed:
   
   ```$ pip install gmusicapi```
* If you do not have pip or are running windows, please see [Unofficial Google Music API usage](http://unofficial-google-music-api.readthedocs.org/en/latest/usage.html)

### Change login credentials
* Near line 89, change the 'username' and 'password' to your Google account credentials.
* NOTE: Users with 2-step authentication enabled will have to create an App Specific Key/Password.
Login into your Google account and head to https://security.google.com/settings/security/apppasswords, there you will be able to manually generate an App Specific password.
After creating the Key/Password, just use it to login into this App, together with your usual Google username/email.

### Run kill_dupes
* The script will automatically detect and remove duplicates on any songs in your library.


Thanks!
