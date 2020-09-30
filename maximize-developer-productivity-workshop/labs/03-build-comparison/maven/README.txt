Lab 03: Goal inputs comparison
==============================

NOTE: To view the build scans, use the credentials provided in the slides

- Build the project two times in a row

    ./mvnw clean test

    example first build scan:
    https://go.gradle.com/wb-ch5-m1

    example second build scan:
    https://go.gradle.com/wb-ch5-m2

  1. Which goal(s) are cacheable but are still executed instead of being resolved from the cache?

- From either scan, click the Compare Build scan button on the lower left and compare these two builds.

  2. Which inputs are impacting goal cacheability?
  3. How would you fix the timestamp problem? Apply those changes before moving forward.

- Now build the project two times in a row again and look at both scans.

    ./mvnw clean test

    e.g.: https://go.gradle.com/wb-ch5-m4

  4. Are all cacheable goals being resolved from the cache or does some volatility remain?
  5. Are the avoidance savings for these builds better or worse than the builds that included
  timestamp files?
