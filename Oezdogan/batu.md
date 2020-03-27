# File Systems Implementation
## 1.) What has to be done, when creating a file foo.txt?
Um ein File foo.txt zu speichern braucht man zuerst Speicherplatz und ein Verwaltungssystem für Files.

## 2.) What has to be done, when the file size has to be increased? Especially take care if it needs additional blocks
Wir stellen die nötigen Blocks zur Verfügung und verknüpfen diese Blöcke effizient(Free Space Management).
Zuerst schauen wir auf die benachbarten Blöcke, falls die auch befüllt sind, müssen wir auf die Naheliegenden zugreifen.  

## 3.) What has to be done if a file is read sequentially?
Wir teilen die Blöcke in Unterblöcke und lesen Block für Block.
Wir müssen sich den zuletzgelesenen Block merken und dann auf den nächsten Block gehen(Pointerlogik). 

## 4.) What has to be done if you want to access foo.txt randomly (seek())? 
Anstatt die ganzen Files durchzuiterieren machen wir eine Berechnung um genau auf die Speicheradresse zu kommen. 

## 5.) What has to be done when the file size decreases? Especially take care if it needs fewer blocks
Die Blöcke müssen frei gegeben werden.

## 6.) What has to be done when a file is deleted?
Der Speicherblock muss freigegeben werden. 
