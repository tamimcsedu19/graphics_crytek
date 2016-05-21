cmake_minimum_required(VERSION 3.2)
project(projection)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(SOURCE_FILES
        main.cpp
        Shader.h
        Model.h Camera.h Mesh.h)



add_executable(projection ${SOURCE_FILES} Model.h Camera.h Mesh.h)

target_link_libraries(projection GL GLU glfw3 X11 Xxf86vm Xrandr pthread Xi dl GLEW Xinerama Xcursor assimp SOIL)

include_directories( /home/tamim/Downloads/glm-0.9.7.3 )
