### Development

```
npm i -g mintlify
```

Run the following command at the root of your documentation (where mint.json is)

Mintlify uses port 3000 by default. 
You can use the `--port` flag to customize the port Mintlify runs on. For example,
use this command to run in port 8080:

```bash
mintlify dev --port 8080
```

To generate the endpoint definitions from your OpenAPI YAML file- 
npx @mintlify/scraping@latest openapi-file ./config/vy-openapi.yml -o api-reference/endpoints


