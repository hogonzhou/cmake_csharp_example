cmake_minimum_required(VERSION 3.1)
project("ExampleProject" CSharp)

set(CMAKE_CSharp_COMPILER "C:/Windows/Microsoft.NET/Framework64/v4.0.30319/csc.exe")

add_subdirectory(Example)
add_subdirectory(WindowsFormsApp)
