cmake_minimum_required(VERSION 2.8)
PROJECT(akaze_demo)

FIND_PACKAGE(OpenCV REQUIRED)

SET(SRC
    main.cpp akaze/akaze_features.cpp akaze/akaze_fed.cpp akaze/akaze_nldiffusion_functions.cpp akaze/akaze_utils.cpp akaze/AKAZE.cpp
)

ADD_EXECUTABLE(${PROJECT_NAME} ${SRC})
TARGET_LINK_LIBRARIES(${PROJECT_NAME} ${OpenCV_LIBS})
