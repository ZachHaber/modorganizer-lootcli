CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

SET(PROJ_NAME lootcli)

PROJECT(${PROJ_NAME})

SET(DEPENDENCIES_DIR CACHE PATH "")

LIST(APPEND CMAKE_PREFIX_PATH ${DEPENDENCIES_DIR}/lootapi)

FILE(GLOB_RECURSE BOOST_ROOT ${DEPENDENCIES_DIR}/boost*/project-config.jam)
GET_FILENAME_COMPONENT(BOOST_ROOT ${BOOST_ROOT} DIRECTORY)

ADD_SUBDIRECTORY(src)
