# Electrical Vehicle Route Planning on Google Map with Reinforcement Learning
More datail please find the README.pdf experiment section

# Library Requirements with Python 3.6.2:
(1) Tensorflow (CPU)
(2) numpy
(3) pandas
(4) haversine
(5) time
(6) random
(7) math
(8) requests
(9) urllib

# How can you get start
(1) enter your start position: name of position or geocode (lat, lng)<br />
(2) enter your destination position: name of position or geocode (lat, lng)<br />
(3) enter the length of each step, higher but less accurate (ex: 1000m takes less time to train compare to 100m)<br />
(4) enter how many episode you want to train<br />

# How does this work
(1) Learning Environment<br />
Make the map like a grid map for the learning agent to navigate on (figure(a)). Strictly speaking, each grid in the grid map is not a rectangle. This phenomenon is caused by the sphere geometry and our restriction on the length of the stride which is demonstrated in figure (b)<br />
![gridmap](https://user-images.githubusercontent.com/25232370/33046405-c89e8556-ce1e-11e7-8f9a-ff50a931ccb5.JPG)<br />
(2) Interact with Google map API /><br />

![map1](https://user-images.githubusercontent.com/25232370/33046910-0d9b5b82-ce21-11e7-8974-4f9c0aa63e22.JPG)<br />


(3) Energy Computation<br /><br />
The following graph shows how to compute the energy for a vehicle to travel uphill (can also be applied on a flat road)<br />
![car2](https://user-images.githubusercontent.com/25232370/33046700-1b515886-ce20-11e7-9b57-d9e735ca0167.JPG)<br />
But noticed that we only compute the elevation between the two position shown in the following graph. To increase the accuracy, you should minimize the distance between these two position (this will increase the computation time).<br />
![car1](https://user-images.githubusercontent.com/25232370/33046721-338fe5b6-ce20-11e7-8c17-3663462ac24f.JPG)<br />


# Result
![result](https://user-images.githubusercontent.com/25232370/33046240-25c5ac2e-ce1e-11e7-9156-faf109c42bbe.JPG)
