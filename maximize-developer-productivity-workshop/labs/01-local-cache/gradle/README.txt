Lab 01: Local build cache
=========================

NOTE: To view the build scans, use the credentials provided in the slides

- Open `gradle.properties`, note that caching is enabled
    - verbose console is enabled to make seeing the effects of caching easier

- Build the project and look at the timeline in the build scan to confirm compilation and test tasks were executed

    ./gradlew build

    e.g.: https://go.gradle.com/wb-ch3-g1

  1. Were the results of any cacheable tasks stored within the cache?
  2. Were there any timesavings due to the cache in these builds?

Hint: To search for tasks resolved from the cache, click the magnifying glass on the timeline view and set "Task output cacheability" to "Cacheable".

- Build again with clean, and filter the timeline view by those tasks whose output were taken from cache

    ./gradlew clean build

    e.g.: https://go.gradle.com/wb-ch3-g2

  3. Which tasks were resolved from the cache?
  4. Were there any cacheable tasks that were not resolved from the cache?
  5. How much faster is the fully cached build than the uncached build?

- (Optional) Take a look at this build scan from the Gradle Build tool project. https://enterprise-training.gradle.com/s/rzht6qise5ujg

  6. Which task types are not cacheable?

