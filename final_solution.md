# File Systems Implementation
## final solution

### Assignment
Write down things to be done when to implement a file / a directory.
Take into account that you have only the operations ReadBlock() and WriteBlock() on the disk.

### Required Tasks
- **What has to be done, when creating a file foo.txt?** 

first of all we need to check if theres enough memory, and then we need to split the file in different chunks, next use the operation write block, therefore we need some kind of free space manager (e.g. every block has a bool value, true=free, false=used), to look what blocks are free. We also have to store the file in some kind of table or list or any information stotage to let the os know the file is here and where it is and store the first block related to the file (store in every block the adress of the next related block and also e.g a value hasNext and isEnd(?))

- **What has to be done, when the file size has to be increased? Especially take care if it needs additional blocks** 

 you have to look for the next free blocks and set hasNext of the last block to the adres of the next appending block.
 As block size increases, it takes longer latency to read a single block
 
- **What has to be done if a file is read sequentially?** 

you need to find the file (look in the table to find the first block) then the ReadBlock() oparations has to read every block of the file in the correct order.

- **What has to be done if you want to access foo.txt randomly (seek())?** 

You need to know where to jump, so you need to calcute the position(position/size). We need a method seek() to get easy and fast acces to this file and we must take care of where the blocks of the file beginns were the blocks are interrupted and where they continue.

- **What has to be done when the file size decreases? Especially take care if it needs fewer blocks** 

you have to deallocate/free every block, that you dont need anymore, you have to check which blocks you need to delete (e.g. with an ID), so that the blocks can be used for new WriteBlock() operation. But if you just need to give a part free, then you just give that part free.

- **What has to be done when a file is deleted?**

you have to deallocate/free all blocks related to that file, jump from block to block with hasNext and overwrite it (e.g. with 0) and remove the file from our table etc. The next time when some blocks would be needed the currently freeed blocks would be available now.
