# Commit & Conquer

### Regolamento

**Commit & Conquer** è un gioco di dadi in cui due o più developer si scontrano per portare a
termine un progetto il più velocemente possibile, con la qualità più alta possibile.

Per completare il progetto i developer dovranno fare dei _commit_ , aprire _pull request_ e chiedere ai
propri colleghi di fare _code review_. Potranno anche consultare la nota piattaforma _HeapOverrun_ ,
da cui copiare codice di dubbia provenienza, che velocizzerà il lavoro aumentando il rischio di _bug_.

Scopo del gioco è arrivare a 20 punti prima degli altri developer.

Come prima cosa, ogni developer sceglie il linguaggio in cui è senior:
Javascript (1) | Python (2) | Java (3) | C++ (4) | PHP (5) | Ruby (6)

Il gioco si svolge a turni, durante i quali un developer può fare una delle seguenti azioni:
**- commit** : aggiungi 1 dado alla riserva
**- copiare da HeapOverrun** : aggiungi 2 dadi alla riserva, ignora il linguaggio senior
**- leggere la documentazione** : ritiri un dado al _push_
**- chiedere una code review** : elimini un _bug_ al _push_
**- push** : lanci tutti i dadi accumulati finora nella riserva

## Accumulare punti

Una volta fatto il push, il developer svuota la riserva e guadagna punti:
- +1 punto per il _commit_ iniziale
- +2 punti per ogni _commit_ oltre quello iniziale
- -3 punti per ogni _bug_ ottenuto

## Bug

Il developer ottiene un bug per ogni dado che ottiene lo stesso risultato di un altro dado:
```
esempioBug = 5 dadi lanciati => 2, 3, 3, 5, 6 => ci sono 2 bug (3, 3)
```

Il developer ignora il primo dado che ottiene il punteggio corrispondente al suo linguaggio
senior, quando calcola i bug:
```
esempioBugSenior_1 = 5 dadi lanciati => 3, 3, 3, 5, 6 => ci sono 2 bug (3, 3)

esempioBugSenior_2 = 5 dadi lanciati => 2, 3, 3, 5, 6 => non ci sono bug
```
