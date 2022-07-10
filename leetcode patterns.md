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
- [ ] 11. container with most water
- [ ] 42. trapping rain water
- [ ] 283.moving zeros
- [ ] 80. remove duplicate II
- [ ] 1047. remove all adjacent duplicates in string




