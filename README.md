# SAA-C02
AWS Certified Solutions Architect - Associate

SAA-C02 Notes
These are my personal notes from Adrian Cantrill's (SAA-C02) course. Learning Aids from aws-sa-associate-saac02. There may be errors, so please purchase his course to get the original content and show support https://learn.cantrill.io
 ****I am working on customized notes for myself for future reference.****
 

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
<li>Can be <strong>public</strong> or <strong>private</strong></li>
</ul>
<h3><a id="user-content-dns-record" class="anchor" aria-hidden="true" href="#dns-record"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>DNS Record</h3>
<ul>
<li>Nameserver (NS): Allows delegation to occur in the DNS.</li>
<li>A and AAAA Records: Maps the host to a v4 or v6 host type. Most of the time
you will make both types of record, A and AAAA.</li>
<li>CNAME Record Type: Allows DNS shortcuts to reduce admin overhead.
CNAMES cannot point directly at an IP address and only another name.</li>
<li>MX records: How emails are sent. They have two main parts:
<ul>
<li>Priority: Lower values for the priority field are higher priority.</li>
<li>Value
<ul>
<li>If it is just a host, it will not have a dot on the right. It is assumed
to be part of the same zone as the host.</li>
<li>If you include a dot on the right, it is a <em><strong>fully qualified domain name</strong></em></li>
</ul>
</li>
</ul>
</li>
<li>TXT Record: Allows you to add arbitrary text to a domain.
One common usage is to prove domain ownership.</li>
</ul>
<h4><a id="user-content-ttl---time-to-live" class="anchor" aria-hidden="true" href="#ttl---time-to-live"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>TTL - Time To Live</h4>
<p>This is a numeric setting on DNS records in seconds.
Allows the admin to specify how long the query can be stored
at the resolver server.
If you need to upgrade the records, it is smart to lower the TTL value first.</p>
<p>Getting the answer from an Authoritative Source is known as an
<strong>Authoritative Answer</strong>.</p>
<p>If another client queries the same thing, they will get back a
<strong>Non-Authoritative</strong> response.</p>
<hr>
<h2><a id="user-content-iam-accounts-aws-organizations" class="anchor" aria-hidden="true" href="#iam-accounts-aws-organizations"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>IAM-Accounts-AWS-Organizations</h2>
<h3><a id="user-content-iam-identity-policies" class="anchor" aria-hidden="true" href="#iam-identity-policies"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>IAM Identity Policies</h3>
<p>Identity Policies are attached to AWS Identities which are
IAM users, IAM groups, and IAM roles. These are a set of security statements
that ALLOW or DENY access to AWS resources.</p>
<p>When an identity attempts to access AWS resources, that identity needs
to prove who it is to AWS, a process known as <strong>Authentication</strong>.
Once authenticated, that identity is known as an <strong>authenticated identity</strong></p>
<h4><a id="user-content-statement-components" class="anchor" aria-hidden="true" href="#statement-components"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Statement Components</h4>
<ul>
<li>Statement ID (SID): Optional field that should help describe
<ul>
<li>The resource you're interacting</li>
<li>The actions you're trying to perform</li>
</ul>
</li>
<li>Effect: is either <code>allow</code> or <code>deny</code>.
<ul>
<li>It is possible to be allowed and denied at the same time</li>
</ul>
</li>
<li>Action are formatted <code>service:operation</code>. There are three options:
<ul>
<li>specific individual action</li>
<li>wildcard as an action</li>
<li>list of multiple independent actions</li>
</ul>
</li>
<li>Resource: similar to action except for format <code>arn:aws:s3:::catgifs</code></li>
</ul>
<h4><a id="user-content-priority-level" class="anchor" aria-hidden="true" href="#priority-level"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Priority Level</h4>
<ul>
<li>Explicit Deny: Denies access to a particular resource cannot be overruled.</li>
<li>Explicit Allow: Allows access so long there is not an explicit deny.</li>
<li>Default Deny (Implicit): IAM identities start off with no resource access.</li>
</ul>
<h4><a id="user-content-inline-policies-and-managed-policies" class="anchor" aria-hidden="true" href="#inline-policies-and-managed-policies"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Inline Policies and Managed Policies</h4>
<ul>
<li>Inline Policy: grants access and assigned on each accounts individually.</li>
<li>Managed Policy (best practice): one policy is applied to all users at once.</li>
</ul>
<h3><a id="user-content-iam-users" class="anchor" aria-hidden="true" href="#iam-users"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>IAM Users</h3>
<p>Identity used for anything requiring <strong>long-term</strong> AWS access</p>
<ul>
<li>Humans</li>
<li>Applications</li>
<li>Service Accounts</li>
</ul>
<p>If you can name a thing to use the AWS account, this is an IAM user.</p>
<p>When a <strong>principal</strong> wants to <strong>request</strong> to perform an action,
it will <strong>authenticate</strong> against an identity within IAM. An IAM user is an
identity which can be used in this way.</p>
<p>There are two ways to authenticate:</p>
<ul>
<li>Username and Password</li>
<li>Access Keys (CLI)</li>
</ul>
<p>Once the <strong>Principal</strong> has authenticated, it becomes an <strong>authenticated identity</strong></p>
<h4><a id="user-content-amazon-resource-name-arn" class="anchor" aria-hidden="true" href="#amazon-resource-name-arn"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Amazon Resource Name (ARN)</h4>
<p>Uniquely identify resources within any AWS accounts.</p>
<p>This allows you to refer to a single or group of resources.
This prevents individual resources from the same account but in
different regions from being confused.</p>
<p>ARN generally follows the same format:</p>
<div class="highlight highlight-source-shell"><pre>arn:partition:service:region:account-id:resource-id
arn:partition:service:region:account-id:resource-type/resource-id
arn:partition:service:region:account-id:resource-type:resource-id</pre></div>
<ul>
<li>partition: almost always <code>aws</code> unless it is china <code>aws-cn</code></li>
<li>region: can be a double colon (::) if that doesn't matter</li>
<li>account-id: the account that owns the resource
<ul>
<li>EC2 needs this</li>
<li>S3 does not need account-id because its globally unique</li>
</ul>
</li>
<li>resource-type/id: changes based on the resource</li>
</ul>
<p>An example that leads to confusion:</p>
<ul>
<li>arn:aws:s3:::catgifs
<ul>
<li>This references an actual bucket</li>
</ul>
</li>
<li>arn:aws:s3:::catgifs/*
<ul>
<li>This refers to objects in that bucket, but not the bucket itself.</li>
</ul>
</li>
</ul>
<p>These two ARNs do not overlap</p>
<h4><a id="user-content-iam-facts" class="anchor" aria-hidden="true" href="#iam-facts"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>IAM FACTS</h4>
<ul>
<li>5,000 IAM users per account</li>
<li>IAM user can be a member of 10 groups</li>
</ul>
<h3><a id="user-content-iam-groups" class="anchor" aria-hidden="true" href="#iam-groups"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>IAM Groups</h3>
<p>Containers for users. <strong>You cannot login to IAM groups</strong> They have no
credentials of their own. Used solely for management of IAM users.</p>
<p>Groups bring two benefits</p>
<ol>
<li>Effective administrative style management of users based on the team</li>
<li>Groups can have Inline and Managed policies attached.</li>
</ol>
<p>AWS merges all of the policies from all groups the user is in together.</p>
<ul>
<li>The 5000 IAM user limit applies to groups.</li>
<li>There is <strong>no all users</strong> IAM group.
<ul>
<li>You can create a group and add all users into that group, but it needs to be
created and managed on your own.</li>
</ul>
</li>
<li>No Nesting: You cannot have groups within groups.</li>
<li>300 Group Limit per account. This can be fixed with a support ticket.</li>
</ul>
<p><strong>Resource Policy</strong> A bucket can have a policy associated with that bucket.
It does so by referencing the identity using an ARN (Amazon Reference Name).
A policy on a resource can reference IAM users and IAM roles by the ARN.
A bucket can give access to one or more users or one or more roles.</p>
<p><strong>GROUPS ARE NOT A TRUE IDENTITY</strong>
<strong>THEY CAN'T BE REFERENCED AS A PRINCIPAL IN A POLICY</strong></p>
<p>An S3 Resource cannot grant access to a group, it is not an identity.
Groups are used to allow permissions to be assigned to IAM users.</p>
<h3><a id="user-content-iam-roles" class="anchor" aria-hidden="true" href="#iam-roles"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>IAM Roles</h3>
<p>A single thing that uses an identity is an IAM User.</p>
<p>IAM Roles are also identities that are used by large groups of individuals.
If have more than 5000 principals, it could be a candidate for an IAM Role.</p>
<p>IAM Roles are <strong>assumed</strong> you become that role.</p>
<p>This can be used short term by other identities.</p>
<p>IAM Users can have inline or managed policies which control which permissions
the identity gets within AWS</p>
<p>Policies which grant, allow or deny, permissions based on their associations.</p>
<p>IAM Roles have two types of roles can be attached.</p>
<ul>
<li>Trust Policy: Specifies which identities are allowed to assume the role.</li>
<li>Permissions Policy: Specifies what the role is allowed to do.</li>
</ul>
<p>If an identity is allowed on the <strong>Trust Policy</strong>, it is given a set
of <strong>Temporary Security Credentials</strong>. Similar to access keys except they
are time limited to expire. The identity will need to renew them by
reassuming the role.</p>
<p>Every time the <strong>Temporary Security Credentials</strong> are used, the access
is checked against the <strong>Permissions Policy</strong>. If you change the policy, the
permissions of the temp credentials also change.</p>
<p>Roles are real identities and can be referenced within resource policies.</p>
<p>Secure Token Service (sts:AssumeRole) this is what generates the temporary
security credentials (TSC).</p>
<h3><a id="user-content-when-to-use-iam-roles" class="anchor" aria-hidden="true" href="#when-to-use-iam-roles"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>When to use IAM Roles</h3>
<p>Lambda Execution Role.
For a given lambda function, you cannot determine the number of principals
which suggested a Role might be the ideal identity to use.</p>
<ul>
<li>Trust Policy: to trust the Lambda Service</li>
<li>Permission Policy: to grant access to AWS services.</li>
</ul>
<p>When this is run, it uses the sts:AssumeRole to generate keys to
CloudWatch and S3.</p>
<p>It is better when possible to use an IAM Role versus attaching a policy.</p>
<h4><a id="user-content-emergency-or-out-of-the-usual-situations" class="anchor" aria-hidden="true" href="#emergency-or-out-of-the-usual-situations"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Emergency or out of the usual situations</h4>
<p>Break Glass Situation - There is a key for something the team does not
normally have access to. When you break the glass, you must have a reason
to do.
A role can have an Emergency Role which will allow further access if
its really needed.</p>
<h4><a id="user-content-adding-aws-into-existing-corp-environment" class="anchor" aria-hidden="true" href="#adding-aws-into-existing-corp-environment"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Adding AWS into existing corp environment</h4>
<p>You may have an existing identity provider you are trying to allow access to.
This may offer SSO (Single Sign On) or over 5000 identities.
This is useful to reuse your existing identities for AWS.
External accounts can't be used to access AWS directly.
To solve this, you allow an IAM role in the AWS account to be assumed
by one of the active directories.
<strong>ID Federation</strong> allowing an external service the ability to assume a role.</p>
<h4><a id="user-content-making-an-app-with-1000000-users" class="anchor" aria-hidden="true" href="#making-an-app-with-1000000-users"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Making an app with 1,000,000 users</h4>
<p><strong>Web Identity Federation</strong> uses IAM roles to allow broader access.
These allow you to use an existing web identity such as google, facebook, or
twitter to grant access to the app.
We can trust these web identities and allow those identities to assume
an IAM role to access web resources such as DynamoDB.
No AWS Credentials are stored on the application.
Can scale quickly and beyond.</p>
<h4><a id="user-content-cross-account-access" class="anchor" aria-hidden="true" href="#cross-account-access"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Cross Account Access</h4>
<p>You can use a role in the partner account and use that to upload objects
to AWS resources.</p>
<h3><a id="user-content-aws-organizations" class="anchor" aria-hidden="true" href="#aws-organizations"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>AWS Organizations</h3>
<p>Without an organization, each AWS account needs it's own set of IAM users
as well as individual payment methods.
If you have more than 5 to 10 accounts, you would want to use an org.</p>
<p>Take a single AWS account <strong>standard AWS account</strong> and create an org.
The standard AWS account then becomes the <strong>master account</strong>.
The master account can invite other existing standard AWS accounts. They will
need to approve their joining to the org.</p>
<p>When standard AWS accounts become part of the org, they
become <strong>member accounts</strong>.
Organizations can only have one <strong>master accounts</strong> and zero or more
<strong>member accounts</strong></p>
<h4><a id="user-content-organization-root" class="anchor" aria-hidden="true" href="#organization-root"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Organization Root</h4>
<p>This is a container that can hold AWS member accounts or the master account.
It could also contain <strong>organizational units</strong> which can contain other
units or member accounts.</p>
<h4><a id="user-content-consolidated-billing" class="anchor" aria-hidden="true" href="#consolidated-billing"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Consolidated billing</h4>
<p>The individual billing for the member accounts is removed and they pass their
billing to the master account.
Inside an AWS organization, you get a single monthly bill for the master
account which covers all the billing for each users.
Can offer a discount with consolidation of reservations and volume discounts</p>
<h4><a id="user-content-create-new-accounts-in-an-org" class="anchor" aria-hidden="true" href="#create-new-accounts-in-an-org"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Create new accounts in an org</h4>
<p>Adding accounts in an organization is easy with only an email needed.
You no longer need IAM users in each accounts. You can use IAM roles
to change these.
It is best to have a single AWS account only used for login.
Some enterprises may use an AWS account while smaller ones may use the master.</p>
<h4><a id="user-content-role-switching" class="anchor" aria-hidden="true" href="#role-switching"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Role Switching</h4>
<p>Allows you to switch between accounts from the command line</p>
<h3><a id="user-content-service-control-policies" class="anchor" aria-hidden="true" href="#service-control-policies"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Service Control Policies</h3>
<p>Can be used to restrict what member accounts in an org can do.</p>
<p>JSON policy document that can be attached:</p>
<ul>
<li>To the org as a whole by attaching to the root container.</li>
<li>A specific Organizational Unit</li>
<li>A specific member only.</li>
</ul>
<p>The master account cannot be restricted by SCPs which means this
should not be used because it is a security risk.</p>
<p>SCPs limit what the account, <strong>including root</strong> can do inside that account.
They don't grant permissions themselves, just act as a barrier.</p>
<h4><a id="user-content-allow-list-vs-deny-list" class="anchor" aria-hidden="true" href="#allow-list-vs-deny-list"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Allow List vs Deny List</h4>
<p>Deny list is the default.</p>
<p>When you enable SCP on your org, AWS applies <code>FullAWSAccess</code>. This means
SCPs have no effect because nothing is restricted. It has zero influence
by themselves.</p>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>Version<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2012-10-17<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>Statement<span class="pl-pds">"</span></span>: {
    <span class="pl-s"><span class="pl-pds">"</span>Effect<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Allow<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>Action<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>*<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>Resource<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>*<span class="pl-pds">"</span></span>
  }
}</pre></div>
<p>SCPs by themselves don't grant permissions. When SCPs are enabled,
there is an implicit deny.</p>
<p>You must then add any services you want to Deny such as <code>DenyS3</code></p>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>Version<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2012-10-17<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>Statement<span class="pl-pds">"</span></span>: {
    <span class="pl-s"><span class="pl-pds">"</span>Effect<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Deny<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>Action<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>s3:*<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>Resource<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>*<span class="pl-pds">"</span></span>
  }
}</pre></div>
<p><strong>Deny List</strong> is a good default because it allows for the use of growing
services offered by AWS. A lot less admin overhead.</p>
<p><strong>Allow List</strong> allows you to be conscience of your costs.</p>
<ul>
<li>To begin, you must remove the <code>FullAWSAccess</code> list</li>
<li>Then, specify which services need to be allowed access.</li>
<li>Example <code>AllowS3EC2</code> is below</li>
</ul>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>Version<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2012-10-17<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>Statement<span class="pl-pds">"</span></span>: [
    {
        <span class="pl-s"><span class="pl-pds">"</span>Effect<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Allow<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>Action<span class="pl-pds">"</span></span>: [
            <span class="pl-s"><span class="pl-pds">"</span>s3:*<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>ec2:*<span class="pl-pds">"</span></span>
        ],
    <span class="pl-s"><span class="pl-pds">"</span>Resource<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>*<span class="pl-pds">"</span></span>
    }
  ]
}</pre></div>
<h3><a id="user-content-cloudwatch-logs" class="anchor" aria-hidden="true" href="#cloudwatch-logs"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>CloudWatch Logs</h3>
<p>This is a public service, this can be used from AWS VPC or on premise
environment.</p>
<p>This allows to <strong>store</strong>, <strong>monitor</strong> and <strong>access</strong> logging data.</p>
<ul>
<li>This is a piece of information data and a timestamp</li>
<li>Can be more fields, but at least these two</li>
</ul>
<p>Comes with some AWS Integrations.
Security is provided with IAM roles or Service roles
Can generate metrics based on logs <strong>metric filter</strong></p>
<h4><a id="user-content-architecture-of-cloudwatch-logs" class="anchor" aria-hidden="true" href="#architecture-of-cloudwatch-logs"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Architecture of CloudWatch Logs</h4>
<p>It is a regional service <code>us-east-1</code></p>
<p>Need logging sources such as external APIs or databases. This sends
information as <strong>log events</strong>. These are stored in <strong>log streams</strong>. This is a
sequence of log events from the same source.</p>
<p><strong>Log Groups</strong> are containers for multiple logs streams of the same
type of logging. This also stores configuration settings such as
retention settings and permissions.</p>
<p>Once the settings are defined on a log group, they apply to all log streams
in that log group. Metric filters are also applied on the log groups.</p>
<h3><a id="user-content-cloudtrail-essentials" class="anchor" aria-hidden="true" href="#cloudtrail-essentials"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>CloudTrail Essentials</h3>
<p>Concerned with who did what.</p>
<p>Logs API calls or activities as <strong>CloudTrail Event</strong></p>
<p>Stores the last 90 days of events in the <strong>Event History</strong>. This is enabled
by default and is no additional cost.</p>
<p>To customize the service you need to create a new <strong>trail</strong>.
Two types of events. Default only logs Management Events</p>
<ul>
<li>
<p>Management Events:
Provide information about management operations performed on resources
in the AWS account. Create an EC2 instance or terminating one.</p>
</li>
<li>
<p>Data Events:
Objects being uploaded to S3 or a Lambda function being invoked. This is not
enabled by default and must be enabled for that trail.</p>
</li>
</ul>
<h4><a id="user-content-cloudtrail-trail" class="anchor" aria-hidden="true" href="#cloudtrail-trail"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>CloudTrail Trail</h4>
<p>Logs events for the AWS region it is created in. It is a regional service.</p>
<p>Once created, it can operate in two ways</p>
<ul>
<li>One region trail</li>
<li>All region trail
<ul>
<li>Collection of trails in all regions</li>
<li>When new regions are added, they will be added to this trail automatically</li>
</ul>
</li>
</ul>
<p>Most services log events in the region they occur. The trail then must be
a one region trail in that region or an all region trail to log that event.</p>
<p>A small number of services log events globally to one region. Global services
such as IAM or STS or CloudFront always log their events to <code>us-east-1</code></p>
<p>A trail must have this enabled to have this logged.</p>
<p>AWS services are largely split into regional services or global services.</p>
<p>When the services log, they log in the region they are created or
to <code>us-east-1</code> if they are a global service.</p>
<p>A trail can store events in an S3 bucket as a compressed JSON file. It can
also use CloudWatch Logs to output the data.</p>
<p>CloudTrail products can create an organizational trail. This allows a single
management point for all the APIs and management events for that org.</p>
<h4><a id="user-content-cloudtrail-exam-powerup" class="anchor" aria-hidden="true" href="#cloudtrail-exam-powerup"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>CloudTrail Exam PowerUp</h4>
<ul>
<li>It is enabled by default for 90 days without S3</li>
<li>Trails are how you configure S3 and CWLogs</li>
<li>Management events are only saved by default</li>
<li>IAM, STS, CloudFront are Global Service events and log to <code>us-east-1</code>
<ul>
<li>Trail must be enabled to do this</li>
</ul>
</li>
<li>NOT REALTIME - There is a delay. Approximately 15 minute delay</li>
</ul>
<h4><a id="user-content-cloudtrail-pricing" class="anchor" aria-hidden="true" href="#cloudtrail-pricing"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>CloudTrail Pricing</h4>
<p><a href="https://aws.amazon.com/cloudtrail/pricing/" rel="nofollow">https://aws.amazon.com/cloudtrail/pricing/</a></p>
<hr>
<h2><a id="user-content-simple-storage-service-s3" class="anchor" aria-hidden="true" href="#simple-storage-service-s3"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Simple-Storage-Service-(S3)</h2>
<h3><a id="user-content-s3-security" class="anchor" aria-hidden="true" href="#s3-security"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>S3 Security</h3>
<p><strong>S3 is private by default!</strong> The only identity which has any initial
access to an S3 bucket is the account root user of the account which owns that
bucket.</p>
<h4><a id="user-content-s3-bucket-policy" class="anchor" aria-hidden="true" href="#s3-bucket-policy"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>S3 Bucket Policy</h4>
<p>This is a <strong>resource policy</strong></p>
<ul>
<li>controls who has access to that resource</li>
<li>can allow or deny access from different accounts</li>
<li>can allow or deny anonymous principals
<ul>
<li>this is explicitly declared in the bucket policy itself.</li>
</ul>
</li>
</ul>
<p>Different from an <strong>identity policy</strong></p>
<ul>
<li>controls what that identity can access</li>
<li>can only be attached to identities in your own account
<ul>
<li>no way of giving an identity in another account access to a bucket.</li>
</ul>
</li>
</ul>
<p>Each bucket can only have one policy, but it can have multiple statements.</p>
<h4><a id="user-content-acls-legacy" class="anchor" aria-hidden="true" href="#acls-legacy"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>ACLs (Legacy)</h4>
<p>A way to apply a subresource to objects and buckets.
These are legacy and AWS does not recommend their use.
They are inflexible and allow simple permissions.</p>
<h4><a id="user-content-s3-exam-powerup" class="anchor" aria-hidden="true" href="#s3-exam-powerup"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>S3 Exam PowerUp</h4>
<p>When to use Identity Policy or Bucket Policy:</p>
<p>Identity</p>
<ul>
<li>Controlling high mix of different resources.
<ul>
<li>Not every service supports resource policies.</li>
</ul>
</li>
<li>Want to manage permissions all in one place, use IAM.</li>
<li>Must have access to all accounts accessing the information.</li>
</ul>
<p>Bucket</p>
<ul>
<li>Managing permissions on a specific product.</li>
<li>If you need anonymous or cross account access.</li>
</ul>
<p>ACLs: NEVER - unless you must.</p>
<h3><a id="user-content-s3-static-hosting" class="anchor" aria-hidden="true" href="#s3-static-hosting"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>S3 Static Hosting</h3>
<p>Normal access is via AWS APIs.
This allows access via HTTP using a web browser.</p>
<p>When you enable static website hosting you need two HTML files:</p>
<ul>
<li>index document
<ul>
<li>default page returned from a website</li>
<li>entry point for most websites</li>
</ul>
</li>
<li>error document
<ul>
<li>similar to index, but only when something goes wrong</li>
</ul>
</li>
</ul>
<p>Static website hosting creates a <strong>website endpoint</strong>.</p>
<p>This is influenced by the bucket name and region it is in.
This cannot be changed.</p>
<p>You can use a custom domain for a bucket, but then the bucket name matters.
The name of the bucket must match the domain.</p>
<h4><a id="user-content-offloading" class="anchor" aria-hidden="true" href="#offloading"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Offloading</h4>
<p>Instead of using EC2 to host an entire website, the compute service
can generate a HTML file which points to the resources hosted on a static
bucket. This ensures the media is retrieved from S3 and not EC2.</p>
<h4><a id="user-content-out-of-band-pages" class="anchor" aria-hidden="true" href="#out-of-band-pages"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Out-of-band pages</h4>
<p>This may be an error page to display maintenance if the server goes offline.
We could then change our DNS and move customers to a backup website on S3.</p>
<h4><a id="user-content-s3-pricing" class="anchor" aria-hidden="true" href="#s3-pricing"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>S3 Pricing</h4>
<ul>
<li>Cost to store data, per GB / month fee
<ul>
<li>Prorated for less than a GB or month.</li>
</ul>
</li>
<li>Data transfer fee
<ul>
<li>Data in is always free</li>
<li>Data out is a per GB charge</li>
</ul>
</li>
<li>Each operation has a cost per 1000 operations.
<ul>
<li>Can add up for static website hosting with many requests.</li>
</ul>
</li>
</ul>
<h3><a id="user-content-object-versioning-and-mfa-delete" class="anchor" aria-hidden="true" href="#object-versioning-and-mfa-delete"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Object Versioning and MFA Delete</h3>
<p>Without Versioning:</p>
<ul>
<li>Each object is identified solely by the object key, it's name.</li>
<li>If you modify an object, the original of that object is replaced.</li>
<li>The attribute, <strong>ID of object</strong>, is set to <strong>null</strong>.</li>
</ul>
<p>Versioning</p>
<ul>
<li>This is off by default.</li>
<li>Once it is turned on, it cannot be turned off.</li>
<li>Versioning can be suspended and enabled again.</li>
<li>This allows for multiple versions of objects within a bucket.</li>
<li>Objects which would modify objects <strong>generate a new version</strong> instead.</li>
</ul>
<p>The latest or current version is always returned when an object version
is not requested.</p>
<p>When an object is deleted, AWS puts a <strong>delete marker</strong> on the object
and hides all previous versions. You could delete this marker to enable
the item.</p>
<p>To delete an object, you must delete all the versions of that object
using their version marker.</p>
<h4><a id="user-content-mfa-delete" class="anchor" aria-hidden="true" href="#mfa-delete"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>MFA Delete</h4>
<p>Enabled within version configuration in a bucket.
This means MFA is required to change bucket versioning state.
MFA is required to delete versions of an object.</p>
<p>In order to change a version state or delete a particular version of an object,
you need to provide the serial number of your MFA token as well as the code
it generates. These are concatenated and passed with any API calls.</p>
<h3><a id="user-content-s3-performance-optimization" class="anchor" aria-hidden="true" href="#s3-performance-optimization"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>S3 Performance Optimization</h3>
<p>Single PUT Upload</p>
<ul>
<li>Objects uploaded to S3 are sent as a single stream by default.</li>
<li>If the stream fails, the upload fails and requires a restart of the transfer.</li>
<li>Single PUT upload up to 5GB</li>
</ul>
<p>Multipart Upload</p>
<ul>
<li>Data is broken up into smaller parts.</li>
<li>The minimum data size is 100 MB.</li>
<li>Upload can be split into maximum of 10,000 parts.
<ul>
<li>Each part can range between 5MB and 5GB.</li>
<li>Last leftover part can be smaller than 5MB as needed.</li>
</ul>
</li>
<li>Parts can fail in isolation and restart in isolation.</li>
<li>The risk of uploading large amounts of data is reduced.</li>
<li>Improves transfer rate to be the speed of all parts.</li>
</ul>
<p>S3 Accelerated Transfer</p>
<ul>
<li>Off by default.</li>
<li>Uses the network of AWS edge locations to speed up transfer.</li>
<li>Bucket name cannot contain periods.</li>
<li>Name must be DNS compatible.</li>
<li>Benefits improve the larger the location and distance.
<ul>
<li>The worse the start, the better the performance benefits.</li>
</ul>
</li>
</ul>
<h3><a id="user-content-encryption-101" class="anchor" aria-hidden="true" href="#encryption-101"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Encryption 101</h3>
<h4><a id="user-content-encryption-at-rest" class="anchor" aria-hidden="true" href="#encryption-at-rest"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Encryption at Rest</h4>
<ul>
<li>An example is a password on a laptop
<ul>
<li>If the laptop is stolen, the data is already encrypted and useless.</li>
</ul>
</li>
<li>Commonly within cloud environments. Even if someone could
find and access the base storage device, they can't do anything with it.</li>
<li>Only one entity involved</li>
</ul>
<h4><a id="user-content-encryption-in-transit" class="anchor" aria-hidden="true" href="#encryption-in-transit"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Encryption in Transit</h4>
<ul>
<li>An encryption tunnel outside the raw data.</li>
<li>Anyone looking from the outside will only see a stream of scrambled data.</li>
<li>Used when there are multiple parties or systems at play.</li>
</ul>
<h4><a id="user-content-terms" class="anchor" aria-hidden="true" href="#terms"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Terms</h4>
<ul>
<li>plaintext: unencrypted data not limited to text</li>
<li>key: a password</li>
<li>ciphertext: encrypted data generated by an algorithm from plaintext and a key</li>
</ul>
<h4><a id="user-content-symmetric-encryption" class="anchor" aria-hidden="true" href="#symmetric-encryption"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Symmetric Encryption</h4>
<p>The key is handed from one entity to another before the data.
This is difficult because the key needs to be transferred securely.
If the data is time sensitive, the key needs to be arranged beforehand.</p>
<h4><a id="user-content-asymmetric-encryption" class="anchor" aria-hidden="true" href="#asymmetric-encryption"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Asymmetric Encryption</h4>
<ul>
<li>public key: cannot decrypt data but can generate ciphertext</li>
<li>private key: can decrypt data encrypted by the public key</li>
</ul>
<p>The public key is uploaded to cloud storage.
The data is encrypted and sent back to the original entity.
The private key can decrypt the data.</p>
<p>This is secure because stolen public keys can only encrypt data.
Private keys must be handled securely.</p>
<h4><a id="user-content-signing" class="anchor" aria-hidden="true" href="#signing"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Signing</h4>
<p>Encryption by itself does not prove who encrypted the data.</p>
<ol>
<li>An entity can encrypt a message with their private key.</li>
<li>Their public key is hosted in an accessible location.</li>
<li>The receiving party can use the public key to confirm who sent the message.</li>
</ol>
<h4><a id="user-content-steganography" class="anchor" aria-hidden="true" href="#steganography"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Steganography</h4>
<p>Encryption is obvious when used. There is no denying that the
data was encrypted. Someone could force you to decrypt the data packet.</p>
<p>A file can be hidden in an image or other file. If it difficult
to find the message unless you know what to look for.</p>
<p>One party would take another party's public key and encrypt some data to create
ciphertext. That ciphertext can be hidden in another file so long as both
parties know how the data will be hidden.</p>
<h3><a id="user-content-key-management-service-kms" class="anchor" aria-hidden="true" href="#key-management-service-kms"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Key Management Service (KMS)</h3>
<ul>
<li>Regional service
<ul>
<li>Every region is isolated when using KMS.</li>
</ul>
</li>
<li>Public service
<ul>
<li>Occupies the AWS public zone and can be connected to from anywhere.</li>
</ul>
</li>
<li>Create, store, and manage keys.
<ul>
<li>Can handle both symmetric and asymmetric keys.</li>
</ul>
</li>
<li>KMS can perform cryptographic operations itself.</li>
<li>Keys never leave KMS.</li>
<li>Keys use <strong>FIPS 140-2 (L2)</strong> security standard.
<ul>
<li>Some features are compliant with Level 3.</li>
<li>All features are compliant with Level 2.</li>
</ul>
</li>
</ul>
<h4><a id="user-content-cmks---customer-master-keys" class="anchor" aria-hidden="true" href="#cmks---customer-master-keys"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>CMKs - Customer Master Keys</h4>
<ul>
<li>Managed by KMS and used within cryptographic operations.</li>
<li>AWS services, applications, and the user can all use them.</li>
<li>Think of them as a container for the actual physical master keys.</li>
<li>These are all backed by <strong>physical</strong> key material.</li>
<li>You can generate or import the key material.</li>
<li>CMKs can be used for up to <strong>4KB of data</strong>.</li>
</ul>
<p>It is logical and contains</p>
<ul>
<li>Key ID: unique identifier for the key</li>
<li>Creation Date</li>
<li>Key Policy: a type of resource policy</li>
<li>Description</li>
<li>State of the Key: active or not</li>
</ul>
<h4><a id="user-content-data-encryption-key-dek" class="anchor" aria-hidden="true" href="#data-encryption-key-dek"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Data Encryption Key (DEK)</h4>
<ul>
<li>Generated by KMS using the CMK and <code>GenerateDataKey</code> operation.</li>
<li>Used to encrypt data larger than 4KB in size.</li>
<li>Linked to a specific CMK so KMS can tell that a specific DEK was
generated with a specific CMK.</li>
</ul>
<p>KMS does not store the DEK, once provided to a user or service, it is
discarded. KMS doesn't actually perform the encryption or decryption
of data using the DEK or anything past generating them.</p>
<p>When the DEK is generated, KMS provides two version.</p>
<ul>
<li>Plaintext Version - This can be used immediately.</li>
<li>Ciphertext Version - Encrypted version of the DEK.
<ul>
<li>This is encrypted by the CMK that generated it.</li>
<li>In the future it can be decrypted by KMS using the CMK assuming
you have the permissions.</li>
</ul>
</li>
</ul>
<p>Architecture</p>
<ol>
<li>DEK is generated right before something is encrypted.</li>
<li>The data is encrypted with the plaintext version of the DEK.</li>
<li>Discard the plaintext data version of the DEK.</li>
<li>The encrypted DEK is stored next to the ciphertext generated earlier.</li>
</ol>
<h4><a id="user-content-kms-key-concepts" class="anchor" aria-hidden="true" href="#kms-key-concepts"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>KMS Key Concepts</h4>
<ul>
<li>Customer Master Keys (CMK) are isolated to a region.
<ul>
<li>Never leave the region or KMS.</li>
<li>Cannot extract a CMK.</li>
</ul>
</li>
<li>AWS managed CMKs
<ul>
<li>Created automatically by AWS when using a service such
as S3 which uses KMS for encryption.</li>
</ul>
</li>
<li>Customer managed CMKS
<ul>
<li>Created explicitly by the customer.</li>
<li>Much more more configurable, for example the key policy can be edited.</li>
<li>Can allow other AWS accounts access to CMKS</li>
</ul>
</li>
</ul>
<p>All CMKs support key rotation.</p>
<ul>
<li>AWS automatically rotates the keys every 1095 days (3 years)</li>
<li>Customer managed keys rotate every year.</li>
</ul>
<p>CMK itself contains:</p>
<ul>
<li>Current backing key, physical material used to encrypt and decrypt</li>
<li>Previous backing keys created from rotating that material</li>
</ul>
<p>KMS can create an alias which is a shortcut to a particular CMK.
Aliases are also per region. You can create a <code>MyApp1</code> alias in all regions
but they would be separate aliases, and in each region it would be pointing
potentially at a different CMK.</p>
<h4><a id="user-content-key-policy-resource-policy" class="anchor" aria-hidden="true" href="#key-policy-resource-policy"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Key Policy (resource policy)</h4>
<ul>
<li>Every CMK has one.</li>
<li>Customer managed CMKs can adjust the policy.</li>
<li>Unlike other policies, KMS has to be explicitly told that keys trust the AWS
account that they're in.</li>
<li>The trust isn't automatic so be careful when adjusting key policies.</li>
<li>You always need a key policy in place so the key trusts the account and so
that the account can manage it by applying IAM permission policies to IAM users
in that account.</li>
<li>In order for IAM to work, IAM is trusted by the account, and the account
needs to be trusted by the key.</li>
<li>It sets up this chain of trust from the key to the account to IAM and then
to an IAM user, if they're granted any identity permissions.</li>
</ul>
<h3><a id="user-content-kms-key-demo" class="anchor" aria-hidden="true" href="#kms-key-demo"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>KMS Key Demo</h3>
<p>Linux/macOS commands</p>
<div class="highlight highlight-source-shell"><pre>aws kms encrypt \
    --key-id alias/catrobot \
    --plaintext fileb://battleplans.txt \
    --output text \
    --query CiphertextBlob \
    --profile iamadmin-general <span class="pl-k">|</span> base64 \
    --decode <span class="pl-k">&gt;</span> not_battleplans.enc</pre></div>
<div class="highlight highlight-source-shell"><pre>aws kms decrypt \
    --ciphertext-blob fileb://not_battleplans.enc \
    --output text \
    --profile iamadmin-general \
    --query Plaintext <span class="pl-k">|</span> base64 --decode <span class="pl-k">&gt;</span> decryptedplans.txt</pre></div>
<h3><a id="user-content-object-encryption" class="anchor" aria-hidden="true" href="#object-encryption"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Object Encryption</h3>
<p>Buckets aren't encrypted, <strong>objects are</strong>.
Multiple objects in a bucket can use a different encryption methods.</p>
<p>Two main methods of encryption S3 is capable of supporting.
Both types are encryption at rest. Data sent from a user to S3 is automatically
encrypted in transit outside of these methods.</p>
<p>Client-Side encryption</p>
<ul>
<li>Objects being encrypted by the client before they leave.</li>
<li>Data being sent the whole time it is sent as cypher text.</li>
<li>AWS has no way to see into the data.</li>
<li>The encryption burden is on the customer and not AWS.</li>
</ul>
<p>Server-Side encryption</p>
<ul>
<li>Data is encrypted in transit using HTTPS</li>
<li>Data inside the tunnel is still in its original unencrypted form.</li>
<li>Data reaches S3 server in plain text form.</li>
<li>After S3 sees the data, it is then encrypted.</li>
<li>AWS will handle some or all of these processes.</li>
</ul>
<h4><a id="user-content-sse-c-server-side-encryption-with-customer-provided-keys" class="anchor" aria-hidden="true" href="#sse-c-server-side-encryption-with-customer-provided-keys"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>SSE-C (Server-side encryption with customer provided keys)</h4>
<ul>
<li>Customer is responsible for the keys themselves.</li>
<li>S3 services manages the actual encryption and decryption
<ul>
<li>Offloads CPU requirements for encryption.</li>
</ul>
</li>
<li>Customer still needs to generate and manage the key.</li>
<li>S3 will see the unencrypted object throughout this process.</li>
</ul>
<p>SSE-C Encryption Steps</p>
<ol>
<li>When placing an object in S3, you provide encryption key and plaintext object</li>
<li>Once the key and object arrive, it is encrypted.</li>
<li>A hash of the key is taken and attached to the object.
The hash can identify if the specific key was used to encrypt the object.</li>
<li>The key is then discarded after the hash is taken.</li>
<li>The encrypted and one-way hash are stored persistently on storage.</li>
</ol>
<p>To decrypt the object, you must tell S3 which object to decrypt and provide
it with the key used to encrypt it. If the key that you supply is correct,
the proper hash, S3 will decrypt the object, discard the key, and return the
plaintext version of the object.</p>
<h4><a id="user-content-sse-s3-aes256-server-side-encryption-w-amazon-s3-managed-keys" class="anchor" aria-hidden="true" href="#sse-s3-aes256-server-side-encryption-w-amazon-s3-managed-keys"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>SSE-S3 AES256 (Server-side encryption w/ Amazon S3 managed keys)</h4>
<p>AWS handles both the encryption and decryption process as well as the
key generation and management. This provides very little control over how
the keys are used, but has little admin overhead.</p>
<p>SSE-S3 Encryption Steps</p>
<ol>
<li>When putting data into S3, only need to provide plaintext.</li>
<li>S3 generates fully managed and rotated <strong>master key</strong> automatically.</li>
<li>Object generates a key specific for each object that is uploaded.</li>
<li>The master key is used to encrypt the specific object key, and the
unencrypted version of that key is discarded.</li>
<li>The encrypted file and encrypted key are stored side by side in S3.</li>
</ol>
<p>Three Problems with this method:</p>
<ul>
<li>Not good for regulatory environment where keys and access must be controlled.</li>
<li>No way to control key material rotation.</li>
<li>No role separation. A full S3 admin can decrypt data and open objects.</li>
</ul>
<h4><a id="user-content-sse-kms-server-side-encryption-w-customer-master-keys-stored-in-aws-kms" class="anchor" aria-hidden="true" href="#sse-kms-server-side-encryption-w-customer-master-keys-stored-in-aws-kms"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>SSE-KMS (Server-side encryption w/ customer master keys stored in AWS KMS)</h4>
<p>Much like SSE-S3, where AWS handles both the keys and encryption process.
KMS handles the master key and not S3. The first time an object is uploaded,
S3 works with KMS to create an AWS managed CMK. This is the default key
which gets used in the future.</p>
<p>Every time an object is uploaded, S3 uses a dedicated key to encrypt that object
and that key is a data encryption key which KMS generates using the CMK.
The CMK does not need to be managed by AWS and can be a customer managed CMK.</p>
<p>SSE-KMS Encryption Steps</p>
<ol>
<li>S3 is provided a plaintext version of the data encryption key as well
as an encrypted version.</li>
<li>The data is encrypted with the plaintext key and the key discarded.</li>
<li>The encrypted key is stored alongside the encrypted object.</li>
</ol>
<p>When uploading an object, you can create and use a customer managed CMK. This
allows the user to control the permissions and the usage of the key material.
In regulated industries, this is reason enough to use SSE-KMS
You can also add logging and see any calls against this key from CloudTrail.</p>
<p>The best benefit is the role separation. To decrypt any object, you need
access to the CMK that was used to generate the unique key that encrypted them.
The CMK is used to decrypt the data encryption key for that object.
That decrypted data encryption key is used to decrypt the object itself.
If you don't have access to KMS, you don't have access to the object.</p>
<h3><a id="user-content-s3-object-storage-classes" class="anchor" aria-hidden="true" href="#s3-object-storage-classes"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>S3 Object Storage Classes</h3>
<p>Picking a storage class can be done while uploading a specific object.
The default is S3 standard. Once an object is uploaded to a specific class,
it can be easily changed as long as some conditions are met.</p>
<p>Objects in S3 are stored in a specific region.</p>
<h4><a id="user-content-s3-standard" class="anchor" aria-hidden="true" href="#s3-standard"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>S3 Standard</h4>
<ul>
<li>Default AWS storage class that's used in S3, should be user default as well.</li>
<li>S3 Standard is region resilient, and can tolerate the failure of an AZ.</li>
<li>Objects are replicated to at least 3+ AZs when they are uploaded.</li>
<li>99999999999% durability</li>
<li>99.99% availability</li>
<li>Offers low latency and high throughput.</li>
<li>No minimums, delays, or penalties.</li>
<li>Billing is storage fee, data transfer fee, and request based charge.</li>
</ul>
<p>All of the other storage classes trade some of these compromises for another.</p>
<h4><a id="user-content-s3-standard-ia" class="anchor" aria-hidden="true" href="#s3-standard-ia"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>S3 Standard-IA</h4>
<ul>
<li>Designed for less frequent rapid access when it is needed.</li>
<li>Cheaper rate to store data you will rarely need, but if you do need it, you
need it quickly.</li>
<li>~54% cheaper than S3 standard.</li>
<li>Minimum 128KB charge for each object.
<ul>
<li>Cost benefits might be negated for smaller objects.</li>
</ul>
</li>
<li>30 days minimum duration charge per object.</li>
<li>Retrieval fee for every GB of data retrieved from this class.</li>
<li>99.9% availability, slightly lower than standard S3.</li>
</ul>
<p>Designed for data that isn't accessed often, long term storage, backups,
disaster recovery files. The requirement for data to be safe is most important.</p>
<h4><a id="user-content-one-zone-ia" class="anchor" aria-hidden="true" href="#one-zone-ia"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>One Zone-IA</h4>
<ul>
<li>Designed for data that is accessed less frequently but needed quickly.</li>
<li>80% of the base cost of Standard-IA.</li>
<li>Same minimum size and duration fee as Standard-IA</li>
<li>Data is only stored in a single AZ, no 3+ AZ replication.</li>
<li>99.5% availability, lower than Standard-IA</li>
</ul>
<p>Great choice for secondary copies of primary data or backup copies.</p>
<p>If data is easily creatable from a primary data set, this would be a great
place to store the output from another data set.</p>
<h4><a id="user-content-s3-glacier" class="anchor" aria-hidden="true" href="#s3-glacier"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>S3 Glacier</h4>
<ul>
<li>No immediate access to objects, retrieval in minutes or hours.</li>
<li>Make a request to access objects then after a duration, you get access.
<ul>
<li>Retrieval time anywhere from 1 min - 12 hrs</li>
</ul>
</li>
<li>Secure, durable, and low cost storage for archival data.</li>
<li>17% of the base cost of S3 standard</li>
<li>99999999999% durability</li>
<li>99.99% availability</li>
<li>3+ AZ replication</li>
<li>40KB minimum object capacity charge</li>
<li>90 days minimum storage duration charge.</li>
</ul>
<p>Retrieval methods:</p>
<ul>
<li>Expedited: 1 - 5 minutes, but is the most expensive</li>
<li>Standard: 3 - 5 hours to restore.</li>
<li>Bulk: 5 - 12 hours. Has the lowest cost and is good for a large set of data.</li>
</ul>
<h4><a id="user-content-s3-glacier-deep-archive" class="anchor" aria-hidden="true" href="#s3-glacier-deep-archive"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>S3 Glacier Deep Archive</h4>
<ul>
<li>Designed for long term backups and as a tape-drive replacement.</li>
<li>4.3% of the base cost of S3 standard</li>
<li>180 days minimum storage duration charge.</li>
<li>Standard retrieval within 12 hours, bulk retrieval in 48 hours.</li>
<li>Cannot use to make data public or download normally.</li>
</ul>
<h4><a id="user-content-s3-intelligent-tiering" class="anchor" aria-hidden="true" href="#s3-intelligent-tiering"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>S3 Intelligent-Tiering</h4>
<ul>
<li>Combination of standard and standard IA.</li>
<li>Uses automation to remove overhead of moving objects.</li>
<li>Additional fee of $0.0025 per 1,000 objects tracked.</li>
<li>If an object is not accessed for 30 days, it will move into Standard-IA.</li>
</ul>
<p>This is good for objects that are unknown their access pattern.</p>
<h3><a id="user-content-object-lifecycle-management" class="anchor" aria-hidden="true" href="#object-lifecycle-management"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Object Lifecycle Management</h3>
<p>Intelligent-Tiering is used for objects where access patterns is unknown.
A lifecycle configuration is a set of <strong>rules</strong> that consists of <strong>actions</strong>.</p>
<h4><a id="user-content-transition-actions" class="anchor" aria-hidden="true" href="#transition-actions"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Transition Actions</h4>
<p>Change the storage class over time such as:</p>
<ul>
<li>Move an object from S3 to IA after 90 days</li>
<li>After 180 days move to Glacier</li>
<li>After one year move to Deep Archive</li>
</ul>
<p>Objects must flow downwards, they can't flow in the reverse direction.</p>
<h4><a id="user-content-expiration-actions" class="anchor" aria-hidden="true" href="#expiration-actions"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Expiration Actions</h4>
<p>Once an object has been uploaded and changed, you can purge older versions
after 90 days to keep costs down.</p>
<h3><a id="user-content-s3-replication" class="anchor" aria-hidden="true" href="#s3-replication"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>S3 Replication</h3>
<p>There are two types of S3 replication available.</p>
<ul>
<li>Cross-Region Replication (CRR)
<ul>
<li>Allows the replication of objects from a source bucket to a destination
bucket in <strong>different</strong> AWS regions.</li>
</ul>
</li>
<li>Same-Region Replication (SRR)
<ul>
<li>Allows the replication of objects from a source bucket to a destination
bucket in the <strong>same</strong> AWS region.</li>
</ul>
</li>
</ul>
<p>Architecture for both is similar, only difference is if both buckets are
in the same account or different accounts.</p>
<p>The replication configuration is applied to the source bucket and configures
S3 to replicate from this source bucket to a destination bucket.
It also configures the IAM role to use for the replication process.
The role is configured to allow the S3 service to assume it based on
its trust policy. The role's permission policy allows it to read objects on the
source bucket and replicate them to the destination bucket.</p>
<p>When different accounts are used, the role is not by default trusted
by the destination account. If configuring between accounts, you must
add a bucket policy on the destination account to allow the IAM role from
the source account access to the bucket.</p>
<h4><a id="user-content-s3-replication-options" class="anchor" aria-hidden="true" href="#s3-replication-options"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>S3 Replication Options</h4>
<ul>
<li>Which objects are replicated.
<ul>
<li>Default is all source objects, but can select a smaller subset of objects.</li>
</ul>
</li>
<li>Select which storage class the destination bucket will use.
<ul>
<li>Default is the same type of storage, but this can be changed.</li>
</ul>
</li>
<li>Define the ownership of the objects.
<ul>
<li>The default is they will be owned by the same account as the source bucket.</li>
<li>If the buckets are in different accounts, the objects in the destination
could be owned by the source account and not allowed access.</li>
</ul>
</li>
<li>Replication Time Control (RTC)
<ul>
<li>Adds a guaranteed level of SLA within 15 minutes for extra cost.</li>
<li>This is useful for buckets that must be in sync the whole time.</li>
</ul>
</li>
</ul>
<h4><a id="user-content-important-replication-tips" class="anchor" aria-hidden="true" href="#important-replication-tips"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Important Replication Tips</h4>
<ul>
<li>Replication is not retroactive.
<ul>
<li>If you enable replication on a bucket that already has objects, the old
objects will not be replicated.</li>
</ul>
</li>
<li>Both buckets must have versioning enabled.</li>
<li>It is a one way replication process only.</li>
<li>Replication by default can handle objects that are unencrypted or SSE-S3.
<ul>
<li>With configuration it can handle SSE-KMS, but KMS requires more
configuration to work.</li>
<li>It cannot replicate objects with SSE-C because AWS does not have the keys
necessary.</li>
</ul>
</li>
<li>Source bucket owner needs permissions to objects. If you grant cross-account
access to a bucket. It is possible the source bucket account will not own
some of those objects.</li>
<li>Will not replicate system events, glacier, or glacier deep archive.</li>
<li>No deletes are replicated.</li>
</ul>
<h4><a id="user-content-why-use-replication" class="anchor" aria-hidden="true" href="#why-use-replication"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Why use replication</h4>
<p>SRR - Log Aggregation
SRR - Sync production and test accounts
SRR - Resilience with strict sovereignty requirements
CRR - Global resilience improvements
CRR - Latency reduction</p>
<h3><a id="user-content-s3-presigned-url" class="anchor" aria-hidden="true" href="#s3-presigned-url"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>S3 Presigned URL</h3>
<p>A way to give another person or application access to a object inside an S3
bucket using your credentials in a safe way.</p>
<p>IAM admin can make a request to S3 to generate a presigned URL by providing:</p>
<ul>
<li>security credentials</li>
<li>bucket name</li>
<li>object key</li>
<li>expiry date and time</li>
<li>indicate how the object or bucket will be accessed</li>
</ul>
<p>S3 will create a presigned URL and return it. This URL will have encoded inside
it the details that IAM admin provided. It will be configured to expire at
a certain date and time as requested by the IAM admin user.</p>
<h4><a id="user-content-s3-presigned-url-exam-powerup" class="anchor" aria-hidden="true" href="#s3-presigned-url-exam-powerup"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>S3 Presigned URL Exam PowerUp</h4>
<ul>
<li>You can create a presigned URL for an object you have do not have access to.
The object will not allow access because your user does not have access.</li>
<li>When using the URL the permission that you have access to, match the identity
that generated it at the moment the item is being accessed.</li>
<li>If you get an access deny it means the ID never had access, or lost it.</li>
<li>Don't generate presigned URLs with an IAM role.
<ul>
<li>The role will likely expire before the URL does.</li>
</ul>
</li>
</ul>
<h3><a id="user-content-s3-select-and-glacier-select" class="anchor" aria-hidden="true" href="#s3-select-and-glacier-select"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>S3 Select and Glacier Select</h3>
<p>This provides a ways to retrieve parts of objects and not the entire object.</p>
<p>If you retrieve a 5TB object, it takes time and consumes 5TB of data.
Filtering at the client side doesn't reduce this cost.</p>
<p>S3 and Glacier select lets you use SQL-like statements to select part of the
object which is returned in a filtered way.
The filtering happens at the S3 service itself saving time and data.</p>
<hr>
<h2><a id="user-content-virtual-private-cloud-vpc" class="anchor" aria-hidden="true" href="#virtual-private-cloud-vpc"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Virtual-Private-Cloud-VPC</h2>
<h3><a id="user-content-networking-refresher" class="anchor" aria-hidden="true" href="#networking-refresher"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Networking Refresher</h3>
<h4><a id="user-content-ipv4---rfc-791-1981" class="anchor" aria-hidden="true" href="#ipv4---rfc-791-1981"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>IPv4 - RFC 791 (1981)</h4>
<p>Dotted decimal notation for human readability.</p>
<ul>
<li>4 numbers from 0 to 255 separated by a period.</li>
<li>Octet are the numbers between the period.</li>
</ul>
<p>There are just over 4 billion addresses.
This was not very flexible because it was either too small or large for
some corporations. Some IP addresses was always left unused.</p>
<h4><a id="user-content-classful-addressing" class="anchor" aria-hidden="true" href="#classful-addressing"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Classful Addressing</h4>
<ul>
<li>Class A range
<ul>
<li>Starts at <code>0.0.0.0</code> and ends at <code>127.255.255.255</code>.</li>
<li>Split into 128 class A networks</li>
<li>Handed out to large companies</li>
</ul>
</li>
<li>Class B Range
<ul>
<li>Half the range of class A.</li>
<li>Starts at <code>128.0.0.0</code> and ends at <code>191.255.255.255</code>.</li>
</ul>
</li>
<li>Class C Range
<ul>
<li>Half of range class B</li>
<li>Starts at <code>192.0.0.0</code> and ends at <code>223.255.255.255</code>.</li>
</ul>
</li>
</ul>
<h4><a id="user-content-internet--private-ips---rfc1918" class="anchor" aria-hidden="true" href="#internet--private-ips---rfc1918"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Internet / Private IPs - RFC1918</h4>
<p>These can't communicate over the internet and are used internally only</p>
<ul>
<li>One class A network: <code>10.0.0.0</code> - <code>10.255.255.255</code></li>
<li>16 Class B networks: <code>172.16.0.0</code> - <code>172.31.255.255</code></li>
<li>256 Class C networks: <code>192.168.0.0</code> - <code>192.168.255.255</code></li>
</ul>
<h4><a id="user-content-classless-inter-domain-routing-cidr" class="anchor" aria-hidden="true" href="#classless-inter-domain-routing-cidr"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Classless inter-domain routing (CIDR)</h4>
<p>CIDR networks are represented by the starting IP address of the network
called the network address and the prefix.</p>
<p>CIDR Example: <code>10.0.0.0/16</code></p>
<ul>
<li><code>10.0.0.0</code> is the first address on the network</li>
<li>/16 is the size of the network called the prefix.
<ul>
<li>The bigger the prefix, the smaller the network</li>
<li>The smaller the prefix, the bigger the network.</li>
</ul>
</li>
<li>/16 provides 65,536 addresses.</li>
<li><code>10.0.0.0/17</code> and <code>10.0.128.0/17</code> are each half of the original example.
<ul>
<li>This is called <strong>subnetting</strong></li>
</ul>
</li>
</ul>
<h4><a id="user-content-ip-address-notations-to-remember" class="anchor" aria-hidden="true" href="#ip-address-notations-to-remember"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>IP address notations to remember</h4>
<ul>
<li><code>0.0.0.0/0</code> means all IP addresses</li>
<li><code>10.0.0.0/8</code> means 10.ANYTHING - Class A</li>
<li><code>10.0.0.0/16</code> means 10.0.ANYTHING - Class B</li>
<li><code>10.0.0.0/24</code> means 10.0.0.ANYTHING - Class C</li>
<li><code>10.0.0.0/32</code> means only 1 IP address</li>
</ul>
<p><code>10.0.0.0/16</code> is the equivalent of <code>1234</code> as a password. You should consider
other ranges that people might use to ensure it does not overlap.</p>
<h4><a id="user-content-packets" class="anchor" aria-hidden="true" href="#packets"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Packets</h4>
<p>Contains:</p>
<ul>
<li>source IP address</li>
<li>destination IP address</li>
<li>data the source IP wants to communicate with the destination IP.</li>
</ul>
<p>TCP and UDP are protocols built on top of IP.</p>
<ul>
<li>TCPIP means TCP running with IP</li>
<li>UDPIP means UDP running with IP</li>
</ul>
<p>TCP/UDP Segment has a source and destination port number.
This allows devices to have multiple conversations at the same time.
In AWS when data goes through network devices, filters can be set based on
IP addresses and port numbers.</p>
<h4><a id="user-content-ipv6---rfc-8200-2017" class="anchor" aria-hidden="true" href="#ipv6---rfc-8200-2017"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>IPv6 - RFC 8200 (2017)</h4>
<p><code>2001:0db8:28ac:0000:0000:82ae:3910:7334</code></p>
<p>The value is hex and there are two octets per spacing or one hextet.
The redundant zeros can be removed to create:</p>
<p><code>2001:0db8:28ac:0:0:82ae:3910:7334</code></p>
<p>or you can remove them all entirely once per address</p>
<p><code>2001:0db8:28ac::82ae:3910:7334</code></p>
<p>Each address is 128 bits long. They are addressed by the start of the network
and the prefix.
Since each grouping is 16 values, we can multiple the groups by this to achieve
the prefix.</p>
<p><code>2001:0db8:28ac::/48</code> really means the network starts at
<code>2001:0db8:28ac:0000:0000:0000:0000:0000</code> and finishes at
<code>2001:0db8:28ac:ffff:ffff:ffff:ffff:ffff</code></p>
<p><code>::/0</code> represents all IPv6 addresses</p>
<h3><a id="user-content-vpc-sizing-and-structure" class="anchor" aria-hidden="true" href="#vpc-sizing-and-structure"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>VPC Sizing and Structure</h3>
<p>VPC Consideration</p>
<ul>
<li>What size should the VPC be. This will limit the use.</li>
<li>Are there any networks we can't use?</li>
<li>Be mindful of ranges other VPCs use or are used in other cloud environments</li>
<li>Try to predict the future uses.</li>
<li>VPC structure with tiers and resilience (availability) zones</li>
<li>VPC min /28 network (16 IP)</li>
<li>VPC max /16 (65456 IP)</li>
<li>Avoid common range 10.0 or 10.1, include up to 10.10
<ul>
<li>Suggest starting of 10.16 for a nice clean base 2 number.</li>
</ul>
</li>
</ul>
<p>Reserve 2+ network ranges per region being used per account.
Think of the highest region you will operate in and add extra as a buffer.</p>
<p>An example using 4 AWS accounts.</p>
<ul>
<li>Regions with 2 ranges in each Region
<ul>
<li>3 regions in US</li>
<li>1 region in Europe</li>
<li>1 region in AUS</li>
</ul>
</li>
<li>Total of 40 ranges, 10 ranges for each account.</li>
</ul>
<h4><a id="user-content-how-to-size-vpc" class="anchor" aria-hidden="true" href="#how-to-size-vpc"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>How to size VPC</h4>
<p>A subnet is located in one availability zone.
Try to split each subnet into tiers (web, application, db, spare).
Since each Region has at least 3 AZ's, it is a good practice to start
splitting the network into 4 different AZs.
This allows for at least one subnet in each AZ, and one spare.
Taking a /16 subnet and splitting it 16 ways will make each a /20.</p>
<h3><a id="user-content-custom-vpc" class="anchor" aria-hidden="true" href="#custom-vpc"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Custom VPC</h3>
<ul>
<li>Regional Isolated and Resilient Service.
<ul>
<li>Operates from all AZs in that region</li>
</ul>
</li>
<li>Allows isolated networks inside AWS.</li>
<li>Nothing IN or OUT of a VPC without explicit configuration.
<ul>
<li>Isolated blast radius. Any problems are limited to that VPC or anything
connected to it.</li>
</ul>
</li>
<li>Flexible configuration</li>
<li>Hybrid networking to allow connection to other cloud or on-prem networking.</li>
<li>Default or Dedicated Tenancy. This refers to how the hardware is configured.
<ul>
<li>Default allows on a per resource decision later on.</li>
<li>Dedicated locks any resourced created in that VPC to be on dedicated
hardware which comes at a cost premium.</li>
</ul>
</li>
</ul>
<h4><a id="user-content-custom-vpc-facts" class="anchor" aria-hidden="true" href="#custom-vpc-facts"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Custom VPC Facts</h4>
<p>IPv4 private and public IPs</p>
<ul>
<li>Allocated 1 mandatory private IPv4 CIDR blocks
<ul>
<li>Min /28 prefix (16 IP)</li>
<li>Max /16 prefix (65,536 IP)</li>
</ul>
</li>
<li>Can add secondary IPv4 Blocks after creation.
<ul>
<li>Max of 5, can be increased with a support ticket</li>
<li>When thinking of VPC, it has a pool of private IPv4 addresses and can
use public addresses when needed.</li>
</ul>
</li>
</ul>
<p>Single assigned IPv6 /56 CIDR block</p>
<ul>
<li>Still being matured, not everything works the same as IPv4.</li>
<li>With increasing use of IPv6, this should be added as a default</li>
<li>Range is either allocated by AWS as in you have no choice on which range
to use, or you can select to use your own IPv6 addresses which you own.</li>
<li>IPv6 does not have private addresses, they are all routed as public by
default.</li>
</ul>
<h4><a id="user-content-dns-provided-by-r53" class="anchor" aria-hidden="true" href="#dns-provided-by-r53"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>DNS provided by R53</h4>
<p>Available on the base IP address of the VPC + 2.
If the VPC is <code>10.0.0.0</code> then the DNS IP will be <code>10.0.0.2</code></p>
<p>Two options that manage how DNS works in a VPC:</p>
<ul>
<li>
<p>Edit DNS hostnames</p>
<ul>
<li>If true, instances with public IPs in a VPC are given public DNS hostnames.</li>
<li>If false, this is not available.</li>
</ul>
</li>
<li>
<p>Edit DNS resolution</p>
<ul>
<li>If true, instances in the VPC can use the DNS IP address.</li>
<li>If false, this is not available.</li>
</ul>
</li>
</ul>
<h3><a id="user-content-vpc-subnets" class="anchor" aria-hidden="true" href="#vpc-subnets"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>VPC Subnets</h3>
<ul>
<li>AZ Resilient subnetwork of a VPC.
<ul>
<li>If the AZ fails, the subnet and services also fail.</li>
<li>High availability needs multiple components into different AZs.</li>
</ul>
</li>
<li>1 subnet can only have 1 AZ.</li>
<li>1 AZ can have zero or many subnets.</li>
<li>IPv4 CIDR is a subset of the VPC CIDR block.
<ul>
<li>Cannot overlap with any other subnets in that VPC</li>
</ul>
</li>
<li>Subnet can optionally be allocated IPv6 CIDR block.
<ul>
<li>(256 /64 subnets can fit in the /56 VPC)</li>
</ul>
</li>
<li>Subnets can communicate with other subnets in the VPC by default.</li>
</ul>
<h4><a id="user-content-reserved-ip-addresses" class="anchor" aria-hidden="true" href="#reserved-ip-addresses"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Reserved IP addresses</h4>
<p>There are five IP addresses within every VPC subnet that you cannot use.
Whatever size of the subnet, the IP addresses are five less than you expect.</p>
<p>If using <code>10.16.16.0/20</code> (<code>10.16.16.0</code> - <code>10.16.31.255</code>)</p>
<ul>
<li>Network address: <code>10.16.16.0</code></li>
<li>Network + 1: <code>10.16.16.1</code> - VPC Router</li>
<li>Network + 2: <code>10.16.16.2</code> - Reserved for DNS</li>
<li>Network + 3: <code>10.16.16.3</code> - Reserved for future AWS use</li>
<li>Broadcast Address: <code>10.16.31.255</code> (Last IP in subnet)</li>
</ul>
<h4><a id="user-content-dhcp-options-set" class="anchor" aria-hidden="true" href="#dhcp-options-set"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>DHCP Options Set</h4>
<p>This is how computing devices receive IP addresses automatically. There is
one options set applied to a VPC at one time and this configuration flows
through to subnets.</p>
<ul>
<li>This can be changed, can create new ones, but you cannot edit one.</li>
<li>If you want to change the settings
<ul>
<li>You can create a new one</li>
<li>Change the VPC allocation to the new one</li>
<li>Delete the old one</li>
</ul>
</li>
</ul>
<h4><a id="user-content-ip-allocation-options" class="anchor" aria-hidden="true" href="#ip-allocation-options"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>IP allocation Options</h4>
<ul>
<li>Auto Assign public IPv4 address
<ul>
<li>This will create a public IP address in addition to their private subnet.</li>
<li>This is needed to make a subnet public.</li>
</ul>
</li>
<li>Auto Assign IPv6 address
<ul>
<li>For this to work, the subnet and VPC need an allocation of addresses.</li>
</ul>
</li>
</ul>
<h3><a id="user-content-vpc-routing-and-internet-gateway" class="anchor" aria-hidden="true" href="#vpc-routing-and-internet-gateway"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>VPC Routing and Internet Gateway</h3>
<p>VPC Router is a highly available device available in every VPC which moves
traffic from somewhere to somewhere else.
Router has a network interface in every subnet in the VPC.
Routes traffic between subnets.</p>
<p>Route tables defines what the VPC router will do with traffic
when data leaves that subnet.
A VPC is created with a main route table. If you don't associate a custom
route table with a subnet, it uses the main route table of the VPC.</p>
<p>If you do associate a custom route table you create with a subnet, then the
main route table is disassociated. A subnet can only have one route table
associated at a time, but a route table can be associated by many subnets.</p>
<h4><a id="user-content-route-tables" class="anchor" aria-hidden="true" href="#route-tables"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Route Tables</h4>
<p>When traffic leaves the subnet that this route table is associated with, the
VPC router reviews the IP packets looking for the destination address.
The traffic will try to match the route against the route table. If there
are more than one routes found as a match, the prefix is used as a priority.
The higher the prefix, the more specific the route, thus higher priority.
If the target says local, that means the destination is in the VPC itself.
Local route can never be updated, they're always present and the local route
always takes priority. This is the exception to the prefix rule.</p>
<h4><a id="user-content-internet-gateway" class="anchor" aria-hidden="true" href="#internet-gateway"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Internet Gateway</h4>
<p>A managed service that allows gateway traffic between the VPC and the internet
or AWS Public Zones (S3, SQS, SNS, etc.)</p>
<ul>
<li>Regional resilient gateway attached to a VPC.</li>
<li>One IGW will cover all AZ's in a region the VPC is using.</li>
<li>A VPC can have either:
<ul>
<li>No IGW and be entirely private.</li>
<li>One IGW</li>
</ul>
</li>
<li>IGW can be created and attached to no VPC.</li>
<li>Runs from within the AWS public zone.</li>
</ul>
<h4><a id="user-content-using-igw" class="anchor" aria-hidden="true" href="#using-igw"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Using IGW</h4>
<p>In this example, an EC2 instance has:</p>
<ul>
<li>Private IP address of 10.16.16.20</li>
<li>Public address of 43.250.192.20</li>
</ul>
<p>The public address is not public and connected to the EC2 instance itself.
Instead, the IGW creates a record that links the instance's private IP
to the public IP. This is why when an EC2 instance is created it only
sees the private IP address. This is IMPORTANT. For IPv4 it is not configured
in the OS with the public address.</p>
<p>When the linux instance wants to communicate with the linux update service,
it makes a packet of data.
The packet has a source address of the EC2 instance and a destination address
of the linux update server. At this point the packet is not configured with
any public addressing and could not reach the linux update server.</p>
<p>The packet arrives at the internet gateway.</p>
<p>The IGW sees this is from the EC2 instance and analyzes the source IP address.
It changes the packet source IP address from the linux EC2 server and puts
on the public IP address that is routed from that instance. The IGW then
pushes that packet on the public internet.</p>
<p>On the return, the inverse happens. As far as it is concerned, it does not know
about the private address and instead uses the instance's public IP address.</p>
<p>If the instance uses an IPv6 address, that public address is good to go. The IGW
does not translate the packet and only pushes it to a gateway.</p>
<h4><a id="user-content-bastion-host--jumpbox" class="anchor" aria-hidden="true" href="#bastion-host--jumpbox"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Bastion Host / Jumpbox</h4>
<p>It is an instance in a public subnet inside a VPC.
These are used to allow incoming management connections.
Once connected, you can then go on to access internal only VPC resources.
Used as a management point or as an entry point for a private only VPC.</p>
<p>This is an inbound management point. Can be configured to only allow
specific IP addresses or to authenticate with SSH. It can also integrate
with your on premise identification service.</p>
<h3><a id="user-content-network-access-control-list-nacl" class="anchor" aria-hidden="true" href="#network-access-control-list-nacl"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Network Access Control List (NACL)</h3>
<p>Network Access Control Lists (NACLs) are a type of security filter
(like firewalls) which can filter traffic as it enters or leaves a subnet.</p>
<p>All VPCs have a default NACL, this is associated with all subnets of that VPC
by default.
NACLs are used when traffic enters or leaves a subnet.
Since they are attached to a subnet and not a resource, they only filter
data as it crosses in or out.
If two EC2 instances in a VPC communicate, the NACL does nothing because
it is not involved.</p>
<p>NACLs have an inbound and outbound sets of rules.</p>
<p>When a specific rule set has been called, the one with the lowest
rule number first.
As soon as one rule is matched, the processing stops for
that particular piece of traffic.</p>
<p>The action can be for the traffic to <strong>allow</strong> or <strong>deny</strong> the traffic.</p>
<p>Each rule has the following fields related to traffic</p>
<ul>
<li>type</li>
<li>protocol: tcp, udp, or icmp</li>
<li>port range</li>
<li>Inbound rule: Source - who traffic is from</li>
<li>Outbound rule: Destination - who traffic is destined to</li>
</ul>
<p>Examples:</p>
<ul>
<li>ssh: tcp port 22</li>
<li>http: tcp port 80</li>
<li>https: tcp port 443</li>
<li>ping traffic: icmp</li>
</ul>
<p>If all of those fields match, then the first rule will either allow or deny.</p>
<p>The rule at the bottom with <code>*</code> is the <strong>implicit deny</strong>
This cannot be edited and is defaulted on each rule list.
If no other rules match the traffic being evaluated, it will be denied.</p>
<h4><a id="user-content-nacls-example-below" class="anchor" aria-hidden="true" href="#nacls-example-below"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>NACLs example below</h4>
<ul>
<li>Bob wants to view a blog using https(tcp/443)</li>
<li>We need a NACL rule to allow TCP on port 443.</li>
<li>All IP communication has two parts
<ul>
<li>Initiation</li>
<li>Response</li>
</ul>
</li>
<li>Bob is initiating a connection to the server to ask for a webpage</li>
<li>Server will respond with an <strong>Ephemeral</strong> port</li>
<li>Bob talks to the webserver connecting to a port on that server (tcp/443)
<ul>
<li>This is a well known port number</li>
</ul>
</li>
<li>Bob's PC tells the server it can talk to back to Bob on a specific port
<ul>
<li>Wide range from port 1024, 65535</li>
<li>That response is outbound traffic</li>
</ul>
</li>
<li>When using NACLs, you must add an outbound port for the response traffic
as well as the inbound port. This is the ephemeral port.</li>
<li>If the webserver is not managing the apps server, it may communicate
back on a different port.</li>
<li>This back and forth communication can be hard to configure for.</li>
</ul>
<h4><a id="user-content-nacl-exam-powerup" class="anchor" aria-hidden="true" href="#nacl-exam-powerup"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>NACL Exam PowerUp</h4>
<ul>
<li>NACLs are stateless
<ul>
<li>Initiation and response traffic are separate streams requiring two rules.</li>
</ul>
</li>
<li>NACLs are attached to subnets and only filter data as it crosses the
subnet boundary. Two EC2 instances in the same subnet will not check against
the NACLs when moving data.</li>
<li>Can explicitly allow and deny traffic. If you need to block one particular
thing, you need to use NACLs.</li>
<li>They only see IPs, ports, protocols, and other network connections.
No logical resources can be changed with them.</li>
<li>NACLs cannot be assigned to specific AWS resources.</li>
<li>NACLs can be used with security groups to add explicit deny (Bad IPs/nets)</li>
<li>One subnet can only be assigned to one NACL at a time.</li>
</ul>
<p>NACLs are processed in order starting at the lowest rule number until
it gets to the catch all. A rule with a lower rule number will be processed
before another rule with a higher rule number.</p>
<h3><a id="user-content-security-groups" class="anchor" aria-hidden="true" href="#security-groups"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Security Groups</h3>
<ul>
<li>SGs are boundaries which can filter traffic.</li>
<li>Attached to a resource and not a subnet.</li>
<li>SGs have two sets of rules like NACLs.</li>
<li>SGs are stateful.
<ul>
<li>Only one inbound rule is needed.</li>
<li>They see traffic and response as the same thing.</li>
</ul>
</li>
<li>Understand AWS logical resources so they're not limit to IP traffic only.
<ul>
<li>Can have a source and destination referencing the instance and not the IP.</li>
</ul>
</li>
<li>Default SG is created in a VPC to allow all traffic.
<ul>
<li>Does so by referencing itself. Anything this SG is attached to is matched
by this rule.</li>
</ul>
</li>
<li>SGs have a hidden implicit <strong>Deny</strong>.
<ul>
<li>Anything that is not allowed in the rule set for the SG is implicitly denied.</li>
</ul>
</li>
<li>SG cannot explicit deny anything.
<ul>
<li>NACLs are used in conjunction with SGs to do explicit denys.</li>
</ul>
</li>
</ul>
<h4><a id="user-content-sgs-vs-nacl" class="anchor" aria-hidden="true" href="#sgs-vs-nacl"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>SGs vs NACL</h4>
<ul>
<li>NACLs are used when products cannot use SGs, e.g. NAT Gateways.</li>
<li>NACLs are used when adding explicit deny, such as bad IPs or bad actors.</li>
<li>SGs is the default almost everywhere because they are stateful.</li>
<li>NACLs are associated with a subnet and only filter traffic that crosses
that boundary. If the resource is in the same subnet, it will not do anything.</li>
</ul>
<h3><a id="user-content-network-address-translation-nat-gateway" class="anchor" aria-hidden="true" href="#network-address-translation-nat-gateway"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Network Address Translation (NAT) Gateway</h3>
<p>Set of different processes that can address IP packets by changing
their source or destination addresses.</p>
<p><strong>IP masquerading</strong>, hides CIDR block behind one IP. This allows many IPv4
addresses to use one public IP for <strong>outgoing</strong> internet access.
Incoming connections don't work. Outgoing connections can get a response
returned.</p>
<ul>
<li>Must run from a public subnet to allow for public IP address.
<ul>
<li>Internet Gateway subnets configure to allocate public IPv4 addresses
and default routes for those subnets pointing at the IGW.</li>
</ul>
</li>
<li>Uses Elastic IPs (Static IPv4 Public)
<ul>
<li>Don't change</li>
<li>Allocated to your account</li>
</ul>
</li>
<li>AZ resilient service , but HA in that AZ.
<ul>
<li>If that AZ fails, there is no recovery.</li>
</ul>
</li>
<li>For a fully region resilient service, you must deploy one NATGW in each AZ
with a Route Table in each AZ with NATGW as target.</li>
<li>Managed service, scales up to 45 Gbps. Can deploy multiple NATGW to increase
bandwidth.</li>
<li>AWS charges on usage per hour and data volume processed.</li>
</ul>
<p>NATGW cannot do port forwarding or be a bastion server. In that case it might
be necessary to run a NAT EC2 instance instead.</p>
<hr>
<h2><a id="user-content-elastic-cloud-compute-ec2" class="anchor" aria-hidden="true" href="#elastic-cloud-compute-ec2"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Elastic-Cloud-Compute-EC2</h2>
<p>EC2 provides Infrastructure as a Service (IaaS Product)</p>
<h3><a id="user-content-virtualization-101" class="anchor" aria-hidden="true" href="#virtualization-101"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Virtualization 101</h3>
<p>Servers are configured in three sections without virtualization.</p>
<ul>
<li>CPU hardware</li>
<li>Kernel
<ul>
<li>Operating system</li>
<li>Runs in <strong>privileged mode</strong> and can interact with the hardware directly.</li>
</ul>
</li>
<li>User Mode
<ul>
<li>Runs applications.</li>
<li>Can make a <strong>system call</strong> to the Kernel to interact with the hardware.</li>
<li>If an app tries to interact with the hardware without a system call, it
will cause a system error and can crash the server or at minimum the app.</li>
</ul>
</li>
</ul>
<h4><a id="user-content-emulated-virtualization---software-virtualization" class="anchor" aria-hidden="true" href="#emulated-virtualization---software-virtualization"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Emulated Virtualization - Software Virtualization</h4>
<p>Host OS operated on the HW and included a hypervisor (HV).
SW ran in privileged mode and had full access to the HW.
Guest OS wrapped in a VM and had devices mapped into their OS to emulate real
HW. Drivers such as graphics cards were all SW emulated to allow the process
to run properly.</p>
<p>The guest OS still believed they were running on real HW and tried
to take control of the HW. The areas were not real and only allocated
space to them for the moment.</p>
<p>The HV performs <strong>binary translation</strong>.
System calls are intercepted and translated in SW on the way. The guest OS needs
no modification, but slows down a lot.</p>
<h4><a id="user-content-para-virtualization" class="anchor" aria-hidden="true" href="#para-virtualization"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Para-Virtualization</h4>
<p>Guest OS are modified and run in HV containers, except they do not use slow
binary translation. The OS is modified to change the <strong>system calls</strong> to
<strong>user calls</strong>. Instead of calling on the HW, they call on the HV using
<strong>hypercalls</strong>. Areas of the OS call the HV instead of the HW.</p>
<h4><a id="user-content-hardware-assisted-virtualization" class="anchor" aria-hidden="true" href="#hardware-assisted-virtualization"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Hardware Assisted Virtualization</h4>
<p>The physical HW itself is virtualization aware. The CPU has specific
functions so the HV can come in and support. When guest OS tries to run
privileged instructions, they are trapped by the CPU and do not halt
the process. They are redirected to the HV from the HW.</p>
<p>What matters for a VM is the input and output operations such
as network transfer and disk IO. The problem is multiple OS try to access
the same piece of hardware but they get caught up on sharing.</p>
<h4><a id="user-content-sr-iov-singe-route-io-virtualization" class="anchor" aria-hidden="true" href="#sr-iov-singe-route-io-virtualization"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>SR-IOV (Singe Route IO virtualization)</h4>
<p>Allows a network or any card to present itself as many mini cards.
As far as the HW is concerned, they are real dedicated cards for their
use. No translation needs to be done by the HV. The physical card
handles it all. In EC2 this feature is called <strong>enhanced networking</strong>.</p>
<h3><a id="user-content-ec2-architecture-and-resilience" class="anchor" aria-hidden="true" href="#ec2-architecture-and-resilience"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>EC2 Architecture and Resilience</h3>
<p>EC2 instances are virtual machines run on EC2 hosts.</p>
<p>Tenancy:</p>
<ul>
<li>
<p><strong>Shared</strong> - Instances are run on shared hardware, but isolated from other customers.</p>
</li>
<li>
<p><strong>Dedicated</strong> - Instances are run on hardware that's dedicates to a single customer.
Dedicated instances may share hardware with other instances from the same AWS account
that are not Dedicated instances.</p>
</li>
<li>
<p><strong>Dedicated host</strong> - Instances are run on a physical server fully dedicated for your use.
Pay for entire host, don't pay for instances.</p>
</li>
<li>
<p>AZ resilient service. They run within only one AZ system.</p>
<ul>
<li>You can't access them cross zone.</li>
</ul>
</li>
</ul>
<p>EC2 host contains</p>
<ul>
<li>Local hardware such as CPU and memory</li>
<li>Also have temporary instance store
<ul>
<li>If instance moves hosts, the storage is lost.</li>
</ul>
</li>
<li>Can use remote storage, Elastic Block Store (EBS).
<ul>
<li>EBS allows you to allocate volumes of persistent storage to instances
within the same AZ.</li>
</ul>
</li>
<li>2 types of networking
<ul>
<li>Storage networking</li>
<li>Data networking</li>
</ul>
</li>
</ul>
<p>EC2 Networking (ENI)</p>
<p>When instances are provisioned within a specific subnet within a VPC
A primary elastic network interface is provisioned in a subnet which
maps to the physical hardware on the EC2 host. Subnets are also within
one specific AZ. Instances can have multiple network interfaces, even within
different subnets so long as they're within the same AZ.</p>
<p>An instance runs on a specific host. If you restart the instance
it will stay on that host until either:</p>
<ul>
<li>The host fails or is taken down by AWS</li>
<li>The instance is stopped and then started, different than restarted.</li>
</ul>
<p>The instance will be relocated to another host in the same AZ. Instances
cannot move to different AZs. Everything about their hardware is locked within
one specific AZ.
A migration is taking a <strong>copy</strong> of an instance and moving it to a different AZ.</p>
<p>In general instances of the same type and generation will occupy the same host.
The only difference will generally be their size.</p>
<h4><a id="user-content-ec2-strengths" class="anchor" aria-hidden="true" href="#ec2-strengths"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>EC2 Strengths</h4>
<p>Long running compute needs. Many other AWS services have run time limits.</p>
<p>Server style applications</p>
<ul>
<li>things waiting for network response</li>
<li>burst or stead-load</li>
<li>monolithic application stack
<ul>
<li>middle ware or specific run time components</li>
</ul>
</li>
<li>migrating application workloads or disaster recovery
<ul>
<li>existing applications running on a server and a backup system to intervene</li>
</ul>
</li>
</ul>
<h3><a id="user-content-ec2-instance-types" class="anchor" aria-hidden="true" href="#ec2-instance-types"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>EC2 Instance Types</h3>
<ul>
<li><strong>General Purpose</strong> (T, M) - default steady state workloads with even resources</li>
<li><strong>Compute Optimized</strong> (C) - Media processing, scientific modeling and gaming</li>
<li><strong>Memory Optimized</strong> (R, X) - Processing large in-memory data sets</li>
<li><strong>Accelerated Computing</strong> (P, G, F) - Hardware GPU, FPGAs</li>
<li><strong>Storage Optimized</strong> (H, I, D) - Large amounts of super fast local storage.
Massive amounts of IO per second. Elastic search and analytic workloads.</li>
</ul>
<h4><a id="user-content-naming-scheme" class="anchor" aria-hidden="true" href="#naming-scheme"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Naming Scheme</h4>
<p>R5dn.8xlarge - whole thing is the instance type. When in doubt give the
full instance type</p>
<ul>
<li>1st char: Instance family.</li>
<li>2nd char: Instance generation. Generally always select the newest generation.</li>
<li>char after period: Instance size. Memory and CPU considerations.
<ul>
<li>Often easier to scale system with a larger number of smaller instance sizes.</li>
</ul>
</li>
<li>3rd char - before period: additional capabilities
<ul>
<li>a: amd cpu</li>
<li>d: NVMe storage</li>
<li>n: network optimized</li>
<li>e: extra capacity for ram or storage</li>
</ul>
</li>
</ul>
<h3><a id="user-content-storage-refresher" class="anchor" aria-hidden="true" href="#storage-refresher"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Storage Refresher</h3>
<ul>
<li><strong>Instance Store</strong>
<ul>
<li>Direct (local) attached storage</li>
<li>Super fast</li>
<li>Ephemeral storage or temporary storage</li>
</ul>
</li>
<li><strong>Elastic Block Store (EBS)</strong>
<ul>
<li>Network attached storage</li>
<li>Volumes delivered over the network</li>
<li>Persistent storage lives on past the lifetime of the instance</li>
</ul>
</li>
</ul>
<h4><a id="user-content-three-types-of-storage" class="anchor" aria-hidden="true" href="#three-types-of-storage"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Three types of storage</h4>
<ul>
<li>
<p>Block Storage: Volume presented to the OS as a collection of blocks. No
structure beyond that. These are mountable and bootable. The OS will
create a file system on top of this, NTFS or EXT3 and then it mounts
it as a drive or a root volume on Linux. Spinning hard disks or SSD. This
could also be delivered by a physical volume. Has no built in structure.
You can mount an EBS volume or boot off an EBS volume.</p>
</li>
<li>
<p>File Storage: Presented as a file share with a structure. You access the
files by traversing the storage. You cannot boot from storage, but you
can mount it.</p>
</li>
<li>
<p>Object Storage: It is a flat collection of objects. An object can be anything
with or without attached metadata. To retrieve the object, you need to provide
the key and then the value will be returned. This is not mountable or
bootable. It scales very well and can have simultaneous access.</p>
</li>
</ul>
<h4><a id="user-content-storage-performance" class="anchor" aria-hidden="true" href="#storage-performance"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Storage Performance</h4>
<ul>
<li>IO Block Size: Determines how to split up the data.</li>
<li>IOPS: How many reads or writes a system can accommodate per second.</li>
<li>Throughput: End rate achieved, expressed in MB/s (megabyte per second).</li>
</ul>
<p><code>Block Size * IOPS = Throughput</code></p>
<p>This isn't the only part of the chain, but it is a simplification.
A system might have a throughput cap. The IOPS might decrease as the block
size increases.</p>
<h3><a id="user-content-elastic-block-store-ebs" class="anchor" aria-hidden="true" href="#elastic-block-store-ebs"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Elastic Block Store (EBS)</h3>
<ul>
<li>Allocate block storage <strong>volumes</strong> to instances.</li>
<li>Volumes are isolated to one AZ.
<ul>
<li>The data is highly available and resilient for that AZ.</li>
<li>All of the data is replicated within that AZ. The entire AZ must have
a major fault to go down.</li>
</ul>
</li>
<li>Two physical storage types available (SSD/HDD)</li>
<li>Varying level of performance (IOPS, T-put)</li>
<li>Billed as GB/month.
<ul>
<li>If you provision a 1TB for an entire month, you're billed as such.</li>
<li>If you have half of the data, you are billed for half of the month.</li>
</ul>
</li>
<li>Four types of volumes, each with a dominant performance attribute.
<ul>
<li>General purpose SSD (gp2)</li>
<li>Provisioned IOPS SSD (io1)
<ul>
<li>maximum IOPS such as databases</li>
</ul>
</li>
<li>T-put optimized HDD (st1)
<ul>
<li>maximum t-put for logs or media storage</li>
</ul>
</li>
<li>Cold HDD (sc1)</li>
</ul>
</li>
</ul>
<h4><a id="user-content-general-purpose-ssd-gp2" class="anchor" aria-hidden="true" href="#general-purpose-ssd-gp2"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>General Purpose SSD (gp2)</h4>
<p>Uses a performance bucket architecture based on the IOPS it can deliver.
The GP2 starts with 5,400,000 IOPS allocated. It is all available instantly.</p>
<p>You can consume the capacity quickly or slowly over the life of the volume.
The capacity is filled back based upon the volume size.
Min of 100 IOPS added back to the bucket per second.</p>
<p>Above that, there are 3 IOPS/GiB of volume size. The max is 16,000 IOPS.
This is the <strong>baseline performance</strong></p>
<p>Default for boot volumes and should be the default for data volumes.
Can only be attached to one EC2 instance at a time.</p>
<h4><a id="user-content-provisioned-iops-ssd-io1" class="anchor" aria-hidden="true" href="#provisioned-iops-ssd-io1"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Provisioned IOPS SSD (io1)</h4>
<p>You pay for capacity and the IOPs set on the volume.
This is good if your volume size is small but need a lot of IOPS.</p>
<p>50:1 IOPS to GiB Ratio
64,000 is the max IOPS per volume assuming 16 KiB I/O.</p>
<p>Good for latency sensitive workloads such as mongoDB.
Multi-attach allows them to attach to multiple EC2 instances at once.</p>
<h4><a id="user-content-hdd-volume-types" class="anchor" aria-hidden="true" href="#hdd-volume-types"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>HDD Volume Types</h4>
<ul>
<li>great value</li>
<li>great for high throughput vs IOPs</li>
<li>500 GiB - 16 TiB</li>
<li>Neither can be used for EC2 boot volumes.</li>
<li>Good for streaming data on a hard disk.
<ul>
<li>Media conversion with large amounts of storage.</li>
</ul>
</li>
<li>Frequently accessed high throughput intensive workload
<ul>
<li>log processing</li>
<li>data warehouses</li>
</ul>
</li>
<li>The access patterns should be sequential
<ul>
<li>Massive inefficiency for small reads and writes</li>
</ul>
</li>
</ul>
<p>Two types</p>
<ul>
<li>st1
<ul>
<li>Starts at 1 TiB of credit per TiB of volume size.</li>
<li>40 MB/s baseline per TiB</li>
<li>Burst of 250 MB/s per TiB</li>
<li>Max t-put of 500 MB/s</li>
</ul>
</li>
<li>sc1
<ul>
<li>Designed for less frequently accessed data, it fills slower.</li>
<li>12 MB/s baseline per TiB</li>
<li>Burst of 80 MB/s per TiB</li>
<li>Max t-put of 250 MB/s</li>
</ul>
</li>
</ul>
<h4><a id="user-content-ebs-exam-power-up" class="anchor" aria-hidden="true" href="#ebs-exam-power-up"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>EBS Exam Power Up</h4>
<ul>
<li>Volumes are created in an AZ, isolated in that AZ.</li>
<li>If an AZ fails, the volume is impacted.</li>
<li>Highly available and resilient in that AZ. The only reason for failure is
if the whole AZ fails.</li>
<li>Generally one volume to one instance, except <strong>io1</strong> with multi-attach</li>
<li>Has a GB/m fee regardless of instance state.</li>
<li>EBS maxes at 80k IOPS per instance and 64k vol (io1)</li>
<li>Max 2375 MB/s per instance, 1000 MiB/s (vol) (io1)</li>
</ul>
<h3><a id="user-content-ec2-instance-store" class="anchor" aria-hidden="true" href="#ec2-instance-store"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>EC2 Instance Store</h3>
<ul>
<li>Local <strong>block storage</strong> attached to an instance.</li>
<li>Physically connected to one EC2 host.
<ul>
<li>They are isolated to that one specific host.</li>
<li>Instances on that host can access them.</li>
</ul>
</li>
<li>Highest storage performance in AWS.</li>
<li>Included in instance price, use it or lose it.</li>
<li>Can be attached ONLY at launch. Cannot be attached later.</li>
</ul>
<p>Each instance has a collection of volumes that are
locked to that specific host. If the instance moves, the data doesn't.</p>
<p>Instances can move between hosts for many reasons:</p>
<ul>
<li>If an instance is stopped and started, that migrates hosts.</li>
<li>If a host undergoes AWS maintenance, it will be wiped.</li>
<li>If you change the type of an instance, these will be lost.</li>
<li>If a physical hardware fails, then the data is gone.</li>
</ul>
<p>The number, size, and performance of instance store volumes vary based on the
type of instance used. Some instances do not have any instance store volumes
at all.</p>
<h4><a id="user-content-instance-store-exam-powerup" class="anchor" aria-hidden="true" href="#instance-store-exam-powerup"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Instance Store Exam PowerUp</h4>
<ul>
<li>Instance store volumes are local to EC2 host.</li>
<li>Can only be added at launch time. Cannot be added later.</li>
<li>Any data on instance store data is lost if it gets moved, or resized.</li>
<li>Highest data performance in all of AWS.</li>
<li>You pay for it anyway, it's included in the price.</li>
<li>TEMPORARY</li>
</ul>
<h3><a id="user-content-ebs-vs-instance-store" class="anchor" aria-hidden="true" href="#ebs-vs-instance-store"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>EBS vs Instance Store</h3>
<p>If the read/write can be handled by EBS, that should be default.</p>
<p>When to use EBS</p>
<ul>
<li>Highly available and reliable in an AZ. Can self correct against HW issues.</li>
<li>Persist independently from EC2 instances.
<ul>
<li>Can be removed or reattached.</li>
<li>You can terminated instance and keep the data.</li>
</ul>
</li>
<li>Multi-attach feature of <strong>io1</strong>
<ul>
<li>Can create a multi shared volume.</li>
</ul>
</li>
<li>Region resilient backups.</li>
<li>Require up to 64,000 IOPS and 1,000 MiB/s per volume</li>
<li>Require up to 80,000 IOPS and 2,375 MB/s per instance</li>
</ul>
<p>When to use Instance Store</p>
<ul>
<li>Great value, they're included in the cost of an instance.</li>
<li>More than 80,000 IOPS and 2,375 MB/s</li>
<li>If you need temporary storage, or can handle volatility.</li>
<li>Stateless services, where the server holds nothing of value.</li>
<li>Rigid lifecycle link between storage and the instance.
<ul>
<li>This ensures the data is erased when the instance goes down.</li>
</ul>
</li>
</ul>
<h3><a id="user-content-ebs-snapshots-restore-and-fast-snapshot-restore" class="anchor" aria-hidden="true" href="#ebs-snapshots-restore-and-fast-snapshot-restore"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>EBS Snapshots, restore, and fast snapshot restore</h3>
<ul>
<li>Efficient way to backup EBS volumes to S3.
<ul>
<li>The data becomes region resilient.</li>
</ul>
</li>
<li>Can be used to migrate data between hosts.</li>
</ul>
<p>Snapshots are incremental volume copies to S3.
The first is a <strong>full copy</strong> of <code>data</code> on the volume. This can take some time.
EBS won't be impacted, but will take time in the background.
Future snaps are incremental, consume less space and are quicker to perform.</p>
<p>If you delete an incremental snapshot, it moves data to ensure subsequent
snapshots will work properly.</p>
<p>Volumes can be created (restored) from snapshots.
Snapshots can be used to move EBS volumes between AZs.
Snapshots can be used to migrate data between volumes.</p>
<h4><a id="user-content-snapshot-and-volume-performance" class="anchor" aria-hidden="true" href="#snapshot-and-volume-performance"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Snapshot and volume performance</h4>
<ul>
<li>When creating a new EBS volume without a snapshot, the performance is
available immediately.</li>
<li>When restoring from S3, performs <strong>Lazy Restore</strong>
<ul>
<li>If you restore a volume, it will transfer it slowly in the background.</li>
<li>If you attempt to read data that hasn't been restored yet, it will
immediately pull it from S3, but this will achieve lower levels of performance
than reading from EBS directly.</li>
<li>You can force a read of every block all data immediately using DD.</li>
</ul>
</li>
</ul>
<p>Fast Snapshot Restore (FSR) allows for immediate restoration.
You can create 50 of these FSRs per region. When you enable it on
a snapshot, you pick the snapshot specifically and the AZ that you want to be
able to do instant restores to. Each combination of Snapshot and AZ counts
as one FSR set. You can have 50 FSR sets per region.
FSR is not free and can get expensive with lost of different snapshots.</p>
<h4><a id="user-content-snapshot-consumption-and-billing" class="anchor" aria-hidden="true" href="#snapshot-consumption-and-billing"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Snapshot Consumption and Billing</h4>
<p>Billed using a GB/month metric.
20 GB stored for half a month, represents 10 GB-month.</p>
<p>This is used data, not allocated data. If you have a 40 GB volume but only
use 10 GB, you will only be charged for the allocated data.
This is not how EBS itself works.</p>
<p>The data is incrementally stored which means doing a snapshot every 5 minutes
will not necessarily increase the charge as opposed to doing one every hour.</p>
<h4><a id="user-content-ebs-encryption" class="anchor" aria-hidden="true" href="#ebs-encryption"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>EBS Encryption</h4>
<p>Provides at rest encryption for block volumes and snapshots.</p>
<p>When you don't have EBS encryption, the volume is not encrypted.
The physical hardware itself may be performing at rest encryption, but
that is a separate thing.</p>
<p>When you set up an EBS volume initially, EBS uses KMS and a customer master key.
This can be the EBS default (CMK) which is referred to as <code>aws/ebs</code> or it
could be a customer managed CMK which you manage yourself.</p>
<p>That key is used by EBS when an encrypted volume is created. The CMK
generates an encrypted data encryption key which is stored on the volume with
the physical disk. This key can only be encrypted by KMS when a role with
the proper permissions makes the request.</p>
<p>When the volume is first used, EBS asks CMS to decrypt the key and stores
the decrypted key in memory on the EC2 host while it's being used. At all
other times it's stored on the volume in encrypted form.</p>
<p>When the EC2 instance is using the encrypted volume, it can use the
decrypted data encryption key to move data on and off the volume. It is used
for all cryptographic operations when data is being used to and from the
volume.</p>
<p>When data is stored at rest, it is stored as ciphertext.</p>
<p>If the EBS volume is ever moved, the key is discarded.</p>
<p>If a snapshot is made of an encrypted EBS volume, the same data encryption
key is used for that snapshot. Anything made from this snapshot is also
encrypted in the same way.</p>
<p>Every time you create a new EBS volume from scratch, it creates a new
data encryption key.</p>
<h5><a id="user-content-ebs-encryption-exam-power-up" class="anchor" aria-hidden="true" href="#ebs-encryption-exam-power-up"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>EBS Encryption Exam Power Up</h5>
<ul>
<li>AWS accounts can be set to encrypt EBS volumes by default.
<ul>
<li>It will use the default CMK unless a different one is chosen.</li>
<li>Each volume uses 1 unique DEK (data encryption key)</li>
<li>Snapshots and future volume use the same DEK</li>
</ul>
</li>
<li>Can't change a volume to NOT be encrypted.
<ul>
<li>You could mount an unencrypted volume and copy things over but you can't
change the original volume.</li>
</ul>
</li>
<li>The OS itself isn't aware of the encryption, there is no performance loss.
<ul>
<li>The volume itself is encrypted using AES256</li>
<li>This occurs between the EC2 host and the EBS system itself.</li>
<li>The OS does not see any encryption. It simply writes data out and reads
data in from a disk.</li>
<li>If an exam question does not use AES256, or it suggests you need an OS to
encrypt or hold the keys, then you need to perform full disk encryption
at the operating system level.</li>
</ul>
</li>
</ul>
<h3><a id="user-content-ec2-network-interfaces-instance-ips-and-dns" class="anchor" aria-hidden="true" href="#ec2-network-interfaces-instance-ips-and-dns"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>EC2 Network Interfaces, Instance IPs and DNS</h3>
<p>An EC2 instance starts with at least one ENI - elastic network interface.
An instance may have ENIs in separate subnets, but everything must be
within one AZ.</p>
<p>When you launch an instance with Security Groups, they are on the
network interface and not the instance.</p>
<h4><a id="user-content-elastic-network-interface-eni" class="anchor" aria-hidden="true" href="#elastic-network-interface-eni"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Elastic Network Interface (ENI)</h4>
<p>Has these properties</p>
<ul>
<li>MAC address</li>
<li>Primary IPv4 private address
<ul>
<li>From the range of the subnet the ENI is within.</li>
<li>Will be static and not change for the lifetime of the instance
<ul>
<li><code>10.16.0.10</code></li>
</ul>
</li>
<li>Given a DNS name that is associated with the address.
<ul>
<li><code>ip-10-16-0-10.ec2.internal</code></li>
<li>Only resolvable inside the VPC and always points at private IP address</li>
</ul>
</li>
</ul>
</li>
<li>0 or more secondary private IP addresses</li>
<li>0 or 1 public IPv4 address
<ul>
<li>The instance must manually be set to receive an IPv4 address or spun into a
subnet which automatically allocates an IPv4.
This is a dynamic IP that is not fixed.
If you stop an instance the address is removed.
When you start up again, it is given a brand new IPv4 address.
Restarting the instance will not change the IP address.
Changing between EC2 hosts will change the address.
This will be allocated a public DNS name. The Public DNS name will resolve to
the primary private IPv4 address of the instance.
Outside of the VPC, the DNS will resolve to the public IP address.
This allows one single DNS name for an instance, and allows traffic to resolve
to an internal address inside the VPC and the public will resolve to a public
IP address.</li>
</ul>
</li>
<li>1 elastic IP per private IPv4 address
<ul>
<li>Can have 1 public elastic interface per private IP address on this interface.
This is allocated to your AWS account.
Can associate with a private IP on the primary interface or secondary interface.
If you are using a public IPv4 and assign an elastic IP, the original IPv4
address will be lost. There is no way to recover the original address.</li>
</ul>
</li>
<li>0 or more IPv6 address on the interface
<ul>
<li>These are by default public addresses.</li>
</ul>
</li>
<li>Security groups
<ul>
<li>Applied to network interfaces.</li>
<li>Will impact all IP addresses on that interface.</li>
<li>If you need different IP addresses impacted by different security
groups, then you need to make multiple interfaces and apply different
security groups to those interfaces.</li>
</ul>
</li>
<li>Source / destination checks
<ul>
<li>If traffic is on the interface, it will be discarded if it is not
from going to or coming from one of the IP addresses</li>
</ul>
</li>
</ul>
<p>Secondary interfaces function in all the same ways as primary interfaces except
you can detach interfaces and move them to other EC2 instances.</p>
<h4><a id="user-content-eni-exam-powerup" class="anchor" aria-hidden="true" href="#eni-exam-powerup"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>ENI Exam PowerUp</h4>
<ul>
<li>Legacy software is licensed using a mac address.
<ul>
<li>If you provision a secondary ENI to a specific license, you can move
around the license to different EC2 instances.</li>
</ul>
</li>
<li>Multi homed (subnets) management and data.</li>
<li>Different security groups are attached to different interfaces.</li>
<li>The OS doesn't see the IPv4 public address.</li>
<li>You always configure the private IPv4 private address on the interface.</li>
<li>Never configure an OS with a public IPv4 address.</li>
<li>IPv4 Public IPs are Dynamic, starting and stopping will kill it.</li>
</ul>
<p>Public DNS for a given instance will resolve to the primary private IP
address in a VPC. If you have instance to instance communication within
the VPC, it will never leave the VPC. It does not need to touch the internet
gateway.</p>
<h3><a id="user-content-amazon-machine-image-ami" class="anchor" aria-hidden="true" href="#amazon-machine-image-ami"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Amazon Machine Image (AMI)</h3>
<p>Images of EC2 instances that can launch more EC2 instance.</p>
<ul>
<li>When you launch an EC2 instance, you are using an Amazon provided AMI.</li>
<li>Can be Amazon or community provided</li>
<li>Marketplace (can include commercial software)
<ul>
<li>Will charge you for the instance cost and an extra cost for the AMI</li>
</ul>
</li>
<li>AMIs are regional with a unique ID.</li>
<li>Controls permissions
<ul>
<li>Default only your account can use it.</li>
<li>Can be set to be public.</li>
<li>Can have specific AWS accounts on the AMI.</li>
</ul>
</li>
<li>Can create an AMI from an existing EC2 instance to capture the current config.</li>
</ul>
<h4><a id="user-content-ami-lifecycle" class="anchor" aria-hidden="true" href="#ami-lifecycle"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>AMI Lifecycle</h4>
<ol>
<li>
<p>Launch: EBS volumes are attached to EC2 devices using block IDs.</p>
<ul>
<li>BOOT /dev/xvda</li>
<li>DATA /dev/xvdf</li>
</ul>
</li>
<li>
<p>Configure: customize the instance from applications or volume sizes.</p>
</li>
<li>
<p>Create Image or AMI</p>
<ul>
<li>AMI contains:
<ul>
<li>Permissions: who can use it, is it public or private</li>
<li>EBS snapshots are created from attached EBS volumes
<ul>
<li>Snapshots are referenced inside the AMI using block device mapping.</li>
<li>Table of data that links the snapshot IDs that you've just
created when making that AMI and it has for each one of those
snapshots, a device ID that the original volumes had on the EC2
instance.</li>
</ul>
</li>
</ul>
</li>
</ul>
</li>
<li>
<p>Launch: When launching an instance, the snapshots are used to create new EBS
volumes in the AZ of the EC2 instance and contain the same block device mapping.</p>
</li>
</ol>
<h4><a id="user-content-ami-exam-powerups" class="anchor" aria-hidden="true" href="#ami-exam-powerups"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>AMI Exam PowerUps</h4>
<ul>
<li>AMI can only be used in one region</li>
<li>AMI Baking: creating an AMI from a configuration instance.</li>
<li>An AMI cannot be edited. If you need to update an AMI, launch an instance,
make changes, then make new AMI</li>
<li>Can be copied between regions</li>
<li>Remember permissions by default are your account only</li>
<li>Billing is for the storage capacity for the EBS snapshots the AMI references.</li>
</ul>
<h3><a id="user-content-ec2-pricing-models" class="anchor" aria-hidden="true" href="#ec2-pricing-models"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>EC2 Pricing Models</h3>
<h4><a id="user-content-on-demand-instances" class="anchor" aria-hidden="true" href="#on-demand-instances"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>On-Demand Instances</h4>
<ul>
<li>Hourly rate based on OS, size, options, etc</li>
<li>Billed in seconds (60s min) or hourly
<ul>
<li>Depends on the OS</li>
</ul>
</li>
<li>Default pricing model</li>
<li>No long-term commitments or upfront payments</li>
<li>New or uncertain application requirements</li>
<li>Short-term, spiky, or unpredictable workloads which can't tolerate disruption.</li>
</ul>
<h4><a id="user-content-spot-instances" class="anchor" aria-hidden="true" href="#spot-instances"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Spot Instances</h4>
<p>Up to 90% off on-demand, but depends on the spare capacity.
You can set a maximum hourly rate in a certain AZ in a certain region.
If the max price you set is above the spot price, you pay only that spot
price for the duration that you consume that instance.
As the spot price increases, you pay more.
Once this price increases past your maximum, it will terminate the instance.
Great for data analytics when the process can occur later at a lower use time.</p>
<h4><a id="user-content-reserved-instance" class="anchor" aria-hidden="true" href="#reserved-instance"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Reserved Instance</h4>
<p>Up to 75% off on-demand.
The trade off is commitment.
You're buying capacity in advance for 1 or 3 years.
Flexibility on how to pay</p>
<ul>
<li>All up front</li>
<li>Partial upfront</li>
<li>No upfront</li>
</ul>
<p>Best discounts are for 3 years all up front.
Reserved in region, or AZ with capacity reservation.
Reserved instances takes priority for AZ capacity.
Can perform scheduled reservation when you can commit to specific time windows.</p>
<p>Great if you have a known stead state usage, email usage, domain server.
Cheapest option with no tolerance for disruption.</p>
<h3><a id="user-content-instance-status-checks-and-autorecovery" class="anchor" aria-hidden="true" href="#instance-status-checks-and-autorecovery"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Instance Status Checks and Autorecovery</h3>
<p>Every instance has two high level status checks</p>
<ul>
<li>System Status Checks
<ul>
<li>Failure of this check could indicate SW or HW problems of the EC2
service or the host.</li>
</ul>
</li>
<li>Instance Status Checks
<ul>
<li>Specific to the file system or has a corrupted Kernel.</li>
</ul>
</li>
</ul>
<p>Autorecovery can kick in and help,</p>
<ul>
<li>Recover this instance
<ul>
<li>can be a number of steps depending on the failure</li>
</ul>
</li>
<li>Stop this instance</li>
<li>Terminate this instance
<ul>
<li>useful in a cluster</li>
</ul>
</li>
<li>Reboot this instance</li>
</ul>
<h3><a id="user-content-horizontal-and-vertical-scaling" class="anchor" aria-hidden="true" href="#horizontal-and-vertical-scaling"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Horizontal and Vertical Scaling</h3>
<h4><a id="user-content-vertical-scaling" class="anchor" aria-hidden="true" href="#vertical-scaling"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Vertical Scaling</h4>
<p>As customer load increases, the server may need to grow to handle more data.
The server can increase in capacity, but this will require a reboot.</p>
<ul>
<li>Often times vertical scaling can only occur during planned outages.</li>
<li>Larger instances also carry a $ premium compared to smaller instances.</li>
<li>Instance size is an upper cap on performance.</li>
<li>No application modification is needed.
<ul>
<li>Works for all applications, even monoliths (all code in one app)</li>
</ul>
</li>
</ul>
<h4><a id="user-content-horizontal-scaling" class="anchor" aria-hidden="true" href="#horizontal-scaling"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Horizontal Scaling</h4>
<p>As the customer load increases, this adds additional capacity.
Instead of one running copy of an application, you can have multiple versions
running on each server.
This requires a load balancer.
When customers try to access an application, the load balancer ensures the
servers get equal parts of the load.</p>
<ul>
<li>Sessions are everything.</li>
<li>With horizontal scaling you can shift between instances equally.</li>
<li>This requires either application support or off-host sessions.</li>
<li>Servers are <strong>stateless</strong>, the app stores session data elsewhere.</li>
<li>No disruption while scaling up or down.</li>
<li>No real limits to scaling.</li>
<li>Uses smaller instances so you pay less, allows for better granularity.</li>
</ul>
<h3><a id="user-content-instance-metadata" class="anchor" aria-hidden="true" href="#instance-metadata"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Instance Metadata</h3>
<p>EC2 service provides data to instances
Accessible inside all instances</p>
<p>Memorize <code>http://169.254.169.254/latest/meta-data/</code></p>
<p>Meta-data contains information on the environment the instance is in.
You can find out about the networking or user-data among other things.
This is not authenticated or encrypted. Anyone who can gain access to the
instance can see the meta-data. This can be restricted by local firewall</p>
<hr>
<h2><a id="user-content-containers-and-ecs" class="anchor" aria-hidden="true" href="#containers-and-ecs"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Containers-and-ECS</h2>
<h3><a id="user-content-intro-to-containers" class="anchor" aria-hidden="true" href="#intro-to-containers"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Intro to Containers</h3>
<p>Virtualization Problems</p>
<p>Using an EC2 virtual machine with Nitro Hypervisor, 4 GB ram, and 40 GB disk,
the OS can consume 60-70% of the disk and much of the available memory.
Containers leverage the similarities of multiple guest OS by removing duplicate
resources. This allows applications to run in their own isolated environments.</p>
<h4><a id="user-content-image-anatomy" class="anchor" aria-hidden="true" href="#image-anatomy"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Image Anatomy</h4>
<p>A Docker image is composed of multiple layers and not a monolithic disk image.
Each line of a Docker image creates a new filesystem layer on top of the
previous. Images are created from scratch or a base image.
Images contain read only layers, images are layer onto images.</p>
<p>Docker container is the same as a Docker image, except it
has an additional READ/WRITE layer of the container.</p>
<p>If you have lots of containers with very similar base
structures, they will share the parts that overlap.
The other layers are reused between containers.</p>
<h4><a id="user-content-container-registry" class="anchor" aria-hidden="true" href="#container-registry"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Container Registry</h4>
<p>Registry or hub of container images.
Dockerfile can create a container image where it gets stored
in the container registry.</p>
<p>Docker hosts can run many containers based on one or more images.
A single image can generate Containers on many different Docker hosts.</p>
<h4><a id="user-content-container-key-concepts" class="anchor" aria-hidden="true" href="#container-key-concepts"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Container Key Concepts</h4>
<ul>
<li>Docker files are used to build Docker images</li>
<li>Containers are portable and always run as expected.
<ul>
<li>Anywhere there is a compatible host, it will run exactly as you intended.</li>
</ul>
</li>
<li>Containers are lightweight, use the host OS for the heavy lifting.
<ul>
<li>File system layers are shared when possible.</li>
</ul>
</li>
<li>Containers only run the application and environment it needs to run.</li>
<li>Ports need to be <strong>exposed</strong> to allow outside access from the host and beyond.</li>
<li>Application stacks can be multi container</li>
</ul>
<h3><a id="user-content-elastic-container-service-ecs-concepts" class="anchor" aria-hidden="true" href="#elastic-container-service-ecs-concepts"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Elastic Container Service (ECS) Concepts</h3>
<ul>
<li>Accepts containers and instructions you provide.</li>
<li>ECS allows you to create a cluster.
<ul>
<li>Clusters are where containers run from.</li>
</ul>
</li>
<li>Container images will be located on a registry.
<ul>
<li>AWS provides ECR (elastic container registry)</li>
<li>Dockerhub can be used as well.</li>
</ul>
</li>
<li><strong>Container definition</strong> gives ECS just enough info about the single container.
<ul>
<li>A pointer to which image to use and the ports that will be exposed.</li>
</ul>
</li>
<li><strong>Task definitions</strong> store the resources used by the task.
<ul>
<li>Stores <strong>task role</strong>, an IAM role that allows the task access to other
AWS resources.</li>
</ul>
</li>
<li>Task is not by itself highly available.</li>
</ul>
<p>ECS <strong>Service</strong> is configured via Service Definition and represents
how many copies of a task you want to run for scaling and HA.</p>
<h3><a id="user-content-ecs-cluster-types" class="anchor" aria-hidden="true" href="#ecs-cluster-types"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>ECS Cluster Types</h3>
<p>ECS Cluster manages:</p>
<ul>
<li>Scheduling and Orchestration</li>
<li>Cluster manager</li>
<li>Placement engine</li>
</ul>
<h4><a id="user-content-ec2-mode" class="anchor" aria-hidden="true" href="#ec2-mode"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>EC2 mode</h4>
<p>ECS cluster is created within a VPC. It benefits from the multiple AZs that
are within that VPC.
You specify an initial size which will drive an <strong>auto scaling group</strong>.</p>
<p>ECS using EC2 mode is not a serverless solution, you need to worry about
capacity for your cluster.</p>
<p>The container instances are not delivered as a managed service, they
are managed as normal EC2 instances.
You can use spot pricing or prepaid EC2 servers.</p>
<h4><a id="user-content-fargate-mode" class="anchor" aria-hidden="true" href="#fargate-mode"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Fargate mode</h4>
<p>Removes more of the management overhead from ECS, no need to manage EC2.</p>
<p><strong>Fargate shared infrastructure</strong> allows all customers
to access from the same pool of resources.</p>
<p>Fargate deployment still uses a cluster with a VPC where AZs are specified.</p>
<p>For ECS tasks, they are injected into the VPC. Each task is given an
elastic network interface which has an IP address within the VPC. They then
run like a VPC resource.</p>
<p>You only pay for the container resources you use.</p>
<h4><a id="user-content-ec2-vs-ecsec2-vs-fargate" class="anchor" aria-hidden="true" href="#ec2-vs-ecsec2-vs-fargate"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>EC2 vs ECS(EC2) vs Fargate</h4>
<p>If you already are using containers, use <strong>ECS</strong>.</p>
<p><strong>EC2 mode</strong> is good for a large workload if you are price conscious.
This allows for spot pricing and prepayment.</p>
<p><strong>Fargate</strong> is great if you,</p>
<ul>
<li>Have a large workload but are overhead conscious.</li>
<li>Have small or burst style workloads.</li>
<li>Use batch or periodic workloads.</li>
</ul>
<hr>
<h2><a id="user-content-advanced-ec2" class="anchor" aria-hidden="true" href="#advanced-ec2"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Advanced-EC2</h2>
<h3><a id="user-content-bootstrapping-ec2-using-user-data" class="anchor" aria-hidden="true" href="#bootstrapping-ec2-using-user-data"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Bootstrapping EC2 using User Data</h3>
<p>Bootstrapping is a process where scripts or other config steps can be run when
an instance is first launched. This allows an instance to be brought to service
in a particular configured state.</p>
<p>In systems automation, bootstrapping allows the system to self configure.
In AWS this is <strong>EC2 Build Automation</strong>.</p>
<p>This could perform some software installs and post install configs.</p>
<p>Bootstrapping is done using <strong>user data</strong> and is injected into the instance
in the same way that meta-data is. It is accessed using the meta-data IP.</p>
<p><a href="http://169.254.169.254/latest/" rel="nofollow">http://169.254.169.254/latest/</a></p>
<p>Anything you pass in is executed by the instance OS only once on launch!</p>
<p>EC2 doesn't validate the user data. You can tell EC2 to pass in trash data
and the data will be injected. The OS needs to understand the user data.</p>
<h4><a id="user-content-bootstrapping-architecture" class="anchor" aria-hidden="true" href="#bootstrapping-architecture"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Bootstrapping Architecture</h4>
<p>An AMI is used to launch an EC2 instance in the usual way to create
an EBS volume that is attached to the EC2 instance. This is based on the
block mapping inside the AMI.</p>
<p>Now the EC2 service provides some user data through to the EC2 instance.
There is SW within the OS designed to look at the metadata IP for any user data.
If it sees any user data, it executes this on launch of that instance.</p>
<p>This is treated like any other script the OS runs. At the end of running
the script, the instance will be in:</p>
<ul>
<li>Running state and ready for service.</li>
<li>Bad config but still likely running.
<ul>
<li>The instance will probably still pass its checks.</li>
<li>It will not be configured as you expected.</li>
</ul>
</li>
</ul>
<h4><a id="user-content-user-data-key-points" class="anchor" aria-hidden="true" href="#user-data-key-points"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>User Data Key Points</h4>
<p>EC2 doesn't know what the user data contains, it's just a block of data.
The user data is not secure, anyone can see what gets passed in. For this
reason it is important not to pass passwords or long term credentials.</p>
<p>User data is limited to 16 KB in size. Anything larger than this will
need to pass a script to download the larger set of data.</p>
<p>User data can be modified if you stop the instance, change the user
data, then restart the instance. This won't be executed since the instance
has already started.</p>
<h4><a id="user-content-boot-time-to-service-time" class="anchor" aria-hidden="true" href="#boot-time-to-service-time"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Boot-Time-To-Service-Time</h4>
<p>How quickly after you launch an instance is it ready for service?
This includes the time for EC2 to configure the instance and any software
downloads that are needed for the user.
When looking at an AMI, this can be measured in minutes.</p>
<p>AMI baking will front load the time needed by configuring as much as possible.</p>
<h3><a id="user-content-awscloudformationinit" class="anchor" aria-hidden="true" href="#awscloudformationinit"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>AWS::CloudFormation::Init</h3>
<p><strong>cfn-init</strong> is a helper script installed on EC2 OS.
This is a simple configuration management system.</p>
<ul>
<li>User Data is procedural and run by the OS line by line.</li>
<li>cfn-init can be procedural, but can also be desired state.
<ul>
<li>Can specify particular versions of packages. It will ensure things are
configured to that end state.</li>
<li>Can manipulate OS groups and users.</li>
<li>Can download sources and extract them using authentication.</li>
</ul>
</li>
</ul>
<p>This is executed as any other command by being passed into the instance as part
of the user data and retrieves its directives from the CloudFormation
stack and you define this data in the CloudFormation template called
<code>AWS::CloudFormation::Init</code>.</p>
<h4><a id="user-content-cfn-init-explained" class="anchor" aria-hidden="true" href="#cfn-init-explained"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>cfn-init explained</h4>
<p>Starts off with a <strong>CloudFormation template</strong>.
This has a logical resource within it which is to create an EC2 instance.
This has a specific section called <code>Metadata</code>.
This then passes in the information passed in as <code>UserData</code>.
cfn-init gets variables passed into the user data by CloudFormation.</p>
<p>It knows the desired state and can work towards a final configuration.
This can monitor the user data and change things as the EC2 data changes.</p>
<h4><a id="user-content-creationpolicy-and-signals" class="anchor" aria-hidden="true" href="#creationpolicy-and-signals"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>CreationPolicy and Signals</h4>
<p>If you pass in user data, there is no way for CloudFormation to know
if the EC2 instance was provisioned properly. It may be marked as complete,
but the instance could be broken.</p>
<p>A <strong>CreationPolicy</strong> is something which is added to a logical resource
inside a CloudFormation template. You create it and supply a timeout value.</p>
<p>This waits for a signal from the resource itself before moving to a create
complete state.</p>
<h3><a id="user-content-ec2-instance-roles" class="anchor" aria-hidden="true" href="#ec2-instance-roles"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>EC2 Instance Roles</h3>
<p>IAM roles are the best practice ways for services to be granted permissions.
EC2 instance roles are roles that an instance can assume and anything
running in that instance has the permissions that role grants.</p>
<p>Starts with an IAM role with a permissions policy.
EC2 instance role allows the EC2 service to assume that role.</p>
<p>The <strong>instance profile</strong> is the item that allows the permissions to get
inside the instance. When you create an instance role in the console,
an instance profile is created with the same name.</p>
<p>When IAM roles are assumed, you are provided temporary roles based on the
permission assigned to that role. These credentials are passed through
instance <strong>meta-data</strong>.</p>
<p>EC2 and the secure token service ensure the credentials never expire.</p>
<p>Key facts</p>
<ul>
<li>Credentials are inside meta-data
<ul>
<li>iam/security-credentials/role-name</li>
<li>automatically rotated - always valid</li>
<li>Resources need to check the meta-data periodically</li>
</ul>
</li>
<li>Should always use roles compared to storing long term credentials</li>
<li>CLI tools use role credentials automatically</li>
</ul>
<h3><a id="user-content-aws-system-manager-parameter-store" class="anchor" aria-hidden="true" href="#aws-system-manager-parameter-store"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>AWS System Manager Parameter Store</h3>
<p>Passing secrets into an EC2 instance is bad practice because anyone
who has access to the meta-data has access to the secrets.</p>
<p>Parameter store allows for storage of <strong>configuration</strong> and <strong>secrets</strong></p>
<ul>
<li>Strings</li>
<li>StringList</li>
<li>SecureString</li>
</ul>
<p>Parameter Store:</p>
<ul>
<li>Can store license codes, database strings, and full configs and passwords.</li>
<li>Allows for hierarchies and versioning.</li>
<li>Can store plaintext and ciphertext.
<ul>
<li>This integrates with <strong>kms</strong> to encrypt passwords.</li>
</ul>
</li>
<li>Allows for public parameters such as the latest AMI parameter to be stored
and referenced for EC2 creating.</li>
<li>Is a public service so any services needs access to the public sphere or
to be an AWS public service.</li>
<li>Applications, EC2 instances, lambda functions can all request access to
parameter store.</li>
<li>Tied closely to IAM, can use
<ul>
<li>Long term credentials such as access keys.</li>
<li>Short term use of IAM roles.</li>
</ul>
</li>
</ul>
<h3><a id="user-content-system-and-application-logging-on-ec2" class="anchor" aria-hidden="true" href="#system-and-application-logging-on-ec2"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>System and Application Logging on EC2</h3>
<p>CloudWatch and CloudWatch Logs cannot natively capture data inside an instance.</p>
<p>CloudWatch Agent is required for OS visible data. It sends this data into CW
For CW to function, it needs configuration and permissions in addition
to having the CW agent installed.
The CW agent needs to know what information to inject into CW and CW Logs.</p>
<p>The agent also needs some permissions to interact with AWS.
This is done with an IAM role as best practice.
The IAM role has permissions to interact with CW logs.
The IAM role is attached to the instance which provides the instance and
anything running on the instance, permissions to manage CW logs.</p>
<p>The data requested is then injected in CW logs.
There is one log group for each individual log we want to capture.
There is one log stream for each group for each instance that needs
management.</p>
<p>We can use parameter store to store the configuration for the CW agent.</p>
<h3><a id="user-content-ec2-placement-groups" class="anchor" aria-hidden="true" href="#ec2-placement-groups"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>EC2 Placement Groups</h3>
<h4><a id="user-content-cluster-placement" class="anchor" aria-hidden="true" href="#cluster-placement"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Cluster Placement</h4>
<p>Pack instances close together</p>
<p>Achieves the highest level of performance available with EC2.</p>
<p>Best practice is to launch all of the instances within that group at the
same time.
If you launch with 9 instances and AWS places you in a place with capacity
for 12, you are now limited in how many you can add.</p>
<p>Cluster placements need to be part of the same AZ. Cluster
placement groups are generally the same rack, but they can even be the same
EC2 host.</p>
<p>All members have direct connections to each other. They can achieve
<strong>10 Gbps single stream</strong> vs 5 Gbps normally. They also have the lowest
latency and max PPS possible in AWS.</p>
<p>If the hardware fails, the entire cluster will fail.</p>
<h5><a id="user-content-cluster-placement-exam-powerup" class="anchor" aria-hidden="true" href="#cluster-placement-exam-powerup"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Cluster Placement Exam PowerUp</h5>
<ul>
<li>Clusters can't span AZs. The first AZ used will lock down the cluster.</li>
<li>They can span VPC peers.</li>
<li>Requires a supported instance type.</li>
<li>Best practice to use the same type of instance and launch all at once.</li>
<li>This is the only way to achieve <strong>10Gbps SINGLE stream</strong>, other data metrics
assume multiple streams.</li>
</ul>
<h4><a id="user-content-spread-placement" class="anchor" aria-hidden="true" href="#spread-placement"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Spread Placement</h4>
<p>Keep instances separated</p>
<p>This provides the best resilience and availability.
Spread groups can span multiple AZs. Information will be put on distinct
racks with their own network or power supply. There is a limit of 7 instances
per AZ. The more AZs in a region, the more instances inside a spread placement
group.</p>
<h5><a id="user-content-spread-placement-exam-powerup" class="anchor" aria-hidden="true" href="#spread-placement-exam-powerup"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Spread Placement Exam PowerUp</h5>
<ul>
<li>Provides the highest level of availability and resilience.
<ul>
<li>Each instance by default runs from a different rack.</li>
</ul>
</li>
<li>7 instances per AZ is a hard limit.</li>
<li>Not supported for dedicated instances or hosts.</li>
</ul>
<p>Use case: small number of critical instances that need to be kept separated
from each other. Several mirrors of an application</p>
<h4><a id="user-content-partition-placement" class="anchor" aria-hidden="true" href="#partition-placement"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Partition Placement</h4>
<p>Groups of instances spread apart</p>
<p>If a problem occurs with one rack's networking or power, it will
at most take out one instance.</p>
<p>The main difference is you can launch as many instances in each partition
as you desire.</p>
<p>When you launch a partition group, you can allow AWS decide or you can
specifically decide.</p>
<h5><a id="user-content-partition-placement-exam-powerup" class="anchor" aria-hidden="true" href="#partition-placement-exam-powerup"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Partition Placement Exam PowerUp</h5>
<ul>
<li>7 partitions maximum for each AZ</li>
<li>Instances can be placed into a specific partition, or AWS can pick.</li>
<li>This is not supported on dedicated hosts.</li>
<li>Great for HDFS, HBase, and Cassandra</li>
</ul>
<h3><a id="user-content-ec2-dedicated-hosts" class="anchor" aria-hidden="true" href="#ec2-dedicated-hosts"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>EC2 Dedicated Hosts</h3>
<p>EC2 host allocated to you in its entirety.
Pay for the host itself which is designed for a family of instances.
There are no instance charges.
You can pay for a host on-demand or reservation with 1 or 3 year terms.</p>
<p>The host hardware has physical sockets and cores. This dictates how
many instances can be run on the HW.</p>
<p>Hosts are designed for a specific size and family. If you purchase one host, you
configure what type of instances you want to run on it. With the older VM
system you cannot mix and match. The new Nitro system allows for mixing and
matching host size.</p>
<h4><a id="user-content-dedicated-hosts-limitations" class="anchor" aria-hidden="true" href="#dedicated-hosts-limitations"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Dedicated Hosts Limitations</h4>
<ul>
<li>AMI Limits, some versions can't be used</li>
<li>Amazon RDS instances are not supported</li>
<li>Placement groups are not supported for dedicated hosts.</li>
<li>Hosts can be shared with other organization accounts using <strong>RAM</strong></li>
<li>This is mostly used for licensing problems related to ports.</li>
</ul>
<h3><a id="user-content-enhanced-networking" class="anchor" aria-hidden="true" href="#enhanced-networking"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Enhanced Networking</h3>
<p>Enhanced networking uses SR-IOV.
The physical network interface is aware of the virtualization.
Each instance is given exclusive access to one part of a physical network
interface card.</p>
<p>There is no charge for this and is available on most EC2 types.
It allows for higher IO and lower host CPU usage
This provides more bandwidth and higher packet per seconds.
In general this provides lower latency.</p>
<h4><a id="user-content-ebs-optimized" class="anchor" aria-hidden="true" href="#ebs-optimized"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>EBS Optimized</h4>
<p>Historically network on EC2 was shared with the same network stack used
for both data networking and EBS storage networking.</p>
<p>EBS optimized instance means that some stack optimizations have taken place
and dedicated capacity has been provided for that instance for EBS usage.</p>
<p>Most new instances support this and have this enabled by default for no charge.</p>
<hr>
<h2><a id="user-content-route-53" class="anchor" aria-hidden="true" href="#route-53"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Route-53</h2>
<h3><a id="user-content-public-hosted-zones" class="anchor" aria-hidden="true" href="#public-hosted-zones"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Public Hosted Zones</h3>
<p>A hosted zone is a DNS database for a given section of global DNS data.
A public hosted zone is a type of R53 hosted zone which is hosted on
R53 provided public DNS name servers. When creating a hosted zone, AWS provides
at least 4 DNS name servers which host the zone.</p>
<p>This is globally resilient service due to multiple DNS servers.</p>
<p>Hosted zones are created automatically when you register a domain using R53.</p>
<p>Hosted zones can be created separately. If you want to register a domain
elsewhere and use R53 to host the zone file and records for that domain, then
you can specifically create a hosted zone and point at an externally
registered domain at that zone.
There is a monthly fee to host each hosted zone within R53 and a fee for
any queries made to that service.</p>
<p>Hosted Zones are what the DNS system references via delegation and name server
records. A hosted zone, when referenced in this way by the DNS system, is known
as being authoritative for a domain.
It becomes the single source of truth for a domain.</p>
<h3><a id="user-content-route-53-health-checks" class="anchor" aria-hidden="true" href="#route-53-health-checks"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Route 53 Health Checks</h3>
<p>Route checks will allow for periodic health checks on the servers.
If one of the servers has a bug, this will be removed from the list.</p>
<p>If the bug gets fixed, the health check will pass and the server will be
added back into a healthy state.</p>
<p>Health checks are separate from, but are used by records inside R53.
You don't create health checks inside records themselves.</p>
<p>These are performed by a fleet of global health checkers. If you think
they are bots and block them, this could cause alarms.</p>
<p>Checks occur every 30 seconds by default. This can be increased to 10 seconds
for additional costs. These checks are per health checker. Since there are many
you will automatically get one every few seconds. The 10 second option will
complete multiple checks per second.</p>
<p>There could be one of three checks</p>
<ul>
<li>TCP checks: R53 tries to establish TCP with end point within 10 seconds.</li>
<li>HTTP/HTTPS: Same as TCP but within 4 seconds. The end point must respond
with a 200 or 300 status code within 3 seconds of checking.</li>
<li>String matching: Same as above, the body must have a string within the first
5120 bytes. This is chosen by the user.</li>
</ul>
<p>It will be deemed healthy or unhealthy.</p>
<p>There are three types of checks.</p>
<ul>
<li>Endpoint checks</li>
<li>CloudWatch alarms</li>
<li>Checks of checks</li>
</ul>
<h3><a id="user-content-route-53-routing-policies-examples" class="anchor" aria-hidden="true" href="#route-53-routing-policies-examples"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Route 53 Routing Policies Examples</h3>
<ul>
<li>
<p>Simple: Route traffic to a single resource. Client queries the resolver
which has one record. It will respond with 3 values and these get forwarded
back to the client. The client then picks one of the three at random.
This is a single record only. No health checks.</p>
</li>
<li>
<p>Failover: Create two records of the same name and the same type. One
is set to be the primary and the other is the secondary. This is the same
as the simple policy except for the response. Route 53 knows the health of
both instances. As long as the primary is healthy, it will respond with
this one. If the health check with the primary fails, the backup will be
returned instead. This is set to implement active - passive failover.</p>
</li>
<li>
<p>Weighted: Create multiple records of the same name within the hosted zone.
For each of those records, you provide a weighted value. The total weight
is the same as the weight of all the records of the same name. If all of the
parts of the same name are healthy, it will distribute the load based
on the weight. If one of them fails its health check, it will be skipped over
and over again until a good one gets hit. This can be used for migration
to separate servers.</p>
</li>
<li>
<p>Latency-based: Multiple records in a hosted zone can be created with
the same name and same type. When a client request arrives, it knows which
region the request comes from. It knows the lowest latency and will respond
with the lowest latency.</p>
</li>
<li>
<p>Geolocation: Focused to delivering results matching the query of your
customers. The record will first be matched based on the country if possible.
If this does not happen, the record will be checked based on the continent.
Finally, if nothing matches again it will respond with the default response.
This can be used for licensing rights. If overlapping regions occur,
the priority will always go to the most specific or smallest region. The US
will be chosen over the North America record.</p>
</li>
<li>
<p>Multi-value: Simple records use one name and multiple values in this record.
These will be health checked and the unhealthy responses will automatically
be removed. With multi-value, you can have multiple records with the same
name and each of these records can have a health check. R53 using this method
will respond to queries with any and all healthy records, but it removes
any records that are marked as unhealthy from those responses. This removes
the problem with simple routing where a single unhealthy record can make it
through to your customers. Great alternative to simple routing when
you need to improve the reliability, and it's an alternative to failover
when you have more than two records to respond with, but don't want
the complexity or the overhead of weighted routing.</p>
</li>
</ul>
<hr>
<h2><a id="user-content-relational-database-service-rds" class="anchor" aria-hidden="true" href="#relational-database-service-rds"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Relational-Database-Service-RDS</h2>
<h3><a id="user-content-database-refresher" class="anchor" aria-hidden="true" href="#database-refresher"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Database Refresher</h3>
<p>Systems to store and manage data.</p>
<h4><a id="user-content-relational-sql" class="anchor" aria-hidden="true" href="#relational-sql"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Relational (SQL)</h4>
<ul>
<li>Structured Query Language (SQL) is a feature of most RDS.</li>
<li>Structure to the data known as a <strong>schema</strong>.
<ul>
<li>Defined in advance.</li>
<li>Defines names of things</li>
<li>Valid values of things</li>
<li>Types of data which is stored and where</li>
</ul>
</li>
<li>Fixed relationship between tables.
<ul>
<li>This is defined before data is entered into the database.</li>
</ul>
</li>
</ul>
<p>Every row in a table must have a value for the <strong>primary key</strong>.
There must be a value stored for every attribute in the table.</p>
<p>SQL systems are relational so we generally define relationships between
tables as well. This is defined with a <strong>join table</strong>.
A join table has a <strong>composite key</strong> which is a key formed of two parts.
Composite keys together must be unique.</p>
<p>Keys in different tables are how the relationships between the tables
are defined.</p>
<p>The Table schema and relationships must be defined in advance which can be
hard to do.</p>
<h4><a id="user-content-non-relational-nosql" class="anchor" aria-hidden="true" href="#non-relational-nosql"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Non-Relational (NoSQL)</h4>
<p>Not a single thing, and is a catch all for everything else.
There is generally no schema or a weak one.</p>
<h5><a id="user-content-key-value-databases" class="anchor" aria-hidden="true" href="#key-value-databases"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Key-Value databases</h5>
<p>This is just a list of keys and value pairs.
So long as every key is unique, there is no real schema or structure needed.
These are really fast and highly scalable.
This is also used for <strong>in memory caching</strong>.</p>
<h5><a id="user-content-wide-column-store" class="anchor" aria-hidden="true" href="#wide-column-store"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Wide Column Store</h5>
<p>DynamoDB is an example of wide column store database.</p>
<p>Each row or item has one or more keys.
One key is called the partition key.
You can have additional keys other than the partition key called the
sort or range key.</p>
<p>It can be <strong>single key</strong> (only partition key) or <strong>composite key</strong>
(partition key and sort key).</p>
<p>Every item in a table can also have attributes, but they don't have to be
the same between values.
The only requirements is that every item inside the table has to use the same
key structure and it has to have a unique key.</p>
<h5><a id="user-content-document" class="anchor" aria-hidden="true" href="#document"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Document</h5>
<p>Documents are generally formatted using JSON or XML.</p>
<p>This is an extension of a key-value store where each document is interacted
with via an ID that's unique to that document, but the value of the document
contents are exposed to the database allowing you to interact with it.</p>
<p>Good for order databases, or collections, or contact stale databases.</p>
<p>Great for nested data items within a document structure such as user profiles.</p>
<h5><a id="user-content-row-database-mysql" class="anchor" aria-hidden="true" href="#row-database-mysql"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Row Database (MySQL)</h5>
<p>Often called OLTP (Online Transactional Processing Databases).</p>
<p>If you needed to read the price of one item you need that
row first. If you wanted to query all of the sizes of every order, you will
need to check for each row.</p>
<p>Great for things which deal in rows and items where they are constantly
accessed, modified, and removed.</p>
<h5><a id="user-content-column-database-redshift" class="anchor" aria-hidden="true" href="#column-database-redshift"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Column Database (Redshift)</h5>
<p>Instead of storing data in rows on disk, they store it based on columns.
The data is the same, but it's grouped together on disk, based on
column so every order value is stored together, every product item, color,
size, and price are all grouped together.</p>
<p>This is bad for transactional style processing, but great for reporting or when
all values for a specific size are required.</p>
<h5><a id="user-content-graph" class="anchor" aria-hidden="true" href="#graph"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Graph</h5>
<p>Relationships between things are formally defined and stored along in the
database itself with the data.
They are not calculated each and every time you run a query.
These are great for relationship driven data.</p>
<p>Nodes are objects inside a graph database. They can have properties.</p>
<p>Edges are relationships between the nodes. They have a direction.</p>
<p>Relationships themselves can also have attached data, so name value pairs.
We might want to store the start date of any employment relationship.</p>
<p>Can store massive amounts of complex relationships between data or between
nodes in a database.</p>
<h3><a id="user-content-databases-on-ec2" class="anchor" aria-hidden="true" href="#databases-on-ec2"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Databases on EC2</h3>
<p>It is always a bad idea to do this.</p>
<ul>
<li>Splitting an instance over different AZs
<ul>
<li>Adds reliability consideration between the AZs</li>
<li>Adds a cost to move the data between AZs</li>
</ul>
</li>
</ul>
<h4><a id="user-content-reasons-ec2-database-might-make-sense" class="anchor" aria-hidden="true" href="#reasons-ec2-database-might-make-sense"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Reasons EC2 Database might make sense</h4>
<ul>
<li>Need access to the OS of the Database.
<ul>
<li>You should question if a client requests this, it rarely is needed.</li>
</ul>
</li>
<li>Advanced DB Option tuning (DBROOT)
<ul>
<li>AWS provides options to tune many of these parameters anyways.</li>
<li>Can be a vendor that is asking for this.</li>
</ul>
</li>
<li>DB or DB version that AWS doesn't provide.</li>
<li>You might need a specific version of an OS and DB that AWS doesn't provide.</li>
</ul>
<h4><a id="user-content-reasons-why-you-really-shouldnt-run-a-database-on-ec2" class="anchor" aria-hidden="true" href="#reasons-why-you-really-shouldnt-run-a-database-on-ec2"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Reasons why you really shouldn't run a database on EC2</h4>
<ul>
<li><strong>Admin overhead</strong> is intense to manage the EC2 host.</li>
<li>Backup and Disaster Management adds complexity.</li>
<li>EC2 is running in one AZ. If the zone fails, access to the database fails.</li>
<li>Will miss out on features from AWS DB products.</li>
<li>EC2 is ON or OFF, there is no way to scale easily.</li>
<li><strong>Replication</strong> can be tricky to manage on your own.</li>
<li>Performance will be slower than other AWS options.</li>
</ul>
<h3><a id="user-content-relational-database-service-rds-1" class="anchor" aria-hidden="true" href="#relational-database-service-rds-1"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Relational Database Service (RDS)</h3>
<ul>
<li>Database-as-a-service (DBaaS)
<ul>
<li>Not entirely true more of DatabaseServer-as-a-service.</li>
<li>Managed Database Instance for one or more databases.</li>
</ul>
</li>
<li>No need to manage the HW or server itself.</li>
<li>Handles engines such as MySQL, MariaDB, PostgreSQL, Oracle, Microsoft SQL.</li>
</ul>
<p>Amazon Aurora. This is so different from normal RDS, it is a separate product.</p>
<h4><a id="user-content-rds-database-instance" class="anchor" aria-hidden="true" href="#rds-database-instance"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>RDS Database Instance</h4>
<p>Runs one of a few types of database engines and can contain multiple
user created databases. Create one when you provision the instance, but
multiple ones can be created after.</p>
<p>When you create a database instance, the way you access it is using a database
host-name, a CNAME, and this resolves to the database instance itself.</p>
<p>RDS uses standard database engines so you can access an RDS instance using the
same tooling as if you were accessing a self-managed database.</p>
<p>The database can be optimized for:</p>
<p>db.m5 general
db.r5 memory
db.t3 burst</p>
<p>There is an associated size and AZ selected.</p>
<p>When you provision an instance, you provision dedicated storage to that instance.
This is EBS storage located in the same AZ.
RDS is vulnerable to failures in that AZ.</p>
<p>The storage can be allocated with SSD or magnetic.</p>
<p>io1 - lots of IOPS and consistent low latency
gp2 - same burst pool architecture as it does on EC2, used by default
magnetic - compatibility mostly for long term historic uses</p>
<p>Billing is per instance and hourly rate for that compute. You are billed
for storage allocated.</p>
<h3><a id="user-content-rds-multi-az-high-availability" class="anchor" aria-hidden="true" href="#rds-multi-az-high-availability"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>RDS Multi AZ (High-Availability)</h3>
<p>This is an option that you can enable on RDS instances.
Secondary hardware is allocated inside another AZ. This is referred to as
the standby replica or standby replica instance. The standby replica has
its own storage in the same AZ as it's located.</p>
<p>RDS enables synchronous replication from the primary instance to the
standby replica.</p>
<p>RDS Access ONLY via database CNAME. The CNAME will point at the primary
instance. You cannot access the standby replica for any reason via RDS.</p>
<p>The standby replica cannot be used for extra capacity.</p>
<p><strong>Synchronous Replication</strong> means:</p>
<ol>
<li>Database writes happen.</li>
<li>Primary database instance commits changes.</li>
<li>Same time as the write is happening, standby replication is happening.</li>
<li>Standby replica commits writes.</li>
</ol>
<p>If any error occurs with the primary database, AWS detects this and will
failover within 60 to 120 seconds to change to the new database.</p>
<p>This does not provide fault tolerance as there will be some impact during change.</p>
<h4><a id="user-content-rds-exam-powerup" class="anchor" aria-hidden="true" href="#rds-exam-powerup"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>RDS Exam PowerUp</h4>
<ul>
<li>Multi-AZ feature is not free tier, extra infrastructure for standby.
<ul>
<li>Generally two times the price.</li>
</ul>
</li>
<li>The standby replica cannot be accessed directly unless a fail occurs.</li>
<li>Failover is highly available, not fault tolerant.</li>
<li>Same region only (others AZ in the VPC).</li>
<li>Backups are taken from standby which removes performance impacts.</li>
<li>Failover can happen for a number of reasons.
<ul>
<li>Full AZ outage</li>
<li>Primary RDS failure</li>
<li>Manual failover for testing</li>
<li>If you change the type of a RDS instance, it will failover as part of
changing that type.</li>
</ul>
</li>
</ul>
<h3><a id="user-content-rds-backup-and-restores" class="anchor" aria-hidden="true" href="#rds-backup-and-restores"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>RDS Backup and Restores</h3>
<p>RPO - Recovery Point Objective</p>
<ul>
<li>Time between the last backup and when the failure occurred.</li>
<li>Amount of maximum data loss.</li>
<li>Influences technical solution and cost.</li>
<li>Business usually provides an RPO value.</li>
</ul>
<p>RTO - Recovery Time Objective</p>
<ul>
<li>Time between the disaster recovery event and full recovery.</li>
<li>Influenced by process, staff, tech and documentation.</li>
</ul>
<p>RDS Backups</p>
<p>First snap is full copy of the data used on the RDS volume. From then on,
the snapshots are incremental and only store the change in data.</p>
<p>When any snapshot occurs, there's a brief interruption to the flow of data
between the compute resource and the storage. If you are using single AZ, this
can impact your application. If you are using Multi-AZ, the snapshot occurs
on the standby replica.</p>
<p>Manual snapshots don't expire, you have to clean them yourself.
Automatic Snapshots can be configured to make things easier.</p>
<p>In addition to automated backup, every 5 minutes database transaction logs are
saved to S3. Transaction logs store the actual data which changes inside a
database so the actual operations that are executed. This allows a database
to be restored to a point in time often with 5 minute granularity.</p>
<p>Automatic cleanups can be anywhere from 0 to 35 days.
This means you can restore to any point in that time frame.
This will use both the snapshots and the translation logs.</p>
<p>When you delete the database, they can be retained but they will expire
based on their retention period.</p>
<p>The only way to maintain backups is to create a final snapshot which will not
expire automatically.</p>
<h4><a id="user-content-rds-backup-exam-powerup" class="anchor" aria-hidden="true" href="#rds-backup-exam-powerup"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>RDS Backup Exam PowerUp</h4>
<ul>
<li>When performing a restore, RDS creates a new RDS with a new endpoint address.</li>
<li>When restoring a manual snapshot, you are setting it to a single point
in time. This influences the RPO value.</li>
<li>Automated backups are different, they allow any 5 minute point in time.</li>
<li>Backups are restored and transaction logs are replayed to bring DB to
desired point in time.</li>
<li>Restores aren't fast, think about RTO.</li>
</ul>
<h3><a id="user-content-rds-read-replicas" class="anchor" aria-hidden="true" href="#rds-read-replicas"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>RDS Read-Replicas</h3>
<p>Kept in sync using <strong>asynchronous replication</strong></p>
<p>It is written fully to the primary and standby instance first.
Once its stored on disk, it is then pushed to the replica.
This means there could be a small lag.
These can be created in the same region or a different region.
This is known as <strong>cross region replication</strong>. AWS handles all of the
encryption, configuration, and networking without intervention.</p>
<h4><a id="user-content-why-do-these-matter" class="anchor" aria-hidden="true" href="#why-do-these-matter"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Why do these matter</h4>
<p>READ performance</p>
<ul>
<li>5 direct read-replicas per DB instance.</li>
<li>Each of these provides an additional instance of read performance.</li>
<li>This allows you to scale out read operations for an instance.</li>
<li>Read-replicas can chain, but lag will become a problem.</li>
<li>Can provide global performance improvements.</li>
<li>Provides global resilience by using cross region replication.</li>
<li>They don't improve RTO</li>
</ul>
<p>Read Replicas provide near 0 RPO</p>
<ul>
<li>If the primary instance fails, you can promote a read-replica to take over.</li>
<li>Once it is promoted, it allows for read and write.</li>
<li>Only works for failures.
<ul>
<li>Read-replicas will replicate data corruption.</li>
<li>In this case you must default back to snapshots and backups.</li>
</ul>
</li>
<li>Promotion cannot be reversed.</li>
</ul>
<h3><a id="user-content-amazon-aurora" class="anchor" aria-hidden="true" href="#amazon-aurora"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Amazon Aurora</h3>
<p>Aurora architecture is VERY different from RDS.</p>
<p>It uses a <strong>cluster</strong> which is:</p>
<ul>
<li>A single primary instance and 0 or more replicas.</li>
<li>The replicas within Aurora can be used for reads during normal operation.
<ul>
<li>Provides benefits of RDS multi-AZ and read-replicas.</li>
</ul>
</li>
<li>Aurora doesn't use local storage for the compute instances.
<ul>
<li>An Aurora cluster has a shared cluster volume.</li>
<li>Provides faster provisioning.</li>
<li>Improved availability.</li>
<li>Better performance.</li>
</ul>
</li>
</ul>
<p>Aurora cluster functions across a number of availability zones.</p>
<p>There is a primary instance and a number of replicas.
The read applications from applications can use the replicas.</p>
<p>There is a shared storage of <strong>max 64 TiB</strong> across all replicas.
This uses 6 copies across AZs.</p>
<p>All instances have access to these storage nodes. This replication
happens at the storage level. No extra resources are consumed during
replication.</p>
<p>By default the primary instance is the only one who can write. The replicas
will have read access.</p>
<p>Aurora automatically detect hardware failures on the shared storage. If there
is a failure, it immediately repairs that area of disk and
recreates that data with no corruption.</p>
<p>With Aurora you can have up to 15 replicas and any of them
can be a failover target. The failover operation will be quicker because
it doesn't have to make any storage modifications.</p>
<ul>
<li>Cluster shared volume is based on SSD storage by default.
<ul>
<li>Provides so high IOPS and low latency.</li>
<li>No way to select magnetic storage.</li>
</ul>
</li>
<li>Aurora cluster does not specify the amount of storage needed.
<ul>
<li>This is based on what is consumed.</li>
</ul>
</li>
<li>High water mark billing or billed for the most used.
<ul>
<li>Storage which is freed up can be re-used.</li>
<li>If you reduce a lot of storage, you will need to create a brand new
cluster and migrate data from the old cluster to the new cluster.</li>
</ul>
</li>
<li>Storage is for the cluster and not the instances which means Replicas can be
added and removed without requiring storage, provisioning, or removal.</li>
</ul>
<h4><a id="user-content-aurora-endpoints" class="anchor" aria-hidden="true" href="#aurora-endpoints"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Aurora Endpoints</h4>
<p>Aurora clusters like RDS use endpoints, so these are DNS addresses which
are used to connect to the cluster. Unlike RDS, Aurora clusters have
multiple endpoints that are available for an application.</p>
<p>Minimum endpoints</p>
<ul>
<li><strong>Cluster endpoint</strong> always points at the primary instance.
<ul>
<li>This is used for read and write applications.</li>
</ul>
</li>
<li><strong>Reader endpoint</strong>
<ul>
<li>Will point at primary instance if that is all there is.</li>
<li>Will load balance across all available replicas for read operations.</li>
<li>Additional replicas which are used for reads will be load balanced
automatically.</li>
</ul>
</li>
</ul>
<h4><a id="user-content-costs" class="anchor" aria-hidden="true" href="#costs"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Costs</h4>
<ul>
<li>No free-tier option</li>
<li>Aurora doesn't support micro instances</li>
<li>Beyond RDS singleAZ (micro) Aurora provides best value.</li>
<li>Compute is billed per second with a 10 minute minimum.</li>
<li>Storage is billed using the high watermark for the lifetime using GB-Month.
<ul>
<li>Additional IO cost per request made to the cluster shared storage.</li>
</ul>
</li>
<li>100% DB size in backups are included for free.
<ul>
<li>100 GB cluster will have 100 GB of storage for backups.</li>
</ul>
</li>
</ul>
<h4><a id="user-content-aurora-restore-clone-and-backtrack" class="anchor" aria-hidden="true" href="#aurora-restore-clone-and-backtrack"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Aurora Restore, Clone and Backtrack</h4>
<p>Backups in Aurora work in the same way as RDS.
Restores create a brand new cluster.</p>
<p>Backtrack must be enabled on a per cluster basis. This allows you to roll back
your data base to a previous point in time. This helps for data corruption.</p>
<p>You can adjust the window backtrack will work for.</p>
<p>Fast clones make a new database much faster than copying all the data.
It references the original storage and only write the differences between
the two. It uses a tiny amount of storage and only stores data that's changed
in the clone or changed in the original after you make the clone.</p>
<h3><a id="user-content-aurora-serverless" class="anchor" aria-hidden="true" href="#aurora-serverless"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Aurora Serverless</h3>
<p>Provides a version of Aurora database product without managing the resources.
You still create a cluster, but it uses ACUs or Aurora Capacity Units.</p>
<p>For a cluster, you can set a min and max ACU based on the load and can even
go down to 0 to be paused. In this case you would only be billed for storage
consumed.</p>
<p>Billing is based on resources used on a per-second basis.</p>
<p>Same resilience as Aurora (6 copies across AZs).</p>
<p>ACUs are stateless and shared across many AWS customers and have no local
storage. They can be allocated to your Aurora Serverless cluster rapidly
when required. Once ACUs are allocated to a cluster, they have access to cluster
storage in the same way as an Aurora Provisioned cluster.</p>
<p>There is a shared proxy fleet. When a customer interacts with the data
they are actually communicating with the proxy fleet. The proxy fleet
brokers an application with the ACU and ensures you can scale in and out
without worrying about usage. This is managed by AWS on your behalf.</p>
<h4><a id="user-content-aurora-serverless---use-cases" class="anchor" aria-hidden="true" href="#aurora-serverless---use-cases"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Aurora Serverless - Use Cases</h4>
<ul>
<li>Infrequently used applications.
<ul>
<li>Low volume blog site.</li>
<li>You only pay for resources as you consume them on a per second basis.</li>
</ul>
</li>
<li>New applications with unpredictable workloads.</li>
<li>Great for variable workloads such as sales cycles.
It can scale in and out based on demand</li>
<li>Good for development and test databases, can scale back when not needed.</li>
<li>Great for multi-tenant applications.
<ul>
<li>Billing a user a set dollar amount per month per license.</li>
<li>If your incoming load is directly tied to more revenue this makes sense.</li>
</ul>
</li>
</ul>
<h3><a id="user-content-aurora-global-database" class="anchor" aria-hidden="true" href="#aurora-global-database"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Aurora Global Database</h3>
<p>Introduces the idea of secondary regions with up to 16 read only replicas.
Replication from primary region to secondary regions happens at the storage
layer and typically occurs within one second.</p>
<ul>
<li>Great for cross region disaster recovery and business continuity.</li>
<li>Global read scaling
<ul>
<li>Low latency performance improvements for international customers.</li>
</ul>
</li>
<li>The application can perform read operations against the read replicas.</li>
<li>There is ~1s or less replication between regions.</li>
<li>It is one way replication.</li>
<li>No additional CPU usage is needed, it happens on the storage layer.</li>
<li>Secondary regions can have 16 replicas.
<ul>
<li>All can be promoted to Read or Write in a DR situation.</li>
</ul>
</li>
<li>Maximum of 5 secondary regions.</li>
</ul>
<h3><a id="user-content-aurora-multi-master-writes" class="anchor" aria-hidden="true" href="#aurora-multi-master-writes"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Aurora Multi-Master Writes</h3>
<p>Allows an aurora cluster to have multiple instances capable of reads and writes.</p>
<p>Single-master Mode</p>
<ul>
<li>one R/W and zero or more read only replicas</li>
<li>Cluster endpoint is normally used to write</li>
<li>Read endpoint is used for load balancing</li>
</ul>
<p>Aurora Multi-master has no endpoint or load balancing. An application
can connect with one or both of the instances inside a multi-master
cluster.</p>
<p>When one of the R/W nodes receives a write request from the application, it
immediately proposes that data be committed to all of the storage notes in that
cluster. At this point, each node that makes up a cluster either confirms
or rejects the proposed change. It will reject if this conflicts with something
already in flight.</p>
<p>The writing instance is looking for a bunch of nodes to agree. If the group
rejects it, it cancels the write in error. If it commits, it will replicate
on all storage nodes in the cluster.</p>
<p>This also ensures storage is updated on in-memory cache's of other nodes.</p>
<p>If a writer goes down in a multi-master cluster, the application will shift
all future load over to a new writer with little if any disruption.</p>
<h3><a id="user-content-database-migration-service-dms" class="anchor" aria-hidden="true" href="#database-migration-service-dms"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Database Migration Service (DMS)</h3>
<p>A managed database migration service.
Starts with a replication instance which runs on top of an EC2 instance.
This replication instance runs one or more replication tasks.
This is where the configuration is defined for the migration of databases.
This runs using a replication instance.</p>
<p>Need to define the source and destination endpoints.
These point at the physical source and target databases.
One of these end points must be on AWS.</p>
<p>Full load migration is a one off process which transfers everything at once.
This requires the database to be down during this process. This might
take several days.</p>
<p>Instead Full Load + CDC allows for a full load transfer to occur and it
monitors any changes that happens during this time. Any of the captured
changes can be applied to the target.</p>
<p>CDC only migration is good if you have a vendor solution that works quickly
and only changes need to be captured.</p>
<p>Schema Conversion Tool or SCT can perform conversions between database types.</p>
<hr>
<h2><a id="user-content-network-storage-efs" class="anchor" aria-hidden="true" href="#network-storage-efs"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Network-Storage-EFS</h2>
<h3><a id="user-content-efs-architecture" class="anchor" aria-hidden="true" href="#efs-architecture"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>EFS Architecture</h3>
<p>EFS moves the instances closer to being stateless.</p>
<ul>
<li>EFS is an implementation of NFSv4</li>
<li>EFS file systems are created and mounted in Linux.</li>
<li>EFS storage exists separately from an EC2 instance like EBS does.
<ul>
<li>EBS is block storage</li>
<li>EFS is file storage</li>
</ul>
</li>
<li>Media can be shared between many EC2 instances.</li>
<li>EFS is a private service.
<ul>
<li>Isolated to the VPC its provisioned into.</li>
<li>Access is via mount targets inside the VPC.</li>
</ul>
</li>
<li>EFS access outside of the VPC with
<ul>
<li>VPC peering</li>
<li>VPN connections</li>
<li>AWS direct connect</li>
</ul>
</li>
</ul>
<h4><a id="user-content-elastic-file-system-explained" class="anchor" aria-hidden="true" href="#elastic-file-system-explained"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Elastic File System Explained</h4>
<p>EFS runs inside a VPC. Inside EFS you create file systems and these use POSIX
permissions. EFS is made available inside a VPC via mount targets.
Mount targets have IP addresses taken from the IP address range of the
subnet they're inside. For HA, you need to make sure that you put mount
targets in each AZ the system runs in.</p>
<p>You can use hybrid networking to connect to the same mount targets.</p>
<h4><a id="user-content-efs-exam-powerup" class="anchor" aria-hidden="true" href="#efs-exam-powerup"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>EFS Exam PowerUp</h4>
<ul>
<li>EFS is Linux Only</li>
<li>Two performance modes:
<ul>
<li>General purpose is good for latency sensitive use cases.
<ul>
<li>General purpose should be default for 99.9% of uses.</li>
</ul>
</li>
<li>Max I/O performance mode can scale to higher levels of aggregate t-put
and IOPS but it does have increased latencies.</li>
</ul>
</li>
<li>Two t-put modes:
<ul>
<li>Bursting works like GP2 volumes inside EBS with a burst pool.
The more data you store in the FS, the better performance you get.</li>
<li>Provisioned t-put modes can specify t-put requirements separately from size.</li>
</ul>
</li>
<li>Two storage classes available:
<ul>
<li>Standard</li>
<li>Infrequent access</li>
<li>Can use lifecycle policies to move data between classes.</li>
</ul>
</li>
</ul>
<hr>
<h2><a id="user-content-ha-and-scaling" class="anchor" aria-hidden="true" href="#ha-and-scaling"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>HA-and-Scaling</h2>
<h3><a id="user-content-load-balancing-fundamentals" class="anchor" aria-hidden="true" href="#load-balancing-fundamentals"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Load Balancing Fundamentals</h3>
<p>Using one server is risky because that server can have performance issues
or be completely unavailable, thus bringing down an application.</p>
<p>A better solution is to use multiple servers.
Without load balancing, this could bring additional problems.</p>
<ul>
<li>The servers can end up with uneven load.
<ul>
<li>Some requests take more CPU than others.</li>
</ul>
</li>
<li>Failed instances will still show up in DNS cache.
<ul>
<li>Due to TTL values, a user can be directed toward a dead server.</li>
</ul>
</li>
</ul>
<h4><a id="user-content-load-balancers-architecture" class="anchor" aria-hidden="true" href="#load-balancers-architecture"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Load Balancers Architecture</h4>
<p>The user connects to a load balancer that is set to listens on port 80 and 443.</p>
<p>Within AWS, the configuration for which ports the load balancer listens on is
called a <strong>listener</strong>.</p>
<p>The user is connected to the load balancer and not the actual server.</p>
<p>Behind the load balancer, there is an application server.
At a high level when the user connects to the load balancer, it distributes
that load to servers on the application server. The users client thinks it is
talking directly to the application server.</p>
<p>LB will run health checks against all of the servers. If one of the servers
does fail, the load balancer will realize this and stop sending connections
to that server. From the users client, the application always works.</p>
<p>As long as 1+ servers are operational, the LB is operational.
Clients shouldn't see errors that occur with one server.</p>
<h4><a id="user-content-lb-exam-powerup" class="anchor" aria-hidden="true" href="#lb-exam-powerup"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>LB Exam PowerUp</h4>
<ul>
<li>Clients connect to the <strong>listener</strong> of the load balancer.</li>
<li>The load balancer connects to one or more <strong>targets</strong> or servers.</li>
<li>Two connections in play.
<ul>
<li>Listener connection: one connection between the client and listener.</li>
<li>Backend connection: one connection between load balancer and target.</li>
</ul>
</li>
<li>The LB abstracts the client away from individual servers.</li>
<li>Used for high availability, fault tolerance, and scaling</li>
</ul>
<h3><a id="user-content-application-load-balancer-alb" class="anchor" aria-hidden="true" href="#application-load-balancer-alb"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Application Load Balancer (ALB)</h3>
<p>ALB is a layer 7 or Application Layer Load Balancer.
It is capable of inspecting data that passes through.
It can understand the application layer <code>http</code> and <code>https</code> and
take actions based on things in those protocols like paths, headers,
and hosts.</p>
<p>Capacity that you have as part of an ALB increases automatically based
on the load which passes through that ALB. This is made of multiple ALB nodes
each running in different AZs. This makes them scalable and highly available.</p>
<p>Load balancing can be internet facing or internal.
The difference is whether the nodes of the LB, the things which
run in the AZs have public IP addresses or not.</p>
<p>Internet facing LB is designed to be connected to, from public internet based
clients, and load balance them across targets.</p>
<p>Internal load balancer is not accessible from the internet and is used to load
balance inside a VPC only.</p>
<p>Load balancer sits between a client and one or more servers.
Front end or listening side, accepts connections from a client.
Back end is used for distribution to the targets.</p>
<p>LB billed on hourly rate and <strong>Load Balancer Capacity Unit</strong> LCU.
LCU that you consume is based on the highest value for all of the
individual measurements. You pay a certain number of LCUs based on your
load over that hour.</p>
<h4><a id="user-content-cross-zone-load-balancing" class="anchor" aria-hidden="true" href="#cross-zone-load-balancing"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Cross zone load balancing</h4>
<p>Each node that is part of the load balancer is able to distribute load
across all instances across all AZ that are registered with that LB,
even if its not in the same AZ. It is the reason we can achieve a balanced
distribution of connections behind a load balancer.</p>
<p>It can also provide health checks on the target servers.
If all instances are shown as healthy, it can distribute evenly.</p>
<p>ALB can support a wide array of targets. Targets are grouped within target
groups and an individual target can be a member of multiple groups. It's the
groups which ALBs distribute connections to. You could create rules
to direct traffic to different Target Groups based on their DNS.</p>
<h4><a id="user-content-alb-exam-powerup" class="anchor" aria-hidden="true" href="#alb-exam-powerup"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>ALB Exam PowerUp</h4>
<ul>
<li>Targets are one single compute resource that connections are connected
towards.</li>
<li>Target groups are groups of targets which are addressed using rules.</li>
<li>Rules are
<ul>
<li>path based <code>/cat</code> or <code>/dog</code></li>
<li>host based if you want to use different DNS names.</li>
</ul>
</li>
<li>Support EC2, EKS, Lambda, HTTPS, HTTP/2 and websockets.</li>
<li>ALB can use SNI for multiple SSL certs attached to that LB.
<ul>
<li>LB can direct individual domain names using SSL certs at different target
groups.</li>
</ul>
</li>
<li>AWS does not suggest using Classic Load Balancer (CLB), these are legacy.
<ul>
<li>This can only use one SSL certificate.</li>
</ul>
</li>
</ul>
<h3><a id="user-content-launch-configuration-and-templates" class="anchor" aria-hidden="true" href="#launch-configuration-and-templates"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Launch Configuration and Templates</h3>
<p>They are documents which allow you to config an EC2 instance in advance.
Anything you usually define at the point of launching an instance can be
selected with a Launch Configuration (LC) or Launch Template (LT).</p>
<p>LTs are newer and provide more features than LCs like versioning.</p>
<p>Both of these are not editable. You define them once and that configuration
is locked.
If you need to adjust a configuration, you must make a new one and launch it.</p>
<p>LTs can be used to save time when provisioning EC2 instances
from the console UI / CLI.</p>
<h3><a id="user-content-autoscaling-groups" class="anchor" aria-hidden="true" href="#autoscaling-groups"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Autoscaling Groups</h3>
<ul>
<li>Automatic scaling and self-healing for EC2</li>
<li>They make use of LCs or LTs to know what to provision.</li>
<li>Autoscaling group uses one LC or one version of a LT which it's linked with.</li>
<li>Three values to control
<ul>
<li>minimum</li>
<li>desired</li>
<li>maximum</li>
</ul>
</li>
</ul>
<p>Provision or terminate instances to keep at the desired level
Scaling Policies can trigger this based on metrics.</p>
<p>Autoscaling Groups will distribute EC2 instances to try and keep the AZs equal.</p>
<h4><a id="user-content-scaling-policies" class="anchor" aria-hidden="true" href="#scaling-policies"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Scaling Policies</h4>
<p>Manual Scaling - manually adjust the desired capacity
Scheduled Scaling - time based adjustments
Dynamic Scaling</p>
<ul>
<li>Simple: If CPU is above 50%, add one to capacity</li>
<li>Stepped: If CPU usage is above 50%, add one, if above 80% add three</li>
<li>Target: Desired aggregate CPU = 40%, ASG will achieve this</li>
</ul>
<p><strong>Cooldown Period</strong> is how long to wait at the end of a scaling action before
scaling again. There is a minimum billable duration for an EC2 instance.
Currently this is 300 seconds.</p>
<p>Self healing occurs when an instance has failed and AWS provisions a new
instance in its place. This will fix most problems that are isolated to one
instance.</p>
<p>AGS can use the load balancer health checks rather than EC2.
ALB status checks can be much richer than EC2 checks because they can monitor
the status of HTTP and HTTPS requests. This makes them more application aware.</p>
<ul>
<li>Autoscaling Groups are free, only billed for the resources deployed.</li>
<li>Always use cool downs to avoid rapid scaling.</li>
<li>Try and use more smaller instances to allow granularity.</li>
<li>You should use ALB with autoscaling groups.</li>
<li>ASG defines when and where, Launch Template defines what.</li>
</ul>
<h3><a id="user-content-network-load-balancer-nlb" class="anchor" aria-hidden="true" href="#network-load-balancer-nlb"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Network Load Balancer (NLB)</h3>
<p>Part of AWS Version 2 series of load balancers.
NLBs are Layer 4, only understand TCP and UDP.</p>
<p>Can't interpret HTTP or HTTPs, but this makes it much faster in latency.
If you see anything about latency and HTTP and HTTPS are not involved, this
should default to a NLB.</p>
<p>There is nothing stopping NLB from load balancing on HTTP just by routing data.
They would do this really fast and can deliver millions of requests per second.</p>
<p>Only member of the load balancing family that can be provided a static IP.
There is 1 interface per AZ. Can also use Elastic IPs (whitelisting) and should
be used for this purpose.</p>
<p>Can perform SSL pass through.</p>
<p>NLB can load balance non HTTP/S applications, doesn't care about anything
above TCP/UDP. This means it can handle load balancing for FTP or things
that aren't HTTP or HTTPS.</p>
<h3><a id="user-content-ssl-offload-and-session-stickiness" class="anchor" aria-hidden="true" href="#ssl-offload-and-session-stickiness"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>SSL Offload and Session Stickiness</h3>
<h4><a id="user-content-bridging---default-mode" class="anchor" aria-hidden="true" href="#bridging---default-mode"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Bridging - Default mode</h4>
<p>One or more clients makes one or more connections to a load balancer.
The load balancer is configured so its <strong>listener</strong> uses HTTPS, SSL connections
occur between the client and the load balancer.</p>
<p>The load balancer then needs an SSL certificate that matches the domain name
that the application uses. AWS has access to this certificate.
If you need to be careful of where your certificates are stored, you may
have a problem with this system.</p>
<p>ELB initiates a new SSL connection to backend instances with a removed
HTTPS certificate. This can take actions based on the content of the HTTP.</p>
<p>The application local balancer requires a SSL certificate because it needs
to decrypt any data that's being encrypted by the client. Once decrypted, it
will interpret it then create new encrypted sessions between it and the back
end EC2 instances. The EC2 instance will need matching SSL certificates.</p>
<p>Needs the compute for the cryptographic operations. Every EC2 instance must
perform these cryptographic operations. This overhead can be significant.</p>
<p>The main benefit is the elastic load balancer gets to see the unencrypted
HTTP and can take actions based on what's contained in this plain text
protocol.</p>
<h4><a id="user-content-pass-through---network-load-balancer" class="anchor" aria-hidden="true" href="#pass-through---network-load-balancer"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Pass-through - Network Load Balancer</h4>
<p>The client connects, but the load balancer passes the connection along without
decrypting the data at all. The instances still need the SSL certificates,
but the load balancer does not. Specifically it's a network load balancer
which is able to perform this style of connection.</p>
<p>The load balancer is configured for TCP, it can see the source or destinations,
but it never touches the encrypted connection. The certificate never
needs to be seen by AWS.</p>
<p>Negative is you don't get any load balancing based on the HTTP part
because that is never exposed to the load balancer. The EC2 instances
still need the compute cryptographic overhead.</p>
<h4><a id="user-content-offload" class="anchor" aria-hidden="true" href="#offload"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Offload</h4>
<p>Clients connect to the load balancer using HTTPS and are terminated on the
load balancer. The LB needs an SSL certificate to decrypt the data, but
on the backend the data is sent via HTTP. While there is a certificate
required on the load balancer, this is not needed on the LB.</p>
<p>Data is in plaintext form across AWS's network. Not a problem for most.</p>
<h4><a id="user-content-connection-stickiness" class="anchor" aria-hidden="true" href="#connection-stickiness"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Connection Stickiness</h4>
<p>If there is no stickiness, each time the customer logs on they will have
a stateless experience. If the state is stored on a particular server,
sessions can't be load balanced across multiple servers.</p>
<p>There is an option available within elastic load balancers called Session
Stickiness. And within an application load balancer this is enabled on a
target group. If enabled, the first time a user makes a request, the load
balancer generates a cookie called AWSALB with a duration. A valid duration
is between one second and seven days. For this time, sessions will be sent to
the same backend instance. This will happen until:</p>
<ul>
<li>A server failure, then the user will be moved to a different server.</li>
<li>The cookie expires, the whole process will repeat and will receive a
new cookie</li>
</ul>
<p>This could cause backend unevenness because one user will always be forced
to the same server no matter what the distributed load is. Applications
should be designed to hold session stickiness somewhere other than EC2.</p>
<hr>
<h2><a id="user-content-serverless-and-app-services" class="anchor" aria-hidden="true" href="#serverless-and-app-services"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Serverless-and-App-Services</h2>
<h3><a id="user-content-architecture-evolution" class="anchor" aria-hidden="true" href="#architecture-evolution"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Architecture Evolution</h3>
<h4><a id="user-content-monolithic" class="anchor" aria-hidden="true" href="#monolithic"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Monolithic</h4>
<ul>
<li>Fails together.
<ul>
<li>One error will bring the whole system down.</li>
</ul>
</li>
<li>Scales together.
<ul>
<li>Everything expects to be running on the same compute hardware</li>
</ul>
</li>
<li>Bills together.
<ul>
<li>All components are always running and always incurring charges.</li>
</ul>
</li>
</ul>
<p>This is the least cost effective way to architect systems.</p>
<h4><a id="user-content-tiered" class="anchor" aria-hidden="true" href="#tiered"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Tiered</h4>
<ul>
<li>Different components can be on the same server or different servers.</li>
<li>Components are coupled together because the endpoints connect together.</li>
<li>Can adjust the size of the server that is running each application tier.</li>
<li>Utilizes load balancers in between tiers to add capacity.</li>
<li>Tiers are still tightly coupled.
<ul>
<li>Tiers expect a response from each other. If one tier fails, subsequent
tiers will also fail because they will not receive the proper response.</li>
<li>Back loads in one tier will impact the other tiers and customer experience.</li>
</ul>
</li>
<li>Tiers must be operational and send responses even if they are not processing
anything of value otherwise the system fails.</li>
</ul>
<h4><a id="user-content-evolving-with-queues" class="anchor" aria-hidden="true" href="#evolving-with-queues"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Evolving with Queues</h4>
<ul>
<li>Data no longer moves between tiers to be processed and instead uses a queue.
<ul>
<li>Often are <strong>FIFO</strong> (first in, first out)</li>
</ul>
</li>
<li>Data moves into a S3 bucket.</li>
<li>Detailed information is put into the next slot in the queue.
<ul>
<li>Tiers no longer expect an answer.</li>
</ul>
</li>
<li>Upload tier sends an async message.
<ul>
<li>The upload tier can add more messages to the queue.</li>
</ul>
</li>
<li>The queue will have an autoscaling group to increase processing capacity.</li>
<li>The autoscaling group will only bring up servers as they are needed.</li>
<li>The queue has the location of the S3 bucket and passes this onto the
processing tier.</li>
</ul>
<h4><a id="user-content-event-driven-architecture" class="anchor" aria-hidden="true" href="#event-driven-architecture"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Event Driven Architecture</h4>
<ul>
<li>Event producers
<ul>
<li>Interact with customers or systems monitoring components.</li>
<li>Produce events in reaction to something.</li>
<li>Clicks, events, errors, actions</li>
</ul>
</li>
<li>Event consumers
<ul>
<li>Pieces of software waiting for events to occur.</li>
<li>Actions are taken and the system returns to waiting</li>
</ul>
</li>
<li>Services can be producers and consumers at once.</li>
<li>Resources are not waiting around to be used.</li>
<li>Event router is needed for event driven architecture that also manages
an event bus.</li>
<li>Only consumes resources while handling events.</li>
</ul>
<h3><a id="user-content-aws-lambda" class="anchor" aria-hidden="true" href="#aws-lambda"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>AWS Lambda</h3>
<ul>
<li>Function-as-a-service (FaaS)
<ul>
<li>Service accepts functions.</li>
</ul>
</li>
<li>Event driven invocation (execution) based on an event occurring.</li>
<li><strong>Lambda function</strong> is piece of code in one language.</li>
<li>Lambda functions use a <strong>runtime</strong> (e.g. Python 3.6)</li>
<li>Runs in a <strong>runtime environment</strong>.
<ul>
<li>Virtual environment that is ready to go to run code in that language.</li>
<li>You are billed only for the duration a function runs.</li>
<li>There is no charge for having lambda functions waiting and ready to go.</li>
</ul>
</li>
</ul>
<h4><a id="user-content-lambda-architecture" class="anchor" aria-hidden="true" href="#lambda-architecture"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Lambda Architecture</h4>
<p>Best practice is to make it very small and very specialized.
Lambda function code, when executed is known as being <strong>invoked</strong>.
When invoked, it runs inside a runtime environment that matches the language the
script is written in.
The runtime environment is allocated a certain amount of memory and an
appropriate amount of CPU. The more memory you allocate, the more CPU it gets,
and the more the function costs to invoke per second.</p>
<p>Lambda functions can be given an IAM role or <strong>execution role</strong>.
The execution role is passed into the runtime environment.
Whenever that function executes, the code inside has access to whatever
permissions the role's permission policy provides.</p>
<p>Lambda can be invoked in an <strong>event-driven</strong> or <strong>manual</strong> way.
Each time you invoke a lambda function, the environment provided is new.
Never store anything inside the runtime environment, it is ephemeral.</p>
<p>Lambda functions by default are public services and can access any websites.
By default they cannot access private VPC resources, but can be configured
to do so if needed. Once configured, they can only access resources within a VPC.
Unless you have configured your VPC to have all of the configuration needed
to have public internet access or access to the AWS public space endpoints, then
the Lambda will not have access.</p>
<p>The Lambda runtime is stateless, so you should always use AWS services for input
and output. Something like DynamoDB or S3. If a Lambda is invoked by an event,
it gets details of the event given to it at startup.</p>
<p>Lambda functions can run up to 15 minutes. That is the max limit.</p>
<h4><a id="user-content-key-considerations" class="anchor" aria-hidden="true" href="#key-considerations"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Key Considerations</h4>
<ul>
<li>Currently 15 min execution limit.</li>
<li>Assume each execution gets a new runtime environment.</li>
<li>Use the execution role which is assumed when needed.</li>
<li>Always load data from other services from public APIs or S3.</li>
<li>Store data to other services (e.g. S3).</li>
<li>1M free requests and 400,000 GB-seconds of compute per month.</li>
</ul>
<h3><a id="user-content-cloudwatch-events-and-eventbridge" class="anchor" aria-hidden="true" href="#cloudwatch-events-and-eventbridge"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>CloudWatch Events and EventBridge</h3>
<p>Delivers near real time stream of system events that describe changes in AWS
products and services. EventBridge will replace CW Events.
EventBridge can also handle events from third parties. Both share the same
underlying architecture. AWS is now encouraging a migration to EB.</p>
<h4><a id="user-content-cloudwatch-events-key-concepts" class="anchor" aria-hidden="true" href="#cloudwatch-events-key-concepts"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>CloudWatch Events Key Concepts</h4>
<p>They can observe if X happens at Y time(s), do Z.</p>
<ul>
<li>X is a supported service which is a producer of an event.</li>
<li>Y can be a certain time or time period.</li>
<li>Z is a supported target service to deliver the event to.</li>
</ul>
<p>EventBridge is basically CloudWatch Events V2 that uses the same underlying
APIs and has the same architecture, but with additional features.
Things created in one can be visible in the other for now.</p>
<p>Both systems have a default Event bus for a single AWS account.
A bus is a stream of events which occur for any supported service inside an
AWS account.
In CW Events, there is only one bus (implicit), this is not exposed.
EventBridge can have additional event buses for your applications or third party
applications and services.
These can be interacted with in the same way as the default bus.</p>
<p>In both services, you create rules and these rules pattern match events which
occur on the buses and when they see an event which matches, they deliver
that event to a target. Alternatively you can have schedule based rules
which match a certain date and time or ranges of dates and times.</p>
<p>Rules match incoming events or schedules. The rule matches an event and routes
that event to one or more targets as you define on that rule.</p>
<p>Architecturally at the heart of event bridge is the default account event bus.
This is a stream of events generated by supported services within the AWS
account. Rules are created and these are linked to a specific event bus
or the default event bus. Once the rule completes pattern matching, the rule
is executed and moves that event that it matched through to one or more targets.
The events themselves are JSON structures and the data can be used by the
targets.</p>
<h3><a id="user-content-application-programming-interface-api-gateway" class="anchor" aria-hidden="true" href="#application-programming-interface-api-gateway"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Application Programming Interface (API) Gateway</h3>
<ul>
<li>A way applications or services can communicate with each other.</li>
<li>API gateway is an AWS managed service.
<ul>
<li>Provides managed AWS endpoints.</li>
<li>Can also perform authentication to prove you are who you claim.</li>
<li>You can create an API and present it to your customers for use.</li>
</ul>
</li>
<li>Allows you to create, publish, monitor, and secure APIs.</li>
<li>Billed based on:
<ul>
<li>number of API calls</li>
<li>amount of data transferred</li>
<li>additional performance features such as caching</li>
</ul>
</li>
<li>Serve as an entry point for serverless architecture.</li>
<li>If you have on premises legacy services that use APIs, this can be integrated.</li>
</ul>
<p>Great during an architecture evolution because the endpoints don't change.</p>
<ol>
<li>Create a managed API and point at the existing monolithic application.</li>
<li>Using API gateway allows the business to evolve along the way slowly.
This might move some of the data to fargate and aurora architecture.</li>
<li>Move to a full serverless architecture with DynamoDB.</li>
</ol>
<h3><a id="user-content-serverless" class="anchor" aria-hidden="true" href="#serverless"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Serverless</h3>
<p>This is not one single thing, you manage few if any servers.
This aims to remove overhead and risk as much as possible.
Applications are a collection of small and specialized functions that do
one thing really well and then stop.</p>
<p>These functions are stateless and run in ephemeral environments.
Every time they run, they obtain the data that they need, they do something
and then optionally, they store the result persistently somehow or deliver
the output to something else.</p>
<p>Generally, everything is event driven. Nothing is running until it's required.
While not being used, there should be little to no cost.</p>
<p>Should use managed services when possible.</p>
<p>Aim is to consume as a service whatever you can, code as little as possible,
and use function as a service for any general purpose compute needs, and
then use all of those building blocks together to create your application.</p>
<h4><a id="user-content-example-of-serverless" class="anchor" aria-hidden="true" href="#example-of-serverless"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Example of Serverless</h4>
<p>A user wants to upload videos to a website for transcoding.</p>
<ol>
<li>User browses to a static website that is running the uploader. The JS runs
directly from the web browser.</li>
<li>Third party auth provider, google in this case, authenticates via <strong>token</strong>.</li>
<li>AWS cannot use tokens provided by third parties. <strong>Cognito</strong> is called to
swap the third party token for AWS credentials.</li>
<li>Service uses these temporary credentials to upload a video to S3 bucket.</li>
<li>Bucket will generate an event once it has completed the upload.</li>
<li>A lambda triggers to transcode the video as needed. The
transcoder will get the original S3 bucket video location and will use
this for its workload.</li>
<li>Output will be added to a new transcode bucket and will put an entry into
DynamoDB.</li>
<li>User can interact with another Lambda to pull the media from the
transcode bucket using the DynamoDB entry.</li>
</ol>
<h3><a id="user-content-simple-notification-service-sns" class="anchor" aria-hidden="true" href="#simple-notification-service-sns"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Simple Notification Service (SNS)</h3>
<ul>
<li>HA, Durable, PUB/SUB messaging service.</li>
<li>Public AWS service meaning to access it, you need network connectivity
with the Public AWS endpoints.</li>
<li>Coordinates sending and delivering of messages up to 256KB in size.
<ul>
<li>Messages are not designed for large binary files.</li>
</ul>
</li>
<li>SNS topics are the base entity of SNS.
<ul>
<li>Permissions are controlled and configuration for SNS is defined.</li>
</ul>
</li>
<li>Publisher sends messages to a topic.
<ul>
<li>Topics have subscribers which receive messages.</li>
</ul>
</li>
<li>Subscribers receive all of the messages sent to the Topic.
<ul>
<li>Subscribers can be HTTP and HTTPS endpoints, emails, or SQS queues.</li>
<li>Filters can be applied to limit messages sent to subscribers.</li>
</ul>
</li>
<li>Fanout allows for a single SNS topic with multiple SQS queues as subscribers.
<ul>
<li>Can create multiple related workflows.</li>
<li>Allows multiple SQS queues to process the workload in slightly different
ways.</li>
</ul>
</li>
</ul>
<p>Offers:</p>
<ul>
<li>Delivery Status including HTTP, Lambda, SQS</li>
<li>Delivery retries which ensure reliable delivery</li>
<li>HA and Scalable (Regional)</li>
<li>SSE (server side encryption)</li>
<li>Topics can be used cross-account via Topic Policy</li>
</ul>
<h3><a id="user-content-aws-step-functions" class="anchor" aria-hidden="true" href="#aws-step-functions"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>AWS Step Functions</h3>
<p>There are many problems with lambdas limitations that can be solved with
a state machine. A state machine is a workflow. It has a start point, end point
and in between there are states. States are things inside a State Machine which
can do things. States can do things, and take in data, modify data, and output
data.</p>
<p>State machine is designed to perform an activity or workflow with lots of
individual components and maintain the idea of data between those states.</p>
<p>Maximum duration for a state machine execution is 1 year.</p>
<p>Two types of workflow</p>
<ul>
<li>
<p>Standard</p>
<ul>
<li>Default</li>
<li>1 year workflow</li>
</ul>
</li>
<li>
<p>Express</p>
<ul>
<li>Designed for IOT or other high transaction uses</li>
<li>5 minute workflow</li>
<li>Provides better processing guarantees</li>
</ul>
</li>
</ul>
<p>Started via API Gateway, IOT Rules, EventBridge, Lambda. Generally used for
back end processing.</p>
<p>With State machines you can use a template to create and export State Machines
once they're configured to your liking, it's called Amazon States Language or
ASL. It's based on JSON.</p>
<p>State machines are provided permission to interact with other AWS services via
IAM roles.</p>
<h4><a id="user-content-step-function-states" class="anchor" aria-hidden="true" href="#step-function-states"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Step Function States</h4>
<p>States are the things inside a workflow, the things which occur. These states
are available.</p>
<ul>
<li>Succeed and Fail
<ul>
<li>the process will succeed or fail.</li>
</ul>
</li>
<li>Wait
<ul>
<li>will wait for a certain period of time</li>
<li>will wait until specific date and time</li>
</ul>
</li>
<li>Choice
<ul>
<li>different path is determined based on an import</li>
</ul>
</li>
<li>Parallel
<ul>
<li>will create parallel branches based on a choice</li>
</ul>
</li>
<li>Map
<ul>
<li>accepts a list of things</li>
<li>for each item in that list, performs an action or set of actions based on
that particular item.</li>
</ul>
</li>
<li>Task
<ul>
<li>represents a single unit of work performed by the State Machine.</li>
<li>it allows the state machine to actually do things.</li>
<li>can be integrated with many different services such as lambda, AWS batch,
dynamoDB, ECS, SNS, SQS, Glue, SageMaker, EMR, and lots of others.</li>
</ul>
</li>
</ul>
<h3><a id="user-content-simple-queue-service-sqs" class="anchor" aria-hidden="true" href="#simple-queue-service-sqs"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Simple Queue Service (SQS)</h3>
<p>Public service that provides fully managed highly available message queues.</p>
<ul>
<li>Replication happens within a region by default.
<ul>
<li>Messages are guaranteed in the order they were received</li>
<li>Provides FIFO with best effort, but no guarantee</li>
</ul>
</li>
<li>Messages up to 256KB in size.
<ul>
<li>Should link to larger sets of data if needed.</li>
</ul>
</li>
<li>Polling is checking for any messages on the queue.</li>
<li><strong>Visibility timeout</strong>
<ul>
<li>The amount of time a client has to process a message in some way</li>
<li>When a client polls and receives messages, they aren't deleted from the
queue and are hidden for the length of this timeout.</li>
<li>This is the amount of time that a client can wait to work on the messages.</li>
<li>If the client does not delete the message by the end, it will reappear in
the queue.</li>
</ul>
</li>
<li><strong>Dead-letter queue</strong>
<ul>
<li>if a message is received multiple times but is unable to be finished, this
puts it into a different workload to try and fix the corruption.</li>
</ul>
</li>
<li>ASG can scale and lambdas can be invoked based on queue length.</li>
<li>Standard queue
<ul>
<li>multi-lane HW</li>
<li>guarantee the order and at least once delivery.</li>
</ul>
</li>
<li>FIFO queue
<ul>
<li>single lane road with no way to overtake</li>
<li>guarantee the order and at exactly once delivery</li>
<li>3,000 messages p/s with batching or up to 300 messages p/s without</li>
</ul>
</li>
</ul>
<p>Billed on <strong>requests</strong> not messages. A request is a single request to SQS.
One request can return 0 - 10 messages up to 64KB data in total.
Since requests can return 0 messages, frequently polling a SQS Queue, makes it
less effective.</p>
<p>Two ways to poll</p>
<ul>
<li>
<p>short (immediate) : uses 1 request and can return 0 or more messages. If the
queue is empty, it will return 0 and try again. This hurts queues that stay
short</p>
</li>
<li>
<p>long (waitTimeSeconds) : it will wait for up to 20 seconds for messages
to arrive on the queue. It will sit and wait if none currently exist.</p>
</li>
</ul>
<p>Messages can live on SQS Queue for up to 15 days. They offer KMS encryption
at rest. Server side encryption. Data is encrypted in transit with SQS and any
clients.</p>
<p>Access to a queue is based on identity policies or a queue policy. Queue
policies only can allow access from an outside account. This is a resource policy.</p>
<h3><a id="user-content-kinesis" class="anchor" aria-hidden="true" href="#kinesis"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Kinesis</h3>
<ul>
<li>Scalable streaming service. It is designed to inject data from
lots of devices or lots of applications.</li>
<li>Many producers send data into a Kinesis Stream.</li>
<li>The stream can scale from low to near infinite data rates.</li>
<li>Highly available public service by design.</li>
<li>Streams store a 24-hour moving window of data.
<ul>
<li>Can be increased to 7 days.</li>
<li>Data 24 hours + 1s is replaced by new data entering the stream.</li>
</ul>
</li>
<li>Kinesis includes the storage costs within it for the amount of data
that can be ingested during a 24 hour period. However much you ingest during
24 hours, that's included.</li>
<li>Multiple consumers can access data from that moving window.
<ul>
<li>One might look at data points once per hour</li>
<li>Another looks at data 1 per minute.</li>
</ul>
</li>
<li>Kinesis stream starts with 1 shard and expands as needed.
<ul>
<li>Each shard can have 1MB/s for ingestion and 2MB/s consumption.</li>
</ul>
</li>
</ul>
<p><strong>Kinesis data records (1MB)</strong> are stored across shards and are the blocks
of data for a stream.</p>
<p><strong>Kinesis Data Firehose</strong> connects to a Kinesis stream. It can move the data
from a stream onto S3 or another service.</p>
<h3><a id="user-content-sqs-vs-kinesis" class="anchor" aria-hidden="true" href="#sqs-vs-kinesis"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>SQS vs Kinesis</h3>
<p>Kinesis</p>
<ul>
<li>Large throughput or large numbers of devices</li>
<li>Huge scale ingestion with multiple consumers</li>
<li>Rolling window for multiple consumers</li>
<li>Designed for data ingestion, analytics, monitoring, app clicks</li>
</ul>
<p>SQS</p>
<ul>
<li>1 thing sending messages to the queue</li>
<li>One consumption group from that tier</li>
<li>Allow for async communications</li>
<li>Once the message is processed, it is deleted</li>
</ul>
<hr>
<h2><a id="user-content-cdn-and-optimization" class="anchor" aria-hidden="true" href="#cdn-and-optimization"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>CDN-and-Optimization</h2>
<h3><a id="user-content-architecture-basics" class="anchor" aria-hidden="true" href="#architecture-basics"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Architecture Basics</h3>
<ul>
<li>CloudFront is a global object cache (CDN)</li>
<li>Download caching only</li>
<li>Content is cached in locations close to customers.</li>
<li>If the content is not available on the local cache when requested, CloudFront
will fetch the item and cache it and deliver it locally.</li>
<li>This provides lower latency and higher throughput for customers.</li>
<li>Can handle static and dynamic content.</li>
<li><strong>Origin</strong> the original location of your content, can be an S3 bucket or LB.</li>
<li><strong>Distribution</strong> the configuration unit of CloudFront.</li>
<li><strong>Edge locations</strong> global infrastructure which hosts a cache of your data.
<ul>
<li>There are over 200 edge locations.</li>
<li>They can be one or more racks in a third party server system.</li>
<li>Normally 90% storage with some small compute.</li>
</ul>
</li>
<li><strong>Regional Edge Cache</strong>
<ul>
<li>Larger version of an edge location.</li>
<li>Support a number of local edge locations.</li>
<li>Designed to hold more data to cache things which are accessed less often.</li>
<li>Provides another layer of caching.</li>
</ul>
</li>
</ul>
<h4><a id="user-content-caching-optimization" class="anchor" aria-hidden="true" href="#caching-optimization"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Caching Optimization</h4>
<p>Parameters can be passed on the url such as query string parameter.
An example is <code>?language=en</code> and <code>?language=es</code></p>
<p>Caching will cache each string parameter storing two different objects.
You must use the same string parameters again to retrieve them. If you remove
them and the object is not caching it will need to be fetched first.</p>
<p>If string parameters aren't involved in the caching, you can select no
to forward them to the origin.</p>
<p>If the application does use query string parameters, you can use all of them for
caching or just selected ones.</p>
<h3><a id="user-content-aws-certificate-manager-acm" class="anchor" aria-hidden="true" href="#aws-certificate-manager-acm"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>AWS Certificate Manager (ACM)</h3>
<ul>
<li>HTTP lacks encryption and is insecure</li>
<li>HTTPS uses SSL/TLS layer of encryption added to HTTP</li>
<li>Data is encrypted in-transit</li>
<li>Certificates allow servers to prove their identity</li>
<li>Signed by a trusted authority (CA).</li>
<li>To be secure, a website generates a certificate, and has a CA sign it. The
website then uses that certificate to prove its authenticity.</li>
<li>ACM allows you to create, renew, and deploy certificates.</li>
<li>Supported AWS services ONLY (CloudFront and ALB, NOT EC2)</li>
<li>If it's not a managed service, ACM doesn't support it.</li>
<li>CloudFront must have a trusted and signed certificate. Can't be self signed.</li>
</ul>
<h3><a id="user-content-origin-access-identity-oai" class="anchor" aria-hidden="true" href="#origin-access-identity-oai"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Origin Access Identity (OAI)</h3>
<ol>
<li>Identity can be associated with a CloudFront distribution.</li>
<li>The edge locations gain this identity.</li>
<li>Create or adjust the bucket policy on the S3 origin. Add an explicit allow
for the OAI. Can remove any other explicit allows on the OAI. This leaves
the implicit deny.</li>
</ol>
<p>As long as accesses are coming from the edge locations, it will know they
are from the OAI and allow them. Any direct attempts will not use the OAI and
will only get the implicit deny.</p>
<p>Best practice is to create one OAI per CloudFront distribution to manage
permissions.</p>
<h3><a id="user-content-aws-global-accelerator" class="anchor" aria-hidden="true" href="#aws-global-accelerator"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>AWS Global Accelerator</h3>
<ul>
<li>Move the AWS network closer to customers.</li>
<li>Designed to optimize the flow of data from users to your AWS infrastructure.</li>
<li>Generally customers who are further away from your infrastructure go through
more internet based hops and this means a lower quality connection.</li>
<li>Normal IP addresses are unicast IP addresses. These refer to one thing.</li>
<li>Global Accelerator starts with 2 <strong>anycast</strong> IP address
<ul>
<li>Special IP address</li>
<li>Anycast IPs allow a single IP to be in multiple locations.</li>
<li>Traffic initially uses public internet and enters Global Accelerator at
the closest edge location.</li>
<li>Traffic then flows globally across the AWS global backbone network.</li>
</ul>
</li>
<li>Global accelerator is a network product, can use TCP/UDP.</li>
</ul>
<hr>
<h2><a id="user-content-advanced-vpc" class="anchor" aria-hidden="true" href="#advanced-vpc"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Advanced-VPC</h2>
<h3><a id="user-content-vpc-flow-logs" class="anchor" aria-hidden="true" href="#vpc-flow-logs"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>VPC Flow Logs</h3>
<ul>
<li>Capture packet metadata, not packet contents.
<ul>
<li>Things like source IP</li>
<li>Destination IP</li>
<li>Packet size</li>
<li>Anything which could be observed from the outside of the packet.</li>
</ul>
</li>
<li>Capture data at various different monitoring points.
<ul>
<li>VPC: all interfaces in that vpc</li>
<li>Subnets: interfaces in that subnet</li>
<li>Interface directly</li>
</ul>
</li>
<li>VPC flow logs are not realtime</li>
<li>Destination can be S3 or CloudWatch logs</li>
<li>Flow log inheritance is downwards starting at the VPC.</li>
<li>RDS can use VPC flow logs</li>
<li>The packet will always have source, then destination, then response.</li>
</ul>
<h3><a id="user-content-egress-only-internet-gateway" class="anchor" aria-hidden="true" href="#egress-only-internet-gateway"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Egress-Only Internet Gateway</h3>
<ul>
<li>IPv4 addresses are private or public</li>
<li>NAT allows private IPs to access public networks and receive responses.</li>
<li>NAT will not allow externally initiated connections IN.</li>
<li>Using IPv6, all IPs are public.
<ul>
<li>Internet Gateway (IPv6) allows all IPs <strong>in</strong> and <strong>out</strong></li>
</ul>
</li>
<li>Egress-only is <strong>outbound only</strong> for IPv6. It is exactly the same as
NAT, only outbound only.</li>
<li>To configure the Egress-only gateway, you must add default IPv6 route <code>::/0</code>
added to RT with <code>eigw-id</code> as target.</li>
</ul>
<h3><a id="user-content-vpc-endpoints-gateway" class="anchor" aria-hidden="true" href="#vpc-endpoints-gateway"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>VPC Endpoints (Gateway)</h3>
<p>Allow a private only resource inside a VPC or any resource inside a private
only VPC access to S3 and DynamoDB.</p>
<p>Normally when you want to access a public service through a VPC, you
need infrastructure. You would create an IGW and attach it to the VPC.
Resources inside need to be granted IP address or implement one or more
NAT gateways which allow instances with private IP addresses to access
these public services.</p>
<p>When you allocate a gateway endpoint to a subnet, a prefix list is added
to the route table. The target is the gateway endpoint.
Any traffic destined for S3, goes via the gateway endpoint.
The gateway endpoint is highly available for all AZs in a region by default.</p>
<p>With a gateway endpoint you set which subnet will be used with it and
it will configure automatically.
A gateway endpoint is a VPC gateway object.
Endpoint policy controls what things can be connected to by that endpoint.</p>
<p>Gateway endpoints can only be used to access services in the same region.
Can't access cross-region services.</p>
<p>S3 buckets can be set to private only by allowing access ONLY from
a gateway endpoint. For anything else, the implicit deny will apply.</p>
<p>They are only accessible from inside that specific VPC.</p>
<h3><a id="user-content-vpc-endpoints-interface" class="anchor" aria-hidden="true" href="#vpc-endpoints-interface"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>VPC Endpoints (Interface)</h3>
<ul>
<li>Provide private access to AWS Public Services.
<ul>
<li>Anything EXCEPT S3 and DynamoDB</li>
</ul>
</li>
<li>These are not HA by default and are added to specific subnets.
<ul>
<li>For HA, add one endpoint, to one subnet, per AZ used in the VPC</li>
<li>Must add one endpoint for one subnet per AZ</li>
</ul>
</li>
<li>Network access controlled via security groups.</li>
<li>You can use Endpoint policies to restrict what can be accessed with
the endpoint.</li>
<li>ONLY TCP and IPv4 at the moment.</li>
<li>Behind the scenes, it uses PrivateLink.</li>
<li>Endpoint provides a <strong>NEW</strong> service endpoint DNS
<ul>
<li>e.g. <code>vpce-123-xyz.sns.us-east-1.vpce.amazonaws.com</code></li>
</ul>
</li>
<li>Regional DNS is one single DNS name that works whatever AZ you're using to
access the interface endpoint. Good for simplicity and HA.</li>
<li>Zonal DNS resolved to that one specific interface in that one specific AZ.</li>
<li>Either of those two points of endpoints can be used by applications to
directly and immediately utilize interface endpoints.</li>
<li>PrivateDNS associates R53 private hosted zone with your VPC. This private
hosted zone carries a replacement DNS record for the default service
endpoint DNS name. It overrides the default service DNS with a new version
that points at your interface endpoint. Enabled by default.</li>
</ul>
<h4><a id="user-content-gateway-endpoints-vs-interface-endpoints" class="anchor" aria-hidden="true" href="#gateway-endpoints-vs-interface-endpoints"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Gateway Endpoints vs Interface Endpoints</h4>
<p><strong>Gateway endpoints</strong> work using prefix lists and route tables so they do not
need changes to the applications. The application thinks it's communicating
directly with S3 or DynamoDB and all we're doing by using a gateway endpoint
is influencing the route that the traffic flow uses. Instead of using IGW,
it goes via gateway endpoint and can use private IP addressing.
<strong>highly available</strong></p>
<p><strong>Interface Endpoints</strong> uses DNS and a private IP address for the interface
endpoint. You can either use the endpoint specific DNS names or you can
enable PrivateDNS which overrides the default and allows unmodified
applications to access the services using the interface endpoint. This doesn't
use routing and only DNS.
<strong>not highly available</strong></p>
<h3><a id="user-content-vpc-peering" class="anchor" aria-hidden="true" href="#vpc-peering"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>VPC Peering</h3>
<p>Direct encrypted network link between two and only two VPCs.
Peering connection can be in the same or cross region and in the same or
across accounts.</p>
<p>When you create a VPC peer, you can enable an option so that public hostnames
of services in the peered VPC resolve to the private internal IPs. You
can use the same DNS names if its in peered VPCs or not. If you attempt
to resolve the public DNS hostname of an EC2 instance, it will resolve
to the private IP address of the EC2 instance.</p>
<p>VPCs in the same region can reference each other by using security group id.
You can do the same efficient referencing and nesting of security groups that
you can do if you're inside the same VPC. This is a feature that only works
with VPC peers inside the same region.</p>
<p>In different regions, you can utilize security groups, but you'll need to
reference IP addresses or IP ranges. If VPC peers are in the same region,
then you can do the logical referencing of an entire security group.</p>
<p>VPC peering connects <strong>ONLY TWO</strong></p>
<p>VPC Peering does not support <strong>transitive peering</strong>.
If you want to connect 3 VPCs, you need 3 connections. You can't route
through interconnected VPCs.</p>
<p>VPC Peering Connections CANNOT be created with overlapping VPC CIDRs.</p>
<hr>
<h2><a id="user-content-hybrid-and-migration" class="anchor" aria-hidden="true" href="#hybrid-and-migration"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Hybrid-and-Migration</h2>
<h3><a id="user-content-aws-site-to-site-vpn" class="anchor" aria-hidden="true" href="#aws-site-to-site-vpn"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>AWS Site-to-Site VPN</h3>
<ul>
<li>A logical connection between a VPC and on-premise network encrypted in transit
using IPSec, running over the public internet.</li>
<li>This can be fully Highly Available if you design it correctly</li>
<li>Quick to provision, less than an hour.</li>
<li>VPNs connect VPCs and private on-prem networks.</li>
<li>Virtual Private Gateway (VGW) is the target on one or more route tables</li>
<li>Customer Gateway (CGW)
<ul>
<li>logical piece of configuration on AWS</li>
<li>thing that configuration represents</li>
</ul>
</li>
<li>VPN connection itself stores the config and links to one VGW and one CGW</li>
<li>Speed cap on VPN with two tunnels of 1.25 Gbps (gigabits per second).
<ul>
<li>AWS limit, will need to check speed supported by customer router.</li>
<li>Will be processing overhead on encrypting and decrypting data.
At high speeds, this overhead can be significant.</li>
</ul>
</li>
<li>Latency is inconsistent because it uses the public internet.</li>
<li>Cost
<ul>
<li>AWS charges hourly</li>
<li>GB transfer out cost</li>
<li>on-premises internet connection costs</li>
</ul>
</li>
<li>VPN setup of hours or less</li>
<li>Great as a backup especially for Direct Connect (DX)</li>
</ul>
<h3><a id="user-content-aws-direct-connect-dx" class="anchor" aria-hidden="true" href="#aws-direct-connect-dx"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>AWS Direct Connect (DX)</h3>
<ul>
<li>Port operating at a certain speed which belongs to a certain AWS account.</li>
<li>Allocated at a DX location which is a major data center.</li>
<li>Two speeds
<ul>
<li>1 Gpbs: 1000-Base-LX</li>
<li>10 Gbps: 10GBASE-LR</li>
</ul>
</li>
<li>This is a cross connect to your customer router (requires VLANS/BGP)</li>
<li>You can connect to a partner router if extending to your location.
<ul>
<li>The port needs to be arranged to connect somewhere else and connect to
your hardware.</li>
</ul>
</li>
<li>This is a single fiber optic cable from the DX port to your network.</li>
<li>VIFs are multiple virtual interfaces (VIFs) over one DX
<ul>
<li>Private VIF (VPC)
<ul>
<li>Represents one VPC</li>
<li>Can have as many Private VIFs as you want.</li>
</ul>
</li>
<li><strong>Public VIF</strong> (Public Zone Services)
<ul>
<li>Only public services, not public internet</li>
</ul>
</li>
</ul>
</li>
</ul>
<p>Has one physical cable with no high availability and no encryption.
DX Port Provisioning is likely quick, the cross-connect takes longer.
Can take weeks or month for physical cable to be installed.
Generally use a VPN first then bring a DX in and leave VPN as backup.</p>
<ul>
<li>Up to 40 Gbps with aggregation, 4 x 10 Gbps ports.</li>
<li>It does not use public internet and provides consistently low latency.
<ul>
<li>Does not consume any data.</li>
</ul>
</li>
</ul>
<p>DX provides NO ENCRYPTION and needs to be managed on a per application basis.
There is a common way around this limitation.
The Public VIF allows connections to AWS public services. Inside the VPC we
already have a virtual private gateway, because this is used for any private
VIFs running over the Direct Connect. Creating a virtual private gateway
creates end points that are located inside the AWS public zone with public
IP addresses. These end points have already been created and they already
exist. We can create a VPN and instead of using the public internet as the
transit network, you can use the public VIF running over Direct Connect.</p>
<p>You run an IPSEC VPN over the public VIF, over the Direct Connect connection,
you get all of the benefits of Direct Connect such as high speeds, and all
the benefits of IPSEC encryption.</p>
<h3><a id="user-content-aws-transit-gateway-tgw" class="anchor" aria-hidden="true" href="#aws-transit-gateway-tgw"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>AWS Transit Gateway (TGW)</h3>
<ul>
<li>Network transit hub to connect VPCs to on premises networks</li>
<li>Significantly reduces network complexity.
<ul>
<li>Supports transitive routing. No need to create a mesh topology.</li>
</ul>
</li>
<li>Single network gateway object which makes it HA and scalable.</li>
<li>Create attachments to allow Transit Gateway to connect to other network objects.
<ul>
<li>VPC attachments</li>
<li>Site to Site VPN attachments</li>
<li>Direct Connect attachments</li>
</ul>
</li>
<li>VPC attachments are configured with a subnet in each AZ where service
is required.</li>
<li>Can be used to create global networks.
<ul>
<li>You can use these for cross-region peering attachments.</li>
</ul>
</li>
<li>Can share between accounts using AWS RAM</li>
</ul>
<h3><a id="user-content-storage-gateway" class="anchor" aria-hidden="true" href="#storage-gateway"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Storage Gateway</h3>
<ul>
<li>Hybrid Storage Virtual Application (On-premise)
<ul>
<li>Can be run inside AWS as part of certain disaster recovery scenarios</li>
<li>Allows for migration of existing infrastructure into AWS slowly.</li>
</ul>
</li>
<li>Tape Gateway (VTL) Mode
<ul>
<li>Virtual Tapes are stored on S3</li>
</ul>
</li>
<li>File Mode (SMB and NFS)
<ul>
<li>File Storage Backed by S3 Objects</li>
</ul>
</li>
<li>Volume Mode (Gateway Stored)
<ul>
<li>Block Storage backed by S3 and EBS</li>
<li>Great for disaster recovery</li>
<li>Data is kept locally</li>
<li>Awesome for migrations</li>
</ul>
</li>
<li>Volume Mode (Cache Mode)
<ul>
<li>Data as added to gateway is not stored locally.</li>
<li>Backup to EBS Snapshots</li>
<li>Primarily stored on AWS</li>
<li>Great for limited local storage capacity.</li>
</ul>
</li>
</ul>
<h3><a id="user-content-snowball--edge--snowmobile" class="anchor" aria-hidden="true" href="#snowball--edge--snowmobile"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Snowball / Edge / Snowmobile</h3>
<p>Designed to move large amounts of data IN and OUT of AWS.
Physical storage the size of a suitcase or truck.
Ordered from AWS, use, then return.</p>
<h4><a id="user-content-snowball" class="anchor" aria-hidden="true" href="#snowball"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Snowball</h4>
<ul>
<li>Any data on Snowball uses KMS at rest encryption.</li>
<li>1 Gbps or 10 Gbps connection</li>
<li>50TB or 80TB Capacity.
<ul>
<li>10TB to 10PB of data is economical range.</li>
<li>Good for multiple locations</li>
</ul>
</li>
<li>No compute</li>
</ul>
<h4><a id="user-content-snowball-edge" class="anchor" aria-hidden="true" href="#snowball-edge"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Snowball Edge</h4>
<ul>
<li>Includes both storage and compute</li>
<li>Larger capacity vs snowball.</li>
<li>Faster networking over Snowball
<ul>
<li>10 Gbps or up to 100 Gbps</li>
</ul>
</li>
<li>Three types of Snowball Edge
<ul>
<li>Storage optimized
<ul>
<li>80TB storage, 24 vCPU, 32 GiB RAM</li>
<li>(with EC2) includes 1TB SSD</li>
</ul>
</li>
<li>Compute optimized
<ul>
<li>100TB storage, 7.68 GB NVME (fast PCI bus storage),52 vCPU, 208 GiB RAM</li>
</ul>
</li>
<li>Compute with GPU
<ul>
<li>Same as compute, but with GPU</li>
</ul>
</li>
</ul>
</li>
</ul>
<h4><a id="user-content-snowmobile" class="anchor" aria-hidden="true" href="#snowmobile"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Snowmobile</h4>
<p>Portable data center within a shipping container on a truck.
This is a special order and is not available in high volume.
Ideal for single location where 10 PB+ is required.
Max is 100 PB per snowmobile.</p>
<h3><a id="user-content-aws-directory-service" class="anchor" aria-hidden="true" href="#aws-directory-service"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>AWS Directory Service</h3>
<p>Directories stores objects, users, groups, computers, servers, file shares with
a structure called a domain / tree. Multiple trees can be grouped into a forest.</p>
<p>Devices can join a directory so laptops, desktops, and servers can all have
a centralized management and authentication. You can sign into multiple
devices with the same username and password.</p>
<p>One common directory is <strong>Active Directory</strong> by Microsoft and its full name is
<strong>Microsoft Active Directory Domain Services</strong> or AD DS.</p>
<ul>
<li>AWS managed implementation.</li>
<li>Runs within a VPC as a private service.</li>
<li>Provides HA by deploying into multiple AZs.</li>
<li>Certain services in AWS need a directory, Amazon Workspaces.</li>
<li>To join EC2 instances to a domain you need a directory.</li>
<li>Can be isolated inside AWS only or integrated with existing on-prem system.</li>
<li>Connect Mode allows you to proxy back to on-premises.</li>
</ul>
<h4><a id="user-content-directory-modes" class="anchor" aria-hidden="true" href="#directory-modes"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Directory Modes</h4>
<ul>
<li><strong>Simple AD</strong>: should be default. Designed for simple requirements.</li>
<li><strong>Microsoft AD</strong>: is anything with Windows or if it needs a trust relationship
with on-prem. This is not an emulation or adjusted by AWS.</li>
<li><strong>AD Connector</strong>: Use AWS services without storing any directory info in the
cloud, it proxies to your on-prem directory.</li>
</ul>
<h3><a id="user-content-aws-datasync" class="anchor" aria-hidden="true" href="#aws-datasync"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>AWS DataSync</h3>
<ul>
<li>Data transfer service TO and FROM AWS.</li>
<li>This is used for migrations or for large amounts of data processing transfers.</li>
<li>Designed to work at huge scales. Each agent can handle 10 Gbps and each job
can handle 50 million files.</li>
<li>Transfers metadata and timestamps</li>
<li>Each agent is about 100 TB per day.</li>
<li>Can use bandwidth limiters to avoid customer impact</li>
<li>Supports incremental and scheduled transfer options</li>
<li>Compression and encryption in transit is also supported</li>
<li>Has built in data validation and automatic recovery from transit errors.</li>
<li>AWS service integration with S3, EFS, FSx for Windows servers.</li>
<li>Pay as you use product.</li>
</ul>
<h4><a id="user-content-aws-datasync-components" class="anchor" aria-hidden="true" href="#aws-datasync-components"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>AWS DataSync Components</h4>
<ul>
<li>Task
<ul>
<li>job within datasync</li>
<li>defines what is being synced how quickly</li>
<li>defines two locations involved in the job</li>
</ul>
</li>
<li>Agent
<ul>
<li>software to read and write to on prem such as NFS or SMB</li>
<li>used to pull data off that store and move into AWS or vice versa</li>
</ul>
</li>
<li>Location
<ul>
<li>every task has two locations <code>FROM</code> and <code>TO</code></li>
<li>example locations:
<ul>
<li>network file systems (NFS), common in Linux or Unix</li>
<li>server message block (SMB), common in Windows environments</li>
<li>AWS storage services (EFS, FSx, and S3)</li>
</ul>
</li>
</ul>
</li>
</ul>
<h3><a id="user-content-fsx-for-windows-file-server" class="anchor" aria-hidden="true" href="#fsx-for-windows-file-server"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>FSx for Windows File Server</h3>
<ul>
<li>Fully managed native windows file servers/shares</li>
<li>Designed for integration with Windows environments.
<ul>
<li>native Windows file system, not emulated server</li>
</ul>
</li>
<li>Integrates with Directory Service or Self-Managed AD</li>
<li>Can be used in <strong>Single</strong> or <strong>Multi-AZ</strong> within a VPC.
<ul>
<li>This controls the network interfaces that are available.</li>
<li>Single mode use replication in the AZ to ensure resiliency.</li>
</ul>
</li>
<li>Can perform full range of different backups
<ul>
<li>Client side and AWS side</li>
<li>Can perform automatic and on-demand backups.</li>
</ul>
</li>
<li>File systems can be access using VPC, Peering, VPN, Direct Connect. Native
windows filesystem or Directory Services.</li>
</ul>
<h4><a id="user-content-words-to-look-for" class="anchor" aria-hidden="true" href="#words-to-look-for"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Words to look for</h4>
<ul>
<li>VSS: User Driven Restores</li>
<li>Native File System (NFS) accessible over SMB</li>
<li>Windows permissions model</li>
<li>Product supports DFS, scale out file share.</li>
<li>Managed service, no file server admin</li>
<li>Integrates with DS and your own directory.</li>
</ul>
<hr>
<h2><a id="user-content-security-deployment-operations" class="anchor" aria-hidden="true" href="#security-deployment-operations"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Security-Deployment-Operations</h2>
<h3><a id="user-content-aws-secrets-manager" class="anchor" aria-hidden="true" href="#aws-secrets-manager"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>AWS Secrets Manager</h3>
<ul>
<li>Share functionality with parameter store. Sometimes both are appropriate.</li>
<li>Designed specifically for secrets, passwords, API keys.</li>
<li>Usable via Console, CLI, API, or SDK (integration)</li>
<li>Supports the automatic rotation of secrets using Lambda.</li>
<li>Directly integrates with RDS and a limited set of AWS products. If lambda
is invoked and changes a secret, the password can automatically change in RDS.</li>
<li>Secrets are encrypted at rest.</li>
<li>Integrates with IAM, can use IAM permissions to control access to secrets.</li>
</ul>
<h4><a id="user-content-secrets-manager-example" class="anchor" aria-hidden="true" href="#secrets-manager-example"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Secrets Manager Example</h4>
<ol>
<li>The Secrets Manager SDK retrieves database credentials.</li>
<li>SDK uses IAM credentials to retrieve the secrets.</li>
<li>Application uses the secrets to access the database.</li>
<li>Periodically, a lambda function is invoked to rotate the secrets.</li>
<li>The Lambda uses an execution role to get permissions.</li>
</ol>
<p>Secrets are secured using KMS so you never risk any leakage via physical access
to the AWS hardware and KMS ensures role separation.</p>
<h3><a id="user-content-aws-shield-and-waf-web-application-firewall" class="anchor" aria-hidden="true" href="#aws-shield-and-waf-web-application-firewall"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>AWS Shield and WAF (Web Application Firewall)</h3>
<p>Provides against DDoS attacks with AWS resources. This is a denial of
service attack. Normally not possible to block them by using individual
IP addresses. Without detailed analysis, the traffic looks like normal
requests to your website.</p>
<ul>
<li>
<p>Shield Standard</p>
<ul>
<li>Free with Route53 and CloudFront as default</li>
<li>Provides layer 3 and layer 4 protection against DDoS attacks.</li>
</ul>
</li>
<li>
<p>Shield advanced</p>
<ul>
<li>$3000 per month</li>
<li>Includes EC2, ELB, CloudFront, Global Acceleration and R53</li>
<li>Provides access to DDoS advanced response team and financial insurance
against increased costs.</li>
</ul>
</li>
<li>
<p>WAF (web application firewall)</p>
<ul>
<li>Layer 7 firewall (HTTP/s) firewall</li>
<li>Protects against complex layer 7 attacks:
<ul>
<li>SQL injections</li>
<li>cross-site scripting</li>
<li>geo blocks</li>
<li>rate awareness</li>
</ul>
</li>
<li>WEBACL integrated with Load Balancers, API gateways, and CloudFront.
<ul>
<li>Rules are added to WEBACL and evaluated when traffic arrives.</li>
</ul>
</li>
</ul>
</li>
</ul>
<h4><a id="user-content-example-of-architecture" class="anchor" aria-hidden="true" href="#example-of-architecture"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Example of Architecture</h4>
<p>Shield standard automatically looks at the data before any data reaches
past Route53.
The user is directed to the closest CloudFront location. Again, shield
standard looks at the data again before it moves on.</p>
<p>WAF Rules are defined and included in a WEBACL which is associated to a
cloud front distribution and deployed to the edge.</p>
<p>Shield advanced can then intercept traffic when it reaches the load balancer.
Once the data reaches the VPC, it has been filtered at Layer 3, 4, and 7
already.</p>
<p>Layer 7 filtering is only provided by WAF.</p>
<h3><a id="user-content-cloudhsm" class="anchor" aria-hidden="true" href="#cloudhsm"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>CloudHSM</h3>
<p>KMS is the key management service within AWS. It is used for encryption within
AWS and it integrates with other AWS products. Can generate keys, manage
keys, and can integrate for encryption. The problem is this is a shared
service. You're using a service which other accounts within AWS also use.
Although the permissions are strict, AWS still does manage the hardware for KMS.
KMS is a hardware security module or HSM. These are industry standard pieces
of hardware which are designed to manage keys and perform cryptographic
operations.</p>
<p>You can run your own HSM on premise. Cloud HSM is a true "single tenant"
hardware security module (HSM) that's hosted within the AWS cloud.
AWS provisions the HW, but it is impossible for them to help. There is no way
to recover data from them if access is lost.</p>
<p>Fully FIPS 140-2 Level 3 (KSM is L2 overall, but some is L3)
IF you require level 3 overall, you MUST use CloudHSM.</p>
<p>KSM all actions are performed with AWS CLI and IAM roles.</p>
<p>HSM will not integrate with AWS by design and uses industry standard APIs.</p>
<ul>
<li>PKCS#11</li>
<li>Java Cryptography Extensions (JCE)</li>
<li>Microsoft CryptoNG (CNG) libraries</li>
</ul>
<p>KMS can use CloudHSM as a custom key store, CloudHSM integrates with KMS.</p>
<p>HSM is not highly available and runs within one AZ. To be HA, you need at least
two HSM devices and one in each AZ you use. Once HSM is in a cluster, they
replicate all policies in sync automatically.</p>
<p>HSM needs an endpoint in the subnet of the VPC to allow resources access
to the cluster.</p>
<p>AWS has no access to the HSM appliances which store the keys.</p>
<h4><a id="user-content-cloud-hsm-use-cases" class="anchor" aria-hidden="true" href="#cloud-hsm-use-cases"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Cloud HSM Use Cases</h4>
<ul>
<li>No native AWS integration with AWS products. You can't use S3 SSE with
CloudHSM.</li>
<li>Can offload the SSL/TLS processing from webservers. CloudHSM
is much more efficient to do these encryption processes.</li>
<li>Oracle Databases can use CloudHSM to enable transparent data encryption (TDE)</li>
<li>Can protect the private keys an issuing certificate authority.</li>
<li>Anything that needs to interact with non AWS products.</li>
</ul>
<hr>
<h2><a id="user-content-nosql-and-dynamodb" class="anchor" aria-hidden="true" href="#nosql-and-dynamodb"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>NoSQL-and-DynamoDB</h2>
<h3><a id="user-content-dynamodb-architecture" class="anchor" aria-hidden="true" href="#dynamodb-architecture"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>DynamoDB Architecture</h3>
<p>NoSQL Database as a Service (DBaaS)</p>
<ul>
<li>Wide column Key/Value database.</li>
<li>Not like RDS which is a Database Server as a Product.
<ul>
<li>This is only the database.</li>
</ul>
</li>
<li>Capacity can be provisioned or use on-demand mode</li>
<li>Highly resilient across AZs and optionally globally resilient.</li>
<li>Data is replicated across multiple storage nodes by default.</li>
<li>Really fast, single digit millisecond access to data.</li>
<li>Supports backups with point in time recovery and encryption at rest.</li>
<li>Allows event-driven integration. Do things when data changes.</li>
</ul>
<h4><a id="user-content-dynamo-db-tables" class="anchor" aria-hidden="true" href="#dynamo-db-tables"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Dynamo DB Tables</h4>
<ul>
<li><strong>Table</strong> a grouping of items which share the same primary key.</li>
<li><strong>Items</strong> within a table are how you manage the data.
<ul>
<li>There is no limit to the number of items in a table.</li>
</ul>
</li>
<li>Two types of primary key:
<ul>
<li>Simple (Partition)</li>
<li>Composite (Partition and Sort)</li>
</ul>
</li>
<li>Every item in the table needs a unique primary key.</li>
<li>Attributes may or may not be there. This is not necessary.</li>
<li>Items can be at most 400KB in size. This includes the primary key and
attributes.</li>
</ul>
<p>In DynamoDB, capacity means speed. If you choose on-demand capacity model
you don't have to worry about capacity. You only pay for the operations
for the table.
If you choose provisioned capacity, you must set this on a per table basis.</p>
<p>Capacity is set per WCU or RCU</p>
<p>1 WCU means you can write 1KB per second to that table
1 RCU means you can read 4KB per second for that table</p>
<h4><a id="user-content-dynamo-db-backups" class="anchor" aria-hidden="true" href="#dynamo-db-backups"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Dynamo DB Backups</h4>
<p><strong>On-demand Backups</strong>: Similar to manual RDS snapshots. Full backup of the table
that is retained until you manually remove that backup. This can be used to
restore data in the same region or cross-region. You can adjust indexes, or
adjust encryption settings.</p>
<p><strong>Point-in-time Recovery</strong>: Must be enabled on each table and is off by
default. This allows continuous record of changes for 35 days to allow you to
replay any point in that window to a 1 second granularity.</p>
<h4><a id="user-content-dynamo-db-considerations" class="anchor" aria-hidden="true" href="#dynamo-db-considerations"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Dynamo DB Considerations</h4>
<ul>
<li>NoSQL, you should jump towards DynamoDB.</li>
<li>Relational data, this is NOT DynamoDB.</li>
<li>If you see key value and DynamoDB is an answer, this is likely the proper
choice.</li>
</ul>
<p>Access to Dynamo is from the console, CLI, or API. You don't have SQL access.</p>
<p>Billing based on:</p>
<ul>
<li>RCU and WCU</li>
<li>Storage on that table</li>
<li>Additional features on that table</li>
</ul>
<p>Can purchase reserved capacity with a cheaper rate for a longer term commit.</p>
<h3><a id="user-content-dynamodb-operations-consistency-and-performance" class="anchor" aria-hidden="true" href="#dynamodb-operations-consistency-and-performance"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>DynamoDB Operations, Consistency, and Performance</h3>
<h4><a id="user-content-dynamodb-reading-and-writing" class="anchor" aria-hidden="true" href="#dynamodb-reading-and-writing"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>DynamoDB Reading and Writing</h4>
<p><strong>On-Demand</strong>: Unknown or unpredictable load on a table. This is also good
for as little admin overhead as possible. Pay a price per million
Read or Write units. This is as much as 5 times the price as provisioned.</p>
<p><strong>Provisioned</strong>: RCU and WCU set on a per table basis.</p>
<p>Every operation consumes at least 1 RCU/WCU</p>
<p>1 RCU = 1 x 4KB read operation per second. This rounds up.
1 WCU = 1 x 1KB write operation per second.</p>
<p>Every single table has a WCU and RCU burst pool. This is 500 seconds
of RCU or WCU as set by the table.</p>
<h4><a id="user-content-query" class="anchor" aria-hidden="true" href="#query"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Query</h4>
<p>You have to pick one Partition Key (PK) value to start.</p>
<p>The PK can be the sensor unit, the Sort Key (SK) can be the day of the
week you want to look at.</p>
<p>Query accepts a single PK value and <strong>optionally</strong> a SK or range.
Capacity consumed is the size of all returned items. Further filtering
discards data, but capacity is still consumed.</p>
<p>In this example you can only query for one weather station.</p>
<p>If you query a PK it can return all fields items that match. It is always
more efficient to pull as much data as needed per query to save RCU.</p>
<p>You have to query for at least one item of PK and are charged for the
response of that query operation.</p>
<p>If you filter data and only look at one attribute, you will still be
charged for pulling all the attributes against that query.</p>
<h4><a id="user-content-scan" class="anchor" aria-hidden="true" href="#scan"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Scan</h4>
<p>Least efficient when pulling data from Dynamo, but the most flexible.</p>
<p>Scan moves through the table item by item consuming the capacity
of every item. Even if you consume less than the whole table, it will
charge based on that. It adds up all the values scanned and will charge
rounding up.</p>
<h4><a id="user-content-dynamodb-consistency-model" class="anchor" aria-hidden="true" href="#dynamodb-consistency-model"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>DynamoDB Consistency Model</h4>
<p><strong>Eventually</strong> Consistent: easier to implement and scales better
<strong>Strongly (Immediately)</strong> Consistent: more costly to achieve</p>
<p>Every piece of data is replicated between storage nodes. There is one
Leader storage node and every other node follows.</p>
<p>Writes are always directed to the <strong>leader node</strong>. Once the leader
is complete, it is <strong>consistent</strong>. It then starts the process of replication.
This typically takes milliseconds and assumes the lack of any faults on the
storage nodes.</p>
<p>Eventual consistent could lead to stale data if a node is checked before
replication completes. You get a discount for this risk.</p>
<p>A strongly consistent read always uses the leader node and is less
scalable.</p>
<p>Not every application can tolerate eventual consistency. If you have a stock
database or medical information, you must use strongly consistent reads.
If you can tolerate the cost savings you can scale better.</p>
<h4><a id="user-content-wcu-example-calculation" class="anchor" aria-hidden="true" href="#wcu-example-calculation"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>WCU Example Calculation</h4>
<ul>
<li>Store 10 items per second with 2.5K average size per item.</li>
<li>Calculate WCU per item, round up, then multiply by average per second.</li>
<li>(2.5 KB / 1 KB) = 3 * 10 p/s = 30 WCU</li>
</ul>
<h4><a id="user-content-rcu-example-calculation" class="anchor" aria-hidden="true" href="#rcu-example-calculation"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>RCU Example Calculation</h4>
<ul>
<li>Retrieve 10 items per second with 2.5K average size per item.</li>
<li>Calculate RCU per item, round up, then multiply by average per second.</li>
<li>(2.5 KB / 4 KB) = 1 * 10 p/s = 10 RCU for strongly consistent.
<ul>
<li>5 RCU for eventually consistent.</li>
</ul>
</li>
</ul>
<h3><a id="user-content-dynamodb-streams-and-triggers" class="anchor" aria-hidden="true" href="#dynamodb-streams-and-triggers"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>DynamoDB Streams and Triggers</h3>
<p>DynamoDB stream is a time ordered list of changes to items in a DynamoDB
table. A stream is a 24 hour rolling window of the changes.
It uses Kinesis streams on the backend.</p>
<p>This is enabled on a per table basis. This records</p>
<ul>
<li>Inserts</li>
<li>Updates</li>
<li>Deletes</li>
</ul>
<p>Different view types influence what is in the stream.</p>
<p>There are four view types that it can be configured with:</p>
<ul>
<li>KEYS_ONLY : only shows the item that was modified</li>
<li>NEW_IMAGE : shows the final state for that item</li>
<li>OLD_IMAGE : shows the initial state before the change</li>
<li>NEW_AND_OLD_IMAGES : shows both before and after the change</li>
</ul>
<p>Pre or post change state might be empty if you use
<strong>insert</strong> or <strong>delete</strong></p>
<h4><a id="user-content-trigger-concepts" class="anchor" aria-hidden="true" href="#trigger-concepts"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Trigger Concepts</h4>
<p>Allow for actions to take place in the event of a change in data</p>
<p>Item change generates an event that contains the data which
was changed. The specifics depend on the view type.
The action is taken using that data. This will combine the
capabilities of stream and lambda. Lambda will complete some compute based on
this trigger.</p>
<p>This is great for reporting and analytics in the event of changes such as
stock levels or data aggregation.
Good for data aggregation for stock or voting apps.
This can provide messages or notifications and eliminates the
need to poll databases.</p>
<h3><a id="user-content-dynamodb-local-lsi-and-global-gsi-secondary-indexes" class="anchor" aria-hidden="true" href="#dynamodb-local-lsi-and-global-gsi-secondary-indexes"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>DynamoDB Local (LSI) and Global (GSI) Secondary Indexes</h3>
<ul>
<li>Great for improving data retrieval in DynamoDB.</li>
<li>Query can only work on 1 PK value at a time and optionally a single
or range of SK values.</li>
<li>Indexes are a way to provide an alternative view on table data.</li>
<li>You have the ability to choose which attributes are projected
to the table.</li>
</ul>
<h4><a id="user-content-local-secondary-indexes-lsi" class="anchor" aria-hidden="true" href="#local-secondary-indexes-lsi"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Local Secondary Indexes (LSI)</h4>
<ul>
<li>Choose alternative sort key with the same partition key on base table data.
<ul>
<li>If item does not have sort key it will not show on the table.</li>
</ul>
</li>
<li>These must be created with a base table in the beginning.
<ul>
<li>This cannot be added later.</li>
</ul>
</li>
<li>Maximum of 5 LSIs per base table.</li>
<li>Uses the same partition key, but different sort key.</li>
<li>Shares the RCU and WCU with the table.</li>
<li>It makes a smaller table and makes <strong>scan</strong> operates easier.</li>
<li>In regards to Attributes, you can use:
<ul>
<li>ALL</li>
<li>KEYS_ONLY</li>
<li>INCLUDE</li>
</ul>
</li>
</ul>
<h4><a id="user-content-global-secondary-index-gsi" class="anchor" aria-hidden="true" href="#global-secondary-index-gsi"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Global Secondary Index (GSI)</h4>
<ul>
<li>Can be created at any time and much more flexible.</li>
<li>There is a default limit of 20 GSIs for each table.</li>
<li>Allows for alternative PK and SK.</li>
<li>GSI will have their own RCU and WCU allocations.</li>
<li>You can then choose which attributes are included in this table.</li>
<li>GSIs are <strong>always</strong> eventually consistent. Replication between
base and GSI is Async</li>
</ul>
<h4><a id="user-content-lsi-and-gsi-considerations" class="anchor" aria-hidden="true" href="#lsi-and-gsi-considerations"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>LSI and GSI Considerations</h4>
<ul>
<li>Must be careful which projections are used to manage capacity.</li>
<li>If you don't project a specific attribute, then you require the attribute when
querying data, it will then fetch the data later in an inefficient way.</li>
<li>This means you should try to plan what will be used on the front.</li>
</ul>
<p><strong>GSI as default</strong> and only use LSI when <strong>strong consistency</strong> is required</p>
<p>Indexes are designed when data is in a base table needs an alternative
access pattern. This is great for a security team or data science team
to look at other attributes from the original purpose.</p>
<h3><a id="user-content-dynamodb-global-tables" class="anchor" aria-hidden="true" href="#dynamodb-global-tables"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>DynamoDB Global Tables</h3>
<ul>
<li>Global tables provide multi-master cross-region replication.
<ul>
<li>All tables are the same.</li>
</ul>
</li>
<li>Tables are created in multiple AWS regions. In one of the tables, you
configure the links between all of the tables.</li>
<li>DynamoDB will enable replication between all of the tables.
<ul>
<li>Tables become table replicas.</li>
</ul>
</li>
<li>Between the tables, <strong>last writer wins</strong> in conflict resolution.
<ul>
<li>DynamoDB will pick the most recent write and replicate that.</li>
</ul>
</li>
<li>Reads and Writes can occur to any region and are replicated within a second.</li>
<li>Strongly Consistent Reads <strong>only</strong> in the same region as writes.
<ul>
<li>Application should allow for eventual consistency where data may be stale.</li>
<li>Replication is generally sub-second and depends on the region load.</li>
</ul>
</li>
<li>Provides Global HA and disaster recovery or business continuity easily.</li>
</ul>
<h3><a id="user-content-dynamodb-accelerator-dax" class="anchor" aria-hidden="true" href="#dynamodb-accelerator-dax"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>DynamoDB Accelerator (DAX)</h3>
<p>This is an in memory cache for Dynamo.</p>
<p><strong>Traditional Cache</strong>: The application needs to access some data and checks
the cache. If the cache doesn't have the data, this is known as a cache miss.
The application then loads directly from the database. It then updates the
cache with the new data. Subsequent queries will load data from the cache as
a cache hit and it will be faster</p>
<p><strong>DAX</strong>: The application instance has DAX SDK added on. DAX and dynamoDB are one
in the same. Application uses DAX SDK and makes a single call for the data which
is returned by DAX. If DAX has the data, then the data is returned directly. If
not it will talk to Dynamo and get the data. It will then cache it for future
use. The benefit of this system is there is only one set of API calls using
one SKD. It is tightly integrated and much less admin overhead.</p>
<h4><a id="user-content-dax-architecture" class="anchor" aria-hidden="true" href="#dax-architecture"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>DAX Architecture</h4>
<p>This runs from within a VPC and is designed to be deployed to multiple
AZs in that VPC. Must be deployed across AZs to ensure it is highly available.</p>
<p>DAX is a cluster service where nodes are placed into different AZs. There is
a <strong>primary node</strong> which is the read and write note. This replicates out to
other nodes which are <strong>replica nodes</strong> and function as read replicas. With this
architecture, we have an EC2 instance running an application and the DAX
SDK. This will communicate with the cluster. On the other side, the cluster
communicates with DynamoDB.</p>
<p>DAX maintains two different caches. First is the <strong>item cache</strong> and this caches
individual items which are retrieved via the <strong>GetItem</strong> or <strong>BatchGetItem</strong>
operation. These operate on single items and must specify the items partition
or sort key.</p>
<p>There is a <strong>query cache</strong> which holds data and the parameters used for the
original query or scan. Whole query or scan operations can be rerun
and return the same cached data.</p>
<p>Every DAX cluster has an endpoint which will load balance across the cluster.
If data is retrieved from DAX directly, then it's called a cache hit and the
results can be returned in microseconds.</p>
<p>Any cache misses, so when DAX has to consult DynamoDB, these are generally
returned in single digit milliseconds. Now in writing data to DynamoDB,
DAX can use write-through caching, so that data is written into DAX at the
same time as being written into the database.</p>
<p>If a cache miss occurs while reading, the data is also written to the primary
node of the cluster and the data is retrieved. And then it's replicated from
the primary node to the replica nodes.</p>
<p>When writing data to DAX, it can use write-through. Data is written to the
database, then written to DAX.</p>
<h4><a id="user-content-dax-considerations" class="anchor" aria-hidden="true" href="#dax-considerations"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>DAX Considerations</h4>
<ul>
<li>Primary node which writes and Replicas which support read operations.</li>
<li>Nodes are HA, if the primary node fails there will be an election and
secondary nodes will be made primary.</li>
<li>In-memory cache allows for much faster read operations and significantly
reduced costs. If you are performing the same set of read operations on the same
set of data over and over again, you can achieve performance improvements
by implementing DAX and caching those results.</li>
<li>With DAX you can scale up or scale out.</li>
<li>DAX supports write-through. If you write data to DynamoDB, you can
use the DAX SDK. DAX will handle that data being committed to DynamoDB
and also storing that data inside the cache.</li>
<li>DAX is not a public service and is deployed within a VPC. Anything
that uses that data many times will benefit from DAX.</li>
<li>Any questions which talk about caching with DynamoDB, assume it is DAX.</li>
</ul>
<h3><a id="user-content-amazon-athena" class="anchor" aria-hidden="true" href="#amazon-athena"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Amazon Athena</h3>
<ul>
<li>You can take data stored in S3 and perform Ad-hoc queries on data. Pay
only for the data consumed.</li>
<li>Start off with structured, semi-structured and even unstructured data that is
stored in its raw form on S3.</li>
<li>Athena uses <strong>schema-on-read</strong>, the original data is never changed
and remains on S3 in its original form.</li>
<li>The schema which you define in advance, modifies data in flight when its read.</li>
<li>Normally with databases, you need to make a table and then load the data in.</li>
<li>With Athena you create a schema and load data on this schema on the fly in
a relational style way without changing the data.</li>
<li>The output of a query can be sent to other services and can be
performed in an event driven fully serverless way.</li>
</ul>
<h4><a id="user-content-athena-explained" class="anchor" aria-hidden="true" href="#athena-explained"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Athena Explained</h4>
<p>The source data is stored on S3 and Athena can read from this data.
In Athena you are defining a way to get the original data and defining
how it should show up for what you want to see.</p>
<p>Tables are defined in advance in a data catalog and data is projected
through when read. It allows SQL-like queries on data without transforming
the data itself.</p>
<p>This can be saved in the console or fed to other visualization tools.</p>
<p>You can optimize the original data set to reduce the amount of space uses
for the data and reduce the costs for querying that data.</p>


