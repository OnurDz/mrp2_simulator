cmake_minimum_required(VERSION 2.8.3)
project(mrp2_gazebo)

find_package(catkin REQUIRED)

catkin_package()

foreach(dir launch models worlds config)
    install(DIRECTORY ${dir}/
        DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/${dir})
endforeach(dir)
