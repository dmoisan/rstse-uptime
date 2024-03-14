Installation Instructions for RSTS/E V7:

1. Open `UPTIME.BAS` in a text editor.
2. Open a session to your RSTS/E system in a terminal program on the same machine; the RSTS/E system can be physical or virtual.
3. Log on to RSTS/E using the system account [1,2], as in typing `HELLO 1,2`.  The default password is usually `SYSTEM`.
4. If the system asks you to attach to an already-running detached job, hit Enter.
5. You should have a `Ready` prompt.  If not, type `SW BASIC`.
6. Type `NEW UPTIME`.
7. Select and copy all the text in your text editor.
8. Paste it in your terminal window, and hit Enter.
9. Type `SAVE`.
10. Type `COMPILE UPTIME.BAC`.  **This is important.** The program uses privileged functions and it will not work unless it's compiled.
11. Type `ASSIGN UPTIME.BAC <232>`. **This is also important.** This sets the protection code for the compiled program.
12. Test the program with `RUN$UPTIME.BAC`. If it runs, and displays no output, please be sure you have assigned the protection code in step 10.
13. OPTIONAL:  Install the program as a CCL command.
14. Open EDT with `EDT $CCL.CMD`.
15. Once in the editor, hit Enter to move through each line of the file.
16. Continue moving through the file until you see a line that looks like "`440    FORCE KB: CCL TY-PE $TYPE.TEC;8`".
17. Type `INSERT` and Enter.
18. Type the following: `FORCE KB: CCL UP-TIME=$UPTIME.BAC;PRIV`
19. Hit Enter, and Control-Z to exit INSERT mode
20. Type EXIT. EDT will tell you that 49 lines (or so) have been written.
21. Reboot RSTS/E for the changes to take effect.
22. UPTIME can now be invoked with `UPTIME` or simply `UP`. This command will run in any account, privileged or unprivileged.
