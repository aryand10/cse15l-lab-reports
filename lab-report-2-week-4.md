# Lab Report 1 (Week 2)

Hello! This page covers some of the errors and their respective solutions for a program called `MarkdownParse`, which has the goal of getting all web links from a `.md` file!

## Error 1: "Not A Link"
___

The file that induced this specific error was:
[`break-test.md`](https://github.com/aryand10/markdown-parse/blob/main/break-test.md)

The following image shows what happened initially when `MarkdownParse` was run with `break-test.md`.

___

![Image](Break-TestResult.jpg)
The above image shows what happened initially when `MarkdownParse` was run with `break-test.md`.

___

![Image](Break-TestFixPicture.png)

To fix the bug that caused the error, the above changes were made to the code.
___

**Relationship Between Bug, Symptom, and Error**

This bug was induced by the `break-test.md` file, which when ran through `MarkdownParse.java`, resulted in the word `something` being placed in the links array and printed, even though `something` was not a link. The word `something` was placed in parentheses with brackets preceding it but was not a link. This was caused by the program simply look for any text in parenthesis with brackets beforehand. This was corrected by adding an if statement to the code that only added text to the links array if it did not have any spaces and featured a "`.`" in the text to ensure it was a link. Thus, when `break-test.md` was tested again, the additional `something` text was not printed.





