---
layout: post
title:  "The ELK stack"
subtitle: "Elasticsearch + Logstash + kibana = awesomeness."
date: 2015-11-05 01:00:00
categories: [tech]
---


We want to capture a lot of event based data, and analyis it quickly. We wanted a way to captuer 100s of MB of event / log data and expose it to other teams in a way that it is easy to search, aggregate and create graphs to get insights from the data.

We explored some options and finally narrowed down to the ELK stack, put together by folks who created [elasticsearch](https://www.elastic.co/). We had some experience with Elasticsearch before and the powerfull UI provided by kibanan was exactly what we needed.

We followed [this](https://www.digitalocean.com/community/tutorials/how-to-install-elasticsearch-logstash-and-kibana-elk-stack-on-ubuntu-14-04) guide by digital ocean and set up the stack on an m1.medium ec2 instance with 10 gigs of harddisk space.

To start with we configured logstash to capture all nginx access logs. Then, we were generating close to 200 MB of nginx access logs every day . We configured geoip to get region details, also we split up user agent details and indexed it separately. We deployed the stack and we started seeing data.

But within a day we ran out of disk space, then we bumped up the disk space to 50 gigs and deployed the stack again. Within a week the stack was already using 34 gigs of diskspace, something looked out of place, we would have sent only 1 GB of logs by now. At this rate the stack would not be very usefull to us.

Another few days passed and to our surprize the stack still used around 34 gigs, the stack stablized around that and is now linearly increasing with the data we send. Looks like its the elasticsearch indexes that is taking up so much space, and we had configured it to index everything. With time elasticsearch probably had created indexes for all possible variations around the data and indexes where not growing as fast as they did in the begining. Alos the responsiveness of kibana UI imporved a lot after the initial spell, and is working flawlessly now.

Now we are looking forward to send more data to the stack and generated insights to help us make better products.
