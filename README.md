![Rerechan02 card name](https://cardivo.vercel.app/api?name=Rerechan02『𝐅𝐍』&description=Hi,%20everyone!%20and%20Nice%20to%20meet%20you%20%F0%9F%91%8B&image=https://raw.githubusercontent.com/Rerechan02/simple-xray/main/funny1.jpg?v=4&backgroundColor=%23ecf0f1&telegram=/&github=Rerechan02&pattern=leaf&colorPattern=%23eaeaea)

## 程序包结构： 
  
 ``` 
 ├── bin 
 │   └── apibox 
 ├── conf 
 │   ├── ssl_cert.crt (默认不存在) 
 │   ├── ssl_cert.key (默认不存在) 
 │   ├── config.json 
 │   └── mime.types 
 ├── log 
 ├── pkg 
 ├── static 
 │   ├── images 
 │   └── scripts 
 └── template 
  
  
 运行环境要求： 
  
 1、Linux Kernel 3.x/x86_64 及更高版本 
 2、建议 Linux 发行版 CentOS 7.0+ / Ubuntu 14.04+ 
 3、启用支持 SSL/TLS 模式访问时，需要生成对应的 SSL 证书文件且放置到 "conf" 文件夹下并配置 "conf.json" 文件 
 4、客户端要求使用 IE9、Chrome 40、Firefox 38、Safari 9 或更高版本的浏览器访问 
 5、服务器端需要对防火墙开启对应的外部访问端口。具体需要开放的端口请参考 "conf" 文件夹下的 "conf.json" 文件中的端口部分的配置 
 6、本程序只能对 Unix/Linux 类的操作系统，且支持 SSH 协议的 OS 进行远程操作 
 7、基于Go1.6+，原生支持 http2  
  
  
 一、部署 
 1、将程序解压或下载至任一目录，运行 "build.sh" 编译可执行文件 
 2、然后运行 "bin" 文件夹下的 "apibox" 文件即可。如:"./apibox start/stop" 
 3、配置文件在 "conf" 文件夹下，核心配置文件为 "conf.json"，部署的时候需要添加跨域白名单来支持其他机器的访问 
 4、后台运行可以配置 "conf" 文件夹下的 "conf.json" 文件,将 "daemon" 项配置为 "true"  
 5、运行时日志文件存放在 "log" 文件夹下，以当天时期命名 
 6、也可以配置程序以 Nginx 的 fcgi 模式运行,以 Nginx 做为访问入口 
 ```
 
 ### Features 
 * tls1.3 + http2 + quic 
 * autocert(Let's Encrypt) support 
 * plain http2 support 
 * tls termination 
 * sni routing 
 * forward chain 
 * global dns cache 
 * custom dns server support 
 * dns over tls support 
 * hosts file support 
 * flexible auth 
 * outbound ip address support 
 * tls prober mitigation 
 * pac file with china_ip_list 
 * country/region bypass rules 
 * traffic metrics 
 * pprof/expvar handler 
 * graceful reload
 * websocket http + https
 * reverense proxy
 * Supporting reverse-proxy, 7 load-balancing algorithms in goproxy: Random, IP Hash, Round Robin, Weight Round Robin, Power of Two Choices (P2C), Consistent Hashing with Bounded Loads, Least Load 
 * Supporting GET/POST/PUT/DELETE Methods in http and CONNECT method in https in goproxy 
 * Supporting HTTP authentication 
 * Filtering and blocking specific http requests and even rewriting them in goproxy 
 * Customizing responses from third-party API 
 * Cache support with memory or Redis to speed up the responding and the expired time of caches is configurable 
 * Flexible and eager-loading configurations 
  
 
 ### What can it do? 
 - Chained proxies, the program itself can be used as an proxies, and if it is set up, it can be used as a secondary proxies or even an N-level proxies. 
 - Communication encryption, if the program is not a level one proxies, and the upper level proxies is also the program, then the communication between the upper level proxies and the upper level proxies can be encrypted, and the underlying tls high-intensity encryption is used, and the security is featureless. 
 - Smart HTTP, SOCKS5 proxy, will automatically determine whether the visited website is blocked. If it is blocked, it will use the upstream proxies (provided that the upstream proxies is configured) to access the website; if the visited website is not blocked, in order to speed up the access, the proxies will Direct access to the website without using a upstream proxies. 
 - Domain name black and white list, more free to control the way the website is accessed. 
 - Cross-platform, whether you are windows, linux, mac, or even raspberry pie, you can run the proxy very well. 
 - Multi-protocol support, support for HTTP(S), TCP, UDP, Websocket, SOCKS5 proxy. 
 - TCP/UDP port forwarding. 
 - Support intranet penetration, protocol supports TCP and UDP. 
 - SSH relay, HTTP (S), SOCKS5 proxy supports SSH relay, the upper Linux server does not need any server, a local proxy can be happy online. 
 - [KCP](https://github.com/xtaci/kcp-go) protocol support, HTTP(S), SOCKS5, SPS proxy supports KCP protocol to transmit data, reduce latency and improve browsing experience. 
 - Dynamic selection of upstream proxies, through the external API, HTTP (S), SOCKS5, SPS proxies can achieve user-based or IP-based speed limit, connection limit, dynamic access to upstream. 
 - Flexible upstream allocation, HTTP(S), SOCKS5 proxy can implement user- or IP-based speed limit, connection limit, and upper-level through configuration files. 
 - Transparent HTTP (S) proxy, in conjunction with iptables, forwards the outgoing 80, 443 traffic directly to the proxy at the gateway, enabling non-aware intelligent router proxy. 
 - Protocol conversion, which can convert existing HTTP(S) or SOCKS5 or SS proxy into one port and support HTTP(S) and SOCKS5 and SS proxy at the same time. Converted SOCKS5 and SS proxy. If the upstream is SOCKS5 proxy, then UDP is supported. Features while supporting powerful cascading authentication. 
 - Custom underlying encrypted transmission, http(s)\sps\socks proxy can encrypt tcp data via tls standard encryption and kcp protocol on top of tcp, in addition to support custom encryption after tls and kcp, that is Said custom encryption and tls|kcp can be used in combination, the internal AES256 encryption, you only need to define a password when you use it. 
 - Underlying compression efficient transmission, http(s)\sps\socks proxy can encrypt tcp data through custom encryption and tls standard encryption and kcp protocol on tcp, and can also compress data after encryption, that is, compression function And custom encryption and tls|kcp can be used in combination. 
 - Secure DNS proxy, which can secure and prevent pollution DNS queries through encrypted proxy communication between the DNS proxy server provided by the local proxy and the upstream proxy. 
 - Load balancing, high availability, HTTP(S)\SOCKS5\SPS proxies supports upstream load balancing and high availability, and multiple upstream repeat-P parameters can be used. 
 - Specify the egress IP. The HTTP(S)\SOCKS5\SPS\TCP proxy supports the client to connect with the ingress IP, and uses the ingress IP as the egress IP to access the target website. If the ingress IP is an intranet IP, the egress IP does not use the ingress IP. 
 - Support speed limit, HTTP(S)\SOCKS5\SPS\TCP proxy supports speed limit. 
 - SOCKS5 proxies supports cascading certification. 
 - The certificate parameter uses base64 data. By default, the -C, -K parameter is the path of the crt certificate and the key file. If it is the beginning of base64://, then the latter data is considered to be base64 encoded and will be used after decoding. 
 - Support client IP black and white list, more secure control of client access to proxy service, if black and white list is set at the same time, then only whitelist is effective. Socks / HTTP(S) / SPS / TCP / UDP / DNS / intranet NAT The bridge/intranet NAT the tbridge and supports the client IP black and white list. 
 - Range ports listen on, HTTP(S)\SOCKS5\SPS\TCP proxy supports port range listening, avoiding starting too many processes and improving performance. 
  
 ### Why do you need it? 
  
 - When for some reason we are unable to access our services elsewhere, we can establish a secure tunnel to access our services through multiple connected proxy nodes. 
 - WeChat interface is developed locally for easy debugging. 
 - Remote access to intranet machines. 
 - Play LAN games with your friends. 
 - I used to play only on the LAN, and now I can play anywhere. 
 - Replace the sword inside Netnet, show IP internal Netcom, peanut shell and other tools. 
 - .. 
  
  
 The manual on this page applies to the latest version of goproxy. Other versions may not be applicable. Please use the command according to your own instructions.
 
 
 ## 🎉 How to use goproxy 
  
 ### 1.Get source code 
  
 ```
( Coming Soon )
 ``` 
  
 **Besides, you also need a Redis to support caching responses if you enable Redis config in goproxy.** 
  
 ### 2.Compile the source code 
  
 ```powershell 
 cd $GOPATH/src/github.com/( soon )
  
 go build 
 ``` 
  
 ### 3.Run 
  
 goproxy uses cfg.toml as its configurations file which is located in `/etc/proxy/cfg.toml` of your server, you should create a cfg.toml in there previously, here is a typical example: 
  
 ```toml 
 # toml file for goproxy 
  
 title = "TOML config for goproxy" 
  
 [server] 
 port = ":8080" 
 reverse = true 
 proxy_pass = ["127.0.0.1:6000"] 
 # 0 - random, 1 - loop, 2 - power of two choices(p2c), 3 - hash, 4 - consistent hashing, 5 - least load 
 inverse_mode = 2 
 auth = false 
 cache = true 
 cache_timeout = 60 
 cache_type = "redis" 
 log = 1 
 log_path = "./logs" 
 user = { agent = "proxy" } 
 http_read_timeout = 10 
 http_write_timeout = 10 
  
 [redis] 
 redis_host = "localhost:6379" 
 redis_pass = "" 
 max_idle = 5 
 idle_timeout = 10 
 max_active = 10 
  
 [mem] 
 capacity = 1000 
 cache_replacement_policy = "LRU" 
 ``` 
  
 ### Configurations： 
 #### [server] 
 - **port**：the port goroxy will listen to 
 - **reverse**：enable the reverse-proxy feature or not 
 - **proxy_pass**：back-end servers that actually provide services, like ["127.0.0.1:80^10","127.0.0.1:88^5","127.0.0.1:8088^2","127.0.0.1:8888"], weight can be assigned to every single server 
 - **inverse_mode**：load-balancing algoritms：0 for Randomized Algorithm； 1 for Weight Round Robin Algorithm； 2 for Power of Two Choices (P2C) Algorithm； 3 for IP Hash Algorithm based on hash ring； 4 for Consistent Hashing with Bounded Loads Algorithm 
 - **auth**：enable http authentication or not 
 - **cache**：enable responses caching or not 
 - **cache_timeout**：expired time of responses caching, in seconds 
 - **cache_type**: redis or memory 
 - **log**：log level, 1 for Debug，0 for info 
 - **log_path**：the path of log files 
 - **user**：user name from http authentication 
 - **http_read_timeout**：duration for waiting response from the back-end server, if goproxy don't get the response after this duration, it will throw an exception 
 - **http_write_timeout**：duration for back-end server writing response to goproxy, if back-end server takes a longer time than this duration to write its response into goproxy, goproxy will throw an exception 
  
 #### [redis] 
 - **redis_host**：redis host 
 - **redis_pass**：redis password 
 - **max_idle**：the maximum idle connections of redis connection pool 
 - **idle_timeout**：duration for idle redis connection to close 
 - **max_active**：maximum size of redis connection pool 
  
 #### [mem] 
  
 - **capacity**: cache capacity of items 
 - **cache_replacement_policy**: LRU or LFU 
  
 There should be a binary named `goproxy` as the same of project name after executing the `go build` command and that binary can be run directly to start a goproxy server. 
  
 The running goproxy server listens in the port set in cfg.toml and it will forward your http requests to the back-end servers set in cfg.toml by going through that port in goproxy


```markdown
# 隧道协议和服务器设置指南

## 目录
- [介绍](#介绍)
- [隧道协议](#隧道协议)
  - [SSH 隧道](#ssh-隧道)
  - [VPN 隧道](#vpn-隧道)
  - [HTTPS 隧道](#https-隧道)
- [服务器设置](#服务器设置)
- [系统要求](#系统要求)
- [使用方法](#使用方法)
- [故障排除](#故障排除)
- [参考文献](#参考文献)

## 介绍
此存储库提供了有关各种隧道协议以及如何在Linux VPS（虚拟专用服务器）上设置隧道服务器的全面指南。隧道协议允许您安全地路由网络流量，访问远程服务器或保护您的互联网连接。

## 隧道协议
### SSH 隧道
SSH 隧道允许您通过SSH连接创建安全通道，可用于网络流量重定向、远程服务器访问或互联网流量加密。

#### 配置示例
要创建SSH隧道服务器，请在您的Linux服务器上配置`/etc/ssh/sshd_config`文件以允许`AllowTcpForwarding yes`选项。然后，使用以下客户端命令作为示例：

```bash
ssh -L <本地端口>:<目标>:<目标端口> 用户@ssh服务器
```

### VPN 隧道
VPN 隧道允许在公共网络上建立安全的网络连接。通常用于远程访问公司网络或隐藏您的IP地址。

#### 配置示例
要使用OpenVPN创建VPN服务器，需要配置OpenVPN配置文件并生成所需的密钥和证书。详细的配置示例可以在OpenVPN文档中找到。

### HTTPS 隧道
HTTPS 隧道允许您通过HTTPS协议创建加密连接，通常用于隐藏Web流量。

#### 配置示例
要使用Stunnel创建HTTPS隧道服务器，需要配置Stunnel配置文件，将特定端口连接到目标服务器通过HTTPS。

## 服务器设置
在`server-setup`目录中，您将找到有关设置每种上述协议的隧道服务器的详细说明和脚本。

## 系统要求
要在Linux VPS上运行隧道服务器，您应该满足以下系统要求：

| 系统            | 支持的   | 测试过的 | 最低      | 推荐       |
|-----------------|---------|----------|----------|------------|
| 虚拟化          | KVM     | KVM      | KVM      | KVM        |
| CPU架构         | amd64   | amd64    | amd64    | amd64      |
| 操作系统        | Debian 10、Ubuntu 20.04 | Debian 10、Ubuntu 20.04 | Debian 10 | Debian 10  |
| 操作系统架构    | 64位     | 64位     | 64位     | 64位       |
| CPU             | -       | 1核      | 1核      | 2核或更多   |
| 内存            | -       | 512MB    | 1GB      | 2GB或更多   |
| 存储            | -       | 20GB     | 15GB     | 20GB或更多  |
| 网络            | 1xIPv4、禁用IPv6、开放端口 | 1xIPv4、禁用IPv6、开放端口 | 1xIPv4、禁用IPv6、开放端口 | 1xIPv4、禁用IPv6、开放端口 |
| ISP             | AWS Lightsail、DigitalOcean、Linode、等等 | AWS Lightsail | - | - |

请确保满足与您打算配置的隧道协议相对应的系统要求。同时，确保您具有管理员（root）权限以配置隧道服务器。

## 使用方法
您可以在此存储库中各个协议目录中找到详细的使用说明和示例。

## 故障排除
如果遇到任何问题或错误，请参考各隧道协议文档中的故障排除部分。

## 参考文献
- [OpenSSH文档](https://www.openssh.com/)
- [OpenVPN文档](https://openvpn.net/index.php/open-source.html)
- [Stunnel文档](https://www.stunnel.org/)

## Contact
- [Rerechan02](mailto:widyabakti02@gmail.com)
- [![Email](https://img.shields.io/badge/Email-widyabakti02%40gmail.com-blue?style=flat-square)](mailto:widyabakti02@gmail.com)
- License: [Creative Commons](https://mirrors.creativecommons.org/presskit/icons/cc.svg)
