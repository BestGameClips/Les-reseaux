# 🌐 Réseau & Cybersécurité — Fiche de cours

![Réseau & Cybersécurité](https://img.shields.io/badge/Domaine-Réseau%20%26%20Cybersécurité-blue)
![Format](https://img.shields.io/badge/Format-Cours%20%2B%20Fiche%20Mémo-green)
![Niveau](https://img.shields.io/badge/Niveau-Débutant%20%2F%20Intermédiaire-orange)

Bienvenue sur ce repository consacré aux **bases du réseau informatique et de la cybersécurité**.

Ce projet rassemble les notions essentielles permettant de comprendre comment les machines communiquent, comment les réseaux sont organisés et comment ils peuvent être protégés.

---

## 📚 Contenu

Le cours couvre notamment :

* 🌐 Bases du réseau
* 🧱 Modèle OSI
* 🔄 Modèle TCP/IP
* 🌍 Adressage IPv4 / IPv6
* 🔢 CIDR
* ✂️ Subnetting
* 📐 VLSM
* 🚚 TCP / UDP
* 📡 ICMP
* 🔗 ARP
* 🌍 DNS
* 📦 DHCP
* 🔒 HTTP / HTTPS
* 🔌 Switch
* 🛣️ Routeur
* 🛡️ Pare-feu
* 🚨 IDS / IPS
* 🔀 Proxy / Reverse Proxy
* 📡 Wi-Fi
* 📦 Encapsulation
* 🛣️ Routage
* 🔄 NAT
* 🧩 VLAN
* 🛡️ DMZ
* 📋 ACL
* 🔐 VPN
* 🧠 Zero Trust
* ⚠️ Attaques réseau
* 🧰 Outils réseau
* ☁️ Réseau Cloud
* 🖥️ Virtualisation

---

# 📖 Sommaire

* [Introduction](#-introduction)
* [Objectifs](#-objectifs)
* [Notions fondamentales](#-notions-fondamentales)
* [Modèle OSI](#-modèle-osi)
* [TCP/IP](#-tcpip)
* [Adressage IP](#-adressage-ip)
* [Protocoles](#-protocoles)
* [Équipements réseau](#-équipements-réseau)
* [Sécurité réseau](#-sécurité-réseau)
* [Attaques](#-attaques-réseau)
* [Outils](#-outils-réseau)
* [Environnements réels](#-environnements-réseau)
* [Fiche mémo](#-fiche-mémo)
* [Avertissement](#️-avertissement)
* [Sources et crédits](#-sources-et-crédits)

---

# 📌 Introduction

Un réseau informatique est un ensemble de machines reliées entre elles afin de communiquer et d'échanger des données.

Les réseaux sont présents partout :

* Entreprises
* Administrations
* Maisons
* Datacenters
* Cloud
* Objets connectés
* Internet

En cybersécurité, le réseau est particulièrement important puisqu'il constitue un moyen majeur de transport des données et une surface d'attaque importante.

---

# 🎯 Objectifs

Ce repository a pour objectif de permettre de comprendre :

* Comment fonctionne un réseau
* Comment les machines communiquent
* Comment les adresses IP sont organisées
* Comment les paquets circulent
* Comment fonctionnent les principaux protocoles
* À quoi servent les équipements réseau
* Comment segmenter et sécuriser un réseau
* Quelles sont les principales attaques réseau
* Quels outils utiliser pour diagnostiquer un problème réseau

---

# 🌐 Notions fondamentales

## LAN

**Local Area Network**

Réseau local utilisé dans une maison, une entreprise ou une infrastructure locale.

## WAN

**Wide Area Network**

Réseau étendu permettant de relier plusieurs réseaux locaux.

Internet est un exemple de WAN.

## Bande passante

Capacité maximale de transmission d'un réseau.

## Débit

Quantité réelle de données transmises par seconde.

## Latence

Temps nécessaire à une donnée pour aller d'un point à un autre.

---

# 🧱 Modèle OSI

Le modèle OSI comporte sept couches.

| Couche | Nom          | Fonction                            |
| -----: | ------------ | ----------------------------------- |
|      7 | Application  | Services réseau                     |
|      6 | Présentation | Formatage, chiffrement, compression |
|      5 | Session      | Gestion des sessions                |
|      4 | Transport    | TCP, UDP, ports                     |
|      3 | Réseau       | IP et routage                       |
|      2 | Liaison      | MAC et trames                       |
|      1 | Physique     | Transmission des signaux            |

### Mémo

```text
7 Application
6 Présentation
5 Session
4 Transport
3 Réseau
2 Liaison
1 Physique
```

---

# 🔄 TCP/IP

Le modèle TCP/IP possède quatre couches :

```text
Application
Transport
Internet
Accès réseau
```

Correspondance :

```text
OSI 7/6/5 → Application
OSI 4     → Transport
OSI 3     → Internet
OSI 2/1   → Accès réseau
```

---

# 🌍 Adressage IP

## IPv4

Une adresse IPv4 possède 32 bits.

Exemple :

```text
192.168.1.1
```

## Adresses privées

```text
10.0.0.0/8
172.16.0.0/12
192.168.0.0/16
```

## Loopback

```text
127.0.0.1
```

## APIPA

```text
169.254.0.0/16
```

---

# 🔢 CIDR

Le CIDR permet de représenter la taille de la partie réseau avec `/x`.

Exemple :

```text
192.168.1.0/24
```

Le CIDR permet notamment de réduire le gaspillage d'adresses et de simplifier le routage.

---

# ✂️ Subnetting

Le subnetting consiste à diviser un réseau en plusieurs sous-réseaux.

Objectifs :

* Sécurité
* Organisation
* Réduction des broadcasts
* Amélioration des performances

Exemple :

```text
192.168.1.0/24
        ↓
       /26
        ↓
4 sous-réseaux
62 hôtes utilisables par sous-réseau
```

---

# 🚚 Protocoles

## TCP

TCP est orienté connexion et privilégie la fiabilité.

Caractéristiques :

* ACK
* Retransmission
* Numéros de séquence
* Contrôle de flux
* Contrôle de congestion

### Three-Way Handshake

```text
SYN
 ↓
SYN-ACK
 ↓
ACK
 ↓
Connexion établie
```

---

## UDP

UDP est sans connexion et privilégie la rapidité.

Utilisations :

* DNS
* Streaming
* VoIP
* Jeux en ligne

### Mémo

```text
TCP = fiabilité
UDP = rapidité
```

---

## ICMP

Utilisé pour le diagnostic et les messages d'erreur.

Exemple :

```text
ping
```

---

## ARP

Permet de faire la correspondance :

```text
IP → MAC
```

---

## DNS

Traduit les noms de domaine en adresses IP.

Exemple :

```text
example.com
     ↓
adresse IP
```

Principaux enregistrements :

* A
* AAAA
* MX
* CNAME
* NS
* TXT

---

## DHCP

Attribue automatiquement la configuration réseau.

### DORA

```text
Discover
Offer
Request
Acknowledge
```

---

## HTTP / HTTPS

### HTTP

Port :

```text
80
```

Les données ne sont pas chiffrées.

### HTTPS

Port :

```text
443
```

Utilise TLS afin d'apporter confidentialité, intégrité et authentification.

---

# 🔌 Équipements réseau

## Switch

* Couche OSI 2
* Utilise les adresses MAC
* Connecte les équipements d'un LAN

## Routeur

* Couche OSI 3
* Utilise les adresses IP
* Interconnecte plusieurs réseaux
* Possède une table de routage

## Pare-feu

Contrôle le trafic réseau selon des règles.

## IDS

Détecte les activités suspectes et génère des alertes.

## IPS

Détecte et bloque automatiquement les activités malveillantes.

## Proxy

Intermédiaire entre client et serveur.

## Access Point

Permet aux appareils Wi-Fi d'accéder au réseau.

---

# 🔐 Sécurité réseau

## VLAN

Permet de segmenter logiquement un réseau.

Exemple :

```text
VLAN 10 → Administration
VLAN 20 → Comptabilité
VLAN 30 → Invités
```

Norme :

```text
IEEE 802.1Q
```

---

## DMZ

Zone intermédiaire entre Internet et le réseau interne.

Exemple :

```text
Internet
   ↓
Pare-feu
   ↓
DMZ
   ↓
Pare-feu
   ↓
Réseau interne
```

Les services exposés publiquement peuvent être placés dans la DMZ.

---

## ACL

Une ACL définit des règles de filtrage.

Une règle peut utiliser :

* IP source
* IP destination
* Port
* Protocole
* Action

Actions possibles :

```text
permit
deny
```

---

## VPN

Crée un tunnel chiffré entre deux points.

Protocoles présentés dans le cours :

* IPsec
* OpenVPN
* WireGuard

---

## Zero Trust

Principe :

> **Aucune confiance implicite.**

Principes :

* Vérification continue
* Moindre privilège
* Micro-segmentation
* Surveillance permanente

Technologies associées :

* MFA
* IAM
* Contrôle d'accès
* Analyse en temps réel

---

# ⚠️ Attaques réseau

## Sniffing

Interception et analyse du trafic réseau.

Risques :

* Vol d'identifiants
* Vol de cookies
* Collecte d'informations

---

## MITM

**Man In The Middle**

L'attaquant s'interpose entre deux parties.

```text
Victime
   ↕
Attaquant
   ↕
Serveur
```

---

## ARP Spoofing

Falsification des informations ARP afin de détourner le trafic.

---

## DNS Spoofing

Falsification d'une réponse DNS afin de rediriger une victime.

---

## DDoS

**Distributed Denial of Service**

Objectif :

> Rendre un service indisponible en saturant ses ressources.

---

## Scan réseau

Permet d'identifier :

* Hôtes
* Ports
* Services
* Versions
* Systèmes

---

# 🧰 Outils réseau

| Outil        | Utilité                                   |
| ------------ | ----------------------------------------- |
| `ping`       | Tester la connectivité                    |
| `traceroute` | Analyser le chemin réseau                 |
| `netstat`    | Afficher connexions et ports              |
| `ss`         | Afficher les connexions réseau            |
| `nmap`       | Scanner et cartographier un réseau        |
| Wireshark    | Capturer et analyser les paquets          |
| tcpdump      | Capturer les paquets en ligne de commande |

---

# 📦 Encapsulation

Le parcours général des données :

```text
Données
   ↓
Segment
   ↓
Paquet
   ↓
Trame
   ↓
Bits
```

À l'arrivée :

```text
Bits
 ↓
Trame
 ↓
Paquet
 ↓
Segment
 ↓
Données
```

C'est la **désencapsulation**.

---

# 🛣️ Routage

Le routage détermine le chemin utilisé par les paquets IP.

### Statique

Configuration manuelle.

### Dynamique

Protocoles permettant l'échange automatique d'informations de routage.

Exemples étudiés :

* OSPF
* BGP

---

# 🔄 NAT

**Network Address Translation**

Permet notamment à plusieurs machines utilisant des adresses privées de communiquer avec Internet.

Types :

* SNAT
* DNAT
* PAT

---

# ☁️ Réseau Cloud

## VPC / VNet

Réseau privé virtuel isolé dans un environnement cloud.

* AWS → VPC
* Azure → VNet

## Security Groups

Pare-feu virtuels appliqués aux instances.

## Load Balancer

Répartit les connexions entre plusieurs serveurs.

Objectifs :

* Performance
* Disponibilité
* Haute disponibilité

---

# 🖥️ Virtualisation

Un hyperviseur permet d'exécuter plusieurs machines virtuelles sur un serveur physique.

Exemples :

* VMware ESXi
* Microsoft Hyper-V
* KVM

Un switch virtuel permet aux machines virtuelles de communiquer entre elles et avec le réseau physique.

---

# 🧠 Fiche mémo express

| Concept   | À retenir                 |
| --------- | ------------------------- |
| LAN       | Réseau local              |
| WAN       | Réseau étendu             |
| OSI       | 7 couches                 |
| TCP/IP    | 4 couches                 |
| TCP       | Fiabilité                 |
| UDP       | Rapidité                  |
| IP        | Adressage/routage         |
| ARP       | IP → MAC                  |
| DNS       | Nom → IP                  |
| DHCP      | Configuration automatique |
| ICMP      | Diagnostic                |
| HTTP      | Port 80                   |
| HTTPS     | Port 443 + TLS            |
| Switch    | MAC / couche 2            |
| Routeur   | IP / couche 3             |
| IDS       | Détection                 |
| IPS       | Détection + blocage       |
| VLAN      | Segmentation              |
| DMZ       | Zone intermédiaire        |
| VPN       | Tunnel chiffré            |
| NAT       | Traduction d'adresses     |
| Nmap      | Scan réseau               |
| Wireshark | Analyse de paquets        |
| tcpdump   | Capture réseau CLI        |

---

# 🛡️ Bonnes pratiques

* Utiliser HTTPS/TLS
* Utiliser des mots de passe forts
* Activer MFA lorsque possible
* Mettre à jour les équipements
* Segmenter les réseaux avec des VLAN
* Isoler les services exposés dans une DMZ
* Utiliser des règles de pare-feu
* Surveiller les logs
* Utiliser IDS/IPS
* Sécuriser les réseaux Wi-Fi
* Désactiver les services inutiles
* Appliquer le principe du moindre privilège
* Utiliser une approche Zero Trust

---

# ⚠️ Avertissement

Les informations et outils présentés dans ce repository ont un objectif **éducatif, de formation et d'administration légitime**.

Les techniques de reconnaissance, de capture de trafic ou d'analyse réseau doivent être utilisées uniquement :

* sur ses propres systèmes ;
* dans un laboratoire ;
* ou avec l'autorisation explicite du propriétaire de l'infrastructure.

L'auteur de ce repository ne cautionne pas l'utilisation malveillante de ces connaissances.

---

# 📚 Sources et crédits

## 💬 Discord

**Datalyx**

https://discord.gg/WcdH49FquP

## 📖 Source principale

Cours :

**Réseau – Bases & Cybersécurité**

Le contenu de ce repository est basé sur le document de cours fourni.

## 👤 Créateur du cours

**Alpha**

## ✍️ Auteur de ce README

**BestGameClips**

---

# ⭐ Contribution

Les améliorations, corrections et propositions pédagogiques sont les bienvenues.

Avant de contribuer :

1. Vérifier que les informations sont exactes.
2. Garder une structure claire.
3. Éviter les informations non vérifiées.
4. Respecter le contexte pédagogique du projet.

---

# 📜 Licence

À définir selon les souhaits du créateur du projet.

---

<div align="center">

### 🌐 Réseau • 🔐 Cybersécurité • 🧠 Apprentissage

**.gg/Datalyx**

</div>
