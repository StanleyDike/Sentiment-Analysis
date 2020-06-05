# Programming project 1: Movie Review Analysis

**Goal: The goal of this assignment is to help students familiarize themselves with the following Java programming concepts:**

1.	Input/Output to and from the terminal. 
2.	Storing data in a file and reading data from a file.
3.	Creating object-oriented classes and methods to handle data.
4.	Using data structures to store data in main memory (e.g. HashSet, ArrayList).
5.	Working with character strings.
6.	Using Javadoc comments and generating and html documentation of the program.
7.	Using Java Exceptions to improve the error handling capabilities of the program.

# Description:
For this assignment you will create a program to classify a set of movie reviews as positive or negative based on their sentiment. This process is known as Sentiment Analysis, and there are multiple approaches to analyze the data and estimate the sentiment. More information about sentiment analysis can be found on Wikipedia and other sources.
https://en.wikipedia.org/wiki/Sentiment_analysis 

In this assignment, you are to write a Java program that will classify a review as positive or negative by counting the number of positive and negative words that appear in that review.  

# Program flow

## Step 1: Start the program

Your program will have two inputs as command line arguments, which are the paths to two text files:  the list of positive words (positive-words.txt) and the list of negative words (negative-words.txt). The program loads the positive words and negative words and stores them in two separate lookup tables. The HashSet data structure can be used as a lookup table in Java as it provides a fast way to look if a word exists in it or not.

## Step 2: Load existing database of movie reviews

Every time your program loads, it should first check if there exists a database file (database.txt) in its working directory. If such a file exists, it should load its contents (movie reviews) into the main memory (a HashMap can be used).

## Step 3: Present the user with an interaction menu

0. Exit program.
1. Load new movie review collection (given a folder or a file path).
2. Delete movie review from database (given its id).
3. Search movie reviews in database by id or by matching a substring.

## Step 4: When the user selects “0”, save the database file and exit the program.

# Notes: 

* The above interaction menu should be coded in a loop, so that the user can choose among the different options multiple times, until they choose option “0”, in which case the program terminates.
* Every time your program loads, it should first check if there exists a database file in its working directory. If such a file exists, it should load its contents (movie reviews) into the main memory (a HashMap can be used). If the database file does not exist, an empty HashMap will be created. When the program exits (user selects action “0”), it should save the new database contents back to the database file, replacing the old one.
* When the user selects option “1”:
  * The program should also ask the user to provide the real class of the review collection (if known). The user can choose from the options: 0. Negative, 1. Positive, and 2. Unknown. 
  * Upon loading each review, your program should assign a unique ID to each review, which should not conflict with existing ones, and it should also assign the value of the real class (as provided by the user). 
  * Then the program should automatically classify each review, as positive or negative by counting the number of positive and negative words that appear in that review and assign a value to the “predictedClass” field of each review. The overall classification accuracy should also be reported, if the real class is known.
  * Finally, the newly loaded reviews should be added to the permanent database.
  * When the user selects option “3”, the results should be printed in a formatted manner. The printed information should be a table with each row showing: review ID, first 50 characters of review text, predicted class, real class.



# How to Run Program:

 Data and project3 folders should be in same base/project folder. (Ex. ProjectFolder/Data and ProjectFolder/Project3). Command Line Arguments can be found in the data folder (data/positive-words.txt and data/negative-words.txt) which will be the two inputs. The filepath for positive-words.txt (data/positive-words.txt) should be args[0] and the filepath for negative-words.txt (data/negative-words.txt) should be args[1].

 When finished you can run the program.

 Then enter 1 to load new movie review collection and the filepath should be "data/Movie-reviews/neg" then input the real class which would be 0 = negative.

 Then repeat but with the pos folder.

 So you would enter 1 again to load new movie review collection and the filepath this time should be "data/Movie-reviews/pos" then input the real class which would be 1 = positive.

 Then you can enter "h" to show the options you can choose from again.

 Now you can use the program functionalities. If you enter 2 you can delete a review from database or if you enter 3 you can search for a review by its ID or substring (here you will see if the program geussed correctly if the review was positive or negative under "Predicted" vs what the review actually is rated under "Real") and then finally if you enter 0 you will exit the program and it saves the database.






