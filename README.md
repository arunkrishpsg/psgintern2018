# psgintern2018
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
/**
* Rainfall Capture
* Captures rainfall in each region based on pincode and date of rainfall. Gives average, minimum and maximum rainfall in the given date range. Amount of rainfall is indicated in cm, date is represented in DD-MM-YYYY format

* Use any of the inmemory datastructure like Array, LinkedList, Map. Do not use any persistent data store like FileSystem or Database
*/

interface RainfallCalculator {
  
  void captureRain(Float measure, 
}
