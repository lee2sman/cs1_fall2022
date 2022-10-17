---
layout: page
title: Midterm-A
permalink: /midterm-a
---

### Short Questions

**Give short responses to the following questions:**

1 What is a boolean?

2 When do you use loops?

3 When do you use rectMode?

4 In Processing, how many shades of grey are there?

5 what are 3 ways to say: set x to 1 more than its current value?

6 What is the difference between a local and global variable?

7 What is the difference between a single = sign versus == ?

8 what is casting (also known as converting)?

9 What's an example of using casting?

10 What are the pushMatrix() and popMatrix() used for?

### Short code

11 I want a random whole number between 1 and 10. My first line of code below is wrong. What is wrong with this code? Describe in words.

```
int num = random(1,10);
print(num);
```

12 What is wrong in the following code and how would you fix it?

```
int age = 20.02;

if (age = 20){
  println("You are 20!");
}
```

13 Based on the function definition below, write a single line of code to call the function using the values 3, 10 and 200.

```
void sum(int a, int b, int c){
    int total = a + b + c;
    println(total);
}
```

14 Write the simplest line(s) of code you can write to draw a plus sign on screen: Write the code to create a line running from the top center to the bottom center, and another line from the center left running across to the center right. The code needs to be able to work on any width/height screen.

15 Write a for-loop that prints out 1 to 20 but skips 13 (it's unlucky!).

### CODE

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
Your first year friend doesn't know what major to pick but they've narrowed down their choices.

```
String[] majors = {"Math and CompSci", "Anthro", 
"Gender Studies", "VA", "Linguistics", "New Media", "Psychology"};

println("Majors: ");

for (int i = 0; i < majors.length; i++){
  println(majors[i]); 
}
```

The above starter code prints the list of majors they are considering. Now add lines of code to select a major and a minor for them at random from their list and print it to the console. (Note: this is probably not a recommended way to pick what you study.)

18 
You've been hired to create a demo of a special clock, a new product for those with a minimalist lifestyle. It's a sleep timer clock and it has no settings. When you're ready to go to sleep you simply hit play and in 7 hours the alarm goes off. Using millis(), create a timer that will print out "alarm" in 7 hours.

