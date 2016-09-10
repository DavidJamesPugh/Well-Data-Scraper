# Well-Data-Scraper
Scrapes the UK Oil well table data and generates an excel document for it

Generates a GUI which enables us to specify a numeric or range of numerics 
to gather data from the UK Well Search Tool 
(https://itportal.decc.gov.uk/pls/wons/wdep0100.qryWell). 

Ranges are specified by two numerics seperated by a hyphen i.e 1-30

There are currently 220 quadrants with at most 30 blocks each.

If we want to get all wells in a specified block, we can leave the well field empty. 
Block defaults to 1-30, which is the maximum block coverage. To specify all Quadrants, 
we can pass the quadrant field 1-220. 

The program will seek to not duplicate any entries. 
So the program can be run on the entire data table (Quadrant: 1-220, Block: 1-30) 
a second time in order to get any wells that may have been added between the first 
time we ran the program to mine the data and the second time.

The program writes to a csv file, oil_table.csv. 
Keep this file with this program as it will append to it as it reads new data. 

