<div align="center">

```
______  ___  _____  _   ___   _______ 
| ___ \/ _ \/  __ \| | / / | | | ___ \
| |_/ / /_\ \ /  \/| |/ /| | | | |_/ /
| ___ \  _  | |    |    \| | | |  __/ 
| |_/ / | | | \__/\| |\  \ |_| | |    
\____/\_| |_/\____/\_| \_/\___/\_|
```

`[ one command, mirrored, logged ]`

![batch](https://img.shields.io/badge/BATCH-ff00c8?style=for-the-badge&labelColor=0a0014)
![robocopy](https://img.shields.io/badge/ROBOCOPY-00fff9?style=for-the-badge&labelColor=0a0014)

</div>

<br>

```
▓▒░ 0x00 // WHAT THIS IS ░▒▓
```

A single-line `robocopy` job, written for a job that needed recently-modified files off `D:\`
mirrored somewhere safe, with a log to prove it ran.

<br>

```
▓▒░ 0x01 // THE JOB ░▒▓
```

`Recursive_Backup.bat`:

```bat
robocopy /S /E /ZB /XJ D:\ DESTINATION /LOG:backup.log
```

| flag | does |
|---|---|
| `/S` | copy subdirectories, skip empty ones |
| `/E` | copy subdirectories, **including** empty ones |
| `/ZB` | restartable mode; falls back to backup mode on access-denied |
| `/XJ` | exclude junction points (no symlink loops) |
| `/LOG:backup.log` | overwrite `backup.log` with this run's output |

<br>

```
▓▒░ 0x02 // RUN IT ░▒▓
```

```console
C:\> Recursive_Backup.bat
```

Edit `DESTINATION` in the script to point at wherever the mirror should land before running.

<br>

<div align="center">

`.: . . : <[ if it isn't logged, it didn't happen ]> : . :.`

</div>
