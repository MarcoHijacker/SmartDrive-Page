---
layout: default
---

### Contesto attuale

La sicurezza stradale e l'efficienza nella guida dei veicoli sono temi di crescente importanza nel contesto delle moderne tecnologie di mobilità. Con l'incremento dell'adozione di sistemi di monitoraggio e telemetria, è diventato possibile raccogliere una quantità significativa di dati riguardanti il comportamento del veicolo e dello stile di guida. 

### Obiettivi dell'applicativo

**SmartDrive** si pone l'obiettivo di sviluppare un sistema integrato per l'acquisizione, l'analisi e la visualizzazione dei dati di guida, al fine di stimare lo stile di guida del conducente e migliorare la sicurezza e l'efficienza.

### Project team

| Matricola          | Cognome            | Nome               | E-mail                                                                                    |
|:-------------------|:-------------------|:-------------------|:------------------------------------------------------------------------------------------|
| 20090064           | Longo              | Marco              | [marco.longo@studenti.unisalento.it](mailto:marco.longo@studenti.unisalento.it)           |
| 20094004           | Tarantino          | Priamo             | [priamo.tarantino@studenti.unisalento.it](mailto:priamo.tarantino@studenti.unisalento.it) |

### Architettura del sistema

- **Back-end**: Realizzato in _Python_ con l'ausilio del framework _Flask_.
- **Front-end**: Sviluppato con _Vue.js_, con l'ausilio di _Chart.js_ per visualizzare i dati su grafici professionali.
- **Database**: Database NoSQL (_MongoDB_) per lo storage dei dati.

<a href="https://raw.githubusercontent.com/MarcoHijacker/SmartDrive-Page/main/assets/images/smartdrive_schema.png" target="_blank">![SmartDrive Schema](https://raw.githubusercontent.com/MarcoHijacker/SmartDrive-Page/main/assets/images/smartdrive_schema.png)</a>

### Raccolta dati

- **Sensori utilizzati**: Accelerometro, giroscopio e GPS dello smartphone.
- **App di acquisizione**: Utilizzo dell'app _Sensor Logger_ per raccogliere dati in tempo reale e inviarli al back-end.

### Analisi dei dati

- **Modello di Machine Learning**: Utilizzo del modello _Random Forest_ per classificare lo stile di guida in 4 categorie (prudente, normale, sportivo, aggressivo).
- **Preparazione dei dati**: Pulizia, normalizzazione ed ingegneria delle features per migliorare la precisione del modello.

### Accessibilità della WebApp

- **Registrazione**: La fase di registrazione richiede all'utente: nome, cognome, e-mail, password ed il _Device ID_ del dispositivo in uso (recuperabile nel menù impostazioni dell'app _Sensor Logger_). Hashing delle password degli utenti con _SHA-256_.
- **Login**: Procedura di accesso sicuro tramite autenticazione _JWT_.

<a href="https://raw.githubusercontent.com/MarcoHijacker/SmartDrive-Page/main/assets/images/login_page.png" target="_blank">![Login Page](https://raw.githubusercontent.com/MarcoHijacker/SmartDrive-Page/main/assets/images/login_page.png)</a>

### Sessioni di guida

Ogni utente registrato può creare delle sessioni di guida. Una volta alla guida (con l'app _Sensor Logger_ avviata), il back-end recepirà i campioni (raccolti con cadenza di 1 secondo) e li salverà sul DB associandoli alla sessione attiva dell'utente.

<a href="https://raw.githubusercontent.com/MarcoHijacker/SmartDrive-Page/main/assets/images/sessions.png" target="_blank">![Sessions CRUD](https://raw.githubusercontent.com/MarcoHijacker/SmartDrive-Page/main/assets/images/sessions.png)</a>

### Visualizzazione dei risultati

- **Statistiche generali**: La sezione principale della dashboard mostra le statistiche medie di guida dell'utente relativamente a tutte le sessioni.

<a href="https://raw.githubusercontent.com/MarcoHijacker/SmartDrive-Page/main/assets/images/dashboard_user.png" target="_blank">![Dashboard User](https://raw.githubusercontent.com/MarcoHijacker/SmartDrive-Page/main/assets/images/dashboard_user.png)</a>

- **Grafici di sessione**: La sezione relativa alle statistiche di sessione mostra svariati grafici per stimare l'andamento puntuale di: accelerazione, velocità, rollìo, beccheggio. Per ogni campione sul grafico è possibile analizzare lo stile di guida istantaneo ad esso associato. Infine è presente una mappa che traccia il percorso effettuato dal guidatore per la sessione in corso.

### Fasi Salienti del Progetto

1. **Acquisizione dei Dati**: Raccolta di oltre 1800 campioni di dati di guida utilizzando Sensor Logger.
2. **Progettazione del Database**: Strutturazione del database con collezioni per campioni, sessioni, test e utenti.
3. **Sviluppo del Modello**: Addestramento del modello Random Forest con i dati raccolti, ottenendo un'accuratezza del 98.82%.
4. **Implementazione delle API**: Creazione di REST API per l'interazione tra front-end e back-end.
5. **Validazione**: Test su strada per verificare l'affidabilità del sistema nel distinguere diversi stili di guida.

<a href="https://raw.githubusercontent.com/MarcoHijacker/SmartDrive-Page/main/assets/images/postman_collection.png" target="_blank">![Postman Collection](https://raw.githubusercontent.com/MarcoHijacker/SmartDrive-Page/main/assets/images/postman_collection.png)</a>

### Sviluppi Futuri

- **Integrazione di Nuovi Dati**: Consumo di carburante, usura dei freni e condizioni ambientali.
- **Espansione a Contesti Professionali**: Applicazione per aziende di trasporto e conducenti di veicoli pesanti.
- **Tecniche Avanzate di ML**: Adattamento a diversi tipi di veicoli e utilizzo di reti neurali profonde.

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
