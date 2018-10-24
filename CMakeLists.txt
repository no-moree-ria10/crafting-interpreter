cmake_minimum_required(VERSION 2.8)


set(CMAKE_CXX_FLAGS " -Wall -g3")
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
# add_definitions("-DMACRO1=bar") # プリプロセッサ定義を追加

include_directories(./src)
file(GLOB_RECURSE SRC_FILES "./src/*.cpp") # 再帰的に.cppファイルを検索する
#file(GLOB_RECURSE HEADER_FILES "./src/*.h") # 再帰的に.cppファイルを検索する
add_executable( clox ${SRC_FILES})
# target_link_libraries(  pthread ) # リンクするライブラリを追加

