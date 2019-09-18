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



