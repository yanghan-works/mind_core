---
tags: 
alias: 
date: 2025-08-02 13:58
---

---

## 基础安全原则

- [[最小权限原则]]

- [[及时更新与打补丁]]

- [[强密码策略]]

- [[定期备份]]



## 用户与认证安全

- [[用户账户安全]] (禁用root直登, 限制sudo权限)

- [[密码策略与复杂度]]

- [[SSH 密钥认证]]

- [[多因素认证 (MFA)]]

- [[PAM 配置]]



## 文件系统安全

- [[文件权限管理]] (umask, chmod, chown)

- [[特殊权限风险]] (SUID, SGID)

- [[文件完整性检查]] (checksum, AIDE)

- [[磁盘加密]]



## 网络安全

- [[防火墙配置]] (iptables, firewalld, UFW)

- [[端口扫描与关闭不必要端口]]

- [[禁用不安全服务]]

- [[VPN (虚拟专用网络)]]

- [[入侵检测系统 (IDS)]] (Snort, Suricata)

- [[入侵防御系统 (IPS)]]



## SELinux 与 AppArmor

- [[SELinux 概述]]

- [[SELinux 模式与策略]]

- [[AppArmor 概述]]

- [[SELinux/AppArmor 配置与故障排除]]



## 审计与日志

- [[系统日志监控]] (journalctl, rsyslog)

- [[审计日志 (Auditd)]]

- [[安全事件响应]]



## 安全审计与合规性

- [[Linux 审计系统 (Auditd)]]

- [[安全合规性标准]] (如 CIS Benchmarks)



## 入侵检测与响应

- [[IDS/IPS 概述]]

- [[安全事件响应流程]]



## 恶意软件防护

- [[Linux 病毒与恶意软件]]

- [[ClamAV]] (杀毒软件)



## 其他安全实践

- [[安全加固脚本]]

- [[容器安全]] (Docker Security)

- [[容器镜像安全]]

- [[内核安全模块]]