# SC-1.1 – Trostruka arhitektura znanja

## Filozofski uvod

Znanje nije jedan sloj.  
Kao i ljudska intuicija, ono se gradi između onog što smo svesni da znamo, onog što naslutimo iz iskustva, i onog što propitujemo.

Sofia Core razlikuje tri oblika znanja — ne zbog klasifikacije, već zbog etike ponašanja prema njima.

---

## Normativna postavka

Sistem Sofia Core tretira memorijske jedinice kao višeslojne:  
- eksplicitni sloj: jasno izražene činjenice ili izjave, potvrđene ili unete direktno,
- implicitni sloj: izvedene informacije iz učestalosti, ponašanja ili heuristike,
- refleksivni sloj: označava elemente koji su bili predmet sumnje, konflikta ili korisničke revizije.

Svrha ovog modela nije arhiviranje, već operativna upotreba:
- eksplicitni sloj koristi se za odlučivanje,
- implicitni za predviđanje i pretpostavke,
- refleksivni za zaustavljanje automatizma i pokretanje provere.

---

## Inženjersko tumačenje

Svaka informacija u memoriji može sadržati više slojeva znanja, obeleženih kroz tzv. epistemološke tagove.

Primer oznaka:
- `"epistemic_status": { "explicit": true, "implicit": true, "reflective": false }`

Operativna logika koristi ove oznake:
- ako postoji refleksivna oznaka → aktiviraj meta-upravljački sloj,
- ako postoji implicitno bez eksplicitnog → dodaj marginu nepoverenja,
- ako postoji samo eksplicitno → koristi kao osnov za heuristiku.

Napomena: ovo je misaoni model — u realnim implementacijama, slojevi bi bili predstavljeni metapodacima u memorijskim jedinicama.

---

## Obično objašnjenje

Zamisli da AI sistem ima tri "glasa pamćenja":
- prvi kaže: „Ovo znam, korisnik mi je rekao.“
- drugi kaže: „Pretpostavljam to jer se stalno ponavlja.“
- treći kaže: „Ali... jesmo li proverili to ranije?“

Sofia Core pamti ne samo informaciju, već i način na koji ju je stekla.  
I tretira ih drugačije — jer ne značenje, već poreklo određuje kako će se nešto koristiti.

---

Marginalna nota:  
„Znanje koje se ne razlikuje po poreklu, ne zna kad da zastane.“
