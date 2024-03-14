Installation instructions for RSTS/E V8, V9 and V10:
1. Open `UPTIME.BAS` in a text editor.
2. Open a session to your RSTS/E system in a terminal program on the same machine; the RSTS/E system can be physical or virtual.
3. Log on to RSTS/E using the system account [1,2], as in typing `HELLO 1,2`.  The default password is usually `SYSTEM`.
4. If the system asks you to attach to an already-running detached job, hit Enter.
5. Type `SW BASIC` to get into the BASIC run-time-system.
6. Type `NEW UPTIME`.
7. Select and copy all the text in your text editor.
8. Paste it in your terminal window, and hit Enter.
9. Type `SAVE`.
10. Type `COMPILE UPTIME.BAC`.  **This is important.** The program uses privileged functions and it will not work unless it's compiled.
11. Type `$ SET FILE UPTIME.BAC /PROTECTION=232`. **This is also important.** This sets the protection code for the compiled program. 
12. Test the program with `RUN$UPTIME.BAC`. If it displays no output, please be sure you have assigned the protection code in step 10.
13. OPTIONAL:  Install the program as a CCL command.
14. Open EDT with `EDT [0,1]START.COM`.
15. Type `type " define/command/system TKB- "` to search for the section with the command definitions.
16. You should see a line that looks like "` 234        define/command/system TKB-       $TKB.TSK`".
17. Type `INSERT` and Enter.
18. Type the following: `define/command/system UP-TIME    $UPTIME.BAC    /privilege`.
19. Hit Enter, and Control-Z to exit INSERT mode
20. Type EXIT. EDT will tell you that 233 lines (or so) have been written.
21. Reboot RSTS/E for the changes to take effect.
22. UPTIME can now be invoked with `UPTIME` or simply `UP`. This command will run in any account, privileged or unprivileged.
