---
description: Open-source Observability Platform for GPT-3 Users
---

# Valyr

<figure><img src=".gitbook/assets/Screen Shot 2023-01-26 at 11.49.53 AM.png" alt=""><figcaption></figcaption></figure>

### What is Valyr

#### Valyr tracks the usage, latency, and cost of your GPT-3 requests

* **Easy to integrate**, requiring only **one line of code** to be added.
* Provides a **user-friendly dashboard** for **analyzing logs and metrics**.
* Segments your metrics by **prompts** and by **users.**

### How Valyr works

Valyr is a proxy server for executing OpenAI completions queries on your behalf, logging useful stats about your request such as the latency, result, and cost to a database.&#x20;

Our workers are secured by Cloudflare to ensure you are getting the best latency on your requests, wherever you are in the world. On average, our proxy adds 30ms to the total roundtrip time, which is normally less than 1% of the OpenAI query time.

You may use our hosted solution as the proxy or self-host workers in your own environment for free!



