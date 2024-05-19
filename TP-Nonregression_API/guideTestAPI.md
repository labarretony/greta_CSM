
### Lancer SoapUI

#### Création du projet et des ressources à utiliser
Créer un nouveau projet vide et votre première ressource

![Gif créer ressources](/docs/ressources.gif)

#### Création d’une suite de test et d’un cas de test
Dans SoapUi, les tests sont décomposés en 3 niveaux : TestSuite, TestCase et TestStep.

- Une suite de test est une collection de cas de tests qui ciblent une même fonctionnalité ou qui ont une
unité logique.
- Un cas de test est une collection d’étapes de tests qui sont assemblées de manière à tester un aspect
du service.
- L’étape de test est donc le bloc de construction du test fonctionnel.

![Gif créer suite de test](/docs/testsuite.gif)

#### Les assertions

Exemple d'assertion :

Assert Status
![Gif status code](/docs/assert_status.gif)

Assert script
![Gif assert script](/docs/assert_script.gif)
```
import groovy.json.JsonSlurper
def response = messageExchange.response.responseContent
def slurper = new JsonSlurper()
def json = slurper.parseText response

assert json.size() == 2

```

```
import groovy.json.JsonSlurper
def response = messageExchange.response.responseContent
def slurper = new JsonSlurper()
def json = slurper.parseText response

assert json[0].id == 'SAL2'

```

Assert jsonPath
![Gif assert jsonPathCount](/docs/assert_jsonpath.gif)
![Gif assert jsonPath](/docs/assert_jsonpath2.gif)


