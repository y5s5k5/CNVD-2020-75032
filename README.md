Experimental environment: win10 x64      
Software official website:https://www.trendmicro.com/en_hk/forHome.html   
Software version：17.0.0.1222      
Affected Component: coreServiceShell.exe  C:\ProgramData\Trend Micro\Corridor\Corridor.dat      

Attackers can use symbolic links to write content to any file with system permissions (the content cannot be controlled) with sysytem permissions.   
If the target file is pci.sys, the computer will not start.   
If you write an antivirus protection program, the antivirus protection will be ignored. 

To exploit this vulnerability, you need to delete the Corridor directory, then create an object manager symbolic link to make \RPC Control\Corridor.dat point to the file name you want to open, then create a directory link Corridor link to \RPC Control, and then start PC-cillin Antivirus updates. You only need to wait a moment to write the target file.

For example, the cmd command:  
CreateSymlink.exe  "C:\ProgramData\Trend Micro\Corridor\Corridor.dat"  "‪C:\Windows\System32\drivers\pci.sys"    
