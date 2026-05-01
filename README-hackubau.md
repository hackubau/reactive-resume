# Come fare il cv con reactive resume

## Installazione

```bash
git clone https://github.com/hackubau/reactive-resume.git #fork di https://github.com/amruthpillai/reactive-resume
cp .env.example .env
docker compose up -d
open localhost:3000
```

### MCP per AI
1) Entrare nel tool
2) SignIn con email
3) Creare api key
4) Setup MCP su Opencode
```jsonc
  "mcp": {
    "reactive-resume": {
      "type": "remote",
      "url": "http://localhost:3000/mcp",
      "headers": {
        "x-api-key": "EJPkxLHXxNLVtNOflmRycQjHEoHKajXsrHJTiysPkvTvUSZtnRATzxisCvBiqXBP"
      }
    }
  }
```

## Procedimento seguito
1) Gemini: guarda il mio cv, trasformalo in html e sistema questo e quest'altro
2) Scarica html > opencode con opus 4.7 > usalo per farti il cv tramite MCP, esempio mia conversazione:
    3) prompt 1: Prendi il mio CV @workspace/cv2.html ed utilizza mcp reactive resume per creare la prima versione di CV
    4) sistemazioncine a mano
    5) prompt 2: Ho sistemato il template. Ora prendi però il nuovo contenuto, chiamato @workspace/cv-super-bello.html , voglio che il cv rispetti alla PERFEZIONE TUTTO il suo contenuto. NON CAMBIARE PAROLE/FRASI e non dimenticarti sezioni. E' IMPORTANTISSIMO che ti impegni al MASSIMO! (come me che mi chiamo marco massimo ahaha)