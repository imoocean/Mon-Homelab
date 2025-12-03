# 🏠 Mon Homelab & Automatisation IA

Ce dépôt documente mon infrastructure personnelle hébergée sur Raspberry Pi 4, sécurisée par Cloudflare Zero Trust, ainsi que mes workflows d'automatisation.

## 🏗️ Infrastructure

Mon infrastructure tourne sous Docker et comprend :
- **n8n** : Orchestration des automatisations.
- **Uptime Kuma** : Supervision des services et de la connexion internet.
- **Homepage** : Dashboard centralisé.
- **Cloudflared** : Tunnel sécurisé (Zero Trust) pour l'accès distant sans ouverture de ports.

## 🤖 Automatisations (n8n)

### Veille Technologique IA
Un workflow quotidien qui :
1. Agrège les flux RSS de plusieurs sources (IT-Connect, Korben,...).
2. Nettoie et trie les articles.
3. **Utilise une IA (Llama 3 / Moonshot via Groq)** pour générer un résumé synthétique.
4. Sauvegarde les liens dans **Notion** (Knowledge Base).
5. Envoie le résumé par **Email** tous les matins à 9h30.

## 🛠️ Installation

1. Cloner le repo :
   ```bash 
   git clone https://github.com/imoocean/Mon-Homelab.git https://github.com/imoocean/Mon-Homelab.git
   ```

2. Créer un fichier .env avec votre Token Cloudflare :
   ```bash 
   TUNNEL_TOKEN=votre_token_ici
   ```
3. Lancer la stack :
   ```bash 
   docker compose up -d

   ```

