# junit-testrule

Sample application to demonstrate NPE with native-maven-plugin 0.9.12 and later. Note that this same setup works successfully with 0.9.11

To run:

1) `mvn clean install -DskipTests`
2) `cd child-project`
3) `mvn test -Pnative`
4) See the following error:

```
[INFO] -------------------------------------------------------
[INFO]  T E S T S
[INFO] -------------------------------------------------------
[INFO] Running com.example.MySampleTest
[INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.028 s - in com.example.MySampleTest
[INFO] 
[INFO] Results:
[INFO] 
[INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0
[INFO] 
[INFO] 
[INFO] --- native-maven-plugin:0.9.13:test (test-native) @ child-project ---
[INFO] ====================
[INFO] Initializing project: child-project
[INFO] ====================
[INFO] Found GraalVM installation from JAVA_HOME variable.
[INFO] ------------------------------------------------------------------------
[INFO] BUILD FAILURE
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  1.770 s
[INFO] Finished at: 2022-07-20T17:43:43-04:00
[INFO] ------------------------------------------------------------------------
[ERROR] Failed to execute goal org.graalvm.buildtools:native-maven-plugin:0.9.13:test (test-native) on project child-project: Execution test-native of goal org.graalvm.buildtools:native-maven-plugin:0.9.13:test failed.: NullPointerException -> [Help 1]

```
