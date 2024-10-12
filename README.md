# Self-GPT: Combines Open WebUI + Ollama to give you a self hosted and open source equivalent of ChatGPT

This installation method uses a single container image that bundles [Open WebUI](https://github.com/open-webui/open-webui) (chat interface front end) with [Ollama](https://github.com/ollama/ollama) (LLM backend), allowing for a streamlined setup via a single command. Choose the appropriate command based on your hardware setup:

**With GPU Support**: Utilize GPU resources by running the following command:

    docker run -d -p 3000:8080 --gpus=all -v ollama:/root/.ollama -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:ollama

**For CPU Only**: If you're not using a GPU, use this command instead:

    docker run -d -p 3000:8080 -v ollama:/root/.ollama -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:ollama

Both commands facilitate a built-in, hassle-free installation of both Open WebUI and Ollama, ensuring that you can get everything up and running swiftly.

After installation, you can access Open WebUI at http://localhost:3000. Enjoy! 😄
