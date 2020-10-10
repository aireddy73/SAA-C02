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

On-Demand Self-Service: Provision and terminate using a UI/CLI without human interaction.
Broad Network Access: Access services over any networks on any devices using standard protocols and methods.
Resource Pooling: Economies of scale, cheaper service.
Rapid Elasticity: Scale up and down automatically in response to system load.
Measured Service: Usage is measured. Pay only for what you consume.

<h3><a id="user-content-public-vs-private-vs-multi-cloud" class="anchor" aria-hidden="true" href="#public-vs-private-vs-multi-cloud"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Public vs Private vs Multi Cloud</h3>
 
 

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
<ol>
<li>On-Demand Self-Service: Provision and terminate using a UI/CLI without
human interaction.</li>
<li>Broad Network Access: Access services over any networks on any devices using
standard protocols and methods.</li>
<li>Resource Pooling: Economies of scale, cheaper service.</li>
<li>Rapid Elasticity: Scale up and down automatically in response to system load.</li>
<li>Measured Service: Usage is measured. Pay only for what you consume.</li>
</ol>
<h3><a id="user-content-public-vs-private-vs-multi-cloud" class="anchor" aria-hidden="true" href="#public-vs-private-vs-multi-cloud"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Public vs Private vs Multi Cloud</h3>
<ul>
<li>Public Cloud: using 1 public cloud such as AWS, Azure, Google Cloud.</li>
<li>Private Cloud: using on-premises real cloud. Must meet 5 requirements.</li>
<li>Multi-Cloud: using more than 1 public cloud in one deployment.</li>
<li>Hybrid Cloud: using public and private clouds in one environment
<ul>
<li>This is <strong>NOT</strong> using Public Cloud and Legacy on-premises hardware.</li>
</ul>
</li>
</ul>
<h3><a id="user-content-cloud-service-models" class="anchor" aria-hidden="true" href="#cloud-service-models"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Cloud Service Models</h3>
<p>The <em>Infrastructure Stack</em> or <em>Application Stack</em> contains multiple components
that make up the total service. There are parts that <strong>you</strong> manage as well
as portions the <strong>vendor</strong> manages. The portions the vendor manages and you
are charged for is the <strong>unit of consumption</strong></p>
<ol>
<li>On-Premises: The individual manages all components from data to facilities.
Provides the most flexibility, but also most IT intensive.</li>
<li>Data Center Hosting: Place equipment in a building managed by a vendor.
You pay for the facilities only.</li>
<li>Infrastructure as a Service (IaaS): Vendor manages facilities and everything
else related to servers up to the OS. You pay per second or minute for the OS
used to the vendor. Lose some flexibility, but big risk reductions.</li>
<li>Platform as a Service (PaaS): Good for running an application only. The
unit of consumption is the runtime environment. You manage the application
and the data, but the vendor manges all else.</li>
<li>Software as a Service (SaaS): You consume the software as a service. This
can be Outlook or Netflix. There are almost no risks or additional costs, but
very little control.</li>
</ol>
<p>There are additional services such as <em>Function as a Service</em>,
<em>Container as a Service</em>, and <em>DataBase as a Service</em> which be explained later.</p>
<hr>
<h2><a id="user-content-aws-fundamentals" class="anchor" aria-hidden="true" href="#aws-fundamentals"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>AWS-Fundamentals</h2>
<h3><a id="user-content-aws-support-plans" class="anchor" aria-hidden="true" href="#aws-support-plans"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>AWS Support Plans</h3>
<ul>
<li>Basic (free)</li>
<li>Developer (one user, general guidance)</li>
<li>Business (multiple users, personal guidance)</li>
<li>Enterprise (Technical account manager)</li>
</ul>
<h3><a id="user-content-public-vs-private-services" class="anchor" aria-hidden="true" href="#public-vs-private-services"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Public vs Private Services</h3>
<p>Refers to the networking only, not permissions.</p>
<ul>
<li>Public Internet: AWS is a public cloud platform and connected to the public
internet. It is not on the public internet, but is next to it.</li>
<li>AWS Public Zone: Attached to the Public Internet.
S3 Bucket is hosted in the Public Zone, not all services are.
Just because you connect to a public service,
that does not mean you have permissions to access it.</li>
<li>AWS Private Zone: No direct connectivity is allowed between the AWS Private
Zone and the public cloud unless this is configured for that service.
This is done by taking a part of the private service and projecting it into the
AWS public zone which allows public internet to make inbound or outbound
connections.</li>
</ul>
<h3><a id="user-content-aws-global-infrastructure" class="anchor" aria-hidden="true" href="#aws-global-infrastructure"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a><a href="https://www.infrastructure.aws/" rel="nofollow">AWS Global Infrastructure</a></h3>
<h4><a id="user-content-regions" class="anchor" aria-hidden="true" href="#regions"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Regions</h4>
<p>AWS Region is an area of the world they have selected for a full deployment of
AWS infrastructure.</p>
<p>Areas such as countries or states</p>
<ul>
<li>Ohio</li>
<li>California</li>
<li>Singapore</li>
<li>Beijing</li>
<li>London</li>
<li>Paris</li>
</ul>
<p>AWS can only deploy regions as fast as their planning allows.
Regions are often not near their customers.</p>
<h4><a id="user-content-aws-edge-locations" class="anchor" aria-hidden="true" href="#aws-edge-locations"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>AWS Edge Locations</h4>
<p>Local distribution points. Useful for services such as Netflix so they can store
data closer to customers for low latency high speed transfers.</p>
<p>If a customer wants to access data stored in Brisbane, they will stream data
from the Sydney Region through an Edge Location hosted in Brisbane.</p>
<h4><a id="user-content-aws-management" class="anchor" aria-hidden="true" href="#aws-management"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>AWS Management</h4>
<p>Regions are connected together with high speed networking.
Some services such as EC2 need to be selected in a region.
Some services are global such as IAM</p>
<h4><a id="user-content-regions-3-benefits" class="anchor" aria-hidden="true" href="#regions-3-benefits"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Region's 3 Benefits</h4>
<ul>
<li>Geographical Separation
<ul>
<li>Useful for natural disasters</li>
<li>Provide isolated fault domain</li>
<li>Regions are 100% isolated</li>
</ul>
</li>
<li>Geopolitical Separation
<ul>
<li>Different laws change how things are accessed</li>
<li>Stability from political events</li>
</ul>
</li>
<li>Location Control
<ul>
<li>Tune architecture for performance</li>
<li>Duplicate infrastructure at closer points to customers</li>
</ul>
</li>
</ul>
<h4><a id="user-content-regions-and-azs" class="anchor" aria-hidden="true" href="#regions-and-azs"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Regions and AZs</h4>
<p>Region Name: Asia Pacific (Sydney)
Region Code: ap-southeast-2</p>
<p>AWS will provide between 2 and 6 AZs per region.
AZs are isolated compute, storage, networking, power, and facilities.
Components are allowed to distribute load and resilience by using multiple zones.</p>
<p>AZs are connected to each other with high speed redundant networks.</p>
<h4><a id="user-content-service-resilience" class="anchor" aria-hidden="true" href="#service-resilience"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Service Resilience</h4>
<ol>
<li>Globally Resilient: IAM or Route 53. No way for them to go down. Data is
replicated throughout multiple regions.</li>
<li>Region Resilient: Operate as separate services in each region. Generally
replicate data to multiple AZs in that region.</li>
<li>AZ Resilient: Run from a single AZ. It is possible for hardware to fail in an
AZ and the service to keep running because of redundant equipment, but should
not be relied on.</li>
</ol>
<h3><a id="user-content-aws-default-vpc" class="anchor" aria-hidden="true" href="#aws-default-vpc"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>AWS Default VPC</h3>
<p>VPC is a virtual network inside of AWS.
A VPC is within 1 account and 1 region which makes it regionally resilient.
A VPC is private and isolated until decided otherwise.</p>
<p>One default VPC per region. Can have many custom VPCs which are all private
by default.</p>
<h4><a id="user-content-default-vpc-facts" class="anchor" aria-hidden="true" href="#default-vpc-facts"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Default VPC Facts</h4>
<p>VPC CIDR - defines start and end ranges of the VPC.
IP CIDR of a default VPC is always: <strong>172.31.0.0/16</strong></p>
<p>Configured to have one subnet in each AZ in the region by default.</p>
<p>Subnets are given one section of the IP ranges for the default service.
In general do not use the Default VPC in a region because it is not flexible.</p>
<p>Default VPC is large because it uses the /16 range.
A subnet is smaller such as /20
The higher the / number is, the smaller the grouping.</p>
<p>Two /17's will fit into a /16, sixteen /20 subnets can fit into one /16.</p>
<h3><a id="user-content-elastic-compute-cloud-ec2" class="anchor" aria-hidden="true" href="#elastic-compute-cloud-ec2"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Elastic Compute Cloud (EC2)</h3>
<p>Default compute service. Provides access to virtual machines called instances.</p>
<p><strong>IaaS</strong> - Infrastructure as as Service</p>
<p>The unit of consumption is an instance
EC2 instance is configured to launch into a single VPC subnet.
Private service by default, public access must be configured.
The VPC needs to support public access. If you use a custom VPC then you must
handle the networking on your own.</p>
<p>EC2 deploys into one AZ. If it fails, the instance fails.</p>
<p>Different sizes and capabilities all use On-Demand Billing - Per second.
Only pay for what you consume.</p>
<p>Charge for running the instance, CPU, memory and storage.
Extra cost for any commercial software the instance deploys with.</p>
<p>Local on-host storage or <strong>Elastic Block Storage</strong></p>
<p>Pricing based on:</p>
<ul>
<li>CPU</li>
<li>Memory</li>
<li>Storage</li>
<li>Networking</li>
</ul>
<h4><a id="user-content-running-state" class="anchor" aria-hidden="true" href="#running-state"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Running State</h4>
<p>Charged for all four categories.</p>
<ul>
<li>Running on a physical host using CPU.</li>
<li>Using memory even with no processing.</li>
<li>OS is stored on disk allocated</li>
<li>Networking is always ready to transfer information.</li>
</ul>
<h4><a id="user-content-stopped-state" class="anchor" aria-hidden="true" href="#stopped-state"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Stopped State</h4>
<p>Charged for EBS storage  only.</p>
<ul>
<li>No CPU resources are being consumed</li>
<li>No memory is being used</li>
<li>Networking is not running</li>
<li>Storage is allocated to the instance for the OS.</li>
</ul>
<h4><a id="user-content-terminated-state" class="anchor" aria-hidden="true" href="#terminated-state"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Terminated State</h4>
<p>No charges, deletes the disk and prevents all future charges.</p>
<h4><a id="user-content-ami-server-image" class="anchor" aria-hidden="true" href="#ami-server-image"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>AMI (Server Image)</h4>
<p>AMI can use used to create an instance or created from an instance.
AMIs in one region are not available from other regions.</p>
<p>Contains:</p>
<ul>
<li>
<p>Permissions: control which accounts can and can't use the AMI.</p>
<ul>
<li>
<p>Public: Anyone can launch it.</p>
</li>
<li>
<p>Owner - Implicit allow, only the owner can use it  spin up new instances</p>
</li>
<li>
<p>Explicit - owner grants access to AMI for specific AWS accounts</p>
</li>
</ul>
</li>
<li>
<p>Root Volume: contain the <strong>Boot Volume</strong></p>
</li>
<li>
<p>Block Device Mapping: links the volumes that the AMI has and
how they're presented to the operating system. Determines which volume is a
boot volume and which volumes is a data volume.</p>
</li>
</ul>
<p>AMI Types:</p>
<ul>
<li>Amazon Quick Start AMIs</li>
<li>AWS Marketplace AMIs</li>
<li>Community AMIs</li>
<li>Private AMIs</li>
</ul>
<h4><a id="user-content-connecting-to-ec2" class="anchor" aria-hidden="true" href="#connecting-to-ec2"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Connecting to EC2</h4>
<ul>
<li>Windows using RDP (Remote Desktop Protocol), Port 3389</li>
<li>Linux SSH protocol, Port 22</li>
</ul>
<p>Login to the instance using an SSH key pair.
Private Key - Stored on local machine to initiate connection.
Public Key - AWS places this key on the instance.</p>
<h3><a id="user-content-s3-default-storage-service" class="anchor" aria-hidden="true" href="#s3-default-storage-service"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>S3 (Default Storage Service)</h3>
<p>Global Storage platform. Runs from all regions and is a public service.
Can be accessed anywhere from the internet with an unlimited amount of users.</p>
<p>This should be the default storage platform</p>
<p>S3 is an object storage, not file, or block storage.
You can't mount an S3 Bucket.</p>
<h4><a id="user-content-objects" class="anchor" aria-hidden="true" href="#objects"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Objects</h4>
<p>Can be thought of a file. Two main components:</p>
<ul>
<li>Object Key: File name in a bucket</li>
<li>Value: Data or contents of the object
<ul>
<li>Zero bytes to 5 TB</li>
</ul>
</li>
</ul>
<p>Other components:</p>
<ul>
<li>Version ID</li>
<li>Metadata</li>
<li>Access Control</li>
<li>Sub resources</li>
</ul>
<h4><a id="user-content-buckets" class="anchor" aria-hidden="true" href="#buckets"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Buckets</h4>
<ul>
<li>Created in a specific AWS Region.</li>
<li>Data has a primary home region. Will not leave this region unless told.</li>
<li>Blast Radius = Region</li>
<li>Unlimited number of Objects</li>
<li>Name is globally unique</li>
<li>All objects are stored within the bucket at the same level.</li>
</ul>
<p>If the objects name starts with a slash such as <code>/old/Koala1.jpg</code> the UI will
present this as a folder. In actuality this is not true, there are no folders.</p>
<h3><a id="user-content-cloudformation-basics" class="anchor" aria-hidden="true" href="#cloudformation-basics"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>CloudFormation Basics</h3>
<p>Templates can modify infrastructure to, create, update and delete.</p>
<p>Written in YAML or JSON</p>
<div class="highlight highlight-source-yaml"><pre><span class="pl-c"><span class="pl-c">#</span># This is not mandatory unless a description is added</span>
<span class="pl-ent">AWSTemplateFormatVersion</span>: <span class="pl-s"><span class="pl-pds">"</span>version date<span class="pl-pds">"</span></span>

<span class="pl-c"><span class="pl-c">#</span># Give details as to what this template does.</span>
<span class="pl-c"><span class="pl-c">#</span># If you use this section, it MUST immediately follow the AWSTemplateFormatVersion.</span>
<span class="pl-ent">Description</span>:
  <span class="pl-s">A sample template</span>

<span class="pl-c"><span class="pl-c">#</span># Can control the command line UI. The bigger your template, the more likely</span>
<span class="pl-c"><span class="pl-c">#</span># this section is needed</span>
<span class="pl-ent">Metadata</span>:
  <span class="pl-s">template metadata</span>

<span class="pl-c"><span class="pl-c">#</span># Prompt the user for more data. Name of something, size of instance,</span>
<span class="pl-c"><span class="pl-c">#</span># data validation</span>
<span class="pl-ent">Parameters</span>:
  <span class="pl-s">set of parameters</span>

<span class="pl-c"><span class="pl-c">#</span># Another optional section. Allows lookup tables, not used often</span>
<span class="pl-ent">Mappings</span>:
  <span class="pl-s">set of mappings</span>

<span class="pl-c"><span class="pl-c">#</span># Decision making in the template. Things will only occur if a condition is met.</span>
<span class="pl-c"><span class="pl-c">#</span># Step 1: create condition</span>
<span class="pl-c"><span class="pl-c">#</span># Step 2: use the condition to do something else in the template</span>
<span class="pl-ent">Conditions</span>:
  <span class="pl-s">set of conditions</span>

<span class="pl-ent">Transform</span>:
  <span class="pl-s">set of transforms</span>

<span class="pl-c"><span class="pl-c">#</span># The only mandatory field of this section</span>
<span class="pl-ent">Resources</span>:
  <span class="pl-s">set of resources</span>

<span class="pl-c"><span class="pl-c">#</span># Once the template is finished it can return data or information.</span>
<span class="pl-c"><span class="pl-c">#</span># Could return the admin or setup address of a word press blog.</span>
<span class="pl-ent">Outputs</span>:
  <span class="pl-s">set of outputs</span></pre></div>
<h4><a id="user-content-resources" class="anchor" aria-hidden="true" href="#resources"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Resources</h4>
<p>An example which creates an EC2 instance</p>
<div class="highlight highlight-source-yaml"><pre><span class="pl-ent">Resources</span>:
  <span class="pl-ent">Instance</span>: <span class="pl-c"><span class="pl-c">#</span># Logical Resource</span>
    <span class="pl-ent">Type</span>: <span class="pl-s"><span class="pl-pds">'</span>AWS::EC2::Instance<span class="pl-pds">'</span></span> <span class="pl-c"><span class="pl-c">#</span># This is what will be created</span>
    <span class="pl-ent">Properties</span>: <span class="pl-c"><span class="pl-c">#</span># Configure the resources in a particular way</span>
      <span class="pl-ent">ImageId</span>: <span class="pl-s">!Ref LatestAmiId</span>
      <span class="pl-ent">Instance Type</span>: <span class="pl-s">!Ref Instance Type</span>
      <span class="pl-ent">KeyName</span>: <span class="pl-s">!Ref Keyname</span></pre></div>
<p>Once a template is created, AWS will make a stack. This is a living and active
representation of a template. One template can create infinite amount of stacks.</p>
<p>For any <strong>Logical Resources</strong> in the stack,
CF will make a corresponding <strong>Physical Resources</strong> in your AWS account.</p>
<p>It is cloud formations job to keep the logical and physical resources in sync.</p>
<p>A template can be updated and then used to update the same stack.</p>
<h3><a id="user-content-cloudwatch-basics" class="anchor" aria-hidden="true" href="#cloudwatch-basics"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>CloudWatch Basics</h3>
<p>Collects and manages operational data on your behalf.</p>
<p>Three products in one</p>
<ul>
<li>Metrics: data relating to AWS products, apps, on-prem solutions</li>
<li>Logs: collection, monitoring</li>
<li>Events: event hub
<ul>
<li>If an AWS service does something, CW events can perform another action</li>
<li>Generate an event to do something at a certain time of day or time of week.</li>
</ul>
</li>
</ul>
<h4><a id="user-content-namespace" class="anchor" aria-hidden="true" href="#namespace"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Namespace</h4>
<p>Container for monitoring data.
Naming can be anything so long as it's not <code>AWS/service</code> such as <code>AWS/EC2</code>.
This is used for all metric data of that service</p>
<h4><a id="user-content-metric" class="anchor" aria-hidden="true" href="#metric"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Metric</h4>
<p>Time ordered set of data points such as:</p>
<ul>
<li>CPU Usage</li>
<li>Network IN/OUT</li>
<li>Disk IO</li>
</ul>
<p>This is not for a specific server. This could get things from different servers</p>
<p>Anytime CPU Utilization is reported, the <strong>datapoint</strong> will report</p>
<ul>
<li>Timestamp = 2019-12-03</li>
<li>Value = 98.3</li>
</ul>
<p><strong>Dimensions</strong> separate data points for different <strong>things</strong> or
<strong>perspectives</strong> within the same metric</p>
<h4><a id="user-content-alarms" class="anchor" aria-hidden="true" href="#alarms"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Alarms</h4>
<p>Has two states <code>ok</code> or <code>alarm</code>.State can send an SNS or action.
Third state can be insufficient data state. Not a problem, just wait.</p>
<h3><a id="user-content-shared-responsibility-model" class="anchor" aria-hidden="true" href="#shared-responsibility-model"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Shared Responsibility Model</h3>
<p>AWS: Responsible for security <strong>OF</strong> the cloud</p>
<p>Customer: Responsible for security <strong>IN</strong> the cloud</p>
<h3><a id="user-content-high-availability-ha-fault-tolerance-ft-and-disaster-recover-dr" class="anchor" aria-hidden="true" href="#high-availability-ha-fault-tolerance-ft-and-disaster-recover-dr"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>High Availability (HA), Fault-Tolerance (FT), and Disaster Recover (DR)</h3>
<h4><a id="user-content-high-availability-ha" class="anchor" aria-hidden="true" href="#high-availability-ha"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>High Availability (HA)</h4>
<ul>
<li>Aims to <strong>ensure</strong> an agreed level of operational <strong>performance</strong>, usually
<strong>uptime</strong>, for a <strong>higher than normal period</strong></li>
<li>Instead of diagnosing the issue, swap it out.</li>
<li>Redundant hardware to minimize downtown</li>
<li>User disruption is not ideal, but is allowed
<ul>
<li>The user might need to log back in or lose some data on their screen.</li>
</ul>
</li>
<li>Maximizing a system's uptime
<ul>
<li>99.9% (Three 9's) = 8.7 hours downtime per year.</li>
<li>99.999 (Five 9's) = 5.26 minutes downtime per year.</li>
</ul>
</li>
</ul>
<h4><a id="user-content-fault-tolerance-ft" class="anchor" aria-hidden="true" href="#fault-tolerance-ft"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Fault-Tolerance (FT)</h4>
<ul>
<li>System can <strong>continue operating properly</strong>
in the event of the <strong>failure of some</strong> (one or more faults within) of its
<strong>components</strong></li>
<li>Fault tolerance is much more complicated than high availability and more
expensive. Outages must be minimized and the system needs levels of
redundancy.</li>
<li>An airplane is an example of system that needs Fault Tolerance. It has
more engines than it needs for redundancy.</li>
</ul>
<p>Example:
A patient is waiting for a life saving surgery and is under anesthetic.
While being monitored, the life support system is dosing medicine.
This type of system cannot only be highly available, even a movement of
interruption is deadly.</p>
<h4><a id="user-content-disaster-recover-dr" class="anchor" aria-hidden="true" href="#disaster-recover-dr"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Disaster Recover (DR)</h4>
<ul>
<li>Set of policies, tools and procedures to <strong>enable the recovery</strong> or
<strong>continuation</strong> of <strong>vital</strong> technology infrastructure and systems
<strong>following a natural or human-induced disaster</strong>.</li>
<li>DR can largely be automated to eliminate the time for recovery and errors.</li>
</ul>
<p>This involves:</p>
<ul>
<li>Pre-planning
<ul>
<li>Ensure plans are in place for extra hardware</li>
<li>Do not store backups at the same site as the system</li>
</ul>
</li>
<li>DR Processes
<ul>
<li>Cloud machines ready when needed</li>
</ul>
</li>
</ul>
<p>This is designed to keep the crucial and non replaceable parts of the
system in place.</p>
<h3><a id="user-content-domain-name-system-dns" class="anchor" aria-hidden="true" href="#domain-name-system-dns"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Domain Name System (DNS)</h3>
<p>DNS is a discovery service. Translates machines into humans and vice-versa.
It is a huge database and has to be distributed.</p>
<p>Parts of the DNS system</p>
<ul>
<li>DNS Client: Piece of software running on the OS for a device you're using.</li>
<li>Resolver: Software on your device or server which queries DNS on your behalf.</li>
<li>Zone: A part of the DNS database.
<ul>
<li>This would be <a href="http://www.amazon.com" rel="nofollow">www.amazon.com</a></li>
<li>What the data is, the substance</li>
</ul>
</li>
<li>Zonefile: physical database for a zone
<ul>
<li>How physically that data is stored</li>
</ul>
</li>
<li>Nameserver: where zonefiles are hosted</li>
</ul>
<p>Steps:</p>
<p>Find the Nameserver which hosts a particular Zonefile.
Query that Nameserver for a record with that Zone.
It then passes the information back to the client.</p>
<h4><a id="user-content-dns-root" class="anchor" aria-hidden="true" href="#dns-root"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>DNS Root</h4>
<p>The starting point of DNS.
DNS names are read right to left with multiple parts separated by periods.</p>
<p><code>www.netflix.com.</code></p>
<p>The period is assumed to be there in a browser when it's not present.
The DNS Root is hosted on DNS Root Servers (13). These are hosted
by 12 major companies.</p>
<p><strong>Root Hints</strong> is a pointer to the DNS Root server</p>
<p>Process</p>
<ol>
<li>DNS client asks DNS Resolver for IP address of a given DNS name.</li>
<li>Using the Root Hints file, the DNS Resolver communicates with one or
more of the root servers to access the root zone and begin the process
of finding the IP address.</li>
</ol>
<p>The Root Zone is organized by IANA (Internet Assigned Numbers Authority).
Their job is to manage the contents of the root zone. IANA is in charge
of the DNS system because they control the root zone.</p>
<h4><a id="user-content-dns-hierarchy" class="anchor" aria-hidden="true" href="#dns-hierarchy"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>DNS Hierarchy</h4>
<p>Assuming a laptop is querying DNS directly for <a href="http://www.amazon.com" rel="nofollow">www.amazon.com</a> and using
a root hints file to know how to access a root server and query the root zone.</p>
<ul>
<li>When something is trusted in DNS, it is an <strong>authority</strong>.</li>
<li>One piece can be authoritative for root.</li>
<li>One piece can be authoritative for amazon.com</li>
<li>The root zone is the start and the only thing trusted in DNS.</li>
<li>The root zone can delegate a part of itself to another zone or entity.</li>
<li>That someone else then becomes authoritative for that piece of itself only.</li>
<li>The root zone is just a database of the top level domains.</li>
</ul>
<p>The top level domains are the only things to the left of the DNS name.</p>
<ul>
<li><code>.com</code> or <code>.org</code> are generic top level domains (GTLD)</li>
<li><code>.uk</code> is a country code top level domains (CCTLD)</li>
</ul>
<p><strong>Registry</strong> maintains the zones for a TLD (e.g .ORG)
<strong>Registrar</strong> has relationships with the .org TLD zone manager
allowing domain registration</p>
<h3><a id="user-content-route53-fundamentals" class="anchor" aria-hidden="true" href="#route53-fundamentals"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Route53 Fundamentals</h3>
<ul>
<li>Registers domains</li>
<li>Can Host Zone Files on managed nameservers</li>
<li>This is a global service, no need to pick a region</li>
<li>Globally Resilience
<ul>
<li>Can operate with failure in one or more regions</li>
</ul>
</li>
</ul>
<h4><a id="user-content-register-domains" class="anchor" aria-hidden="true" href="#register-domains"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Register Domains</h4>
<p>Has relationships with all major registries</p>
<ul>
<li>Route 53 will check with the top level domain to see if the name is available</li>
<li>Router 53 creates a zonefile for the domain to be registered</li>
<li>Allocates nameservice for that zone
<ul>
<li>Generally four of these for one individual zone</li>
<li>This is a hosted zone</li>
<li>The zone file will be put on these four managed nameservers</li>
</ul>
</li>
<li>Router 53 will communicate with the <code>.org</code> registry and add the nameserver
records into the zone file for the top level domain.
<ul>
<li>This is done with a nameserver record.</li>
</ul>
</li>
</ul>
<h4><a id="user-content-route53-details" class="anchor" aria-hidden="true" href="#route53-details"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Route53 Details</h4>
<p><strong>Zonefiles</strong> in AWS
Hosted on four managed name servers</p>
<ul>



   
