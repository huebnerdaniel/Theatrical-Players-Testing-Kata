# Theatrical-Players-Testing-Kata

The idea for this kata originates from the case study of the Refactoring book by Martin Fowler.

However, I did not want to start with the existing code and do the refactoring but rather take the requirements and use them to build up the production code with backing tests. 

Why? 

Because I see potential in the requirements for developing the production with domain objects only. This is a different approach than using stateless service class with stateful JavaBeans as data containers very common in my current team (and others I've worked with).

Your task is to complete as many of the requirements as you like or can be done in the given time box.

## Prerequisites

The project uses JDK 11, Apache Maven, JUnit 5 and my common setup with Lombok and AssertJ (as maven dependencies).

## Requirements 

A theater offers special performances that can be booked by companies for in-house events. A company simply books a performance and fills the theatre with their employees and friends & family. Depending on the play type, a number of seats are included in the base price. For addition seats an extra charge per seat is added to the base price. Number of included seats and seat price differ between the play types. Also, the company collects credits, they get one credit per seat that is booked additionally to the first 30 seats that are uncredited.

The theatre currently has the following play types and parameters attached:

### tragedy

* Base price is USD 400
* Included seats: 30
* Extra charge per additional seat: USD 10

### comedy

* Base price is USD 300
* Included seats: 20
* Extra fee, in case more than 20 seats are taken (upgrade to bigger show room): USD 100 
* Extra charge per additional seat: USD 5
* Extra credits for every five comedy attendees

## Sample input

BigCo ordered three performances of the theatre in total. Now it is time to send them their invoice statement.

Here are the details of the performances:
* Hamlet, tradegy, 55 seats booked
* As you like it, comedy, 35 seats booked
* Othello, tradegy, 40 seats booked

The statement send to BigCo reads:

    Statement for BigCo
        Hamlet: $650.00 (55 seats)
        As You Like It: $580.00 (35 seats)
        Othello: $500.00 (40 seats)
    Amount owed is $1,730.00
    You earned 47 credits