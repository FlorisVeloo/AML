**Question 1:** Do bird species eat more fish than mammal species on average?
**Question 2:** Is there a mammal species which only eat fruit?

**SQL-code** 
**1:** SELECT AVG(BirdFuncDat.DietFish) > AVG(MamFuncDat.DietFish)
FROM MamFuncDat
JOIN BirdFuncDat
ON MamFuncDat.rowid = BirdFuncDat.rowid ;
**2:** SELECT MAX(DietFruit) == 100
FROM MamFuncDat

**Answers:** 
**1:** Yes, bird species eat more fish on average.
**2:** No, there is not a mammal species which only eat fruit.

**Transformation from the original files to the database**

Step 1: Open LibreOffice Calc
Step 2: Click on 'File', 'Open', choose the .txt file, 'Open', 'Ok'.
Step 3: Click on 'Save as', save as .csv file, 'Save'
Step 4: Open SQLite Manager extension
Step 5: Click on 'Database', 'New database' and choose a name
Step 6: Click on 'Database', 'Import', select the .csv file, 'Ok'.
Step 7: Click on 'Ok'a few more times.

Now the original files are imported in the database.

**Notes:** - Diet-Vfish and Diet-Fruit have been renamed in the .csv file to DietFish and DietFruit, respectively, in order to let the SQL-programm read the column.
- All 4 files have been converted from .txt files to .csv files.