# rsync_screen

Usage: rsync_screen SOURCEDIR TARGETUSER@TARGETHOST:TARGETDIR 

rsync_screen copies complete folders (not single files!) using rsync, with the transfer continuing in the background also in case of network disruption. 
It also keeps the rsync log (in the user home directory), and prints the exit status at the end.
SOURCEDIR and the complete directory tree below it will be copied to the TARGETHOST machine, with SOURCEDIR itself being renamed to TARGETDIR.

Notes:

1. If the username in the target machine is identical to the username in source machine, TARGETUSER@ can be dropped (including the @ sign)

2. If TARGETDIR already exists, the result of the command will be that the directory tree below SOURCEDIR will be combined with the existing directory tree below TARGETDIR on TARGETHOST.

3. If TARGETDIR is a relative path (does not start with / or \~), the path will be relative to the home directory of TARGETUSER on TARGETHOST.

4. If TARGETDIR starts with \~, \~ will be substituted with the home directory of TARGETUSER on TARGETHOST.

5. If TARGETDIR is omitted (but with the preceding ':' character intact), TARGETDIR is the home directory of TARGETUSER on TARGETHOST.


To download the script to your machine, please run


  wget https://raw.githubusercontent.com/civier/rsync_screen/main/rsync_screen
  
  chmod u+x rsync_screen


Author:
Oren Civier

Acknowledgments:
The author acknowledge the facilities and scientific and technical assistance of the National Imaging Facility, a National Collaborative Research Infrastructure Strategy (NCRIS) capability, at Swinburne Neuroimaging, Swinburne University.
