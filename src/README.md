# Standard D Flip-Flop Struct
## 概述
一系列标准的触发器，采用`verlog`编写，并遵循`verilog-2001`标准。触发器默认位宽`DATA_WIDTH=16`，触发器均采用`always`模块实现，下面列出支持的触发器结构。

- `dff`：无复位，无使能
- `dffl`：无复为，<font color=Aqua>高电平使能</font>，失能时保持输出
- `dfflr`：<font color=Aqua>复位下降沿触发</font>，复位后输出`0`，<font color=Aqua>高电平使能</font>，失能时保持原输出
- `dfflrc`：<font color=Aqua>复位下降沿触发</font>，复位后输出`0`，<font color=Aqua>高电平使能</font>，失能时输出`0`
- `dfflrs`：<font color=Aqua>复位下降沿触发</font>，复位后输出`1`，<font color=Aqua>高电平使能</font>，失能时保持原输出
- `dffr`：<font color=Aqua>复位下降沿触发</font>，复位后输出`0`，无使能
- `dffrs`：<font color=Aqua>复位下降沿触发</font>，复位后输出`1`，无使能

---

## 触发器结构
![image](image/D-Flip-Flop.png)

---

## 调用方法
moduleName：`dff`，`dffr`，`dffrs`
```verilog
moduleName #(DATA_WIDTH) instName (clk, rstn, d, q);
```
moduleName：`dffl`，`dfflr`，`dfflrc`，`dfflrs`
```verilog
moduleName #(DATA_WIDTH) instName (clk, rstn, en, d, q);
```
---
