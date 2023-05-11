# CMake Build Template

### HN

This is a CMake build template designed to help you quickly set up a C++ project with CMake as the build system. CMake is a popular cross-platform build tool that provides a simple and efficient way to manage the build process of your project.

## Prerequisites

Before using this template, make sure you have the following installed on your system:

- CMake (version 3.18.4 required)
- C++ compiler (compatible with your operating system)

## Build CMake 3.18.4
Get and build CMake:

```
sudo apt update
sudo apt install cmake
```

Or use the shell script:

```
chmod +x build_cmake.sh
./build_cmake.sh
```

## Getting Started

To use this template, follow these steps:

1. Clone this repository or download the source code to your local machine.
2. Open a terminal and navigate to the root directory of the project.

## Building the Project

To build the project, follow these steps:

1. Create a `build` directory in the root of the project:  
   `mkdir build`
2. Navigate to the `build` directory:  
   `cd build`
3. Generate the build files using CMake:  
   `cmake ..`
4. Build the project using the generated build files:  
   `cmake --build .`

By default, the project will be built using the default configuration for your system.

## Configuring the Build

CMake allows you to configure the build according to your requirements. Here are some common options:

- Changing the build type (e.g., Debug or Release):  
  `cmake -DCMAKE_BUILD_TYPE=Debug ..`
- Specifying a custom install directory:  
  `cmake -DCMAKE_INSTALL_PREFIX=/path/to/install ..`

You can pass these options to the initial CMake configuration step or modify them in the `CMakeLists.txt` file.

## Running the Project

Once the project is built successfully, you can run the executable produced by the build. The location of the executable will depend on your build configuration and the platform you are using.

To run the project, navigate to the build directory and execute the generated executable:

```
cd build/src
./<executable_name>
```

## Testing

This build template does not currenly support Google Testing. For more information visit:

- [GoogleTest](https://google.github.io/googletest/quickstart-cmake.html)

## Additional Resources

For more information on using CMake, refer to the following resources:

- [CMake Documentation](https://cmake.org/documentation/)
- [CMake Tutorial](https://cmake.org/cmake/help/latest/guide/tutorial/index.html)

## License

This project is licensed under the [MIT License](LICENSE). Feel free to modify and distribute it as needed.

## Acknowledgments

This CMake build template is based on best practices and common conventions followed in C++ projects. Special thanks to the CMake community for providing a powerful build tool.
