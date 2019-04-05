# CSE316 Assignment
This is the solution sumbission for the Academic Task: Simulation Based Assignment of Operating System CSE316 for the Academic Year 2019.

## Personal Info

Name : Mohammad Ashar Khan

Section : K17SM

Roll Number : 47

Group : 2

## Problem Statements

### Problem 11

Reena’s operating system uses an algorithm for deadlock avoidance to manage the allocation of resources say three namely A, B, and C to three processes P0, P1, and P2. Consider the following scenario as reference .user must enter the current state of system as given in this example :

Suppose P0 has 0,0,1 instances , P1 is having 3,2,0 instances and P2 occupies 2,1,1 instances of A,B,C resource respectively.

Also the maximum number of instances required for P0 is 8,4,3 and for p1 is 6,2,0 and finally for P2 there are 3,3,3 instances of resources A,B,C respectively. There are 3 instances of resource A, 2 instances of resource B and 2 instances of resource C available. Write a program to check whether Reena’s operating system is in a safe state or not in the following independent requests for additional resources in the
current state:

- Request 1: P0 requests 0 instances of A and 0 instances of B and 2 instances of C
- Request 2: P1 requests for 2 instances of A, 0 instances of B and 0 instances of C.

All the request must be given by user as input.

### Problem 22



Consider following and Generate a solution to find whether the system is in safe state or not?



![](https://i.imgur.com/reIWM1L.png)

---



## Solutions



### Problem 11

Running the program on the above input

```bash
./solution11.out < in11.txt
```

If you want to compile it yourself,

```bash
gcc solution11.c -o solution11.out
```

If you want to get a log of what program does and works, Compile with Verbose enabled as

```bash
gcc solution22.c -o solution22.out -DVERBOSE_ENABLED
```

![](https://i.imgur.com/kx3CjNk.png)

> Request to P0 Granted. It caused a DEADLOCK when the request was granted. 

> Request to P1 Granted. System was in Safe State even after request was granted.

All the logs are printed via `stderr` so, you can redirect it into a file by running :

```bash
./solution11.c 2> logfile.txt
```

It will write all the logs in the file named `logfile.txt` and output will be displayed on the console.



### Problem 22

Running the program on the above input

```bash
./solution22.out < in22.txt
```

If you want to compile it yourself, 

```bash
gcc solution22.c -o solution22.out
```

If you want to get a log of what program does and works, Compile with Verbose enbaled as 

```bash
gcc solution22.c -o solution22.out -DVERBOSE_ENABLED
```

![Imgur](https://i.imgur.com/sUyrEyW.png)


> No Dead Lock Found. System is in valid state if following order of process execution is followed : 
	P0->P2->P3->P4->P1

All the logs are printed via `stderr` so, you can redirect it into a file by running :

```bash
./solution22.c 2> logfile.txt
```

It will write all the logs in the file named `logfile.txt` and output will be displayed on the console.

