find_package(OpenGL)
if (OPENGL_FOUND)
    message(STATUS "Found OpenGL at: ${OPENGL_LIBRARIES}")
    set_target_properties(OpenGL::GL
            PROPERTIES IMPORTED_GLOBAL TRUE)
endif ()