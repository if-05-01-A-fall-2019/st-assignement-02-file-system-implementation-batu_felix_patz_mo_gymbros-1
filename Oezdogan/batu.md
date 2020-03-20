# File Systems Implementation
## 1.) What has to be done, when creating a file foo.txt?
Um ein File foo.txt zu speichern braucht man zuerst Speicherplatz und ein Verwaltungssystem für Files

## 2.) What has to be done, when the file size has to be increased? Especially take care if it needs additional blocks
Wir stellen die nötigen Blocks zur Verfügung und verknüpfen diese Blöcke effizient(Free Space Management) 

## 3.) What has to be done if a file is read sequentially?
Wir teilen die Blöcke in Unterblöcke und lesen Block für Block. 

## 4.) What has to be done if you want to access foo.txt randomly (seek())? 


## 5.) What has to be done when the file size decreases? Especially take care if it needs fewer blocks
Die Blöcke müssen frei gegeben werden.

## 6.) What has to be done when a file is deleted?
Der Speicherblock muss freigegeben werden.
