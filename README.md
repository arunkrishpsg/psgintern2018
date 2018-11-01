# Internship @ PSG Software Technologies (Academic Year: 2018 - 19)
Assessments for internship at PSG Software Technologies for the period Dec 2018 till May 2019

## Programming Aptitude

### 1. Implement the following function

```Java
/**
* The function obfuscate converts the given input string to another string based on the following logic in the given order
* 1. If a word in the string is present in given wordMap (a Map data structure having key - value pair, replace the word with its corresponding value in the wordMap in the output string
* 2. Else if a word is composed of all numerical characters, then multiply that number with the number in "charOffset" parameter and place it in output string
* 3. Else replace every character in the word with the ASCII offset given in charOffset. For instance charOffset of 2 applied on A (ascii value 65) is C
* Keep the special characters as it is
*/

String obfuscate(String input, Integer charOffset, Map<String, String> wordMap);
```

### 2. Implement the following interface

```Java
/**
* Rainfall Capture
* Captures rainfall in each region based on pincode and date of rainfall. Gives average, minimum and maximum rainfall in the given date range. Amount of rainfall is indicated in cm, date is represented in DD-MM-YYYY format

* Use any of the inmemory datastructure like Array, LinkedList, Map. Do not use any persistent data store like FileSystem or Database
*/

interface RainfallCalculator {
  /**
  * Captures rain occured in the given region
  * @param measure amount of rainfall in centi meters
  * @param rainDate date on which rainfall measure is recorded
  * @param pincode identifies the location of rainfall where this was recorded
  */
  void captureRain(Float measure, Date rainDate, String pincode);
  
  /**
  * Region which has gt maximum rainfall in the given . If more than 1 region got the same maximum, then return whichever has got the rain recently.  If both have got the rain on the same date, return whichever was captured first
  */
  RainfallRegion getRegionWithMaxRainfall(Date fromDate, Date toDate);
  
  /**
  * Similar to above, but which region has got minimum rainfall
  */
  RainfallRegion getRegionWithMinRainfall(Date fromDate, Date toDate);
  
  /**
  * Compute the average rainfall in the given date range and return the average
  */
  Float getAverageRainfall(Date fromDate, Date fromDate);
}
```

For the above problem assume that you have the following class defined. Feel free to create as many classes as you want to solve the above problem

```Java
class RainfallRegion {
  String pincode;
  Float measure;
}
```

## Object Oriented Analysis and Design

### 1. Student Trip Planner
Analyze the below mentioned system requirements and come up with an system design and to be specific object oriented design identifying Entities, States / Properties and behaviour

Assume that you have read only access to student database containing their basic information and all the information about the student that you need for this system. Whenever there is a vacation, students in hostel have to book tickets to and from their home town. This student trip planner, helps in bringing co-located students (students in same city) together to collaborate and schedule their trip.

System's admin maintain data about transport agencies, their buses and cost. They also create / maintain vacations as per the acadmic calendar. Sets-up reminder / notification to student for various process steps.

A trip plan starts by  creation of a trip in the system specifying their destination date, time and place.  The student who is creating a trip, can invite his / her friends to join the trip. Students in the same place gets notified about a new trip being created and they join the trip by opting for it.

One week before the start date for vacation, system admin gets a regionwise report showing how many students have joined together for a trip to a particular destination.

System admin, can launch a poll to choose the bus or choose the time to leave.

Once the bus is selected, system admin can collect the payment to confirm the booking and update their payment status.

For the return trip too, a similar approach can be followed.

DO NOT have to implement any login screen as the system will leverage the single-sign-on server.
