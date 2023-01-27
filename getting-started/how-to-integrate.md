---
description: Integrate Valyr today with one line of code
---

# How to integrate

{% tabs %}
{% tab title="Curl" %}
Replace the OpenAI base url

```url
POST https://api.openai.com/v1
```

with Valyr's

```
POST https://oai.valyrai.com/v1
```
{% endtab %}

{% tab title="Python" %}
Change the default base API url to Valyr's



```python
import openai

openai.api_base = "https://oai.valyrai.com/v1"
```
{% endtab %}

{% tab title="Node.js" %}
Add a `basePath` to the `Configuration:`



Before:

```typescript
import { Configuration, OpenAIApi } from "openai";

const configuration = new Configuration({
  apiKey: process.env.OPENAI_API_KEY
});

const openai = new OpenAIApi(configuration);
```



After:

```typescript
import { Configuration, OpenAIApi } from "openai";

const configuration = new Configuration({
  apiKey: process.env.OPENAI_API_KEY,
  basePath: "https://oai.valyrai.com/v1",
});

const openai = new OpenAIApi(configuration);
```
{% endtab %}
{% endtabs %}
