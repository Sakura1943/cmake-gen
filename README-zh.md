# cmake-gen
CMake项目生成器
---

[English](./README.md) | 简体中文

---

## 准备

> Python >= 3.6<br>
> CMake >= 3.0.0<br>

---

## 🤖 安装
存放于环境变量`$PATH`中已存在的路径，比如`/usr/bin`，或者`$HOME/.local/bin`。

```shell
git clone https://github.com/Sakura1943/cmake-gen.git
cd cmake-gen
cp -f ./cmake-gen $HOME/.local/bin
```

---
## 📖 使用方法
### 帮助信息

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

### 生成项目
#### 可执行项目

```shell
cmake-gen --executable
```

```txt
> 软件包名: demo
> 软件包版本(默认0.1.0): 
> c或者cpp(默认c): 
> Cmake配置创建成功，路径: /home/xxx/code/cpp/demo/CMakeLists.txt
> 
> 正在创建源码文件夹以及入口文件
> 源码文件夹创建成功, 路径: /home/xxx/code/cpp/demo/src
> main入口文件创建成功，路径: main.c
> 
> 正在构建example
> 生成构造后Makefile存放文件夹，路径: /home/xxx/code/cpp/demo/build
> 开始构建最终target
> 正在生成Makefile
> 正在进入构建文件夹
> 开始构建
-- The C compiler identification is GNU 13.1.1
-- The CXX compiler identification is GNU 13.1.1
...
-- Configuring done (0.4s)
-- Generating done (0.0s)
-- Build files have been written to: /home/xxx/code/cpp/demo/build
> 构建Makefile成功
> 开始生成最终目标程序
[ 50%] Building C object CMakeFiles/demo.dir/main.c.o
[100%] Linking C executable demo
[100%] Built target demo
> 目标程序生成成功
> 执行example
Hello, demo!
> 回到项目根目录
> 
> 初始化完成
```

#### 代码库项目

```shell
cmake-gen --library
```

```txt
> 软件包名: demo
> 软件包版本(默认0.1.0): 
> c或者cpp(默认c): 
> Cmake配置创建成功，路径: /home/xxx/code/cpp/demo/CMakeLists.txt
> 
> 正在创建源码文件夹以及入口文件
> 源码文件夹创建成功, 路径: /home/xxx/code/cpp/demo/src
> 代码库入口文件创建成功，路径: /home/xxx/code/cpp/demo/demo.c
> 
> 初始化完成
```

---

## License
The MIT License ([MIT](https://opensource.org/licenses/MIT))
