# Балтаев Тимур ИУ8-22
## Задание 1
```sh
$ git clone https://github.com/tp-labs/lab03
$ cd formatter_lib
```
```sh
$ cat > CMakeLists.txt <<EOF
> cmake_minimum_required(VERSION 3.4)
> project(formatter)
> EOF
```
```sh
$ cat >> CMakeLists.txt <<EOF
> set(CMAKE_CXX_STANDARD 11)
> set(CMAKE_CXX_STANDARD_REQUIRED ON)
> set(CMAKE_CURRENT_SOURCE_DIR /home/timur/BaltaevTimur/workspace/lab03_hw/lab03/formatter_lib/)
> EOF
```
```sh
$ cat >> CMakeLists.txt <<EOF
> add_library(formatter STATIC \${CMAKE_CURRENT_SOURCE_DIR}/formatter.cpp)
> EOF
```
```sh
$ cat >> CMakeLists.txt <<EOF
> include_directories(\${CMAKE_CURRENT_SOURSE_DIR}/formatter.h)
> EOF
```
```sh
$ cmake -H. -B_build
```
```sh
-- The C compiler identification is GNU 10.3.1
-- The CXX compiler identification is GNU 10.3.1
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Check for working C compiler: /usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Check for working CXX compiler: /usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Configuring done
-- Generating done
-- Build files have been written to: /home/timur/BaltaevTimur/workspace/lab03_hw/lab03/formatter_lib/_build
```
$ cmake --build _build
```
```sh
[ 50%] Building CXX object CMakeFiles/formatter.dir/formatter.cpp.o
[100%] Linking CXX static library libformatter.a
[100%] Built target formatter
```
### CMakeLists.txt
```sh
cmake_minimum_required(VERSION 3.4)
project(formatter)
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CURRENT_SOURCE_DIR /home/timur/BaltaevTimur/workspace/lab03_hw/lab03/formatter_lib/)
add_library(formatter STATIC ${CMAKE_CURRENT_SOURCE_DIR}/formatter.cpp)
include_directories(${CMAKE_CURRENT_SOURSE_DIR}/formatter.h)
```
## Задание 2
```sh
$ cd..
$ cd formatter_ex_lib
```
```sh
cat > CMakeLists.txt <<EOF
> cmake_minimum_required(VERSION 3.4)
> project(formatter_ex)
> EOF                       
```
```sh
$ cat >> CMakeLists.txt <<EOF
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CURRENT_SOURCE_DIR /home/timur/BaltaevTimur/workspace/lab03_hw/lab03/formatter_ex/)
EOF
```
```sh
     $ cat >> CMakeLists.txt <<EOF
add_library(formatter_ex STATIC \${CMAKE_CURRENT_SOURCE_DIR}/formatter_ex.cpp)
EOF               
```
```sh
$ cat >> CMakeLists.txt <<EOF
include_directories(/home/timur/BaltaevTimur/workspace/lab03_hw/lab03/formatter_lib/)
EOF                      
```
```sh
$ cat >> CMakeLists.txt <<EOF
include_directories(\${CMAKE_CURRENT_SOURSE_DIR}/formatter_ex.h)
EOF
```
```sh
$ cmake -H. -B_build
```
```sh
-- Configuring done
-- Generating done
-- Build files have been written to: /home/timur/BaltaevTimur/workspace/lab03_hw/lab03/formatter_ex_lib/_build
```
```sh
$ cmake --build _build
```
```sh
[ 50%] Building CXX object CMakeFiles/formatter_ex.dir/formatter_ex.cpp.o
[100%] Linking CXX static library libformatter_ex.a
[100%] Built target formatter_ex
```
