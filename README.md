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

<p align="center">
<img src="https://i.imgur.com/3d3CEwZ.png" height="85%" width="85%" alt="RDP event fail logs to iP Geographic information"/>
</p>
<h2>Languages Used</h2>

- <b>PowerShell:</b> Extract RDP failed logon logs from Windows Event Viewer 

<h2>Utilities Used</h2>

- <b>ipgeolocation.io:</b> IP Address to Geolocation API

<h2>Attacks from only USA and Russia coming in; Custom logs being output with geodata</h2>

<p align="center">
<img src="https://i.imgur.com/LhDCRz4.jpeg" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<h2>World map of incoming attacks after 24 hours (built custom logs including geodata)</h2>

<p align="center">
<img src="https://i.imgur.com/krRFrK5.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
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
