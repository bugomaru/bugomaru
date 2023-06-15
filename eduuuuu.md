proxies:
- name: hheheh
  server: 172.67.73.39
  port: 443
  type: trojan
  password: cffc48c0-0b8f-11ee-b7b1-1239d0255272
  skip-cert-verify: true
  sni: sg-2.test3.net
  network: ws
  ws-opts:
    path: /howdy
    headers:
      Host: sg-2.test3.net
  udp: true
