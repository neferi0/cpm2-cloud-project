<p align="center">
<img src="https://upload.wikimedia.org/wikipedia/commons/9/93/Amazon_Web_Services_Logo.svg" height="25%" width="35%"/>
</p>

<h1> Creating Secure Private Cloud Environment: Second Milestone </h1>
This is a walkthrough on how I created a Cloud Environment that was secured through a Virtual Private Cloud.<br/>


<h2> Software & Technologies Used</h2>

- Amazon Web Services (Virtual Machines/Cloud Platform)
  
<h2>Steps</h2>
<h3 align="center">Security Groups and Outbound Rules</h3>
<br />
<p>
<h3 align="center">For this portion of the course project, I started by creating 2 security groups for both of my subnets so that I can control the inbound and outbound traffic from within the VPC. The specific rule that I wanted to enable for the VPC is allowing SSH traffic between the two subnets, and to do this we made sure that the instances had the same connectivity requirements in place. I first added inbound rules to security group 1 that allowed instances in subnet A from any range within my own network (See Figure 1). I then did the same for subnet B, but the only difference was that the subnet would allow instances from B and allow communication between A and B instances. (See Figure 2). For the outbound rules, both are left to the default to allow any connections to both ports (See Figure 3).
</p>
<p>
    <img src="https://i.imgur.com/hCtGUuP.png" height="65%" width="75%" />
</p>
<p>
    <img src="https://i.imgur.com/JokWpOX.png" height="65%" width="75%" />
</p>
<br />
<p>
    <img src="https://i.imgur.com/jE3MIy1.png" height="65%" width="75%" />  
</p>
<h3 align="center">Network ACLs and User Groups</h3>
<br />
<p>
<h3 align="center">). For the next portion, I created a Network Access Control List so that I could filter the inbound and outbound traffic on a subnet level, but I left it at the default for now and will most likely configure it in Milestone 5 in the testing phase (See Figure 4). To provide least privilege principles, I utilized Amazon Identity and Access Management rules to establish an administrative, development, and an operations group and granted them access to different aspects of the VPC to ensure that the risk of attackers gaining access to any critical systems is severely reduced (See Figure 5).
<p>
<br />
   <img src="https://i.imgur.com/XhlFVcX.png" height="65%" width="75%" />
</p>
<br />
<br />
<p>
  <img src="https://i.imgur.com/RDMgAzq.png" height="65%" width="75%" />
</p>
<br />
<br />
<h3 align="center">This concludes the second milestone </h3>
