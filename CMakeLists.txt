PROJECT(simhash)

CMAKE_MINIMUM_REQUIRED(VERSION 2.6)

ADD_DEFINITIONS(-O3 -Wall -g)
IF(APPLE) 
    ADD_DEFINITIONS(-std=c++11)
endif()

ADD_SUBDIRECTORY(src)
ADD_SUBDIRECTORY(test)

ENABLE_TESTING()
ADD_TEST(NAME test.run COMMAND test.run)
