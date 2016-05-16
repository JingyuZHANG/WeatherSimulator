Test Data for the Weather Prediction
========================

This software used to provide non existing sequences of weather data in buildings applications with a method adopted to all kind of climates. There are four modules of description, modelling, generations, and evaluation of weather data. Except fact data in item.txt, a user also can modified the dataset via alerts.json file.  The value of "temperaturechange" can be change to any value in alerts.json. For example, setting { "temperaturechange":1} which means all dataset will be increased 1% if a user want a warm sequence.

It develop with java 1.7 on Eclipse with MacOs 10.10.x. A nested HashMap is used to store items in this model because the  time complexity for look up and insert a HashMap is O(1) if there is not a hash collision. The Arrays<> is good solution to replace this hashMap if the number of items is defined.

The algorithms in this application are reference some research papers in following

[1] Harry Boyer, François Garde, Jean Claude Gatina, Jean Brau:
    A multimodel approach to building thermal simulation for design and research purposes. CoRR abs/1212.5262 (2012)

[2] Laetitia Adelard, Harry Boyer, F. Garde, Jean Claude Gatina:
    Detailed weather data generator for building simulations. CoRR abs/1212.3930 (2012)

[3] L. O. Degelman, A Weather simulation model for Building Analysis ASHRAE Trans., Symposium on Weather Data, Seattle, WA,435-447 (1995)

[4] L. O. Degelman, A statistically -based hourly weather data generator for driving energy simulation and equipment design
software for buildings.2nd world congress of technology for improving the energy use, comfort, and economic of building
worldwide, International Building Performance Simulation As., Nice, Sophia-Antipolis (1991)


System requirements
-------------------

All you need to build this project is Java 1.7 or better, Maven 2.6 or better.

The application this project produces is designed to be run on command line

Configure Maven
---------------

If you have not yet done so, you must configure Maven before using this project. 

Run the application 
-------------------

(1)
./start.sh

OR

(2)

java -cp Interview.jar Main <file> <file> <date> <duration> <file>

e.g. java -cp Interview.jar Main items.txt alerts.json 2016-05-20 30 output.txt


Debug the Application
------------------------------------

If you want to debug the source code in the project, run either of the following commands to pull them into your local repository. The IDE should then detect them.

        mvn dependency:sources



Functional testing
------------------------------------

Run

java -cp Interview.jar Main items.txt alerts.json 2016-06-20 30 output.txt

Output

--------------------------------------------

SYD|33.86,151.21,39|2016-06-20T01:22:20Z|Sunny|+9.6|1092|27

HBA|42.83,147.5,4|2016-06-20T01:22:24Z|Sunny|-3.9|1057|20

SYD|33.78,151.11,65|2016-06-20T01:22:21Z|Snow|-1.9|967|50

MEL|37.73,144.91,78|2016-06-20T01:22:12Z|Sunny|-3.7|1124|22

MEL|37.76,144.83,113|2016-06-20T01:22:15Z|Sunny|+6.3|1082|28

HBA|42.89,147.33,51|2016-06-20T01:22:13Z|Snow|-2.5|883|57

BNE|27.48,153.04,8|2016-06-20T01:22:19Z|Sunny|+5.1|1097|39

BNE|27.39,153.13,5|2016-06-20T01:22:20Z|Sunny|+12.6|1110|37

PER|31.93,115.98,15|2016-06-20T01:22:26Z|Snow|-0.9|909|57

.......
--------------------------------------------
=============================================
