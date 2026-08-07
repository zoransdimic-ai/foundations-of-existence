# Poglavlje 10: Sprega (coupling) — logičko-matematičko modelovanje

*Sastavljeno iz razgovora "Logičko-matematičko modelovanje sprege i interakcije" (21.06.2026).*

---

## 10.1 Tri slike, jedna struktura

Polazna zapažanja: najjednostavnija logička sprega je konjunkcija ($a\ \text{AND}\ b$) — kada sprega postoji, rezultat je 1, kada ne postoji, 0. Najjednostavnija skupovna sprega je presek skupova — kada sprega postoji, presek nije prazan. Najjednostavnija aritmetička sprega je proizvod $a\cdot b$ — kada je rezultat 0, nema sprege; kada je rezultat konstanta, sprega je najjednostavnija.

Ova tri "paralelna" primera nisu tri analogije — to je **jedna ista struktura** posmatrana kroz tri sočiva. Karika koja ih spaja je indikatorska (karakteristična) funkcija skupa: ako se skupu pridruži funkcija koja daje 1 za članove i 0 za nečlanove, tada je

$$\chi_{A\cap B}(x) = \chi_A(x)\cdot\chi_B(x)$$

— presek skupova je tačno množenje njihovih indikatorskih funkcija. Na skupu vrednosti $\{0,1\}$, množenje se poklapa sa konjunkcijom ($1\cdot1=1$, sve ostalo 0 — istinitosna tablica za AND). Logika je, dakle, dvovrednosna verzija; skupovi su ista stvar podignuta na članstvo; aritmetika je njena neprekidna ekstenzija. (U viševrednosnoj/fuzzy logici, ta neprekidna ekstenzija konjunkcije zove se *t-norma*, i proizvod $a\cdot b$ na $[0,1]$ je jedna od tri fundamentalne, tzv. *product t-norm*.)

## 10.2 Kada sprega uopšte postoji: mešoviti izvod

Trijada "nema sprege / najjednostavnija sprega / složena sprega" može se učiniti potpuno preciznom preko **separabilnosti**, odnosno mešovitog (drugog parcijalnog) izvoda. Za funkciju dve promenljive $f(a,b)$, kriterijum glasi:

$$\frac{\partial^2f}{\partial a\,\partial b} \overset{?}{=} 0$$

- $f=a+b$: mešoviti izvod je $0$. Promenljive su nezavisne, razdvojive — **nema sprege**. Sabiranje samo stavlja stvari jednu pored druge.
- $f=a\cdot b$: mešoviti izvod je $1$, konstanta različita od nule — **najmanja moguća neseparabilna funkcija**, monom najnižeg stepena čiji mešoviti izvod ne iščezava. U sasvim preciznom smislu, ovo je "najjednostavnija sprega".
- $f=a^2b$, $e^{ab}$, itd.: mešoviti izvod je sam promenljiva funkcija — sprega koja se menja od tačke do tačke, "komplikovanija".

Vredi razdvojiti dva nivoa: "sprežna *funkcija*" ($a\cdot b$) je najjednostavnija po kriterijumu mešovitog izvoda; "sprežni *zakon*" ($a\cdot b=k$, nivo-kriva/hiperbola) je posebna tvrdnja o *vrednosti* tog proizvoda. Oba su validna i uklapaju se: najjednostavnija sprežna funkcija generiše najjednostavniji sprežni zakon.

## 10.3 Zašto baš ovaj oblik zakona vlada fizikom

Nije slučajno što fundamentalni odnosi u FOUNDATIONS pristupu — a i van njega — imaju baš oblik "proizvod dve veličine jednak univerzalnoj konstanti":

- $E\cdot T = h$ (Poglavlje 2)
- $V^2\epsilon\mu = 1$, odnosno $V=1/\sqrt{\epsilon\mu}$ (Poglavlje 1)
- Bojl-Mariotov zakon, $pV=\text{const}$
- Hajzenbergova relacija neodređenosti, $\Delta x\,\Delta p \gtrsim \hbar/2$

Sve su to iskazi oblika "sprega između ove dve veličine je najprostija moguća — njihov proizvod je univerzalna konstanta". Recipročni zakon (kad jedno raste, drugo opada tako da proizvod ostaje invarijantan) jeste najkruća, najprostija uzajamna veza koja uopšte postoji.

Zašto baš proizvod, a ne na primer $\min(a,b)$ — koji je takođe validna neprekidna ekstenzija konjunkcije? Zato što je $\min(a,b)$ **neglatka** funkcija (ima "lom" na dijagonali $a=b$), dok je $a\cdot b$ analitička, glatka svuda. Za teoriju koja počiva na pretpostavci savršeno glatkog kontinuuma (Poglavlje 1), množenje je prirodan izbor upravo zato što je glatko produženje konjunkcije. To nije estetska sitnica — to je doslednost sa temeljnom pretpostavkom cele knjige.

## 10.4 Šta ovoj slici ne pripada: uslovljenost

Jedina prava korekcija ove slike tiče se reč-grozda *sprega, interakcija, prožimanje, uslovljenost* — ovaj grozd nije homogen. Prve tri su **simetrične**: $a\cdot b=b\cdot a$, $A\cap B=B\cap A$, AND je komutativan — savršeno se slažu sa proizvodom/presekom/konjunkcijom.

Ali *uslovljenost* je, u opštem slučaju, **asimetrična** i usmerena: "ako $a$, onda $b$" nije isto što i obrnuto. Njen logički dom je implikacija ($a\to b$), a u aritmetici — funkcionalna zavisnost $b=f(a)$. Simetrična operacija po konstrukciji ne može da nosi usmerenu uslovljenost.

Poseban slučaj vredi izdvojiti: kada je sama sprega proizvod, $x\cdot y=h$, tada je $y=h/x$ *i* $x=h/y$ — uslovljenost postoji, ali je komutativna. Logički pandan tome nije implikacija, već **ekvivalencija**:

$$(a\leftrightarrow b) \equiv (a\to b)\wedge(b\to a)$$

— konjunkcija (ne disjunkcija!) dve implikacije: "važi i u jednom i u drugom smeru istovremeno". (Disjunkcija $(a\to b)\vee(b\to a)$ je, u klasičnoj logici, tautologija — uvek tačna, za svaki par — pa uopšte ne bi mogla da uhvati suštinu uzajamnog određenja.) Kad je sprega proizvod, svaka veličina jednoznačno i ravnopravno određuje drugu — to je ekvivalencija, ne implikacija.

## 10.5 Dve poštene ograde

Tvrdnja "proizvod je nula ⟺ jedan činilac odsutan" tačna je u $\mathbb{R}$ (nema delitelja nule), pa za realnovrednosni kontinuum ovog modela važi bez ograde. U prstenima sa deliteljima nule (npr. $\mathbb{Z}/6\mathbb{Z}$, matrice) može biti $a\cdot b=0$ uz oba činioca različita od nule — "skrivena" poništavajuća sprega uprkos prisustvu oba. Za $\epsilon,\mu,E,T$ ovo nije problem, ali je vredno znati granicu tvrdnje.

---

*Sledeće poglavlje: **Filozofske digresije** — Gabrijelov rog i pitanje beskonačne površine sa konačnom zapreminom, kao vežba u razlikovanju matematičke idealizacije od fizičke realnosti.*
