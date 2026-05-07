# linux-firewall-lab
Linux iptables防火墙实验：NAT伪装、最小权限策略、内网流量控制
# Linux iptables 内网流量控制实验

## 实验目标
在虚拟化环境中配置Linux网关，使用iptables实现NAT地址转换、内网访问控制和最小权限策略。

## 核心实践
- **NAT配置**：通过POSTROUTING链配置MASQUERADE规则，实现内网主机对外网的访问与IP隐藏
- **访问控制**：使用INPUT/OUTPUT/FORWARD链配置过滤规则，基于"最小权限原则"限制SSH等通信
- **网络调试**：使用ip route、ping、ssh等工具排查路由、连通性和防火墙规则顺序问题

## 实验环境
- VMware虚拟机（四台：网关M2 + 内网主机M1、M4 + 外网主机M3）
- Linux系统（Ubuntu 20.04）
- iptables、ip route

## 实验报告
详见仓库中的 [基于Linux iptables的内网流量控制实验.docx]
## 关键收获
- 掌握iptables规则顺序对策略生效的决定性影响
- 理解企业网络中NAT和最小权限原则的实际落地方式
- 积累网络分层故障排查经验（服务层→网络层→防火墙层）
- 本实验为合肥工业大学《网络信息安全》课程实验，由我独立完成
