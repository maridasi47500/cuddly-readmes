# 🎻 Ghost Play

**Ghost Play** est un projet musical basé sur [LilyPond](http://lilypond.org),
dédié à la composition de mélodies pour violon enrichies d'indications
techniques précises : coups d'archet, doigtés, cordes, positions sur le
manche, et nuances stylistiques. Il permet de générer des partitions
expressives dans les styles français, italien, allemand ou russe.

---

## 🎼 Fonctionnalités

Ghost Play permet d'ajouter automatiquement ou manuellement :

- 🎯 **Doigté** (`\finger`): numéros de doigt pour chaque note
- 🧵 **Corde** (`\stringNumber`): indication de la corde jouée
- 📍 **Position sur le manche** : annotation textuelle (`\markup`) ou
graphique
- 🏹 **Coups d’archet** :
  - `\upbow`, `\downbow`
  - `\wholeBow`, `\halfBow`, `\middleBow`
  - `\frosch`, `\spitze` (extrémités de l’archet)
- 🎶 **Articulations** :
  - `\slur`, `\spiccato`, `\tremolo`, `\glissando`
- 🌍 **Style culturel** :
  - Mélodies inspirées des traditions **française**, **italienne**,
**allemande** ou **russe**

---

## 🛠 Exemple de code LilyPond

```lilypond
\version "2.24.2"

violinMelody = \relative c'' {
  \clef treble
  \key d \minor
  \time 4/4

  \once \override TextScript.self-alignment-X = #LEFT
  d4^\markup { 1ère position, corde A, doigt 1 }^\upbow^\frosch
  f^\markup { doigt 3 }^\downbow^\middleBow
  a^\markup { corde E, doigt 1 }^\spiccato
  bes^\markup { glissando vers do }^\glissando^\spitze

  \slurUp
  d( f a bes)

  \repeat tremolo 4 { a16^\tremolo }
}

\score {
  \new Staff {
    \violinMelody
  }
  \layout { }
}
