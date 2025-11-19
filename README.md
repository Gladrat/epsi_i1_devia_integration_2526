# epsi_i1_devia_integration_2526 


https://github.com/Gladrat

# Environnement

- Installer n8n : `npm install -g n8n`
  - Lancer n8n : `n8n`
- Installer Ollama
  - Fermer le client (desktop) Ollama
  - Pull un modèle : `ollama pull gemma3:4b`
  - Lancer le serveur d'API Ollama : `ollama serve`
  - Charger le modèle en mémoire : `curl "http://localhost:11434/api/generate" -d '{"model": "gemma3:4b", "keep_alive": -1}'`
  - Tester un prompt : `curl "http://localhost:11434/api/generate" -d '{"model": "gemma3:4b", "prompt": "Dis bonjour en 3 langues différentes", "stream": false}'`