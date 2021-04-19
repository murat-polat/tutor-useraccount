
## MFE plugin for frontend-app-account

https://github.com/edx/frontend-app-account 
This is a micro-frontend application responsible for the display and updating of a user's account information.
In this MFE: Private user settings UIs. Public facing profile is in a separate MFE (Profile)

Account settings page
Demographics collection
IDV (Identity Verification). End modified for Tutor Open edX. This is an example plugin for to implement a micro-frontend application to Tutor Open edX.  Please test it before using in production !



Installation:
If using virtualenv: (optional)

$ python3 -m venv ~/tutor

$ source ~/tutor/bin/activate

### Cloning and installing plugin

$ git clone https://github.com/murat-polat/tutor-useraccount 

$ pip3 install -e tutor-useraccount

$ tutor plugins list

$ tutor plugins enable useraccount

$ tutor config save

Building new Docker services for Tutor

$ tutor images build useraccount

$ tutor local quickstart

After login ==> visit http://yourdomain.com:1997. 

