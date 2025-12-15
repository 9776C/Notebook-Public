# Identify:
A PTO is a "power take off" where you have some sort of mechanism/gearshift that switches a motor between two (or more applications)
#### Why do we need a PTO?
In our last bot we were very fast, to achieve that (without overheating) we needed a 6 motor drive, this was ***very*** limiting on the other mechanisms on our bot because we only had 2 more motors we could use. 

A PTO can help solve this problem; we don't always need the torque of all 6 motors, so when we don't need them on the drive train we can switch 2 motor off and use them in other mechanisms. This would be especially useful for mechanism's that could use energy stored in elastics/similar (ex. like theorized in [Linear Scoring](../new-scoring/02-linear-scoring.md))

Timeline of PTO:
Use stored energy is used --> PTO switches 2 motors off the drive train --> those 2 motors wind up the stored energy --> the energy is used --> repeat.

Even if we aren't going to store energy is is still very viable

# Brainstorm:

How would we actuality accomplish this?
There are 2 main ways of implementing a PTO:

Vertically:
This method rotates the motor gear around a pivot point to mesh with a top or bottom gear:
![Down](/images/time-based/04-wasatch-future/new-drivetrain/vertical-pto-down.png)
![Up](/images/time-based/04-wasatch-future/new-drivetrain/vertical-pto-up.png)
[Image Credit](https://www.youtube.com/watch?v=3tkbR7OZv7A)


Horizontally:
This method slides the motor gear along a shaft and slides to the teeth of one gear or another, I can't find a very good example of this method for a PTO but this one is a transmission and the concept is the same:

![Up](/images/time-based/04-wasatch-future/new-drivetrain/horizontal-pto.png)
Image Credit: I can't' find where I got this from...

This particular one uses two "fingers" to move the gears side to side and engage different gears.

### Pros/Cons:

#### Vertical:
##### Pros:
- Very fast switching 
- Relatively simple
##### Cons:
- If enough pressure isn't applied it can skip teeth under high load
- Requires a lot of vertical space

#### Horizontal:
##### Pros:
- Loses no torque
- Very reliable when tuned
##### Cons:
- Not super fast switching
- A bit more complicated
- More friction

# Select:
I am going to select the horizontal method because the chance of running out of air is not worth it to me, because if we ran out of air for the vertical method, we wouldn't be able to use it in ether application (drivetrain/other). 