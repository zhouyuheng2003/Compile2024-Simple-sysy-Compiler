# Compile2024-Simple-sysy-Compiler

## Introduction / 简介 

2024编译原理课程设计（2024.5.9~2024.6.20

## Team Member / 组员

- [Zysun2002](https://github.com/Zysun2002)

- [zhouyuheng2003](https://github.com/zhouyuheng2003)

- [JluShy](https://github.com/JluShy)

## Run / 运行指南

### Intermediate code generation / 生成中间代码

- Installe Flex and Bison (for Windows OS, utilized installation packages from the setup folder) and configure environment variables / 安装flex和bison（windows操作系统可以用setup文件夹中的安装包，并配置环境变量）

- Created a new 'build' directory / 新建build文件夹

- Executed the following commands: / 运行如下指令：

  ```
  flex -l sysy.l
  bison -d sysy.y
  g++ main.cpp lex.yy.c sysy.tab.c -o sys2koopa.exe -std=c++11
  sys2koopa input.sy output.koopa
  ```


### Target code generation / 生成目标代码

Run the koopa2riscv tool provided in the setup to convert output.koopa to output.riscv by executing the following command: / 运行setup中提供的koopa2riscv，比如要将output.koopa转化为output.riscv，需执行：

```
./koopa2riscv output.koopa output.riscv
```

Perform this step in a Linux environment. / 这一步操作需要在Linux环境里进行。

## Reference / 参考材料

- [北京大学编译实践课程在线文档](https://pku-minic.github.io/online-doc/#/)

- [llvm compiler infrastructure](https://llvm.org/docs/)
- [北京大学编译原理课程实践报告-George M](https://zhuanlan.zhihu.com/p/640953686)
- [2021Spring北京大学编译实践lab报告-江枫渔火](https://zhuanlan.zhihu.com/p/584830038)
- [Compiler_Koopa_RISCV-胡剑铮，衣然，郭冠男](https://github.com/HocRiser01/Compiler_Koopa_RISCV)
