<div align="center">
<img src="./assets/hero.svg" width="100%"/>
</div>


```
▓▒░ 0x00 // ABOUT ░▒▓
```


Windows batch script for automated file backup. Uses `robocopy` to mirror a
source directory to a destination, copying only files modified within a
configurable time window. Designed for scheduled task execution.

<br>

```
▓▒░ 0x01 // USAGE ░▒▓
```


Edit the top of `backup.bat` to set your paths and age threshold:

```bat
SET SOURCE=C:\Users\user\Documents
SET DEST=D:\Backup\Documents
SET MAX_AGE=7
```

Run directly or schedule via Task Scheduler:

```bat
backup.bat
```

<br>

<div align="center">

`.: . . : <[ end of transmission ]> : . :.`

</div>
