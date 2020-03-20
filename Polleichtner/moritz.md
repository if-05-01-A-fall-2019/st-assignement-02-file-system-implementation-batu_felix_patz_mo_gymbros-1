# File Systems Implementation
## Own Approach

### Assignment
Write down things to be done when to implement a file / a directory.
Take into account that you have only the operations ReadBlock() and WriteBlock() on the disk.

### Required Tasks
- **What has to be done, when creating a file foo.txt?**
first of all we need enough memory, and then we need to use the operations write block, therefore we need some kind of free space manager
- **What has to be done, when the file size has to be increased? Especially take care if it needs additional blocks**
you have to connect the blocks you have to append connect to the other blocks of the file etc.
- **What has to be done if a file is read sequentially?**
the ReadBlock() oparations has to read every block of the file and therefore you have to know which block belongs to which file
- **What has to be done if you want to access foo.txt randomly (seek())?**
- **What has to be done when the file size decreases? Especially take care if it needs fewer blocks**
you have to deallocate/free every block, that you dont need anymore, so that the blocks can be used for new WriteBlock() operation
- **What has to be done when a file is deleted?**
you have to deallocate/free all blocks related to that file
