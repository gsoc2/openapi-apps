# Postman to OpenAPI
As we run everything as OpenAPI in gsoc2, we needed a way to transform postman to OpenAPI. Here's how.


1. **Install Postman to OpenAPI**
```
npm i postman-to-openapi -g
```

Docs: https://joolfe.github.io/postman-to-openapi/

2. **Run p2o (postman-2-openapi)**
This example runs towards an Automox Postman Collection, translated to OpenAPI 
```
~/.npm-global/lib/node_modules/postman-to-openapi/bin/cli.js fluency.json -f fluency.yaml
```

PS: It may be located in a different location after install. Check the logs from the install.

3. **Upload it to Gsoc2**
Upload the new Yaml file to Gsoc2, then finish the configuration (e.g. add image, fix potential auth issues or naming issues).

4. Move it back to the OpenAPI location (this repository)
