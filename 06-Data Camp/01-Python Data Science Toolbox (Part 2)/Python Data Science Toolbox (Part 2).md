# Python Data Science Toolbox (Part 2)

Table of Content

1. Using iterators in Pythonland 

2. List comprehensions and generators

   

   ## Iterating over iterables (1)

   - Create a `for` loop to loop over `flash` and print the values in the list. Use `person` as the loop variable.
   - Create an *iterator* for the list `flash` and assign the result to `superspeed`.
   - Print each of the items from `superspeed` using `next()` 4 times.

   ```python
   # Create a list of strings: flash
   flash = ['jay garrick', 'barry allen', 'wally west', 'bart allen']
   
   # Print each list item in flash using a for loop
   for person in flash:
       print(person)
   
   # Create an iterator for flash: superspeed
   superspeed = iter(flash)
   
   # Print each item from the iterator
   print(next(superspeed))
   print(next(superspeed))
   print(next(superspeed))
   print(next(superspeed))
   ```

   

   ## Iterating over iterables (2)

   - Create an **iterator** object `small_value` over `range(3)` using the function `iter()`.
   - Using a `for` loop, iterate over `range(3)`, printing the value for every iteration. Use `num` as the loop variable.
   - Create an **iterator** object `googol` over `range(10 ** 100)

```python
# Create an iterator for range(3): small_value
small_value = iter(range(3))

# Print the values in small_value
print(next(small_value))
print(next(small_value))
print(next(small_value))

# Loop over range(3) and print the values
for num in range(3):
    print(num)

# Create an iterator for range(10 ** 100): googol
googol = iter(range(10**100))

# Print the first 5 values from googol
print(next(googol))
print(next(googol))
print(next(googol))
print(next(googol))
print(next(googol))
```

## Iterators as function arguments

- Create a `range` object that would produce the values from 10 to 20 using `range()`. Assign the result to `values`.
- Use the `list()` function to create a list of values from the range object `values`. Assign the result to `values_list`.
- Use the `sum()` function to get the sum of the values from 10 to 20 from the range object `values`. Assign the result to `values_sum`.

```python
# Create a range object: values
values = range(10,21)

# Print the range object
print(values)

# Create a list of integers: values_list
values_list = list(values)

# Print values_list
print(values_list)

# Get the sum of values: values_sum
values_sum = sum(values)

# Print values_sum
print(values_sum)

```

## Using enumerate

- Create a list of tuples from `mutants` and assign the result to `mutant_list`. Make sure you generate the tuples using `enumerate()` and turn the result from it into a list using `list()`.
- Complete the first `for` loop by unpacking the tuples generated by calling `enumerate()` on `mutants`. Use `index1` for the index and `value1` for the value when unpacking the tuple.
- Complete the second `for` loop similarly as with the first, but this time change the starting index to start from `1` by passing it in as an argument to the `start` parameter of `enumerate()`. Use `index2` for the index and `value2` for the value when unpacking the tuple.

```python
# Create a list of strings: mutants
mutants = ['charles xavier', 
            'bobby drake', 
            'kurt wagner', 
            'max eisenhardt', 
            'kitty pryde']

# Create a list of tuples: mutant_list
mutant_list = list(enumerate(mutants))

# Print the list of tuples
print(mutant_list)

# Unpack and print the tuple pairs
for  index1,value1 in enumerate(mutants):
    print(index1, value1)

# Change the start index
for index2,value2 in enumerate(mutants, start=1):
    print(index2, value2)

```

## Using zip

- Using `zip()` with `list()`, create a *list* of *tuples* from the three lists `mutants`, `aliases`, and `powers` (in that order) and assign the result to `mutant_data`.
- Using `zip()`, create a *zip object* called `mutant_zip` from the three lists `mutants`, `aliases`, and `powers`.
- Complete the `for` loop by unpacking the `zip` object you created and printing the tuple values. Use `value1`, `value2`, `value3` for the values from each of `mutants`, `aliases`, and `powers`, in that order.

```python
# Create a list of tuples: mutant_data
mutant_data = list(zip(mutants,aliases,powers))

# Print the list of tuples
print(mutant_data)

# Create a zip object using the three lists: mutant_zip
mutant_zip = zip(mutants,aliases,powers)

# Print the zip object
print(mutant_zip)

# Unpack the zip object and print the tuple values
for value1,value2,value3 in mutant_zip:
    print(value1, value2, value3)
```

## Using * and zip to 'unzip'

```python
# Create a zip object from mutants and powers: z1
z1 = zip(mutants,powers)

# Print the tuples in z1 by unpacking with *
print(*z1)

# Re-create a zip object from mutants and powers: z1
z1 = zip(mutants,powers)

# 'Unzip' the tuples in z1 by unpacking with * and zip(): result1, result2
result1, result2 = zip(*z1)

# Check if unpacked tuples are equivalent to original tuples
print(result1 == mutants)
print(result2 == powers)

```
