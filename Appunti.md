# HTML & CSS

### Struttura o File System di un sito web
-| www.miosito.it
 |--img
 |--css
 |--js
 |index.html

Ho bisogno di avere un file che si chiama index.html nella cartella del sito perché serve ai WEB SERVER come homepage

## ELEMENTI (TAG o MARKUP)
Sono i tag e ce ne sono di 2 tipi:

- **block** (cominciano sempre con una nuova riga e occupano tutto lo spazio disponibile)
- **inline** (si dispongono uno accanto all'altro e occupano solo lo spazio necessario)
- **vuoti** (sono tag che non hanno chiusura ma solo apertura) es: `<img>`; `<input>`; `<hr>`; `<br>`

Questa divisione detta le regole della nidificazione

OSS: **Spazi Vuoti** nello HTML gli spazi vuoti, bianchi che si utilizzano intorno ai contenuti non contanto, cioè non vengono renderizzati

### Commenti
`<!-- -->` Questo è il selettore per poter scrivere un commento.

In VSC posso anche usare la combinazione `Alt + ù` per poter commentare una riga o un blocco di righe

### Elementi di Heading
Questi sono elementi importantissimi poiché permettono di dare un titolo alla pagina o alla section. Quando la nostra pagina viene scandagliata dai motori di ricerca questi elementi permettono immediatamente di far capire di cosa stiamo parlando.

Ci sono 6 intestazione:
- `<h1> </h1>` intestazione più importante
- `<h2> </h2>` 
- `<h3> </h3>` 
- `<h4> </h4>` 
- `<h5> </h5>` 
- `<h6> </h6>` intestazione meno importante

**OSS**: All'interno di 1 pagina ci dovrebbe essere sempre e solo un `<h1>`

**OSS**: Non utilizzare i tag **h** per fare tipografia. Cioè se sono in un titolo `<h3>` e mi serve con un font maggiore NON passo all' `h2` perché in questo modo gli sto dando solo maggiore importanza.

### `<p>`
Questo elemento definisce un paragrafo.

Testo che descrive qualcosa. Anche i tag p sono elementi di tipo block

### `<ul>`
Liste non ordinate (unordered list). Con all'interno il tag `<li>` crea delle liste puntate di elementi (list items)
```html
<ul>
    <li>item 1</li>
    <li>item 2</li>
    <li>item 3</li>
</ul>
```


### `<hr>` `<pre>` `<br>`
- hr: tira una linea orizzonatale
- pre: imposta un testo preformattato
- br: va a capo. ATT: non utilizzando per creare spazi in verticale

### Semantica del testo (tutti inline)

| Elemento | Significato | Resa tipica |
|---|---|---|
| `<b>` | Grassetto, senza importanza aggiuntiva | grassetto |
| `<strong>` | Testo **importante** (enfasi semantica) | grassetto |
| `<i>` | Voce/tono diverso: termini tecnici, parole straniere | corsivo |
| `<em>` | Testo **enfatizzato** (enfasi semantica) | corsivo |
| `<small>` | Note a margine: copyright, testo legale | più piccolo |
| `<mark>` | Testo evidenziato per riferimento | evidenziato |
| `<del>` | Testo eliminato | barrato |
| `<ins>` | Testo inserito successivamente | sottolineato |
| `<sub>` | Pedice | in basso |
| `<sup>` | Apice | in alto |

### Citazioni e abbreviazioni

| Elemento | Tipo | Uso |
|---|---|---|
| `<q>` | inline | Citazione breve; il browser aggiunge le virgolette |
| `<blockquote>` | block | Citazione estesa; il browser applica un rientro. Attributo `cite` = URL della fonte |
| `<cite>` | inline | **Titolo** di un'opera (reso in corsivo) |
| `<abbr>` | inline | Abbreviazione/acronimo; `title` contiene la forma estesa |


### Semantica del codice (tutti inline, resi in monospace)

| Elemento | Rappresenta | Esempio |
|---|---|---|
| `<kbd>` | Input dell'utente (tastiera, comandi vocali) | `<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>R</kbd>` |
| `<samp>` | Output di un programma | `<samp>Tastiera non trovata</samp>` |
| `<code>` | Frammento di codice | `La proprietà <code>display</code>…` |
| `<var>` | Variabile (matematica o programmazione) | `<var>l</var> × <var>w</var> × <var>h</var>` |

##  Immagini e percorsi

### Percorsi relativi e assoluti
**I percorsi assoluti** puntano a file (immagini e altro) esistenti sul web e hostati su server esterni attraverso il loro link.
**I percorsi relativi** puntano a file esistenti nella cartella del progetto

## Collegamento al foglio di stile CSS
Il CSS (Cascade Style Sheet). Foglio di stile a cascata. Mi permette di fornire regole di stile e formattazione agli elementi della pagina.

Come e dove collego un foglio di stile:
```html
<head>
    .
    .
    .
    <link rel="stylesheet" href="./css/style.css">
</head>
```
Và sempre collegato al fondo della head.

**TIPS**: una volta costruito il tag link al fondo della head posso fare `Ctrl + click` sul path dello href per permettere a VSC di creare per me sia la cartella css sia il file style.css 

### Selettori 
- Tag Name (**nomeTag**) 
- Class (**.nomeClasse**)
- Id (**#idElemento**)

**ATT**: Quando fornmisco una regola css ad un selettore tag allora tutti gli elementi con quel tag nella pagina avranno le stesse regole. Stessa cosa vale per le classi

**ATT**: l'attributo id è univoco all'interno del file: uno e un solo elemento può avere quell'attributo collegato

In Html:
```html
<h1 id = "titoloPrincipale">...</h1>
```
In CSS
```css
#titoloPrincipale{
    font-size: 25px
}
```

**ATT**: l'attributo class può essere ripetuto su quanti elementi vogliamo e ogni singolo elemento può avere n classi

In Html:
```html
<h2 class = "txtRed txtBig">...</h2>
<h3 class = "txtRed txtBig">...</h2>
```
In CSS:
```css
.txtRed{
    color: red;
}
```
Ovviamente un tag che ha un id può tranquillamente avere una classe o più classi.

### Style in linea con il codice (NON CONSIGLIATO)



## TIP e TRICKS per VSCode
- Commenti automatici `Ctrl + ù`
- Inseguire un link `Ctrl + click` sul path per aprire quel file. Se non lo trova lo crea