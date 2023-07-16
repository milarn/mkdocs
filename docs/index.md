# Lund.store Dokumentasjon

Dette er test av MKdocs og potensialet for dokumentasjons side.

## Code Annotation examples

### Codeblocks

Eksempel på kode: `Her skriver vi inn koden vi har` Så får vi litt mer oversiktlig kode

### plain codeblock

a plain codeblock:

```
Her er litt kode for funksjon
def myfunction()
// her skriver du kommentar om koden
```

### Code for a specific language

Some more code with the `py` at the start:

``` py
import tensorflow as tf
def whatever()
```

### Med en tittel

``` py title="bubble_sort.py"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```


## Icons and emojis

:smile:

:fontawesome-regular-face-laugh-wink:

:fontawesome-brands-twitter:{ .twitter }

:octicons-heart-fill-24:{ .heart }