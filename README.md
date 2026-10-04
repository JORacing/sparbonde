# Spar Bonde

Et multiplayer-kortspil i browseren for 2–8 spillere: dansk Sorteper med almindelige kort. Det virker på Android, iPhone og PC via et link. Der er ingen app store, ingen server og det koster 0 kr.

## Spillet

- Der spilles med 51 kort, fordi klør bonde er fjernet.
- Et par er to kort med samme værdi og samme farve (rød/sort). Derfor kan spar bonde aldrig parres.
- Par smides automatisk, når kortene er givet, og efter hvert træk.
- På skift trækker man blindt et kort fra den næste spiller, der stadig er med.
- Den, der løber tør for kort, er ude. Den sidste med spar bonde har tabt.

## Sådan spiller I

1. **Opret rum:** Skriv dit navn og tryk "Opret nyt rum". Du er nu vært.
2. **Del linket:** Send linket (siden + `#KODE`) eller den 4-bogstavs kode til dine venner.
3. **Deltag:** Vennerne åbner linket, skriver deres navn og trykker "Deltag". Uden link kan man skrive koden i stedet.
4. Værten trykker "Start spil", når alle er med.

**Alene:** Tryk "🤖 Prøv mod 3 computere" på forsiden for at spille mod tre computere med det samme. Det kræver hverken rum eller netværk. I lobbyen kan værten også fylde op med "Tilføj computer". Computerne trækker et tilfældigt kort, når det er deres tur.

## Arkitektur

- Én selvstændig `index.html` (HTML/CSS/vanilla JS), hostet på GitHub Pages.
- Multiplayer kører peer-to-peer via WebRTC med [PeerJS](https://peerjs.com/), som bruger PeerJS' gratis signaling-server til at forbinde spillerne.
- Den, der opretter rummet, er vært. Spillogikken kører kun i værtens browser, og hver spiller får kun sin egen hånd at se.

## Kendte begrænsninger

- Værten skal holde siden åben, så længe der spilles.
- Mister en spiller forbindelsen midt i et spil, må værten trykke "Nyt spil".

## Kommer senere

- **Jerlev:** en lokal variant. Reglerne kommer senere.
