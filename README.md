# Particle Filter
This is a simple particle filter for localization of a moving object in a 2D environment written in C++. The program is used with the simulator linked above to localize the position a vehicle given a map and sensor information.

## Introduction
The program takes a map of the vehicle's environment that contains landmarks, a (noisy) GPS estimate of the vehicle's initial location, and (noisy) sensor and control data.

Each time the vehicle receives a measurement of its environment, the program uses the received sensor data to estimate the vehicle's most likely position on the global map.

For a general introduction to particle filters for localization, please refer to the paper ["Particle Filters in Robotics"](http://robots.stanford.edu/papers/thrun.pf-in-robotics-uai02.pdf).

## Dependencies

* cmake >= 3.5
 * All OSes: [click here for installation instructions](https://cmake.org/install/)
* make >= 4.1
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* gcc/g++ >= 5.4
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: same deal as make - [install Xcode command line tools]((https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)
* [uWebSockets](https://github.com/uWebSockets/uWebSockets)
  * Run either `./install-mac.sh` or `./install-ubuntu.sh`. It is recommended to use one of these scripts to install uWS. Perform a manual installation as explained below only if these scripts don't work for you.
  * If you install from source, checkout to commit `e94b6e1`, i.e.
    ```
    git clone https://github.com/uWebSockets/uWebSockets
    cd uWebSockets
    git checkout e94b6e1
    ```
    Some function signatures have changed in v0.14.x. See [this PR](https://github.com/udacity/CarND-MPC-Project/pull/3) for more details.
* A Simulator which you can download from [here](https://github.com/udacity/self-driving-car-sim/releases) in the classroom.

## Basic Build Instructions

1. Clone this repo.
2. Make a build directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./particle_filter`

Once you run the executable, simply run the simulator app and select the particle filter simulation.

## Inputs to the Particle Filter
You can find the inputs to the particle filter in the `data` directory.

#### The Map
`map_data.txt` includes the position of landmarks (in meters) on an arbitrary Cartesian coordinate system. Each row has three columns
1. x position
2. y position
3. landmark id

All other data, such as observations and controls, is returned by the simulator.
