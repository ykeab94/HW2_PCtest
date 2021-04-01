# HW2_PCtest

- To start this homework, I have create directory /OS/HW2 under /home/s21900335/
- First I made 2 C source codes files which are target and solution. A C source code file called "Target" receive inputs from user and prints out "Hello (user inputs)".
- For C source code "Solution" which is almost same with Target code but it tells users if he or she types number instead of charaters.
-  In the homework, pctest uses a compiler to build two executable files respectively but I do not know how so I have done it by manually.
-  <img width="342" alt="스크린샷 2021-04-01 오후 2 18 45" src="https://user-images.githubusercontent.com/63792404/113247067-2fb58480-92f5-11eb-8a1f-51b57de29278.png">
-  <img width="337" alt="스크린샷 2021-04-01 오후 2 17 44" src="https://user-images.githubusercontent.com/63792404/113246989-08f74e00-92f5-11eb-94b8-d8dfa9b29a16.png">
-  

- <img width="342" alt="스크린샷 2021-04-01 오후 2 21 20" src="https://user-images.githubusercontent.com/63792404/113247217-8a4ee080-92f5-11eb-9467-e9ab68c5b8a5.png">

-  and a set of program inputs _Tests_. 
- 학생 프로그램과 꺼와 선생꺼의 프로그램이 런이 되어야 함.
- 두 개의 프로그램 결과를 비교, 올바른 결과나 실패(오답을) 리턴하는지 결정짓기 위해.
- 다양한 용도 프로세스 컨트롤 용도의 알맞는 시스템 라이버리 함수들을 찾아야함. 그리고 pctest를 만들 때 적합하게 사용해야 함.
- 개인의 프로그램이 요구사항에 명시된데로 작동하는지를 보여주기 위해 비디오 영상도 제작해야 함.

- pctest receives as input (1) two source code files, target and solution. 
    - target은 c source code file
    - solution은 맞는 c 코드.
        - 포크를 만들어서 다른
- (2) a set of program inputs Tests.
- Tests consists of one to ten text files each of which is an input of target and solution.
- a target (or solution) program is programmed to receive inputs only via the standard input and produce output only to the standard output.

- after receiving source code files, pctest uses a compiler to build two executable files respectively, then runs these two executables with each of the test input file in Tests.
- ***pctest determines whether the execution result of target for an input is correct or not by checking if the program terminated successfully and the texts produced to the standard output is identical to one that produced by solution. 
- ***pctest displays the summary of the test results (see Section 2.3) via the standard output. The summary must include (1) whether the compilation was succeeded or not,(배열, 0,1) (2) the number of the correct test executions and the number of failed test executions, (3) the maximum and the minimum time of a single test execution, and the sum of all test execution time of target. Meanwhile, what target and solution print to the standard output must not be shown in the display. 
- pctest launches target and solution with each input file in Tests one by one. for each test input, pctest must create one process for target and the other for solution and run them concurrently.
- pctest must kill a process running target if its execution exceeds a predefined time limit, because it may run indefinitely. (Such a test execution should be recognized as a failed one.)
- In addition, when running target on a new process, pctest must disallow the process to open a new file to limit the danger of executing untrusted student’s code on the instructor’s computer.
- pctest determines that target fails for a given test input if the corresponding test execution falls into one of the following cases: 
    - a crash (runtime/fatal error) occurs, or 
    - the program returns an error code at termination, or 
    - the program does not terminate within a certain amount of execution time (i.e., time over), or 
    - the text printed to the standard output is not identical to that of solution
    - pctest also measures the test execution time to maintain the following three values: 
        - the maximum execution time of a single test run in milliseconds, and 
        - the minimum execution time of a single test run in milliseconds, and 
        - the sum of the execution time of all test runs in milliseconds.
