# RPL-IOT-Project
Implémentation et évaluation d'un module de sécurité pour le Routage RPL dans IOT
<h1>RPL-Security-IoT </h1>
<br>
<h2>Description</h2>
This project focuses on evaluating the resilience of the RPL routing protocol in IoT networks against a black hole attack. Using Contiki Cooja, we simulated the RPL protocol, generated a black hole attack, and collected performance metrics such as delay, PDR, overhead, and energy consumption. The results helped assess the impact of the attack and identify the security vulnerabilities of RPL.


<h2>Utilities Used</h2>
<b>Contiki-</b>
<b>Cooja-</b>
<b>VirtualBox</b>


<h2>Walkthrough</h2>
<h3>Installation</h3>
1- Install Contiki 3.0 From the url : https://sourceforge.net/projects/contiki/
<br>
2- Install VirtualBox From the url : https://www.virtualbox.org/wiki/Downloads
<br>
3- Add Contiki to VirtualBox :
<br>
<img src="https://imgur.com/HbOjhzl.png"  height="80%" width="80%" alt="landing page"/>
<br>
<img src="https://imgur.com/xouHEw6.png"  height="80%" width="80%" alt="landing page"/>
<br>
<img src="https://imgur.com/j3aIzRn.png"  height="80%" width="80%" alt="landing page"/>
<br>
<img src="https://imgur.com/j3aIzRn.png"  height="80%" width="80%" alt="landing page"/>
<br>
4- Install Cooja dependencies :
<img src="https://imgur.com/HzdkcDx.png"  height="80%" width="80%" alt="landing page"/>
<br>
5- Starting Cooja :
<img src="https://imgur.com/s9qqzzH.png"  height="80%" width="80%" alt="landing page"/>
<br>
<h3>Execution of the RPL protocol</h3>
  - Add the root node (sync).
<br>
  - Add the sender nodes.
<br>
  - Open the Collect-View.
<br>
  - Start the network simulation.
 <br>
 <img src="https://imgur.com/sFaVBsr.png"  height="80%" width="80%" alt="landing page"/>
<br>
After a few minutes, all the information characterizing the network can be seen in the Collect-View:
 <br>
 <img src="https://imgur.com/wO7t9YT.png"  height="80%" width="80%" alt="landing page"/>
 <img src="https://imgur.com/3j9Ik8I.png"  height="80%" width="80%" alt="landing page"/>
  <img src="https://imgur.com/yW6ObxG.png"  height="80%" width="80%" alt="landing page"/>
  <img src="https://imgur.com/jInC4W6.png"  height="80%" width="80%" alt="landing page"/>
  <img src="https://imgur.com/2mRLSn8.png"  height="80%" width="80%" alt="landing page"/>
  <img src="https://imgur.com/boM625U.png"  height="80%" width="80%" alt="landing page"/>
<br>
<h3>Evaluation with existing metrics</h3>
- <b>Delay :</b><br>
The "Delay" metric is used to evaluate the time required to transmit packets between nodes in a network. It measures the packet propagation time and helps select the fastest or least congested routes. However, the specific method of measuring delay can vary depending on the protocol implementation. Other metrics, such as cost, reliability, or energy consumption, may also be considered when choosing the best route in low-power, low-consumption networks.
<br>
  <img src="https://imgur.com/yb7owV7.png"  height="80%" width="80%" alt="landing page"/>
<br>
<b>Packet Delivery Ratio: </b><br>
PDR is a metric that measures the success rate of packet delivery in a network. It represents the percentage of packets that successfully reach their destination from the source node. A high PDR indicates better communication quality. This metric is used to assess network efficiency, detect connectivity issues, and enhance communication reliability.
<br><br>
<b>Overhead:</b><br>
Overhead refers to the additional load or extra cost introduced in a communication system. It measures the amount of extra data needed to perform a specific operation or function
<br><br>
<b>Energy:</b> <br>
it measures the energy consumption in a communication system, which is crucial for optimizing energy efficiency, extending device lifespan, and ensuring the sustainable operation of
low-power networks.
<br><br>
  <img src="https://imgur.com/HqI18aO.png"  height="80%" width="80%" alt="landing page"/>
<br>
<h3>Blackhole Attack Procedure:</h3>
<br>
- Add the malicious node that will carry out the attack.
<br>
- Start the simulation and begin collecting data.
<br>
  <img src="https://imgur.com/m30sBUS.png"  height="80%" width="80%" alt="landing page"/>
<br>
We can observe that only 8 nodes are executing the protocol (out of 11), while the others are blocked by the malicious node, resulting in traffic being diverted and creating a "black hole.
<br>
<h3>Proposed Solutions</h3>
<br>
<b>Using an AI Model:</b> <br>
    Implementing an artificial intelligence model can help detect early signs of a black hole attack, such as abnormal traffic flows or a sudden increase in the number of requests. This enables preventive measures to be taken to counter the attack before it can cause damage.
<br><br>
<b>Data Encryption:</b><br>
    Encrypting sensitive data is a solution to counter black hole attacks, ensuring that the information cannot be compromised even if intercepted by the attacker.
    <br><br>
<b>Using a Dynamic Server:</b><br>
    Utilizing a dynamic server allows for real-time modification of communication routes to bypass nodes or links potentially compromised by a black hole attack. This approach minimizes the effects of the attack by redirecting traffic to secure paths.
