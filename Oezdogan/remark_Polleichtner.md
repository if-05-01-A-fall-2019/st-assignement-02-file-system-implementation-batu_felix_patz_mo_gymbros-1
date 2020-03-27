# File Systems Implementation
## 1.) What has to be done, when creating a file foo.txt?
Um ein File foo.txt zu speichern braucht man zuerst Speicherplatz und ein Verwaltungssystem für Files.//to implement a FS is your task?xD

## 2.) What has to be done, when the file size has to be increased? Especially take care if it needs additional blocks
Wir stellen die nötigen Blocks zur Verfügung und verknüpfen diese Blöcke effizient(Free Space Management).
Zuerst schauen wir auf die benachbarten Blöcke, falls die auch befüllt sind, müssen wir auf die Naheliegenden zugreifen.**//How do you implement your free space manager? How do you know which block is the next?**

## 3.) What has to be done if a file is read sequentially?
Wir teilen die Blöcke in Unterblöcke und lesen Block für Block.
Wir müssen sich den zuletzgelesenen Block merken und dann auf den nächsten Block gehen(Pointerlogik).**//How would you implement this pointerlogic?**

## 4.) What has to be done if you want to access foo.txt randomly (seek())? 
Anstatt die ganzen Files durchzuiterieren machen wir eine Berechnung um genau auf die Speicheradresse zu kommen.**//How do you calculate this?**

## 5.) What has to be done when the file size decreases? Especially take care if it needs fewer blocks
Die Blöcke müssen frei gegeben werden.**//Again how would you know which blocks belong to the file**

## 6.) What has to be done when a file is deleted?
Der Speicherblock muss freigegeben werden. und den Status auf frei umstellen,damit es für den Free Space Management bekannt ist.**//inaccurate again**
