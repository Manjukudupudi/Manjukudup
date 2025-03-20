**PYTHON**

It is a high-level, interpreted programming language known for its simplicity and readability. It is widely used for web development, data analysis, machine leaning, automation, and more. Python offers a large standard library, supports multiple programming paradigms(object-oriented, procedural, and functional).

Python syntax for a common software development interview question

***FizzBuzz:***

Go through the integers from 1 to 100.
If a number is divisible by 3, print "fizz."
If a number is divisible by 5, print "buzz."
If a number is both divisible by 3 and by 5, print "fizzbuzz."
Otherwise, print just the number.

***Syntax***
![image](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/Python/Screenshot%202025-03-04%20163707.png)

***Result***
![image](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/Python/Screenshot%202025-03-04%20163735.png)

***By using the Student.csv file Exploring and loading the data in Python***
![Data.Csv](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/Python/student%20(1).csv)

1. Write the code to read a CSV file into a Pandas DataFrame?
![image](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/Python/Importing%20student%20file%20in%20python.png)

2. Write the code to display the first 5 rows of the DataFrame?
![image](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/Python/Print%20first%205%20rows.png)

3. Write the code to get the information about the DataFrame?
![image](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/Python/Dataframe%20info.png)

4. Write the code to get summary statistics for the DataFrame?
![image](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/Python/Dataframe%20describe.png)

***Indexing and Slicing***
1. Write the code to select the 'name' column?

    - print(dataframe['name'])

2. Write the code to select the 'name' and 'mark' columns?

    - dataframe[['name','mark']]

3. Write the code to select the first 3 rows?

    - dataframe.head(3)

4. Write the code to select all rows where the 'class' is 'Four'?

   - dataframe[dataframe['class'] == 'Four']
![image](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/Python/Screenshot%202025-03-07%20115255.png)

***Data Manipulation***

1. Write the code to add a new column 'passed' that indicates whether the student passed (mark >= 60)?

   - dataframe['passed'] =dataframe['mark'] >=60
     dataframe

2. Write the code to rename the 'mark' column to 'score'?

   - dataframe.rename(columns={'mark':'score'}, inplace=True)
   dataframe

3. Write the code to drop the 'passed' column?

   - dataframe.drop(columns=['passed'], inplace=True)
   dataframe

***Aggregation and Grouping***

1. Write the code to group the DataFrame by the 'class' column and calculate the mean 'mark' for each group?

   - dataframe.groupby('class') ['score']. mean()

2. Write the code to count the number of students in each class?

   - dataframe['class'].value_counts()

3. Write the code to calculate the average mark for each gender?

   - dataframe.groupby('gender')['score'].mean()

***Advanced Operations***

1. Write the code to create a pivot table with 'class' as rows, 'gender' as columns, and 'mark' as values?
![image](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/Python/Screenshot%202025-03-07%20115504.png)

2. Write the code to create a new column 'grade' where marks >= 85 are 'A', 70-84 are 'B', 60-69 are 'C', and below 60 are 'D'?
   ![image](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/Python/Screenshot%202025-03-07%20115549.png)

3. Write the code to sort the DataFrame by 'mark' in descending order?
   ![image](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/Python/Screenshot%202025-03-07%20115639.png)

***Exporting Data***

Write the code to save the DataFrame with the new 'grade' column to a new CSV file?

  - dataframe.to_csv('student_grades.csv', index=False)
  print("dataframe saved to 'student_grades.csv'")

***By using the GDP (nominal) per capita file 
![Data.csv](https://github.com/Manjukudupudi/Manjukudup/edit/Projects/Python/README.md)
we will work on some more python queries***

•	Read and save the ‘GDP (nominal) per Capita’ data to a data frame called “df” in Jupyter notebook

![image](https://github.com/user-attachments/assets/d4400dbb-b22d-4f66-beca-b74fefbed0e8)

•	Print the first 10 rows

![image](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/Python/Print%20first%2010%20rows.png)

•	Print the last 5 rows 

![image](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/Python/Print%20last%205%20rows.png)

•	Print ‘Country/Territory’ and ‘UN_Region’ columns

![image](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/Python/print%202%20columns.png)

***Additional Data with visualizations***

![image](https://github.com/user-attachments/assets/c6d4d8e9-132e-459d-90f1-53b87826d59d)

![image](https://github.com/user-attachments/assets/e3fe7291-8e45-49c4-8627-1b6834568949)

![image](https://github.com/user-attachments/assets/89819054-1449-4fa7-bca6-14fe30d462f5)

![image](https://github.com/user-attachments/assets/a010ab07-4131-466d-909b-236db21c2bd9)

![image](https://github.com/user-attachments/assets/c6828437-1ba2-4df9-b017-12e6c3b731f8)

![image](https://github.com/user-attachments/assets/2677a372-c17a-42d0-9a87-fa36e5502328)

![image](https://github.com/user-attachments/assets/817d27f8-3e0a-4203-a9ae-121bc23d9a5b)

![image](https://github.com/user-attachments/assets/f56638e7-c1e8-47a5-ac7a-c2f31967b7f4)

![image](https://github.com/user-attachments/assets/7e41b07d-53e0-469d-83e4-8275a39ed28a)

![image](https://github.com/user-attachments/assets/2ccc678e-291c-45cc-bda9-61c5508e1185)

![image](https://github.com/user-attachments/assets/cb35cdc6-b70d-4562-81a2-1620f38c4927)

![image](https://github.com/user-attachments/assets/c4d4b1b3-0e2c-44ad-992a-e15e95104e22)

![image](https://github.com/user-attachments/assets/5f39315c-6e05-4ab4-8a8c-15905f9e143e)

![image](https://github.com/user-attachments/assets/f04613b8-3ca0-4d9e-b8c5-8b9349490862)

![image](https://github.com/user-attachments/assets/9bd019b3-274d-40f9-8db7-95ab6d7987b5)

![image](https://github.com/user-attachments/assets/c7806c7a-db6a-486e-a393-21e1f84c4e2e)

![image](https://github.com/user-attachments/assets/88879676-17ed-4378-9d0e-43724a547e7c)

![image](https://github.com/user-attachments/assets/83a70bf9-b60b-4ea1-a29c-a8b68f7570e9)

![image](https://github.com/user-attachments/assets/0bcef943-aea4-4b59-ae81-19dac97f3669)

![image](https://github.com/user-attachments/assets/471057ca-9ff7-4d67-9b3c-16d3720e648a)

![image](https://github.com/user-attachments/assets/72be8e0e-43d6-429b-8aad-4c089b33e116)
























  




     






