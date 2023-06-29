# cmake-gen
Cmake project generator
---

English | [简体中文](./README-zh.md)

---
## 🤖 Installation
Stored in paths that exist in the `$PATH` environment variable, such as `/usr/bin`, or `$HOME/.local/bin`.
```shell
git clone https://github.com/Sakura1943/cmake-gen.git
cp -f ./cmake-gen $HOME/.local/bin
```
---
## 📖 Usage
### Help information
```shell
cmake-gen --help
```
```txt
usage: cmake-gen [-h] [--executable] [--library] [-v]

Generate CMake projects

options:
  -h, --help     show this help message and exit
  --executable   generate executable project
  --library      generate code library
  -v, --version  display version
```

### Generate the project
#### Executable project
```shell
cmake-gen --executable
```
```txt
> Package name: demo
> Package version (default 0.1.0): #
> c or cpp (default: c):
> Cmake configuration created successfully, path: /home/xxx/code/cpp/demo/CMakeLists.txt
> 
> The source folder and entry file are being created
> Source folder created successfully, path: /home/xxx/demo/src
> main entry file created successfully, path: main.c
> 
> An example is being built
>  After generating the Makefile storage folder, path: /home/xxx/code/cpp/demo/build
> Start building the final target
> Generating Makefile
> Entering build folder
> Start building
-- The C compiler identification is GNU 13.1.1
-- The CXX compiler identification is GNU 13.1.1
...
-- Build files have been written to: /home/xxx/code/cpp/demo/build
> Build Makefile successfully
> Start building the final target program
[ 50%] Building C object CMakeFiles/demo.dir/main.c.o
[100%] Linking C executable demo
[100%] Built target demo
> The target program builds successfully
> Perform example
Hello, demo!
> Go back to the project root
> 
> Initialization completed
```

#### Library project
```shell
cmake-gen --library
```
```txt
> Package name: demo
> Package version (default 0.1.0): 
> c or cpp (default: c): 
> Cmake configuration created successfully, path: /home/xxx/code/cpp/demo/CMakeLists.txt
> 
> The source folder and entry file are being created
> Source folder created successfully, path: /home/xxx/code/cpp/demo/src
> library entry file created successfully, path: /home/xxx/code/cpp/demo/demo.c
> 
> Initialization completed
```
---
## License
The MIT License ([MIT](https://opensource.org/licenses/MIT))