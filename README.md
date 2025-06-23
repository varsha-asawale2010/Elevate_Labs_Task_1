# Elevate_Labs_Task_1
1.find out Local ip range <br>
Command: nmap -sn 172.22.34.67/24 <br>
Description:-sn: Ping scan — discover live hosts without port scanning.<br>
Output-Link:https://github.com/varsha-asawale2010/Elevate_Labs_Task_1/blob/main/Scan_report.html
<br>
2. TCP SYN Scan<br>
Command: nmap -sS 172.22.34.67/24<br>
Description:The -sS option in Nmap stands for a TCP SYN scan, also called a half-open scan.<br>
Output-Link:https://github.com/varsha-asawale2010/Elevate_Labs_Task_1/blob/main/Scan_report1.html
<!DOCTYPE html>
<html>
<head>
  <tittle>Some Ip address and their open ports</tittle>
</head>
<body>
  <h2>Ip address and open ports</h2>
  <table border="1">
    <tr>
      <th>Ip Address</th>
      <th>Port</th>
      <th>State</th>
      <th>services</th>
    </tr>
    <tr>
      <td>172.22.34.1</td>
      <td>23/tcp <br>80/tcp</td>
      <td>open</td>
       <td>telnet<br> http</td>
    <tr>
      <td>172.22.34.3</td>
      <td>80/tcp<br>443/tcp<br>554/tcp <br>8000/tcp<br></td>
      <td>open</td>
      <td>http<br>https<br>rtsp<br>http-alt</td>
       </tr>
    <tr>
    <td>172.22.34.20</td>
    <td>
    135/tcp <br>139/tcp<br>445/tcp<br>3389/tcp<br>7070/tcp</td>
    <td>open</td>
    <td>msrpc<br>netbios-ssn<br>microsoft-ds<br>ms-wbt-server<br> realserver
    </td>
  </tr>
  <tr>
  <td> 172.22.34.12</td>
<td>135/tcp<br> 139/tcp<br>445/tcp <br> 3389/tcp</td>
<td>open</td>  
<td>msrpc
<br>  netbios-ssn
 <br>  microsoft-ds
<br>  ms-wbt-server
</td>
</tr>
<td> 172.22.34.58
</td>
<td>
1521/tcp <br>3306/tcp</td><td>open </td> 
   <td> oracle<br>
    mysql</td></tr>
    <tr>
      <td>172.22.34.53
      </td>
<td>10001/tcp</td><td>open</td>  <td> scp-config</td>
    </tr> 
  <tr>
  <td> 172.22.34.54</td>
<td>
3389/tcp </td><td>open</td> <td> ms-wbt-server</td></tr>
  <tr><td> 172.22.34.64</td>
<td>5357/tcp</td><td>open</td>
<td> wsdapi</td></tr>
  <tr>
  <td>172.22.34.65</td> <td>1027/tcp</td><td>open</td><td>IIS</td></tr>
  <tr><td>172.22.34.72</td>
  <td>2869/tcp</td>
    <td>open</td>
  <td>icslap</td></tr>
  <tr>
  <td>
   172.22.34.111
  </td><td>
135/tcp <br> 5357/tcp<br>49152/tcp</td> <td>open</td> <td>  msrpc<br>  wsdapi
<br> unknown</td></tr>
  <tr>
  <td>172.22.34.254</td>
<td>80/tcp<br> 554/tcp </td> <td>open</td><td> http
<br> rtsp</td></tr>
  <tr>
  <td>
   172.22.34.67</td>
<td>5357/tcp<br>16992/tcp</td>
<td>open</td> <td>  wsdapi<br>  amt-soap-http</td>
  </tr></table>
</body>
</html>

Analyze Packet using wireshark:
Apply Display Filters:<br>
ip.addr == 192.168.146.65 <br>
tcp.port == 80<br> 
![image](https://github.com/user-attachments/assets/952092ba-ca75-4a8d-9935-f578c4cc3551)


<pre>Port Service Name    Common Use<br>
21	ftp	     File Transfer Protocol
22	ssh	     Secure Shell (remote login)
23	telnet	     Remote terminal access (insecure)
80	http	     Web server (insecure)
135	msrpc        Microsoft RPC
139	netbios-ssn  Windows file/printer sharing (NetBIOS)
443	https  	     Secure web server
445	microsoft-ds Microsoft file sharing (SMB over TCP)
554	rtsp	     Real Time Streaming Protocol
1027	IIS	     Microsoft IIS alternate port (dynamic)
2869	icslap	     Windows Service Location Protocol
2968	enpp	    Encrypted Network Protocol Port
3306	mysql	    MySQL database
3389	ms-wbt-server	Microsoft Remote Desktop (RDP)
3580	nati-svrloc	Cisco NAC (used for device management)
49152+	unknown	        Dynamic/ephemeral ports (Windows services)
5357	wsdapi	Web Services for Devices API (Windows)
5432	postgresql	PostgreSQL database
7070	realserver	RealMedia streaming
8000	http-alt	Alternate HTTP port
8443	https-alt	Alternate HTTPS port
9010	sdr	Software Defined Radio (custom use)
10001	scp-config	Secure Copy Config (varies by vendor)
1521	oracle	Oracle database
2179	vmrdp	Remote Desktop (Hyper-V virtual machines)
8080	http-proxy	Common for proxy or alternative HTTP server
16992	amt-soap-http	Intel Active Management Technology (AMT)</pre>

Open Ports & Their Security Risks <br>
1. 21/FTP	:Transmits credentials in plaintext; vulnerable to brute force, sniffing, and anonymous login misuse.<br>
2. 23/Telnet:	Unencrypted and outdated; allows credential sniffing and unauthorized remote access.<br>
3. 80/HTTP:	Unencrypted; vulnerable to MITM (Man-in-the-Middle), session hijacking, and outdated web exploits.<br>
4. 443/HTTPS:	Safer than HTTP, but weak SSL/TLS configurations or expired certificates are a risk.<br>
5. 135/MSRPC:	Can be exploited for Windows enumeration, used in lateral movement and DCOM/RPC-based attacks.<br>
6. 139/NetBIOS-SSN:	Supports SMB over NetBIOS; prone to information leakage and LLMNR poisoning.<br>



