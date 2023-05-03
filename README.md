Download Link: https://assignmentchef.com/product/solved-cs224-assignment-2
<br>
<h1>1             Text Based Adventure</h1>

In this assignment you will be creating a text based dungeon crawler game. You have been given a source file main.cpp which contains the overall structure of the code that you need to write. There is also Assignment2.exe given to you so that you can play the game and judge how it works. Keep in mind that the dungeon needs to be hidden in your final submission. It is shown here for debugging purposes. The functions given here are all that you will need but you can make your own new functions. Details about the assignment are as following:

<ul>

 <li>The dungeon should not be smaller than 8×8 grid.</li>

 <li>P marks the position of player</li>

 <li>X marks the position of Exit</li>

 <li>E represents enemies on map</li>

 <li>F represents food on map</li>

 <li>T represents trap on map</li>

 <li>H represents health on map</li>

 <li>w represents wall on map</li>

</ul>

<h2>1.1           Dungeon Creation</h2>

You will create a dungeon of size <strong>width </strong>x <strong>height</strong>. What this means is that you will need to create a single dimensional dynamic char array of size <strong>width </strong>x <strong>height </strong>as given by the user. This should be done inside the <strong>CreateDungeon </strong>function. You may need to store the starting point and the exit point by using the <strong>Point </strong>structure. The <strong>Traversal </strong>function will then use char array to help with the traversing. Here are the guidelines as to how the dungeon should be created:

<ul>

 <li>You should place walls around the borders of the dungeon</li>

 <li>Traverse the empty spaces one by one and place objects with a 20% probability. If the probability is met then you should generate another random integer. If the value is between 0 and 15, place an enemy. 15 and 30, place health. 30 and 45 place trap. 45 and 60 place food and a wall if it is beyond 60. This will create a dungeon with a reasonable randomness. The numbers can vary if you want to change the difficulty of your dungeon.</li>

 <li>Now traverse the dungeon again and place the player’s starting position at random right next to the left edge of the dungeon. In case you traverse and are unable to place the starting position, place it on the top-left corner by default.</li>

 <li>Place the exit the same way right next to the right edge of the dungeon. Again, if you are unable to place the exit at random, place it at the bottom right corner by default.</li>

</ul>

<h2>1.2           Dungeon Traversal</h2>

Rules for traversing the dungeon are as following:

<ul>

 <li>You will move left, right, up or down every time</li>

 <li>Each step will consume 1 food</li>

 <li>If you encounter a wall or an edge, you will not move and lose 1 food</li>

 <li>If you reach H, you will gain 1 health.</li>

 <li>If you reach T, you will lose 1 health. You will call the <strong>TrapStatements </strong>function at this point which will show one of the three random statements.</li>

 <li>If you reach F, you will gain food for 4 to 8 days. You will call the <strong>FoodStatements </strong>function at this point which will show one of the three random statements.</li>

 <li>If you reach E, you will fight 2 to 4 enemies. You will call the <strong>Combat </strong>function at this point which will play the combat automatically. In combat you will attack the enemy with a 30% probability to score a hit. If you hot the enemy, You will call the <strong>HitStatements </strong>function which will show one of the three random statements. The enemies will attack you as well with a 10% probability each for making a hit. If they hit you, you will call the <strong>GetHitStatements </strong>function which will show one of the three random statements. This will go on till either the enemies die or you die.</li>

 <li>If you reach X, you will win the game</li>

 <li>If you run out of food, you will die</li>

 <li>If you choose ’x’ as input for your turn, you will die</li>

</ul>

<h1>2             Tips</h1>

Here are a few tips that can help you in doing this assignment:

<ul>

 <li>Do not do this assignment in one sitting. It will overwhelm you.</li>

 <li>You will need to do a bit of calculations to make the single dimensional array to behave like a multidimensional array. Keeping the array size small in the beginnnig will help.</li>

 <li>Do not forget to deallocate memory locations when they are no longer in use or if your program is ending.</li>

 <li>Showing the dungeon in every step will have you debug easily.</li>

 <li>Run the given executable many times to see how the program should work. Many of your questions would be answered that way. It is however missing a few checks that you will need to add yourself.</li>

</ul>

<h1>3             Further Enhancements (Not Required)</h1>

If you end up completing the assignment and had fun, you can make it even better by doing the following additions:

<ul>

 <li>You can have enemies with different health pools. Basically, they will be created as player objects.</li>

 <li>You can have more than 3 statements in every function. This will make your adventure story less redundant and more fun.</li>

 <li>You can have your enemies move every turn too (randomly or with your defined AI)</li>

 <li>You can have a series of rooms. As you reach an exit, you move to a new room</li>

 <li>You can add story elements as well for example, you find notes. As you find all the notes a story becomes clearer.</li>

 <li>You can have the game play itself, which would mean that you will define player AI.</li>

</ul>

Let your creativity run wild and you can add much much more to this text based adventure