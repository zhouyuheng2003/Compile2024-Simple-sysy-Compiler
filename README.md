# Compile2024-Simple-sysy-Compiler

## 简介

2024编译原理课程设计（2024.5.9~2024.6.20）

## 组员

- [Zysun2002](https://github.com/Zysun2002)

- [zhouyuheng2003](https://github.com/zhouyuheng2003)

- [JluShy](https://github.com/JluShy)

## 运行指南

### 生成中间代码

- 安装flex和bison（windows操作系统可以用setup文件夹中的安装包，并配置环境变量）

- 新建build文件夹

- 运行如下指令：

  ```
  flex -l sysy.l
  bison -d sysy.y
  g++ main.cpp lex.yy.c sysy.tab.c -o sys2koopa.exe -std=c++11
  sys2koopa input.sy output.koopa
  ```


### 生成目标代码

运行setup中提供的koopa2riscv，比如要将output.koopa转化为output.riscv，需执行：

```
./koopa2riscv output.koopa output.riscv
```

这一步操作需要在Linux环境里进行。

## 参考材料

- [北京大学编译实践课程在线文档](https://pku-minic.github.io/online-doc/#/)

- [llvm compiler infrastructure](https://llvm.org/docs/)
- [北京大学编译原理课程实践报告-George M](https://zhuanlan.zhihu.com/p/640953686)
- [2021Spring北京大学编译实践lab报告-江枫渔火](https://zhuanlan.zhihu.com/p/584830038)
- [Compiler_Koopa_RISCV-胡剑铮，衣然，郭冠男](https://github.com/HocRiser01/Compiler_Koopa_RISCV)
