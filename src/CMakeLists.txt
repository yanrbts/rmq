#
# Copyright 2024-2024 yanruibinghxu@gmail.com
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#   http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#
cmake_minimum_required(VERSION 3.29.0)
set(CMAKE_BUILD_TYPE Debug)
project(rmq)

include_directories(../rabbitmq-c/include)
link_directories(../build/rabbitmq-c)

set(SOURCES rmq.c)
add_executable(rmq ${SOURCES})
target_link_libraries(rmq PRIVATE rabbitmq)