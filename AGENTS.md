<!-- Written by learn-author 0.5.1: learn-author new ci lo riscrive. Per cambiarlo, togli questa riga. -->
# Come si scrive questo corso

Questo repository contiene i sorgenti di un corso di Learn2K: lezioni in MDX, quiz, esercizi e simulatori, che `learn-author` compila. Il workflow `.github/workflows/learn2k.yml` verifica il corso a ogni pull request e lo pubblica su Learn2K a ogni push su `main`.

## Le guide

Le regole sono nelle guide della versione di `learn-author` in uso, che il comando stampa:

- `learn-author guide formato`: struttura, lezioni, componenti, quiz, simulatori, pubblicazione e CI. `--toc` ne dà l'indice, `--section "<titolo>"` una sola sezione.
- `learn-author guide esercizi`: gli esercizi, verificati in Docker come con `learn check`.
- `learn-author guide demo <cartella>`: copia il corso demo, con un esempio di ogni componente.

Prima di scrivere una lezione, un quiz, un esercizio o un simulatore, leggi la sezione della guida che ne parla.

## Regole

- Dopo ogni modifica esegui `learn-author validate`: deve finire senza errori, e gli avvisi vanno corretti.
- Gli id di corso, moduli, lezioni, attività e obiettivi sono stabili: dopo la pubblicazione non si cambiano più, perché i progressi degli studenti restano legati agli id. `learn-author new …` li ricava dal titolo una volta sola.
- Nelle lezioni niente JavaScript: né espressioni `{…}` né `import` o `export`, solo Markdown e i componenti della guida.
- Ogni immagine ha un testo alternativo che descrive ciò che mostra.
- Un simulatore è una pagina autonoma, `simulators/<id>/index.html`, e segue «Simulatori accessibili» della guida.
- La soluzione di ogni esercizio supera le verifiche e lo starter no: `learn-author test-exercises` lo controlla in Docker.
- `learn-author preview` mostra il corso come lo vedranno gli studenti.

## Pubblicazione

Il corso non si pubblica a mano: la CI lo pubblica a ogni push su `main`, se il repository è collegato al corso nel backoffice di Learn2K («Pubblicazione dalla CI»). Una versione nuova arriva agli studenti solo quando il docente sposta la loro coorte. Per passare a una versione più recente di `learn-author`, aggiornalo ed esegui `learn-author new ci`: riscrive il workflow e questo file.
