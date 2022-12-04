# Padavan-build
0.点击右上角的Fork按钮，进入自己fork后的仓库。
1.修改/workflows/build-padavan.yml里的插件与机型。修改TNAME: K2P 中的K2P为需要编译的型号，注意名称要与configs/templates/目录下的名字
相同。修改后commit changes保存。
2.点击页面上部的Actions按钮，点击I understand my workflows，go ahead and enable them绿色按钮启用action。
3.点击右上角的 Star 星星按钮即可开始自动编译（自己点击才会编译）。修改配置后若需再次编译，先点击Star取消Star后，再点击Star即可重新编译。
编译完成后在Actions页面底部下载固件。

超频设置：trunk/linux-3.4.x/arch/mips/rt2880/init.c
(0x362=1100 0x3B2=1200)

#if defined(CONFIG_RALINK_MT7621_PLL900)

           if ((reg & 0x7ff) != 0x3B2) {
           
                         reg &= ~(0x7ff);
                         
                         reg |=  (0x3B2);
                         
trunk/configs/templates/NETGEAR-BZV.config

CONFIG_FIRMWARE_CPU_900MHZ=y

将CONFIG_FIRMWARE_CPU_900MHZ前的注释“#”去掉就好

端口WiFi设置：trunk/user/shared/defaults.h

修改logo：trunk/user/www/n56u_ribbon_fixed/bootstrap/img/asus_logo.png  里替换asus_logo.png
