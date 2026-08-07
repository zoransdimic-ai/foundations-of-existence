# Koja je jednačina za brzinu prostiranja...

Ovaj fajl sadrži autentičan i potpun prepis razgovora o fizici talasa, brzini zvuka kroz različite medijume, dimenzionoj analizi gustine energije i akustici zategnute žice.

---

### Korisnik
Koja je jednačina za brzinu prostiranja zvuka kroz vodu (kroz tečnosti)? Isto pitanje, ali za prostiranje zvuka kroz čvrsta tela.

### Model
Brzina prostiranja zvuka kroz tečnosti (uključujući vodu) računa se preko modula stišljivosti i gustine tečnosti: 

$$c = \sqrt{\frac{K}{\rho}}$$

Kroz čvrsta tela, brzina longitudinalnih zvučnih talasa zavisi od Jangovog modula elastičnosti i gustine: 

$$c = \sqrt{\frac{E}{\rho}}$$

#### Brzina zvuka kroz tečnosti (Njutn-Laplasova jednačina)
Formula: 
$$c = \sqrt{\frac{K}{\rho}}$$

Oznake:
*   $c$ = brzina zvuka
*   $K$ = adijabatski modul stišljivosti (ili koeficijent elastične stišljivosti fluida)
*   $\rho$ = gustina tečnosti

Detalji: Tečnosti se opiru promeni zapremine, pa veća otpornost na stišljivost ($K$) povećava brzinu, dok veća gustina ($\rho$) usporava kretanje talasa.

#### Brzina zvuka kroz čvrsta tela
Formula (za longitudinalne talase kroz tanku šipku / 1D): 
$$c = \sqrt{\frac{E}{\rho}}$$

Oznake:
*   $c$ = brzina zvuka
*   $E$ = Jangov modul elastičnosti čvrstog tela
*   $\rho$ = gustina čvrstog tela

Detalji: U trodimenzionalnom neograničenom čvrstom medijumu formula je nešto složenija jer uključuje i smicajni (transverzalni) modul elastičnosti, ali osnovni oblik sa Jangovim modulom se koristi u standardnoj literaturi za šipke i jednodimenzionsko prostiranje. Čvrsta tela imaju znatno veće module elastičnosti od tečnosti, pa se kroz njih zvuk i najbrže prostire.

Da li želite da uradimo konkretan numerički primer izračunavanja brzine zvuka za vodu ili neko čvrsto telo poput čelika?

---

### Korisnik
A u gasovima?

### Model
Brzina prostiranja zvuka kroz gasove računa se pomoću formule: 

$$c = \sqrt{\frac{\gamma \cdot R \cdot T}{M}}$$

#### Brzina zvuka kroz gasove (Njutn-Laplasova jednačina)
Formula: 
$$c = \sqrt{\frac{\gamma \cdot p}{\rho}} = \sqrt{\frac{\gamma \cdot R \cdot T}{M}}$$

Oznake:
*   $c$ = brzina zvuka
*   $\gamma$ = adijabatski eksponent (za vazduh iznosi oko 1.4)
*   $p$ = pritisak gasa
*   $\rho$ = gustina gasa
*   $R$ = univerzalna gasna konstanta ($8.314 \, \text{J/(mol}\cdot\text{K)}$)
*   $T$ = apsolutna temperatura u Kelvinima (K)
*   $M$ = molarna masa gasa

#### Ključne zavisnosti
*   **Temperatura:** Brzina zvuka u gasovima najviše zavisi od temperature. Što je gas topliji, molekuli se brže kreću i zvuk se brže prenosi.
*   **Molarna masa:** Zvuk se prostire brže kroz lakše gasove (npr. helijum ili vodonik) nego kroz teže gasove (npr. kiseonik ili ugljen-dioksid) na istoj temperaturi.
*   **Pritisak:** Iz same formule se vidi da pritisak i gustina rastu proporcionalno, pa promena atmosferskog pritiska (pri konstantnoj temperaturi) zapravo ne utiče na brzinu zvuka.

Da li želite da izračunamo brzinu zvuka u vazduhu na nekoj konkretnoj temperaturi (npr. na 20°C)?

---

### Korisnik
Znači ... uvek imamo kvadratni koren odnosa ... gustine energije i gustine (mase)...

### Model
Da, to je odličan zaključak i sjajna fizikalna intuicija! Brzina zvuka u svim sredinama uvek ima isti fundamentalni oblik: kvadratni koren iz odnosa elastičnih svojstava (koja su dimenziono identična gustini energije) i inercije (gustine mase).

Evo kako se to precizno poklapa kroz dimenzionu analizu i fiziku:

#### 1. Dimenziona provera (Gustina energije)
Gustina energije je energija po jedinici zapremine:
$$\frac{\text{Džul}}{\text{metar}^{3}}=\frac{\text{N}\cdot \text{m}}{\text{m}^{3}}=\frac{\text{N}}{\text{m}^{2}}=\text{Paskal\ (Pa)}$$

To znači da gustina energije ima potpuno istu mernu jedinicu kao pritisak, Jangov modul elastičnosti ($E$) i modul stišljivosti ($K$).

#### 2. Kako se to primenjuje na formule?
*   U tečnostima: $c = \sqrt{\frac{K}{\rho}} \rightarrow \sqrt{\frac{\text{modul stišljivosti (Pa)}}{\text{gustina mase}}}$
*   U čvrstim telima: $c = \sqrt{\frac{E}{\rho}} \rightarrow \sqrt{\frac{\text{modul elastičnosti (Pa)}}{\text{gustina mase}}}$
*   U gasovima: $c = \sqrt{\frac{\gamma \cdot p}{\rho}} \rightarrow$ gde je $p$ pritisak (bilo statički ili dinamički, što je direktno zapreminska gustina kinetičke energije molekula gasa).

#### 3. Zašto je to tako?
Zvuk je mehanički talas. Da bi se prostirao, potrebna su dva faktora:
*   **Elastičnost (brojilac):** Sposobnost sredine da akumulira potencijalnu energiju i vrati se u prvobitno stanje (izvor sile koja "gura" talas napred).
*   **Inercija (imenilac):** Otpor sredine prema ubrzavanju (gustina mase koja usporava to "guranje").

Zato veća elastičnost (gustina energije) uvek ubrzava zvuk, a veća gustina mase ga usporava.

Želite li da pogledamo kako se iz ove opšte zakonitosti izvodi brzina zvuka na primeru zategnute žice, gde se umesto zapreminske koristi podužna gustina?

---

### Korisnik
Da :-)

### Model
Kod zategnute žice (jednodimenzionalnog sistema) važi potpuno ista logika, ali pošto nemamo zapreminu, posmatramo silu zatezanja kao izvor energije i podužnu gustinu kao tromost (inerciju).

Brzina prostiranja talasa duž zategnute žice računa se po formuli:
$$c=\sqrt{\frac{F}{\mu }}$$

Značenje oznaka:
*   $c$ = brzina prostiranja talasa duž žice
*   $F$ = sila zatezanja žice (izražena u Njutnima, N)
*   $\mu$ = podužna gustina žice (masa po jedinici dužine, $\frac{m}{L}$, izražena u $\frac{\text{kg}}{\text{m}}$)

#### Kako se ovo poklapa sa tvojom intuicijom?
Ako formu pomnožimo i gore i dole sa površinom poprečnog preseka žice ($S$), dobićemo vezu sa zapreminskim jedinicama:
*   **U brojiocu:** Sila podeljena sa površinom ($\frac{F}{S}$) je napon (pritisak), što je zapravo ponovo gustina energije (Pa).
*   **U imeniocu:** Podužna gustina podeljena sa površinom ($\frac{\mu}{S} = \frac{m}{L \cdot S}$) daje standardnu gustinu mase ($\rho$).

Tako se formula transformiše u:
$$c=\sqrt{\frac{\text{napon}}{\rho }}$$

Opet smo dobili isti fundamentalni odnos: kvadratni koren iz odnosa elastičnosti (energije) i inercije (mase). Što jače zategneš žicu (veća energija), talas putuje brže. Što je žica deblja i teža (veća inercija), talas putuje sporije.

Da li te zanima kako ova brzina zatezanja žice direktno određuje frekvenciju (visinu tona) koji čujemo kada trznemo žicu na gitari ili klaviru?

---

### Korisnik
Da :-)

### Model
Kada trzneš žicu na gitari ili klaviru, brzina talasa ($c$) koju smo upravo definisali direktno diktira visinu tona (frekvenciju $f$) preko osnovne formule za talase: $f = \frac{c}{\lambda}$, gde je $\lambda$ (lambda) talasna dužina.

Evo kako se to precizno dešava na instrumentu:

#### 1. Zarobljeni talas (Osnovni harmonik)
Kada je žica fiksirana na oba kraja (kod kobilice i čivije), talas se odbija od krajeva i formira takozvani stojeći talas.
Najduži i najjači talas koji tako može nastati ima dužinu koja je tačno dvostruko veća od dužine same žice ($L$).
Dakle, talasna dužina osnovnog tona je: $\lambda = 2L$.

#### 2. Glavna formula za frekvenciju žice
Kada ubacimo formulu za brzinu ($c = \sqrt{\frac{F}{\mu}}$) i talasnu dužinu ($\lambda = 2L$) u osnovnu jednačinu, dobijamo Mersenov zakon:
$$f=\frac{1}{2L}\sqrt{\frac{F}{\mu }}$$

#### Kako muzičari kontrolišu ovu fiziku?
Svaki muzičar nesvesno upravlja trima varijablama iz ove formule kako bi promenio visinu tona:
*   **Dužina žice ($L$):** Kada pritisneš prag na gitari, ti skraćuješ aktivni deo žice. Manje $L$ u imeniocu znači viša frekvencija (viši ton).
*   **Sila zatezanja ($F$):** Kada okrećeš čiviju da naštimuješ instrument, menjaš silu $F$. Jače zategnuta žica daje viši ton.
*   **Podužna gustina ($\mu$):** Zato su bas žice (npr. najdeblja E žica) namotane i teške. Veća masa po metru dužine ($\mu$) usporava talas, što daje dubok ton.

Da li želiš da izračunamo tačnu frekvenciju za neku konkretnu žicu (npr. ako znamo njenu dužinu i debljinu), ili te zanima kako ovi talasi sa žice prelaze u vazduh i postaju zvuk koji čujemo?

