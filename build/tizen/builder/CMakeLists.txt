SET(BUILDER_SRC_DIR ${ROOT_SRC_DIR}/builder)

SET(DALI_BUILDER_SRCS ${BUILDER_SRC_DIR}/dali-builder.cpp)
SET(DALI_BUILDER_SRCS ${DALI_BUILDER_SRCS} "${ROOT_SRC_DIR}/shared/resources-location.cpp")
ADD_EXECUTABLE(dali-builder ${DALI_BUILDER_SRCS})
TARGET_LINK_LIBRARIES(dali-builder ${REQUIRED_PKGS_LDFLAGS})
INSTALL(TARGETS dali-builder DESTINATION ${BINDIR})
