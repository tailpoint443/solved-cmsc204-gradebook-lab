Download Link: https://assignmentchef.com/product/solved-cmsc204-gradebook-lab
<br>



You will be creating a JUnit Test Class for Gradebook.java, that has been provided for you.  Upload Gradebook.java and GradeBookTest.java to the repository in GitHub you created in Lab 1 in a directory named JUnit_Lab.

Add the following two methods to the Gradebook class.  Do not modify the other methods of Gradebook.

<ol>

 <li>Add a getScoreSize() method to the Gradebook class which returns scoresSize;</li>

 <li>Add a toString() method to the Gradebook class that returns a string with each score in scores separated by a space.</li>

</ol>




Create the Test Class GradebookTester.

<ol>

 <li>Select the setUp and tearDown method.</li>

 <li>Select all of the methods of Gradebook, except for the constructor to create tests for.</li>

 <li>In the setUp method of GradebookTester, create at least two objects of Gradebook of size 5. Call the addScore method for each of the Gradebook classes at least twice (but no more than 5 times).</li>

 <li>In the teardown method of GradebookTester, set the two objects of Gradebook to null;</li>

 <li>Create test for the methods of Gradebook:

  <ol>

   <li>addScore

    <ol>

     <li>Use the toString method to compare the contents of what is in the scores array vs. what is expected to be in the scores array</li>

    </ol></li>

  </ol></li>

</ol>

assertTrue( . . .)

<ol>

 <li>Compare the scoreSize to the expected number of scores entered.</li>

</ol>

assertEquals(. . .)

<ol>

 <li>sum

  <ol>

   <li>Compare what is returned by sum() to the expected sum of the scores entered.</li>

  </ol></li>

 <li>minimum

  <ol>

   <li>Compare what is returned by minimum() to the expected minimum of the scores entered.</li>

  </ol></li>

 <li>finalScore

  <ol>

   <li>Compare what is returned by finalScore() to the expected finalscore of the scores entered.</li>

  </ol></li>

</ol>

The finalScore is the sum of the scores, with the lowest score dropped if there are at least two scores, or 0 if there are no scores.

Example:




Add a private member of GradeBookTest:

GradeBook g1;




In setup:

g1 = new GradeBook(5);

g1.addScore(50);

g1.addScore(75);




In teardown:

g1 = null;




in testSum():

assertEquals(125, g1.sum(), .0001);




in testMinimum():

assertEquals(50, g1.minimum(), .001);




in addScoreTest();

assertTrue(g1.toString().equals(“50.0 75.0 ”);





