cmake_minimum_required(VERSION 2.8.3)
project(riptide_msgs)

find_package(catkin REQUIRED
    COMPONENTS
    geometry_msgs
    message_generation
    std_msgs
)

add_message_files(
    FILES
    Depth.msg
    Thrust.msg
    ThrustStamped.msg
    OdomWithAccel.msg
    Pwm.msg
    PwmStamped.msg
    Esc.msg
    Thrusters.msg
    Bat.msg
    BatStamped.msg
)

generate_messages(DEPENDENCIES std_msgs geometry_msgs)

catkin_package(CATKIN_DEPENDS message_runtime)

include_directories(${catkin_INCLUDE_DIRS})
