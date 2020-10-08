# CMDS
Tool to view Command prompt files that are running (hidden or not) by their titles and get the PIDS
works in color
works with batch files
# HELP FILE:
```CMDS Command Prompt Window Lister by IT Command

CMDS [/S] [/P] [/L] [/W] [/V] [/G Num] [/K Num] [/TK String] [/TS String]

 /S         Displays the simple but high information version (fast)
 /P         Pauses Before Exiting. Usefull if using from Run.
 /L         Pauses and refreshes on press of key. Use CTRL+C to quit.
 /W         Refreshes only when a new cmd instance starts (new PID).
            Note: This will not refresh if an old window closes
                  and a new one opens at the same time.
 /G         For use when listing entries. Copies an entry from a
            displayed list to clipboard.
 /K         For use when listing entries. Kills an entry from
            displayed list.
 Num        The number of the entry to copy to clipboard or kill.
 /V         Ignores unnamed windows.
 /TS        Use within a batch file to search for a Window Title.
 /TK        Use within a batch file to kill a matching Window Title.
 String     The Window Title to search for with /TS or /TK


 with /TS the errorlevel will be set to 1 if the title was not found.
 If it is found, the errorlevel will be set to the PID of the cmd instance.


Example:

   CMDS /TS "My Window"

    The Above Command Will set the errorlevel to the PID of the cmd instance
    with the title "My Window" (set with the title command). If the instance
    is not found (there is no running window) the errorlevel will be 1.
    if the Syntax was incorrect, errorlevel will be set to 2.


 Created by Lucas Elliott with IT Command  www.ITCommand.net
 ```
