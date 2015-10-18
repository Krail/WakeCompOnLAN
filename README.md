
# Prerequisites #

  1. Download a WakeOnLan source directory (I used https://github.com/jpoliv/wakeonlan).
       Extract the directory, read its README.md file, and follow the instructions given.

  2. Run the provided initialization script:

        $ ./initialize

   NOTE: This creates the ~/.wolrc configuration file.

  3. Input your own machine's MAC address and the absolute path of your WakeOnLan's
       source directory into the ~/.wolrc configuration file.


# Turning on your computer #

  Assuming that the computer you are running this command from is connected
    to the same LAN as your shutdown computer:

	$ ./wakecomponlan


# Finding your computer's IP address #

  Assuming that the computer you are running this command from is connected
    to the same LAN as your computer:

	$ ./iscomponline

  NOTE: Don't forget to give your computer some time to boot up (mine takes a few minutes!).


# Finally #

  You can ssh from anywhere to your now online computer with:

    $ ssh [username]@[ip returned from ./iscomponline]


# ToDo #

	1. Combine prerequisites 2 and 3 into a query and answer with user.
	2. Combine the *iscomponline* command with the *ssh* command
		to make it a single command.
