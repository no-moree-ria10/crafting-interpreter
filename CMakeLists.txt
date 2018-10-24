cmake_minimum_required(VERSION 2.8)


set(CMAKE_C_FLAGS " -Wall")
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
# add_definitions("-DMACRO1=bar") # プリプロセッサ定義を追加

file(GLOB_RECURSE SRC_FILES "./src/*.c") # 再帰的に.cppファイルを検索する
add_executable(clox ${SRC_FILES})
# target_link_libraries(  pthread ) # リンクするライブラリを追加

