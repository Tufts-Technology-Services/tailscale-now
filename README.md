
<img src="https://github.com/Tufts-Technology-Services/tailscale-now/assets/17954/3ec0658c-0ada-4911-b163-d61573fd2724" width="400">

Create a [new ticket 🎫](https://github.com/Tufts-Technology-Services/tailscale-now/issues/new).

# Making tailscale a first class citizen in the Tufts Tool Ecosystem

The purpose of this repository is to facilitate discussions to make [Tailscale](https://tailscale.com/) a first class component at Tufts. We also want to introduce 
Tailscale to other teams to help them assess its utility and potential benefits for their specific requirements.

### What is Tailscale?

There are many definitions out there about tailscale and most of them frame it within the context of VPNs. It is much more than that. Tailscale is an overlay network, essentially a network built on top the existing physical network infrastructure. Its primary role is to enhance connectivity by alleviating various complexities that have accumulated in the networking stack over the years, many of which were implemented for security purposes.

You can also think about Tailscale as the “control plane” for [Wireguard](https://www.wireguard.com/) connections (data plane). If you want a detailed explanation of what Tailscale is and how it works, please read [this document](https://tailscale.com/blog/how-tailscale-works). 

### How do we use it in my team (data strategy)?

Tailscale is a core component for us. Most of our network communications happen on top of a tailnet (Tailscale’s network). Here are a few projects where we use Tailscale. 

#### Increased connectivity

All the [Denodo](https://www.denodo.com/en) servers are part of our Tailnet. Because of that, we have been able to access the resources they provide immediately, independently of the underlying physical network.

#### Gitops

Our [github runners](https://docs.github.com/en/actions/using-github-hosted-runners/about-github-hosted-runners) use Tailscale to access the resources they need to do their jobs. As an example, we can update our prometheus server by pushing commits to our [observability stack project](https://github.com/TuftsUniversity/dscicd).

#### Security without the churn

We can seamlessly grant our Tailscale users access to resources like Grafana dashboards without requiring a secondary authentication step. Once authenticated to the Tailnet, users need not re-authenticate for each resource. Their identity is effectively recognized and verified through the network itself, simplifying access and enhancing user experience.

#### Seamless connectivity

Our dental users experienced some delays when using the software that runs in all the dental locations. We deployed a group of devices to collect telemetry over time to help us understand and quantify the issues. We shipped those machines to the different locations. After booting, all the machines joined our Tailnet and start collecting metrics and sending them to our prometheus server. This data collection has been ongoing for several months now, providing us with valuable insights into the issues at hand.

#### Onboarding

We can onboard our consultants immediately by asking them to join our Tailnet (via email) and give them access to our resources in a very granular manner. For example, we want our denodo consultants to be able to access the http port on all the denodo servers. Once they have access we can create a denodo user for them with whatever permissions they require.

## How can we help?

Our objective is to make Tailscale a top-tier component within the set of tools offered at Tufts.
Curious about Tailscale or wondering if it could benefit your team? If you have questions or wish to discuss Tailscale's potential for your team, please [open an issue 🎫](https://github.com/Tufts-Technology-Services/tailscale-now/issues/new).

Thank you for reading.


