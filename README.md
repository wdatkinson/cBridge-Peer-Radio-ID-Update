# cBridge-Peer-Radio-ID-Update
Pulls csv's from radioid.net and updates the cBridge Maps

This script needs to run under a an admin level user on the cBridge.  It is recommended to create a user specific to this purpose, but you can use an existing admin user.  Once that user has been created/selected, edit the config.txt file and place the username on the first line and the password on the second.  Save the file and exit your editor.

The script allows for custom radio/peer ID's to be added to the import process by including them in the following files respectively.

	1). custom_peers.csv
	2). custom_radios.csv
  
Format for each files is:

	user alias,ID
  
Example from my custom_peers.csv:
  
	DMRLink - Parrot -- 1311811,1311811

Ensure that there are no blank lines, including at the end of the file, otherwise parsing errors may occur during import.

Installation:

	1). mkdir /opt/cbridge-id-update (or wherever you want to install)
	2). cd /opt/cbridge-id-update
	3). git clone https://github.com/wdatkinson/cBridge-Peer-Radio-ID-Update.git .
	4). edit config.txt and add your login info as noted above
	5). edit id_update.sh so that the SCRIPTPATH variable matches what you chose in #1.  Leave alone if you used default path.
	6). run the script: ./id_update and confirm no errors are reported.  Check your cBridge and confirm radio/peer ID's are updated.
	7). schedule cron job to run id_update at your preferred interval.  Every 24 hours is a good place o start.
