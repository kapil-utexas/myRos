# myRos
This project is part of the Texas Guadalupe team's effort to build a communication back-end for the HyperLoop Pod. It is build on top of a ROS node network.

The repo contains ros packages for inter machine communication using just the ros-comm mechanism of simply publishing and subscribing to a JSON topic. 

It further extends the capability of these topic based communication by using a ROS library calledrosbridge which provides another abstraction on top of the ROS node to be accesible over the internet. It accomplish that via websockets which are just an abstraction of the IP web-sockets, where in the low-level stuff of binding to ports etc. is taken care by the library.

The repo also contains an example javascript server client package which can be used to collect data from different nodes(slaves) to a master node which in our case can be the remote machine used for visualizing that data. An interesting idea will be to have a local master which can provide a centralized aggregation scheme and then send the data over to the remote machine, running a JavaScript back end to publish this data.
