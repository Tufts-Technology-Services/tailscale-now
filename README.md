<div>
  <img src="[https://github.com/Tufts-Technology-Services/tailscale-now/assets/17954/261036db-8bb5-4f10-9451-57d987917de7](https://github.com/Tufts-Technology-Services/tailscale-now/assets/17954/2790c3f3-64ee-44b8-935f-124369472e5a)" width="400" />
</div>

# Making tailscale a first class citizen

The purpose of this repository is to capture discussions to help [Tailscale](https://tailscale.com/) become a first class component at Tufts. We also want to introduce 
Tailscale to other teams to help them determine if Tailscale can be useful for them.

### What is Tailscale?

There are many definitions out there about tailscale and most of them try to place it within the context of VPNs. Tailscale is an overlay network (a network on top of the physical network) that increases connectivity by removing some of the burdens introduced over the years in the networking stack (most of them in the name of security). You can also think about Tailscale as the “control plane” for [Wireguard](https://www.wireguard.com/) connections (data plane). If you want a detailed explanation of what Tailscale is and how it works, please read [this document](https://tailscale.com/blog/how-tailscale-works). 

### How do we use it in my team (data strategy)?

Tailscale is a very important component in our group (Data strategy). Most of our communications happen on top of a tailnet (Tailscale’s network). Here are a few projects where we use Tailscale. 

#### Increased connectivity

All the [Denodo](https://www.denodo.com/en) servers are part of our Tailnet. Because of that, we have been able to access those servers since day one independently of the underlying physical network.

#### Gitops

Our [github runners](https://docs.github.com/en/actions/using-github-hosted-runners/about-github-hosted-runners) use Tailscale to temporarily join our Tailnet and get the necessary access to do their jobs. As an example, we can update our prometheus server by pushing commits to our [observability stack project](https://github.com/TuftsUniversity/dscicd).

#### Better authentication

We can give access to our users (tailscale users) to our grafana dashboards (or any other resources) without having a second level of authentication. You have already authenticated to the network (the tailnet) so you don’t have to authenticate again when accessing, for example, a grafana dashboard. We can get your identity from the network.

#### Seamless connectivity

Our dental users experienced some delays when using the software that runs in all the dental locations. We deployed a group of devices to collect telemetry over time to help us understand and quantify the issues. We shipped those machines to the different locations. After booting, all the machines joined our Tailnet and start collecting metrics and sending them to our prometheus server. We have been collecting data for months now.

#### Onboarding

We can onboard our consultants immediately by asking them to join our Tailnet (via email) and give them access to our resources in a very granular manner. For example, we want our denodo consultants to be able to access the http port on all the denodo servers. Once they have access we can create a denodo user for them with whatever permissions they require.

## How can we help?

We want to make sure Tailscale is a first class component in the list of tools available at Tufts and it is available to everyone that wants to use it. 

Do you have questions about Tailscale? Do you think your Team may benefit from Tailscale? No? That’s ok. Yes? great, please, open an [issue](XXXX) so we can have discussions to address all the questions you may have. 

Thank you for reading.


