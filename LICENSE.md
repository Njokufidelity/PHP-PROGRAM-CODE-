
Write a php program code that we store the number of courses in an array and assign a score to them.
The courses are
COM411
COM412
COM413
COM414
COM415
GNS412
EED412
the program we implement the following
An array
For loop 
If else









Here's the PHP program code that stores the number of courses in an array, assigns scores, and utilizes a loop and conditional statements:


<?php

// Define the courses as an array
$courses = array("COM411", "COM412", "COM413", "COM414", "COM415", "GNS412", "EED412");

// Loop through each course
for ($i = 0; $i < count($courses); $i++) {
  
  // Prompt user to enter score for current course
  echo "Enter score for " . $courses[$i] . ": ";
  $score = (int)fgets(STDIN); // Read input and convert to integer

  // Validate score (optional)
  if ($score < 0 || $score > 100) {
    echo "Invalid score. Please enter a score between 0 and 100.\n";
    continue; // Skip to next iteration
  }

  // Display score based on grade range
  if ($score >= 90) {
    echo "Grade: A (Excellent)\n";
  } elseif ($score >= 80) {
    echo "Grade: B (Very Good)\n";
  } elseif ($score >= 70) {
    echo "Grade: C (Good)\n";
  } elseif ($score >= 60) {
    echo "Grade: D (Satisfactory)\n";
  } else {
    echo "Grade: F (Failing)\n";
  }
}

?>
