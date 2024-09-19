# Rocero_PA-4

# ECE BOARD EXAM PROBLEM
image.png
``` Pyhton
#Import pandas as library
import pandas as pd
```
``` Python
#Input of the board2.xlsx file
df = pd. read_excel ("board2.xlsx" )

#Calculate the average of their scores
df ['Average'] = df.mean (numeric_only=True, axis=1)
df

Name	Gender	Track	Hometown	Math	Electronics	GEAS	Communication	Average
0	S1	Male	Instrumentation	Luzon	58	89	75	78	75.00
1	S2	Female	Communication	Mindanao	52	75	90	52	67.25
2	S3	Female	Instrumentation	Mindanao	83	74	77	57	72.75
3	S4	Male	Instrumentation	Visayas	65	58	91	68	70.50
4	S5	Male	Communication	Luzon	59	86	43	88	69.00
5	S6	Female	Microelectronics	Visayas	88	45	86	83	75.50
6	S7	Female	Instrumentation	Luzon	66	60	60	48	58.50
7	S8	Male	Instrumentation	Luzon	49	81	64	53	61.75
8	S9	Male	Instrumentation	Luzon	50	36	63	42	47.75
9	S10	Male	Microelectronics	Mindanao	80	84	61	44	67.25
10	S11	Female	Communication	Visayas	48	56	48	67	54.75
11	S12	Male	Communication	Visayas	89	67	84	64	76.00
12	S13	Female	Microelectronics	Luzon	88	35	83	43	62.25
13	S14	Female	Microelectronics	Luzon	83	77	89	73	80.50
14	S15	Female	Microelectronics	Mindanao	69	41	40	86	59.00
15	S16	Female	Communication	Luzon	71	70	87	81	77.25
16	S17	Female	Microelectronics	Mindanao	81	79	77	45	70.50
17	S18	Male	Communication	Visayas	81	40	81	52	63.50
18	S19	Male	Microelectronics	Luzon	79	63	79	71	73.00
19	S20	Female	Communication	Mindanao	59	60	62	85	66.50
20	S21	Female	Microelectronics	Visayas	83	51	68	72	68.50
21	S22	Female	Communication	Visayas	64	39	89	58	62.50
22	S23	Male	Instrumentation	Luzon	84	70	74	47	68.75
23	S24	Female	Microelectronics	Visayas	85	45	60	41	57.75
24	S25	Male	Communication	Luzon	74	91	94	42	75.25
25	S26	Female	Instrumentation	Visayas	71	47	83	62	65.75
26	S27	Male	Microelectronics	Visayas	70	47	40	86	60.75
27	S28	Male	Communication	Visayas	85	53	80	53	67.75
28	S29	Male	Instrumentation	Mindanao	73	48	71	62	63.50
29	S30	Male	Instrumentation	Luzon	78	81	57	56	68.00
```

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
