find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)
find_package(Glew REQUIRED)

include_directories( ${GLEW_INCLUDE_DIRS} )

ADD_EXECUTABLE(SimpleSIFT SimpleSIFT.cpp)
TARGET_LINK_LIBRARIES(SimpleSIFT siftgpu)

ADD_EXECUTABLE(TestWinGlut TestWinGlut.cpp BasicTestWin.cpp )
TARGET_LINK_LIBRARIES(TestWinGlut siftgpu)

set(CMAKE_VERBOSE_MAKEFILE ON)
