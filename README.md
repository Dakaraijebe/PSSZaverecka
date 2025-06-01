# PSSZaverecka
# Krabička odnaučující kouření

> Ročníkový projekt – Vojtěch Plichta, C3b  
> Předmět: PSS

## O čem je projekt

Tento projekt představuje krabičku na cigarety, která má za cíl pomoci uživatelům omezit kouření. Pomocí Arduina a elektroniky je výdej cigaret řízen tak, že jsou dostupné pouze po určitých intervalech, které se po každém stisknutí automaticky prodlužují.

## V čem je řešení unikátní

- Intervaly výdeje se prodlužují o 20 po každém pokusu.
- Používá kapacitní tlačítko místo mechanického – moderní a bezúdržbové.
- LED signalizace ukazuje, kdy je možné si vzít cigaretu.
- Elektromagnetický mechanismus cigaretu mechanicky vysune.

## Použité technologie a součástky

- Arduino Nano
- LED dioda (vestavěná)
- Kapacitní dotykový spínač
- Relé modul (5V)
- Elektromagnet
- 12V akumulátor
- Papírová krabička
- Nepájivé pole a vodiče
- Vypínač

## Jak to funguje

1. Po zapnutí začne běžet časový interval (30 minut).
2. Po jeho uplynutí se rozsvítí LED.
3. Uživatel stiskne dotykový spínač.
4. Arduino sepne relé a aktivuje elektromagnet (na 0,5 s).
5. Cigareta se mechanicky vysune.
6. Interval se prodlouží (např. ×1.2).
7. Proces se opakuje – dokud zařízení běží.

## Základní algoritmus

Start → Časovač → LED svítí → Spínač stisknut?
    → Ano → Relé → Elektromagnet → Vysunutí cigarety
    → Interval * 1.2 → Zpět na start
