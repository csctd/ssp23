# Day 3 Q&A

## if confused on something that u did and didnt post in the chat room how do i study that part while studying 

On this website, I'm posting my notebooks that I make in class. 

I would recommend going throgh the prismia fully and reviewing all the code sent playing around with all of the functions
we have used in jupyter hub 
 
### i thought variables  start with "var" is that a different language
Declairing variables are typically different in each language . In python you declare a variable by doing 
`variable_name = value`, for example : `x = 5`  . in c++ and java you have to specify the type of the variable
by doing `int x = 5;` . typically `var` is used in javascript, which you will see later in CSC106 .
## I am still a little confused on writing the groupby code, like I am able to explain the chart but not sure how the actual code works”
 
GroupBy allows us to group the data based on different features to get a more accurate idea about your data ( ex: race  ) 
a groupby would put all the like data together in a group. you can also group by multiple things . The groupby() is a feature 
of the pandas library. 
## is there like a tool that could help us finish codes if we forget?

There are certain ides(integrated development environment) like [vs code](https://code.visualstudio.com/) that have features that catch your mistakes 
and recommend answers for you . But in general when you forget to do something google is your best freind . you can always 
search through stack overflow ,youtube and other sites to find the answer your looking for expecially if its only synthax
(how to write it) and not logic . But its important to remember that these tools are just meant to help you get started with 
your programs not write it all for you . 
## how do you make a pie graph?
 
`kind='pie'` : pie plot ; however a pie chart requires either y column or 'subplots=True'
## What does the `.T` do?

‟I dont get how "race_score_recid.T.plot(kind='bar')" graph is like completely different than "race_score_recid.plot(kind='bar')"”

The `.T` transposes the `DataFrame`, which you can think of swapping the rows for the columns,  so the graph will swap what the vertical and horizontal axes are
   
