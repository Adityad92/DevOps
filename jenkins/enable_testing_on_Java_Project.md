# Enable testing on a Java Project

### Pre-requisites
1. Jenkins server on T2.Medium instance
2. Maven setup

### Procedure: 
1. Install below plug-ins
   1. Junit
   2. FindBugs
   3. PMD
   4. CheckStyle
   5. Static Analysis Collector
 
 #However, without a Jenkins plugin to integrate the results of static code analysis into the build, the various XML, JSON and text files these tools crate will simply lie dormant   on the filesystem. Unfortunately, the old FindBugs, PMD and CheckStyle plugins are deprecated. Fortunately, the three deprecated plugins have been replaced by one that is         extensible and much easier to use.
      Install Jenkins Warnings Next Generation plugin from the management console and you will have a single Jenkins plugin capable of processing the results from all three             tools.
 #https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/Jenkins-Warnings-Plugin-CheckStyle-FindBugs-PMD-Example-Tutorial

1. Create a Maven Project  
   GitHub URL : https://github.com/ravdy/petclinic.git  
   Maven Goals: clean package checkstyle:checkstyle findbugs:findbugs pmd:pmd  
   Build settings: chose checkstyle, findbugs, pmd  

2. Run you job
