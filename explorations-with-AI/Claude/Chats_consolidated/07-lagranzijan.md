# Poglavlje 7: Lagranžijan — demistifikacija

*Sastavljeno iz razgovora "Light Deflection in Gravitational Field" (22.07.2025) i "Time perception in young children" (21.09.2025) — artefakt izveden direktno iz F=dp/dt i F=dE/ds, bez pozivanja na princip najmanje akcije kao polaznu tačku.*

---

## Problem sa Tradicionalnim Pristupom

Standardno izvođenje Lagranžijanske mehanike oslanja se na:
- **Princip najmanje akcije** (pojavljuje se kao matematička magija)
- **Varijacioni račun** (apstraktan matematički okvir)
- **Kružno rezonovanje**: Biramo L = T - V jer "funkcioniše"

## Prirodan, Fizički Pristup

### Polazak od Elementarnih Zapažanja

**Eksperiment sa Kolicima:**
- Kolica u mirovanju → guranje → dobijaju brzinu
- Jače guranje → veće ubrzanje
- Sila stvara promenu brzine u vremenu

**Prirodne Definicije:**
1. **Sila iz ubrzanja**: F = ma = m(dv/dt)
2. **Impuls**: p = mv (količina kretanja)
3. **Sila iz impulsa**: F = dp/dt

### Otkrivanje Energije

**Lajbnicovo zapažanje**: Dužina zaustavljanja ∝ v²

Iz F = ma i osnovne kinematike:
$$F = m\frac{dv}{dt} = mv\frac{dv}{ds}$$

Integraljenjem duž putanje:
$$\int F \, ds = \int mv \, dv = \frac{1}{2}mv^2 = E$$

Dakle: **F = dE/ds**

## Fundamentalno Izvođenje

### Dve Ekvivalentne Definicije Sile

Sada imamo dva osnovna izraza za silu:
$$F = \frac{dp}{dt} \quad \text{i} \quad F = \frac{dE}{ds}$$

### Fizička Argumentacija za ∂E_k/∂h

**Ključni uvid**: Kada se telo kreće u gravitacionom polju:
- Visina h i kinetička energija E_k se istovremeno menjaju
- Kroz konzervaciju energije: E_total = E_k + E_p = konstanta
- Za slobodni pad: v² = 2g(h₀ - h)
- Dakle: E_k = mg(h₀ - h)
- **Rezultat**: ∂E_k/∂h = -mg

### Matematička Transformacija

Pošto oba izraza jednaka su sili:
$$\frac{dp}{dt} = \frac{dE}{ds}$$

**Ključni uvid**: Impuls se može zapisati kao:
$$p = \frac{dE}{dv} = \frac{dE}{d\dot{s}}$$

Dakle:
$$\frac{dp}{dt} = \frac{d}{dt}\left(\frac{dE}{d\dot{s}}\right)$$

### Nastajanje Lagranžijanove Jednačine

Kombinovanjem naših rezultata:
$$\frac{d}{dt}\left(\frac{dE}{d\dot{s}}\right) = \frac{dE}{ds}$$

Za svaki koordinatni pravac:
$$\frac{d}{dt}\left(\frac{\partial E}{\partial \dot{s}}\right) = \frac{\partial E}{\partial s}$$

## Precizno Matematično Izvođenje kroz Generalisane Koordinate

### Transformacija Rada

Rad u Karterovim koordinatama:
$$dW = f_x dx + f_y dy + f_z dz$$

Za sistem sa dva stepena slobode (X, Y):
$$dW = F_X dX + F_Y dY$$

### Koordinatne Transformacije

$$dx = \frac{\partial x}{\partial X} dX + \frac{\partial x}{\partial Y} dY$$
$$dy = \frac{\partial y}{\partial X} dX + \frac{\partial y}{\partial Y} dY$$
$$dz = \frac{\partial z}{\partial X} dX + \frac{\partial z}{\partial Y} dY$$

### Generalisane Sile

$$F_X = f_x \frac{\partial x}{\partial X} + f_y \frac{\partial y}{\partial X} + f_z \frac{\partial z}{\partial X}$$

Koristeći Newton-ove zakone f_x = m(dẋ/dt):

$$F_X = m \left(\frac{d\dot{x}}{dt} \frac{\partial x}{\partial X} + \frac{d\dot{y}}{dt} \frac{\partial y}{\partial X} + \frac{d\dot{z}}{dt} \frac{\partial z}{\partial X}\right)$$

### Ključna Matematička Manipulacija

Koristeći pravilo proizvoda i vezu ∂x/∂X = ∂ẋ/∂Ẋ:

$$F_X = \frac{d}{dt} \left(\frac{\partial T}{\partial \dot{X}}\right) - \frac{\partial T}{\partial X}$$

gde je T = ½m(ẋ² + ẏ² + ż²) kinetička energija.

### Uključivanje Potencijalne Energije

Iz konzervacije energije: dT = -dV, dakle:
- F_X = -∂V/∂X (definicija konzervativnih sila)
- Kombinovanjem: -∂V/∂X = d/dt(∂T/∂Ẋ) - ∂T/∂X
- Pregrupisavanjem: ∂(T-V)/∂X = d/dt(∂T/∂Ẋ)

### Finalna Forma

Definišući L = T - V:
$$\frac{\partial L}{\partial X} = \frac{d}{dt}\left(\frac{\partial L}{\partial \dot{X}}\right)$$

**Ovo su Euler-Lagrange-ove jednačine!**

## Fizički Značaj

### Zašto je ovo Izvođenje Fundamentalno

1. **Bez misterioznih principa**: Izgrađeno iz posmatrajnih kolica
2. **Bez apstraktne matematike**: Koristi samo osnovni kalkulus
3. **Fizička transparentnost**: Svaki korak ima jasno fizičko značenje
4. **Prirodno nastajanje**: Lagranžijanske jednačine se neizbežno javljaju iz definicija sile

### Zakoni Konzervacije su Primarni

- **Akcija-reakcija** je posledica konzervacije energije i impulsa
- **Matematika proistače iz fizike**, a ne obrnuto
- Naše misli i matematičke apstrakcije su **fizički procesi**

### Duboka Istina

Svaka predstavljena linija izvođenja čvrsto je zasnovana na realnosti, na osnovnim zakonima realnosti, i iz ovih osnovnih stvari se izvoode opštije "stvari", odnosno jednačina poznata kao Lagranžijan.

## Zaključak

Lagranžijan nije misteriozna matematička konstrukcija nametnuta prirodi. To je **neizbežna posledica** najosnovnijih fizičkih zapažanja o sili, kretanju i energiji.

Ovaj pristup otkriva da:
- Fizika je primarna, matematika je sekundarna
- Složene teorije prirodno nastaju iz jednostavnih zapažanja
- Razumevanje dolazi iz fizičke intuicije, a ne iz matematičke apstrakcije
- Minus znak u L = T - V prirodno proizlazi iz konzervacije energije

---

*Priroda se raduje jednostavnosti. I priroda nije glupa.* — Isak Newton

---

*Sledeće poglavlje: **Vrtlog (vortex) model** — kako sudar dva energetska solitona formira stabilnu rotirajuću strukturu, i šta to govori o poreklu "materijalnih" čestica.*
