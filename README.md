# acdt_cpp

To run the command line should go to the appropriate directory (/acdt/ - for the version continuous attributes). Then you start typing the name of the program and selected parameters and their values.


Usage: acdt --parameter_name_1[=value] --parameter_name_2[=value]
For example (LINUX): './acdt --dataSet=zoo'
For example (WIN - CMD): 'acdt.exe --dataSet=zoo'
Parameters:
    --dataSet - dataset name, which is located in the '/datasets/' (without '_tr.am' // '_te.am' // '_clean.am' For example: '--dataSet=car'). Default: 'car'
    --ld - number of iterations. Default: 250
    --wp - number of ants in population. Default: 25
    --q0 - a value parameter exploitation/exploration rate. Default: 0.1



The results are stored in the directory '/results/' in the file with the same name as the parameters

---------

The input data should be stored in the directory '/datasets/' and must be located in three files:
     name_tr.am - training set data
     name_te.am - test set data for the learning algorithm
     name_clean.am - test set (clean) set data, viewing the final result - are not used during the construction of decision tree



Dataset format is as follows:
576 - First line, number of objects
6 - Second line, number of conditional attributes
4 - Third line, number of classes of decision
0 403 - Next line, the number of objects in the first decision class
1 128 - Next line, the number of objects in the second decision class
... ect. - Next lines, the numbers of objects in the next decision class 
4 4 4 3 3 3 - Next line, Number of possible values of attributes
Then the objects - their value following attributes (int) separated by spaces (one object in each line)
