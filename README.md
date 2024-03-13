UPTIME.BAS is a RSTS/E BASIC-PLUS system program that will display the current uptime of the system in days, hours, minutes and seconds.
It is based on the original SYSTAT command-line utility in RSTS/E.
It has been tested to run in RSTS/E V7 and V10.2, and it should run in any RSTS/E system in existence, physical or virtual.

Follow these steps to install it:

1. Open UPTIME.BAS in a text editor.
2. Open a session to your RSTS/E system in a terminal program on the same machine; the RSTS/E system can be physical or virtual.
3. Log on to RSTS/E using the system account [1,2], as in typing HELLO 1,2.  The default password is usually SYSTEM.
4. You should have a "Ready" prompt.  If not, type SW BASIC and Enter.
5. Type NEW UPTIME.
6. Select and copy all the text in your text editor.
7. Paste it in your terminal window, and hit Enter.
8. Type SAVE.
9. Type COMPILE UPTIME.BAC.  This is important. The program uses privileged functions and it will not work unless it's compiled.
10. Test the program with RUN$UPTIME.BAC.
11. OPTIONAL:  Install the program as a CCL command.
12. Open EDT with EDT $CCL.CMD.
13. Once in the editor, hit Enter to move through each line of the file.
14. Continue moving through the file until you see a line that looks like "440    FORCE KB: CCL TY-PE $TYPE.TEC;8".
15. Type INSERT and Enter.
16. Type the following: FORCE KB: CCL UP-TIME=$UPTIME.BAC;PRIV
17. Hit Enter, and Control-Z to exit INSERT mode
18. Type EXIT. EDT will tell you that 49 lines (or so) have been written.
19. Reboot RSTS/E for the changes to take effect.
20. UPTIME can now be invoked with UPTIME or simply UP.

Example output:

UPTIME/HELP:

UP/HELP

UPTIME Options:

/SHORT -- Prints brief uptime message without banner

/BOOT  -- Prints time of current boot

/FULL  -- Prints full uptime report with banner

/DEBUG -- Prints debugging messages

/HELP  -- Prints this message

If UPTIME is invoked outside CCL (RUN$UPTIME), the full report is printed.
UPTIME in CCL (UP-TIME) will default to the short (/SHORT) report.

UPTIME
System uptime    : 27 day(s), 19:46:24

UPTIME/BOOT
System started at: 14-Feb-24 09:41 PM

UPTIME/FULL
RSTS V7.0-07 DM Prod RSTS/E
System uptime    : 27 day(s), 19:47:58
System started at: 14-Feb-24 09:41 PM

RUN$UPTIME
RSTS V7.0-07 DM Prod RSTS/E
System uptime    : 27 day(s), 20:15:21
System started at: 14-Feb-24 09:41 PM

This is dedicated to all former (and current!) RSTS/E system administrators.  This was the first computer I ever used, in high school, and it has brought me nearly 40 years in the field.
Keep running!

-- David C. Moisan



