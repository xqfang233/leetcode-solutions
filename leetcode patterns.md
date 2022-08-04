# Two pointers

## same direction

 ```
 0, ..., i-->, ..., j-->, ..., end
 
[0:i): processed
[i:j): processed but do not want
[j:]: unprocessed

 ```


## opposite direction

```
0, ..., i-->, ... <--j, ..., end

[0:i),[j:]: processed
[i:j): unprocessed

```

## related problems

- [x] 344. reversed string
- [x] 26. remove duplicate
```
same direction, compare nums[i-1] with nums[j]
```
- [x] 11. container with most water
```
compare the height[l] and height[r], move the shorter one to the middle
```
- [ ] 42. trapping rain water
- [ ] 283.moving zeros
- [ ] 80. remove duplicate II
- [ ] 1047. remove all adjacent duplicates in string



# Binary search
+ shrink the search range in every iteration
+ can't exclude the potential result when shrinking


## 3 templates
### find an accurate value
+ l<=r
+ l = mid + 1, r = mid - 1


### find a vague value
+ l < r
+ l = mid, r =mid-1 or l = mid+1, r = mid

### general purpose
+ l < r-1
+ l = mid, r = mid


## problems
- [ ] 1062
- [ ] 410
- [ ] 1231
- [ ] 852
- [ ] 1011
- [ ] 1292






# Single Linked list

## iteration
two pointers
+ direction: same direction
+ distance between two pointers
+ the moving speed of two pointers


eg:
1. **find mid node of a linked list**

```
1 --> 2 --> 3 --> 4 --> 5
i
j


1 --> 2 --> 3 --> 4 --> 5
      i
            j
            
1 --> 2 --> 3 --> 4 --> 5
            i
                        j
                                   
```

same starting point, while fast pointer (j) still inside bound(j and j.next not null):
  j (fast) moves 2 steps forward, i (slow) moves 1 step forward

return the node that i points to



2. find the last kth node

```
k = 2

1 --> 2 --> 3 --> 4 --> 5
i
            j

1 --> 2 --> 3 --> 4 --> 5
      i
                        j
                        
1 --> 2 --> 3 --> 4 --> 5
            i
                           j                        

```
j (fast) is k steps ahead of i (slow)
while fast pointer (j) still inside bound(j not null), move i, j forward at same speed
return the node that i points to


## recursion
bottom-up recursion

+ ask for next recursion level result          --
+ do something on current level of recursion     |--- 1, 3 should have same meaning
+ return result                                --


## problems

- [ ] 237. 
- [ ] 141
- [ ] 92
- [ ] 25


# Stack

Last in First Out (LIFO)

for problems that needs to record the previous states, and fetch the top element or come back to previous state

+ define the stack
+ define the operations on each element



- [ ] 739
- [ ] 735
- [ ] 20
- [ ] 496
- [ ] 503
- [ ] 394
- [ ] 636
- [ ] 84


# Heap

a complete binary tree implemented by array

root = max or min value

Common APIs:

peek(): check the element at heap top O(1)

poll(): get the element at the heap top (and reheap) O(logN)

insert(): add element to heap O(logN)


## online and offline algorithm
+ online: using heap. for streaming data, no fixed length, can be scaled on demand
+ offline: using sort. for fixed length data, need to be recalculated each time after scaling

## practice

many problems related to TopK


- [ ] 215
- [ ] 23
- [ ] 253
- [ ] 347
- [ ] 295
- [ ] 767
- [ ] 703



# hashmap

- [ ] 1
- [ ] 3
- [ ] 560
- [ ] 49
- [ ] 138
- [ ] 340
- [ ] 554
- [ ] 535



# BFS
search by layer
queue

## general steps
+ initialize queue with all entry points
+ while queue not empty
 + for each node in the queue (current)
 + poll out element (add to result)
 + expand the element, add children to queue in ordr
 + go to next level


each node enter/exit queue once O(n)


- [ ] 101
- [ ] 103
- [ ] 104
- [ ] 111
- [ ] 199
- [ ] 515
- [ ] 429




# DFS











