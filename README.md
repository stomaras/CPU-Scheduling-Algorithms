# Operating Systems

# Important Notes 

1) Any I/O Device will have a buffer(memory or register) associated with it 

2)CPU = Central Process Unit 

3)Memory->1)RAM
          2)Hard Disk 
          3)Cache
          4)Registers
          
4) RAM                              HARD DISK
   -Not permanent                   -Permanent
   -Fast                            -Slow
   -Costly                          -Cheaper
   
5) Size RAM < Size HARD DISK 

6)CPU understand 0's and 1's

7)Hello.c -> Compiler -> Machine Code (executable code or low level program) present in Hard Disk 

8)CPU cannot access hard disk directly 

9)Short-term-scheduler = Decides which process will access the CPU first from RAM ( RAM -> CPU)

10)Long-term-scheduler = Decides which from programs will move to RAM from HARD DISK (hARD DISK -> RAM)

11)Steps 9 and 10 is Resource Allocation 

12)Operating System = Resource Manager

13)Operating System Functionality -> 1) Resource Allocation 
                                     2)Resource Management
                                     
14)Operating System is a core which have a lots of functions 

15)Operating System takes a set of addresses this called OS code 

16)RAM space  = 1)OS space
                2)User space
                
17)When execution of a program is done then removed from the RAM 

Example of Calculator 

Step 1 )If i write 2 then 010 move from keyboard buffer to RAM then if i write 3 the 011 overwrite 010 and move from keyboard buffer to RAM

Step 2)CPU have registers ...then Operations done by CPU ->Result overwritten in any Register depends on implementation  

Step 3) CPU have 2 parts ->1)Control Unit (CU)
                           2)Arithmetic Logical Unit (ALU)

Step 4)Arithmetic and Logic Unit -> Operations ->1)Addition 
                                                 2)Division e.t.c
                                                 
Step 5)From register of CPU ,placed inside the RAM 

Step 6) Result placed into Monitors Buffer 

18)Hard Disk act as ->Input Device
                    ->Output Device 
                    
19)Turn-Around-Time = Waiting time + Burst time + I/O time

20)States of a process
                              1)New Sate 
                              2)Ready State
                              3)Running Sate 
                              4)Waiting State
                              5)Terminated State
                              6)Suspend State Ready 
                              7)Suspend Wait State

            
21)Degree of Multiprogramming  = size of RAM / size of single Process(Assumption ...size of all processes are the same )

22)Types od Operating Systems : 1) Batch os -> 1 CPU
                                2) Multiprogramming os -> 1 CPU
                                3) Multiprocessing os -> More than 1 CPU 
                                
 23)This Program for which the process is created is also called as "Passive Entity"
 
 24)The process which is actually created for the program is also called as "Active Entity"
 
 25)Dynamically Allocating Memory : Allocating Memory at the Runtime with malloc function
 
 26)Stack Space and Heap Space depends on the program
 
 27)For every process we have a process control block PCB(stack,heap,static/globalvariables,prgram)
 
 28)local variables allocated in the stack 
 
 29)Scheduling Algorithms ->1)FCFS
                            2)SJF
                            
                            
 30)Process Attributes: 1)Process id 
                        2)Program Counter
                        3)Process State
                        4)General Purpose Registers
                        5)Priority
                        6)List of open files
                        7)List of open devices
                        8)Protection 
                        
31)Program Counter : A register which will be maintained closer to the CPU 

32)General Purpose Registers : Set of registers values of the program 

33)Protection : For every process our os code needs to make sure that a process is not using the space of another process...ok?

34)Context of the process P1 ->1)process id
                               2)program counter
                               3)process state
                               4)General Purpose Registers
                               5)Priority
                               6)List of open files 
                               7)List of open devices 
                               8)Protection 
                               
35) Parts of OS code -> 1)Long-Term-Scheduler
                     -> 2)Short-Term-Scheduler
                     -> 3)Medium-Term-Scheduler
                     
36)From Hard Disk which processes will be moved into the RAM is deciding by something called as Long-Term-Scheduler

37)Every process has a priority number

38)Medium-Term-Scheduler -> A function of OS which decide which process should swap-out of RAM so the higher priority process swap-into the RAM 

39)swap-in -> from HARD DISK to RAM 
   swap-out -> from RAM to HARD DISK
40)Context - Switching : Let's assume CPU execute p1 and whenever p4 comes into RAM who's priority higher than p1,p1 has to be preemtive and context of p1 saved and p4 has to be scheduled by CPU this call as context-switching 

41)Various times related to a process 
                                        1)Arrival Time 
                                        2)Burst Time(also calleds as Execution time)
                                        3)Completion time
                                        4)Turn-Around-Time
                                        5)Waiting-Time
                                        6)Response Time
                                        7)I/O time
                                        
 42) Arrival Time = point-in-time which process is moved from Hard Disk to RAM 
 
 43)Turn-Around-Time = The total time which the process is inside the RAM 
    Turn-Around-Time = Completion Time - Arrival Time
    Turn-Around-Time = Burst Time + I/O Time + Waiting Time 
    
 44)Waiting Time =  time that a process spend inside the RAM without doing anything 
 
 45) Point-In-Time               Duration-in-time
                                        
          1) Arrival Time               1)Burst Time
                                        
          2) Execution Time             2)Turn Around Time 
                    
                                        3)Waiting Time
                                        
                                        4)Response Time 
 46) Schedule Length = Completion Time of last process - Arrival Time of 1st Process
 
 47) Throughput = Num Of Processes / Schedule Length
 
 48) Response Time = Waiting time of that process until it gets the CPU for the first time 
 
 49) In any Non-Preemtive Scheduling Algorithm(e.g FCFS,SJF) , Response Time = Waiting Time 
 
 50) Context Switching Overhead = 0 time unit ... then Useful Time Of CPU = 100%
 
 51) While ( Context Switching Overhead . Increase) then (CPU Efficiency and Computer Speed Decrease)  
 
 52) Starvation Problem : An Algorithm suffers from starvation problem if there is a chance for a process in the 
                          the ready state to wait indefinitely to get the CPU 
                          
 53) Any kind of Algorithm which follow the concept of FIFO does not suffer from Starvation Problem 
 
 
 
 
     Algorithms                                    Problem of Starvation 
     
     
 54) Shortest-Job-First                            YES Disadvantage
      
     Shortest Remaining Time First                 YES Disadvantage 
 
     First Come First Served                       No Advantage 
     
 55) Convoy Effect : A smaller process(process with very small execution time) or process with very small burst time 
                     waiting for one big process to get off(release) the CPU. An Algorithm with convoy effect problem 
                     may lead to higher waiting time and higher Turn-Around-time in comparison to an algorithm without 
                     convoy effect problem FCFS, SJF suffers from convoy effect problem .On the other hand SRTF does not 
                     suffer from convoy effect problem.
                     
 56) SJF, SRTF difficult to implement because depends on burst time and burst time depends on a lot of factors which means power system 
               system capacity and all this.
      FCFS     easy to implement , we can simply place a clock inside in our computer
      
 57) LJF Scheduling Algorithm : : - Priority based scheduling algorithm 
                                  - Starvation problem exists ( Maybe process wait indefinitely )
                                  - Convoy effect problem exists ( Small process waiting for larger process)
                                  - Throughput is very less 
                                  - Practically us very difficult to implement ( we don't know burst time)
                                  
58) Time Quantum : Maximum Allowable time a process can run without getting preemted

59) Round Robin Scheduling Algorithm (Time Quantum + First Come First Served): 1) it works on the basis of a particular time quantum
                                                                               2) Uses Queue Data Structure
                                                                               3) Very Popular used in most of the OS Today
                                                                               4) No starvation Problem 
                                                                               5) No convoy effect problem
                                                                               6) Practically Implementable not based on Burst Time
                                                                               7) Response Time is good 
                                                                               8) Throughput is good but not as good as SJF, SRTF
                                                                               
                                                                              
 60) Priority based Scheduling Algorithm : There is no definitely rule that priority Number is higher you need to give the higher                                                  priority or if priority number is lesser you need to give the higher priority it really 
                                           depends on the problem itself.
                                           
 60) Versions of Priority based Scheduling Algorithm : 1) Preemtive 
                                                       2) Non - Preemtive
                                                       3) On preemtive priority based scheduling algorithm and non-preemtive scheduling
                                                          Algorithm priority based on priority number.
                                                          
 62) Processes which are in I/O state and processes which are in Ready State are in different queues in Ram
 
 63) Highest Response Ration Next Scheduling Algorithm (HRRN)
                                                            Mode: Non - Preemtive
                                                            Response ration = (w + b) / b
                                                            w = waiting time of a process 
                                                            b = burst time
                                                            Note: For every process we calculate Response Ratio 
                                                            Increase w <=> Increase RR
                                                            As burst time increase <=> value of response ratio decrease
                                                            As burst time decrease <=> value of response ratio increase
                                                            Note : Among all the processes that are in ready state the 
                                                                   (HRRN) Scheduling Algorithm will select the process 
                                                                   with bigger Response Ratio. So we are dealing with 
                                                                   the throughput as well as with decrease Starvation 
                                                                   Problem.
                                                                   
64) Every Program from New State goes to Ready State
    Note !!! CPU needs to understanding the program, only then can go undergo I/O State.
    Note !!! Also a program cannot go to Run State directly from Hard Disk to CPU.
    Note !!! Maybe a new process created inside the Hard Disk let's Assume RAM is completely full and there is no space 
             to place any process. A higher priority process is being created and needs to be executed by the CPU. In order to executed
             by the CPU this process has to be present inside the RAM. Problem is our RAM hasn't free space. So will move one process
             from RAM to HARD DISK.Let's assume the process which move from RAM to HARD DISK is in ready state so now goes to something
             called Suspend Ready State.if process was in I/O State then goest to something called Suspend I/O State.If complete I/O
             in HARD DISK then moved to Suspend Ready State because of lack of space
             
65) Scheduler is a part of a function which decides which process will be executed from the CPU next. Scheduler after decding which         process to execute next by the CPU, it will call Dispatcher Function.This function will load the contents of register to execute
    further.
66) Dispatcher is also a Program, is part of Operating Systems Code.

67) CPU registers -> faster memory in Our Computers

68) Entire memory consists of Verbs-> We can place an instruction or we can place data

69) Some computers use 2 words to present an instruction .It depends on implementation some pc use 1 word -> 4bytes , 1 word -> 8bytes

70) Every verb will hava an address

71) Addresses represent in Binary Format

72) CPU asks for a verb from the RAM , if CPU want verb in line 4, then will ask for the address in line 4 to the RAM.Now RAM what will     do?... will get the copy of this DATA and give to the registers .Now CPU gets this DATA and process it.

73) Now how the CPU requests the verb as well as how this data is move into register?
    for this use something called bus
    bus: Collection of wires,which are used to connect all the devices of your computer
    CPU requests the verbs -> sends the Address through something called the Address bus
    Data bus -> Collection of wires which are actually used to send the Data from RAM to CPU Registers
    
74) Memory Size => Depends on num of words => 2^M words => M bits

75) Physical Address spaces => All addresses of RAM 
    So inside the RAM replace processes: A process will have a collection of Addresses
    Collection of addresses of a process is also called => Logical Address Space
    
76) What is meant by Memory Allocation?
          We are trying to place our Proceses inside the RAM that is what we mean by Allocation
77) Various methods used to load the processes to Main Memory
          1) Contigious Allocation:
                    -> Fixed Partitioning(Also called as static partitioning)
                    -> Variable Partitioning(Also calleds as Dynamic partitioning)
          2) Non-Contigious-Allocation
78) In case of Fixed Partitioning let's assume divide RAM into 4 partitions ( fixed partition) will never change

79) There is no External Fragmentation problem in Fixed Partitioning

80) Fixed Partitioning - Disadvantages :
          1) Internal Fragmentation problem exists
          2) Process Size is limited by the size of the largest partition
          3) Degree of Multiprogramming is limited by the number of partitions
          
81) 2 Important rules of Fixed Partitioning:
          1) A partition can hold only one process data
          2) A process can be placed in only one partition
             and it cannot span across 2 or more partitions
          
82) Internal Fragmentation Problem : is nothing but in Fixed Partitioning size of process maybe less than size of partition 
                                     and so, some space within the partition has to be wasted without being utilized.
                                    
83) In Fixed Partitioning use partitions will always remain fixed and it will never change

84) In Variable Partitioning we don't actually do any part before placing any process

85) Variable Partitioning: 
                              1) No internal fragmentation problem
                              2) Degree of Multiprogramming is not limited by Partitions
                              3) Size of a process is not limited by size of largest Partition rather 
                                 it is limited by the Size of RAM.
                                 
86) Variable Partitioning suffers from problem of External Fragmentation

87) External Fragmentation Problem exists when there is enough space from the process in the 
    RAM, but still we are not able to do because we want to achieve the property of 
    Contigious Allocation
    
88) Memory Allocation Algorithms : 1) First Fit
                                   2) Next Fit
                                   3) Best Fit
                                   4) Worst Fit
 
 89) First Fit : A new process come into RAM from HARD DISK and whenever i found a hole, which is big enough to hold the process
                 again i will accomodate that process
                 
 90) Next Fit: is almost same with the first fit algorithm which means we start traversing the Address space and once you find out 
               the hole which is big enough to hold the process we will accomodate a process exactly like first fit
               .Next fit does not scan the whole list, it starts scanning the list from the next Node.
               
 91) Best Fit: The Best Fit Algorithm tries to find out the smallest hole is possible in the list that can accomodate the size                          requirement of the process.
 
               Using the Best Fit has some disadvantages:
               a) It is slower because it scans the entire list every time and tries to find out the smallest hole which can satisfy
                  the requirement of the process
               b) Due to the fact that the difference between the whole size and the process size is very small, the holes produced 
                  will be as small as it can not be used to load any process and therefore it remains useless.
                  
 92) Worst Fit Algorithm: The worst fit algorithm scans the entire list every time and tries to find out the biggest hole in the list 
                          which can fulfill the requirement of the process.
                          Despite the fact that this algorithm produces the larger hole to load the other processes,this is not better
                          approach due to the fact that it is slower because it searches the entire list every time angain and again
                          
 # Binary addressing revisited
 
 so -> Ho -> Fo
          -> F1
 so->  H1 -> F2
          -> F3
 s1 -> H2 -> F4
          -> F5
 s1->  H3 -> F6
          -> F7
 s2 -> H4 -> F8
          -> F9
 s2->  H5 -> F10
          -> F11
 s3 -> H6 -> F12
          -> F13
 s3->  H7 -> F14
          -> F15
 
 Let us assume we have four streets againsts creates a city has four streets i'am naming the streets->So
                                                                                                    ->S1                          
                                                                                                    ->S2
                                                                                                    ->S3
  Every Street has 2 houses (00)so -> H0
                                   -> H1
                               
                            (01)s1 -> H2
                                   -> H3
                               
                            (10)s2 -> H4
                                   -> H5
                               
                            (11)s3 -> H6
                                   -> H7
                               
  Every house has 2 floors and maintaining the floors...
  
  H0 -> F0 (0000)
     -> F1 (0001)
     
  H1 -> F2 (0010)
     -> F3 (0011)
     
  H2 -> F4 (0100)
     -> F5 (0101)
     
  H3 -> F6 (0110)
     -> F7 (0111)
     
  H4 -> F8 (1000)
     -> F9 (1001)
     
  H5 -> F10 (1010)
     -> F11 (1011)
     
  H6 -> F12 (1100)
     -> F13 (1101)
     
  H7 -> F14 (1110)
     -> F15 (1111)
     
     
I can split this address 1001 in 2 parts 

For Example here there are 4 streets 

1001 - > 10 indicate street number 
     ->  0 indicate house number 
     ->  1 indicate floor number
     
In order to number 2 houses we need exactly 1 bit

Byte Addressable System : means every byte which is present in our RAM will be given an address

Assume we have 4 partitions ... Now in order to indicate 4 partitions 2^2 partitions -> we need exactly 2 bits

for each byte we need 4 bits, there are 4 partitions we need exactly 2 bits to address a partition , taken first 2 bits 
,we taken the partition number .Every partition has exactly 4 bytes and in order to address 4 bytes you need 2 bits

(_0_ _0_)( _1_ _1_)
   |        |
Partition Bytes
Number    Number
   |        |
   0        3
   
   This is the basic idea of paging 

          


                                                            
                                                            
                                                                               
