---
layout: page
title: Midterm-B
permalink: /midterm-b
---

### Short Questions

**Give short responses to the following questions:**

1 How do setup() and draw() differ?

2 When do you use an IF statement?

3 Why are functions used in coding?

4 Why are comments used in code?

5 What is the difference between a local and global variable?

6 What are datatypes? Name 3 examples.

7 What is translate for?

8 How do you convert from a float to an integer?

9 If you created a variable for a coinflip, what kind of variable type would you need for the result?

10 If you try to draw a default rectangle and an ellipse both at 100,100 with the same width and height, they do not overlap completely. Why not?

### Short answer

11 **You wrote a line of code to pick a random number from 1 to 100:**

```int c=random(1, 100);```

**Will this code run correctly? If not, rewrite and fix the error.**

12 As a result of this code (or if needed, your fixed code), could c turn out to be:


- 1?

- 30?

- 80?

- 100?

13 Write a for-loop that prints out the numbers 100 to one million, incrementing by 100.

14 Describe clearly in words what this program does.

```
void mousePressed(){
  if ((mouseX > width/2) && (mouseY < height/2)){
    background(0);
  } else {
    background(255);
  }
}
```

15 Write the simplest line(s) of code you can write to draw two crossed lines on screen: Write code to create a line running from the top left to the bottom right corner, and another line from the top right running to the bottom left corner. The code needs to be able to work on any width/height screen.

# CODE

*Note: This question is to help you see a (simple) example of how you could add buttons to change state for your Tamagotchi project. It is overly simplified. If you use buttons, they should be clearly marked or have images on them.*

16 I have a very simple *pet rock* Tamagotchi-like creature. It is either "awake" or "sleeping." (To be honest, my pet rock looks the same either way.)

Here's some starter code:

```
String currentState = "sleeping";

void setup(){
  size(400,400);
  fill(120);
}
```

I have the pet rock on screen and a button in the top left corner of my screen. 

```
void draw(){
  //pet rock
  fill(120);
  ellipse(width/2,height/2,120,100);
  //button
  fill(255);
  rect(0,0,50,50);
  //button text
  fill(0);
  text("wake",10,10);
  
  //check for state
  if (currentState == "sleeping"){
    sleep();
  } else {
    awake();
  }
}

void sleep(){
  println("shhhhhhhhhh!");
}
void awake(){
  println("i'm awake!");
}
```

When my program starts, the rock is sleeping. When I click inside the button, I want to print out that the button was pressed. Add the code that should appear inside the void keyPressed(). I also want to change the rock's state to "awake".

```
void mousePressed(){
  //code to check if we clicked in the button here
  //if so, print out "button pressed"
  //and also change the state so that the awake() function will run instead of sleep().
}
```

17
You have been hired by Goldenvox, the company that organizes Goatchella, to help them select their headlining duo as they develop the lineup for next year's Goatchella Festival. "Our audience has come to expect viral mashups: Kanye with Daft Punk, Childish Gambino with Ariana Grande, and Rage Against The Machine with Frank Ocean. We need even more random mashups this year or everyone will start going to underground college festivals like Culture Shock instead. Can you build us software to select our big headliner collab? We'll give you our list of bands, we need you to write software to select two of them as our headliners, and then just in case those two won't agree to perform together we need you to make one more selection of two performers. Oh yeah, and we have less than an hour. We've narrowed down our list of possible performers to Cardi B, Harry Styles, Bad Bunny, Charli XCX, 21 Savage, Lil Nas X, Steve Lacy, Dua Lipa, Ed Sheeran, Marshmellow and BLACKPINK. Thanks."

Note: Your program's output should look something like this:
This year's headliners: Cardi B with Marshmellow. Backup headliners: Lil Nas X with BLACKPINK.

For EXTRA CREDIT: Now add additional code so that the program does not select the same name twice. We don't want to see 'Lil Nas X' x 'Lil Nas X' for example.

Starter code:

```
String[] performers = { "Cardi B", "Harry Styles", "Bad Bunny", "Charli XCX", "21 Savage", "Lil Nas X", "Steve Lacy", "Dua Lipa", "Ed Sheeran", "Marshmellow", "BLACKPINK" };
```

18
In a surprise move of capitalist innovation Dubweiser Beverages has announced their new Non-Alcoholic Kombucha Brew called KomBrewcha will premiere this winter. They've decided they want to make a poster campaign as an homage to the tune 99 bottles of beer on the wall. They've hired a robotic jingle company to sing the ad jingle; now they just need you to write the words. Please write code to print out the lyrics beginning at "99 bottles of KomBrewcha on the wall, 99 bottles of KomBrewcha, take one down, pass it around, 98 bottles of Kombrewcha on the wall." etc, finally ending at zero bottles of KomBrewcha. 

