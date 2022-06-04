<h1>Failed RDP to IP Geolocation Information</h1>

<h2>Description</h2>
<b>The Powershell script in this repository is from @joshmadakor1 and this script parses out Windows Event Log information for failed RDP attacks. Thereafter, it uses a third party API (ipgeolocation.io) to collect geographic information about the attackers location.
</b>
<br />
<br />
Following Josh's Youtube Tutorial, I setup Azure Sentinel (SIEM) and connected it to a live virtual machine acting as a honey pot.
I allowed it to receive live attacks (RDP Brute Force) from all around the world for 24 hours. I then used Josh's custom PowerShell script to look up the attackers' Geolocation information and plot it on an Azure Sentinel Map.
<br />
<br />

<h2>Languages Used</h2>

- <b>PowerShell:</b> Extract RDP failed logon logs from Windows Event Viewer 

<h2>Utilities Used</h2>

- <b>ipgeolocation.io:</b> IP Address to Geolocation API

<h2>Attacks from only USA and Russia coming in; Custom logs being output with geodata</h2>

<p align="center">
<img width="1135" alt="Powershell screenshot" src="https://user-images.githubusercontent.com/106617464/171990547-91162824-9097-470c-b8c3-34caba107ea1.png">

</p>

<h2>World map of incoming attacks after 24 hours (built custom logs including geodata)</h2>
<b>I used the free version of the geolocation API which has a daily request limit of 1000 requests. It seems that the attacks came from 5 main IP addresses and were from USA and Russia
</b>
<p align="center">
<img width="720" alt="World map attacks" src="https://user-images.githubusercontent.com/106617464/171990612-328ebd1f-c28a-405c-9415-3a070b5e9965.png">
</p>


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
