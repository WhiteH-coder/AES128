# 1. 目录结构
- doc       毕业论文   
- prj       包含四个Vivado工程
- rep       ASIC流程中的dc和icc报告
- rtl       设计的硬件代码
- scripts   与设计相关的使用脚本
- sw        设计应用程序代码
- tb        仿真激励文件

# 2. 开发环境 
- 软件版本 Vivado 2018.3
- 使用器件 xz7010clg400-1
- 应用程序 Python 3.8.3 

# 3. 文件说明
## 3.1 doc
## 3.2 prj
  - aes128   
  - aes128led
  - aes128vip
  - crypt
  
### 3.2.1 aes128
    基础的Vivado设计工程，主要用于设计的仿真测试
### 3.2.2 aes128led
    进行在线调试（ila与vio）的Vivado工程，需要根据实际使用的开发板修改对应的引脚约束
### 3.2.3 aes128vip
    对已封装成带有AXI4-Lite接口的AES IP的Vivado验证工程
### 3.2.4 crypt
    完整AES加解密系统的Vivado工程，即包含PS（处理器端）代码
## 3.3 rep
### 3.3.1 dc
### 3.3.2 icc
## 3.4 rtl
### 3.4.1 boolsbox
    直接由组合逻辑搭建的sbox电路，采用同构域的思想，详细解释可参考doc目录下的参考文献
### 3.4.2 设计实际使用代码
- aes128.v
- decode
- encode
- keyexp
- mixcol
- reg_128.v
- reg128.v
- sbox          基于改进型查找表(求逆电路)实现的sbox
- shiftmap.v
- xtime.v

## 3.5 scripts
### 3.5.1 char2hex
    ASCII字符域十六进制的转换
### 3.5.2 filecrpty
    AES文件加解密的python脚本
### 3.5.3 GF8_INV
    用于求取有限域GF(2^8)中元素的乘法逆元的C代码
### 3.5.4 tiny-AES-c-master
    开源的AESc代码实现，可用于数据结果验证
## 3.6 sw
    Pyqt5编写的界面程序
## 3.7 tb
    RTL代码的仿真测试文件，包括sbox、密钥扩展和总体模块的功能仿真

# 4. 一些问题的解决
    
