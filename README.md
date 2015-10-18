# Prerequisites #

  1. Download a WakeOnLan source directory (I used https://github.com/jpoliv/wakeonlan).
       Extract the directory, read its README.md file and follow the instructions given.

	2. Run the initialization script: $ ./initialize
	     This creates the ~/.wolrc configuration file.

	3. Input your own machine's MAC address and the absolute path of your WakeOnLan's
	     source directory into the ~/.wolrc configuration file.


# 1. Turn on your computer #

  So it is assumed that the computer you are reading this from is connected to the same
    LAN as your computer which is shutdown right now, and you also completed the
    above prerequisites.

	$ ./wakecomponlan


# 2. Find your computer's IP address #

  Again it is assumed that the computer you are reading this from is connected to the same
    LAN as your computer which is online right now, and you also completed the
    above prerequisites.
  Don't forget to give your computer some time to boot up (mine takes a few minutes!).

	$ ./iscomponline
