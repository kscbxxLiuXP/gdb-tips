# gdb-tips

## 简介

本项目来源 <https://github.com/hellogcc/100-gdb-tips>

在此基础上进行修改，并使用`gitbooks`在gitlab上构建出一个文档

本项目中有丰富的gdb调试技巧，除了这些，大家可以往里面补充一些自己的技巧，比如一些好用的脚本

## 开始阅读

- [gdb-gitbooks(推荐)](https://kscbxxliuxp.github.io/gdb-tips/)
- [gdb-tips(markdown)](SUMMARY.md)

## gdbinit

下面是我自己使用的`.gitinit`中定义了一些方便调试的脚本

```
set print pretty on
set print null-stop
set listsize 20

set max-value-size unlimited 

define px
    p/x $arg0
end

define ix
    i/x $arg0
end


define i5x
    i/5x $arg0
end


define i10x
    i/10x $arg0
end


define i15x
    i/15x $arg0
end

define cmd
    focus cmd
end

define src
    focus src
end

define lsrc
    layout src
end

define lspit
    layout split
end

define lasm
    layout asm
end


define pir1
    set $a = $arg0->info.mnemonic
    set $b = $arg0->info.op_str
    printf "%s %s\n", $a , $b
end

define ppir1
    set $a = pir1->info.mnemonic
    set $b = pir1->info.op_str
    printf "0x%lx\t%s %s\n", pc,$a , $b
end

#print array
define pir1list
    set $i = ir1_num
    p $i
    while $i>0
        set $ir1 = ir1_list[$i-1]
        set $pc = ir1_list[$i-1]->info.address
        set $a = ir1_list[$i-1]->info.mnemonic
        set $b = ir1_list[$i-1]->info.op_str
        printf "0x%lx\t%s %s\n", $pc,$a , $b
        set $i--
    end

end
    

```
