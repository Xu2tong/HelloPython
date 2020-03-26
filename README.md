# HelloPython
My learning notes of Python 101

IBM course of Data Science with Python

Dictionary:

>grades = {'Ana':'B','John':'A+','Denise':'A','Katy':'A'}
>grades['John']: A+
>grades['Tongtong']: Error
>grades['Tongtong'] = 'A+'
>del(grades['Ana']) --> grades of Ana is now deleted

```
grades.keys() --> lists out all the keys
grades.values()--> lists out all the values
```

```
animals = { 'a': ['aardvark'], 'b': ['baboon'], 'c': ['coati']}
animals['d'] = ['donkey']
animals['d'].append('dog')
animals['d'].append('dingo')
aDict = animals
def how_many(aDict):
    i = 0
    for key in aDict:
        i += len(aDict[key])
    return i
```
>aDict: A dictionary, where all the values are lists.
>returns: int, how many individual values are in the dictionary.

```
def how_many(aDict): 
    result = 0
    for value in aDict.values():
        # Since all the values of aDict are lists, aDict.values() will 
        #  be a list of lists
        result += len(value)
    return result
```

>aDict: A dictionary, where all the values are lists.
>returns: The key with the largest number of values associated with it

```
def biggest(aDict):
    result = None
    biggestValue = 0
    for key in aDict.keys():
        if len(aDict[key])>= biggestValue:
            result = key
            biggestValue = len(aDict[key])
        return result
```

```
def biggest(aDict):
    return max((len(aDict[k]), k) for k in aDict)
```

>aList = (len(aDict[key]),key)

```
def fib_efficient (n,d):
    if n in d:
        return d[n]
    else:
        ans = fib_efficient (n-1, d)+fib_efficient (n-2,d)
        d[n]=ans
        return ans
d = {0:0,1:1}
print (fib_efficient(6,d))
```

```
def fib(n):
    if n==0 or n==1:
        return n
    else:
        return fib(n-1) + fib(n-2)
    
print (fib(6))
```




