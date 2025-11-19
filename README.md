# epsi_i1_devia_integration_2526 


https://github.com/Gladrat

# Environnement

- Installer Powershell 7.5 : [https://github.com/PowerShell/PowerShell/releases/download/v7.5.4/PowerShell-7.5.4-win-x64.msi](https://github.com/PowerShell/PowerShell/releases/download/v7.5.4/PowerShell-7.5.4-win-x64.msi)
- Installer n8n : `npm install -g n8n`
  - Lancer n8n : `n8n`
- Installer Ollama
  - Fermer le client (desktop) Ollama
  - Pull un modèle : `ollama pull gemma3:4b`
  - Lancer le serveur d'API Ollama : `ollama serve`
  - Charger le modèle en mémoire : `curl "http://localhost:11434/api/generate" -d '{"model": "gemma3:4b", "keep_alive": -1}'`
  - Tester un prompt : `curl "http://localhost:11434/api/generate" -d '{"model": "gemma3:4b", "prompt": "Dis bonjour en 3 langues différentes", "stream": false}'`
  
Pour les galères de Powershell :

```ps
Invoke-RestMethod `
  -Uri "http://localhost:11434/api/generate" `
  -Method Post `
  -ContentType "application/json" `
  -Body '{"model": "gemma3:4b", "keep_alive": -1}'
```

# Projet n°1 : Veille automatisée

- Scraper (DEV+IA) : [https://tldr.tech/dev/2025-11-18](https://tldr.tech/dev/2025-11-18)
- Scraper (INFRA+CYBER) : [https://tldr.tech/infosec/2025-11-18](https://tldr.tech/infosec/2025-11-18)
- Vous devez récupérer :
  - Titre
  - Description
  - URL
  - (Durée)
- Synthèse de la description par IA
- Catégorisation de l'article par IA
- Chargement dans Notion