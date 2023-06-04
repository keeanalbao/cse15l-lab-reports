# Lab Report 5

## 1. Student EdStem Question

**What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?**

Visual Studio Code & JUnit

**Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”.**

I am trying to debug the ListExamples.java file, and there are failures in the testMerge1 and testMerge2 tests. Here is the symptom:

![](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/b1b94785-e451-41ed-912e-e0f73adcf9c5)

![](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/78a878e0-b013-46b8-9ccf-c26a230250da)

I expected to see the two lists merge in order, but I seem to be merging them in reverse order. 

**Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.**

![](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/dacc85ab-ce48-4db2-8c65-5cd7beed56ca)

I can also use `bash test.sh` to compile and run these tests, but I'm not using Linux right now.

## 2. Initial TA Response

May I see what your `merge` method looks like so I can get a better idea of where the bug might be?
Make sure you update the index variables correctly and within their respective list loops (e.g. index1 in list1 loop and index2 in list2 loop).

## 3. Additional Information From Student

Here is the merge method. The while loops and index variables seem to be correct.

![](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/90300016-9308-4cf0-a481-6f401cfb13b2)


## 4. Final TA Response

*File & directory structure needed*

![1](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/42ed9ed8-703a-4ecd-b7ec-dacfd27223cd)

*Contents of each file before fixing the bug*

![](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/13ec4b41-a202-460a-a43b-985b5f162a6d)

![](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/75bf4f6f-262b-454e-9f9e-7a74dc1e44b9)

![](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/076276bb-bd58-432b-a489-edd5a1c20073)


*Full command line(s) ran to trigger the bug*

![](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/3fc6abde-2a5b-48c0-b3b4-0975316281b1)


*Description of what to edit to fix the bug*

To fix this bug, you need to change the line containing the first if statement: `if(list1.get(index1).compareTo(list2.get(index2)) > 0)` to `if(list1.get(index1).compareTo(list2.get(index2)) < 0)` (the greater than operator is now a less than operator). This line compares the element at index1 in list1 to the element at index2 in list2. The bug made it so that if the first element was greater than the second element, then add the second element to the `result` list first, which made the list in descending order. By switching the sign, it will now merge in ascending order.

![](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/d2681656-af26-4632-9802-013a688ac3b6)

![](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/023f81fe-df4c-4e77-8b31-2ffd38c6e55e)


## 5. Reflection

Something new that I learned in the second half of this quarter was Vim. I have never used Vim before much less even heard of it. It is a very unique programming language and text editor, and I wouldn't say I loved it, but I did find it very interesting and useful for the last few labs. I'm not sure how often I will use Vim in the future, but I'm glad I got to learn the basics of it in case I do use it.
