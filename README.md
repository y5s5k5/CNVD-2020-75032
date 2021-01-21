Experimental environment: win10 x64      
Software official website:https://www.trendmicro.com/en_hk/forHome.html   
Software version：17.0.0.1222      
Affected Component: coreServiceShell.exe  C:\ProgramData\Trend Micro\Corridor\Corridor.dat      

Attackers can use symbolic links to write content to any file with system permissions (the content cannot be controlled) with sysytem permissions.   
If the target file is pci.sys, the computer will not start.   
If you write an antivirus protection program, the antivirus protection will be ignored. 

To exploit this vulnerability, you need to delete the Corridor directory, then create a symbolic link pointing to the file name to be written, and then start the PC-cillin antivirus update. You only need to wait a while before you can write the target file.
