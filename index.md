---
layout: default
---

### SmartDrive: Sistema di Monitoraggio dello Stile di Guida

---

# Funzionalità Principali

## Raccolta Dati
- **Sensori Utilizzati**: Accelerometro, giroscopio e GPS dello smartphone.
- **App di Acquisizione**: Utilizzo dell'app Sensor Logger per raccogliere dati in tempo reale e inviarli al server.

## Architettura del Sistema
- **Back-End**: Realizzato in Python con il framework Flask.
- **Database**: MongoDB per la gestione dei dati.
- **Front-End**: Sviluppato con Vue.js per visualizzare i dati in tempo reale.

## Analisi dei Dati
- **Modello di Machine Learning**: Random Forest per classificare lo stile di guida in categorie (prudente, normale, sportivo, aggressivo).
- **Preparazione dei Dati**: Pulizia, normalizzazione e ingegneria delle features per migliorare la precisione del modello.

## Visualizzazione dei Risultati
- **Dashboard**: Interfaccia utente intuitiva che mostra le statistiche di guida e le previsioni del modello.
- **Grafici Interattivi**: Utilizzo di librerie come Chart.js per visualizzare le metriche di guida.

## Sicurezza
- **Crittografia**: Hashing delle password degli utenti con SHA-256.
- **Autenticazione**: Utilizzo di JSON Web Token (JWT) per la gestione sicura delle sessioni.

# Fasi Salienti del Progetto

1. **Acquisizione dei Dati**: Raccolta di oltre 1800 campioni di dati di guida utilizzando Sensor Logger.
2. **Progettazione del Database**: Strutturazione del database con collezioni per campioni, sessioni, test e utenti.
3. **Sviluppo del Modello**: Addestramento del modello Random Forest con i dati raccolti, ottenendo un'accuratezza del 98.82%.
4. **Implementazione delle API**: Creazione di REST API per l'interazione tra front-end e back-end.
5. **Validazione**: Test su strada per verificare l'affidabilità del sistema nel distinguere diversi stili di guida.

# Sviluppi Futuri

- **Integrazione di Nuovi Dati**: Consumo di carburante, usura dei freni e condizioni ambientali.
- **Espansione a Contesti Professionali**: Applicazione per aziende di trasporto e conducenti di veicoli pesanti.
- **Tecniche Avanzate di ML**: Adattamento a diversi tipi di veicoli e utilizzo di reti neurali profonde.

[Scarica il PDF completo del progetto](./SmartDrive_executive_summary_IoT_Longo_Tarantino.pdf)

---

Questo progetto offre un sistema completo per monitorare e migliorare lo stile di guida, fornendo uno strumento utile per aumentare la sicurezza stradale e l'efficienza dei veicoli.

# Header 1

This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](./another-page.html).

There should be whitespace between paragraphs.

There should be whitespace between paragraphs. We recommend including a README, or a file with information about your project.

# Header 1

This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

## Header 2

> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.

### Header 3

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
