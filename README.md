# My_VPN
My personal VPN setup on EC2&amp;Bandwagon

## Setup L2TP/IPsec on Bandwagon VPS
<ol>
<li>After bought KVM VPS from Bandwagon, write down the SSH port and root password for future login.</li>
<li>For OS X users, use "terminal" to login remote VPS. An example is shown in following picture.
  <img src="https://github.com/CapSOSkw/My_VPN/blob/master/pic/Screen%20Shot%202018-10-29%20at%2017.15.21.png" alt="drawing" width="600"/></li>
<li>Then we will successfully log into VPS.</li>
<li>Follow the instructions from <a href="https://github.com/hwdsl2/setup-ipsec-vpn/blob/master/README-zh.md">"SETUP-IPSEC-VPN"</a>. VPN is ready!</li>
  </ol>
  
## Setup ShadowsocksR server on Bandwagon VPS
<ol>
  <li>After entering the VPS, we are going to firstly enable BBR service provided by Google.</li>
  <li>By using command, the script is downloaded.
    
```bash
wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh"
```
  </li>
  <li> Then enter the commands, and follow the instructions shown in your screen. 
  
  ```bash
  chmod +x tcp.sh
  bash tcp.sh
  ```
  Once BBR is installed and VPS is reboot, you have to enable BBR service which is option 3.
  <img src="https://github.com/CapSOSkw/My_VPN/blob/master/pic/Screen%20Shot%202018-10-29%20at%2017.51.56.png" alt="pic2" width="600" />
  </li>
<li> After finishing BBR, we are going to install ShadowsocksR(SSR) server by using following command.
  
  ```bash
  wget -N --no-check-certificate https://raw.githubusercontent.com/ToyoDAdoubi/doubi/master/ssr.sh && chmod +x ssr.sh && bash ssr.sh
  ```
  <img src="https://github.com/CapSOSkw/My_VPN/blob/master/pic/Screen%20Shot%202018-10-29%20at%2017.59.03.png" alt="pic2" width="600"/>
</li>  
<li>Following the instructions, you will set up port (0~2333), encryption method, password, etc. Once all parameters setup, VPN is ready!</li>
<li>For Windows users, download SSR client from <a href="https://github.com/shadowsocksrr/shadowsocksr-csharp/releases">"Windows SSR client"</a>.</li>
<li>For OSX users, download SSR client from <a href="https://github.com/shadowsocks/ShadowsocksX-NG/releases">"MAC SSR client"</a>.</li>
</ol>

