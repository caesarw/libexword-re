CMAKE_MINIMUM_REQUIRED(VERSION 3.5)

PROJECT("libexword-re")

SET(BIN_NAME "exword")
INCLUDE_DIRECTORIES(${PROJECT_SOURCE_DIR}/includes)
FILE(GLOB srcfile "databuffer.c" "dict.c" "exword.c" "obex.c" "util.c" )
ADD_EXECUTABLE(${BIN_NAME} main.c ${srcfile})

TARGET_LINK_LIBRARIES(exword usb-1.0 readline)