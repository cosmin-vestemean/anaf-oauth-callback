# ANAF OAuth Callback

Mini callback public pentru OAuth ANAF. Se publica pe GitHub Pages si nu contine secrete.

## Callback URL pentru ANAF

Dupa publicarea cu GitHub Pages, foloseste in portalul ANAF URL-ul:

```text
https://<user>.github.io/anaf-oauth-callback/
```

Inlocuieste `<user>` cu utilizatorul sau organizatia GitHub.

## Flux

1. ANAF redirectioneaza browserul catre acest URL cu `?code=...`.
2. Pagina afiseaza codul OAuth si ofera buton de copiere.
3. Codul se lipeste in aplicatia locala ANAF Local.
4. Aplicatia locala face schimbul `code -> token` folosind `client_secret` din `.env`.

Nu pune `Client Secret` in acest repo.
