
# Gnss_visualizer
A simple GNSS positioning and display demo

- Use longitude-latitude-altitude(gnss) only, and computing direction information;
- Display positions on the Google Maps;

![2022-06-06-22-21-43](https://raw.githubusercontent.com/zhuhu00/img/master/2022-06-06-22-21-43.png)

## Dependency

- ROS-Meloadic/noetic

- [rviz_satellite](https://github.com/nobleo/rviz_satellite)

## Install

Use the following commands to download and compile the package.

```
cd ~/catkin_ws/src
git clone https://github.com/zhuhu00/gnss_visualizer.git
cd ..
catkin_make
```

## Other notes

1. adjust the topic

    use ```remap``` to change the topic ```/fix``` to your gnss topic,

2. check the ```NavSatFix``` status in ```GNSSCallback```

3. before run your bag(contain gps topic), you need change  ```ori_lat,ori_lon,ori_alt``` in```run.launch``` at `map_load` node.

4. reopen the ```run.launch``` and replay your bag.

## Run the package

1. Run the launch file:
```
roslaunch gnss_visualizer run.launch
```

2. Play existing bag files:
```
rosbag play your-bag.bag --clock
```

## Acknowledgements
The gnss_localizer is implemented based on Autoware-AI;
Thanks rviz_satellite and Autoware-AI;