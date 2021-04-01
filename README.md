# HW2_PCtest

- To start this homework, I have create directory /OS/HW2 under /home/s21900335/
- First I made 2 C source codes files which are target and solution. A C source code file called "Target" receive inputs from user and prints out "Hello (user inputs)".
- For C source code "Solution" which is almost same with Target code but it tells users if he or she types number instead of charaters.
-  In the homework, pctest uses a compiler to build two executable files respectively but I do not know how so I have done it by manually.
-  <img width="342" alt="스크린샷 2021-04-01 오후 2 18 45" src="https://user-images.githubusercontent.com/63792404/113247067-2fb58480-92f5-11eb-8a1f-51b57de29278.png">
-  <img width="337" alt="스크린샷 2021-04-01 오후 2 17 44" src="https://user-images.githubusercontent.com/63792404/113246989-08f74e00-92f5-11eb-94b8-d8dfa9b29a16.png">
  
- To find out whether both target and solution file works, I have created input
<img width="366" alt="스크린샷 2021-04-01 오후 2 36 38" src="https://user-images.githubusercontent.com/63792404/113248326-aeabbc80-92f7-11eb-9108-f8566832f0b8.png">
- <img width="366" alt="스크린샷 2021-04-01 오후 2 33 18" src="https://user-images.githubusercontent.com/63792404/113248073-3513ce80-92f7-11eb-8ac7-6e1f16854211.png">
- and using this input I got results that I wanted from running target and solution file.
- <img width="366" alt="스크린샷 2021-04-01 오후 2 35 24" src="https://user-images.githubusercontent.com/63792404/113248246-802de180-92f7-11eb-8bcb-01197033e6ce.png">

- Moreover, because of my ignorance, I have compared the results of target and solution file manually to get the result I wanted.
- <img width="342" alt="스크린샷 2021-04-01 오후 2 21 20" src="https://user-images.githubusercontent.com/63792404/113247217-8a4ee080-92f5-11eb-9467-e9ab68c5b8a5.png">
- <img width="366" alt="스크린샷 2021-04-01 오후 2 26 48" src="https://user-images.githubusercontent.com/63792404/113247585-4c9e8780-92f6-11eb-8773-bfc96ed06419.png">
by using linux standard output I could get the expected result right. 

- A student may submit a C source code with an error such as shown below picture.
- <img width="413" alt="스크린샷 2021-04-01 오후 6 02 06" src="https://user-images.githubusercontent.com/63792404/113270563-926a4880-9314-11eb-8cf0-a04f476fe131.png">
- In order to capture this error I have used "gcc -o target target.c 2> log" and able to capture the error.
- <img width="564" alt="스크린샷 2021-04-01 오후 6 05 53" src="https://user-images.githubusercontent.com/63792404/113270885-e7a65a00-9314-11eb-8d60-52e596456b3c.png">
- In order to close the file that runs forever, one way is using setitimer

-To run target and answer file, first I made a parent and child process by using fork() and able to run target program on child process and run answer program on parent process.
<img width="561" alt="스크린샷 2021-04-01 오후 9 17 30" src="https://user-images.githubusercontent.com/63792404/113292581-ac655480-932f-11eb-99e1-2da17c2c1a04.png">
<img width="561" alt="스크린샷 2021-04-01 오후 9 17 06" src="https://user-images.githubusercontent.com/63792404/113292540-9d7ea200-932f-11eb-85b5-eab0dcf5d715.png">

-Because of my ignorance, I have used time to check how much time it took for a program to complete.
<img width="359" alt="스크린샷 2021-04-01 오후 9 29 55" src="https://user-images.githubusercontent.com/63792404/113293982-68734f00-9331-11eb-890b-028657522ea9.png">

-If target code does not run properly, a user can kill the process using "kill -9 (PID)"
<img width="1282" alt="스크린샷 2021-04-01 오후 9 26 11" src="https://user-images.githubusercontent.com/63792404/113293711-15010100-9331-11eb-8a73-7049a879acd0.png">
