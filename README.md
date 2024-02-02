##Snake Game using Turtle in Python ✅ Source Code 👇👇

import required modules
import turtle import time import random

delay = 0.1 score = 0 high_score = 0

##Creating a window screen
wn = turtle.Screen() wn.title("Snake Game") wn.bgcolor("blue")

the width and height can be put as user's choice
wn.setup(width=600, height=600) wn.tracer(0)

##head of the snake
head = turtle.Turtle() head.shape("square") head.color("white") head.penup() head.goto(0, 0) head.direction = "Stop"

##food in the game
food = turtle.Turtle() colors = random.choice(['red', 'green', 'black']) shapes = random.choice(['square', 'triangle', 'circle']) food.speed(0) food.shape(shapes) food.color(colors) food.penup() food.goto(0, 100)

pen = turtle.Turtle() pen.speed(0) pen.shape("square") pen.color("white") pen.penup() pen.hideturtle() pen.goto(0, 250) pen.write("Score : 0  High Score : 0", align="center",font=("candara", 24, "bold"))

##assigning key directions
def group(): if head.direction != "down": head.direction = "up"

def godown(): if head.direction != "up": head.direction = "down"

def goleft(): if head.direction != "right": head.direction = "left"

def goright(): if head.direction != "left": head.direction = "right"

def move(): if head.direction == "up": y = head.ycor() head.sety(y+20) 
            if head.direction == "down": y = head.ycor() head.sety(y-20) 
            if head.direction == "left": x = head.xcor() head.setx(x-20) 
            if head.direction == "right": x = head.xcor() head.setx(x+20)

wn.listen() wn.onkeypress(group, "w") wn.onkeypress(godown, "s") wn.onkeypress(goleft, "a") wn.onkeypress(goright, "d")

segments = []

/** This code is a simple implementation of the classic snake game using the turtle graphics library in Python. The snake is represented by a series of segments, 
with the head being a separate turtle. The snake moves in the direction of the arrow keys pressed by the player. The food is another turtle that the snake tries to eat.
When the snake eats the food, a new segment is added to the end of the snake. The game ends when the snake collides with the boundary of the screen or with its own body. 
The score increases as the snake eats more food.

Here's a breakdown of the code:

The wn variable is an instance of the turtle.Screen class. This is the main window where the game will be displayed.

The head variable is an instance of the turtle.Turtle class. This represents the head of the snake.

The food variable is another instance of the turtle.Turtle class. This represents the food that the snake tries to eat.

The segments list is used to store the segments of the snake.

The colors and shapes variables are used to randomly choose the color and shape of the snake and food.

The group function is used to move the snake in the direction of the arrow keys pressed by the player.

The godown, goleft, and goright functions are used to change the direction of the snake based on the arrow keys pressed by the player.

The move function is used to move the snake one step in its current direction.

The while True: loop is the main game loop. It updates the screen, checks for collisions, and moves the snake.

The if head.xcor() > 290 or head.xcor() < -290 or head.ycor() > 290 or head.ycor() < -290: 
condition checks if the snake has collided with the boundary of the screen. If it has, the game is reset.

The if head.distance(food) < 20: 
condition checks if the snake has eaten the food. If it has, a new segment is added to the end of the snake, and the score increases.

The for index in range(len(segments)-1, 0, -1): 
loop is used to move the segments of the snake to the position of the segment in front of them.

The if len(segments) > 0: 
condition checks if there are any segments in the snake. If there are, the head of the snake is moved to the position of the first segment.

The time.sleep(delay) line is used to control the speed of the game. The delay is decreased each time the snake eats food, making the game progressively faster.

The wn.mainloop() line is used to start the main game loop.

The explain this code function is used to explain the code to the player.

The pen.clear() and pen.write() lines are used to clear the score display and write the updated score on the screen.

The time.sleep(1) line is used to pause the game for 1 second when the snake collides with the boundary or its own body.

The segment.goto(1000, 1000) line is used to move the segments of the snake off the screen when the game is reset.

The segment.goto(x, y) lines are used to move the segments of the snake to the position of the segment in front of them.

The if segment.distance(head) < 20: condition checks if the snake has collided with its own body. If it has, the game is reset.

The colors = random.choice(['red', 'blue', 'green']) and shapes = random.choice(['square', 'circle']) lines are used to randomly choose the color and shape of the snake and food when the game is reset.

The segment.goto(1000, 1000) line is used to move the segment off the screen
