<p align="center">
<a href=https://twitter.com/mangopi_sbc><img alt="Twitter Follow" src="https://img.shields.io/twitter/follow/mangopi_sbc?logo=twitter&style=flat-square"></a>

</p>

# Tina-Linux
Tina-Linux for F133/T113/D1-H


### Ubuntu18.04 environment 
  $ sudo apt-get install build-essential subversion git-core libncurses5-dev zlib1g-dev gawk flex quilt libssl-dev xsltproc libxml-parser-perl mercurial bzr ecj cvs unzip lib32z1 lib32z1-dev lib32stdc++6 libstdc++6 libmpc-dev libgmp-dev -y

### SDK download from GitHub
``` sh
  $ git clone  https://github.com/flyingcys/tina_linux_d1h_t133_t113.git 
  $ cd tina_linux_d1h_t133_t113
  $ git submodule update --init --recursive

  # download the static file
  $ wget https://github.com/flyingcys/tina_linux_d1_t133_t113/releases/download/0.0.1/prebuilt.tar.gz .
  # or
  $ wget https://riscv-tools.oss-cn-shanghai.aliyuncs.com/tina-linux/prebuilt.tar.gz .
  $ tar xzvf prebuilt.tar.gz
  # dl.tar.gz
  $ wget https://riscv-tools.oss-cn-shanghai.aliyuncs.com/tina-linux/dl.tar.gz .
  $ tar xvf dl.tar
  
  $ wget https://github.com/flyingcys/tina_linux_d1_t133_t113/releases/download/0.0.1/riscv64-linux-x86_64-20200528.tar.xz -P ./lichee/brandy-2.0/tools/toolchain/
  $ wget https://github.com/flyingcys/tina_linux_d1_t133_t113/releases/download/0.0.1/gcc-linaro-7.2.1-2017.11-x86_64_arm-linux-gnueabi.tar.xz -P ./lichee/brandy-2.0/tools/toolchain/
  
  # or
  $ wget https://riscv-tools.oss-cn-shanghai.aliyuncs.com/tina-linux/riscv64-linux-x86_64-20200528.tar.xz -P ./lichee/brandy-2.0/tools/toolchain/
  $ wget https://riscv-tools.oss-cn-shanghai.aliyuncs.com/tina-linux/gcc-linaro-7.2.1-2017.11-x86_64_arm-linux-gnueabi.tar.xz -P ./lichee/brandy-2.0/tools/toolchain/
  
```

### Compile
  $ source build/envsetup.sh
  $ lunch
``` sh
  You're building on Linux

Lunch menu... pick a combo:
     1. d1_mq_pro-tina
     2. d1_nezha_min-tina
     3. d1_nezha-tina
     4. f133_evb1-tina
     5. f133_mq_r-tina
     6. t113_evb1-tina
     7. t113_mq_r-tina


  $ 1 or 5 or 7
  
  $ make
  $ mboot
  $ pack
  
  Tina-Linux/out/d1-mq_pro/tina_d1-mq_pro_uart0.img
  
  ``` 
  
### Flash to TF-Card

just used [phoenixcard for windows](https://mangopi.org/_media/phoenixcard4.2.8.zip) 

more info : https://mangopi.org
  
