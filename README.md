# Elevate_Labs_Task_1
1.find out Local ip range <br>
Command: nmap -sn 172.22.34.67/24 <br>
Description:-sn: Ping scan — discover live hosts without port scanning.<br>
Output-Link:https://github.com/varsha-asawale2010/Elevate_Labs_Task_1/blob/main/Scan_report.html
<br>
2. TCP SYN Scan<br>
Command: nmap -sS 172.22.34.67/24<br>
Description:The -sS option in Nmap stands for a TCP SYN scan, also called a half-open scan.<br>
Output-Link:
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

