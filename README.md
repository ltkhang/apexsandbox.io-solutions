# Solution for problems on Apexsandbox.io

## Apex 101

### #18 - Teenager

- Problem

  ```text
  Given a person's age, return true if the person is a teenager (age 13 - 19).

  isTeenager(5) = false

  isTeenager(15) = true
  ```

- Solution

  ```java
  public Boolean isTeenager(Integer age) {
    return age >= 13 && age <= 19;
  }
  ```

### #4 - Number Difference

- Problem

  ```text
  Implement a function diff that calculates the absolute difference between two integers.

  diff(5, 2) = 3

  diff(2, 5) = 3
  ```

- Solution

  ```java
  public Integer diff(Integer a, Integer b) {
      return System.Math.abs(a - b);
  }
  ```

### #14 - Sum Equals

- Problem

  ```text
  Given Integers a, b, and c, return true if a and b add up to c.

  sumEquals(5, 5, 10) = true

  sumEquals(2, 8, 9) = false
  ```

- Solution

  ```java
  public Boolean sumEquals(Integer a, Integer b, Integer c) {
    return a + b == c;
  }
  ```

### #20 - Ascending Order

- Problem

  ```text
  Given three Integers a, b, and c, return true if they are in ascending order. For our purposes, two equal numbers will be considered to be in an ascending order.

  ascendingOrder(10, 10, 15) = true

  ascendingOrder(15, 14, 13) = false
  ```

- Solution

  ```java
  public Boolean ascendingOrder(Integer a, Integer b, Integer c) {
    return a <= b && b <= c;
  }
  ```

### #21 - A or An

- Problem

  ```text
  Given a work, prepend it with the correct indefinite article ("a" or "an") followed by a space based on the following rule: words starting with a vowel (a, e, i, o, or u) are prepended with "an", while words starting with any other letter are prepended with "a".

  aOrAn('apple') = 'an apple'

  aOrAn('banana') = 'a banana'
  ```

- Solution

  ```java
  public String aOrAn(String word) {
    String[] vowels = new List<String>{'u', 'e', 'o', 'a', 'i'};
    for (String c: vowels) {
        if (word.startsWith(c)) {
            return 'an ' + word;
        }
    }
    return 'a ' + word;
  }
  ```

### #3 - Largest of Three

- Problem

  ```text
  Given three Integers, return the largest
  ```

- Solution

  ```java
  public static Integer findLargest(Integer num1, Integer num2, Integer num3) {
    return System.Math.max(System.Math.max(num1, num2), System.Math.max(num2, num3));
  }
  ```

### #137 - Tip Calculator

- Problem

  ```text
  Create a function that given a total bill, and an integer percentage value between 0 and 100, computes the tip at the specified percentage. You can assume the percentage specified will be an integer within the valid range.

  For an example, computeTip(200.0, 50) evaluates to 100.0, because 50% of 200 is 100.
  ```

- Solution

  ```java
  public Decimal computeTip(Decimal total, Integer percent) {
    return total * percent / 100.0;
  }
  ```

### #19 - Passing Students

- Problem

  ```text
  A student passes a course if any two of the following three conditions are true: they have passed the exam, they have passed assignments, and they have passed the course project.

  Implement the function isPassed that takes in three parameters passedExam, passedAssignments, and passedProject, and returns true of at least two of the passed variables are true.

  isPassed(true, false, true) = true. Student did not pass assignments, but passes overall because they passed the exam and the project.

  isPassed(false, false, true) = false. Student only passed the project, and therefore does not pass overall.
  ```

- Solution

  ```java
  public Boolean isPassed(Boolean passedExam, Boolean passedAssignments, Boolean passedProject) {
      return (passedExam && passedAssignments) || (passedExam && passedProject) || (passedAssignments && passedProject);
  }
  ```

### #90 - Ends With 0

- Problem

  ```text
    Given an integer, return true if the integer ends with 0, otherwise return false.

    isEndWithZero(12) == false

    isEndWithZero(1230) == true
  ```

- Solution

  ```java
  public Boolean isEndWithZero(Integer num){
      //code here
      Integer lastDigit = Math.Mod(num, 10);
      return lastDigit == 0;
  }
  ```

### #15 - Which Two

- Problem

  ```text
  Given Integers a, b, and c, determine if any two of them add up to the third and return 'a', 'b', 'c' depending on which the sum is. If no two numbers add up to a third number, return an empty string. Assume that multiple solutions do not exist.

  whichTwo(5, 10, 5) = 'b'

  whichTwo(2, 0, 3) = ''
  ```

- Solution

  ```java
  public String whichTwo(Integer a, Integer b, Integer c) {
      return a + b == c ? 'c' : a + c == b ? 'b' : b + c == a ? 'a' : '';
  }
  ```

### #5 - Even or Odd

- Problem

  ```text
  Given an Integer, return 'even' if the Integer is even, or 'odd' if the Integer is odd. Remember to use the Math.mod function.

  evenOrOdd(15) = 'odd'

  evenOrOdd(-64) = 'even'
  ```

- Solution

  ```java
  public String evenOrOdd(Integer num) {
      return Math.Mod(num, 2) == 0 ? 'even' : 'odd';
  }
  ```

### #12 - Rock Paper Scissors

- Problem

  ```text
  Rock beats scissors, scissors beats paper, paper beats rock. Implement the method rockPaperScissors that takes as parameters two strings player1 and player2 representing the moves played by player 1 and player 2, valid moves being 'rock', 'paper', and 'scissors'. Return 1 if player 1 wins, 2 if player 2 wins, and 0 if no one wins.

  rockPaperScissors('rock', 'paper') = 2

  rockPaperScissors('scissors', 'paper') = 1

  rockPaperScissors('paper', 'paper') = 0
  ```

- Solution

  ```java
  public Integer rockPaperScissors(String player1, String player2) {
      if (player1 == player2) return 0;

      if (player1 == 'rock') {
          if (player2 == 'paper') return 2;
          return 1;
      }
      if (player1 == 'paper') {
          if (player2 == 'scissors') return 2;
          return 1;
      }
      if (player2 == 'rock') return 2;
      return 1;
  }
  ```

### #17 - Age Group

- Problem

  ```text
  Given a person's age, return their age group as a string: 'Infant' for ages 0-1, 'Child' for ages 2 - 14, 'Youth' for ages 15 - 21, and 'Adult' for ages 22+.

  ageGroup(5) = 'Child'

  ageGroup(15) = 'Youth'
  ```

- Solution

  ```java
  public String ageGroup(Integer n) {
      if  (n <= 1) return 'Infant';
      if  (n <= 14) return 'Child';
      if  (n <= 21) return 'Youth';
      return 'Adult';
  }
  ```

### #54 - Companion Plants

- Problem

  ```text
  Some plants are considered companion plants. They grow better when planted next to each other. For the purpose of this problem, we consider the following plants to be companions: lettuce and cucumbers, lettuce and onions, onions and carrots, and onions and tomatoes.

  Write a function isCompanion that takes as input two strings plant1 and plant2. If the two plants are companion plants based on the criteria described above, return true. Otherwise, return false.

  companionPlants('onions', 'lettuce') = true

  companionPlants('lettuce', 'tomatoes') = false
  ```

- Solution

  ```java
  public Boolean companionPlants(String plant1, String plant2) {
      Map<String, Boolean> companionMap = new Map<String, Boolean>{
          'lettuce-cucumbers' => true,
          'lettuce-onions' => true,
          'onions-carrots' => true,
          'onions-tomatoes' => true
      };
      return companionMap.get(plant1 + '-' + plant2) != null || companionMap.get(plant2 + '-' + plant1) != null;
  }
  ```

### #6 - Leap Year

- Problem

  ```text
  A year is considered a leap year if it is evenly divisible by 4, with the exception of years that are also evenly divisible by 100. Years evenly divisible by 100 must also be evenly evenly divisible by 400 to by considered leap years. Implement a method isLeapYear that takes as input an Integer year and returns true if the year is a leap year, and false otherwise.

  isLeapYear(1900) = false. Year 1900 is evenly divisible by 4, but it is also evenly divisible by 100 which means it additionally needs to be evenly divisible by 400 to qualify as a leap year. 1900 is not evenly divisible by 400.

  isLeapYear(2000) = true. Year 2000 is evenly divisible by 4. It is also evenly divisibly by 100, which means it additionally needs to be evenly divisible by 400, which it is. Therefore, it is a leap year.

  isLeapYear(2004) = true. Year 2004 is evenly divisible by 4. It is not divisible by 100, and therefore a leap year.

  isLeapYear(1933) = false. Year 1933 is not evenly divisible by 4, and therefore not a leap year.
  ```

- Solution

  ```java
  public Boolean isLeapYear(Integer year) {
      return (Math.Mod(year, 4) == 0 && Math.Mod(year, 100) != 0) || (Math.Mod(year, 400) == 0);
  }
  ```

### #7 - Prime Number

- Problem

  ```text
  A prime number is a number greater than 1 that is not evenly divisible by any number greater than one and smaller than itself. For example, 13 is a prime number because it is not evenly divisible by any number between 1 and 13.

  Implement the function isPrime that takes as input an integer greater than 1, returns true if the integer is a prime number, and returns false otherwise. Assume that the input will always be greater than 1.

  isPrime(10) = false. 10 is not a prime number because it is evenly divisible by 2 and 5.

  isPrime(23) = true. 23 is a prime number because it is not evenly divisible by any number from 2 to 22.
  ```

- Solution

  ```java
  public Boolean isPrime(Integer num) {
      for (Integer i = 2; i <= Math.round(Math.sqrt(num)); i++) {
          if (Math.Mod(num, i) == 0) return false;
      }
      return true;
  }
  ```

### #16 - Sum 1 to N

- Problem

  ```text
  Implement the method sumToN that calculates and returns the sum of all numbers (inclusive) from 1 to n. Assume that n will be non-zero positive integer.

  sumToN(5) = 15

  sumToN(2) = 3
  ```

- Solution

  ```java
  public Integer sumToN(Integer n) {
      Integer sum = 0;
      for (Integer i = 1; i <= n; i++) {
          sum += i;
      }
      return sum;
  }
  ```

### #9 - Full Name

- Problem

  ```text
  Given two non-empty strings firstName and lastName, return the name as a single string with a space in between (firstName lastName).

  formatName('Jane', 'Doe') = 'Jane Doe'
  ```

- Solution

  ```java
  public String formatName(String firstName, String lastName) {
      return firstName + ' ' + lastName;
  }
  ```

### #10 - Format Name

- Problem

  ```text
  Given two strings firstName and lastName, return the name in the format LastName, FirstName. In case one of the names is null or empty, return only the non-empty part of the name. If both are null or empty, return an empty string.

  formatName('Jane', 'Doe') = 'Doe, Jane'

  formatName('Jane', '') = 'Jane'
  ```

- Solution

  ```java
  public String formatName(String firstName, String lastName) {
      if (firstName == null || firstName == '') {
          if (lastName == null || lastName == '') {
              return '';
          }
          return lastName;
      }
      if (lastName == null || lastName == '') return firstName;
      return lastName + ', ' + firstName;
  }
  ```

### #11 - Name from Email

- Problem

  ```text
  Implement a function nameFromEmail that takes as input a valid email address in the format firstname.lastname@example.com. The function should extract the first name and last name from this email address and return a capitalized full name (i.e. FirstName LastName). Assume that the input will always be a valid email address with both the first name and last name separated by a period (.).

  nameFromEmail('john.doe@apexsandbox.io') = 'John Doe'

  nameFromEmail('JANE.DOE@GMAIL.COM') = 'Jane Doe'
  ```

- Solution

  ```java
  public String nameFromEmail(String email) {
      String[] emailParts = email.split('@', 2);
      String name = emailParts[0];
      String[] nameParts = name.split('\\.');
      String firstName = nameParts[0].toLowerCase().capitalize();
      String lastName = nameParts[1].toLowerCase().capitalize();
      return firstName + ' ' + lastName;
  }
  ```

### #79 - Change Time Format

- Problem

  ```text
  13:50 and 01:50 PM are 24-hour and 12-hour representations of the same time. Implement the method changeTimeFormat that takes as input a string strTime formatted as a 24-hour string, and returns the equivalent 12-hour string.

  Examples:

  changeTimeFormat('08:05') returns '08:05 AM'

  changeTimeFormat('00:05') returns '12:05 AM'

  changeTimeFormat('23:15') returns '11:15 PM'
  ```

- Solution

  ```java
  public String changeTimeFormat(String strTime) {
      String[] timeParts = strTime.split(':');
      String hourStr = timeParts[0];
      String minuteStr = timeParts[1];
      Integer hour = Integer.valueOf(hourStr);
      String postFix = 'AM';
      if (hour == 0) {
          hour = 12;
      } else {
          if (hour >= 12) {
              postFix = 'PM';
              if (hour > 12) {
                  hour -= 12;
              }
          }
      }
      if (hour < 10) {
          hourStr = '0' + hour.format();
      } else {
          hourStr = hour.format();
      }

      return hourStr + ':' + minuteStr + ' ' + postFix;
  }
  ```

### #13 - Fibonacci

- Problem

  ```text
  The first two numbers in the fibonacci sequence are 1, and all other numbers in the sequence are defined as the sum of the last two fibonacci numbers. The first 10 numbers in the fibonacci sequence are 1, 1, 2, 3, 5, 8, 13, 21, 34, and 55.

  Implement the function fibonacci that takes as input an Integer n and returns the nth fibonacci number. Assume that n will always be greater than 0.

  fibonacci(1) = 1

  fibonacci(2) = 1

  fibonacci(5) = 5
  ```

- Solution

  ```java
  public Integer fibonacci(Integer n) {
      if (n == 1 || n == 2) return 1;
      Integer fibo1 = 1;
      Integer fibo2 = 1;
      Integer fibo = fibo1 + fibo2;
      for (Integer i = 4; i <= n; i++) {
          fibo1 = fibo2;
          fibo2 = fibo;
          fibo = fibo1 + fibo2;
      }
      return fibo;
  }
  ```

### #8 - Next Prime

- Problem

  ```text
  A prime number is a number greater than 1 that is not evenly divisible by any number greater than one and smaller than itself. For example, 13 is a prime number because it is not evenly divisible by any number from 2 to 12.

  Implement the function nextPrime that takes as input an integer num and returns the smallest prime number greater than num.

  nextPrime(10) = 11. 11 is the smallest prime number greater than 10

  nextPrime(8) = 11. 11 is the smallest prime number greater than 8
  ```

- Solution

  ```java
  public Integer nextPrime(Integer num) {
      if (num <= 1) return 2;
      Boolean isEnd = false;
      while (!isEnd) {
          num += 1;
          Boolean isPrime = true;
          for (Integer i = 2; i <= Math.round(Math.sqrt(num)); i++) {
              if (Math.mod(num, i) == 0) {
                  isPrime = false;
                  break;
              }
          }
          isEnd = isPrime;
      }
      return num;
  }
  ```

### #113 - Reverse Order of Words

- Problem

  ```text
  Implement a function reverseWordsInASentence that will take a String containing words separated by spaces as an argument, and return a string with the order of the words reversed.

  Example : If the sentence is The quick brown fox jumps over the lazy dog, then reverseWordsInASentence(String sentence) should evaluate to dog lazy the over jumps fox brown quick The
  ```

- Solution

  ```java
  public String reverseWordsInASentence(String sentence){
      if (sentence == null) return sentence;
      String[] words = sentence.split(' ');
      String result = '';
      for (Integer i = words.size() - 1; i >= 0; i--) {
          result += words[i];
          if (i > 0) result += ' ';
      }
      return result;
  }
  ```
## Database 101

### #126 - Insert Student

- Problem

  ```text
  The method insertStudent takes as input strings name and email, and returns a record ID. Implement the method to insert an apxio__Student__c record with the Name and apxio__Email__c fields filled out, and return the Id of the new record.

  You will be working with the following custom object and field names for this problem:

  apxio__Student__c
  apxio__Student__c.apxio__Email__c
  ```

- Solution

  ```java
  public Id insertStudent(String name, String email) {
      apxio__Student__c student = new apxio__Student__c();
      student.Name = name;
      student.apxio__Email__c = email;
      insert student;
      return student.Id;
  }
  ```

### #132 - Insert Course

- Problem

  ```text
  The method insertCourse takes as input strings name and details, an integer credits, and returns a record ID. Implement the method to insert a apxio__Course__c record with the Name and apxio__Course_Details__c and apxio__Credits__c fields filled out, and return the Id of the new record.

  Note thatapxio__Credits__c is a restricted picklist with valid values 1, 2, 3, and 4. If an invalid value is provided for this picklist, return null.

  You will be working with the following custom object and field names for this problem:

  apxio__Course__c
  apxio__Course__c.apxio__Course_Details__c
  apxio__Course__c.apxio__Credits__c
  ```

- Solution

  ```java
  public Id insertCourse(String name, String details, Integer credits) {
      if (credits < 1 || credits > 4) return null;
      apxio__Course__c course = new apxio__Course__c();
      course.Name = name;
      course.apxio__Course_Details__c = details;
      course.apxio__Credits__c = String.valueOf(credits);
      insert course;
      return course.Id;
  }
  ```

### #127 - Register Student

- Problem

  ```text
  The method registerStudent takes as input strings name, phone and email, and returns a string. Implement the method to insert an apxio__Student__c record with the Name, apxio__Phone__c and apxio__Email__c fields filled out, and return the autogenerated apxio__Registration_Number__c of the new record.

  You will be working with the following custom object and field names for this problem:

  apxio__Student__c
  apxio__Student__c.apxio__Email__c
  apxio__Student__c.apxio__Phone__c
  apxio__Student__c.apxio__Registration_Number__c
  ```

- Solution

  ```java
  public String registerStudent(String name, String phone, String email) {
      apxio__Student__c student = new apxio__Student__c();
      student.Name = name;
      student.apxio__Phone__c = phone;
      student.apxio__Email__c = email;
      insert student;
      Id id = student.id;
      apxio__Student__c newStudent = [SELECT apxio__Registration_Number__c FROM apxio__Student__c WHERE Id = :Id];
      return newStudent.apxio__Registration_Number__c;
  }
  ```

### #128 - Active Students

- Problem

  ```text
  Implement the method selectActiveStudents that returns a list of all apxio__Student__c records with apxio__Active__c field checked. Make sure the students have a value in the Id and Name fields.

  You will be working with the following custom object and field names for this problem:

  apxio__Student__c
  apxio__Student__c.apxio__Active__c
  ```

- Solution

  ```java
    public List<apxio__Student__c> selectActiveStudents() {
        List<apxio__Student__c> activeStudents = [SELECT Id, Name FROM apxio__Student__c WHERE apxio__Active__c = True];
        return activeStudents;
    }
  ```

### #130 - Unreachable Students

- Problem

  ```text
  Implement the method selectUnreachableStudents that queries for and returns a list of all active apxio__Student__c records that are unreachable because they are missing both an email and a phone number. Make sure to include the Id and Name fields in the result. The returned list should be sorted A-Z on Name.
  ```

- Solution

  ```java
  public List<apxio__Student__c> selectUnreachableStudents() {
      List<apxio__Student__c> unreachableStudents = [SELECT Id, Name
          FROM apxio__Student__c
          WHERE
              apxio__Active__c = True
              AND apxio__Phone__c = null
              AND apxio__Email__c = null
              ORDER BY NAME];
      return unreachableStudents;
  }
  ```

### #129 - Students Missing Info

- Problem

  ```text
  Implement the method selectStudentsWithoutContactInfo that queries for and returns a list of all active apxio__Student__c records that are missing an email, phone, or both. Make sure to include the Id and Name fields in the result. The returned list should be sorted A-Z on Name.
  ```

- Solution

  ```java
  public List<apxio__Student__c> selectStudentsWithoutContactInfo() {
      List<apxio__Student__c> missingStudents = [
          select id, name
          from apxio__Student__c
          where apxio__Active__c = true
          and (
              apxio__Email__c = null
              or apxio__Phone__c = null
          )
          order by name
      ];
      return missingStudents;
  }
  ```

### #131 - Course and Class

- Problem

  ```text
  The method createCourseAndClass takes as input string parameters courseName and description, and returns void. Provide an implementation of the method that first inserts a apxio__Course__c record with the provided name and description (if provided) copied into the Name and apxio__Course_Details__c fields, and then inserts a child apxio__Class__c record with the same name and description copied into the Name and apxio__Description__c fields.

  There is, however, a difference between the course details and description fields on the two objects. While the apxio__Course__c.apxio__Course_Details__c has type Rich Text capable of storing thousands of characters, apxio__Class__c.apxio__Description__c can only store a maximum of 255 characters. Make sure to truncate the description to 255 characters before adding it to your apxio__Class__c record. You can assume that the provided description will never be too large for the rich text field.

  You will be working with the following custom object and field names for this problem:

  apxio__Course__c
  apxio__Course__c.apxio__Course_Details__c
  apxio__Class__c
  apxio__Class__c.apxio__Course__c
  apxio__Class__c.apxio__Description__c
  ```

- Solution

  ```java
  public void createCourseAndClass(String name, String description) {
      String classDesc;
      if (description != null) classDesc = description.left(255);
      apxio__Course__c course = new apxio__Course__c();
      course.name = name;
      course.apxio__Course_Details__c = description;
      insert course;
      Id courseId = course.Id;
      apxio__Class__c clazz = new apxio__Class__c();
      clazz.name = name;
      clazz.apxio__Description__c = classDesc;
      clazz.apxio__Course__c = courseId;
      insert clazz;
  }
  ```

### #133 - Student List

- Problem

  ```text
  The method insertStudents takes as input two lists of strings studentNames and studentEmails. The two lists will always have the same size, with studentNames[i] and studentEmails[i] (for any in-range value of i) representing a student's name and email.

  Write an implementation of the method that creates apxio__Student__c records for each entry in the lists with the Name and apxio__Email__c fields filled out.

  You will be working with the following custom object and field names for this problem:

  apxio__Student__c
  apxio__Student__c.apxio__Email__c
  ```

- Solution

  ```java
  public void insertStudents(List<String> studentNames, List<String> studentEmails) {
      List<apxio__Student__c> students = new List<apxio__Student__c>();
      for (Integer i = 0; i < studentNames.size(); i++) {
          apxio__Student__c student = new apxio__Student__c();
          student.name = studentNames[i];
          student.apxio__Email__c = studentEmails[i];
          students.add(student);
      }
      insert students;
  }
  ```

### #134 - Class from Course

- Problem

  ```text
  Implement the method classFromCourse that takes as input a string courseName, creates an apxio__Class__c record associated with the course named courseName, and returns the Id of the new record. The new class should have the same Name as the course.

  You should not create a new apxio__Course__c record. The new class should be linked to the course that already exists in the database. In case no course with the given name is found, do not create any class record and return null.

  You will be working with the following custom object and field names for this problem:

  apxio__Course__c
  apxio__Class__c
  apxio__Class__c.apxio__Course__c
  ```

- Solution

  ```java
  public Id classFromCourse(String courseName) {
      List<apxio__Course__c> courses = [SELECT Id, Name FROM apxio__Course__c WHERE Name = :courseName];
      if (courses.size() == 0) return null;
      apxio__Class__c cls = new apxio__Class__c();
      cls.apxio__Course__c = courses[0].Id;
      cls.Name = courses[0].Name;
      insert cls;
      return cls.Id;
  }
  ```

### #135 - Enroll Students

- Problem

  ```text
  Implement the method enrollStudents that takes as input a list of strings emails and a string className. The method should enroll all students with the provided emails into a class with the given name by creating apxio__Class_Enrollment__c records.

  Note that apxio__Student__c and apxio__Class__c records already exist in the database.

  You will be working with the following custom object and field names for this problem:

  apxio__Student__c
  apxio__Student__c.apxio__Email__c
  apxio__Class__c
  apxio__Class_Enrollment__c
  apxio__Class_Enrollment__c.apxio__Student__c
  apxio__Class_Enrollment__c.apxio__Offered_Class__c
  ```

- Solution

  ```java
  public void enrollStudents(List<String> emails, String className) {
      List<apxio__Class_Enrollment__c> enrollments = new List<apxio__Class_Enrollment__c>();
      List<apxio__Student__c> students = [
          select Id, apxio__Email__c
          from apxio__Student__c
          where apxio__Email__c IN :emails
      ];
      List<apxio__Class__c> cls = [
          select Id, name
          from apxio__Class__c
          where name = :className
      ];
      for (Integer i = 0; i < students.size(); i++) {
          apxio__Class_Enrollment__c enrollment = new apxio__Class_Enrollment__c();
          enrollment.apxio__Student__c = students[i].Id;
          enrollment.apxio__Offered_Class__c = cls[0].Id;
          enrollments.add(enrollment);
      }
      insert enrollments;
  }
  ```

## Apex Language Features

### #100 - sObject Type

- Problem

  ```text
  Implement the method isTypeAccount(), which accepts a sObject as input and returns a true if type of input is Account object else it should return as false.

  Given the following test code:

  Account acc = new Account(name='Apple')
  Boolean result = isTypeAccount(acc);
  result should be equal to true
  ```

- Solution

  ```java
  public Boolean isTypeAccount(sObject record)
  {
      return record instanceof Account;
  }
  ```

### #93 - Convert 15-digit ID to 18-digit ID

- Problem

  ```text
  Implement the method convert15to18DigitId() , which accepts a String of length 15 digit and returns a new String with 18 digit salesforce Id. If the input string length is not equal to 15 digits, then return '-1'.

  Given the following test code:

  String fifteenDigit = '0SO90000000PBDu';
  String eighteenDigit = convert15to18DigitId(fifteenDigit);
  eighteenDigit should be equal to '0SO90000000PBDuGAO'

  Note:

  Use case 1: You have exported a Salesforce report with Ids. These Ids are 15 characters. You want to ensure that these Ids are not altered by Excel, you need to manage them with 18 characters.
  Use case 2: You need to compare Ids but your comparison mechanism is not case sensitive. You will have to extend them to 18 characters
  ```

- Solution

  ```java
  public String convert15to18DigitId(String fifteenDigit)
  {
      if (fifteenDigit == null) return null;
      if (fifteenDigit.length() != 15) return '-1';
      ID eighteenDigit = fifteenDigit;
      return eighteenDigit;
  }
  ```

### #97 - Handle Exception

- Problem

  ```text
  Implement the method divide which takes two integers a and b as input, divides a by b using the / operator, and returns the result. If any exception occurs, the method should return the exception message.

  Given the following test code:
  String result = divide(10,0);
  result should be 'Divide by 0';
  Given the following test code:
  String result = divide(100, 18);
  result should be '5';. The result of integer division 100/19 is 5 with a remainder of 10.
  ```

- Solution

  ```java
  public String divide(Integer a, Integer b){
      try {
          Integer result = a / b;
          return String.valueOf(result);
      } catch (Exception e) {
          return e.getMessage();
      }
  }
  ```

### #102 - Throw An Exception

- Problem

  ```text
  Implement the method checkAccounts, which accepts a list of accounts as an input and returns a list of accounts. The method should behave as follows:

  If all accounts in the list have BillingCity present, the method should return the original list.
  If the passed list is null the method should throw the built-in IllegalArgumentException with message 'accounts should not be null'
  If any of the accounts in the list do not have a BillingCity present, the method should throw the custom AccountException exception with message 'Invalid BillingCity'. Do not create new exception class - use the AccountException class that has already been created for you.
  Given the following test code:

  List<Account> accounts = new List<Account>();
  accounts.add(new Account(name ='Salesforce', BillingCity ='Boston'));
  accounts.add(new Account(name ='Microsoft'));
  The method callcheckAccounts(accounts); should fail, throwing an AccountException.
  ```

- Solution

  ```java
  public List<Account> checkAccounts(List<Account> accounts)
  {
      if (accounts == null) throw new IllegalArgumentException('accounts should not be null');
      for (Account account: accounts) {
          if (account.BillingCity == null) {
              throw new AccountException('Invalid BillingCity');
          }
      }
      return accounts;
  }

  //do not remove the following custom-defined exception
  public class AccountException extends Exception {}
  ```

### #94 - Safe Navigation Operator

- Problem

  ```text
  Implement the method getAccountBillingCityWithSafeNavigation, which accepts a list of accounts as an input and returns the BillingCity in upper case of the first account in the list. Use the Safe Navigation (?.) to ensure null is returned in case the BillingCity is null.

  Given the following test code:

  List<Account> acts = new ListList<Account>();
  acts.add(new Account(Name = 'Acme', BillingCity = 'Chicago'));
  acts.add(new Account(Name = 'Dove', BillingCity = 'Boston'));
  String result = getAccountBillingCityWithSafeNavigation(acts);
  result should be 'CHICAGO'
  ```

- Solution

  ```java
  public String getAccountBillingCityWithSafeNavigation(List<Account> accounts){
    if (accounts == null) return null;
    Account account = accounts[0];
    return account.BillingCity?.toUpperCase();
  }
  ```

### #103 - Dynamic Field Values

- Problem

  ```text
  Implement the method getFieldsValue, which accepts the following inputs:

  An account acc
  A list of strings fields, with each string in the list representing a valid field on the account object.
  The method should return a list of values from the account record for fields listed in the list fields in the correct order.

  Given the following test code:
  Account acc = new Account(
      Name = 'Salesforce',
      BillingCity = 'Boston',
      AnnualRevenue=10000, Rating='Hot');
  List fields = new List{'Industry','Name','Rating'};
  List result = getFieldsValue(acc, fields);
  result should be [null, 'Salesforce', 'Hot']
  ```

- Solution

  ```java
  public List<String> getFieldsValue(Account acc, List<String> fields)
  {
      List<String> results = new List<String>();
      for (String field: fields) {
          results.add(String.valueOf(acc.get(field)));
      }
      return results;
  }
  ```

### #95 - Serialize sObjects

- Problem

  ```text
  Implement the method getAccountsInJSONFormat(), a list of accounts and returns a list of accounts in string JSON format.

  Given the following test code:

  List<Account> accounts = new ListList<Account>();
  accounts.add(new Account(Name = 'Acme', BillingCity = 'Chicago'));
  accounts.add(new Account(Name = 'Dove', BillingCity = 'Boston'));
  String result = getAccountsInJSONFormat(accounts);
  result should be equals to

  '[{"attributes":{"type":"Account"},"Name":"Acme","BillingCity":"Chicago"},{"attributes":{"type":"Account"},"Name":"Dove", "BillingCity":"Boston"}]';
  ```

- Solution

  ```java
  public String getAccountsInJSONFormat(List<Account> accounts){
    return JSON.serialize(accounts);
  }
  ```

### #101 - List of sObjects

- Problem

  ```text
  Implement the method getListOfsObject(), which accepts two parameters, a list of accounts, and a list of contacts, as an input and returns a list of sObjects. If both lists are empty or null, return an empty list of sObject.

  Given the following test code:

  List<Account> accounts = new List<Account>();
  accounts.add(new Account(name ='Salesforce'));
  accounts.add(new Account(name ='Microsoft'));
  List<Contact> contacts= new List<Contact>();
  contacts.add(new Contact(lastName = 'Benioff'));
  contacts.add(new Contact(lastName = 'Taylor'));
  List result = getListOfsObject(accounts,contacts);
  result should be (Account:{Name=Salesforce}, Account:{Name=Microsoft}, Contact:{LastName=Benioff}, Contact:{LastName=Taylor})

  Note: Adding different types into a list of sObjects can be used to perform operations on multiple object types in a single DML operation.
  ```

- Solution

  ```java
  public List<sObject> getListOfsObject(List<Account> accounts, List<Contact> contacts)
  {
      List<sObject> results = new List<sObject>();
      if (accounts != null) {
      for (Account account: accounts) {
          results.add(account);
      }
      }
      if (contacts != null) {
          for (Contact contact: contacts) {
              results.add(contact);
          }
      }
      return results;
  }
  ```

### #96 - Deserialize sObjects

- Problem

  ```text
  Implement the method getAccountsFromJSONString, which takes a JSON string of a list of accounts as an input and returns a list of accounts. If the input string is empty or null, return null.

  Given the following test code:

  String inputJSON = '[{"attributes":{"type":"Account","url":"/services/data/v55.0/sobjects/Account/00158000002zBhUAAU"},"Id":"00158000002zBhUAAU","Name":"Customer1"},{"attributes":{"type":"Account","url":"/services/data/v55.0/sobjects/Account/00158000002zBhWAAU"},"Id":"00158000002zBhWAAU","Name":"Customer2"}]';

  List<Account> result = getAccountsFromJSONString(inputJSON);
  accounts.add(new Account(Name = 'Dove', BillingCity = 'Boston'));
  result should be list of accounts (Account:{Id=00158000002zBhUAAU, Name=Customer1}, Account:{Id=00158000002zBhWAAU, Name=Customer2})
  ```

- Solution

  ```java
  public List<Account> getAccountsFromJSONString(String inputJSON){
      if (inputJSON == '' || inputJSON == null) return null;
      List<Account> accounts = (List<Account>)JSON.deserialize(inputJSON, List<Account>.class);
      return accounts;
  }
  ```

### #106 - Context User

- Problem

  ```text
  Implement the method getContextUserInformation(), which returns a Map of the current logged in user's (context user's) UserName, ProfileId, EmailId, and Type as keys and their field values as corresponding values in the map.

  Given the following sample code:

  Map<String,String> userMap = getContextUserInformation();
  ```

- Solution

  ```java
  public Map<String,String> getContextUserInformation(){
      Map<String, String> userMap = new Map<String, String>();
      userMap.put('EmailId', UserInfo.getUserEmail());
      userMap.put('ProfileId', UserInfo.getProfileId());
      userMap.put('Type', UserInfo.getUserType());
      userMap.put('UserName', UserInfo.getUserName());
      return userMap;
  }
  ```

### #105 - Trigger Validation

- Problem

  ```text
  Implement the method validateInsert, which accepts a newly inserted list of opportunities as an input and adds errors to the opportunity fields as follows: if the opportunity record's StageName is 'Closed Won' and the Description is null or empty, add an error on the Description field of that record with the error message set to 'Description should not be empty for Closed Won opportunity.'.
  ```

- Solution

  ```java
  public void validateInsert(List<Opportunity> opportunities){
      for (Integer i = 0; i < opportunities.size(); i++) {
          if (opportunities[i].StageName == 'Closed Won' && (opportunities[i].Description == null || opportunities[i].Description == '')) {
              opportunities[i].addError('Description should not be empty for Closed Won opportunity.');
          }
      }
  }
  ```

### #98 - Sort List of sObjects

- Problem

  ```text
  Implement the method getAccounts(), function, which accepts a list of accounts as input and returns a new list of accounts sorted in descending order based on the Annual Revenue field.
  ```

- Solution

  ```java
  public List<Account> getAccounts(List<Account> accounts) {
      List<Account> results = new List<Account>(accounts);
      results.sort(new AccountComparator());
      return results;
  }
  // write extra class here

  public class AccountComparator implements Comparator<Account> {
      public Integer compare(Account acc1, Account acc2) {
          if (acc1.AnnualRevenue == acc2.AnnualRevenue) {
              return 0;
          }
          if (acc1.AnnualRevenue > acc2.AnnualRevenue) {
              return -1;
          }
          return 1;
      }
  }
  ```

## SObjects

### #56 - Duplicate Contacts

- Problem

  ```text
  For this problem, we consider two Contacts as duplicates if they have the same phone number or the same email address.

  Implement the method duplicateContacts that takes as input two Contact records c1 and c1, returns true if they are duplicates, and returns false otherwise.

  For example, given the following test data:

  Contact c1 = new Contact(LastName = 'Doe', Email = 'robert@example.com');
  Contact c2 = new Contact(LastName = 'Doe', Email = 'robert.doe@example.com');
  duplicateContacts(c1, c2) == false because the two contacts do not have a phone number at all, and do not have a matching email address.
  ```

- Solution

  ```java
  public Boolean duplicateContacts(Contact c1, Contact c2) {
      Boolean isMatchPhone = false;
      if (c1.Phone != null && c2.Phone != null) {
          isMatchPhone = c1.Phone == c2.Phone;
      }
      Boolean isMatchEmail = false;
      if (c1.Email != null && c2.Email != null) {
          isMatchEmail = c1.Email == c2.Email;
      }
      return isMatchPhone || isMatchEmail;
  }
  ```

### #57 - Account Rating

- Problem

  ```text
  Implement a method setAccountRating that looks at an Account's AnnualRevenue, and sets the value of the Rating picklist field based on the following criteria:

  Accounts with AnnualRevenue less than or equal to 100,000 get a rating of "Cold"
  Accounts with AnnualRevenue less than or equal to 500,000 but greater than 100,000 get a rating of "Warm"
  Accounts with AnnualRevenue greater than 500,000 get a rating of "Hot"
  Given the following test code:

  Account a = new Account(AnnualRevenue = 150000);
  setAccountRating(a);
  The expression a.Rating == 'Warm' should be true because the AnnualRevenue was over 100,000 but less than 500,000
  ```

- Solution

  ```java
  public void setAccountRating(Account a) {
      Decimal annualRevenue = a.AnnualRevenue;
      if (annualRevenue <= 100000) {
          a.Rating = 'Cold';
      } else if (annualRevenue <= 500000) {
          a.Rating = 'Warm';
      } else {
          a.Rating = 'Hot';
      }
  }
  ```

### #59 - Contact Birthday

- Problem

  ```text
  Given a Contact with the Birthdate field set to some date, return true if today is the Contact's birthday and return false if not. Assume that a future date will not be set on the Birthdate field.

  Given the following test code:

  Contact c1 = new Contact();
  c1.Birthdate = Date.newInstance(1992, 5, 15)
  The expression isBirthday(c1) should return true if executed on 5/15/2022 or 5/15/2020.
  ```

- Solution

  ```java
  public Boolean isBirthday(Contact c) {
      if (c == null || c.BirthDate == null) return false;
      Date today = System.today();
      return c.BirthDate.day() == today.day() && c.BirthDate.month() == today.month();
  }
  ```

### #60 - Key Account

- Problem

  ```text
  For this problem, we define minimum annual revenue thresholds an account must meet to be considered a key account. The annual revenue thresholds are defined by industry:

  Banking: 600,000
  Technology: 800,000
  Retail: 2,000,000
  All others: 500,000
  Implement the method isKeyAccount that takes as input an Account with the AnnualRevenue field and the Industry picklist fields filled out, returns true if the account is a key account, and returns false otherwise.

  Account a1 = new Account();
  a1.AnnualRevenue = 750000;
  a1.Industry = 'Technology';
  The expression isKeyAccount(a1) should return false because the annual revenue does not meet the minimum threshold of 800,000 for the technology industry.
  ```

- Solution

  ```java
  public Boolean isKeyAccount(Account a) {
      Map<String, Decimal> thresholdMap = new Map<String, Decimal>();
      thresholdMap.put('Banking', 600000);
      thresholdMap.put('Technology', 800000);
      thresholdMap.put('Retail', 2000000);
      Decimal threshold = thresholdMap.get(a.Industry);
      threshold = threshold == null ? 500000 : threshold;
      return a.AnnualRevenue >= threshold;
  }
  ```

### #61 - Escalate Case

- Problem

  ```text
  In-progress cases dealing with mechanical or electrical breakdown need to be escalated. Implement a method escalateIfMeetsCriteria that takes as input a Case record, and sets the IsEscalated field to true if Type is Mechanical or Electrical, Reason is Breakdown, and Status is In Progress
  ```

- Solution

  ```java
  public void escalateIfMeetsCriteria(Case c) {
      c.IsEscalated = (c.Type == 'Mechanical' || c.Type == 'Electrical' || c.Type == 'Electronic') && c.Reason == 'Breakdown' && c.Status == 'In Progress';
  }
  ```

### #63 - Same Parent

- Problem

  ```text
  Implement the method sameParent that takes as input an opportunity opp and a contact c, and returns true if both the opportunity and contact have the same parent account.
  ```

- Solution

  ```java
  public Boolean sameParent(Contact c, Opportunity opp) {
      if (c.AccountId == null || opp.AccountId == null) return false;
      return c.AccountId == opp.AccountId;
  }
  ```

### #64 - Same Parent II

- Problem

  ```text
  Implement the method sameParent that takes as input an account acc, a contact con, and an opportunity opp and returns true if both the opportunity and contact have the given account as the parent.
  ```

- Solution

  ```java
  public Boolean sameParent(Account acc, Contact con, Opportunity opp) {
      if (acc.Id == null) return false;
      if (con.AccountId == null || opp.AccountId == null) return false;
      return acc.Id == con.AccountId && acc.Id == opp.AccountId && con.AccountId == opp.AccountId;
  }
  ```

### #66 - Set Parent Account

- Problem

  ```text
  Implement the method setParent that takes as input an account acc, a contact con, and an opportunity opp and sets the account is the parent for both the opportunity and contact. Make sure to not take any action if the provided account or its Id is null.
  ```

- Solution

  ```java
  public void setParent(Account acc, Contact con, Opportunity opp) {
      if (acc == null || acc.Id == null) return;
      con.AccountId = acc.Id;
      opp.AccountId = acc.Id;
  }
  ```

### #67 - Set Parent Case

- Problem

  ```text
  Implement the method linkParent that takes as input two cases c1 and c2, and sets the case created first as the parent of the case created later only if both cases look up to the same Contact. Ensure to handle the special case where the cases do not have any related contacts.
  ```

- Solution

  ```java
  public void linkParent(Case c1, Case c2) {
      if (c1 == null || c1.ContactId == null || c2 == null || c2.ContactId == null) return;
      if (c1.ContactId != c2.ContactId) return;
      if (c1.CreatedDate < c2.CreatedDate) {
          c2.ParentId = c1.Id;
      } else if (c1.CreatedDate > c2.CreatedDate) {
          c1.ParentId = c2.Id;
      }
  }
  ```

## Lists

### #92 - Sorting a List

- Problem

  ```text
  Implement the method getNamesInAscOrder(), which accepts a list of fullnames as input and returns the list sorted in ascending order. Use the standard library method to sort.
  ```

- Solution

  ```java
  public List<String> getNamesInAscOrder(List<String> accountNames)
  {
      if (accountNames == null) return null;
      accountNames.sort();
      return accountNames;
  }
  ```

### #1 - Array Sum

- Problem

  ```text
  Implement the method arraySum that takes as input a non-empty list of Integers numbers, and returns the sum of all numbers in the list.
  ```

- Solution

  ```java
  public static Integer arraySum(List<Integer> numbers) {
      Integer sum = 0;
      for (Integer num: numbers) {
          sum += num;
      }
      return sum;
  }
  ```

### #138 - Count Target in List

- Problem

  ```text
  Given a list of Integers nums and an Integer target, count number of times target is found in nums. If the target is not in the list, simply return 0.
  ```

- Solution

  ```java
  public Integer findTargetCount(List<Integer> nums, Integer target) {
      Integer appearanceCount = 0;
      for (Integer num: nums) {
          if (target == num) appearanceCount += 1;
      }
      return appearanceCount;
  }
  ```

### #139 - Last Occurrence

- Problem

  ```text
  Find the last occurrence of Integer target in a list of integers nums and return its index. If the target is not found, return -1

  For instance, in the list of integers {4, 6, 1, 9, 7, 9, 2}, the function would return index 0 for the target 4, index 5 for target 9 (occurs twice), and -1 for target 3 (not found).
  ```

- Solution

  ```java
  public static Integer findLast(List<Integer> nums, Integer target) {
    Integer index = -1;
    for (Integer i = 0; i < nums.size(); i++) {
        if (nums[i] == target) index = i;
    }
    return index;
  }
  ```

### #70 - Even Numbers

- Problem

  ```text
  Given a non-zero positive integer n, return a list of the first n non-zero positive even numbers, ordered ascending.

  Example: evenNumbers(5) returns a list containing the numbers 2, 4, 6, 8, 10.
  ```

- Solution

  ```java
  public List<Integer> evenNumbers(Integer n) {
      List<Integer> results = new List<Integer>();
      for (Integer i = 2; i <= 2 * n; i+=2) {
          results.add(i);
      }
      return results;
  }
  ```

### #2 - Largest Element

- Problem

  ```text
  Implement the method findLargest that takes as input a non-empty list of Integers nums, and returns the largest Integer in the list.

  Example: findLargest(new List {5, 2, 8, 4, 2, 1}) evaluates to 8 because 8 is the largest Integer in the list.
  ```

- Solution

  ```java
  public static Integer findLargest(List<Integer> nums) {
      Integer max = nums[0];
      for (Integer num: nums) {
          if (num > max) max = num;
      }
      return max;
  }
  ```

### #71 - Positive Integers

- Problem

  ```text
  A positive integer is defined as an integer greater than zero. Implement the method positiveIntegers that takes as input a list of integers numbers, and returns a new list with non-positive integers removed.

  Example: positiveIntegers(new List {2, -3, 6, 2}) returns a list containing the numbers 2, 6, 2.
  ```

- Solution

  ```java
  public List<Integer> positiveIntegers(List<Integer> numbers) {
      List<Integer> results = new List<Integer>();
      for (Integer num: numbers) {
          if (num > 0) results.add(num);
      }
      return results;
  }
  ```

### #119 - Consecutive Ones

- Problem

  ```text
  Given a List of Integers containing only binary numbers (0 and 1), return the maximum number of consecutive 1s appearing in the List.
  ```

- Solution

  ```java
  public Integer maxConsecutiveOnes(Integer[] numbers) {
      Integer maxAppearanceCount = 0;
      Integer curAppearance = 0;
      numbers.add(0);
      for (Integer num: numbers) {
          if (num == 0) {
              maxAppearanceCount = curAppearance > maxAppearanceCount ? curAppearance : maxAppearanceCount;
              curAppearance = 0;
          } else {
              curAppearance += 1;
          }
      }
      return maxAppearanceCount;
  }
  ```

### #136 - Number Average

- Problem

  ```text
  Given a list of decimals, return the average rounded to two decimal places.
  ```

- Solution

  ```java
  public Decimal average(List<Decimal> numbers){
      Integer numberCount = numbers.size();
      if (numberCount == 0) return 0;
      Decimal sum = 0;
      for (Decimal num: numbers) sum += num;
      return (sum / numberCount).setScale(2);
  }
  ```

### #111 - Insert at Beginning

- Problem

  ```text
  Implement a method that would take an element and a List of elements as arguments and return the same List with the element inserted at the 0th position.
  ```

- Solution

  ```java
  public void insertAtStart(String cityName, List<String> cities) {
      if (cities == null) return;
      if (cities.size() == 0) { cities.add(cityName); return; }
      String firstItem = cities[0];
      cities.add('');
      cities[0] = cityName;
      for (Integer i = 1; i < cities.size(); i++){
          String tmp = cities[i];
          cities[i] = firstItem;
          firstItem = tmp;
      }
  }
  ```

### #72 - Full Names

- Problem

  ```text
  Implement the method fullNames that takes as input two equal-sized lists of strings firstNames and lastNames, and returns a new list containing full names, with each full name generated by the concatenating the first name and last name at the corresponding location in the input lists.
  ```

- Solution

  ```java
  public List<String> fullNames(List<String> firstNames, List<String> lastNames) {
      List<String> fullNames = new List<String>();
      for (Integer i = 0; i < firstNames.size(); i++) {
          fullNames.add(firstNames[i] + ' ' + lastNames[i]);
      }
      return fullNames;
  }
  ```

### #55 - Companion Plants 2

- Problem

  ```text
  Some plants are considered companion plants. They grow better when planted next to each other. For the purpose of this problem, we consider the following plants to be companions: lettuce and cucumbers, lettuce and onions, onions and carrots, and onions and tomatoes. The same plants planted next to each other are not considered companions.

  Write a function isCompanion that takes as input a list of plants being planted in a row. Return true only if every plant in the list is planted next to a companion and return false otherwise.

  companionPlants(new List { 'onions', 'lettuce', 'onions', 'carrots', 'onions', 'lettuce', 'cucumbers'}) = true

  companionPlants(new List { 'lettuce', 'onions', 'carrots', 'lettuce', 'cucumbers'}) = false. We have non-companion plants carrots and lettuce planted together
  ```

- Solution

  ```java
  public Boolean companionPlants(List<String> plants) {
      if (plants.size() == 0) return true;
      if (plants.size() == 1) return false;
      Map<String, String> companionMap = new Map<String, String>();
      companionMap.put('lettuce', 'cucumbers');
      companionMap.put('cucumbers','lettuce');
      companionMap.put('lettuce', 'onions');
      companionMap.put('onions','lettuce');
      companionMap.put('onions','carrots');
      companionMap.put('carrots', 'onions');
      companionMap.put('onions','tomatoes');
      companionMap.put('tomatoes', 'onions');
      Boolean isCompanion = true;
      for (Integer i = 1; i < plants.size(); i++) {
          if (companionMap.get(plants[i]) != plants[i - 1]) {
              isCompanion = false;
              break;
          }
      }
      return isCompanion;
  }
  ```

### #69 - Fibonacci Series

- Problem

  ```text
  The first two numbers in the fibonacci sequence are 1, and all other numbers in the sequence are defined as the sum of the two preceding fibonacci numbers. The first 10 numbers in the fibonacci sequence are 1, 1, 2, 3, 5, 8, 13, 21, 34, and 55.

  Given a non-zero positive integer n, return a list of integers of size n containing (in correct order) the first n numbers in the fibonacci series.

  Example: fibonacciSeries(5) returns a list containing the numbers 1, 1, 2, 3, and 5.
  ```

- Solution

  ```java
  public List<Integer> fibonacciSeries(Integer n) {
      List<Integer> results = new List<Integer>();
      if (n == 0) return results;
      if (n == 1) {
          results.add(1);
          return results;
      }
      if (n == 2) {
          results.add(1);
          results.add(1);
          return results;
      }
      results.add(1);
      results.add(1);
      for (Integer i = 2; i < n; i++) {
          results.add(results[i - 1] + results[i - 2]);
      }
      return results;
  }
  ```

### #74 - Org Names

- Problem

  ```text
  Some Salesforce orgs (Trailhead playground orgs, for example) are given random names that include a combination of an adjective and an animal as a prefix. For instance, cunning-impala, curious-raccoon, and brave-hawk are possible prefixes for names for such orgs.

  Implement the method generateOrgNames that takes as input two lists of strings adjectives and animals, and returns a list of strings containing all org name prefixes that can be formed by combining the adjectives and animals. Assume that the input lists will never be empty
  ```

- Solution

  ```java
  public List<String> orgNames(List<String> adjectives, List<String> animals) {
      List<String> results = new List<String>();
      for (String adj: adjectives) {
          for (String animal: animals) {
              results.add(adj + '-' + animal);
          }
      }
      return results;
  }
  ```

### #73 - Sorted List

- Problem

  ```text
  A list is considered to be sorted ascending when no element in the list is smaller than the preceding element if one is present. Similarly, a list is considered sorted descending if no element in the list is larger than the preceding element if any.

  Implement the method isSorted that takes as input a list of integers numbers, returns true if the list is sorted in any direction (acsending or descending), and returns false otherwise.

  Example: isSorted(new List<Integer> {5, 2, 0, -1}) evaluates to true because the input list is sorted descending.
  ```

- Solution

  ```java
  public boolean isSorted(List<Integer> numbers) {
      Boolean isAsc = true;
      Boolean isDesc = true;
      for (Integer i = 0; i < numbers.size() - 1; i++) {
          if (numbers[i] > numbers[i + 1]) isAsc = false;
          if (numbers[i] < numbers[i + 1]) isDesc = false;
      }
      return isAsc || isDesc;
  }
  ```

### #68 - Second Largest Element

- Problem

  ```text
  Given an list of Integers numbers, return the second largest integer in the list. Assume that the input list will always contain at least two distinct integers.

  Example: secondLargest(new List {5, 2, 8, 4, 8, 1}) evaluates to 5 because 5 is the second largest Integer in the array, with 8 being the largest integer.

  Note: While not necessary to solving this problem, it may be be helpful to know the smallest possible Integer: -2,147,483,648. However, you cannot set an integer directly to this value because of a bug in Apex, but you can do the following:

  Integer num = -2147483647 - 1;
  ```

- Solution

  ```java
  public Integer secondLargest(List<Integer> numbers) {
      Integer max = numbers[0];
      for (Integer num: numbers) {
          if (num > max) max = num;
      }
      Integer secondmax = -2147483647 - 1;
      for (Integer num: numbers) {
          if (num > secondmax && num < max) secondmax = num;
      }
      return secondmax;
  }
  ```
