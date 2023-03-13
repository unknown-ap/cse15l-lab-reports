# Lab Report 5
For Lab Report 4, a different method of completing the task is using a `bash` script. This would allow me to only have to run one command in the terminal instead of all the ones necessary for steps 4-9. For example, I could create a file called `tasks1.sh` and add in all of the following commands on separate lines:  
```
ssh cs15lwi23aok@ieng6.ucsd.edu
git clone git@github.com:unknown-ap/lab7.git
cd lab7/
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
nano ListExamples.java
```

Then I could edit the file and run the next bash file called `tasks2.sh` that would have these lines of code:  
```
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
git commit ListExamples.java -m "changes"
git push
```
In order to run these bash scripts, I would just type in `bash tasks1.sh` and `bash tasks2.sh`, which is must faster than typing out everything above. 
