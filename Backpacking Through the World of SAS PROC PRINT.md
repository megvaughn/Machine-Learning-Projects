SESUG Paper 80-2024
Backpacking Through the World of SAS PROC PRINT
Megan Vaughn, Florida State University; Bailey Glidden, University of Central Florida

README 

ABSTRACT 

This comprehensive paper strives to encompass the versatility and simplicity of the SAS function, PROC PRINT. This paper aims to contribute a review of the PROC PRINT procedure and its many purposes. The first example covers the simplicity of creating a table in PROC PRINT and the features that can be added on, such as titles and labels. The second example compares and contrasts PROC PRINT and PROC REPORT by listing their respective functions and differences. The third example covers the versatility of the PROC PRINT SAS function and how it can be used in addition to other functions to make SAS output more legible and concise. In our conclusion we discuss the ramifications of PROC PRINT and how this function is used to create titles, works in addition to other functions within SAS, and demonstrates the benefits of using PROC PRINT over other functions due to its straightforward nature. 


INTRODUCTION 

In data analytics, the ability to present the information analyzed in an understandable and comprehensive way is essential to data analyzation. The ability to grasp data is essential to navigating in the world as good decisions are based on weighing all the factors that would become the outcome of any decision. A steadfast and trustworthy way to accomplish this is by using the PROC PRINT function in the SAS software. This function allows for the display, presentation, and comprehension of data and datasets. In this paper we will show the abilities that PROC PRINT has along with some pros of using the function over other functions and some examples to fully understand how this function works. 


VISUALIZATION 
In PROC PRINT you have the ability to create tables to best suit the needs of your datasets. For many, it is easier to visualize the data and its variables by creating tables to determine how to best approach the data set. PROC PRINT gives you the ability to include labels and titles in your table. The PROC PRINT function also has the ability to make output look more clear and concise, which is beneficial to both the author and the reader. 

   Title ‘Blood Types’;
DATA Blood;
INPUT Gender $ BloodType $ Age;
DATALINES;
M A- 20
M B+ 17
M O+ 19
F A+ 22
F B+ 20
M O- 21
;
PROC PRINT DATA = Blood;
Run;
 
Figure 1: PROC PRINT output highlighting the features available in the SAS function, such as title. 

By creating a table that outlines the various variables in the dataset as well as the number of observations, it is easier to decipher the attributes of the given data set. For example, in the given ‘blood’ data set, the number of observations, variables such as Gender, BloodType, and Age are easily observable by the reader. The title at the top of the table ‘Blood Types’ is an additional feature that can be added to PROC PRINT at the user’s discretion. PROC PRINT can be used to customize various tables and charts in SAS. 


SIMPLICITY 
PROC PRINT has pros over other functions in SAS that have the ability to present data. A good example to demonstrate this is comparing PROC PRINT and PROC REPORT. Both of these SAS functions are used in the display of data but both have distinct ways that they show the analyzation of the data. 
A good example to show a pro in using PROC PRINT over using other means such as PROC REPORT is that PROC PRINT automatically puts a space in between the first line in the table showing the names of the columns and the second line in the table showing the output. 
 




Figure 2: PROC PRINT vs PROC REPORT showing space between the first two lines in their respective tables (“Go”).
By creating this space, it is easier to automatically separate the data from the column names of this data which in turn makes it easier to comprehend where the actual data starts and easier to find the name of the data column. There is a way to remedy this when using PROC REPORT which is to add “nowd headskip” after the PROC REPORT in that line of code. But due to this being an extra step that is just automatically done when using PROC PRINT, PROC PRINT is the easier, more understanding method. 
Another example of a way PROC PRINT is able to simplify expressing data is when showing the number of observations in a table that is created by the PROC functions. Numbering the observations in the table is automatic when you use the PROC PRINT function but under the PROC REPORT function you need to write code that makes SAS read the observation column and then add a count of 1 to each observation as it goes down the list. This adds four lines of code after the initial PROC REPORT which is unnecessary if PROC PRINT was used. 

 





Figure 3. PROC PRINT vs PROC REPORT numbering the observations (“GO”). 
Both of these examples show that PROC PRINT as a function is already set up to be the easiest way to display the data in an easy to understand way that is superior to some other functions that procure data such as PROC REPORT. 

VERSATILITY

PROC PRINT can be used in addition to many other SAS functions. The PROC PRINT function allows users to add code to clarify the output by adding specific variables. PROC PRINT automatically includes variable labels, which makes the output easier to discern. 
   
   Title ‘Grocery Prices Publix;
DATA Publix;
INPUT Item $ Price $;
DATALINES;
Milk $5.99
Cheese $6.99
Cereal $3.99
;
RUN;
PROC PRINT DATA = Publix;
RUN;

   Title ‘Grocery Prices Whole Foods’;
DATA Wholefoods;
INPUT Item $ Price $;
DATALINES;
Granola $11.99
Oil $17.99
Gouda $60.99
;
RUN;
PROC PRINT DATA = Wholefoods;
RUN;

   Title ‘Grocery Prices Merged’;
DATA Publix_wh_merge;
	SET Publix Wholefoods;
RUN;
PROC PRINT DATA = Publix_wh_merge;
RUN;

  	



 




Figure 4: PROC PRINT can be used in addition to other SAS functions. 
For example, in the given data set, the datalines function was used to input the data into SAS. Then, PROC PRINT was used to print both the Publix and Whole Foods datalines. The SET function was then used in addition to PROC PRINT to merge the Publix and Whole Foods datasets into one merged dataline, which is then printed with PROC PRINT. PROC PRINT is a very versatile function because it can be used in addition with other SAS functions to make output more organized and easier to read. 

CONCLUSION
In conclusion, the SAS function PROC PRINT gives us the ability to display data in a very straightforward visual manner that is easy to comprehend. This is shown through the PROC PRINT function’s ability to create columns and column titles as well as titles for the entire table it produces. PROC PRINT also automatically returns the results with a clear way to read the data as seen with the line in between the column title and the data as well as numbering the observations. This function being automatic means you do not have to add code to create a more simple and easily understood table like you would with PROC REPORT. PROC PRINT also allows for the ability to demonstrate the merging of two data sets as one table of both of them, which allows for all the data to be in one place. This creates an environment where both data sets are easier to comprehend as they are together and can be compared and contrasted, instead of flipping from one table to the next. Overall, PROC PRINT allows for the method of demonstrating and viewing data to be quick and easy, while displaying the data in a way that is understandable and easier to process. 

REFERENCES
Go, Imelda & Tavakoli, Abbas. (2013). Getting Out of the PROC PRINT Comfort Zone to Start 
_Getting_Out_of_the_PROC_PRINT_Comfort_Zone_to_Start_Using_PROC_REPORT 
Hecht, D. (n.d.). PROC PRINT and ODS: Teaching an Old PROC New Tricks. Programming: Foundations and Fundamentals, SAS Global Forum 2011. https://support.sas.com/resources/papers/proceedings11/270-2011.pdf 
Kaptsanov, E. All the Data That Fits, We Print. 
https://www.lexjansen.com/nesug/nesug97/sassolu/stuelpne.pdf 
Lindsey, C. (n.d.-a). Stop Madly Merging: Proc Print to the Rescue! Coders’ Corner, SUGI 27. 
https://support.sas.com/resources/papers/proceedings/proceedings/sugi27/p085-27.pdf 
SAS Documentation. (2023, October 17). PRINT Procedure. SAS help center. 
https://documentation.sas.com/doc/en/pgmsascdc/9.4_3.5/proc/p1dlh3svb4rrasn14h8jm6nyrj5o.htm 
Zach. (2023, May 2). How to Use PROC PRINT in SAS (With Examples). Statology. 
https://www.statology.org/sas-proc-print/ 

CONTACT INFORMATION 
Your comments and questions are valued and encouraged. Contact the author at:
Megan Vaughn
mcv20m@fsu.edu

Bailey Glidden
ba401181@ucf.edu 


SAS and all other SAS Institute Inc. product or service names are registered trademarks or trademarks of SAS Institute Inc. in the USA and other countries. ® indicates USA registration. 
Other brand and product names are trademarks of their respective companies. 
 
