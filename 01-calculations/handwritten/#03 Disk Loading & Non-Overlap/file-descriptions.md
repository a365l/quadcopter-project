# #03 Disk Loading & Non-Overlap
## Date - 02/08/2026
- Note: This days commit marks the first meaningful contribution to the project, hence the documention strucutre and methods are subject to change (basically I'll probably get better at writing this over time)

## What is present
- In attached files, handwritten notes reguarding Disk Loading Values (via momentum theory) and Non-overlap placement checks (via pythagorous's theorum) are present. 
- Firstly the section titled 'DJI DL calculation for referance' includes the calculations for the mass produced DJI Matrice 30 drone. Here I used the rotor diamter and drone weight - availavle online - to calculate a DL of 71.2 N/m^2. This value seems to be quite low compared to standard drone and reflects the preferance of industrual efficiency over recreational speed. A lower DL equates to a less responsive but more efficient copter. I used this value to compare potential options to a industry leading design. This value suprised me as it stood out as low comparitivley. 
- Next, using my previously defined PDS AUW weight value of 3.5kg I calculated the DL value of a 13" prop compared to a 15" prop. I found the 15" prop had a similar DL to the DJI at 75.2 N/m^2 whereas the 13" prop had a DL of 100.1 N/m^2.
- I then used the non-overlap equation to calulcate the frame diagonal required to accomodate a 13" and 15" prop. Here I also calculate that a 700mm frame paired with a 15" prop gives 114mm of clearance and a 600mm frame paired with a 13" prop gives 94mm of clearance. 
- Finally, based on DL values and non-overlap outcomes I decieded on 15" props and 700mm diagonal frame and updated the frame-diameter-vs-prop.md trade study

## Files appended 
- \logbook\session\#03 Disk Loading Based Decisions 26-08-02.md
- \02-trade-studdies\frame-diameter-vs-prop.md

