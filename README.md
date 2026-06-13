# 🏦 Mise en place d’un SOC et Supervision d’une Infrastructure Bancaire
> **Projet de Groupe | ECE Paris | Bachelor 3 Cybersécurité & Réseaux**

## 📝 Présentation du Projet
Ce projet, réalisé en équipe, avait pour objectif de simuler l'infrastructure critique d'un établissement bancaire et d'y déployer un **SOC (Security Operations Center)** complet. Nous avons collaboré pour concevoir une architecture capable de garantir la disponibilité des services, la confidentialité des données et une détection ultra-rapide des menaces.

## 👥 Dynamique de Groupe & Collaboration
*   **Répartition des tâches** : Configuration des agents sur les endpoints (Windows/Linux), déploiement du serveur maître SOC (AlmaLinux) et design des dashboards de visualisation.
*   **Gestion des incidents en équipe** : Analyse collective des logs pour diagnostiquer les pannes de communication entre Zabbix et Grafana.
*   **Outils collaboratifs** : Utilisation de Git pour le versioning des configurations et de la documentation technique.

## 🏗️ Architecture du Système (5 VM Interconnectées)
Chaque membre de l'équipe a participé à la sécurisation d'un segment spécifique :
*   **VM1-Client** : Poste Windows simulant un employé de banque.
*   **VM2-Alma** : Serveur central hébergeant Wazuh, Zabbix et Grafana.
*   **VM3-DB-Server** : Serveur MySQL critique (transactions clients).
*   **VM4-Web-Server** : Serveur Apache hébergeant l'application bancaire.
*   **VM5-Ubuntu-Client** : Poste d'administration utilisé pour les tests de sécurité.

## 🛠️ Stack Technologique (Open Source Industriel)
*   **Wazuh (SIEM/HIDS)** : Analyse des journaux système et détection d'activités suspectes.
*   **Zabbix** : Supervision proactive de la santé du matériel (CPU, RAM, ports réseau).
*   **Grafana** : Centralisation et corrélation visuelle des alertes de sécurité.

## 🛡️ Scénarios de Sécurité Validés en Équipe
Pour certifier notre installation, nous avons mené des tests de pénétration simulés :
1.  **Attaque Brute Force SSH** : Détection automatique des tentatives d'échec de connexion répétées par Wazuh.
2.  **File Integrity Monitoring (FIM)** : Surveillance du fichier `/etc/` et alerte instantanée lors de la création d'un fichier suspect (`hack_banque.txt`).
3.  **Analyse de flux Web** : Détection de requêtes HTTP malveillantes sur le serveur bancaire Apache.

## 🚀 Résolution de Problématiques Techniques
Le travail d'équipe a été déterminant pour résoudre les défis suivants :
*   **Conflits d'agents** : Gestion des doublons d'identifiants Wazuh sur les machines clonées.
*   **Diagnostic API** : Utilisation de la commande `zabbix_get` pour identifier et corriger les erreurs de configuration entre Zabbix et l'interface Grafana.

---
[📄 Consulter le Rapport Pédagogique Complet (PDF)](./Docs2/Rapport pédagogique du projet.pdf)
