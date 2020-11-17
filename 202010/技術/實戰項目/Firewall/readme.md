# 實測:
```
使用 iptables 防禦 syn flood 攻擊


```

# 學習目標
```


```

# 系統環境

![FIREWALL.jpg](FIREWALL.jpg)

# 測試步驟
```


```
### SYN Flood(洪水) 攻擊
```
原理:

攻擊測試指令:

hping3 -S -p 80 --flood 10.0.2.6

```
### 防火牆規則
```
        iptables -N SYNFLOOD
        iptables -A SYNFLOOD -p tcp --syn -m limit --limit 50/s -j RETURN
        iptables -A SYNFLOOD -p tcp -j LOG --log-level alert
        iptables -A SYNFLOOD -p tcp -j REJECT --reject-with tcp-reset
        iptables -A INPUT -p tcp -m state --state NEW -j SYNFLOOD
```
