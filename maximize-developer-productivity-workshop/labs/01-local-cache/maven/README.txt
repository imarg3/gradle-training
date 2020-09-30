Lab 01: Local build cache
=========================

NOTE: To view the build scans, use the credentials provided in the slides

- Open `.mvn/gradle-enterprise.xml`, note that the local cache is not configured explicitly since it is enabled by default

- Build the project and look at the timeline in the build scan to confirm compilation and test goals were executed

    ./mvnw clean test

    e.g.: https://enterprise-training.gradle.com/s/c4hozjdm42t72

  1. Were the results of any cacheable goals stored within the cache?
  2. Were there any timesavings due to the cache in these builds?

  Hint: To search for tasks resolved from the cache, click the magnifying glass on the timeline view and set "Goal output cacheability" to "Cacheable".

- Build again with clean, and filter the timeline view by those goals whose output were taken from cache

    ./mvnw clean test

    e.g.:  https://enterprise-training.gradle.com/s/suvhanjqluhms

  3. Which goals were resolved from the cache?
  4. Were there any cacheable goals that were not resolved from the cache?
  5. How much faster is the fully cached build than the uncached build?

- Execute just a clean

    ./mvnw clean

    e.g.: https://enterprise-training.gradle.com/s/uxfwr36udogte

- Then execute tests without clean and notice the cache was not used leading to much longer build time than previously

    ./mvnw test

    e.g.: https://enterprise-training.gradle.com/s/qoohozy2y4qd2

- (Optional) Take a look at this build scan from the Spring Boot project: https://enterprise-training.gradle.com/s/76cvqqo7xvtio

  6. How much build time could be saved if checkstyle were cacheable?
