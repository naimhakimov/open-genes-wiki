## Это старое описание эндпоинтов API, которое вскоре будет перенесено в Swagger


API проекта возвращает данные в формате json. Все эндпоинты принимают параметр&nbsp;?lang&nbsp;(en|ru)

### `GET` /api/gene — получение общего списка всех занесенных в базу генов с краткой информацией по каждому гену

параметры: `lang(string, "en"|"ru")`

```json
[
  {
    "id": 20,
    "symbol": "NFKB2",
    "name": "nuclear factor of kappa light polypeptide gene enhancer in B-cells 2 (p49/p100)",
    "ncbiId": "4791",
    "uniprot": "NFKB2_HUMAN",
    "origin": {
      "id": 24,
      "phylum": "Bilateria",
      "age": "190",
      "order": 24
    },
    "familyOrigin": {
      "id": 24,
      "phylum": "Bilateria",
      "age": "190",
      "order": 24
    },
    "homologueTaxon": "Bilateria",
    "aliases": [
      "CVID10",
      "H2TF1",
      "LYT-10"
    ],
    "diseases": {
      "51": {
        "icd_id": "D83.0",
        "name": "Immunodeficiency, common variable"
      }
    },
    "functionalClusters": [
      {
        "id": 17,
        "name": "intercellular matrix"
      },
      {
        "id": 27,
        "name": "signaling"
      }
    ],
    "expressionChange": "decreased",
    "timestamp": 1630401670,
    "ensembl": "ENSG00000077150",
    "methylationCorrelation": "decrease",
    "diseaseCategories": {
      "D80-D89": {
        "icd_category_name": "Certain disorders involving the immune mechanism"
      }
    },
    "commentCause": {
      "8": "Age-related changes in gene expression/protein activity in mammals"
    }
  }, ...
]
```

### `GET` /api/gene/&lt;symbol&gt; — получение полной информации об одном гене по его символу

параметры: `lang(string, "en"|"ru"), symbol(string, "ADCY5")`

```json
{
  "id": 254,
  "name": "adenylate cyclase 5",
  "symbol": "ADCY5",
  "aliases": [
    "AC5",
    "FDFM"
  ],
  "homologueTaxon": "Bilateria",
  "origin": {
    "id": 3,
    "phylum": "Eumetazoa",
    "age": "800",
    "order": 5
  },
  "familyOrigin": {
    "id": 3,
    "phylum": "Eumetazoa",
    "age": "800",
    "order": 5
  },
  "diseases": {
    "274": {
      "icd_id": "G51.4",
      "name": "Dyskinesia, familial, with facial myokymia"
    }
  },
  "diseaseCategories": {
    "G50-G59": {
      "icd_category_name": "Nerve, nerve root and plexus disorders"
    }
  },
  "ncbiId": "111",
  "uniprot": "ADCY5_HUMAN",
  "commentEvolution": "Adenylyl cyclases are conserved enzymes...",
  "commentFunction": "",
  "descriptionNCBI": "This gene encodes a member of...",
  "descriptionOG": "ADCY5 catalyzes the synthesis...",
  "commentCause": {
    "6": "Gene activity modulation increases mammalian lifespan",
    "13": "Modulation of gene activity protects against age-related impairment"
  },
  "commentAging": "ADCY5 knock-out increases the ...",
  "commentsReferenceLinks": {
    "1": "10.1124/pr.109.001370",
    "2": "10.1124/mol.115.099556"
  },
  "rating": null,
  "functionalClusters": [
    {
      "id": 27,
      "name": "signaling"
    },
    {
      "id": 8,
      "name": "glucose metabolism"
    }
  ],
  "researches": {
    "increaseLifespan": [
      {
        "interventionType": "gene knockout",
        "interventionResult": "increases lifespan",
        "modelOrganism": "mice",
        "organismLine": "wild type",
        "age": "0 days",
        "genotype": "",
        "valueForMale": "",
        "valueForFemale": "",
        "valueForAll": "30%",
        "doi": "10.1016/j.cell.2007.05.038",
        "pmid": "",
        "comment": ""
      }
    ],
    "geneAssociatedWithProgeriaSyndromes": [
      {
        "progeriaSyndrome": "синдром Кокейна",
        "doi": "",
        "pmid": " 21416736",
        "comment": "Есть пять генов, ответственных за прогероидный синдром Кокейна: CSA, CSB, XPB, XPD и XPG, в которых были обнаружены различные мутации."
      }
    ],
    "geneAssociatedWithLongevityEffects": [
      {
        "longevityEffect": "ассоциация с долголетием",
        "allelicPolymorphism": "rs1042522",
        "sex": "оба пола",
        "allelicVariant": "C",
        "modelOrganism": "человек",
        "changeType": "",
        "dataType": "геномные",
        "doi": "10.4161/cc.7.2.5249",
        "pmid": "",
        "comment": "Полиморфизм C/G (P72R). Исследование проведено среди населения Дании (n=9219)"
      }
    ],
    "ageRelatedChangesOfGene": [
      {
        "changeType": "повышение экспрессии гена",
        "sample": "костный мозг",
        "modelOrganism": "человек",
        "organismLine": "",
        "ageFrom": "41 г.",
        "ageTo": "67 г.",
        "valueForMale": "",
        "valueForFemale": "",
        "valueForAll": "130%",
        "measurementType": "мРНК",
        "doi": "10.1111/j.1474-9726.2008.00377.x",
        "pmid": "",
        "comment": "Увеличение экспрессии гена р53 (в 2,3 раза, p<0,01, тест Манна-Уитни) обнаружено в мезенхимальных стволовых клетках человека, полученных от людей старшего возраста (n=9; ≥55 лет) по сравнению с более молодыми людьми (n=3; <50 лет)."
      }
    ],
    "interventionToGeneImprovesVitalProcesses": [
      {
        "geneIntervention": "gene knockout",
        "vitalProcess": "cardiovascular system",
        "modelOrganism": "mice",
        "organismLine": "wild type",
        "interventionResult": "improvement",
        "age": "0 days",
        "genotype": "",
        "sex": "both",
        "doi": "10.1016/j.cell.2007.05.038",
        "pmid": "",
        "comment": "Old AC5 KO mice are protected from aging-induced cardiomyopathy, e.g., hypertrophy, apoptosis, fibrosis, and reduced cardiac function"
      }
    ],
    "proteinRegulatesOtherGenes": [
      {
        "proteinActivity": "активирует",
        "regulationType": "экспрессия гена",
        "doi": "10.1038/onc.2011.35",
        "pmid": "",
        "comment": "P53 трансактивирует FOXO3 в клетках, связываясь с сайтом во втором интроне гена FOXO3, - геномная область, связанная с увеличением продолжительности жизни у человека.",
        "regulatedGene": {
          "id": "122",
          "symbol": "FOXO3",
          "name": "forkhead box O3",
          "ncbiId": "2309"
        }
      }
    ],
    "additionalEvidences": [
      {
        "doi": "",
        "pmid": "25731027",
        "comment": "Полиморфизм генов эксцизионной репарации XPD Asp312Asn, XRCC1 Arg399Gln, OGG1 Ser326Cys и ERCC6 Met1097Val проанализирован методом ..."
      }
    ]
  },
  "expression": [
    {
      "name": "heart",
      "exp_rpkm": "22.9328"
    },
    {
      "name": "brain",
      "exp_rpkm": "7.27413"
    },
    {
      "name": "pancreas",
      "exp_rpkm": "0.566677"
    }
  ],
  "functions": [
    {
      "proteinActivity": "upregulates",
      "proteinActivityObject": "cAMP synthesis",
      "processLocalization": "",
      "comment": ""
    }
  ],
  "proteinClasses": [
    "Disease related genes",
    "Enzymes",
    "Potential drug targets"
  ],
  "expressionChange": "decreased",
  "band": "3q21.1",
  "locationStart": "123282296",
  "locationEnd": "123448545",
  "orientation": "-1",
  "accPromoter": "",
  "accOrf": "NM_183357",
  "accCds": "NP_899200",
  "terms": {
    "biological_process": [
      {
        "1973": "adenosine receptor signaling pathway"
      },
      {
        "3091": "renal water homeostasis"
      }
    ],
    "cellular_component": [
      {
        "5623": "cell"
      },
      {
        "5886": "plasma membrane"
      }
    ],
    "molecular_activity": [
      {
        "4016": "adenylate cyclase activity"
      },
      {
        "5524": "ATP binding"
      }
    ]
  },
  "orthologs": {
    "CG43373": "",
    "Drosophila melanogaster": "Adcy5",
    "Rattus norvegicus": "Adcy5",
    "Mus musculus": "adcy5",
    "Danio rerio": ""
  },
  "why": [
    "mammal"
  ],
  "timestamp": 1628007922,
  "human_protein_atlas": {
    "Gene": "ADCY5",
    "GeneSynonym": [
      "AC5"
    ],
    "Ensembl": "ENSG00000173175",
    "GeneDescription": "Adenylate cyclase 5",
    "Uniprot": [
      "O95622"
    ],
    "Chromosome": "3",
    "Position": "123282296-123449758",
    ... (full HPA array)
  },
  "ensembl": "ENSG00000173175",
  "methylationCorrelation": ""
}
```

### `GET` /api/gene/by-latest — получение четырех последних обновленных генов

параметры: `lang(string, "en"|"ru")`

```json
[
  {
    "id": 372,
    "origin": null,
    "familyOrigin": {
      "id": 2,
      "phylum": "Eukaryota",
      "age": "1000–1900",
      "order": 2
    },
    "homologueTaxon": null,
    "symbol": "TUBB6",
    "timestamp": 1630435177
  }, ...
]
```

### `GET` /api/gene/by-functional-cluster/&lt;ids&gt; — получение списка генов, принадлежащих одновременно ко всем перечисленным функциональным кластерам

параметры: `lang(string, "en"|"ru"), ids (string, список id через запятую, "12,14,15")`


Структура ответа такая же, как в&nbsp;/api/gene

### `GET` /api/gene/by-selection-criteria/&lt;ids&gt;&nbsp;- получение списка генов, принадлежащих одновременно ко всем перечисленным критериям отбора.


параметры: `lang(string, "en"|"ru"), ids (string, список id через запятую, "12,14,15")`

Структура ответа такая же, как в&nbsp;`/api/gene`
### `GET` /api/gene/by-go-term/&lt;term&gt;&nbsp;- получение списка генов, имеющих заданный GeneOntology term.

параметры: `lang(string, "en"|"ru"), term (string, "cytosol")`

Структура ответа такая же, как в&nbsp;`/api/gene`
### `GET` /api/gene/by-expression-change/&lt;expression-change&gt;&nbsp;- получение списка генов, имеющих заданное значение изменения экспрессии

параметры: `lang(string, "en"|"ru"), expression-change (string, "decreased")`

Структура ответа такая же, как в&nbsp;`/api/gene`
### `GET` /api/disease - получение списка заболеваний

параметры: `lang(string, "en"|"ru")`

```json
[
  {
    "id": "1",
    "icd_code": "E78.0",
    "name": "Hypercholesterolemia, familial",
    "icd_name": "Pure hypercholesterolaemia"
  },
  {
    "id": "2",
    "icd_code": "E34.3",
    "name": "Growth hormone deficiency, isolated partial",
    "icd_name": "Short stature, not elsewhere classified"
  }, ...
]
```

### `GET` /api/disease-category - получение списка категорий заболеваний

параметры: lang(string, "en"|"ru")

```json
[
  {
    "icd_code": "E70-E90",
    "icd_category_name": "Metabolic disorders"
  },
  {
    "icd_code": "E20-E35",
    "icd_category_name": "Disorders of other endocrine glands"
  }, ...
]
```
