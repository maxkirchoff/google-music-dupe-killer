Google Music Dupe Killer
========================

Really small scripts designed to remove pesky duplicates from Google Music.

** The duplicates must have all correct meta data as this evaluates their title and album for detection.

Thanks to [simon weber](https://github.com/simon-weber) for a GREAT client library that made this super easy to code.

## Usage
These are incredibly simple scripts, but do require a few small configurations.

### Install [Unofficial Google Music Api](https://github.com/simon-weber/Unofficial-Google-Music-API)
* For most environments with Python 3 already installed:
   
   ```$ pip install gmusicapi```
* If you do not have pip or are running windows, please see [Unofficial Google Music API usage](http://unofficial-google-music-api.readthedocs.org/en/latest/usage.html)

### Change login credentials
* Near line 12 in the script, change the 'username' and 'password' to your Google account credentials. 
* Alternatively, create an empty file called 'credentials.py' in the script directory and set the username and password variables there.

```python
# credentials.py
username = 'changeme@gmail.com'
password = 'changeme'
#android_id = 'deadbeefc0decafe'
```

* NOTE: Users with 2-step authentication enabled will have to create an App Specific Key/Password.
Login into your Google account and head to https://security.google.com/settings/security/apppasswords, there you will be able to manually generate an App Specific password.
After creating the Key/Password, just use it to login into this App, together with your usual Google username/email.

* NOTE: If you see the error message "a valid MAC could not be determined."
you are running into a [known issue](https://github.com/simon-weber/gmusicapi/issues/408) with the Google Music API.
To workaround, set a new 16 digit hexadecimal number as your android_id on line 17 or in credentials.py.

### Run kill_dupes
* The script will automatically detect and remove duplicates on any songs in your library.

### Run kill_playlist_dupes
* This script works on one playlist at a time and removes the second through nth duplicate of a track in a playlist.


Thanks!
