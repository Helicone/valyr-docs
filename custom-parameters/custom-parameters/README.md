---
description: >-
  Custom parameters allow users to add extra metadata that is specific to their
  workflow which is common among LLM developers. Adding custom parameters help
  our users a bunch with
---

# Custom Parameters

### Possible parameters

`Valyr-Prompt-ID`: Unique identifier for this prompt. (ex: "wedding-cards-001")

`Valyr-Request-ID`: A user specified UUID for that request. (Must be a uuidv4)

`Valyr-User-ID`: Any string representation of your user. (ex: "fred@example.com")



### Adding a custom parameter to your query

{% tabs %}
{% tab title="Curl" %}
You can simply add those as headers like this

```
  -H 'Valyr-Prompt-ID: "wedding-cards-001"'
  -H 'Valyr-User-ID: "fred@example.com"'
```
{% endtab %}

{% tab title="Node.js" %}
In your OpenAI configuration, you can add an extra argument called `baseOptions` and include the custom parameter has a header.

```typescript
import { Configuration, OpenAIApi } from "openai";
const configuration = new Configuration({
  apiKey: process.env.OPENAI_API_KEY,
  basePath: "http://127.0.0.1:8787/v1",
  baseOptions: {
    headers: {
      "Valyr-Prompt-ID": "wedding-cards-001",
      "Valyr-User-ID": "fred@example.com",
    },
  },
});
const openai = new OpenAIApi(configuration);
```
{% endtab %}
{% endtabs %}
