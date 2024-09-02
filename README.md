# BrainF-ck

===================================
Basics of BrainFuck
===================================

===================================

Chapter 1-

BrainFuck?

Brainfuck is an esoteric programming language created in 1993 by Urban Müller. 
Notable for its extreme minimalism, the language consists of only eight simple commands, a data pointer and an instruction pointer.

How to use BrainFuck

As stated previosly, there are only 8 simple commands that consist of the following characters:
.,+-[]<>

When you are thinking about BrainFuck, you want to think about thousands of tables with a pointer that points at only one.


[ ] [ ] [ ] [ ] [ ] [ ] [ ] ...

 ^

 
Each table can hold a value and the pointer can change which table it is pointing at.
Let's start looking at how to code in this language now.

Like previously mentioned, we can change which table the pointer is looking at by using the < and > symbols.
> : Move to the table on the right
< : Move to the table on the left

If I type > and run the code, this is what happens.

>

[ ] [ ] [ ] [ ]

     ^
     
As you can see the pointer changed from the first table to the second.
Next we can add values to the tables. Each table has a starting value of zero.

+ : Add 1 to a table
- : Subtract 1 from a table

So what we can do is - 

++++++++++>+++++

[10] [5 ] [ ] [ ] [ ]

      ^
As we can see, we added 10 to the first table. Then we moved the pointer to the second table and added 5.

Now, this may still seem some what obscure but it will slowly add up.
Each letter on our keyboard has been given an ASCII value. We can find these values by searching it up on the internet.
To output something withour code, we need to make a table equal the value of the desired output.
Let's use an example.

>+++++++++[<++++++++>-]<.

The code given may seem complicated but if you can multiply, this should make sense soon.
The code prints the letter H which has an ASCII Value of 72.
If you want to print H, we can of course just add 72 + signs, but that would be really annoying and tedious.
So instead, we can use loops indicated by the [ ] signs.
Let's break down the code.

First, we move the pointer to the right and add 9.

[ ] [9] [ ] [ ]

     ^
     
Next we start the loop.
In the most simplest terms, the code adds 8 to the first table everytime the second table looses 1.
We can see that in the code, after the bracet, it moves back the the first table, adds 8, then goes to the second table, and subtracts 1.
This reapeats until the second table reaches zero.
Once it does, we can print the output with the . symbol.
We can see how the table looks after a few loops.

[8] [8]

     ^
     
[16] [7]

     ^
     
...

[72] [0]

      ^
      
If we do the math, 8x9, we get 72 which gives us our ASCII value of 72.

Alright, great, you printed your first letter in brainfuck!
Now lets print some more.
One thing is that after you print the values, the tables values do not reset.
If we want to print "Hello World!", we need to go from the ASCII Value of H to the ASCII Value of e.

*Upper and Lower Case have different ASCII Values*

So if we look at the values, we need to change 72 to 101.
In other words, we have to add 29.

>+++++++++[<++++++++>-]<.>+++++++[<++++>-]<+.

The first part of the code like previously mentioned prints out the Letter H (Beginning to the first period)
Then, we can see a similar syntax for printing the letter e.
Now, it is just a bit more complicated.
29 is a prime number which means no matter what you multiply with, you cant get to 29.
But what we can do is get the value 28, get out of the loop then add 1 to get 29.

>+++++++[<++++>-]<+.

You can see that being done here.
We add 7 to the second table, then add 4 for every 1 taken away from the second table.
Then once the loop is finished, we add 1 more to get an additional 29.

Now I challenge you to print "Hello World!" using these skills.
Note, if you want to decrease values, use the - sign inside the loop instead of the + sign.

Now there are many different ways you could have done this but, here is one way.
Also, don't get discouraged if you could not get this on your first try!

>+++++++++[<++++++++>-]<.>+++++++[<++++>-]<+.+++++++..+++.>>>++++++++[<++++>-]
<.>>>++++++++++[<+++++++++>-]<---.<<<<.+++.------.--------.>>+.>++++++++++.

With that, you now know the basics of BrainFuck!
If you noticed, this first chapter was not super in depth.
That's because there is alot more to this minamalistic language than just adding, subtracting, and multiplying.
We also did not cover one of the commands. The , sign.
These are all things the will be covered in the next chapter.

===============================================================================
