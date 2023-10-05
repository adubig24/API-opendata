localhost:5001

# Opendata API

Opendata API est une simple API qui sert à récupérer les informations de consommations d'électricité par région

## Questions Collection [/questions]

### Lister toutes les consommations [GET]

+ Response 200 (api/consommation/)

        [
           	{
        		"ANNEE": 2009,
        		"CONSOA": 0,
        		"CONSOI": 0,
        		"CONSONA": 0,
        		"CONSOR": 1455,
        		"CONSOT": 14712,
        		"DEPARTEMENT": "Seine-Saint-Denis"
    		}
        ]

### Créer une nouvelle consommation [POST]

On peut créer une nouvelle consommation avec le POST

+ Request (api/consommation/)

        "query": [
		{
			"key": "ANNEE",
			"value": "2014"
		},
		{
			"key": "CONSOR",
			"value": "42"
		},
		{
			"key": "CONSOT",
			"value": "42"
		},
		{
			"key": "CONSOI",
			"value": "42"
		},
		{
			"key": "CONSOA",
			"value": "42"
		},
		{
			"key": "CONSONA",
			"value": "42"
		},
		{
			"key": "DEPARTEMENT",
			"value": "Loire"
		}
	]

+ Response 200 (application/json)

    + Body

        {
    		"message": "ok"
	}

### Lister toutes les consommations d'un département [GET]

+ Response 200 (api/consommation/<nom du département>)

        [
    		{
        		"ANNEE": "2014",
        		"CONSOA": "42",
        		"CONSOI": "42",
        		"CONSONA": "42",
        		"CONSOR": "42",
        		"CONSOT": "42",
        		"DEPARTEMENT": "Loire"
    		},
	]

### Supprimer une entrée d'un département [DELETE]

+ Request (api/consommation/<nom du département>)


	"query": [
		{
			"key": "DEPARTEMENT",
			"value": "Var"
		},
	]

+ Reponse 200 

{
    "message": "ok"
}

### Créer une nouvelle consommation [PUT]

On peut update une nouvelle consommation avec le PUT

+ Request (api/consommation/)

        "query": [
		{
			"key": "ANNEE",
			"value": "2014"
		},
		{
			"key": "CONSOR",
			"value": "42"
		},
		{
			"key": "CONSOT",
			"value": "42"
		},
		{
			"key": "CONSOI",
			"value": "42"
		},
		{
			"key": "CONSOA",
			"value": "42"
		},
		{
			"key": "CONSONA",
			"value": "42"
		},
		{
			"key": "DEPARTEMENT",
			"value": "Loire"
		}
	]