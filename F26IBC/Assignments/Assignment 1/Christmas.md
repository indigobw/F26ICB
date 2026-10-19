```python
#Defining the variables in the song
```


```python
days = ["First", "Second", "Third", "Fourth", "Fifth", "Sixth", "Seventh", "Eighth", "Ninth", "Tenth", "Eleventh", "Twelfth",]
gifts = ["A partridge in a pear tree", "Two turtle doves", "Three French hens", "Four calling birds", "Five golden rings", "Six geense a-laying", 
         "Seven swans a-swimming", "Eight maids a-milking", "Nine ladies dancing", "Ten lords a-leaping", "Eleven pipers piping", 
         "Twelve drummers drumming",]
```


```python
#Trying out a loop
```


```python
for i in range(12):
    print("On the", days[i], "day of Christmas")
    print("my true love gave to me")
```

    On the First day of Christmas
    my true love gave to me
    On the Second day of Christmas
    my true love gave to me
    On the Third day of Christmas
    my true love gave to me
    On the Fourth day of Christmas
    my true love gave to me
    On the Fifth day of Christmas
    my true love gave to me
    On the Sixth day of Christmas
    my true love gave to me
    On the Seventh day of Christmas
    my true love gave to me
    On the Eighth day of Christmas
    my true love gave to me
    On the Ninth day of Christmas
    my true love gave to me
    On the Tenth day of Christmas
    my true love gave to me
    On the Eleventh day of Christmas
    my true love gave to me
    On the Twelfth day of Christmas
    my true love gave to me
    


```python
#Adding another loop - for the gifts
```


```python
for i in range(12):
    print("On the", days[i], "day of Christmas my true love gave to me:")
    for j in range(1, 12):
        print(gifts[j])
```

    On the First day of Christmas my true love gave to me:
    Two turtle doves
    Three French hens
    Four calling birds
    Five golden rings
    Six geense a-laying
    Seven swans a-swimming
    Eight maids a-milking
    Nine ladies dancing
    Ten lords a-leaping
    Eleven pipers piping
    Twelve drummers drumming
    On the Second day of Christmas my true love gave to me:
    Two turtle doves
    Three French hens
    Four calling birds
    Five golden rings
    Six geense a-laying
    Seven swans a-swimming
    Eight maids a-milking
    Nine ladies dancing
    Ten lords a-leaping
    Eleven pipers piping
    Twelve drummers drumming
    On the Third day of Christmas my true love gave to me:
    Two turtle doves
    Three French hens
    Four calling birds
    Five golden rings
    Six geense a-laying
    Seven swans a-swimming
    Eight maids a-milking
    Nine ladies dancing
    Ten lords a-leaping
    Eleven pipers piping
    Twelve drummers drumming
    On the Fourth day of Christmas my true love gave to me:
    Two turtle doves
    Three French hens
    Four calling birds
    Five golden rings
    Six geense a-laying
    Seven swans a-swimming
    Eight maids a-milking
    Nine ladies dancing
    Ten lords a-leaping
    Eleven pipers piping
    Twelve drummers drumming
    On the Fifth day of Christmas my true love gave to me:
    Two turtle doves
    Three French hens
    Four calling birds
    Five golden rings
    Six geense a-laying
    Seven swans a-swimming
    Eight maids a-milking
    Nine ladies dancing
    Ten lords a-leaping
    Eleven pipers piping
    Twelve drummers drumming
    On the Sixth day of Christmas my true love gave to me:
    Two turtle doves
    Three French hens
    Four calling birds
    Five golden rings
    Six geense a-laying
    Seven swans a-swimming
    Eight maids a-milking
    Nine ladies dancing
    Ten lords a-leaping
    Eleven pipers piping
    Twelve drummers drumming
    On the Seventh day of Christmas my true love gave to me:
    Two turtle doves
    Three French hens
    Four calling birds
    Five golden rings
    Six geense a-laying
    Seven swans a-swimming
    Eight maids a-milking
    Nine ladies dancing
    Ten lords a-leaping
    Eleven pipers piping
    Twelve drummers drumming
    On the Eighth day of Christmas my true love gave to me:
    Two turtle doves
    Three French hens
    Four calling birds
    Five golden rings
    Six geense a-laying
    Seven swans a-swimming
    Eight maids a-milking
    Nine ladies dancing
    Ten lords a-leaping
    Eleven pipers piping
    Twelve drummers drumming
    On the Ninth day of Christmas my true love gave to me:
    Two turtle doves
    Three French hens
    Four calling birds
    Five golden rings
    Six geense a-laying
    Seven swans a-swimming
    Eight maids a-milking
    Nine ladies dancing
    Ten lords a-leaping
    Eleven pipers piping
    Twelve drummers drumming
    On the Tenth day of Christmas my true love gave to me:
    Two turtle doves
    Three French hens
    Four calling birds
    Five golden rings
    Six geense a-laying
    Seven swans a-swimming
    Eight maids a-milking
    Nine ladies dancing
    Ten lords a-leaping
    Eleven pipers piping
    Twelve drummers drumming
    On the Eleventh day of Christmas my true love gave to me:
    Two turtle doves
    Three French hens
    Four calling birds
    Five golden rings
    Six geense a-laying
    Seven swans a-swimming
    Eight maids a-milking
    Nine ladies dancing
    Ten lords a-leaping
    Eleven pipers piping
    Twelve drummers drumming
    On the Twelfth day of Christmas my true love gave to me:
    Two turtle doves
    Three French hens
    Four calling birds
    Five golden rings
    Six geense a-laying
    Seven swans a-swimming
    Eight maids a-milking
    Nine ladies dancing
    Ten lords a-leaping
    Eleven pipers piping
    Twelve drummers drumming
    


```python
#Didn't define the second loop right, time to start experimenting
```


```python
for i in range(12):
    print("On the", days[i], "day of Christmas my true love gave to me:")
    for j in range(i, 1, -1):
        print(gifts[j])
```

    On the First day of Christmas my true love gave to me:
    On the Second day of Christmas my true love gave to me:
    On the Third day of Christmas my true love gave to me:
    Three French hens
    On the Fourth day of Christmas my true love gave to me:
    Four calling birds
    Three French hens
    On the Fifth day of Christmas my true love gave to me:
    Five golden rings
    Four calling birds
    Three French hens
    On the Sixth day of Christmas my true love gave to me:
    Six geense a-laying
    Five golden rings
    Four calling birds
    Three French hens
    On the Seventh day of Christmas my true love gave to me:
    Seven swans a-swimming
    Six geense a-laying
    Five golden rings
    Four calling birds
    Three French hens
    On the Eighth day of Christmas my true love gave to me:
    Eight maids a-milking
    Seven swans a-swimming
    Six geense a-laying
    Five golden rings
    Four calling birds
    Three French hens
    On the Ninth day of Christmas my true love gave to me:
    Nine ladies dancing
    Eight maids a-milking
    Seven swans a-swimming
    Six geense a-laying
    Five golden rings
    Four calling birds
    Three French hens
    On the Tenth day of Christmas my true love gave to me:
    Ten lords a-leaping
    Nine ladies dancing
    Eight maids a-milking
    Seven swans a-swimming
    Six geense a-laying
    Five golden rings
    Four calling birds
    Three French hens
    On the Eleventh day of Christmas my true love gave to me:
    Eleven pipers piping
    Ten lords a-leaping
    Nine ladies dancing
    Eight maids a-milking
    Seven swans a-swimming
    Six geense a-laying
    Five golden rings
    Four calling birds
    Three French hens
    On the Twelfth day of Christmas my true love gave to me:
    Twelve drummers drumming
    Eleven pipers piping
    Ten lords a-leaping
    Nine ladies dancing
    Eight maids a-milking
    Seven swans a-swimming
    Six geense a-laying
    Five golden rings
    Four calling birds
    Three French hens
    


```python
#Fixing the first three days
```


```python
for i in range(12):
    print("On the", days[i], "day of Christmas my true love gave to me:")
    for j in range(i, -1, -1):
        print(gifts[j])
```

    On the First day of Christmas my true love gave to me:
    A partridge in a pear tree
    On the Second day of Christmas my true love gave to me:
    Two turtle doves
    A partridge in a pear tree
    On the Third day of Christmas my true love gave to me:
    Three French hens
    Two turtle doves
    A partridge in a pear tree
    On the Fourth day of Christmas my true love gave to me:
    Four calling birds
    Three French hens
    Two turtle doves
    A partridge in a pear tree
    On the Fifth day of Christmas my true love gave to me:
    Five golden rings
    Four calling birds
    Three French hens
    Two turtle doves
    A partridge in a pear tree
    On the Sixth day of Christmas my true love gave to me:
    Six geense a-laying
    Five golden rings
    Four calling birds
    Three French hens
    Two turtle doves
    A partridge in a pear tree
    On the Seventh day of Christmas my true love gave to me:
    Seven swans a-swimming
    Six geense a-laying
    Five golden rings
    Four calling birds
    Three French hens
    Two turtle doves
    A partridge in a pear tree
    On the Eighth day of Christmas my true love gave to me:
    Eight maids a-milking
    Seven swans a-swimming
    Six geense a-laying
    Five golden rings
    Four calling birds
    Three French hens
    Two turtle doves
    A partridge in a pear tree
    On the Ninth day of Christmas my true love gave to me:
    Nine ladies dancing
    Eight maids a-milking
    Seven swans a-swimming
    Six geense a-laying
    Five golden rings
    Four calling birds
    Three French hens
    Two turtle doves
    A partridge in a pear tree
    On the Tenth day of Christmas my true love gave to me:
    Ten lords a-leaping
    Nine ladies dancing
    Eight maids a-milking
    Seven swans a-swimming
    Six geense a-laying
    Five golden rings
    Four calling birds
    Three French hens
    Two turtle doves
    A partridge in a pear tree
    On the Eleventh day of Christmas my true love gave to me:
    Eleven pipers piping
    Ten lords a-leaping
    Nine ladies dancing
    Eight maids a-milking
    Seven swans a-swimming
    Six geense a-laying
    Five golden rings
    Four calling birds
    Three French hens
    Two turtle doves
    A partridge in a pear tree
    On the Twelfth day of Christmas my true love gave to me:
    Twelve drummers drumming
    Eleven pipers piping
    Ten lords a-leaping
    Nine ladies dancing
    Eight maids a-milking
    Seven swans a-swimming
    Six geense a-laying
    Five golden rings
    Four calling birds
    Three French hens
    Two turtle doves
    A partridge in a pear tree
    


```python

```
