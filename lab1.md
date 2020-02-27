
# Lab 1

> Tuples, Lists and Dictionaries

List : `x = [5,6.3]`

Get `x[2]` is as simple as `print(x[2])`

Add more number to the list `x` by using `x.apppend(4)`

Tuple : `y = ('jan','feb','mar','apr','may','jun','jul','aug','sep','oct','nov','dec')`

Dictionary : `phonebook = {'Adam':'6014-7845641','Betty':'6011-78459632'}`

*Example with Lists:*


```python
x = [5,6,3]
```


```python
print(x[2])
```


```python
x.append(8)
```


```python
print(x)
```

*Example with Tuples*


```python
y = ('jan','feb','mar','apr','may','jun','jul','aug','sep','oct','nov','dec')
```


```python
print(y[0])
```

*Example with Dictionaries:*


```python
phonebook = {'Adam':'6014-7845641','Betty':'6011-78459632'}
```


```python
print(phonebook['Adam'])
```

### Application of `*key* in *dictionary*` function


```python
ages = {}

ages['Adam'] = 18
ages['Botan'] = 24
ages['Catherine'] = 14
ages['Dokutah'] = 99
```


```python
if ('Adam' in ages):
    print("Adam in ages")
else:
    print("Adam not in ages")
```

> Pandas


```python
import pandas as pd # import pandas and named it pd for easy access

step_data = [3620, 7891, 9761, 3907, 4338, 5373] # Create a list

step_counts = pd.Series(step_data,name='steps') # Convert the list into series and named it 'steps'

print(step_counts) # Display the series
```


```python
step_counts.index = pd.date_range('20150329', periods=6) # Automate assigned starting date and period of dates to all the series
```


```python
print(step_counts)
```

As can see from the result above, the date are appeared as 'key' of the series.

The 'list' are kinda become a 'dictionary' in a way.

> Exercise 1 ( Grocery Store )

*Create a dictionary of 5 item for any grocery items together with its price.*

1. Find one item in your dictionary and print the price of the item
2. Add 2 more items to the list making it 7 items


```python
items = {
    'Apple': 0.5,
    'Banana': 0.7,
    'Citrus': 0.4,
    'Dr. Pepper': 1.2,
    'Eggs': 2.5
}
```


```python
selected_item = input('Please enter an item: ')
```


```python
if (selected_item in items):
    print('The price of ' + selected_item + ' is $' + str(items[selected_item]))
else:
    print('The item you entered is not in the dictionary')
```


```python
items['Fish'] = 5.99
items['Grapes'] = 1.5
```


```python
print(items)
```
