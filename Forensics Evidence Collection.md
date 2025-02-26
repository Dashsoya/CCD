# Windows Memory Live Acquisition

## BelkaSoft

## DumpIT
To acquire memory image (RAM) of a live Windows machine.
Ensure the USD Stick which holds the DumpIT tool is larger than the machine's RAM size as the acquired memory image will have the same size.

<br>
<br>
<br>
<br>
<br>

# Windows Memory Dead Acquisition
RAM data is cleared.

## hiberfil.sys (Hibernation file)
Contains replica of memory content when machine is put into hibernation and is used to restore the user session when the system boots up.

## pagefile.sys (Paging file)
Used to store parts from memory on local hard drive.
Extends available system memory by allowing OS to move infrequent accessed memory content from RAM to page file on disk for better performance.

## CrashDumps
.dmp file is created by OS containing the recorded state of the computer memory at the time of the crash.

<br>
<br>
<br>
<br>
<br>

# Linux Systems 

## Acquire Volatile Memory for Linux (AVML)

## Linux Memory Extractor (LiME)
Requires the manual creation of Linux device tailored to the kernel version of the system.
To find out kernel version of Linux machine ($uname -a)

# Encrypted Drive Detection
To check for existence of disk encryption before cutting the power. Once power is cut, disk gets encrypted, making data inaccessible.
Best to perform live triage and disk acquisition while machine is still powered on if disk encryption is present.

($EDDv310.exe)
