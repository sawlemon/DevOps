# Google Professional Cloud Architect

https://www.udemy.com/course/google-cloud-platform-from-zero-to-hero-the-complete-guide

Google started their cloud journey with App Engine.

GCP has a different concept of subnets compared to other clouds.

- The frontend and backend isolation with the provate and public subnets is not here from my understanding so far.
- To isolate frontend from backend we need to create a totally new VPC and use firewall rules to restrict traffic.

![gcp-hierarchy](gcp-hierarchy.png)

### Shared VPCs
- VPCs are scoped to a GCP project, inorder to share VPC cross project the Shared VPC concept can be used.
- Host project is the one which shares the vpc to other project
- Service vpc is the one accessing the host project's VPC.


### How to choose a private access Implementation

![private-access-flowchart](pvt-acces-fc.png)

### Serverless VPC Access
- A non-vpc component needs to access a VPC component, then serverless VPC access is used
- A connector is spun up (basically a VM) which scales and acts as a proxy to our requests.