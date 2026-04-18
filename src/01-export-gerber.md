# 导出 Gerber

```admonish abstract title="本步目标"
为制板机准备**三个 Gerber 层文件** + **一份 Excellon 钻孔文件**:

- **F.Cu**——顶层铜箔
- **B.Cu**——底层铜箔
- **Edge.Cuts**——板框轮廓
- **.drl**——钻孔文件（EDA 通常会分成 PTH / NPTH 两个）
```

```admonish info title="你知道吗：PTH 和 NPTH 为什么要分开？" collapsible=true
PTH（Plated Through Hole，电镀通孔）和 NPTH（Non-Plated Through Hole，非电镀孔）的分家是**可电镀工艺时代**留下的流程：

1. 先钻 **PTH**(要电镀的孔)
2. 对整板做电镀——孔壁沉积铜
3. 再钻 **NPTH**(机械孔)——在电镀之后钻，所以不会被镀到

两种孔的用途也不同——PTH 用作信号/电源的通孔（需要两面连通），NPTH 用作安装孔、定位孔（不需要导电）。

然而对我们而言，因为[没有电镀环节](./00-prepare-pcb/background.md)，这两种孔在加工上已经**完全没有区别**——EDA 仍然习惯性地分成两个文件，照样导出就行。
```

根据你使用的 EDA 选择对应章节：

- [KiCad](./01-export-gerber/kicad.md)
- [立创 EDA](./01-export-gerber/lceda.md)
- [Altium Designer](./01-export-gerber/altium.md)
