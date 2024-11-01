set(SOURCES src/OmegaESP32I2CController.c)
set(PUBLIC_HEADER_DIRS inc)
set(PRIVATE_HEADER_DIRS priv/inc)

file(
        DOWNLOAD https://raw.githubusercontent.com/Omegaki113r/OmegaUtilityDriver/refs/heads/main/inc/OmegaUtilityDriver.h 
        ${CMAKE_CURRENT_SOURCE_DIR}/inc/OmegaUtilityDriver.h
    )
idf_component_register(
                    SRCS ${SOURCES}
                    INCLUDE_DIRS ${PUBLIC_HEADER_DIRS}
                    PRIV_INCLUDE_DIRS  ${PRIVATE_HEADER_DIRS}
                    REQUIRES driver
                    )