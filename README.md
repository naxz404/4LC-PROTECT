Le bot Gestion de 4LC
# 🛡️ 4LC PROTECT — Bot Discord de Sécurité & Modération

**4LC PROTECT** est un bot Discord complet écrit en Node.js, spécialement conçu pour protéger votre serveur contre les raids, sécuriser l'accès des nouveaux membres via un système de Captcha, et offrir des outils puissants de modération, de gestion de tickets et de logs en temps réel.

---

## 🚀 Fonctionnalités Principales

### 🔒 Anti-Raid & Protection Serveur (`ProtectCore` / `ProtectModules`)
- **Anti-Bot :** Empêche l'ajout de bots non autorisés.
- **Anti-Spam & Anti-MassMention :** Bloque le spam agressif et les mentions de masse.
- **Anti-Link :** Détection et suppression automatique des liens suspects ou non autorisés.
- **Anti-Nuke / Anti-Channel-Delete :** Protection contre la destruction massive de salons, rôles ou paramètres.
- **Captcha System :** Vérification interactive des nouveaux membres à leur arrivée pour filtrer les comptes automatisés.

### 🛠️ Modération (`Commands/Moderation`)
- Outils classiques et avancés : `ban`, `kick`, `mute`/`timeout`, `warn`, `clear`/`purge`.
- Système d'avertissements (warns) sauvegardé en base de données.

### 🎟️ Gestion des Tickets (`Commands/Tickets`)
- Création de tickets via boutons/menus déroulants.
- Salons temporaires dédiés au support utilisateur avec système de fermeture et de sauvegarde.

### 📊 Logs Détaillés (`ProtectCore/Logs`)
- Journalisation complète des événements du serveur : arrivées/départs, suppressions/modifications de messages, sanctions administratives, modifications de rôles et de salons.

---

## 📁 Structure du Projet

```text
.
├── Commands/           Commandes du bot (Moderation, Admin, Utility, Tickets)
├── Events/             Événements Discord.js (ready, messageCreate, guildMemberAdd...)
├── ProtectCore/        Moteur principal de sécurité et gestion des logs
├── ProtectModules/     Modules de protection spécifiques (Anti-Raid, Captcha, Anti-Spam...)
├── Database/           Gestion du stockage des données (configuration, sanctions, etc.)
├── index.js            Point d'entrée principal de l'application
├── config.json         Fichier de configuration globale
└── package.json        Dépendances Node.js
```

---

## 🛠️ Prérequis

- [Node.js](https://nodejs.org/) (v16.x ou supérieure recommandée)
- Un bot Discord enregistré sur le [Discord Developer Portal](https://discord.com/developers/applications) avec les **Privileged Gateway Intents** activés :
  - `SERVER MEMBERS INTENT`
  - `MESSAGE CONTENT INTENT`
  - `PRESENCE INTENT` (si nécessaire)

---

## 📦 Installation

1. **Cloner le projet ou extraire l'archive :**
   ```bash
   git clone <https://github.com/naxz404/4LC-PROTECT>
   cd 4LC-PROTECT
   ```

2. **Installer les dépendances :**
   ```bash
   npm install
   ```

3. **Configuration :**
   Renommez ou éditez le fichier `config.json` (ou `.env` selon votre configuration) avec vos identifiants :
   ```json
   {
     "token": "VOTRE_TOKEN_DISCORD_ICI",
     "prefix": "!",
     "ownerID": "VOTRE_ID_DISCORD"
   }
   ```

4. **Lancer le bot :**
   ```bash
   npm start
   # ou avec node directement :
   node index.js
   ```

---

## ⚙️ Configuration de la Sécurité

Une fois le bot en ligne sur votre serveur :
1. Utilisez la commande d'administration (`!setup` ou `/setup` selon vos commandes) pour configurer les salons de logs.
2. Activez les modules souhaités (Anti-Raid, Anti-Link, Captcha) via le panneau de configuration du bot.
3. Assurez-vous que le rôle du bot est positionné **en haut de la liste des rôles** dans les paramètres de votre serveur Discord afin qu'il puisse modérer efficacement les membres et gérer les rôles.

---

## 📝 Licence & Contribution

Projet privé / développé pour la gestion et la sécurité des serveurs Discord.
