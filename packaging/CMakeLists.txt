# Remove this to get package names that are formatted as
# ${CPACK_PACKAGE_NAME}-${CPACK_PACKAGE_VERSION}-${CPACK_SYSTEM_NAME}.
set(CPACK_PACKAGE_FILE_NAME "Halide" CACHE STRING "Name of package created by distrib target")
set(CPACK_PACKAGE_VENDOR "Halide")
set(CPACK_RESOURCE_FILE_LICENSE "${Halide_SOURCE_DIR}/LICENSE.txt")
set(CPACK_MONOLITHIC_INSTALL OFF)
if (WIN32)
    set(CPACK_GENERATOR ZIP)
else ()
    set(CPACK_GENERATOR TGZ)
endif ()
include(CPack)