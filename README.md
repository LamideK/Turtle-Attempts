# Turtle-Attempts
Tried out turtle, now it has circle 

    import turtle
    import math
    
# draws a square
    bob = turtle.Turtle()
    x = turtle.Turtle()
    for i in range(4):
        bob.lt(90)
        bob.fd(100)
    #print(bob)

# draws a polygon (my way)
    def polygon(sides):
        t = turtle.Turtle()
        angles = math.ceil(360/sides)
        for i in range(sides):
            t.lt(angles)
            t.fd(angles)


## This entire polyline - circle methods is for circle
#draws n sided polygon (according to material)
    def polyline (t, n, length, angle):
        t = turtle.Turtle()
        for i in range(n):
            t.fd(length)
            t.lt(angle)
# use polyline to rewrite polygon, and make an arc for a circle
    def another_polygon(t,n,length):
        angle = 360.0/n
        polyline(t,n,length,angle)

    def arc(t,r,angle):
        arc_length = 2 * math.pi * r * angle / 360
        n = int(arc_length / 3) + 1
        step_length = arc_length / n
        step_angle = float(angle) / n
        polyline(t, n, step_length, step_angle)

# finally, use arc to draw a circle
    def circle(t,r):
        arc(t,r,360)

# function to call to draw more than one at a time and space them out
    def move(t,length):
        t.pu()
        t.fd(length)
        t.pd()

# drawing a triangle
#def triangle(sides):


turtle.Turtle()
