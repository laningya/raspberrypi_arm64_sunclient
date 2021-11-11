在树梅派上如何实现无公网IP的访问，向日葵作为一款好用的远控软件，但可惜的是没有对树梅派进行适配，这个deb包是一位大佬在向日葵官方包的基础上修改得来。
## 环境要求：
raspberrypi   arm64位操作系统   且必须用debain的源，不得替换为raspberry的源<br>
sudo apt update && sudo apt upgrade<br>
sudo apt install git <br>
git clone 项目地址<br>
cd raspberry_arm64_sunclient<br>
sudo dpkg -i ./com.oray.sunlogin.client_11.0.0.38604_arm64.deb  #注意此处的./<br>
接下来你可能想要向日葵的开机自启动，步骤如下：<br>
cd /home/pi/.config<br>
mkdir autostart && cd autostart<br>
cp /usr/share/applications/com.oray.sunlogin.client.desktop .<br>
cd<br>
完成！！！
