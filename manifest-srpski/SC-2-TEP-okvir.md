# SC-2 – TEP okvir (Poverenje, Greška, Preferencija)

## Filozofski uvod

Sofia Core ne tretira znanje kao homogeni entitet, već kao strukturu u kojoj različiti oblici znanja – eksplicitni, implicitni i refleksivni – koegzistiraju i međusobno utiču.  
Da bi sistem mogao da odlučuje pod uslovima nesigurnosti, potrebno je da koristi skup evaluacionih mehanizama. Tu nastaje TEP okvir: **Trust (T)**, **Error (E)**, **Preference (P)**.

Umesto pitanja „da li je nešto tačno?“, TEP pita:  
- **Koliko verujem u ovu informaciju?**  
- **Koliko puta se pokazala kao nepouzdana?**  
- **Koliko se podudara sa vrednostima korisnika?**

---

## Normativna postavka

TEP ne pokušava da izmeri istinu — već operativnu **relevantnost znanja** u određenom kontekstu.

- **T (Trust / Poverenje):** utemeljeno na poreklu informacije, učestalosti potvrda, reputaciji izvora.
- **E (Error / Greška):** beleži broj i intenzitet prethodnih grešaka u vezi sa tom memorijskom jedinicom.
- **P (Preference / Preferencija):** meri u kojoj meri se sadržaj podudara sa korisnikovim vrednostima, emocijama ili eksplicitnim prioritetima.

TEP okvir omogućava:
- evaluaciju memorijske jedinice pre upotrebe,
- automatsku suspenziju u slučaju niskog T ili visokog E,
- korisničko pravo veta ako je P izrazito nizak.

---

## Inženjersko tumačenje

Sistem može koristiti formulu:

```
RELEVANCE_SCORE = T × E × P
```

Gde su sve tri komponente decimalne vrednosti između 0 i 1.

Primer:
```json
{
  "memory_id": "A234",
  "T": 0.91,
  "E": 0.88,
  "P": 0.42,
  "RELEVANCE_SCORE": 0.34
}
```

Na osnovu praga, sistem odlučuje:
- RS < 0.30 → ignoriši ili traži dodatni kontekst
- RS 0.30 – 0.65 → predloži uz oprez
- RS > 0.65 → koristi samouvereno, ali beleži reakciju

* Buduće verzije: uključiti mehanizam za konflikt između slojeva (npr. kada implicitna heuristika osporava eksplicitnu tvrdnju).

---

## Obično objašnjenje

Zamisli da AI pokušava da ti da savet. Ali se zaustavi. Kaže:

> „Ova informacija je tehnički tačna (T), ali ti se ranije nije dopala (P). Takođe, u prošlosti se pokazala kao nepouzdana (E). Možda bi trebalo da pitam pre nego što predložim.“

To je TEP — sistem koji ne pita „šta znaš?“, već „da li si siguran da to znaš — i da to vredi sada reći?“

---

Marginalna nota:  
„Znanje bez konteksta je pamćenje bez duše. TEP uči kako da pamćenje služi – a ne vlada.“  
