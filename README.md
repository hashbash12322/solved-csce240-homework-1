Download Link: https://assignmentchef.com/product/solved-csce240-homework-1
<br>
Everyone in computing should have a basic understanding of binary integers. To that end, you will write an app to convert decimal to binary.

The application should perform as follows:

<ul>

 <li>The program is called and runs with no prompt for input.</li>

 <li>The first value provided to the standard input stream shall be an integer and be interpreted as the number of bits of binary output. This value should be something in the range [1, 31]. Do be careful, sometimes I get careless and enter values outside this range. If that happens, the app should quietly exit with a value of 1.</li>

 <li>The second value provided is the decimal integer to be converted. Though I can guarantee that you will see values in the range [0<em>, </em>2<sup>3<a href="#_ftn1" name="_ftnref1">[1]</a></sup>− 1], I am sometimes careless about the number of bits required to represent a decimal integer. If I make a mistake by entering a value too large for the number of bits, that is on me and you should still only print the number of bits requested. If I enter a negative value, do not print a two’s complement; again, quietly exit, this time with a value of 2.</li>

 <li>An algorithm to convert decimal number, <em>n</em>, to binary (without arrays):

  <ol>

   <li>Use loop to calculate the largest power of 2, call it <em>i</em>, in <em>n</em>, print a 1 and subtract 2<em><sup>i </sup></em>from <em>n</em>.<sup>1</sup></li>

   <li>For each exponent, <em>j</em>, from <em>i </em>− 1 down to 0,</li>

  </ol></li>

</ul>

(a) if that 2<em><sup>j </sup></em>≤ <em>n</em>, print a 1 and subtract 2<em><sup>j </sup></em>from <em>n </em>(b) otherwise if that <em>n &lt; </em>2<em><sup>j</sup></em>, print a 0.

There are other algorithms which are easier as well as improvements to this algorithm. You should not solve this with an array (or string). That defeats the purpose of the assignment.

I provided you with a test file to test your code. You should ensure that your code satisfies the tester’s requirements. It is the tool I will use to grade your submissions. I will only change the input and expected values.

To utilize the tester, you will need access to a python3 interpreter. The tester can be called using the make file, assuming that python3 is in your path and that your present working directory is ../hw1

<h1>Point Awards</h1>

Correctly converting and printing a valid value is worth 2 points. Correctly catching an incorrect number of bits is worth  points. Correctly catching negative decimal input is worth  points. Style is worth 2 points. I have provided you a make file. You should definitely read the makefile and I would encourage you to read the python tester.

CSCE 240                                                                          Homework 1                                                                       Page 2 of 2

Late assignments will lose 25% per day late, with no assignment begin accepted after 4 days (100% reduction in points).

Check your syllabus for further caveats of grading.

The End.

<a href="#_ftnref1" name="_ftn1">[1]</a> Do not forget to check whether this exponent is less than or equal to the first integer passed to standard input. If it is outside that value, you should subtract as indicated, but not print. You should then find the next largest exponent and try again.