port: 7890
socks-port: 7891
redir-port: 7892
mixed-port: 7893
tproxy-port: 7895
ipv6: false
mode: global
log-level: silent
allow-lan: true
external-controller: 0.0.0.0:9090
secret: ""
bind-address: "*"
unified-delay: true
profile:
  store-selected: true
dns:
  enable: true
  ipv6: false
  enhanced-mode: redir-host
  listen: 0.0.0.0:7874
  nameserver:
    - 8.8.8.8
    - 1.0.0.1
    - https://dns.google/dns-query
  fallback:
    - 1.1.1.1
    - 8.8.4.4
    - https://cloudflare-dns.com/dns-query
    - 112.215.203.254
  default-nameserver:
    - 8.8.8.8
    - 1.1.1.1
    - 112.215.203.254
proxies:
  - name: natanvpnn
    server: 104.17.3.81
    port: 80
    type: vmess
    uuid: c09751b6-b6c0-4a52-9b22-bc30625a7aa7
    alterId: 0
    cipher: auto
    tls: false
    skip-cert-verify: true
    servername: dox2.natanvpn.xyz
    network: ws
    ws-opts:
      path: /vmess
      headers:
        Host: dox2.natanvpn.xyz
    udp: true
rules:
  - MATCH,FASTSSH-SSHKIT-HOWDY
