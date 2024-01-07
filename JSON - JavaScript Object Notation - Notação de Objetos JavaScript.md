
>É uma formatação leve de troca de dados. Quando formos consultar uma API é bem provável que ela nos retorne um JSON

**JSON** é um formato de dados baseado em texto seguindo a sintaxe do objeto JavaScript. Mesmo que se assemelhe à sintaxe literal do objeto JavaScript, ele pode ser usado independentemente do JavaScript, e muitos ambientes de programação possuem a capacidade de ler (analisar) e gerar JSON

JSON é uma sintaxe para serialização de objetos, matrizes, números, strings, booleanos, e null. Baseia-se em sintaxe Javascript, mas é distinta desta: 
>Alguns Javascript não são JSON, e alguns JSON não são Javascript.
#### Exemplo de Sintaxe:
```JSON
{
  "squadName": "Super hero squad",
  "homeTown": "Metro City",
  "formed": 2016,
  "secretBase": "Super tower",
  "active": true,
  "members": [
    {
      "name": "Molecule Man",
      "age": 29,
      "secretIdentity": "Dan Jukes",
	      "powers": ["Radiation resistance", "Turning tiny", "Radiation blast"]
    },
    {
      "name": "Madame Uppercut",
      "age": 39,
      "secretIdentity": "Jane Wilson",
	      "powers": [
	        "Million tonne punch",
	        "Damage resistance",
	        "Superhuman reflexes"
	     ]
    },
    {
      "name": "Eternal Flame",
      "age": 1000000,
      "secretIdentity": "Unknown",
	      "powers": [
	        "Immortality",
	        "Heat Immunity",
	        "Inferno",
	        "Teleportation",
	        "Interdimensional travel"
	      ]
    }
  ]
}
```

---
Fontes:
- https://developer.mozilla.org/pt-BR/docs/Learn/JavaScript/Objects/JSON
- https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/JSON
Tags: #softwaredevelopment 