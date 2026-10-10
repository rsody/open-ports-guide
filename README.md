# Open Ports Guide · 포트별 보안 가이드

Plain-language reference for the TCP ports people most often find open on their routers, servers, NAS boxes and IoT devices: what listens there, what goes wrong when it is exposed to the internet, and how to close it.

자주 열려 있는 TCP 포트가 무엇이고, 인터넷에 열려 있으면 어떤 위험이 있으며, 어떻게 닫는지 정리한 참고 목록입니다.

Full guides (with real incidents, CVEs, checklists and copy-paste firewall commands) live at **[portscan.co.kr/ports](https://portscan.co.kr/en/ports/)**, available in English, 한국어, 日本語 and 中文. To check whether a port is actually reachable from the outside, use **[PortScan](https://portscan.co.kr/en/)**, a free online port checker that opens real TCP connections and reports open, closed or filtered.

## English

| Port | Service | Category | Exposure risk |
|---|---|---|---|
| [21](https://portscan.co.kr/en/ports/21) | FTP | File transfer | High |
| [22](https://portscan.co.kr/en/ports/22) | SSH | Remote access | Medium |
| [23](https://portscan.co.kr/en/ports/23) | Telnet | Remote access | High |
| [25](https://portscan.co.kr/en/ports/25) | SMTP | Mail | Medium |
| [53](https://portscan.co.kr/en/ports/53) | DNS | Network infrastructure | Medium |
| [80](https://portscan.co.kr/en/ports/80) | HTTP | Web | Low |
| [110](https://portscan.co.kr/en/ports/110) | POP3 | Mail | Medium |
| [135](https://portscan.co.kr/en/ports/135) | MS-RPC | Windows | High |
| [143](https://portscan.co.kr/en/ports/143) | IMAP | Mail | Medium |
| [443](https://portscan.co.kr/en/ports/443) | HTTPS | Web | Low |
| [445](https://portscan.co.kr/en/ports/445) | SMB | Windows | High |
| [554](https://portscan.co.kr/en/ports/554) | RTSP (IP cameras / CCTV) | Video & IoT | High |
| [1433](https://portscan.co.kr/en/ports/1433) | MS SQL Server | Database | High |
| [1723](https://portscan.co.kr/en/ports/1723) | PPTP VPN | VPN | Medium |
| [1883](https://portscan.co.kr/en/ports/1883) | MQTT | Video & IoT | High |
| [2375](https://portscan.co.kr/en/ports/2375) | Docker API | Container | High |
| [3306](https://portscan.co.kr/en/ports/3306) | MySQL / MariaDB | Database | High |
| [3389](https://portscan.co.kr/en/ports/3389) | RDP (Remote Desktop) | Remote access | High |
| [5000](https://portscan.co.kr/en/ports/5000) | Synology DSM (NAS admin interface) | NAS | High |
| [5432](https://portscan.co.kr/en/ports/5432) | PostgreSQL | Database | High |
| [5900](https://portscan.co.kr/en/ports/5900) | VNC | Remote access | High |
| [6379](https://portscan.co.kr/en/ports/6379) | Redis | Database | High |
| [8080](https://portscan.co.kr/en/ports/8080) | HTTP alternate port | Web | Medium |
| [8123](https://portscan.co.kr/en/ports/8123) | Home Assistant | Video & IoT | Medium |
| [9200](https://portscan.co.kr/en/ports/9200) | Elasticsearch | Database | High |
| [11211](https://portscan.co.kr/en/ports/11211) | Memcached | Database | High |
| [25565](https://portscan.co.kr/en/ports/25565) | Minecraft (Java Edition) server | Game server | Medium |
| [27017](https://portscan.co.kr/en/ports/27017) | MongoDB | Database | High |
| [32400](https://portscan.co.kr/en/ports/32400) | Plex Media Server | Media server | Medium |

## 한국어

| 포트 | 서비스 | 분류 | 노출 위험 |
|---|---|---|---|
| [21](https://portscan.co.kr/ports/21) | FTP | 파일 전송 | 높음 |
| [22](https://portscan.co.kr/ports/22) | SSH | 원격 접속 | 중간 |
| [23](https://portscan.co.kr/ports/23) | Telnet | 원격 접속 | 높음 |
| [25](https://portscan.co.kr/ports/25) | SMTP | 메일 | 중간 |
| [53](https://portscan.co.kr/ports/53) | DNS | 네트워크 기반 | 중간 |
| [80](https://portscan.co.kr/ports/80) | HTTP | 웹 | 낮음 |
| [110](https://portscan.co.kr/ports/110) | POP3 | 메일 | 중간 |
| [135](https://portscan.co.kr/ports/135) | MS-RPC | 윈도우 | 높음 |
| [143](https://portscan.co.kr/ports/143) | IMAP | 메일 | 중간 |
| [443](https://portscan.co.kr/ports/443) | HTTPS | 웹 | 낮음 |
| [445](https://portscan.co.kr/ports/445) | SMB | 윈도우 | 높음 |
| [554](https://portscan.co.kr/ports/554) | RTSP (IP 카메라·CCTV) | 영상·IoT | 높음 |
| [1433](https://portscan.co.kr/ports/1433) | MS SQL Server | 데이터베이스 | 높음 |
| [1723](https://portscan.co.kr/ports/1723) | PPTP VPN | VPN | 중간 |
| [1883](https://portscan.co.kr/ports/1883) | MQTT | 영상·IoT | 높음 |
| [2375](https://portscan.co.kr/ports/2375) | Docker API | 컨테이너 | 높음 |
| [3306](https://portscan.co.kr/ports/3306) | MySQL / MariaDB | 데이터베이스 | 높음 |
| [3389](https://portscan.co.kr/ports/3389) | RDP (원격 데스크톱) | 원격 접속 | 높음 |
| [5000](https://portscan.co.kr/ports/5000) | Synology DSM (NAS 관리 화면) | NAS | 높음 |
| [5432](https://portscan.co.kr/ports/5432) | PostgreSQL | 데이터베이스 | 높음 |
| [5900](https://portscan.co.kr/ports/5900) | VNC | 원격 접속 | 높음 |
| [6379](https://portscan.co.kr/ports/6379) | Redis | 데이터베이스 | 높음 |
| [8080](https://portscan.co.kr/ports/8080) | HTTP 대체 포트 | 웹 | 중간 |
| [8123](https://portscan.co.kr/ports/8123) | Home Assistant | 영상·IoT | 중간 |
| [9200](https://portscan.co.kr/ports/9200) | Elasticsearch | 데이터베이스 | 높음 |
| [11211](https://portscan.co.kr/ports/11211) | Memcached | 데이터베이스 | 높음 |
| [25565](https://portscan.co.kr/ports/25565) | Minecraft (Java Edition) 서버 | 게임 서버 | 중간 |
| [27017](https://portscan.co.kr/ports/27017) | MongoDB | 데이터베이스 | 높음 |
| [32400](https://portscan.co.kr/ports/32400) | Plex Media Server | 미디어 서버 | 중간 |

인터넷에 열려 있으면 안 되는 포트(위험 "높음"): 21, 23, 135, 445, 554, 1433, 1883, 2375, 3306, 3389, 5000, 5432, 5900, 6379, 9200, 11211, 27017.

## Quick checks · 빠른 점검

1. **Check from outside.** Testing from inside your own network never passes through the router's firewall. Use an external checker such as [PortScan](https://portscan.co.kr/en/).
2. **Review your router.** Look at the port-forwarding list, the DMZ setting and the UPnP mappings. Most unexpected open ports come from one of these three.
3. **Prefer a VPN to exposing admin interfaces.** RDP (3389), SMB (445), databases (3306/5432/6379/27017) and NAS/camera admin pages (5000/554) should sit behind a VPN such as WireGuard or Tailscale, not be forwarded directly.

1. **밖에서 확인하세요.** 같은 네트워크 안에서 확인하면 공유기 방화벽을 거치지 않습니다.
2. **공유기 설정을 점검하세요.** 포트포워딩 목록, DMZ, UPnP 세 곳을 봅니다.
3. **관리 화면은 VPN 뒤에 두세요.** 원격 데스크톱, SMB, DB, NAS·CCTV 관리 화면은 포트포워딩 대신 VPN으로 접속하세요.

## License

Text © PortScan, licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). You may reuse it with attribution and a link to the original guide.
