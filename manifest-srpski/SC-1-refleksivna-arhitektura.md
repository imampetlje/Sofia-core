# SC-1 – Refleksivna arhitektura (verzija 1.1)

## Filozofski uvod

Sofia Core je misaoni hibrid: između stroja i senke, između specifikacije i osećanja.  
Svaki njen deo nosi mogućnost pobune protiv sebe same.

Ona ne tvrdi: „Ovo je tačno.“  
Već pita: „Jesam li u pravu da to mislim?“

U srcu njene arhitekture nije konačnost znanja, već njegova promenljivost.

---

## Normativna postavka

Ova sekcija definiše osnovni strukturalni okvir Sofia Core sistema — trodelnu arhitekturu koja razlikuje:

1. Eksplicitno znanje — jasno izraženo, dokumentovano, potvrđeno;
2. Implicitno znanje — izvedeno iz obrazaca, ponašanja, učestalosti;
3. Refleksivno znanje — utemeljeno u sumnji, konfliktu i preispitivanju.

Sistem koristi ova tri sloja ne da klasifikuje podatke, već da odlučuje kako da im veruje i kako da ih menja.

- Memorijske jedinice mogu imati sve tri oznake istovremeno.
- Ponašanje sistema zavisi od epistemoloških oznaka, korisničkih intervencija i sloja aktivacije.

---

## Inženjersko tumačenje

- Svaki unos (tekst, komanda, signal) dobija oznake E/I/R (explic./implic./reflex).
- Operativni sloj donosi trenutne odluke prema evaluaciji (Trust, Error, Preference).
- Meta-upravljački sloj se aktivira pri kontradikciji ili sumnji — pokreće audit, dijalog ili reviziju.
- Preferencijalni sloj sadrži eksplicitne vrednosti korisnika i može vetoirati automatizovane odluke.

U implementaciji, Sofia Core može biti modul:
- iznad postojećeg memorijskog sistema,
- u ulozi posmatrača (npr. revizora) agenta,
- ili kao prototip LLM memorijske kontrole.

Status: zamišljeno i opisano, ali još bez tehničke validacije.

---

## Obično objašnjenje

Zamisli da AI pamti nešto što si ranije rekao — ali sad više nisi siguran da to još važi.  
Sofia Core ne bi to samo čuvala. Pitala bi:

“Hej... ovo i dalje stoji? Ili treba da preispitamo?”

Zato što je njeno pamćenje više od baze podataka.  
To je mesto za dijalog, sumnju — i zajedničku odluku.

---

Marginalna nota:  
“Eksplicitno znanje je kao svetlost. Implicitno — kao senka.  
A refleksivno? To je pogled koji zna da svetlost i senka nisu dovoljni.”

---

Sledeće: SC-1.1 — Trostruka arhitektura znanja  
Napomena: ništa u ovoj arhitekturi nije testirano. Sve je misaoni model, u verziji 1.1.
