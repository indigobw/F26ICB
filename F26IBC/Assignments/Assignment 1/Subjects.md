```python
#Opening the file nad trying to get the values
```


```python
counts = {}

with open("C:/Users/VivaA/2214/IntroBiolComp-2026/Assignment1/Gesquiere2011_data.csv", "r") as file:
    next(file)

    for line in file:
        values = line.split()

        if values:
            individual = values[0]
            counts[individual] = counts.get(individual, 0) + 1
    print(individual, count)
```

    127 13
    


```python
#Finding Individaul 8
```


```python
counts = {}

with open("C:/Users/VivaA/2214/IntroBiolComp-2026/Assignment1/Gesquiere2011_data.csv", "r") as file:
    next(file)

    for line in file:
        values = line.split()

        if values:
            individual = values[0]
            counts[individual] = counts.get(individual, 0) + 1

maleID = input("Enter maleID")

if maleID in counts:
    print("maleID", maleID)
    print("Num_samples:", counts[maleID])
else:
    print("Individual not found")
```

    Enter maleID 8
    

    maleID 8
    Num_samples: 17
    


```python
#Finding Individual 22
```


```python
counts = {}

with open("C:/Users/VivaA/2214/IntroBiolComp-2026/Assignment1/Gesquiere2011_data.csv", "r") as file:
    next(file)

    for line in file:
        values = line.split()

        if values:
            individual = values[0]
            counts[individual] = counts.get(individual, 0) + 1

maleID = input("Enter maleID")

if maleID in counts:
    print("maleID", maleID)
    print("Num_samples:", counts[maleID])
else:
    print("Individual not found")
```

    Enter maleID 22
    

    maleID 22
    Num_samples: 5
    


```python
#Pulling the file and finding the individuals
```


```python
counts = {}

with open("C:/Users/VivaA/2214/IntroBiolComp-2026/Assignment1/Gesquiere2011_data.csv", "r") as file:
    for line in file:
        values = line.split() #Had to split to get the right number for the maleID

        if values:
            individual = values[0]
            counts[individual] = counts.get(individual, 0) + 1

for individual, count in counts.items():
    print(individual, count)
```

    maleID 1
    1 10
    2 2
    3 61
    4 46
    5 28
    6 7
    7 5
    8 17
    9 4
    10 21
    11 26
    12 23
    13 16
    14 1
    15 40
    16 31
    17 3
    18 4
    19 3
    20 4
    21 12
    22 5
    23 36
    24 35
    25 35
    26 22
    27 5
    29 33
    30 63
    31 1
    32 3
    33 1
    34 16
    35 5
    36 39
    37 38
    38 1
    39 3
    40 32
    41 53
    42 5
    43 2
    44 56
    45 1
    46 24
    47 34
    48 23
    49 19
    50 21
    51 25
    52 6
    53 3
    54 22
    55 20
    56 41
    57 46
    58 1
    59 25
    60 51
    61 20
    62 13
    63 35
    64 34
    65 38
    66 20
    67 1
    68 10
    69 22
    70 33
    71 5
    72 2
    73 10
    74 1
    75 15
    76 39
    77 2
    78 29
    79 4
    80 35
    81 1
    82 27
    83 2
    84 11
    85 1
    86 39
    87 18
    88 46
    89 25
    90 24
    91 32
    92 1
    93 7
    94 25
    95 71
    96 17
    97 17
    98 5
    99 2
    100 13
    101 26
    102 15
    103 26
    104 29
    105 6
    106 46
    107 7
    108 41
    109 28
    110 3
    111 24
    112 3
    113 1
    114 1
    115 1
    116 14
    118 23
    119 1
    120 42
    121 12
    122 9
    123 39
    124 1
    125 39
    126 15
    127 13
    


```python
#Need to skip the first row
```


```python
counts = {}

with open("C:/Users/VivaA/2214/IntroBiolComp-2026/Assignment1/Gesquiere2011_data.csv", "r") as file:
    next(file)
    for line in file:
        values = line.split() #Had to split to get the right number for the maleID

        if values:
            individual = values[0]
            counts[individual] = counts.get(individual, 0) + 1

for individual, count in counts.items():
    print(individual, count)
```

    1 10
    2 2
    3 61
    4 46
    5 28
    6 7
    7 5
    8 17
    9 4
    10 21
    11 26
    12 23
    13 16
    14 1
    15 40
    16 31
    17 3
    18 4
    19 3
    20 4
    21 12
    22 5
    23 36
    24 35
    25 35
    26 22
    27 5
    29 33
    30 63
    31 1
    32 3
    33 1
    34 16
    35 5
    36 39
    37 38
    38 1
    39 3
    40 32
    41 53
    42 5
    43 2
    44 56
    45 1
    46 24
    47 34
    48 23
    49 19
    50 21
    51 25
    52 6
    53 3
    54 22
    55 20
    56 41
    57 46
    58 1
    59 25
    60 51
    61 20
    62 13
    63 35
    64 34
    65 38
    66 20
    67 1
    68 10
    69 22
    70 33
    71 5
    72 2
    73 10
    74 1
    75 15
    76 39
    77 2
    78 29
    79 4
    80 35
    81 1
    82 27
    83 2
    84 11
    85 1
    86 39
    87 18
    88 46
    89 25
    90 24
    91 32
    92 1
    93 7
    94 25
    95 71
    96 17
    97 17
    98 5
    99 2
    100 13
    101 26
    102 15
    103 26
    104 29
    105 6
    106 46
    107 7
    108 41
    109 28
    110 3
    111 24
    112 3
    113 1
    114 1
    115 1
    116 14
    118 23
    119 1
    120 42
    121 12
    122 9
    123 39
    124 1
    125 39
    126 15
    127 13
    


```python
#Need to add the right headers
```


```python
counts = {}

with open("C:/Users/VivaA/2214/IntroBiolComp-2026/Assignment1/Gesquiere2011_data.csv", "r") as file:
    next(file)
    for line in file:
        values = line.split() #Had to split to get the right number for the maleID

        if values:
            individual = values[0]
            counts[individual] = counts.get(individual, 0) + 1
print("maleID", "Num_samples", sep="\t")

for individual, count in counts.items():
    print(individual, count)
```

    maleID	Num_samples
    1 10
    2 2
    3 61
    4 46
    5 28
    6 7
    7 5
    8 17
    9 4
    10 21
    11 26
    12 23
    13 16
    14 1
    15 40
    16 31
    17 3
    18 4
    19 3
    20 4
    21 12
    22 5
    23 36
    24 35
    25 35
    26 22
    27 5
    29 33
    30 63
    31 1
    32 3
    33 1
    34 16
    35 5
    36 39
    37 38
    38 1
    39 3
    40 32
    41 53
    42 5
    43 2
    44 56
    45 1
    46 24
    47 34
    48 23
    49 19
    50 21
    51 25
    52 6
    53 3
    54 22
    55 20
    56 41
    57 46
    58 1
    59 25
    60 51
    61 20
    62 13
    63 35
    64 34
    65 38
    66 20
    67 1
    68 10
    69 22
    70 33
    71 5
    72 2
    73 10
    74 1
    75 15
    76 39
    77 2
    78 29
    79 4
    80 35
    81 1
    82 27
    83 2
    84 11
    85 1
    86 39
    87 18
    88 46
    89 25
    90 24
    91 32
    92 1
    93 7
    94 25
    95 71
    96 17
    97 17
    98 5
    99 2
    100 13
    101 26
    102 15
    103 26
    104 29
    105 6
    106 46
    107 7
    108 41
    109 28
    110 3
    111 24
    112 3
    113 1
    114 1
    115 1
    116 14
    118 23
    119 1
    120 42
    121 12
    122 9
    123 39
    124 1
    125 39
    126 15
    127 13
    


```python
#Add tab separation between values
```


```python
counts = {}

with open("C:/Users/VivaA/2214/IntroBiolComp-2026/Assignment1/Gesquiere2011_data.csv", "r") as file:
    next(file)
    for line in file:
        values = line.split() #Had to split to get the right number for the maleID

        if values:
            individual = values[0]
            counts[individual] = counts.get(individual, 0) + 1
print("maleID", "Num_samples", sep="\t")

for individual, count in counts.items():
    print(individual, count, sep="\t")
```

    maleID	Num_samples
    1	10
    2	2
    3	61
    4	46
    5	28
    6	7
    7	5
    8	17
    9	4
    10	21
    11	26
    12	23
    13	16
    14	1
    15	40
    16	31
    17	3
    18	4
    19	3
    20	4
    21	12
    22	5
    23	36
    24	35
    25	35
    26	22
    27	5
    29	33
    30	63
    31	1
    32	3
    33	1
    34	16
    35	5
    36	39
    37	38
    38	1
    39	3
    40	32
    41	53
    42	5
    43	2
    44	56
    45	1
    46	24
    47	34
    48	23
    49	19
    50	21
    51	25
    52	6
    53	3
    54	22
    55	20
    56	41
    57	46
    58	1
    59	25
    60	51
    61	20
    62	13
    63	35
    64	34
    65	38
    66	20
    67	1
    68	10
    69	22
    70	33
    71	5
    72	2
    73	10
    74	1
    75	15
    76	39
    77	2
    78	29
    79	4
    80	35
    81	1
    82	27
    83	2
    84	11
    85	1
    86	39
    87	18
    88	46
    89	25
    90	24
    91	32
    92	1
    93	7
    94	25
    95	71
    96	17
    97	17
    98	5
    99	2
    100	13
    101	26
    102	15
    103	26
    104	29
    105	6
    106	46
    107	7
    108	41
    109	28
    110	3
    111	24
    112	3
    113	1
    114	1
    115	1
    116	14
    118	23
    119	1
    120	42
    121	12
    122	9
    123	39
    124	1
    125	39
    126	15
    127	13
    


```python
#Saving as csv file
```


```python
counts = {}

with open("C:/Users/VivaA/2214/IntroBiolComp-2026/Assignment1/Gesquiere2011_data.csv", "r") as file:
    next(file)
    for line in file:
        values = line.split() #Had to split to get the right number for the maleID

        if values:
            individual = values[0]
            counts[individual] = counts.get(individual, 0) + 1

with open("C:/Users/VivaA/2214/F26IBC/Assignments/Assignment 1/Num_samples.csv", "w", newline="") as output_file:
    writer = csv.writer(output_file)
    writer.writerow(["maleID", "Num_samples"])

    for individual, count in counts.items():
        writer.writerow([individual, count])

print("Sample counts saved to Num_samples.csv")
```

    Sample counts saved to Num_samples.csv
    


```python

```
