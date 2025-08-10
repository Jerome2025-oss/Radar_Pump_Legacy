
## 🔧 Configuration avancée
| Paramètre | Localisation | Description |
|-----------|--------------|-------------|
| Fréquence | Dernière cellule | Modifiez `time.sleep(600)` |
| Limite tokens | Cellule `LIMIT` | Nombre max de cryptos à tracker |
| Filtre tokens | `tokens_perpetuels.txt` | Liste personnalisée (optionnel) |

## ❓ FAQ
**Q** : Ça marche si je ferme Colab ?  
**R** : Non, sauf avec Colab Pro (fonctionnalité background).

**Q** : Puis-je changer la devise ?  
**R** : Oui, modifiez `convert=USD` dans l'URL API.

## 📜 License
MIT - Libre d'utilisation et modification


# 🚀 Radar Pump Legacy - Crypto Performance Tracker

![Google Colab](https://colab.research.google.com/assets/colab-badge.svg) ![Python](https://img.shields.io/badge/python-3.8%2B-blue) ![License](https://img.shields.io/badge/license-MIT-green) ![API Limit](https://img.shields.io/badge/API_limit-10min%2Freq-red)

## ⚠️ Attention : Limitations de l'API
**Ne pas descendre en dessous de 10 minutes entre les requêtes**  
CoinMarketCap bloque les requêtes trop fréquentes :
- Limite standard : 10-30 appels/min (selon votre plan)
- Ce script est configuré pour **1 requête/10min** (safe)
- Modification risquée : changer `time.sleep(600)` pourrait faire bannir votre clé API

## 📌 Description
Outil automatisé qui :
- Récupère les données crypto via l'API CoinMarketCap
- Stocke l'historique en format Parquet
- Génère un rapport Excel des meilleures performances
- Tourne automatiquement toutes les 10 minutes (config sécurisée)

## 🛠 Prérequis
- Compte Google (Colab + Drive)
- Clé API CoinMarketCap ([obtenez-la ici](https://pro.coinmarketcap.com/signup))
- **Plan gratuit** : Jusqu'à 10k req/mois (suffisant pour ce script)

## 🚀 Comment lancer
1. **Ouvrez dans Colab** :  
   [![Ouvrir dans Colab](https://colab.research.google.com/assets/colab-badge.svg)](lien_vers_votre_nb)

2. **Exécution** :
   ```bash
   Runtime > Run all  # Ou cellule par cellule avec ▶
