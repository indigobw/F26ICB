```python
#Step 1: Preperation
```


```python
#Preheat_oven(400) #Will be in °F
#Grease_Pan()
#Get_bowls()
#Get_measuringcupes()
```


```python
#Step 2: Make Batter
```


```python
#Flour = 2 cups
#Sugar = 1.5 cups
#Eggs = 4
#Butter = 0.5 cups
#Milk = 1 cup
#Vanilla = 3 tsp
#Oil = 3 tsp
```


```python
#Mix Flour AND Sugar IN Bowl
#Add Eggs AND Milk
#MIX
#Add Vanilla AND Oil
#BEAT thoroughly UNTIL smooth
```


```python
#Step 3: Bake
```


```python
#POUR batter IN Grease_Pan
#Put Grease_Pan IN Oven
#START timer(20) #In minutes
#WHILE timer > 0, wait
#WHEN timer = 0, end timer
```


```python
#If Inserted_knife = Clean THEN
#Print(Cake is Ready)
#Else: START timer (5)
#WHEN timer = 0, loop to knife

#AFTER Insereted_knife = Clean
#TAKE Grease_Pan OUT of Oven
#Cool Cake ON Rack
```


```python
#End seqeunce
```
>[!NOTE]
>This is good overall, but it may have been more helpful to put your `if`/`else` statements inside a`while` loop that runs while the knife comes out with batter, since this would be more similar to how you'd code this in most languages. I see that you did something similar, but writing it out in a little more "code-y" way can help translate pseudocode to code. For example
>
>```
>Cake = "not_done"
>
>while Cake == "not_done"
>    Inserted_knife = insert_knife(cake)
>    if Inserted_knife == Clean
>        Cake = "done"
>        Print(Cake is Ready)
>    else
>        START timer (5)
>
>TAKE Grease_Pan OUT of Oven
>Cool Cake ON Rack
>````
