# Viure amb distonia · Informació, orientació i acompanyament

Web estàtica (HTML, CSS i JavaScript, sense servidor ni dades personals) feta per al Treball de Recerca de Batxillerat. Pensada per a persones amb distonia i per a qui les acompanya.

## Què conté

| Pàgina | Fitxer | Què fa |
|---|---|---|
| Inici | `index.html` | Portada amb accés a totes les seccions |
| Com et trobes? | `orientacio.html` | Qüestionari ramificat (33 preguntes, 13 finals) que dona una orientació |
| Registre diari | `registre.html` | Apuntar ànim, símptomes, dolor, cansament, estrès, son, zones afectades i notes; gràfic dels últims 30 dies; exportació a CSV |
| Sobre la distonia | `informacio.html` | Què és, tipus, símptomes, causes, diagnòstic, tractaments, emocions i fonts |
| Família i entorn | `entorn.html` | Consells per acompanyar i una targeta imprimible per explicar la distonia |
| Visita al metge | `visita.html` | Resum del registre i preguntes per al neuròleg, imprimible o en PDF |
| Recursos | `recursos.html` | Associació Distonia Catalunya, fonts mèdiques i telèfons d'ajuda (112, 024, 061) |

Fitxers de suport:

| Fitxer | Què conté |
|---|---|
| `style.css` | Tot el disseny (inclou mode fosc automàtic i mode «lletra gran») |
| `common.js` | El menú i el peu de totes les pàgines. Per afegir una pàgina al menú, edita la llista `PAGINES` |
| `lib.js` | Les escales del registre (`ESCALES`), les zones (`ZONES`) i els càlculs del resum |
| `arbre.js` | **Totes les preguntes, opcions i finals del qüestionari** |

## Com publicar-la a GitHub Pages

1. Crea un repositori **públic** a [github.com](https://github.com).
2. Clica **Add file → Upload files** i arrossega **tots els fitxers** (`.html`, `.css`, `.js` i aquest `README.md`) a l'arrel del repositori. Si ja n'hi ha de pujats amb el mateix nom, es substitueixen. Clica **Commit changes**.
3. Ves a **Settings → Pages**. A **Source** tria **Deploy from a branch**, a **Branch** tria `main` i `/ (root)`, i clica **Save**.
4. Espera 1-2 minuts. L'adreça serà `https://EL_TEU_USUARI.github.io/NOM_DEL_REPOSITORI/`.

Cada cop que canviïs un fitxer i facis *Commit*, la web s'actualitza sola.

## Com editar el qüestionari

A `arbre.js`, cada pregunta és un node:

```js
A1: { t: "Com estàs avui?", o: [
  ["Bé", "A2"],
  ["Malament", "A9"]
]},
```

- `A1` és el codi de la pregunta; `t`, el text; `o`, les opcions `["text de l'opció", "codi on porta"]`.
- Si el codi comença per `F` (F1, F2...), porta a un **final**, que es defineix a `FINALS`.

## Sobre les dades

La web no té servidor. Tot el que s'apunta (qüestionari i registre diari) es guarda **només al navegador de cada persona** i es pot descarregar com a CSV. Per tant, **tu no reps les dades dels altres usuaris**. Si vols recollir dades de diverses persones per a l'anàlisi del TDR, demana'ls el CSV o afegeix un enllaç a un formulari, i avisa'ls sempre del que recolliràs.

## Avís

Aquesta web és divulgativa i orientativa i no substitueix un professional sanitari. En una urgència: 112. Línia d'atenció a la conducta suïcida: 024.
