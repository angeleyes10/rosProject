cmake_minimum_required(VERSION 2.8.3)
project(tester)


find_package(catkin REQUIRED genmsg std_msgs message_generation kovan turtlesim roscpp geometry_msgs)
generate_messages(DEPENDENCIES std_msgs)
catkin_package(DEPENDS message_runtime)

include_directories(include ${catkin_INCLUDE_DIRS})

add_executable(template src/template.cpp)
target_link_libraries(template ${catkin_LIBRARIES})
