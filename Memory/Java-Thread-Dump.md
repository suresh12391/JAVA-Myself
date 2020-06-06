Java Memory Analysis:
=====================

1) JConsole (J2SE Monitoring and Management Console)
   Ex: jconsole

2) JVisualVM
   Ex: visualvm

3) JMap (Java Memory Map)
   Ex: jmap -dump:format=b,file=heap_dump.bin PATH PID
       jmap -histo PID | head

4) Jhat (Java Heap Analysis Tool) 
   Ex: jhat heap_dump.bin

5) jstack PID > thread_dump.log or jcmd <PID> Thread.print

6) kill -3 PID. Writes the dump into catalina.out file incase of tomcat process.


CMD:
====
- jps
- ps -au
- jmap -dump:format=b,file=heap_dump.bin PATH PID
- jstack PID > thread_dump.log
- jmap -clstats PID
- ps -aef | grep "tomcat"
- kill -3 <PID>
- jstack PID > thread_dump.log

Reference:
https://spring.io/blog/2015/12/10/spring-boot-memory-performance
