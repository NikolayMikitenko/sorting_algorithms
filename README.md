# sorting_algorithms

## Goal
Implement BST (Balanced Binary Search Tree) and Counting Sort algorithm 
Generate 100 random datasets and measure complexity
Figure out when Counting Sort doesn’t  
Measure perfomance  

## Balanced Binary Search Tree
### Run
```
python bbst.py
```

### Result
```
   size, rows  duration, sec  duration per item, microsec
0         100            0.033840                   338.397026
0         100            0.025928                   259.284973
0         100            0.024014                   240.135193
0         100            0.023847                   238.471031
0         100            0.023393                   233.933926
0         100            0.023222                   232.222080
0         100            0.022490                   224.897861
0         100            0.021918                   219.182968
0        1000            0.037452                    37.452459
0        1000            0.034446                    34.445763
0        1000            0.032784                    32.784224
0       10000            0.323755                    32.375503
0        1000            0.032024                    32.023668
0        1000            0.032016                    32.016039
0      100000            2.828792                    28.287919
0       10000            0.266781                    26.678109
0        1000            0.024018                    24.018288
0      100000            2.238770                    22.387698
0      100000            2.204875                    22.048752
0      100000            2.196287                    21.962872
*******************************************************************
After Init: 
R----14
     L----7
     |    L----3
     |    |    L----1
     |    |    |    L----0
     |    |    |    R----2
     |    |    R----5
     |    |         L----4
     |    |         R----6
     |    R----11
     |         L----9
     |         |    L----8
     |         |    R----10
     |         R----12
     |              R----13
     R----23
          L----19
          |    L----17
          |    |    L----16
          |    |    |    L----15
          |    |    R----18
          |    R----21
          |         L----20
          |         R----22
          R----27
               L----25
               |    L----24
               |    R----26
               R----28
                    R----29
After Deletion: 
R----14
     L----7
     |    L----3
     |    |    L----1
     |    |    |    L----0
     |    |    |    R----2
     |    |    R----5
     |    |         L----4
     |    |         R----6
     |    R----11
     |         L----9
     |         |    L----8
     |         |    R----10
     |         R----12
     R----23
          L----19
          |    L----17
          |    |    L----16
          |    |    |    L----15
          |    |    R----18
          |    R----21
          |         L----20
          |         R----22
          R----27
               L----25
               |    L----24
               |    R----26
               R----28
                    R----29
Find Item Node: 
R----12
*******************************************************************
10000 size tree
Init duration: 0.14449095726013184
Deletion duration: 2.288818359375e-05
Find duration: 0.0007207393646240234
```


## Counting Sort algorithm
### Run
```
python cs.py
```

### Result
```
   size, rows  number range  duration, sec  duration per item, microsec
0         100      10000000            0.966499                  9664.986134
0         100      10000000            0.946239                  9462.387562
0        1000      10000000            1.196158                  1196.157932
0        1000      10000000            1.194175                  1194.175243
0         100       1000000            0.115039                  1150.388718
0         100       1000000            0.095877                   958.774090
0       10000      10000000            1.501334                   150.133395
0        1000       1000000            0.141884                   141.884089
0        1000       1000000            0.133468                   133.468390
0        1000       1000000            0.119334                   119.333982
0       10000      10000000            1.187401                   118.740058
0         100        100000            0.009766                    97.663403
0         100        100000            0.009533                    95.329285
0         100        100000            0.009372                    93.717575
0        1000        100000            0.014954                    14.953613
0      100000      10000000            1.431251                    14.312508
0       10000       1000000            0.136982                    13.698173
0      100000      10000000            1.354976                    13.549759
0       10000       1000000            0.132235                    13.223505
0       10000       1000000            0.131449                    13.144851
...
0     1000000       1000000            0.645247                     0.645247
...
0     1000000           100            0.189286                     0.189286
0      100000           100            0.018663                     0.186632
```

### Conclusion: Counting Sort algorithm do not perform on highly ditributed data (high distance between nearest numbers, expensive count array tasks)

## Profiling
```
python bbst_perfomance.py > log.csv
```

Result: 
`log.csv`

Analyze:
`Profiling.xlsx`

### Search, insert and delete `O(log n)` 
![image](https://user-images.githubusercontent.com/52753625/203656113-e47eac4e-c45c-426a-aa81-adfdd1f58079.png)


### Memory size `O(n)` 
![image](https://user-images.githubusercontent.com/52753625/203656159-e6d56dbf-b5d4-4a8c-a05d-4710ee059baf.png)


