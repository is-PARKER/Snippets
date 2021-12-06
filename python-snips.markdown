# Python Snips #

Python Snips is intended to highlight useful Python methods, modules, libraries, etc.

### setdefault() and defaultdict() ###


```
periodic_table = {'Hydrogen':1, "Helium":2}
carbon = periodic_table.setdefault('Carbon',12)
helium = periodic_table.setdefault('Helium',947)
print(helium) ## Returns 2 because the setdefault doesn't allow the overwrite
```

Another option is to use defaultdict() which accoomplishes a few things. 

First, it can provide a default answer when key is asked for that doesn't have a value. 

```
from collections import defaultdict

def no_idea():
  return "huh?"
  
bestiary = defaultdict(no_idea)
print(bestiary['b']) ##  Returns "huh?" because there are no keys with 'b'
```

Additionally, the defaultdict() can be used to instance a dictionary and provide a default so that it doesn't need to be defined.

```
from collections import defaultdict

food_counter = defaultdict(int)
for food in ['spam', 'spam', 'eggs', 'spam']:
    food_counter[food] += 1

for food, count in food_counter.items():
    print(food,count)
```

The alternative would like:

```


dict_counter = {}
for food in ['spam','spam','eggs','spam']
  if not food in dict_counter:
    dict_counter[food] = 0 
  dict_counter[food] += 1
  
for food, count in dict_counter.items():
  print(food,count)
```

### Random Module ###

Choice is simple for selecting a single item:

``` from random import choice 

fusion = ['wasabi', 'sushi', 'rice', 'tofu', 'sesame']

print(choice(fusion)) 
print(choice(fusion))
print(choice(fusion))

#Sushi
#Wasabi
#rice

```

Another is sample:

```
from random import sample 

numbers = [23, 45, 65, 76, 33, 45, 11, 22, 33]

nums = sample(numbers, 3)

print(nums)

#[45,76,33]

```

Then there is randin() and randrange
```
from random import randint

print(randint(38,74))

from random import randrange

print(randrange(38, 78))
```

With the above randrange() is half-open interval and doesn't include the last interval. 



