cmake_minimum_required(VERSION 3.14)
project(lr2 VERSION 1.0.0 LANGUAGES CXX)

# Настройка стандарта C++
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# Включаем поддержку тестов
enable_testing()

# Опции для сборки
option(BUILD_TESTS "Build tests" ON)

# Подключаем подпроекты
add_subdirectory(src)

if(BUILD_TESTS)
    # Добавляем папку с тестами (она будет обработана позже)
    add_subdirectory(test)
endif()