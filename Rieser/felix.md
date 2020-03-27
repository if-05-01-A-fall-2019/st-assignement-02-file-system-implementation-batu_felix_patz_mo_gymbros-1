### What has to be done, when creating a file foo.txt?
we need enough empty blocks and memory

### What has to be done, when the file size has to be increased? Especially take care if it needs additional blocks
you have to find an empty block and connect this one with the other blocks of your file

### What has to be done if a file is read sequentially? 
You have to locate the blocks of your file and read them in sequence.

### What has to be done if you want to access foo.txt randomly (seek())?
search the blocks from foo.txt and go trough the block to the position which seek() wants.

### What has to be done when the file size decreases? Especially take care if it needs fewer blocks
If the block is not needed anymore, then you can make it empty and give it free.

### What has to be done when a file is deleted?
you have to make all blocks from the deleted file writeable/empty
