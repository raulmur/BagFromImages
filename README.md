# BagFromImages

ROS package to generate a rosbag from a collection of images. Images are ordered alphabetically. The timestamp for each image is assigned according to the specified frequency. 

The bag will publish the images to topic `/camera/image_raw`.

Tested in ROS Fuerte.

## Installation

In your ROS_PACKAGE_PATH (check your environment variable ROS_PACKAGE_PATH):

    git clone https://github.com/raulmur/BagFromImages.git BagFromImages
    
    cd BagFromImages
    mkdir build
    cd build
    cmake ..
    make

## Usage:

    rosrun BagFromImages BagFromImages PATH_TO_IMAGES IMAGE_EXTENSION FREQUENCY PATH_TO_OUPUT_BAG
  
 - `PATH_TO_IMAGES`: Path to the folder with the images
 - `IMAGE_EXTENSION`: .jpg, .png, etc. write the dot "."
 - `FREQUENCY`: Frames per second.
 - `PATH_TO_OUTPUT_BAG`: Path to save the bag (including the filename e.g. directory/filename.bag)

