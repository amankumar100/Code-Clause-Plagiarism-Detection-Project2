# Code-Clause-Plagiarism-Detection-Project2
This is my 2nd Project made for AI internship at Code Clause


For this project I have used difflib and Sequential Matcher as a library or package.

This compares the two different files and detects the amount of plagiarism.

I have mentioned the simple python code below.

To execute it just copy the code and instead of 2 different file locations at line 2 put your 2 different file locations.



from difflib import SequenceMatcher          # here difflib can be used as conjunction for AI and ML for plagiarism detection

with open(r"File location 1") as file1, open(r"File Location 2") as file2: #opens 2 different files assigning them to file1 and file2
    
    file1_data = file1.read()        #reads the file 1
    
    file2_data = file2.read()        #reads the file 2
    
    similarity_ratio=SequenceMatcher(None, file1_data, file2_data).ratio() #will generate the ratio as per comparison of 2 files
    
    print('Plagiarism detected = ',similarity_ratio*100,'%')  #It gives the percentage of plagiarism in the file.
