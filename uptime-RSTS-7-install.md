Instructions for RSTS/E V7:

1. Open `UPTIME.BAS` in a text editor.
2. Open a session to your RSTS/E system in a terminal program on the same machine; the RSTS/E system can be physical or virtual.
3. Log on to RSTS/E using the system account [1,2], as in typing `HELLO 1,2`.  The default password is usually `SYSTEM`.
4. You should have a `Ready` prompt.  If not, type `SW BASIC`.
5. Type `NEW UPTIME`.
6. Select and copy all the text in your text editor.
7. Paste it in your terminal window, and hit Enter.
8. Type `SAVE`.
9. Type `COMPILE UPTIME.BAC`.  **This is important.** The program uses privileged functions and it will not work unless it's compiled.
10. Type `ASSIGN UPTIME.BAC <232>`. **This is also important.** This sets the protection code for the compiled program.
11. Test the program with `RUN$UPTIME.BAC`. If it runs, and displays no output, please be sure you have assigned the protection code in step 10.
12. OPTIONAL:  Install the program as a CCL command.
13. Open EDT with `EDT $CCL.CMD`.
14. Once in the editor, hit Enter to move through each line of the file.
15. Continue moving through the file until you see a line that looks like "`440    FORCE KB: CCL TY-PE $TYPE.TEC;8`".
16. Type `INSERT` and Enter.
17. Type the following: `FORCE KB: CCL UP-TIME=$UPTIME.BAC;PRIV`
18. Hit Enter, and Control-Z to exit INSERT mode
19. Type EXIT. EDT will tell you that 49 lines (or so) have been written.
20. Reboot RSTS/E for the changes to take effect.
21. UPTIME can now be invoked with `UPTIME` or simply `UP`.
