SET (DB_MANAGER_POSTGIS_VERSIONING_DIR ${DB_MANAGER_POSTGIS_DIR}/plugins/versioning)

FILE(GLOB PY_FILES *.py)

FILE(GLOB UI_FILES *.ui)
PYQT4_WRAP_UI(PYUI_FILES ${UI_FILES})
ADD_CUSTOM_TARGET(db_manager_postgis_versioning ALL DEPENDS ${PYUI_FILES})

INSTALL(FILES ${PY_FILES} DESTINATION ${DB_MANAGER_POSTGIS_VERSIONING_DIR})
INSTALL(FILES ${PYUI_FILES} DESTINATION ${DB_MANAGER_POSTGIS_VERSIONING_DIR})

