在树梅派上如何实现无公网IP的访问，向日葵作为一款好用的远控软件，但可惜的是没有对树梅派进行适配，这个deb包是一位大佬在向日葵官方包的基础上修改得来。
环境要求：
raspberrypi   arm64位操作系统   且必须用debain的源，不得替换为raspberry的源
sudo apt update && sudo apt upgrade
sudo apt install git 
git clone 项目地址
cd raspberry_arm64_sunclient
sudo dpkg -i ./com.oray.sunlogin.client_11.0.0.38604_arm64.deb  #注意此处的./
接下来你可能想要向日葵的开机自启动，步骤如下：
cd /home/pi/.config
mkdir autostart && cd autostart
cp /usr/share/applications/com.oray.sunlogin.client.desktop .
cd
完成！！！
