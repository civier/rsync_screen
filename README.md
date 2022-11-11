# rsync_screen

Usage: rsync_screen SOURCEDIR TARGETUSER@TARGETHOST:TARGETDIR 

rsync_screen copies complete folders (not single files!) using rsync, with the transfer continuing in the background also in case of network disruption. 
It also keeps the rsync log, and prints the exit status at the end.

Notes:

1. If the username in the target machine is identical to the username in source machine, TARGETUSER@ can be dropped (including the @ sign)

2. If TARGETDIR is a relative path (does not start with / or ~), the path will be relative to the home directory of TARGETUSER on TARGETHOST

3. If TARGETDIR already exists, the content of SOURCEDIR will be copied to TARGETDIR

To download the script to your machine, please run


  wget https://raw.githubusercontent.com/civier/rsync_screen/main/rsync_screen
  
  chmod u+x rsync_screen


Author:
Oren Civier

Acknowledgments:
The author acknowledge the facilities and scientific and technical assistance of the National Imaging Facility, a National Collaborative Research Infrastructure Strategy (NCRIS) capability, at Swinburne Neuroimaging, Swinburne University.
