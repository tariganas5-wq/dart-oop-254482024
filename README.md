Dart OOP Assignment: Kigali Bus Card

Name: Tarig Anas
Reg num: 254482024

My Numbers

* D = 24
* L = 4
* Starting balance = 1240 RWF
* Bus fare = 224 RWF
* Student discount = 14%

Part 1: BusCard

I did not add a setter for balance because I want to change it only through topUp() and pay(). This helps prevent invalid balance changes.

Part 2: StudentCard

The ~/ operator divides two numbers and returns an integer.

For example:

237 * 17 ~/ 100 = 40

It returns 40 instead of 40.29.

StudentCard extends BusCard and uses super to access the parent class.

The student discount is 31 RWF, so the final fare is 193 RWF.

Part 3: Main Output

Error: name too short
Owner: Tarig Anas | Balance: 1240 RWF
Owner: Tarig Anas | Balance: 1240 RWF
Error: top-up must be 500 to 50000 RWF
Topped up 2000 RWF
Paid 224 RWF
Paid 224 RWF
Owner: Tarig Anas | Balance: 2792 RWF
Student discount: 31 RWF
Paid 193 RWF
Owner: Tarig Anas | Balance: 1047 RWF
Student card: 14% off

Part 4: Bug Hunt

I found and fixed these five bugs:

1. Initialized _brand and _battery.
2. Added a battery setter to accept values from 0 to 100.
3. Added restart() to the Phone class.
4. Added super(brand, battery) to the SmartPhone constructor.
5. Changed p.battery() to p.battery because battery is a getter.

The use of new in Phone p = new Phone('Tecno', 50); is correct in Dart.

Output:

100

Part 5: Prediction

My prediction was:

1
5

The negative value is rejected, so the first output is 1. BigBag adds two items each time, so the second output is 5.

Actual output:

1
5

My prediction was correct.
