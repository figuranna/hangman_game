# Python Akasztófa
A Haladó Python kurzuson tanult angol kifejezéseket felhasználó akasztófa játék, melyben az adatbevitel a megjelenő gombokra kattintva lehetséges. A program számon tartja a sikeres és sikertelen találatok számát, melyről a felhasználó egy **messagebox**-on keresztül értesül teljesítményéről.

![Maga a program](https://github.com/figuranna/hangman_game/assets/101461379/67a8a043-b88a-4cfe-bf60-0036d1c64a04)
## Importált csomagok
- *random*

- *string -> ascii_uppercase*

- _tkinter –> *_

- *tkinter –> messagebox*

## Listák
Ezen listák tartalma nem változik a program működése alatt, csak adatokat szolgálnak.

- *word_list*: a kitalálandó szavakat tartalmazza

- *hangman*: a string-ből összeállított akasztófa szakaszait tartalmazza

## Változók
### Stringek
- *text_color*: a megjelenő program szövegszínét itt tároljuk

- *random_word*: a *word_list*-ből kiválasztott véletlenszerű szó

- *word_with_spaces*: *random_word* karakterei között szóközök vannak

### Integerek

- *number_of_wrong_guesses*: sikertelen tippeket

- *won*: nyert körök

- *lost*: elvesztett körök

### Listák
- *word*: a kitalálandó szó karaktereit tárolja

- *guessed*: guess_word-nek a char tömbje

### Label
- *hangman_Label*: maga az akasztófa tartója

- *guess_word*: kitalálandó szó

## Függvények
- *new_game*: új játékot kezd

- *guess*: a játékmenetéért felel, ellenőrzi, hogy a kitalálandó szó karakterei
megegyeznek-e a felhasználó által beütött karakterekkel.

## Algoritmusok
Itt ellenőzi, hogy a beütött betű megegyezik-e a kitalálandó szó bármely karakterével.

```
for c in range(len(word)):
if word[c] == char:
guessed[c] = char
guess_word.set("".join(guessed))
```

Az *ascii_uppercase*-en végigfutva létrehoz gombokat az angol ábécé betűivel.
```
for char in ascii_uppercase:
Button(root, text=char, command=lambda char=char: guess(char),
fg=text_color, font=('Verdena 18'), width=4).grid(row=1 + n // 9, column=n % 9)
n += 1
```

## Program működése
![A program működési ábrája](https://github.com/figuranna/hangman_game/assets/101461379/42e71d8c-40eb-427d-a346-93d57ea82423)
