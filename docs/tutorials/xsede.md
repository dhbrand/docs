# Account Setup Guide

You'll benefit from greatly enhanced speed and reliability using high-speed compute resources freely-available from the open-source science community. You'll need to set up accounts with the Texas Advanced Computing Center (TACC) and Extreme Science & Engineering Discovery Environment (XSEDE) to gain the most benefit from these tutorials. If you're working in an academic laboratory, you should have little trouble registering for accounts and allocations available to users with a .edu email address. Bear in mind that large allocations may require approval for a specific research need.

## TACC

You'll need to make an account at https://portal.tacc.utexas.edu/ to get started. Unless you are a professor or in charge of a collaborative project at your company/institution, simply list the PI option near the end of the application as Ineligible. After you've created your account, you'll need to configure two-factor authentication back at the user portal before you can log on to TACC machines.

## XSEDE

Extreme Science & Engineering Discover Environment represents a collection of advanced digital services for scientific collaboration. Your account with them grants you access to the Agave API for job submission and data management, and allows you to run jobs on Stampede using your project allocation.

Register for an account following the steps at https://www.xsede.org/using-xsede
To use Agave, request an allocation following the instructions at https://portal.xsede.org/allocation-request-steps
If you are a staff member at the iPlant Collaborative, send a message to support@iplantcollaborative.org to request access to the "iPlant-Collabs" allocation. Getting access may take a day or two, but you will know for sure upon trying out Stampede for yourself. Note that you will not immediately receive a notification upon getting access. The only way to know for sure is to try it out!

## Accessing Stampede

To access Stampede, you may use a number of different SSH clients, depending on your operating system:

localhost$ ssh taccuserid@stampede.tacc.utexas.edu
For Windows:

SSH support is built into PowerShell for Windows 10.

For the technically curious or advanced, Cygwin is an open-source project to bring a Unix-like environment to windows. While the initial installation options may be overwhelming, all you need are the ssh tools to use the shell to access Stampede. You may also quickly get an Ubuntu image up and running through Atmosphere once you've set up your Cyverse account.

PuTTY: a no-frills Unix-esque SSH client
WinSCP: A more user-friendly interface similar to Windows Explorer. Allows integration with PuTTY and drag-and-drop transfer of files from local drive to remote computer.
For Mac:

Terminal: ssh is built into Mac OS. For extensive use many prefer iTerm2.
Cyberduck
For Unix/Linux:

Terminal: The standard Unix terminal may be used to access Stampede through the ssh command.
