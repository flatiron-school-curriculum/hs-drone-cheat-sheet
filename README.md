## NODE-AR-DRONE
More documentation here: [http://github.com/felixge/node-ar-drone](github.com/felixge/node-ar-drone)

### BASIC MOVES

```javascript
client.takeoff()
```

```javascript
client.land()
```

`client.up(speed)` / `client.down(speed)` <br>
Makes the drone gain or reduce altitude. Speed can be a value from 0 to 1.

`client.clockwise(speed)` / `client.counterClockwise(speed)` <br>
Causes the drone to spin. Speed can be a value from 0 to 1.

`client.front(speed)` / `client.back(speed)` <br>
Controls the pitch, which is the vertical direction the drone's nose is pointing. Speed can be a value from 0 to 1.

`client.left(speed)` / `client.right(speed)` <br>
Controls the roll, which makes the drone tilt left or right. Speed is any value from 0 to 1.

```javascript
client.stop()
```
Sets all drone movement commands to 0, making it effectively hover in place.

### GETTING FANCY

```javascript
client.animate(animation, duration)
```
Example: 
```javascript
client.animate('flipLeft', 1000);
```
This performs a pre-programmed flight sequence for a given duration (in ms). Try these in place of `'flipLeft'` above:
```
['phiM30Deg', 'phi30Deg', 'thetaM30Deg', 'theta30Deg', 'theta20degYaw200deg',
'theta20degYawM200deg', 'turnaround', 'turnaroundGodown', 'yawShake',
'yawDance', 'phiDance', 'thetaDance', 'vzDance', 'wave', 'phiThetaMixed',
'doublePhiThetaMixed', 'flipAhead', 'flipBehind', 'flipLeft', 'flipRight']
```
Please note that the drone will need a good amount of altitude and headroom to perform a flip. So be careful!

For more information about Flatiron School, [visit our site](precollege.flatironschool.com)!
