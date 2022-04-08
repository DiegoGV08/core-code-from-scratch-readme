# core-code-from-scratch-readme

# Week 1
## Tuesday 05/04/2022
### 1. Interpreted And Compiled Programming Languages

#### Compiled programming languajes: 
When you write your source code in your computer, this code pass in a compiler to create a separate file that contains the machine code, (a languaje that only contain 1 and 0) and this is an execatuble file. You need to “rebuild” the program every time you need to make a change.  
The compiled programming languaje is ready to run, is private, faster, not cross-platform and needs to be compiled before use it.
#### Interpreted programming languajes: 
You don't need to compile your source code, you share a copy of your code and the web browser interpreted your javascript file, ths reads line by line and processing at the time.
The interpreted programming languaje is simpler to test, is public, slower, cross-platform, easier to debug and needs a interpreter.
### 2. Is Java compiled or interpreted, or both?
Java is a combination of compiled and interpreted languaje. Java source code is compiled down to bytecode by the Java compiler. The bytecode is executed by a Java Virtual Machine (JVM) making it as interpreted language.
### 3. Pseudocode Currency Converter exercise.
1. START
2. PRINT Enter amount in dollars to convert to BTC:
3. D <--- GET // Amount in dollars
4. S <--- 0.000022358 // amount of satoshis equivalent to 1 dollar  (8:02 pm - 04/05/2022)
5. B = D*S
6. PRINT Amount of BTC is:
7. PRINT B
8. END
### 4. High and Low level languages.
#### Low level languages:
Low level language, is a language that is very close to hardware and can be directly executable on the computing hardware without any compiler or interpreter.
#### High level languages:
High level language, is a languaje that is very close to humans language, is easier to read, write and maintain.

## Wensday 06/04/2022
### 1. Your date of birth in the matrix?.
#### My birthday:  04 / 08 / 1993 - (dd/mm/yyyy)
#### Day: 100
#### Month: 1000
#### Year: 11111001001
### My birthday (binary):  100 / 1000 / 1111100100 - (dd/mm/yyyy)
### 2. MIPS.
### 2.1 Create a program that adds any two given numbers provided by the user.
    .data
            number1: .asciiz "\nIngrese el primer numero: "
            number2: .asciiz "\nIngrese el segundo numero: "
            add_numbers: .asciiz "\nEl resultado de la suma es: "
      .text
            main:
                  li $v0, 4
                  la $a0, number1
                  syscall

                  li $v0, 5
                  syscall

                  move $t0, $v0

                  li $v0, 4
                  la $a0, number2
                  syscall

                  li $v0, 5
                  syscall

                  move $t1, $v0

                  add $t2, $t0, $t1

                  li $v0, 4
                  la $a0, add_numbers
                  syscall

                  li $v0, 1
                  move $a0, $t2
                  syscall
### 2.2 Create a program that displays your name.
    .data
            name: .asciiz "\nMi nombre es: Diego Galdamez"

      .text
            main:
                  li $v0, 4
                  la $a0, name
                  syscall

## Thursday 07/04/2022
### 1. Print special numbers.
### 1.1 For.
    for (var n = 0; n <= 100; n++) {
        if (n % 2 == 0) {
            console.log(i);
        }
    }
### 1.2 While.
    var n = 0;

    while (n <= 100) {
        if (n % 2 == 0) {
            console.log(n);
        }
        n=n+1;
    }
### 1.3 do While.
    var n = 0;

    do {
        if (n % 2 == 0) {
            console.log(n);
        }
        n=n+1;
    } while (n <= 100);
### 2. Bad Code.
    var n = 100;

    if (n == 100) {
        console.log('This is a special number!');
    }
    else if (n < 1000 && n % 10 == 0 && n != 100) {
        console.log('This number is almost special');
    } else {
        console.log('Just a regular number');
    }
    
The error was in the "else if" condition, you need to add the condition of number is less than 1000, multiple of 10 and different from 100 in the same condition with the logical operator that is called "AND".
### 3. Bad Code 2.
    var cond = false;

    if ((cond == true)) {
      console.log('The cond variable is true');
    } else {
      console.log('The cond variable is false');
    }
    
The error was at the beginig of the control flow "if", you have to reemplace the = for == to make a comparisson in the control flow, not a new asignation of the variable.
