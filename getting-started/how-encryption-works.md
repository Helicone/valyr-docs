---
description: We take the security of your OpenAI requests extremely seriously
---

# How encryption works

### What happens to your OpenAI key

When you call a completions request with Valyr's cloud hosted proxy, we get your OpenAI key to execute the query on your behalf. We also hash your key using the cryptographically secure SHA-256 hash function and log the hash with your response.

****:bulb:**Your OpenAI key is never stored on our servers.**

The first time you login to Valyr's web application, you will enter your OpenAI key. We hash it in your client using the same hash function above and persist only the hash in our server.&#x20;

This allows the web application to match your completion requests with your account, even though we never know what your key is.

#### :bulb:The hash function is irreversible and it is not possible to infer your OpenAI Key from the hash of your keys.

### Don't believe us? Check out our open-source code

Valyr is an evolving [open source project ](https://github.com/Helicone/valyr)that is committed to earning the trust of developers. By making our code publicly available, we provide transparency and allow developers to confirm best security practices for themselves and suggest improvements where possible.





