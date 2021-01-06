set(TS_FILES Sqlite3QT_ru_RU.ts)

set(PROJECT_SOURCES
        adminwindow.h
        adminwindow.cpp
        adminwindow.ui
        columncreator.h
        columncreator.cpp
        columncreator.ui
        columnrenamer.h
        columnrenamer.cpp
        columnrenamer.ui
        dbmanager.cpp
        dbmanager.h
        entitycreator.h
        entitycreator.cpp
        entitycreator.ui
        fkcreator.h
        fkcreator.cpp
        fkcreator.ui
        loginwindow.h
        loginwindow.cpp
        loginwindow.ui
        main.cpp
        mainwindow.cpp
        mainwindow.h
        mainwindow.ui
        ${TS_FILES}
)

add_executable(Sqlite3QT ${PROJECT_SOURCES})


qt5_create_translation(QM_FILES ${CMAKE_SOURCE_DIR} ${TS_FILES})




target_link_libraries(Sqlite3QT PRIVATE
    Qt5::Widgets
    Qt5::Sql)
