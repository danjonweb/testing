Purpose
===
The purpose of this site is to enable (math) teachers easily generate different versions of a test. It was designed to work specifically with math tests and has support for ASCIIMathML. [Click here](http://www1.chapman.edu/~jipsen/mathml/asciimath.html) to view the document for the ASCIIMathML project, which enables you to type out math symbols in a human-readable format. However, it can work with any type of text.

How to use it
===
Create a folder structure that looks like this:
* index.html
* main.css
* Test 1/questions.txt
* Test 2/questions.txt

Open the index.html file and edit the `<title>` tag to specificy which test folder to use and which version of the test to generate. For example, if you set the title to "Test 1.1", it will use the Test 1 folder and generate version 1. If you set it to "Test 1.2", it will use the Test 1 folder and generate version 2. Reload index.html and it will read the questions.txt file located in the appropriate test folder. Questions are displayed in randomized order every time you reload, and you can change the title of the index page to name one of these randomized test. You can toggle the display of answers by pressing the 'a' key and can show an alert box of the answer by pressing the 'd' key.

Questions.txt
===
The questions.txt file needs to have a certain format. Questions take the following form:
```
    The minute hand of a clock is 5 inches long. What is the area of the circle, in square inches, created as the hand
    sweeps an hour?
    ===
    `10pi`
    `20pi`
    *`25pi`
    `100pi`
    `150pi`
```

The tick marks are used by ASCIIMathML.js to tell it which text to parse. In this case, the "pi" text will be rendered as the &pi; symbol. The correct answer is denoted by using an asterisk. Separate questions using two returns.
