# Drivetrain speed

## Identify:
We need a fast drivetrain, our current one is ~76in/s and it is ok, but it is just a little bit too fast (in my option; one of my team mates would beg to differ) I think the ideal is 70in/s

Goal: speed of 70in/s

Ideally we would have these things:
- Only gear down 
  - The all the motor cartridges are gearing down, if you were to gear up you would be gearing down then back up again, reducing efficiency.
- Small wheels
  - Smaller wheels mean more room for other things.
- Good spacing

## Brainstorm:

There are 3 motor speeds we can use, 100RPM, 200RPM, and 600RPM 
None are great on there own so we need to have a gear ratio.

### Gear ratios

| Teeth | 12  | 24  | 36  | 48  | 60  | 72  |
| ----- | --- | --- | --- | --- | --- | --- |
| 12    | 1:1 | 1:2 | 1:3 | 1:4 | 1:5 | 1:6 |
| 24    | 2:1 | 1:1 | 2:3 | 1:2 | 2:5 | 1:3 |
| 36    | 3:1 | 3:2 | 1:1 | 3:4 | 3:5 | 1:2 |
| 48    | 4:1 | 2:1 | 4:3 | 1:1 | 4:5 | 2:3 |
| 60    | 5:1 | 5:2 | 5:3 | 5:4 | 1:1 | 5:6 |
| 72    | 6:1 | 3:1 | 2:1 | 3:2 | 6:5 | 1:1 |

Possible RPM with gear ratios:
Geared down:

| RPM | 1:1 | 5:6   | 4:5 | 3:4 | 2:3   | 3:5 | 1:2 | 2:5 | 1:3  | 1:4 | 1:5 | 1:6  |
| --- | --- | ----- | --- | --- | ----- | --- | --- | --- | ---- | --- | --- | ---- |
| 100 | 100 | 83.3  | 80  | 75  | 66.7  | 60  | 50  | 40  | 33.3 | 25  | 20  | 16.7 |
| 200 | 200 | 166.7 | 160 | 150 | 133.3 | 120 | 100 | 80  | 66.7 | 50  | 40  | 33.3 |
| 600 | 600 | 500   | 480 | 450 | 400   | 360 | 300 | 240 | 200  | 150 | 120 | 100  |

Geared up:

| RPM | 6:1  | 5:1  | 4:1  | 3:1  | 5:2  | 2:1  | 5:3   | 3:2 | 4:3   | 5:4 | 6:5 | 1:1 |
| --- | ---- | ---- | ---- | ---- | ---- | ---- | ----- | --- | ----- | --- | --- | --- |
| 100 | 600  | 500  | 400  | 300  | 250  | 200  | 166.7 | 150 | 133.3 | 125 | 120 | 100 |
| 200 | 1200 | 1000 | 800  | 600  | 500  | 400  | 333.3 | 300 | 266.7 | 250 | 240 | 200 |
| 600 | 3600 | 3000 | 2400 | 1800 | 1500 | 1200 | 1000  | 900 | 800   | 750 | 720 | 600 |

All possible speeds (in/s):

| Wheel Ø | 16.7 | 20  | 25  | 33.3 | 40  | 50   | 60   | 66.7 | 75   | 80   | 83.3 | 100  | 120  | 125  | 133.3 | 150  | 160  | 166.7 | 200  | 240  | 250  | 266.7 | 300  | 333.3                                    | 360                                      | 400                                      | 450                                      | 480                                      | 500                                      | 600   | 720   | 750   | 800   | 900   | 1000  | 1200  | 1500  | 1800  | 2400  | 3000  | 3600  |
| ------- | ---- | --- | --- | ---- | --- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ----- | ---- | ---- | ----- | ---- | ---- | ---- | ----- | ---- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| 4"      | 3.5  | 4.2 | 5.2 | 7.0  | 8.4 | 10.5 | 12.6 | 14.0 | 15.7 | 16.8 | 17.4 | 20.9 | 25.1 | 26.2 | 27.9  | 31.4 | 33.5 | 34.9  | 41.9 | 50.3 | 52.3 | 55.9  | 62.8 | <span style="color: #4caf50">69.8</span> | <span style="color: #fdd835">75.4</span> | 83.8                                     | 94.2                                     | 100.5                                    | 104.7                                    | 125.7 | 150.8 | 157.1 | 167.6 | 188.5 | 209.4 | 251.3 | 314.2 | 377.0 | 502.7 | 628.3 | 754.0 |
| 3.25"   | 2.8  | 3.4 | 4.3 | 5.7  | 6.8 | 8.5  | 10.2 | 11.3 | 12.8 | 13.6 | 14.2 | 17.0 | 20.4 | 21.3 | 22.6  | 25.5 | 27.2 | 28.3  | 34.0 | 40.8 | 42.5 | 45.3  | 51.0 | 56.6                                     | 61.2                                     | <span style="color: #4caf50">68.0</span> | <span style="color: #f9a825">76.5        | 81.6                                     | 85.0                                     | 102.0 | 122.3 | 127.5 | 136.0 | 153.0 | 170.0 | 204.0 | 255.0 | 306.0 | 408.0 | 510.0 | 612.0 |
| 2.75"   | 2.4  | 2.9 | 3.6 | 4.8  | 5.8 | 7.2  | 8.6  | 9.6  | 10.8 | 11.5 | 12.0 | 14.4 | 17.3 | 18.0 | 19.2  | 21.6 | 23.0 | 24.0  | 28.8 | 34.6 | 36.0 | 38.4  | 43.2 | 48.0                                     | 51.8                                     | 57.6                                     | <span style="color: #f9a825">64.8</span> | <span style="color: #4caf50">69.1</span> | <span style="color: #4caf50">72.0</span> | 86.4  | 103.7 | 108.0 | 115.2 | 129.6 | 144.0 | 172.8 | 216.0 | 259.2 | 345.6 | 432.0 | 518.4 |

With the goal of ~70in/s there are a few candidates

###### 4" wheels:

| Speed    | Wheel RPM | Motor RPM | Gear ratio | Gear1 | Gear2 |
| -------- | --------- | --------- | ---------- | ----- | ----- |
| 69.8in/s | 333.3     | 200       | 5:3 (up)   | 60T   | 36T   |
| 75.4in/s | 360       | 600       | 3:5 (down) | 36T   | 60T   |

###### 3.25" wheels:
| Speed    | Wheel RPM | Motor RPM | Gear ratio | Gear1 | Gear2 |
| -------- | --------- | --------- | ---------- | ----- | ----- |
| 68.0in/s | 400       | 600       | 2:3 (down) | 24T   | 36T   |
| Alt1     | 400       | 600       | 2:3 (down) | 48T   | 72T   |
| Alt2     | 400       | 200       | 2:1 (up)   | Many  | Many  |
| Alt3     | 400       | 100       | 4:1 (up)   | 48T   | 12T   |
| 76.5in/s | 450       | 600       | 3:4 (down) | 36T   | 48T   |

###### 2.75" wheels:

| Speed    | Wheel RPM | Motor RPM | Gear ratio | Gear1 | Gear2 |
| -------- | --------- | --------- | ---------- | ----- | ----- |
| 64.8in/s | 450       | 600       | 3:4 (down) | 36T   | 48T   |
| 69.1in/s | 480       | 600       | 4:5 (down) | 48T   | 60T   |
| 72.0in/s | 500       | 600       | 5:6 (down) | 60T   | 72T   |
| Alt1     | 500       | 200       | 5:2 (up)   | 60T   | 24T   |
| Alt2     | 500       | 100       | 5:1 (up)   | 60T   | 12T   |

## Select:

Based on the ideal goals (gearing up, small wheels) these are the best options:

| Wheel size | Speed        | Wheel RPM | Motor RPM | Gear ratio     | Gear1   | Gear2   |
| ---------- | ------------ | --------- | --------- | -------------- | ------- | ------- |
| 2.75"      | 69.1in/s     | 480       | 600       | 4:5 (down)     | 48T     | 60T     |
| ~~2.75"~~  | ~~72.0in/s~~ | ~~500~~   | ~~600~~   | ~~5:6 (down)~~ | ~~60T~~ | ~~72T~~ |
| 3.25"      | ~~68.0in/s~~ | ~~400~~   | ~~600~~   | ~~2:3 (down)~~ | ~~24T~~ | ~~36T~~ |
| 3.25"      | Alt1         | 400       | 600       | 2:3 (down)     | 48T     | 72T     |
| 3.25       | 64.8in/s     | 450       | 600       | 3:4 (down)     | 36T     | 48T     |
Now to check spacing:

2.75" 480rpm:

![480 RPM 2.75in wheel](/images/time-based/04-wasatch-future/new-drivetrain/480rpm2.75in.jpeg)
or
![480 RPM 2.75in wheel long](/images/time-based/04-wasatch-future/new-drivetrain/480rpm2.75in-long.png)
[Image credit](https://www.vexforum.com/t/catalogue-of-drive-gearings/109498)

~~2.75" 500rpm:~~
The gearing is so ugly that i cant find an image, and I'm too lazy to make one.
Also the 72T gears are bigger than the 2.75" wheels so it would be driving on the gears

3.25" 400rpm:

48T:72T
![400RPM 3.25in wheel](/images/time-based/04-wasatch-future/new-drivetrain/400rpm3.25in.jpeg)[Image credit](https://www.vexforum.com/t/catalogue-of-drive-gearings/109498)

24T:36T
The gears are too small, the wheels would have to clip into each other

3.25" 450rpm:
![400RPM 3.25in wheel](/images/time-based/04-wasatch-future/new-drivetrain/450rpm3.25in.jpeg)
[Image credit](https://www.vexforum.com/t/catalogue-of-drive-gearings/109498)

#### Final options:
| Wheel size | Speed    | Wheel RPM | Motor RPM | Gear ratio | Gear1 | Gear2 |
| ---------- | -------- | --------- | --------- | ---------- | ----- | ----- |
| 2.75"      | 69.1in/s | 480       | 600       | 4:5 (down) | 48T   | 60T   |
| 3.25"      | 68.0in/s | 400       | 600       | 2:3 (down) | 48T   | 72T   |
| 3.25       | 64.8in/s | 450       | 600       | 3:4 (down) | 36T   | 48T   |

I would like the smaller wheels and i see more potential in the 2.75" option, and it is closer to the ideal 70in/s.

The chosen wheel/rpm is: **2.75" 480rpm**

But there is a large problem
It would be really hard to fit in 5 un wide (more in [Size](05-size.md)) and if it is wider than 5 un then screws aren't long enough to bridge the gap for [Screw Joints](06-misc-and-build-practices.md#Screw%20Joints).

The ***real*** chosen speed is:
**3.25" 450rpm**
 

	Daren 12/08/25



	Daren 12/08/25-12/14/25
