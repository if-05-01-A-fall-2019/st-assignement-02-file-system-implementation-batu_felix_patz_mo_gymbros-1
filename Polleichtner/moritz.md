# File Systems Implementation
## Own Approach

### Assignment
Write down things to be done when to implement a file / a directory.
Take into account that you have only the operations ReadBlock() and WriteBlock() on the disk.

### Required Tasks
- **What has to be done, when creating a file foo.txt?** 
first of all we need enough memory, and then we need to use the operations write block, therefore we need some kind of free space manager, to look what blocks are free. We also have to store the file in some kind of table or list or any information stotage to let the os know the file is here and where it is

- **What has to be done, when the file size has to be increased? Especially take care if it needs additional blocks** 
 you have to look for the next free blocks (free space manager) and connect them to the other blocks of the file
 
- **What has to be done if a file is read sequentially?** 
you need to find the file (look in the table etc) then the ReadBlock() oparations has to read every block of the file and therefore you have to know which block belongs to which file

- **What has to be done if you want to access foo.txt randomly (seek())?** 


- **What has to be done when the file size decreases? Especially take care if it needs fewer blocks** 
you have to deallocate/free every block, that you dont need anymore, therefore you need to know which block belongs to the file we want to delete, so that the blocks can be used for new WriteBlock() operation
- **What has to be done when a file is deleted?**
you have to deallocate/free all blocks related to that file and remove the file from our table etc.
