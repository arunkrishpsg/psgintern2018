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
