# Venice AI 🐍

Welcome to the Venice AI repository! This Python client allows you to integrate advanced Generative AI capabilities into your applications. Whether you need chat, image generation, audio text-to-speech, or embeddings, Venice AI has you covered. 

[![Releases](https://img.shields.io/github/v/release/lelyanalkhamaiseh/venice-ai)](https://github.com/lelyanalkhamaiseh/venice-ai/releases)

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Getting Started](#getting-started)
- [Usage](#usage)
  - [Synchronous vs Asynchronous](#synchronous-vs-asynchronous)
  - [Error Handling](#error-handling)
- [Examples](#examples)
  - [Chat](#chat)
  - [Image Generation](#image-generation)
  - [Text-to-Speech](#text-to-speech)
- [Contributing](#contributing)
- [License](#license)
- [Support](#support)

## Features

Venice AI provides a range of features to enhance your applications:

- **Chat** 💬: Engage users with intelligent conversations.
- **Image Generation** 🖼️: Create stunning visuals from text prompts.
- **Text-to-Speech** 🔊: Convert text into natural-sounding audio.
- **Embeddings**: Generate meaningful representations of text.
- **Synchronous and Asynchronous Support**: Choose the method that suits your needs.
- **Streaming**: Handle real-time data efficiently.
- **Robust Error Handling**: Manage errors gracefully.

## Installation

To get started with Venice AI, install the package via pip:

```bash
pip install venice-ai
```

Make sure you have Python 3.6 or higher installed. If you encounter issues, refer to the [Releases](https://github.com/lelyanalkhamaiseh/venice-ai/releases) section for the latest version and updates.

## Getting Started

After installation, you can start using Venice AI in your Python projects. Import the library and initialize it with your API key.

```python
import venice_ai

client = venice_ai.Client(api_key='YOUR_API_KEY')
```

Replace `'YOUR_API_KEY'` with your actual API key. 

## Usage

### Synchronous vs Asynchronous

Venice AI supports both synchronous and asynchronous calls. You can choose the method that best fits your application's architecture.

#### Synchronous Example

```python
response = client.chat("Hello, how are you?")
print(response)
```

#### Asynchronous Example

For asynchronous usage, ensure you have an event loop running.

```python
import asyncio

async def main():
    response = await client.chat_async("Hello, how are you?")
    print(response)

asyncio.run(main())
```

### Error Handling

Venice AI has built-in error handling. If an error occurs, the client raises exceptions that you can catch and handle.

```python
try:
    response = client.chat("What is the weather today?")
except venice_ai.Error as e:
    print(f"An error occurred: {e}")
```

## Examples

### Chat

The chat feature allows you to create conversational agents.

```python
response = client.chat("Tell me a joke.")
print(response)
```

### Image Generation

Generate images based on textual descriptions.

```python
image = client.generate_image("A futuristic city skyline at sunset.")
image.show()
```

### Text-to-Speech

Convert text to audio with ease.

```python
audio = client.text_to_speech("Hello, welcome to Venice AI.")
audio.play()
```

## Contributing

We welcome contributions to Venice AI. If you have ideas for improvements or new features, please fork the repository and submit a pull request. 

1. Fork the repository.
2. Create a new branch for your feature.
3. Make your changes.
4. Submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Support

For questions or issues, please open an issue in the repository or check the [Releases](https://github.com/lelyanalkhamaiseh/venice-ai/releases) section for updates.

Thank you for using Venice AI! We look forward to seeing what you build with it.