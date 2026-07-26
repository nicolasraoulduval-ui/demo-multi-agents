# Démos multi-agents

Trois simulations interactives qui montrent comment fonctionne un système multi-agents IA — non pas par une explication, mais en regardant une équipe travailler : découpage des tâches, dépendances, blocages, erreurs détectées par un agent critique, sous-tâches créées en route, décisions collectives par vote.

Chaque démo est un fichier HTML autonome (zéro dépendance, zéro build) : il suffit de l'ouvrir dans un navigateur. La simulation se déroule toute seule (contrôles pause / ×2 / ×3) et se termine par un récapitulatif qui traduit chaque scène en concept d'architecture multi-agents réelle.

## Les trois niveaux

| Fichier | Niveau | Sujet |
|---|---|---|
| `soiree-pizza.html` | Grand public | 6 personnes organisent une soirée pizza pour 20 invités — appartement vu de dessus, personnages animés, zéro jargon |
| `comite-vc.html` | Cas métier | Un fonds VC décide en une journée d'investir 2 M€ dans une startup — bureau isométrique 3D, due diligence complète, 3 red flags, vote de comité |
| `agentos.html` | Vue système | Lancement d'un SaaS restaurateurs — interface de contrôle : flux d'événements, Kanban, documents versionnés, réunion d'arbitrage |

`index.html` sert de page d'accueil et relie les trois.

## Concepts illustrés

- **Orchestrateur** : un agent découpe la mission, assigne et arbitre sans rien produire lui-même
- **Mémoire partagée (blackboard)** : tableau de tâches et documents communs plutôt que tout-par-messages
- **Graphe de dépendances** : des agents bloqués en attente d'autres — le parallélisme n'est jamais total
- **Agent critique / adversarial** : un rôle dédié à contredire les autres, qui attrape les erreurs invisibles à leurs auteurs
- **Décomposition dynamique** : des tâches créées en cours de route quand un imprévu apparaît
- **Décision collective** : débat cadré, vote, et objection minoritaire consignée

## Déploiement

Compatible GitHub Pages tel quel : Settings → Pages → Deploy from branch → `main` / racine. La page d'accueil sera servie automatiquement via `index.html`.

## Limite honnête

Les scénarios sont scriptés pour être pédagogiques. Un vrai système multi-agents produit ces comportements de façon émergente — avec plus de bruit, des erreurs non rattrapées et des coûts en tokens. L'orchestration montrée ici est précisément ce qui est difficile à obtenir en production.
# demo-multi-agents
