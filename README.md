# Dart OOP Assignment: Kigali Bus Card

**Name:** Tarig Anas  
**Student ID:** 254482024

## My Numbers

- D = 24
- L = 4
- Starting balance = 1240 RWF
- Bus fare = 224 RWF
- Student discount = 14%

## Part 1: BusCard

The balance does not have a setter because it should only be changed through controlled methods such as topUp() and pay(). This prevents invalid balance changes.

## Part 2: StudentCard

The `~/` operator performs integer division and returns an integer instead of a decimal number.

For example:

`237 * 17 ~/ 100 = 40`

Using `/` would return `40.29`.
### How StudentCard works

StudentCard extends BusCard, so it inherits its properties and methods.

The super keyword calls the parent class constructor and methods.

The pay() method calculates the discount first, then calls super.pay() to deduct the discounted fare from the balance.

### How my personal numbers are used

My starting balance is 1240 RWF.
My bus fare is 224 RWF.
My student discount is 14%.

The discount is 31 RWF after integer division.
The final student fare is 193 RWF.

## Part 3: Main Output

```text
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
```

## Part 4: Bug Hunt

The five bugs and their corrections:

1. The private fields were not initialized. I initialized `_brand` and `_battery`.
2. The battery setter was missing. I added a setter that accepts values from 0 to 100.
3. The parent class did not have a `restart()` method. I added it so the child class can override it.
4. The SmartPhone constructor was missing the call to the parent constructor. I added `super(brand, battery)`.
5. The battery getter was called like a method. I corrected `p.battery()` to `p.battery`.

The line `Phone p = new Phone('Tecno', 50);` is correct because using `new` is allowed in Dart.

### Part 4 Output

```text
100
```

## Part 5: Prediction

My prediction before running the program:

```text
1
5
```

### Explanation

The first Bag has 1 item because the negative value is rejected by the setter.

BigBag adds 2 items each time its add() method is called. After two calls, it has 4 items. Then one more item is added, making the final value 5.

### Actual Output

```text
1
5
```

My prediction was correct.