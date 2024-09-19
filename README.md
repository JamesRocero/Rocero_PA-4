# Rocero_PA-4

# ECE BOARD EXAM PROBLEM
![image](https://github.com/user-attachments/assets/b555ca10-e216-4709-8148-4f3a63b14e0b)

##### • Import pandas as library
``` Python
import pandas as pd
```
##### • Input of the board2.xlsx file
``` Python
df = pd. read_excel ("board2.xlsx" )
```
##### • Calculate the average of their scores
``` Python
df ['Average'] = df.mean (numeric_only=True, axis=1)
df
```
![image](https://github.com/user-attachments/assets/cb7bd45e-1615-4598-955b-753b5cf65c6e)

## a. Filename: Instru = [“Name”, “GEAS”, “Electronics >70”]; where track is constant as Instrumentation and hometown Luzon
##### • Function to print the instruction asked.
``` Python
print("Instru")
```
##### • Sort the Luzon students by using Instrumentation as their track.
##### • To see the same output as the provided output, select the desired columns.
``` Python
Instru = df.loc[(df.Track=="Instrumentation") & (df.Hometown=="Luzon") & (df.Electronics>70), ['Name', 'GEAS' , 'Electronics']]
Instru
```
![image](https://github.com/user-attachments/assets/80179ab3-07b4-490a-b2de-8277a948aec4)

## b. Filename: Mindy = [ “Name”, “Track”, “Electronics”, “Average >=55”]; where hometown is constant as Mindanao and gender Female
##### • Function to print the instruction asked.
``` Python
print("Mindy")
```
##### • Remove the female students whose hometown is Mindanao.
##### • Only those pupils whose average score is 55 or higher should be included.
##### • Pick out wanted columns for desired output
``` Python
Mindy = df.loc[(df.Hometown=="Mindanao") & (df.Gender=="Female") & (df.Average>=55) , ['Name', 'Track', 'Electronics', 'Average']]
Mindy
```
![image](https://github.com/user-attachments/assets/6edb2338-ff21-456d-b0f3-4624f10637bc)

## 2. Create a visualization that shows how the different features contributes to average grade. Does chosen track in college, gender, or hometown contributes to a higher average score
##### • Import matplotlib as library
``` Python
import matplotlib.pyplot as plt
```
##### • Print the graph showing the chosen track's correlation with grades using this function.
``` Python
plt.figure (figsize=(5,6))
plt.bar (df ['Track'], df ['Average'])
plt.xlabel ("Chosen Track in College") 
plt.ylabel ("Average")
plt.title ("Table 1.1: The relationship of chosen track in college .")
Text(0.5, 1.0, 'Table 1.1: The relationship of chosen track in college .')
```
![image](https://github.com/user-attachments/assets/0a256894-5fcc-414f-b7d2-b36200b9a726)

##### • This function prints a graph showing the relationship between grades and the selected track.
``` Python
plt.figure (figsize=(5,6))
plt.bar (df ['Gender'], df ['Average'])
plt.xlabel ("'Gender")
plt.ylabel ("Average")
plt.title ("Table 1.2: The relationship of gender and average grade.")
Text(0.5, 1.0, 'Table 1.2: The relationship of gender and average grade.')
```
![image](https://github.com/user-attachments/assets/de8f790c-8b18-4879-b4a2-867d972cea62)

##### • Print the graph showing the link between grades and this function.
``` Python
plt.figure(figsize=(5,6))
plt.bar (df['Hometown'],df ['Average'])
plt.xlabel ("Hometown" ) 
plt.ylabel ("Average")
plt.title ("Table 1.3: The relationship of hometown and average grade.")
Text(0.5, 1.0, 'Table 1.3: The relationship of hometown and average grade.')
```
![image](https://github.com/user-attachments/assets/89a7ff9a-d74b-4b92-89ba-dafcb4dc299e)
