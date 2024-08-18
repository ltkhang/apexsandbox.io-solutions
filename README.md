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
