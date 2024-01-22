<div>
  <img src="https://github.com/Tufts-Technology-Services/tailscale-now/assets/17954/aa17782b-a000-4ac2-8f9f-ba12819fcccf" width="100" />
  <img src="https://github.com/Tufts-Technology-Services/tailscale-now/assets/17954/261036db-8bb5-4f10-9451-57d987917de7" width="100" />
  <img src="https://github.com/Tufts-Technology-Services/tailscale-now/assets/17954/1d451bea-f95d-4762-bd07-46658bb1f57f" width="100" />
</div>

# Making tailscale a first class citizen at Tufts

The purpose of this document is to answer questions to help make [Tailscale](https://tailscale.com/) a first class citizen within the list of components and tools we use at Tufts. We also want to use this repository as a location to introduce Tailscale to other teams to hopefully help them improve their connectivity so they can focus on delivering value faster.

### What is Tailscale?

There are many definitions out there about tailscale and most of them try to place it in the VPN type of products. Tailscale is an overlay network (a network on top of the physical network) that increases connectivity by removing some of the burdens introduced over the years in the networking stack, most of them in the name of security. You can also think about Tailscale as the “control plane” for [wireguard](https://www.wireguard.com/) connections (the “data plane”). If you want to see what it is in more detail and how it works, I suggest you read [this document](https://tailscale.com/blog/how-tailscale-works). 

### How do we use it?

Tailscale is a very important component in our group (Data strategy team). Most of our communications happen on top of a tailnet (Tailscale’s network). Here are a list of projects where we use tailscale. 

All the [Denodo](https://www.denodo.com/en) servers are part of our Tailnet. Because of that we have been able to access those servers since day one independently of the underlying change so the physical network.

Our github runners use Tailscale to temporarily join our Tailnet and get the necessary access to do their job. As an example, we can update our prometheus server by pushing commits to our [observability stack project](https://github.com/TuftsUniversity/dscicd).

We can give access to our Tailscale users to our grafana dashboards (and other resources) without having to request another level of authentication. You have already authenticated to the network (the tailnet) so you don’t have to authenticate again when accessing, for example, a grafana dashboard. We can get your identity from the network. 

Our dental users experienced some delays when using the software that runs in all the dental locations. We deployed a group of devices to collect telemetry over time to help us understand and quantify the issues. We shipped those machines to the different locations. After booting, all the machines join our Tailnet and start collecting metrics and sending them to our prometheus server.

### Now what?

What can we do to make help Tailscale a first class component at Tufts? Do you think your Team may benefit from Tailscale? Great, please, open an [issue](XXXX) so we can have a discussion to address all the questions you may have. 

Thank you for reading.
