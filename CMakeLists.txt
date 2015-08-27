cmake_minimum_required(VERSION 2.8.9)

project(PointSetProcessing)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "http://www.example.com/Slicer/Extensions/PointSetProcessing")
set(EXTENSION_CATEGORY "Filtering")
set(EXTENSION_CONTRIBUTORS "Mikael Brudfors (brudfors@gmail.com)")
set(EXTENSION_DESCRIPTION "Performs point set processing in Slicer.")
set(EXTENSION_ICONURL "http://www.example.com/Slicer/Extensions/PointSetProcessing.png")
set(EXTENSION_SCREENSHOTURLS "http://www.example.com/Slicer/Extensions/PointSetProcessing/Screenshots/1.png")

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(PointSetProcessingPy)
add_subdirectory(PointSetProcessingCpp)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_CPACK})