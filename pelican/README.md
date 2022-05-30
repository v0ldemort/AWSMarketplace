## **Pelican on AWS marketplace**

### Overview
Datametica intends to bring its suite of products starting with the Pelican Data Verification product to the cloud marketplace. We have implemented support to launch and use Pelican over Kubernetes and can be integrated with AWS's EKS as a Kubernetes app from the marketplace.

Pelican can be deployed using helm charts on EKS. There are two offerings as shown in below architectural diagrams. In the case of UBB (Usage Based Billing) - the custom metered billing is applicable in the 'pay as you go model' - billed by AWS monthly. In the case of BYOL - the customer has to connect to DM support and ask for a Pelican product license.

### Deployment

** To deploy Pelican with usage base billing (UBB) model, refer: [Pelican UBB deployment document](Pelican-UBB-README.md)

** To deploy Pelican with bring your own license (BYOL), refer: [Pelican BYOL deployment document](Pelican-BYOL-README.md)

** To configure TLS Load Balancer, refer: [Access Pelican web UI over https](HTTPS.md)
