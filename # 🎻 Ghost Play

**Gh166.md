# 🎻 Ghost Play

**Ghost Play** est un outil de composition musicale en langage [LilyPond](
https://lilypond.org/) qui permet d'écrire des mélodies expressives pour
instruments à cordes, avec des annotations techniques avancées pour
l'interprétation.

## ✨ Fonctionnalités

Ghost Play permet d'ajouter automatiquement ou manuellement les éléments
suivants à une partition :

- 🎼 **Mélodie** en notation LilyPond
- 🏹 **Upbow / Downbow** (`\upbow`, `\downbow`)
- 🖐️ **Doigté** (`\finger`)
- 🎻 **Corde jouée** (`\string`)
- 📍 **Position sur le manche** (ex: 1ère, 3ème position)
- 🌀 **Liaisons (slurs)** (`( ... )`)
- 🪶 **Type d'archet** :
  - `whole bow`
  - `half bow`
  - `middle`
  - `Frosch` (talon)
  - `Spitze` (pointe)

## 🛠️ Exemple de syntaxe LilyPond

```lilypond
\version "2.24.1"

violin = \relative c' {
  \clef treble
  \key d \major
  \time 4/4

  \set Staff.instrumentName = #"Violin"

  d4^\markup { \column { "1ère position" "corde A" "doigt 1" "whole bow" }
}^\downbow (
  e^\markup { "doigt 2" }^\upbow
  f^\markup { "doigt 3" "middle" }^\downbow
  g^\markup { "doigt 4" "Spitze" }^\upbow )
}
\score {
  \new Staff \violin
}
