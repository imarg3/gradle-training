Lab 04: Troubleshooting with build scans
=============================

NOTE: To view the build scans, use the credentials provided in the slides
See SOLUTIONS.TXT for additional context and answers to the questions posed by this lab

1. Run a build to publish a build scan

      ./mvnw clean test

2. Follow the link in the console output to view your build scan. If prompted to login, use username "attendee", password "gradle"

  e.g.: https://enterprise-training.gradle.com/s/tmdsvcaeeyaao

3. Find the answers to the following questions:

  - How much time is being spent on garbage collection?
  - What is the peak memory usage?

4. Fix the issue degrading build performance

  - Hint: https://maven.apache.org/ref/3.6.1/maven-embedder/

5. Find the answers to the following questions:

  - Are the custom-logger project and example-project modules compiling with the same version slf4j-api?
  - Why does the console log contain messages about multiple slf4j bindings?

6. Fix the dependency issues discovered in step 5 so that only a single implementation of slf4j is used

  - Hint: For small builds, keeping all dependency declarations consistent can be sufficient

7. Publish another build scan and verify that the memory pressure and dependency issues are fixed

e.g.: https://enterprise-training.gradle.com/s/7gsdmd3ryq5oo

8. Find the "See before and after" button toward the bottom of the left column of the build scan
   - In the list of builds you've run, find the first build scan you produced for this project
   - Mouse over the earlier build and click the "compare with this build" button that looks like a venn-diagram
   - Observe the impact of your fixes in the build comparison view

9. Optional: Open this build scan taken from the Gradle Build Tool project:
  https://enterprise-training.gradle.com/s/rzht6qise5ujg

  Find the answers to the following questions:
    - What version of `commons-lang` is used by the build?
    - How many times is the `publishing` plugin applied to the build?
    - What OS and JVM versions was the build run with?
    - Was the build cache enabled?
    - How much time was spent configuring the build?
    - Was there any memory pressure while running the build?
    - What was the average download speed when fetching from the remote cache?
    - How long was the daemon that executed the build already running before?
