## Atelier 1.1 : Installation de la CLI ArgoCD (30 min)

#### Objectif
Installer et configurer l'outil en ligne de commande ArgoCD sur votre machine locale.

#### Prérequis
- Accès à un terminal
- Connexion internet
- Droits d'administration (pour l'installation)

#### Instructions

**Sur Linux :**
```bash
# Téléchargement de la dernière version
curl -sSL -o argocd-linux-amd64 https://github.com/argoproj/argo-cd/releases/latest/download/argocd-linux-amd64

# Installation
sudo install -m 555 argocd-linux-amd64 /usr/local/bin/argocd

# Nettoyage
rm argocd-linux-amd64

# Vérification
argocd version --client
```

**Sur macOS :**
```bash
# Avec Homebrew
brew install argocd

# Vérification
argocd version --client
```

**Sur Windows :**
```powershell
# Téléchargement manuel depuis GitHub
# https://github.com/argoproj/argo-cd/releases/latest

# Ou avec Chocolatey
choco install argocd-cli

# Vérification
argocd version --client
```

#### Validation
Vous devriez voir une sortie similaire à :
```
argocd: v2.9.0+unknown
  BuildDate: 2023-11-13T19:22:51Z
  GitCommit: abcd1234
  GoVersion: go1.21.3
  Compiler: gc
  Platform: linux/amd64
```

#### Questions
1. Quelle version d'ArgoCD avez-vous installée ?
2. À quoi sert la CLI par rapport à l'interface web ?

## Atelier 1.2 : Exploration de l'architecture (45 min)

#### Objectif
Comprendre en profondeur l'architecture d'ArgoCD et le rôle de chaque composant.

#### Activité 1 : Schéma d'architecture collaboratif

**Étapes :**
1. Divisez la classe en groupes de 3-4 personnes
2. Chaque groupe dessine l'architecture d'ArgoCD sur un tableau blanc/papier
3. Incluez tous les composants et leurs interactions
4. Présentez votre schéma aux autres groupes (5 min par groupe)

**Points à inclure :**
- Git Repository
- API Server
- Repository Server
- Application Controller
- Redis
- Kubernetes Cluster
- UI / CLI
- Flux de données
