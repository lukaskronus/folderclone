# folderclone #
A project which allows you copy public folders to a Shared Drive using Google Service Accounts from GSuite Business or GSuite Education accounts.

## Requirements for using the scripts ##

	Python 3.7+ (Use 64-Bit Python only)
	The following modules from pip3: oauth2client, google-api-python-client, progress & httplib2shim
	
### Getting all emails

#### Windows :-

  1) Open PowerShell and cd into the root of copied accounts folder

  2) Execute:- `$emails = Get-ChildItem .\**.json |Get-Content -Raw |ConvertFrom-Json |Select -ExpandProperty client_email >>emails.txt`

This will give you all of your emails into `emails.txt` file 


#### For linux / MacOs users :-

  1)`grep -oPh '"client_email": "\K[^"]+' *.json > emails.txt`

This will give you all of your emails into `emails.txt` file 

<br />

