# copy drive contents to folder via user controlled batch file

i don't know coding. the script is made by github copilot via prompts to get the desired functionality, behavior and display

***<ins>The text file needs to be converted to batch file, and then the batch file to be copied inside the drive the user wants to backup frequently</ins>***

<ins>TL;DR</ins>
- the script creates a folder in a user-specific location in the pc and copies all contents of the drive (microsd, hdd, ssd) it is saved in.
- if there is a pre-existing folder with the same name in the user-specified destination directory, the script deletes the pre-exsiting folder, creates a new one with the same name and copies the contents of the drive it is stored in.

that's to avoid digging deeper into synchronization in a batch (if it's doable). for frequent use and backup directly from a drive's directory without 3rd party software. i wouldn't recommend to use it for very large files, i do not know how it would handle them. in my case it is made to copy gcode files.

<ins>More detail:</ins>

It is an one time user-centric double click way to keep a copy of all the contents of a drive (3d printer's microsd in my case) to a specific folder in the pc while avoiding doing all the tedious steps like creating/deleting/opening folders, selecting, right clicking (or hotkeying) etc while also avoiding to make use of a sync/backup 3rd party software where the changing drive letters require repetitive actions to retarget drives. it's made that way, (stored to the desired drive), to be instantly available when navigating to that drive via a file explorer reducing the process in 5 steps using only mouse clicks and no keyboard interaction:

1. open a file explorer,
2. navigate to the drive and open it,
3. double click the batch file saved inside the drive,
4. when the script starts to run a cmd will appear showing the steps of the process for both cases 1. if there is a folder and 2. if there isn't, and a list of the contents that are copied in the user specified folder with 3 second delays between steps due to the user-centric nature of the script to let the user catch-up,
5. navigate to the user-specified folder to view the files.

*in the text file, the desired path and the name of the folder also need to be changed (currently i left mine, name of folder MicroSD-clone-Ender-2-Pro and path C:\Docs\- 3D printer\MicroSD-clone-Ender-2-Pro, to give an idea what needs change).*
