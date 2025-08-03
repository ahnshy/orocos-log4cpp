# 📦 orocos-log4cpp for Windows (CMake Build)
&nbsp;This project provides a clean and easy-to-follow setup for building [orocos-log4cpp](https://github.com/orocos-toolchain/log4cpp) on **Windows** using **CMake v3.31.8**.<br/>
&nbsp;✅ Tested on Windows 10 / Visual Studio 2019 / CMake 3.31.8 <br/>
<br/>

## About orocos-log4cpp
 `orocos-log4cpp` is a fork of the original [log4cpp](https://sourceforge.net/projects/log4cpp/) library. <br/>
 It provides a powerful and flexible logging system for C++ applications, suitable for real-time systems such as Orocos (Open Robot Control Software). <br/>
<br/><br/>

## 🖥️ Overview
 Building orocos-log4cpp for Windows using the CMake utility. <br/>
 The artifacts generated from the repository built with CMake can be directly added and used in your Qt for Windows or Win32 or MFC project. <br/>
<br/><br/>

## ⚙️ Build Environment
- `Windows 10+` <br/>
- `Git for Windows` <br/>
- [Visual Studio 2019](https://visualstudio.microsoft.com/) <br/>
- [CMake 3.20+](https://cmake.org/download/) <br/>
<br/><br/>

## 🚀 Build Instructions
``` command
git clone --branch master https://github.com/orocos-toolchain/log4cpp.git
cd orocos-log4cpp-windows
mkdir build
cd build
cmake .. -G "Visual Studio 16 2019" -DCMAKE_BUILD_TYPE=Release -DBUILD_SHARED_LIBS=ON
```
<br/><br/>

## 📁 Folder Tree
/ `Root` <br/>
 ├── CMakeLists.txt # Main CMake configuration <br/>
 ├── log4cpp/ # Source code (forked) <br/>
 ├── build/ # CMake build output <br/>
 └── README.md # You are here <br/>
<br/><br/>

## 🔍 Notes
 ✅ CMake version 3.8 and above may result in build errors. It is recommended to install and use a version between 3.2 and 3.7
 This setup disables unnecessary components like doxygen and test targets by default for faster builds. <br/>
 If needed, you can modify CMakeLists.txt to include logging destinations or additional compilation options. <br/>
<br/><br/>

## 📤 Output
Compiled libraries (.lib, .dll) will be located in:
``` path
 log4cpp/Debug
 log4cpp/x64/Release
 log4cpp/x64/RelWithDebInfo
```
<br/>

## 💡 Usage Example Code
``` cpp
# include <log4cpp/Category.hh>

int main() {
    log4cpp::Category& root = log4cpp::Category::getRoot();
    root.setPriority(log4cpp::Priority::INFO);
    root.info("log4cpp demo infomation.");
}
```
<br/><br/>

## 💻 [Preview]
<br/><br/>

## 📃 License
 This project inherits the original [LGPL-2.1 License.](https://opensource.org/licenses/LGPL-2.1)
<br/><br/>
