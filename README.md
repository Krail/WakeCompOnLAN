# How it works #

  This application is meant to run on a server in order to turn on and access a computer on the same LAN by its MAC address. It utilizes Wake-On-LAN to turn on a computer by its MAC address within the same LAN. Once the computer boots up and is added to the local ARP table (checkout my other GitHub project called [Heartbeat](https://github.com/Krail/Heartbeat)), its global IP address can be determined. The IP address can be used to SSH into the computer.


# Prerequisites #

  1. Download a WakeOnLan source directory (I used [jpoliv's wakeonlan](https://github.com/jpoliv/wakeonlan)).
  Extract the directory, read its README.md file, and follow the instructions given.

  2. Run the provided initialization script:
  ```
$ ./initialize
  ```
  NOTE: This creates the ~/.wolrc configuration file.

  3. Input your own machine's MAC address and the absolute path of your WakeOnLan's
  source directory into the ~/.wolrc configuration file.


# Turning on your computer #

  Assuming that the server you are running this command from is connected
  to the same LAN as your powered down computer:
  ```
$ ./wakecomponlan
  ```

# Finding your computer's IP address #

  Assuming that the server you are running this command from is connected
  to the same LAN as your computer:
  ```
$ ./iscomponline
  ```
  NOTE: Don't forget to give your computer some time to boot up (mine takes a few minutes!).
  Also, you may need my other GitHub project called [Heartbeat](https://github.com/Krail/Heartbeat), which pings your server on startup so that your computer is quickly added to the ARP table.


# Finally #

  You can ssh from anywhere to your now online computer with:
  ```
$ ssh [username]@[ip returned from ./iscomponline]
  ```
