# Chocolate sticks!

You recently received a bag of chocolate sticks for Halloween. To prevent you from compulsively eating all the chocolate sticks in one go, your dietician devises the following fun game.

In each move, you choose one of the sticks from your bag. Then, you either eat it, or break it into some number of equally-sized parts and save the pieces for later. The lengths of all sticks must always be integers, so breaking a stick into _d_ parts is possible only if _d_ is a divisor of the stick's length, and _d_ is greater than 1.

Note that this means that a stick of length 1 cannot be broken anymore, and can only be eaten.

For example, a chocolate stick of length 4 will be dealt with as shown below.

![image](https://s3.amazonaws.com/hr-assets/0/1512379963-3180b66375-choc.png)

Given the chocolate sticks you received, determine the length of the longest sequence of moves you can perform.

Complete the function  `longestSequence`  which takes in a python list of integers, denoting the lengths of the chocolate sticks, as input. Return the maximum number of moves you can perform to consume the chocolate sticks according the game. Your output should be a single integer which is the number of moves in the longest sequence.

In the example above, the output would be 7. If there two sticks of length 4, the answer would be 14.