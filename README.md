#  🚀 BEM WARS 🚀

by Annette Le Sage
version 1.0 (updated 3/12/23)

Star Wars Cards styled with scaleable CSS using BEM notation, OOCSS and SASS. The Language Galactic Basic has been used in the cards, which can be hovered over for a translation into English. Since Galactic-Basic font used uses Roman numbers, for a more interesting user experience, R2-D2 and C3-PO have been spelled out without numbers, as seen for C3-PO on the Star Wars website.

## Techonologies

This project demonstrates styles in CSS using Block__Element--modifier naming conventions, which have been developed further using SASS. The CSS examples are inlcuded in the assets/css directory and the sass examples are in the assets/sass directory. The final compiled version included in the html file is in the stylesheets directory.

## Block__Element--modifier

A "Block" is a standalone entity that is meaningful on its own. Examples used in this project include navbar, page and card. These are css classes and in the sass files they provide outer level nesting.

An "Element" is part of a block. An element has no meaning on its own. Examples in this project include card__header, navbar_item and page__heading. These use the double underscore __ to define themselves as children of their blocks. In the sass files they are nested directly inside the outer levels.

A "Modifier" changes - or modifies- a block or element's appearance or behaviour. Examples in this project include card__image--gold and card__heading--coconut. These use the double hyphen -- to define themselves as children of their elements. In the sass files they are nested directly inside the elements.

## Mixins and Extend

Mixins have been used to group some CSS declarations that are reused. The purpose of these has been primarily to enabling reuse colour schemes and border/shadow styling amoning elements.

The use of extend has enabled sharing of a set of CSS properties from one selector to another. In this project it has enabled the card headings to share properties with the card text.

## Usage

Since the language Galactic Basic has been used in the cards, which you might not be fluent in, you can hover over each card for a translation into English.