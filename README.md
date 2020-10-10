# SAA-C02
AWS Certified Solutions Architect - Associate

SAA-C02 Notes
These are my personal notes from Adrian Cantrill's (SAA-C02) course. Learning Aids from aws-sa-associate-saac02. There may be errors, so please purchase his course to get the original content and show support https://learn.cantrill.io.

<h2><a id="user-content-table-of-contents" class="anchor" aria-hidden="true" href="#table-of-contents"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Table of Contents</h2>
<ul>
<li><a href="#Cloud-Computing-Fundamentals">Cloud-Computing-Fundamentals</a></li>
<li><a href="#AWS-Fundamentals">AWS-Fundamentals</a></li>
<li><a href="#IAM-Accounts-AWS-Organizations">IAM-Accounts-AWS-Organizations</a></li>
<li><a href="#Simple-Storage-Service-S3">Simple-Storage-Service-S3</a></li>
<li><a href="#Virtual-Private-Cloud-VPC">Virtual-Private-Cloud-VPC</a></li>
<li><a href="#Elastic-Cloud-Compute-EC2">Elastic-Cloud-Compute-EC2</a></li>
<li><a href="#Containers-and-ECS">Containers-and-ECS</a></li>
<li><a href="#Advanced-EC2">Advanced-EC2</a></li>
<li><a href="#Route-53">Route-53</a></li>
<li><a href="#Relational-Database-Service-RDS">Relational-Database-Service-RDS</a></li>
<li><a href="#Network-Storage-EFS">Network-Storage-EFS</a></li>
<li><a href="#HA-and-Scaling">HA-and-Scaling</a></li>
<li><a href="#Serverless-and-App-Services">Serverless-and-App-Services</a></li>
<li><a href="#CDN-and-Optimization">CDN-and-Optimization</a></li>
<li><a href="#Advanced-VPC">Advanced-VPC</a></li>
<li><a href="#Hybrid-and-Migration">Hybrid-and-Migration</a></li>
<li><a href="#Security-Deployment-Operations">Security-Deployment-Operations</a></li>
<li><a href="#NoSQL-and-DynamoDB">NoSQL-and-DynamoDB</a></li>
</ul>
<hr>
<h2><a id="user-content-cloud-computing-fundamentals" class="anchor" aria-hidden="true" href="#cloud-computing-fundamentals"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Cloud-Computing-Fundamentals</h2>
<p>Cloud computing provides</p>


<h3><a id="user-content-public-vs-private-vs-multi-cloud" class="anchor" aria-hidden="true" href="#public-vs-private-vs-multi-cloud"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Public vs Private vs Multi Cloud</h3>
 
 




   
