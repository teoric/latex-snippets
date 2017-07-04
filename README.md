# Some LaTeX Snippets for Emacs [YaSnippet](http://joaotavora.github.io/yasnippet/)

## Citation
- `autocite \autocite` <kbd>ct</kbd>
- `textcite \textcite` <kbd>ct</kbd>


## Sectioning

labels generated with `clean-label`

```elisp
(defun clean-label (str)
  "Prepare STR to be usable as label."
  (replace-regexp-in-string
   "[^[:ascii:]]" ""
   (replace-regexp-in-string
    "[[:space:]]" "-"
    (ucs-normalize-NFD-string
     (replace-regexp-in-string
      "ä" "ae"
      (replace-regexp-in-string
       "ö" "oe"
       (replace-regexp-in-string
        "ü" "ue"
        (replace-regexp-in-string
         "ß" "ss"
        (replace-regexp-in-string
         "ł" "l"
         (downcase str))))))))))
```

- `chapter` <kbd>chap</kbd>
- `section` <kbd>sec</kbd>
- `subsec`  <kbd>ssec</kbd>
- `subsubsec` <kbd>ssub</kbd>

## Sectioning + Beamer Frame

- `frame-chapter` <kbd>chapf</kbd>
- `frame-section` <kbd>secf</kbd>
- `frame-subsec`  <kbd>ssecf</kbd>


## (OLD)

- `slide` for [pdfslide](https://www.ctan.org/pkg/pdfslide)
  and [ifmslide](https://www.ctan.org/pkg/ifmslide) <kbd>slide</kbd>

# Fonts
- `emph` <kbd>em</kbd>
- `textbf` <kbd>bf</kbd>
- `textit` <kbd>it</kbd>
- `textsc` <kbd>sc</kbd>
- `textsf` <kbd>tsf</kbd>

