#pragma once // Директива предотвращения повторного включения
#include <exception> // Подключаем базовый класс исключений
#include <string> // Подключаем строки для текста ошибки

class FileException : public std::exception { // Класс исключения для ошибок файла
private:
    std::string message; // Поле для хранения текста ошибки
public:
    FileException(const std::string& msg) : message(msg) {} // Конструктор, принимающий текст
    const char* what() const noexcept override { return message.c_str(); } // Переопределение метода what
};

class MemoryException : public std::exception { // Класс исключения для ошибок памяти
private:
    std::string message; // Поле для хранения текста ошибки
public:
    MemoryException(const std::string& msg) : message(msg) {} // Конструктор, принимающий текст
    const char* what() const noexcept override { return message.c_str(); } // Переопределение метода what
};

class InputException : public std::exception { // Класс исключения для некорректного ввода
private:
    std::string message; // Поле для хранения текста ошибки
public:
    InputException(const std::string& msg) : message(msg) {} // Конструктор, принимающий текст
    const char* what() const noexcept override { return message.c_str(); } // Переопределение метода what
};

class IndexException : public std::exception { // Класс исключения для выхода за границы индекса
private:
    std::string message; // Поле для хранения текста ошибки
public:
    IndexException(const std::string& msg) : message(msg) {} // Конструктор, принимающий текст
    const char* what() const noexcept override { return message.c_str(); } // Переопределение метода what
