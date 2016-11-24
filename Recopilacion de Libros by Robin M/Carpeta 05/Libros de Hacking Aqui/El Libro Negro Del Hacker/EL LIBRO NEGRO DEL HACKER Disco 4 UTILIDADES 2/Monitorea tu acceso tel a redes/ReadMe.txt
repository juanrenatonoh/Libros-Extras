Dial-Up Networking Monitor v2.0
Copyright © 1997 Jon Grieve


About
-----
Dial-Up Networking Monitor shows a graph and statistics of the current Dial-Up Networking
connection, including the current throughput and total, maximum and average bytes sent
and received.



Installation
------------
Dial-Up Networking Monitor doesn't have an installation program.  All that's required is
the program itself (DUNMon.exe) and the VB5 Runtime DLL (MSVBVM50.DLL).  If the runtime
file is not present Dial-Up Networking Monitor will not start.  The runtime file can be
downloaded from my homepage (URL below) or from Windows95.com (http://www.windows95.com).

Once downloaded, put the runtime file into the Windows\System directory and DUNMon.exe
into the directory of your choice.  Then, create the usual shortcuts for your Desktop
and Start Menu.


Usage
-----
DunMon will only start logging the throughput on the current Dial-Up connection when it
finds an established connection.  This means you can, for example, run DunMon prior to
firing up your connection and it will not come to life until the connection is made.  It
will also stop logging when that connection is dropped.  This means that the figures
are valid for the whole Dial-Up 'session', and the totals, maximum and average figures
will make sense.  If you fire up another connection, it will come back to life and continue
logging.

If you fire up DunMon while a connection is already active, it will start logging at that
point - so the totals, maximum and average will only be since DunMon was started.  In
this situation, the connection time will be shown with a '>' symbol (showing the
connection time is greater than the time shown).


Known Issues
------------
				** IMPORTANT **

In order for Dial-Up Networking Monitor to function, the latest version of Dial-Up Networking
MUST be installed -- the version that ships with Windows 95 (Gold or SP1) and
Windows 95b/OSR2 cannot be used.

To obtain the updated version, download the Dial-Up Networking v1.2 Update (aka PPTP
for Windows 95) from the Microsoft Web site.  The download location for this update has
moved many times in the past, so I put the latest download location on my homepage, at:
    http://www.southdown.co.uk/users/jgrieve/dunmon.htm


				** IMPORTANT **

In some installations, Dial-Up Networking Monitor requires updated system DLLs.  This
becomes apparent when you load Dial-Up Monitor and receive the following messages:

"The file MSVBVM50.DLL is linked to the the exported routine OLEAUT32.DLL:421 which
is not present"

To fix this, download the following file from my homepage and unzip into
your \Windows\System directory:
  http://www.southdown.co.uk/users/jgrieve/oleupd.zip (265k)

"Run-time error '453'.  Can't find DLL entry point IntitCommonControlesEx in comctl32.dll"

To fix this, download the following file from my homepage and unzip into
your \Windows\System directory:
  http://www.southdown.co.uk/users/jgrieve/comctl32.zip (183k)


				** IMPORTANT **

On Windows NT, Dial-Up Monitor uses the Performance Monitor counters to monitor the RAS
throughput.  This can cause problems when other applications need to modify the counters
database -- normally when adding or removing applications (for example, when installing or
removing Exchange Server).  You may need to unload Dial-Up Monitor to release control of
the counters when installing, removing or configuring some applications.


Revision History
----------------
v2.0
- Interface changes:
  - Application is now 'system tray' based.
  - Graph window uses far less screen space and has options to show/hide everything.
  - Graph colours now user-definable.  Scale, Markers, etc. can be hidden.
  - Detail level of graph is configurable.
  - AutoShow/Hide of graph window when connected/disconnected.
  - AutoShow/Hide of statistics window when connected/disconnected.
  - Left-click on tray icons brings up Dial-Up Networking Dial/Hangup options.
- Added support for NT Server and Workstation v4.0 (v3.5x not tested).
- Added support for non-English versions of Windows 98.
- Figures can be updated at different intervals (0.5, 1, 2, 5 or 10 seconds).
- Sound support.  Play sounds when connected, disconnected and when connection is idle.
- Option to load when Windows is started (Windows 95 only).
- Information window shows version of Winsock and TCP/IP details (Handy for dynamic IP address).
- Works correctly with common controls library (COMCTL32.DLL) prior to IE3/4 versions.
- Fixed bug where Average figures would go negative if connection went past midnight.
- Fixed bug where Graph/Statistics windows would not re-display correctly in Windows 98.

v1.0b3
- Supports Dial-Up Networking v1.2
- Interface changes:
  - Tabbed details - splitting graph and statistics onto separate tabs.
  - Window is now sizable!
  - Averages now shown on graph.
- Averaging of throughput (to 100s of second) produces much smoother graph.
- Homepage moved to www.southdown.co.uk

v1.0b2
- First public beta.
- Added support for 'skipped' seconds where, for example, a 16-bit application would suspend the timer and DUNMon would only get to update it's graph/data after 'n' seconds (where n is anything greater than 1).  In this situation, DUNMon will graph an average of the throughput over the skipped period.

v1.0b1
- Initial (non-public) beta release.


Credits
-------
Many thanks to my older brother Andrew Grieve for his feedback on the initial release.


Contact
-------
The latest version will be available on my homepage, at:
    http://www.southdown.co.uk/users/jgrieve

E-mail me, at:
    jgrieve@southdown.co.uk