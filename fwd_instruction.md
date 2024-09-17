have a look at instructions.md and the index.html 

based on that logic I need a fwd.html file that will do what I call a flow with data. Reply what to put in that file.

The table format is as follows: 

Task;Info1;Info2;Info3;...
analyze pricing;stocks app;;
collect gossip;read newspapers;talk with taxi driver;watch news
make a purchase;;;

and the output is a flow diagram as follows:

flowchart TD
    task1[analyze pricing]
    data1_1[(stocks app)]
    data1_1 --> task1
    task2[collect gossip]
    data2_1[(rread newspapers)]
    data2_2[(talk with taxi driver)]
    data2_3[(watch news)]
    data2_1 --> task2
    data2_2 --> task2
    data2_3 --> task2
    task1 --> task2
    task3[make a purchase]
    task2 --> task3



Important notes: 

+ Do note the number of info elements can be more than 3! 
+ The info elements are using a different look than the Tasks