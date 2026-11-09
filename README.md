# Programmare in RPG su IBM i

Sorgenti del corso in formato Learn2K: un'introduzione a ILE RPG, dal formato libero
all'accesso ai file di database, all'SQL embedded e al codice storico a colonne fisse.

```sh
learn-author validate   # controlla i sorgenti
learn-author preview    # anteprima con ricarica a caldo
learn-author build      # bundle e manifest in dist/
```

## Documentazione

Le regole del formato sono nelle guide della versione di `learn-author` in uso, che il comando
stampa:

```sh
learn-author guide formato                           # lezioni, componenti, quiz, simulatori, CI
learn-author guide formato --toc                     # l'indice
learn-author guide formato --section "<Simulator>"   # una sola sezione
learn-author guide esercizi                          # gli esercizi, verificati in Docker
learn-author guide demo <cartella>                   # il corso demo, un esempio per componente
```

Le stesse guide, con il corso demo e gli schemi JSON per l'editor, sono nel materiale per gli
autori, che si scarica dalla pagina «learn-author» del backoffice di Learn2K
(«Scarica il materiale»).

`AGENTS.md` dice agli agenti AI quale sezione leggere prima di scrivere una lezione, un quiz,
un esercizio o un simulatore.
