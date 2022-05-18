# Week 8 Lab Report

**A link to your markdown-parse repository and a link to the one you reviewed in week 7:**

* [My repository](https://github.com/calistajlee/lab6-markdown-parser)
* [The repository I reviewed](https://github.com/calistajlee/markdown-parse-peer-review)
---

**For each test above:**

* **Decide on what it should produce (i.e., expected output) by using either VScode preview or the CommonMark demo site**
**Showing the code in MarkdownParseTest.java for how you turned it into a test**

These pictures show the expected output in VS Code.
Snippet 1:
![snippet1](snippet1.png)

Snippet 2:
![snippet2](snippet2.png)

Snippet 3:
![snippet3](snippet3.png)

This is my code in MarkdownParseTest.java and it shows how I turned it into JUnit tests.
![junit_tests](junit_tests.png)

* **For your implementation, the corresponding output when running the tests; if it passed, say so. If it didn’t pass, show the specific part of the JUnit output that shows the test failure.**
**For the implementation you reviewed in Week 7, the corresponding output when running the tests; if it passed, say so. If it didn’t pass, show the specific part of the JUnit output that shows the test failure.**

For my implementation, this is the corresponding output when running the tests. It failed all three tests.
![my implementation tests](test_my_repo.png)

For the implementation in Week 7, this is the corresponding output when running the tests. It failed all three tests.
![week 7 implementation tests](test_wee7_repo.png)


---

**Answer the following questions with 2-3 sentences each:**

* **Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases that use inline code with backticks? If yes, describe the code change. If not, describe why it would be a more involved change.**

There is a small (<10 lines) code change that will make the program work for snippet 1 and all related cases that use inline code with backticks. We can use an if statement that says if the character at the current index is ever a backtick, we can set the current index to the closing parenthesis and continue over that link. This is something similar to what we did to skip over images when there was an exclamation mark in front of the opening bracket.


* **Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets? If yes, describe the code change. If not, describe why it would be a more involved change.**

This is a small (<10) code change that will make the program work for snsnippet 2 and all related cases that nest parentheses, brackets, and escaped brackets. We can write an if statement saying checking for additional `[`,`]`, `(`,`)` beyond the expected opening and closing brackets and parentheses. If there are any, we can check to see if there is a backslash right before the index where the additional brackets and parenthesis occurs. If there are backslashes, we can continue normally. If there are no backslashes, we can move the current index to skip over this link.


* **Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related cases that have newlines in brackets and parentheses? If yes, describe the code change. If not, describe why it would be a more involved change.**

There would be a more involved code change that will make the program work for snippet 3 and all related cases that have newlines in brackets and parentheses because there are more cases to account for. For example, we have to account for the case of the parentheses being read when there are new lines between them. We also have to account for when there is never a closing parenthesis and everything is written as text instead of a link. There is also another case where we have to account for the link being on it's own line and the parentheses and brackets showing up in the preview on VS Code. There are many nuances with the new lines separating the links, parentheses, and closing brackets that make this more difficult to change in less than 10 lines.