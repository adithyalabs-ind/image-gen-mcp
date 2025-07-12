# Image Generation MCP Server for Text-to-Image Services

![GitHub release](https://img.shields.io/github/release/adithyalabs-ind/image-gen-mcp.svg) ![License](https://img.shields.io/badge/license-MIT-blue.svg)

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [API Reference](#api-reference)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Overview

This repository contains an MCP server that integrates with the **gpt-image-1** and **Gemini imagen4** models. It provides text-to-image generation services, allowing users to create images from textual descriptions. 

For the latest updates and downloads, visit our [Releases](https://github.com/adithyalabs-ind/image-gen-mcp/releases).

## Features

- **Text-to-Image Generation**: Generate high-quality images based on textual input.
- **Integration with Advanced Models**: Utilizes gpt-image-1 and Gemini imagen4 for enhanced image generation.
- **MCP Server**: A robust server architecture that supports multiple requests and high availability.
- **Easy to Use API**: Simple endpoints for seamless integration into applications.
- **Extensible Architecture**: Easily add new models or features in the future.

## Installation

To set up the server, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/adithyalabs-ind/image-gen-mcp.git
   cd image-gen-mcp
   ```

2. **Install Dependencies**:
   Use the following command to install required libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. **Download and Execute the Server**:
   You can find the latest release [here](https://github.com/adithyalabs-ind/image-gen-mcp/releases). Download the appropriate file and execute it.

## Usage

Once the server is running, you can use the API to generate images. Here’s a basic example:

### Start the Server

Run the following command to start the server:
```bash
python server.py
```

### API Endpoints

#### Generate Image

**Endpoint**: `POST /generate`

**Request Body**:
```json
{
  "text": "A serene landscape with mountains and a river"
}
```

**Response**:
```json
{
  "image_url": "http://example.com/generated_image.png"
}
```

### Example Request Using cURL

```bash
curl -X POST http://localhost:5000/generate \
-H "Content-Type: application/json" \
-d '{"text": "A serene landscape with mountains and a river"}'
```

## API Reference

### `/generate`

- **Method**: `POST`
- **Description**: Generates an image based on the provided text.
- **Request Body**:
  - `text`: A string containing the description of the image.
- **Response**:
  - `image_url`: URL of the generated image.

### `/status`

- **Method**: `GET`
- **Description**: Checks the status of the server.
- **Response**:
  - `status`: Indicates if the server is running.

## Contributing

We welcome contributions to improve the project. To contribute:

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Submit a pull request.

Please ensure that your code adheres to the existing style and includes tests where applicable.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For questions or support, please reach out to the project maintainers.

For the latest updates and downloads, visit our [Releases](https://github.com/adithyalabs-ind/image-gen-mcp/releases).

![Image Generation](https://example.com/image-generation.png) 

---

### Note

This README provides an overview of the image generation MCP server. For more detailed documentation, please refer to the Wiki section of the repository.