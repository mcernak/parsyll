#
# CMake file for syllabledecoder_PLP.c
#
# Milos Cernak
# May 2014
#

#Project generalities
PROJECT(syllabledecoder)

MESSAGE("nsylb files will be built in ${PROJECT_SOURCE_DIR}/bin")
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)
SET(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)

INCLUDE_DIRECTORIES(/idiap/resource/software/matlab/8.5/extern/include)
LINK_DIRECTORIES(/idiap/resource/software/matlab/8.5/bin/glnxa64)

add_executable(nsylb syllabledecoder_PLP.c)
target_link_libraries(nsylb m mat mx)

