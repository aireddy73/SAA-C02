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

   
