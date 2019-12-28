# useless
FPGA 项目练习
Artix 7 型号  XC7A100T-2FGG484I   xc7a100tfgg484-2

供电顺序：
 Artix-7 FPGA电源有VCCINT, VCCBRAM, VCCAUX, VCCO, VMGTAVCC和VMGTAVTT。
 VCCINT为 FPGA内核供电引脚，需接1.0V；VCCBRAM,为FPGA Block RAM的供电引脚；接1.0V； 
 VCCAUX为FPGA辅助供电引脚, 接1.8V；VCCO为FPGA的各个BANK的电压，包含 BANK0,BANK13~16, BANK34~35，在 AC7100核心板上，
 BANK34，BANK35因为 需要连接DDR3，BANK的电压连接的是1.5V，其它BANK的电压都是3.3V，
 其中BANK15和BANK16的VCCO是由LDO供电，可以通过更换LDO芯片更改BANK的 电平。
 VMGTAVCC为FPGA内部GTP收发器的供电电压，接1.0V，VMGTAVTT为GTP收发 器的端接电压，接1.2V。 
 
 有源差分晶振 ：
  200Mhz差分时钟 SYS_CLK_P R4 
                SYS_CLK_N T4； 通过PLLs和DCMs调整频率。 
  
  125Mhz差分时钟  MGT_CLK0_P F6 
                 MGT_CLK0_N E6； 
 
 复位按键：
  低电平有效 RESET_N  T6
  
 矩阵键盘：
 https://detail.tmall.com/item.htm?spm=a1z10.5-b-s.w4011-21725054633.69.39044eb45bpcqs&id=596448347432&rn=1662222fed3188e0fde5fff2b78b2544&abbucket=1
