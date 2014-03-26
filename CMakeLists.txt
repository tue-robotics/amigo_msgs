cmake_minimum_required(VERSION 2.8.3)
project(amigo_msgs)

find_package(catkin REQUIRED COMPONENTS message_generation std_msgs)

add_message_files(
  DIRECTORY msg
  FILES
    AmigoGripperCommand.msg
    cart_pos.msg
    people_detect.msg
    ref_point.msg
    spindle_setpoint.msg
    AmigoGripperMeasurement.msg
    LaserScannerSignal.msg
    pera_status.msg
    RGBLightCommand.msg
)

generate_messages(DEPENDENCIES std_msgs)

catkin_package(CATKIN_DEPENDS message_runtime std_msgs)
