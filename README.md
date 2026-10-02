# Ventisette

Il codice di questo progetto è privato. Qui racconto cosa fa, come è costruito e come l'ho verificato.

## Cosa fa

È un'app per il telefono che aiuta chi lavora a controllare la propria busta paga e a capire il proprio contratto
nazionale (CCNL). Si sceglie il contratto e il livello, si indica da quando si è in azienda, e l'app calcola il fisso
lordo del mese con gli scatti di anzianità e la paga oraria.

Poi si copiano le cifre dalla busta: scatti, straordinari, trasferte, elemento perequativo. L'app le confronta voce per
voce con il contratto e dice quali tornano e quali vanno verificate, con la differenza in euro e cosa si può fare: chi
chiamare, cosa mostrare all'ufficio paghe. Il controllo si salva, si condivide o si stampa in PDF.

Ci sono anche un aiuto per capire se il livello in busta è quello giusto per il lavoro che si fa, un diario di ore e
trasferte e gli avvisi quando il contratto è scaduto o quando è già firmato un aumento.

## Come è costruito

Un motore di calcolo unico e un pacchetto di dati per ogni contratto. Ogni contratto ha la sua scheda con le fonti,
e da quei dati uno script genera il pacchetto che l'app carica. Aggiungere un contratto vuol dire aggiungere dati,
non riscrivere l'app. È pubblicata su Cloudflare.

## Come l'ho verificato

- 80 test sul motore di calcolo, con le cifre controllate a mano sul testo del contratto.
- 43 test sulle schermate, eseguiti con Playwright in un browser vero.

## Stato

Online in prova.
