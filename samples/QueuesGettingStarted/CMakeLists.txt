cmake_minimum_required(VERSION 3.17)
message("Starting Build")
project(Application)


include_directories(. 
	/usr/local/include 
	/home/gvigelet/azure-storage-cpp/Microsoft.WindowsAzure.Storage/samples/SamplesCommon)

set(SOURCE_FILES Application.cpp)

link_directories(/usr/local/lib
	/usr/lib/lib)

add_executable(app ${SOURCE_FILES})
target_link_libraries(app ssl)
target_link_libraries(app crypto)
target_link_libraries(app azurestorage)

