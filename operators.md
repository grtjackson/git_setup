#OPERATORS
++counter - prefix, increments first
counter++ - postfix, increments after

#prefix
let counter = 1;
let a = ++counter; // increments first, returns 2
console.log(a); //2

The prefix will return the value after it has incremented,
the console will log 2.

#postfix
let counter = 1;
let a = counter++; //returns 1, then increments
console.log(a); //a

The postfix will return the current value (1) before adding the increment,
the console will log 1 but the value is 2 now.



#No assignment
++counter
counter++

both of these increment by 1 when there is no return value.

