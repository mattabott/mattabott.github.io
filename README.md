# mattabott.github.io

Sito di supporto per **Airsoft Tactical**.

Serve due cose:

- `/.well-known/assetlinks.json` e `/.well-known/apple-app-site-association`,
  i file con cui Android e iOS verificano che questo dominio possa aprire
  l'app invece del browser (App Links / Universal Links);
- `/at/j`, la pagina che vede chi apre un invito senza avere l'app
  installata: mostra la partita e il codice da incollare.

`.nojekyll` serve perché GitHub Pages, passando per Jekyll, salterebbe la
cartella `.well-known` (comincia con un punto) e i due file di verifica
risponderebbero 404.

I dati dell'invito viaggiano nel **frammento** dell'URL (dopo `#`), che il
browser non invia mai al server: questo sito non riceve né registra nulla di
quelle partite.
