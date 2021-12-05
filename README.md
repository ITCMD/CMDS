# CMDS
A cmd.exe instance management tool that allows you to interract with cmd.exe windows knowing only their titles, or via a text-based graphical interface. CMDS provides colorful and clear displays of information. See the usage below.

[CMDS is under the GNU Public License version 3](https://github.com/ITCMD/CMDS/blob/master/License.txt)
# Installation

To Install CMDS, head over to the [releases](https://github.com/ITCMD/CMDS/releases) page. You have two options for using CMDS: Using the portable files or the installer.

### Recommended Installation For Developers
- Developers should download the portable CMDS.bat file from the [releases](https://github.com/ITCMD/CMDS/releases) page and package it with their programs.

### Recommended Installation For Users
- Individual can use the provided installers which will place the file in the system32 folder. This will allow users to use CMDS like it is a default program in windows, running the command from any cmd window or batch file. Users without administrator access (or who do not want to add a file to their system32 directory) may alternatively download CMDS.bat and use it as a portable file by calling it directly.

***Note that whether you use the installer or the portable version, CMDS.bat takes up the same amount of storage space (16KB as of version 23).***

## Update 23 - *STABILITY PLUS PLUS*
**CMDS has had a complete revamp under the hood, increasing efficiency and GREATLY increasing stability!**
- /W loop now keeps track of windows individually, monitoring title changes and replaced instances, not just counts.
- /G and /K get the list from a variable set in the last list, so even if new windows open or close, the PID will still match
- Added self-checking and error handling. Double checks PID and title matches before executing taskkills and retries up to 3 times if discrepencies are found.
- Added version checking with /ver or /version


# HELP FILE:
Remember to **call** CMDS.bat if you are using it from a batch file or it will end the batch file calling it!
```CMDS Command Prompt Window Lister by IT Command

CMDS [/S] [/P] [/L] [/W] [/V] [/Ver] [/G Num] [/K Num] [/TK String] [/TS String]

 /S         Displays the simple but high information version (fast)
 /P         Pauses Before Exiting. Usefull if using from Run.
 /L         Pauses and refreshes on press of key. Use CTRL+C to quit.
 /W         Refreshes only when a new cmd instance starts (new PID).
 /G         For use when listing entries. Copies an entry from a
            displayed list to clipboard.
 /K         For use when listing entries. Kills an entry from
            displayed list.
 Note:      /G and /K will pull numbers and PIDs from the previous CMDS
            list through a variable to increase accuracy.
 Num        The number of the entry to copy to clipboard or kill.
 /V         Ignores unnamed windows.
 /Ver       Prints the current version of CMDS and allows you to check
            for an update. /version may also be used.
 /TS        Use within a batch file to search for a Window Title.
 /TK        Use within a batch file to kill a matching Window Title.
 String     The Window Title to search for with /TS or /TK


 with /TS the errorlevel will be set to 1 if the title was not found.
 If it is found, the errorlevel will be set to the PID of the cmd instance.

Press any key to continue . . .

Example:

   CMDS /TS "My Window"

    The Above Command Will set the errorlevel to the PID of the cmd instance
    with the title "My Window" (set with the title command). If the instance
    is not found (there is no running window) the errorlevel will be 1.
    if the Syntax was incorrect, errorlevel will be set to 2.


 Created by Lucas Elliott with IT Command  www.itcommand.net
 ```

# View our Other Programs
at [programs.itcommand.net](https://programs.itcommand.net)
