# Create Network Isolated LXD Containers for Testing use  

Two Bash Scripts to *Create* (***isolate-on.sh***) &amp; and to *Cleanup* (***isolate-off.sh)***
three separated LXD Network bridges (lxdbr1, lxdbr2, lxdbr3) and the attached but 
Network Isolated (from each other) LXD containers (C1, C2, C3).

Why?  There are probably alot of examples but one might be that you may want to test something 
like a VPN between servers on multiple Clouds but don't want to pay for multiple Cloud Server 
Instances.   You could use these scripts to simulate isolated Cloud servers.
  
*Here are 2 simple Bash scripts.*  
  
> **isolate-on.sh**  
> **isolate-off.sh**

---

### isolate-on.sh
  
***Purpose:***   
* Create 3 new LXD Bridges (lxdbr1, lxdbr2, lxdbr3)
* Create 3 new LXD Containers each attached to its corresponding LXD Bridge

***Assignments are***  

| LXD Container   | Bridge |
| :-------------- | ------:|
| C1              | lxdbr1 |
| C2              | lxdbr2 |
| C3              | lxdbr3 |

After executing ***isolate-on.sh*** each of those 3 LXD Containers will be network isolated from each other  
but not from their Host or the Internet  

---
  
### isolate-off.sh  
  
***Purpose:*** 
* Delete the 3 isolated LXD lxd Containers (C1, C2, C3)  
* Delete the LXD Network Bridges (lxdbr1, lxdbr2, lxdbr3)  
  
After executing ***isolate-off.sh*** LXD will clean up the containers (C1, C2, C3) and remove the LXD   
Network Bridges (lxdbr1, lxdbr2, lxdbr3)  



