cmake_minimum_required(VERSION 3.8)
project(ExoAudioOpenAL CXX)

file(GLOB SOURCES
	include/*.h
	include/**/**.h
	src/*.cpp
	src/**/**.cpp
)

set(AUDIO_DIR ../audio)

include_directories(
	include
	${AUDIO_DIR}/include)

add_library(ExoAudioOpenAL SHARED ${SOURCES})
