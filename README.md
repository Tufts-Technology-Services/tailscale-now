
<img src="https://github.com/Tufts-Technology-Services/tailscale-now/assets/17954/3ec0658c-0ada-4911-b163-d61573fd2724" width="400">

[new 🎫](https://github.com/Tufts-Technology-Services/tailscale-now/issues/new).

# Making tailscale a first class citizen in the Tufts Tool Ecosystem

The purpose of this repository is to facilitate discussions to help [Tailscale](https://tailscale.com/) become a first class tool component at Tufts. We also want to introduce 
Tailscale to other teams to help them assess its utility and potential benefits for their specific requirements.

### What is Tailscale?

There are many definitions out there about tailscale and most of them try to place it within the context of VPNs. Tailscale is an overlay network (a network on top of the physical network) that increases connectivity by removing some of the burdens introduced over the years in the networking stack (most of them in the name of security). You can also think about Tailscale as the “control plane” for [Wireguard](https://www.wireguard.com/) connections (data plane). If you want a detailed explanation of what Tailscale is and how it works, please read [this document](https://tailscale.com/blog/how-tailscale-works). 

### How do we use it in my team (data strategy)?

Tailscale is a core component for us. Most of our network communications happen on top of a tailnet (Tailscale’s network). Here are a few projects where we use Tailscale. 

#### Increased connectivity

All the [Denodo](https://www.denodo.com/en) servers are part of our Tailnet. Because of that, we have been able to access the resources they provide immediately, independently of the underlying physical network.

#### Gitops

Our [github runners](https://docs.github.com/en/actions/using-github-hosted-runners/about-github-hosted-runners) use Tailscale to access the resources they need to do their jobs. As an example, we can update our prometheus server by pushing commits to our [observability stack project](https://github.com/TuftsUniversity/dscicd).

#### Security without the churn

We can give access to our users (tailscale users) to our grafana dashboards (or any other resources) without having a second level of authentication. You have already authenticated to the network (the tailnet) so you don’t have to authenticate again when accessing, for example, a grafana dashboard. We can get your identity from the network.

#### Seamless connectivity

Our dental users experienced some delays when using the software that runs in all the dental locations. We deployed a group of devices to collect telemetry over time to help us understand and quantify the issues. We shipped those machines to the different locations. After booting, all the machines joined our Tailnet and start collecting metrics and sending them to our prometheus server. This data collection has been ongoing for several months now, providing us with valuable insights into the issues at hand.

#### Onboarding

We can onboard our consultants immediately by asking them to join our Tailnet (via email) and give them access to our resources in a very granular manner. For example, we want our denodo consultants to be able to access the http port on all the denodo servers. Once they have access we can create a denodo user for them with whatever permissions they require.

## How can we help?

We want to ensure that Tailscale is a first-class component among the tools available at Tufts. And we want this tool to be easily accessible to anyone who chooses to use it.

Curious about Tailscale or wondering if it could benefit your team? Whether you're uncertain or enthusiastic, we'd like to help! If you have questions or wish to discuss Tailscale's potential for your team, please open an issue. 

Thank you for reading.


