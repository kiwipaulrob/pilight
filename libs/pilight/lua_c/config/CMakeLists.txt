project(pilight_lua_c_config)

add_subdirectory(devices)

file(GLOB ${PROJECT_NAME}_sources "${PROJECT_SOURCE_DIR}/*.c")
file(GLOB ${PROJECT_NAME}_headers "${PROJECT_SOURCE_DIR}/*.h")

set(${PROJECT_NAME}_files ${${PROJECT_NAME}_sources} ${${PROJECT_NAME}_headers} CACHE INTERNAL "")

set(${PROJECT_NAME}_files
	${${PROJECT_NAME}_sources}
	${${PROJECT_NAME}_headers}
	${${PROJECT_NAME}_devices_files}
CACHE INTERNAL "")