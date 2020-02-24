# Database & Analytics Programming

This is a repo for the module Databases and Analytics Programming.


Programs for all the Labs will be added to this as and when I complete them.

## Programs


### Pascal's Triangle
Create an empty dictionary object called myDict . Using a loop structure, add an entry to myDict for each value in myList . The key values for entries in myDict should be integer values commencing at 0.


```
def printPascals(num):
    feed = [0, 1, 0]
    print(*feed[1:len(feed)-1], sep = '\t')
    for j in range(num-1):
        newFeed = [0]
        lengthOfFeed = len(feed) - 1
        for i in range(lengthOfFeed):
            newFeed.append(feed[i] + feed[i+1])
        newFeed.append(0)
        print(*newFeed[1:len(newFeed)-1], sep = '\t')
        feed = newFeed

printPascals(int(input('Enter number of rows:')))
```

Here the feed array is used as a starting poing for the algorithm.
**Every array has a starting 0 and a trailing 0 to facilitate the correct addition of the elements.**

`feed` array is used to calculate the next row in the pascals triangle, which is stored in the `newFeed` array.

`    print(*feed[1:len(feed)-1], sep = '\t')`

The above print statement prints all the elements in the list `feed` except for first and last element. And the elements are seperated by a tab character `\t`.

**Logic for Pascals:**

![alt text](https://github.com/sab3r-ncirl/dap/blob/master/Images/pascals.PNG "Pascals Triangle Logic")