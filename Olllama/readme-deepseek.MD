docker run -d -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama
docker exec -it ollama /bin/bash
ollama pull deepseek-r1:8b
ollama run deepseek-r1:8b

docker run -d -p 3000:8080 -e OLLAMA_BASE_URL=http://<YOUR-IP>:11434 -v
open-webui:/app/backend/data --name open-webui --restart always
ghcr.io/open-webui/open-webui:main