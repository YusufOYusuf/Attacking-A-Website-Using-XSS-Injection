<h1>Attacking A Website Using XSS Injection</h1>


<h2>Description</h2>
In this lab, I learned to attack a website using cross-site scripting (XSS) injection. XSS injection is malicious content sent to the web browser. These contents are often of a segment of JavaScript, HTML, Flash, or any other type of code that the browser may execute. The attacks include transmitting private data, like cookies or other session information, to the attacker. It can redirect the victim to the web content controlled by the attacker or can perform other malicious operations on the user's machine under the guise of the vulnerable site.
<br />



<h2>Environments Used </h2>

- <b>Kali GNU/Linux Rolling</b> 

<h2>Utilities and Language </h2>

- <b>DVWA</b>

<h2>Program walk-through:</h2>

<p align="center">
From the left sidebar open Firefox ESR <br/>
<img src="https://i.postimg.cc/cJKxYX9Y/Screen-Shot-2022-12-28-at-4-10-26-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />
  
  
  
  
  
<br />
Type "http://localhost/dvwa/login.php" in the address bar then type in username and password <br/>
<br />
Scroll down and select DVWA Security  <br/>
<img src="https://i.postimg.cc/1t5KJVFp/Screen-Shot-2022-12-28-at-4-15-09-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />



<br />
In the DVWA Security window select a "low" security level and then click submit.  <br/>
<img src="https://i.postimg.cc/nVwCs9c6/Screen-Shot-2022-12-28-at-4-19-41-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />




<br />
In the left pane click "XSS (Reflected)"
<img src="https://i.postimg.cc/bNVJwpnY/Screen-Shot-2022-12-28-at-6-36-22-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />






<br />
In the whats your name textbox type "(<)body onload=alert('uCertify')(>)'" and then click submit
<img src="https://i.postimg.cc/QxWfmk3p/Screen-Shot-2022-12-28-at-6-43-42-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />



<br />
Again in the Whats your name textbox type "(<)script(>)alert(document.cookie)(<)/script(>) and then click submit and then go to XSS (stored) in the left pane
<img src="https://i.postimg.cc/JhvNs06R/Screen-Shot-2022-12-28-at-6-51-17-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />





<br />
Type the "ucian1" for the name texbox and then "(<)script(>)alert("uCertify"(<)/script(>)"
<img src="https://i.postimg.cc/NftjgtxS/Screen-Shot-2022-12-28-at-6-55-44-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />





<br />
Type the "ucian2" for the name texbox and then "(<)body onload=alert(document.location(>)"
<img src="https://i.postimg.cc/SKdWGVxN/Screen-Shot-2022-12-28-at-6-57-32-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />








