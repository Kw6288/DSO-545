# 1. Writing your own functions



## #Q1. Write a simple function

```python
# Define the function shout
def shout():
    """Print a string with three exclamation marks"""
    # Concatenate the strings: shout_word
    
    shout_word = 'congratulations'+'!!!'
    # Print shout_word
    print(shout_word)

# Call shout
shout()
```

## #Q2. Single parameter function

```python
# Define shout with the parameter, word
def shout(word):
    """Print a string with three exclamation marks"""
    # Concatenate the strings: shout_word
    shout_out = word + '!!!'

    # Print shout_word
    print(shout_out)

# Call shout with the string 'congratulations'
shout('congratulations')		
```

## #Q3. Functions that return single values

```python
# Define shout with the parameter, word
def shout(word):
    """Return a string with three exclamation marks"""
    # Concatenate the strings: shout_word
    shout_word = word +'!!!'

    # Replace print with return
    return(shout_word)

# Pass 'congratulations' to shout: yell
yell = shout('congratulations')

# Print yell
print(yell)
```



```python
# Select retweets from the Twitter DataFrame: result
result = filter(lambda x:x[0:2]=='RT', tweets_df['text'])

# Create list from filter object result: res_list
res_list= list(result)

# Print all retweets in res_list
for tweet in res_list:
    print(tweet)
```

