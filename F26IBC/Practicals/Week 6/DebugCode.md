```python
#Fought for my life trying to get this message to not give me an error back (besides the error in the output)
```


```python
import pickle
genetic_code = pickle.load(open("C:/Users/VivaA/2214/IntroBiolComp-2026/Python/genetic_code.pickle", "rb"))

test_mRNA = "AUGGAAUUCUCGCUCUGAAGGUAA"

def get_amino_acids(mRNA):
    i = 0
    aa_sequence = []
    while (i + 3) < len(mRNA):
        codon = mRNA[i:(i + 3)]
        aa = genetic_code[codon]
        if aa == "Stop":
            break
        else:
            aa_sequence.append(aa)
        i = i + 4
    return "".join(aa_sequence)

print(get_amino_acids(test_mRNA))
```

    MNLLEV
    


```python
#Trying to identify the what each line is doing
```


```python
#This is telling python that I'm using pickle
import pickle
#This defines what "genetic_code" is and where to fine it in my files
genetic_code = pickle.load(open("C:/Users/VivaA/2214/IntroBiolComp-2026/Python/genetic_code.pickle", "rb"))

#This is defining what sequence the mRNA is
test_mRNA = "AUGGAAUUCUCGCUCUGAAGGUAA"

#This makes the first function that has to get the amino acids using the mRNA from the previous command
def get_amino_acids(mRNA):
    #This makes i a variable that's set to 0
    i = 0
    #This makes a place for the new data to go
    aa_sequence = []
    #This tells python that while i is less than the amount of nucleotides in the mRNA to keep searching
    while (i + 3) < len(mRNA):
        #This tells python that a codon is made up of i to i = 3
        codon = mRNA[i:(i + 3)]
        #This tells python to use the genetic_code file from the first command to read the sequence
        aa = genetic_code[codon]
        #This tells python to check for a stop codon, if it finds one, stop sequencing
        if aa == "Stop":
            break
        #If it doesn't find a stop sequence, keep going
        else:
            aa_sequence.append(aa)
        #Then go back and start on the i value plus 4
        i = i + 4
    #This makes all the amino acids that were individually found into one sequence
    return "".join(aa_sequence)

#This prints out the amino acid sequence
print(get_amino_acids(test_mRNA))
```

    MNLLEV
    


```python
import pdb
def get_amino_acids(mRNA):
    i = 0
    aa_sequence = []
    while (i + 3) < len(mRNA):
        codon = mRNA[i:(i + 3)]
        aa = genetic_code[codon]
        if aa == "Stop":
            break
        else:
            aa_sequence.append(aa)
        i = i + 4
    return "".join(aa_sequence)
pdb.set_trace()
print(get_amino_acids(test_mRNA))
```

    > [32mc:\users\vivaa\appdata\local\temp\ipykernel_22088\1822780433.py[39m([92m14[39m)[36m<module>[39m[34m()[39m
    
    

    ipdb>  i = i + 4
    

    *** NameError: name 'i' is not defined
    

    ipdb>  q
    


```python
#The issue with the code is that after it translates a codon, the next set of nucleotides is started 4 after the current one, that's not how codons work
```


```python
#The command after else should be i = i + 3
```


```python
#Correct code
```


```python
import pickle
genetic_code = pickle.load(open("C:/Users/VivaA/2214/IntroBiolComp-2026/Python/genetic_code.pickle", "rb"))

test_mRNA = "AUGGAAUUCUCGCUCUGAAGGUAA"

def get_amino_acids(mRNA):
    i = 0
    aa_sequence = []
    while (i + 3) < len(mRNA):
        codon = mRNA[i:(i + 3)]
        aa = genetic_code[codon]
        if aa == "Stop":
            break
        else:
            aa_sequence.append(aa)
        i = i + 3
    return "".join(aa_sequence)

print(get_amino_acids(test_mRNA))
```

    MEFSL
    


```python

```
