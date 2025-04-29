# operating-system-homework-3-solved
**TO GET THIS SOLUTION VISIT:** [Operating System Homework 3 Solved](https://www.ankitcodinghub.com/product/operating-system-hw3-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;110243&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;Operating System Homework 3 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
Scheduler Simulator

Objective

● Understand how to implement user-level thread scheduling

● Understand how signal works in Linux

● Understand how scheduling algorithms affect results

Architecture

Requirement (1/5)

1. Tasks &amp; task manager

○ Use ucontext and the related APIs to create tasks

○ Implement a task manager to manage tasks, including their state, data structures and so on

○ Implement task state-related APIs that can be used by the tasks (described in slide 10-11)

i. void task_sleep(int msec_10); ii. void task_exit();

Requirement (2/5)

2. Task scheduler

○ Use ucontext and the related APIs to do context switch ○ Implement three scheduling algorithms

■ FCFS

■ RR with time quantum = 30 (ms)

■ priority-based preemptive scheduling, smallest integer → highest priority ○ The algorithm is determined at execution: ./scheduler_simulator {algorithm} ■ algorithm = FCFS / RR / PP

○ Once the scheduler dispatches CPU to a task, print a message in the format:

Task {task_name} is running.

○ If there are no tasks to be scheduled, but there are still tasks waiting, print a message in the format:

CPU idle.

Requirement (2/5)

function.h function.c

Requirement (3/5)

3. Resource handler

○ Implement resource-related APIs that can be used by the task (described in slide 12-13)

i. void get_resource(int count, int *resource_list);

ii. void release_resource(int count, int *resource_list);

○ There should be 8 resources with id 0-7 in the simulation.

○ How to simulate resources is up to your design. For example, you can use a boolean array, resource_available = { true, false, true, …. }

Requirement (4/5)

4. Timer &amp; signal handler

○ Use related system calls to set a timer that should send a signal (SIGVTALRM) every 10 ms ○ The signal handler should do the followings:

i. Calculate all task-related time (granularity: 10ms)

ii. Check if any tasks’ state needs to be switched iii. Decide whether re-scheduling is needed

Requirement (5/5)

5. Command line interface

start

shell mode simulation mode

Ctrl + z or simulation over

○ Should support four more commands (details are described in slide 14-17)

i. add: Add a new task

ii. del: Delete a existing task

iii. ps: Show the information of all tasks, including TID, task name, task state, running time, waiting time, turnaround time, resources occupied and priority (if any)

iv. start: Start or resume simulation

○ Ctrl + z should pause the simulation and switch to shell mode

○ Timer should stop in the shell mode and resume when the simulation resumes

○ When the simulation is over, switch back to shell mode after printing a message in the format: Simulation over.

API Description (1/4)

● void task_sleep(int msec_10);

○ Print a message in the format: Task {task_name} goes to sleep.

○ This task will be switched to WAITING state

○ After 10 * msec_10 ms, this task will be switched to READY state

API Description (2/4)

● void task_exit();

○ Print a message in the format: Task {task_name} has terminated.

○ This task will be switched to TERMINATED state

API Description (3/4)

● void get_resource(int count, int *resource_list);

○ Check if all resources in the list are available

➢ If yes

■ Get the resource(s)

■ Print a message for each resource in the list in the format:

Task {task_name} gets resource {resource_id}.

➢ If no

■ This task will be switched to WAITING state

■ Print a message in the format: Task {task_name} is waiting resource.

■ When all resources in the list are available, this task will be switched to READY state

■ Check again when CPU is dispatched to this task

API Description (4/4)

● void release_resource(int count, int *resource_list);

○ Release the resource(s)

○ Print a message for each resource in the list in the format:

Task {task_name} releases resource {resource_id}.

Shell Command (1/4)

● add

○ Command format: add {task_name} {function_name} {priority}

○ Create a task named task_name that runs a function named function_name

○ priority is ignored if the scheduling algorithm is not priority-based preemptive scheduling

○ This task should be set as READY state

○ Print a message in the format: Task {task_name} is ready.

Shell Command (2/4)

● del

○ Command format: del {task_name}

○ The task named task_name should be switched to TERMINATED state ○ Print a message in the format: Task {task_name} is killed.

Shell Command (3/4)

● ps

○ Command format: ps

○ Show the information of all tasks, including TID, task name, task state, running time, waiting time, turnaround time, resources occupied and priority (if any)

○ Example

1) The TID of each task is unique, and TID starts from 1.

2) There is no turnaround time for unterminated tasks.

3) Time unit: 10ms

Shell Command (4/4)

● start

○ Command format: start

○ Start or resume the simulation

○ Print a message in the format: Start simulation.

Grading

● If you cannot explain smoothly, you won’t get points.

Precautions

● All purple texts are prescribed formats and must be followed.

● You should implement hw3 with C language.

● You will get a template from hw3 github classroom (see Appendix for details).

● You can modify makefile as you want, but make sure your makefile can compile your codes and generate the executable file correctly.

● The executable file should be named scheduler_simulator.

● Make sure your codes can be compiled and run in the DEMO environment introduced in the hw0 slide.

GitHub Classroom

● GitHub classroom

Click Here to start your assignment.

Reference

● ucontext

○ The Open Group Library

○ Linux manual page

■ getcontext()

■ setcontext()

■ makecontext()

■ swapcontext()

● signal

○ Gitbook

○ Linux manual page

● timer

○ Linux manual page

○ IBM® IBM Knowledge Center

Appendix – file structure of the template

● shell.h/.c, command.h/.c, builtin.h/.c are shell-related files, and builtin.c contains the four commands need to be implemented in this assignment

● resource.h/.c contains resource-related APIs that need to be implemented

● task.h/.c contains task state-related APIs that need to be implemented

● function.h/.c contains functions run by tasks. These 2 files cannot be modified

● test folder contains all test cases, an auto-judge script for the shell and an auto-run script for the simulation

Appendix – how to use auto-judge and auto-run

● Auto-run the scheduler simulator

➢ python3 test/auto_run.py {algorithm} {test_case}

➢ algorithm can be FCFS, RR, PP or all, where all will perform three rounds of simulation for all scheduling algorithms

➢ test_case can be test/general.txt, test/test_case1.txt or test/test_case2.txt

■ Test case files contain a list of commands seperated by newlines. You can also write your own test cases, just follow the format

■ test/general.txt tests all requirements except pausing

■ test/test_case1.txt and test/test_case2.txt are test cases that need to observe the results

➢ The auto-run script will generate a file to store the simulation result, and the file name is {test_case’s file name}_{algorithm}.txt, for example, general_FCFS.txt

➢ Auto-run script does not support pausing with Ctrl + z
