
add_airliner_app_def(sens
    FILE SENS
    SOURCES
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/sens_app.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/sens_app.h
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/sens_config_utils.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/sens_events.h
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/sens_msg.h
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/sens_tbldefs.h
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/sens_version.h
   
    INCLUDES
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/

    USER_DOCS   ${CMAKE_CURRENT_SOURCE_DIR}/user_doxy.in
    DESIGN_DOCS ${CMAKE_CURRENT_SOURCE_DIR}/detail_doxy.in
)

add_airliner_app_unit_test(sens-ut
    UTASSERT
    SOURCES
        ${CMAKE_CURRENT_SOURCE_DIR}/../unit_test/sens_app_test.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/../unit_test/sens_app_test.h
        ${CMAKE_CURRENT_SOURCE_DIR}/../unit_test/sens_cmds_test.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/../unit_test/sens_cmds_test.h
        ${CMAKE_CURRENT_SOURCE_DIR}/../unit_test/sens_config_tbl_test.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/../unit_test/sens_config_tbl_test.h
        ${CMAKE_CURRENT_SOURCE_DIR}/../unit_test/sens_testrunner.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/../unit_test/sens_test_utils.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/../unit_test/sens_test_utils.h
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/sens_app.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/sens_app.h
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/sens_config_utils.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/sens_events.h
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/sens_msg.h
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/sens_tbldefs.h
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/sens_version.h
        
    INCLUDES
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/
        ${CMAKE_CURRENT_SOURCE_DIR}/../unit_test/
        
    VALGRIND_SUPPRESSION_FILE
        ${CMAKE_CURRENT_SOURCE_DIR}/../unit_test/valgrind.supp
)
