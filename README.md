<div>
  <img src="https://github.com/Tufts-Technology-Services/tailscale-now/assets/17954/aa17782b-a000-4ac2-8f9f-ba12819fcccf" width="100" />
  <img src="https://github.com/Tufts-Technology-Services/tailscale-now/assets/17954/261036db-8bb5-4f10-9451-57d987917de7" width="100" />
  <img src="https://github.com/Tufts-Technology-Services/tailscale-now/assets/17954/1d451bea-f95d-4762-bd07-46658bb1f57f" width="100" />
</div>

# Making tailscale a first class citizen

The purpose of this repository is to help answer questions to help make [Tailscale](https://tailscale.com/) a first class citizen 
within the list of components and tools we use at Tufts. We also want to use this repository to introduce 
Tailscale to other teams and see if it can help them on their daily activities.

### What is Tailscale?

There are many definitions out there about tailscale and most of them try to place it within the context of VPNs. Tailscale is an overlay network (a network on top of the physical network) that increases connectivity by removing some of the burdens introduced over the years in the networking stack (most of them in the name of security). You can also think about Tailscale as the “control plane” for [wireguard](https://www.wireguard.com/) connections (data plane). If you want a detailed explanation of what Tailscale is and how it works, I suggest you read [this document](https://tailscale.com/blog/how-tailscale-works). 

### How do we use it?

Tailscale is a very important component in our group (Data strategy team). Most of our communications happen on top of a tailnet (Tailscale’s network). Here are a few projects where we use Tailscale. 

#### Increased connectivity

All the [Denodo](https://www.denodo.com/en) servers are part of our Tailnet. Because of that we have been able to access those servers since day one independently of the underlying changes of the physical network.

#### Gitops
Our github runners use Tailscale to temporarily join our Tailnet and get the necessary access to do their jobs. As an example, we can update our prometheus server by pushing commits to our [observability stack project](https://github.com/TuftsUniversity/dscicd).

#### Better authentication
We can give access to our Tailscale users to our grafana dashboards (and other resources) without having to request another level of authentication. You have already authenticated to the network (the tailnet) so you don’t have to authenticate again when accessing, for example, a grafana dashboard. We can get your identity from the network. 

#### Seamless connectivity

Our dental users experienced some delays when using the software that runs in all the dental locations. We deployed a group of devices to collect telemetry over time to help us understand and quantify the issues. We shipped those machines to the different locations. After booting, all the machines join our Tailnet and start collecting metrics and sending them to our prometheus server.

#### Onboarding

We can onboard our consultants immediately by asking them to join our Tailnet and then give them access to our resources in a very granular manner.

### How can we help?

We want to make sure Tailscale is a first class component in the list of tools available at Tufts for whoever wants to use it. Do you think your Team may benefit from Tailscale? No? That’s ok. Yes? great, please, open an [issue](XXXX) so we can have a discussion to address all the questions you may have. 

Thank you for reading.


