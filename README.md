UPTIME.BAS is a RSTS/E BASIC-PLUS system program that will display the current uptime of the system in days, hours, minutes and seconds.
It is based on the original SYSTAT command-line utility in RSTS/E.
It has been tested to run in RSTS/E V7 and V10.2, and it should run in any RSTS/E system in existence, physical or virtual.

Installation instructions for V7 and V8 or later have been put in separate files.


Example output:

```
UPTIME/HELP:

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
```

This is dedicated to all former (and current!) RSTS/E system administrators.  This was the first computer I ever used, in high school, and it has brought me nearly 40 years in the field. As far as I know, this is the first RSTS/E CUSP (Commonly Used System Program) to be coded in 40 years!

Keep running!

-- David C. Moisan



