# Random Spirograph Generator

This Python script generates colorful spirographs using the Turtle module.

## Description

The script utilizes the Turtle module to draw colorful spirographs on the screen. Each spirograph consists of circles drawn with random colors, creating visually appealing patterns.

## Usage

1. Ensure you have Python installed on your system.
2. Clone this repository.
3. Run the script using Python:

    ```bash
    python random_spirograph.py
    ```

4. Watch as the Turtle draws colorful spirographs on the screen.

## Example


[![Random Spirograph](https://github.com/EngAnwarAlkhteeb/Draw-spirograph/blob/main/Spirograph.png)]

## Code

```python
import turtle as t
import random

tim = t.Turtle()
t.colormode(255)
tim.speed('fastest')

def random_color():
    r = random.randint(0, 255)
    g = random.randint(0, 255)
    b = random.randint(0, 255)
    color = (r, g, b)
    return color

def draw_spirograph(size_of_gap):
    for _ in range(int(360 / size_of_gap)):
        tim.color(random_color())
        tim.circle(100)
        tim.setheading(tim.heading() + size_of_gap)

draw_spirograph(4)

s = t.Screen()
s.exitonclick()
