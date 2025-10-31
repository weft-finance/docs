### Development Setup

#### Installation

Install Mintlify globally:

```bash
npm i -g mintlify
```

#### Running the Development Server

Run the following command at the root of your documentation (where `docs.json` is located):

```bash
mintlify dev
```

Mintlify uses port 3000 by default. You can customize the port using the `--port` flag:

```bash
mintlify dev --port 8080
```

#### Generating API Reference from OpenAPI

To generate endpoint definitions from your OpenAPI YAML file:

```bash
npx @mintlify/scraping@latest openapi-file ./config/vy-openapi.yml -o api-reference/endpoints
```

**Important:** After running this command, you need to manually update your documentation structure:

1. Open `docs.json`
2. Add the generated endpoint files to the `navigation` section under the appropriate group
3. Example structure:

```json
{
  "navigation": [
    {
      "group": "API Reference",
      "pages": [
        "api-reference/endpoints/endpoint-1",
        "api-reference/endpoints/endpoint-2"
      ]
    }
  ]
}
```

This will make your API endpoints visible in the documentation sidebar.
