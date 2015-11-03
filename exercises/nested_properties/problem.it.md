# NESTED PROPERTIES

CSS has quite a few properties that are in “namespaces;” for instance, `font-family`, `font-size`, and `font-weight` are all in the `font` namespace. In CSS, if you want to set a bunch of properties in the same namespace, you have to type it out each time. Sass provides a shortcut for this: just write the namespace once, then nest each of the sub-properties within it. For example:

```scss
.funky {
  font: {
    family: fantasy;
    size: 30em;
    weight: bold;
  }
}
```

is compiled to:

```css
.funky {
  font-family: fantasy;
  font-size: 30em;
  font-weight: bold; }
```

The property namespace itself can also have a value. For example:

```scss
.funky {
  font: 20px/24px fantasy {
    weight: bold;
  }
}
```

is compiled to:

```css
.funky {
  font: 20px/24px fantasy;
    font-weight: bold;
}
```

# EXERCISE

Define a selector `.sassy`, and use nested properties to set `border-width` to '10px', `border-color` to 'red' and `border-radius` to '5px'.

--
## SUGGERIMENTI

Per creare un foglio di stile Sass (SCSS), crea un nuovo file con l'estensione `.scss` e comincia a scrivere in SCSS. Quando hai terminato, devi eseguire:

```sh
$ {appname} verify stylesheet.scss
```

per proseguire. Il tuo foglio di stile sarà verificato, un rapporto generato, e la lezione marcata come 'completa' se hai completato l'esercizio con successo.
