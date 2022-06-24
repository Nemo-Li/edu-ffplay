cmake_minimum_required(VERSION 3.15)
project(edu_ffplay)

set(CMAKE_CXX_STANDARD 14)
# 这个SDL开发包的路径，可以通过brew info sdl2查出来
set(SDL_DIR /usr/local/Cellar/sdl2/2.0.10)
# 添加SDL头文件搜索路径
include_directories(${SDL_DIR}/include/SDL2)
include_directories(${CMAKE_SOURCE_DIR}/include/)
include_directories(/Users/nemoli/FFmpeg/FFmpeg-n4.4.1/mac/include/)
include_directories(/Users/nemoli/FFmpeg/FFmpeg-n4.4.1/)

# 增加SDL链接库目录
link_directories(${SDL_DIR}/lib/)
link_directories(/Users/nemoli/FFmpeg/FFmpeg-n4.4.1/mac/lib/)

add_executable(edu_ffplay ffplay.c cmdutils.c)

target_link_libraries(edu_ffplay SDL2 avcodec avdevice avformat avutil swscale swresample avfilter postproc)