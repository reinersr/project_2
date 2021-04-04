Robert Reiners
Project 2

<h2>Question 1</h2>
LOCAL
spark-submit --class project_2.main --master local[*] target/scala-2.12/project_2_2.12-1.0.jar .\2014to2017.csv exactF2
==================================
Exact F2. Time elapsed:140s. Estimate: 0
==================================

GCP
==================================
Exact F2. Time elapsed:45s. Estimate: 0
==================================

<h2>Question 2</h2>
LOCAL
spark-submit --class project_2.main --master local[*] target/scala-2.12/project_2_2.12-1.0.jar .\2014to2017.csv ToW 10 3
==================================
Tug-of-War F2 Approximation. Width :10. Depth: 3. Time elapsed:4s. Estimate: 9
==================================

GCP
==================================
Tug-of-War F2 Approximation. Width :10. Depth: 3. Time elapsed:12s. Estimate: 1
==================================

<h2>Question 3</h2>
LOCAL
spark-submit --class project_2.main --master local[*] target/scala-2.12/project_2_2.12-1.0.jar .\2014to2017.csv BJKST 10 5
==================================
BJKST Algorithm. Bucket Size:10. Trials:5. Time elapsed:5s. Estimate: 22.0
==================================

GCP
==================================
BJKST Algorithm. Bucket Size:10. Trials:5. Time elapsed:16s. Estimate: 22.0
==================================

<h2>Question 4</h2>
The Tug of War and exact F2 were close, but not exactly the same, for the amount of data being analyzed, it is a good estimate. The BJKST and exact F0 were very far off. The exact F0 yielded 7406649 while BJKST was nowhere near that.