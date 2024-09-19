# Rocero_PA-4

# ECE BOARD EXAM PROBLEM
![image](https://github.com/user-attachments/assets/b555ca10-e216-4709-8148-4f3a63b14e0b)

``` Python
#Import pandas as library
import pandas as pd

#Input of the board2.xlsx file
df = pd. read_excel ("board2.xlsx" )

#Calculate the average of their scores
df ['Average'] = df.mean (numeric_only=True, axis=1)
df
```
![image](https://github.com/user-attachments/assets/cb7bd45e-1615-4598-955b-753b5cf65c6e)


## a. Filename: Instru = [“Name”, “GEAS”, “Electronics >70”]; where track is constant as Instrumentation and hometown Luzon
``` Python
#Function to print the instruction asked.
print("Instru")

#Sort the Luzon students by using Instrumentation as their track.
#To see the same output as the provided output, select the desired columns.

Instru = df.loc[(df.Track=="Instrumentation") & (df.Hometown=="Luzon") & (df.Electronics>70), ['Name', 'GEAS' , 'Electronics']]
Instru

Instru
Name	GEAS	Electronics
0	S1	75	89
7	S8	64	81
29	S30	57	81
```

## b. Filename: Mindy = [ “Name”, “Track”, “Electronics”, “Average >=55”]; where hometown is constant as Mindanao and gender Female
``` Python
#Function to print the instruction asked.
print("Mindy")

#Remove the female students whose hometown is Mindanao.
#Only those pupils whose average score is 55 or higher should be included.
#Pick out wanted columns for desired output

Mindy = df.loc[(df.Hometown=="Mindanao") & (df.Gender=="Female") & (df.Average>=55) , ['Name', 'Track', 'Electronics', 'Average']]
Mindy

—-Mindy--
Name	Track	Electronics	Average
1	S2	Communication	75	67.25
2	S3	Instrumentation	74	72.75
14	S15	Microelectronics	41	59.00
16	S17	Microelectronics	79	70.50
19	S20	Communication	60	66.50
```

## 2. Create a visualization that shows how the different features contributes to average grade. Does chosen track in college, gender, or hometown contributes to a higher average score
``` Python
#Import matplotlib as library
import matplotlib.pyplot as plt
#Print the graph showing the chosen track's correlation with grades using this function.

plt.figure (figsize=(5,6))
plt.bar (df ['Track'], df ['Average'])
plt.xlabel ("Chosen Track in College") 
plt.ylabel ("Average")
plt.title ("Table 1.1: The relationship of chosen track in college .")
Text(0.5, 1.0, 'Table 1.1: The relationship of chosen track in college .')

#This function prints a graph showing the relationship between grades and the selected track.

plt.figure (figsize=(5,6))
plt.bar (df ['Gender'], df ['Average'])
plt.xlabel ("'Gender")
plt.ylabel ("Average")
plt.title ("Table 1.2: The relationship of gender and average grade.")
Text(0.5, 1.0, 'Table 1.2: The relationship of gender and average grade.')

#Print the graph showing the link between grades and this function.

plt.figure(figsize=(5,6))
plt.bar (df['Hometown'],df ['Average'])
plt.xlabel ("Hometown" ) 
plt.ylabel ("Average")
plt.title ("Table 1.3: The relationship of hometown and average grade.")
Text(0.5, 1.0, 'Table 1.3: The relationship of hometown and average grade.')
```
