# Some LaTeX Snippets for Emacs [YaSnippet](http://joaotavora.github.io/yasnippet/)

## Citation
- `autocite` <kbd>ct</kbd>
- `fullcite` <kbd>ct</kbd>
- `parencite` <kbd>ct</kbd>
- `textcite` <kbd>ct</kbd>


## Sectioning

labels generated with `clean-label`

```elisp
(defun clean-label (str)
  "Prepare STR to be usable as (La)TeX label."
  ;; replace spaces by dash
  (replace-regexp-in-string
   "[[:space:]]" "-"
   ;; remove rest, e.g., remaining accents
   (replace-regexp-in-string
    "[^[:ascii:]]" ""
    ;; decompose to get rid of accents
    (ucs-normalize-NFD-string
     ;; treat special characters (mostly for German)
     (replace-regexp-in-string
      "æ" "ae"
      (replace-regexp-in-string
       "ø" "oe"
       (replace-regexp-in-string
        "œ" "oe"
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
             (downcase str)))))))))))))
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

