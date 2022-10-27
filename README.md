# rsync_screen

Usage: rsync_screen SOURCEDIR TARGETHOST:TARGETDIR 

rsync_screen copies folders using rsync, with the transfer continuing in the background also in case of network disruption. 
It also keeps the rsync log, and prints the exit status at the end

Note: to download the script to your machine, please run


  wget https://raw.githubusercontent.com/civier/rsync_screen/main/rsync_screen
  
  chmod u+x rsync_screen


Author:
Oren Civier

Acknowledgments:
The author acknowledge the facilities and scientific and technical assistance of the National Imaging Facility, a National Collaborative Research Infrastructure Strategy (NCRIS) capability, at Swinburne Neuroimaging, Swinburne University.
