cmake_minimum_required(VERSION 2.8.12)
project(Montage)

#set(Montage_LIBRARIES Montage)

if(NOT ITK_SOURCE_DIR)
  find_package(ITK REQUIRED)
  list(APPEND CMAKE_MODULE_PATH ${ITK_CMAKE_DIR})
  include(ITKModuleExternal)
else()
  itk_module_impl()
endif()

itk_module_examples()
