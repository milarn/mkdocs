# Aktivere environment (IT)

## Når man skal slå på for å dokumentere:

Åpne cmd og skriv inn:

```
C:\Users\Martin>cd mkdocs
C:\Users\Martin\mkdocs>.\venv\Scripts\activate

(venv) C:\Users\Martin\mkdocs>code .
```

`Code .` åpner opp VSC

`.\venv\Scripts\activate` Aktiverer python environementet

Husk å starte mkdocs i Visual studio code terminal

`PS C:\Users\Martin\mkdcos> mkdocs serve`

`mkdocs serve` Starter da, og så kan du se live updates via local host


Dette er det du vil få opp i consolen:

```
PS C:\Users\Martin\mkdocs> mkdocs serve
INFO     -  Building documentation...
INFO     -  Cleaning site directory
INFO     -  Documentation built in 0.73 seconds
INFO     -  [00:28:58] Watching paths for changes: 'docs', 'mkdocs.yml'
INFO     -  [00:28:58] Serving on http://127.0.0.1:8000/
```