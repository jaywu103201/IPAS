#
```

```


# iptables 參數
```
Usage: iptables -[ACD] chain rule-specification [options]
 iptables -I chain [rulenum] rule-specification [options]
 iptables -R chain rulenum rule-specification [options]
 iptables -D chain rulenum [options]
 iptables -[LS] [chain [rulenum]] [options]
 iptables -[FZ] [chain] [options]
 iptables -[NX] chain
 iptables -E old-chain-name new-chain-name
 iptables -P chain target [options]
 iptables -h (print this help information)

Commands:
Either long or short options are allowed.
 --append -A chain Append to chain
 --check -C chain Check for the existence of a rule
 --delete -D chain Delete matching rule from chain
 --delete -D chain rulenum
 Delete rule rulenum (1 = first) from chain
 --insert -I chain [rulenum]
 Insert in chain as rulenum (default 1=first)
 --replace -R chain rulenum
 Replace rule rulenum (1 = first) in chain
 --list -L [chain [rulenum]]
 List the rules in a chain or all chains
 --list-rules -S [chain [rulenum]]
 Print the rules in a chain or all chains
 --flush -F [chain] Delete all rules in chain or all chains
 --zero -Z [chain [rulenum]]
 Zero counters in chain or all chains
 --new -N chain Create a new user-defined chain
 --delete-chain
 -X [chain] Delete a user-defined chain
 --policy -P chain target
 Change policy on chain to target
 --rename-chain
 -E old-chain new-chain
 Change chain name, (moving any references)
Options:
 --ipv4 -4 Nothing (line is ignored by ip6tables-restore)
 --ipv6 -6 Error (line is ignored by iptables-restore)
[!] --protocol -p proto protocol: by number or name, eg. `tcp'
[!] --source -s address[/mask][...]
 source specification
[!] --destination -d address[/mask][...]
 destination specification
[!] --in-interface -i input name[+]
 network interface name ([+] for wildcard)
 --jump -j target
 target for rule (may load target extension)
 --goto -g chain
 jump to chain with no return
 --match -m match
 extended match (may load extension)
 --numeric -n numeric output of addresses and ports
[!] --out-interface -o output name[+]
 network interface name ([+] for wildcard)
 --table -t table table to manipulate (default: `filter')
 --verbose -v verbose mode
 --wait -w [seconds] maximum wait to acquire xtables lock before give up
 --wait-interval -W [usecs] wait time to try to acquire xtables lock
 default is 1 second
 --line-numbers print line numbers when listing
 --exact -x expand numbers (display exact values)
[!] --fragment -f match second or further fragments only
 --modprobe=<command> try to insert modules using this command
 --set-counters PKTS BYTES set the counter during insert/append
[!] --version -V print package version.
-I, –insert chain [rulenum] rule-specification ： -I 代表 insert 的意思，新增一個 rule ，

第一個參數會 chain 的名稱
第二個參數為 rule 的順序，預設值為 1 ，如果你指定為 1 ，那麼新的 rule 會放在列表的最上頭。
範例： sudo iptables -I INPUT 1 -j ACCEPT
-j, –jump target ：當封包符合這個 rule ，透過 -j 的指示，將這個封包丟到指定的 chain 去決定下一個行為。
我們可以使用指令 ” sudo iptables -N newChain “，來建立一新的 chain 叫 “newChain” ，
再透過 -j newChain ，將封包下一步的行為傳到這個新的 chain 來決定，

例如下面這個範例，我將 80 port 的所有封包丟給 newChain 來決定要怎麼處理，”newChain” 裡面再指定 “-j REJECT”， 
REJECT 是一個預設的 Rule Target ，代表拒絕這個封包。
```
