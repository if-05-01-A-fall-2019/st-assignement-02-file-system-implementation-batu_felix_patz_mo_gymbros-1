#What has to be done, when creating a file foo.txt?
We need enough blocks and a filesystem manager

#What has to be done, when the file size has to be increased? Especially take care if it needs additional blocks
We need new blocks that are free. If we create a file A and a File B and want to increase the filesize of a now we must take care of the fact that we can't take the next block that is after the last block that has been occupied for A, because this block is already occupied for B. So we have to occupy a new block or blocks after the last block for B and then we need to link the two blockqueues for A together

#What has to be done if a file is read sequentially?
We may not read blocks that are not for our goal file A. 

For example: 1 2 3 4 5 6 7 8 9 10 
             A A A B B B A A C D
We may not read the blocks sequenteially from 1-8. We should read the blocks from 1-3 and then from 7-8 and we may not read 4-6.

#What has to be done if you want to access foo.txt randomly (seek())?
We need a method to get easy and fast acces to this file.

#


