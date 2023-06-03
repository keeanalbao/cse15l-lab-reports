# Lab Report 5

## 1. Student EdStem Question

**What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?**

Visual Studio Code & JUnit

**Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”.**

I am trying to debug the ListExamples.java file, and there are failures in the testMerge1 and testMerge2 tests. Here is the symptom:

![1](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/b1b94785-e451-41ed-912e-e0f73adcf9c5)

![2](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/78a878e0-b013-46b8-9ccf-c26a230250da)

I expected to see the two lists merge in order, but I seem to be merging them in reverse order. 

**Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.**

![3](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/dacc85ab-ce48-4db2-8c65-5cd7beed56ca)

(I can also use `bash test.sh` to compile and run these tests, but I'm not using Linux right now).

## 2. Initial TA Response

May I see what your `merge` method looks like so I can get a better idea of where the bug might be?
Make sure you update the index variables correctly and within their respective list loops (e.g. index1 in list1 loop and index2 in list2 loop).

## 3. Additional Information From Student

Here is the merge method. The while loops and indexes seem to be correct.

![4](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/90300016-9308-4cf0-a481-6f401cfb13b2)


## 4. Final TA Response

*File & directory structure needed*


*Contents of each file before fixing the bug*


*Full command line(s) ran to trigger the bug*


*Description of what to edit to fix the bug*



## 5. Reflection
