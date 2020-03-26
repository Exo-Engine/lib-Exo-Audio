cmake_minimum_required(VERSION 3.8)
project(ExoAudio CXX)

file(GLOB SOURCES
	audio/include/*.h
	audio/include/**/**.h
	audio/src/*.cpp
	audio/src/**/**.cpp
	OpenAL/include/*.h
	OpenAL/include/**/**.h
	OpenAL/src/*.cpp
	OpenAL/src/**/**.cpp
)

include_directories(
	audio/include
	OpenAL/include)

add_library(ExoAudio SHARED ${SOURCES})
