# 📄 V2C Thirdparty API Documentation

This repository contains the OpenAPI specification for the V2C Thirdparty API, along with the necessary instructions to generate interactive documentation in HTML format.

## 🚀 Quick Start

### Prerequisites

You must have **Node.js** and **npm** (or Yarn/pnpm) installed on your system.

Additionally, you need the Redocly CLI client, which can be installed globally (or locally in the project):

```bash
npm install -g @redocly/cli
# Alternatively, for a local installation:
# npm install @redocly/cli
```

-----

## 🛠️ Project Structure

The core of your documentation is the OpenAPI specification file:

| File | Description |
| :--- | :--- |
| **`openapi.yaml`** | Contains the complete **RESTful definition of the API** (endpoints, parameters, schemas, security, etc.). All API modifications must be made within this file. |
| `index.html` | The HTML output file. This is the final generated documentation, ready to be viewed in a web browser. |

-----

## 👁️ How to View the Documentation

Once generated, the documentation is contained within the **`index.html`** file.

Simply open this file in any web browser to access the interactive, user-friendly API documentation.

-----

## 📝 How to Update the Documentation

To ensure that changes made in the **`openapi.yaml`** file are reflected in the final HTML documentation, you must run the Redocly CLI build command.

1.  **Modify:** Make all necessary adjustments (corrections, additions, or deletions) in the **`openapi.yaml`** file.
2.  **Generate:** Execute the following command to generate the new `index.html` file:

<!-- end list -->

```bash
npx @redocly/cli build-docs openapi.yaml -t template.hbs -o index.html
```

This command will read the updated specification, apply the documentation theme, and overwrite the **`index.html`** file with the latest version.

Search API docs by redoc and delete all div, replace redoc.standalone.js by redoc.js