# gdb-tips

---

## 信息显示

* [显示gdb版本信息](doc/show-version.md)
* [显示gdb版权相关信息](doc/show-copying-warranty.md)
* [启动时不显示提示信息](doc/start-gdb-silently.md)
* [退出时不显示提示信息](doc/quit-gdb-silently.md)
* [输出信息多时不会暂停输出](doc/set-pagination-off.md)

---

## 函数

* [列出函数的名字](doc/info-function.md)
* [是否进入带调试信息的函数](doc/step-and-next-function.md)
* [进入不带调试信息的函数](doc/set-step-mode-on.md)
* [退出正在调试的函数](doc/finish-and-return.md)
* [直接执行函数](doc/call-func.md)
* [打印函数堆栈帧信息](doc/info-frame.md)
* [打印尾调用堆栈帧信息](doc/set-debug-entry-values.md)
* [选择函数堆栈帧](doc/select-frame.md)
* [向上或向下切换函数堆栈帧](doc/up-down-select-frame.md)

---

## 断点

* [在匿名空间设置断点](doc/break-anonymous-namespace.md)
* [在程序地址上打断点](doc/break-on-address.md)
* [在程序入口处打断点](doc/break-on-entry.md)
* [在文件行号上打断点](doc/break-on-linenum.md)
* [保存已经设置的断点](doc/save-breakpoints.md)
* [设置临时断点](doc/set-tbreak.md)
* [设置条件断点](doc/set-condition-break.md)
* [忽略断点](doc/ignore-break.md)

---

## 观察点

* [设置观察点](doc/set-watchpoint.md)
* [设置观察点只针对特定线程生效](doc/set-watchpoint-on-specified-thread.md)
* [设置读观察点](doc/set-read-watchpoint.md)
* [设置读写观察点](doc/set-read-write-watchpoint.md)

---

## Catchpoint

* [让catchpoint只触发一次](doc/tcatch.md)
* [为fork调用设置catchpoint](doc/catch-fork.md)
* [为vfork调用设置catchpoint](doc/catch-vfork.md)
* [为exec调用设置catchpoint](doc/catch-exec.md)
* [为系统调用设置catchpoint](doc/catch-syscall.md)
* [通过为ptrace调用设置catchpoint破解anti-debugging的程序](doc/catch-ptrace.md)

---

## 打印

* [打印ASCII和宽字符字符串](doc/print-ascii-and-wide-string.md)
* [打印STL容器中的内容](doc/print-STL-container.md)
* [打印大数组中的内容](doc/print-large-array.md)
* [打印数组中任意连续元素值](doc/print-consecutive-array-elements.md)
* [打印数组的索引下标](doc/print-array-indexes.md)
* [格式化打印数组](doc/print-formatted-array.md)
* [打印函数局部变量的值](doc/print-local-variables.md)
* [打印进程内存信息](doc/print-process-memory.md)
* [打印静态变量的值](doc/print-static-variables.md)
* [打印变量的类型和所在文件](doc/print-variable-info.md)
* [打印内存的值](doc/examine-memory.md)
* [打印源代码行](doc/print-source-lines.md)
* [每行打印一个结构体成员](doc/set-print-pretty-on.md)
* [按照派生类型打印对象](doc/print-derived-type.md)
* [指定程序的输入输出设备](doc/set-io-tty.md)
* [使用“$\\_”和“$\\__”变量](doc/use-$_-$__-variables.md)
* [打印程序动态分配内存的信息](doc/print-malloc-memory.md)
* [打印调用栈帧中变量的值](doc/print-frame-variables.md)

---

## 多进程/线程

* [调试已经运行的进程](doc/attach-process.md)
* [调试子进程](doc/set-follow-fork-mode-child.md)
* [同时调试父进程和子进程](doc/set-detach-on-fork.md)
* [查看线程信息](doc/print-threads.md)
* [打印所有线程的堆栈信息](doc/print-all-threads-bt.md)
* [在Solaris上使用maintenance命令查看线程信息](doc/maint-info-sol-threads.md)
* [不显示线程启动和退出信息](doc/show-print-thread-events.md)
* [只允许一个线程运行](doc/set-scheduler-locking-on.md)
* [使用“$_thread”变量](doc/use-$_thread-variable.md)
* [一个gdb会话中同时调试多个程序](doc/add-copy-inferiors.md)
* [打印程序进程空间信息](doc/maint-info-program-space.md)
* [使用“$_exitcode”变量](doc/use-$_exitcode.md)

---

## core dump文件

* [为调试进程产生core dump文件](doc/generate-core-dump-file.md)
* [加载可执行程序和core dump文件](doc/load-executable-and-coredump-file.md)

---

## 汇编

* [设置汇编指令格式](doc/set-disassembly-flavor.md)
* [在函数的第一条汇编指令打断点](doc/break-on-first-assembly-code.md)
* [自动反汇编后面要执行的代码](doc/disassemble-next-line.md)
* [将源程序和汇编指令映射起来](doc/map-source-code-and-assembly.md)
* [显示将要执行的汇编指令](doc/display-instruction-pc.md)
* [打印寄存器的值](doc/print-registers.md)
* [显示程序原始机器码](doc/disassemble-raw-machine-code.md)

---

## 改变程序的执行

* [改变字符串的值](doc/change-string.md)
* [设置变量的值](doc/set-var.md)
* [修改PC寄存器的值](doc/modify-pc-register.md)
* [跳转到指定位置执行](doc/jump.md)
* [使用断点命令改变程序的执行](doc/breakpoint-command.md)
* [修改被调试程序的二进制文件](doc/patch-program.md)

---

## 信号

* [查看信号处理信息](doc/info-signals.md)
* [信号发生时是否暂停程序](doc/stop-signal.md)
* [信号发生时是否打印信号信息](doc/print-signal.md)
* [信号发生时是否把信号丢给程序处理](doc/pass-signal.md)
* [给程序发送信号](doc/send-signal.md)
* [使用“$_siginfo”变量](doc/use-$_siginfo-variable.md)

---

## 共享库

* [显示共享链接库信息](doc/info_sharedlibrary.md)

---

## 脚本

* [配置gdb init文件](doc/config-gdbinit.md)
* [按何种方式解析脚本文件](doc/set-script-extension.md)
* [保存历史命令](doc/save-history-commands.md)

---

## 源文件

* [设置源文件查找路径](doc/directory.md)
* [替换查找源文件的目录](doc/substitute-path.md)

---

## 图形化界面

* [进入和退出图形化调试界面](doc/tui-mode.md)
* [显示汇编代码窗口](doc/layout-asm.md)
* [显示寄存器窗口](doc/layout-regs.md)
* [调整窗口大小](doc/winheight.md)

---

## 其它

* [命令行选项的格式](doc/option-format.md)
* [支持预处理器宏信息](doc/preprocessor-macro.md)
* [保留未使用的类型](doc/keep-unused-types.md)
* [使用命令的缩写形式](doc/use-short-command.md)
* [在gdb中执行shell命令和make](doc/run-shell-command.md)
* [在gdb中执行cd和pwd命令](doc/run-cd-pwd.md)
* [设置命令提示符](doc/set-prompt.md)
* [设置被调试程序的参数](doc/set-program-args.md)
* [设置被调试程序的环境变量](doc/set-program-env.md)
* [得到命令的帮助信息](doc/help.md)
* [记录执行gdb的过程](doc/set-logging.md)
* [打印C++虚表及其内容](doc/show-vtbl-content.md)
