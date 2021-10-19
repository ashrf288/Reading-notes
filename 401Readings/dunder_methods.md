# Dunder Methods
 They are easy to recognize because they start and end with double underscores, for example` __init__ `or `__str__`.

 sometimes called **magic methods.**

## 1-Object Initialization:` __init__`

construct account objects from the Account class I need a constructor (setting up the object)
 ```
class Account:
    """A simple account class"""

    def __init__(self, owner, amount=0):
        """
        This is the constructor that lets us create
        objects from this class
        """
        self.owner = owner
        self.amount = amount
        self._transactions = []
 ```


## Object Representation: `__str__`, `__repr__`
provide a string representation of your object for the consumer of your class
+ __repr__: The “official” string representation of an object
+ __str__: The “informal” or nicely printable string representation of an object.


## Iteration: `__len__`,` __getitem__`, `__reversed__`

to iterate over our account object

```
    def __len__(self):
        return len(self._transactions)

    def __getitem__(self, position):
        return self._transactions[position]
```

### To iterate over transactions in reversed order you can implement the __reversed__ special method:
```
def __reversed__(self):
    return self[::-1]
```

## Operator Overloading for Comparing : `__eq__`,` __lt__`

to compare Python objects

```
from functools import total_ordering

@total_ordering
class Account:
    # ... (see above)

    def __eq__(self, other):
        return self.balance == other.balance

    def __lt__(self, other):
        return self.balance < other.balance
```


## Operator Overloading for Merging  `__add__`

```
def __add__(self, other):
    owner = '{}&{}'.format(self.owner, other.owner)
    start_amount = self.amount + other.amount
    acc = Account(owner, start_amount)
    for t in list(self) + list(other):
        acc.add_transaction(t)
    return acc
```


## Callable Python Objects: `__call__`

make an object callable like a regular function 

```
  def __call__(self):
        print('Start amount: {}'.format(self.amount))
        print('Transactions: ')
        for transaction in self:
            print(transaction)
        print('\nBalance: {}'.format(self.balance))
```

to call it
`acc()`

## Context Manager Support and the With Statement: `__enter__`, `__exit__`




# probability and statistics 


![](https://i.imgur.com/egqrj58.jpg)


## probability

What is the chance of an event happening,event is some outcome of interest

the high point in a normal distribution represents the event with the **highest probability** of occurring. As you get farther away from this event on either side, the probability drops rapidly, forming that familiar **bell-shape.**

## statistics 

The high point in a statistical context actually represents the **mean.** As in probability, as you get farther from the mean, you rapidly drop off in frequency. That is to say, extremely high and low deviations from the mean are present but exceedingly **rare**.

## Central Limit Theorem

 Central Limit Theorem dictates that the distribution of these estimates will look like a normal distribution


 ###  Three Sigma Rule
The arithmetic mean is the simplest and most widely used measure of a mean, or average. 

![](https://i.imgur.com/Mt3RyE0.png)



### Z-score

A Z-score is a numerical measurement that describes a value's relationship to the mean of a group of values. Z-score is measured in terms of standard deviations from the mean. 

![](https://i.imgur.com/3TuDF4G.jpg)

