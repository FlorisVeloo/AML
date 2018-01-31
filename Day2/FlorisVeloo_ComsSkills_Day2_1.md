1. data format: .csv

**key characteristics**
- .csv stands for comma-seperated-values
- The format uses a table-like presentation of plain text data in which the values are seperated by commas (or variants).
- the data format it often used to exchange data between different spreadsheet programms. 
- It is also used to move data from one database to another.

**history**
The .csv format is around since 1972.

*reference:*
- IBM FORTRAN Program Products for OS and the CMS Component of VM/370 General Information (PDF) (first ed.), July 1972, p. 17, GC28-6884-0, retrieved January 31,2018, For users familiar with the predecessor FORTRAN IV G and H processors, these are the major new language capabilities

**data handling tools**

This data format can be handled by any excel-like programm given the specified seperation value. In R, the data format can be read by the following line of code: read.csv('File.csv') and R will create a data frame from it. Additional arguments need to be specified if the first line contains the variable names; 'header = true' or the file contains missing values; na.strings = 'NA'. more additional arguments can be found in R by typing; ?read.csv. 