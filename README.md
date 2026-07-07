# Bitcoin Astronomical Architecture

**Автор:** Любомир Станков · София, България  
**Сайт:** [iddqd-bg.github.io/BitcoinHashExplorer](https://iddqd-bg.github.io/BitcoinHashExplorer/)  
**Академична статия:** [stankov-bitcoin-astronomical-architecture-2026.pdf](stankov-bitcoin-astronomical-architecture-2026.pdf) — CC BY 4.0

---

## За проекта

Проектът документира и визуализира 12 оригинални математически открития, свързващи Bitcoin протокола с астрономически и исторически системи — Прабългарски календар, Метонов цикъл, Антикитерски механизъм и Хеопсовата пирамида.

---

## Файлове

| Файл | Описание |
|------|----------|
| [`index.html`](index.html) | Landing page — 12-те открития |
| [`bitcoin-hash-explorer.html`](bitcoin-hash-explorer.html) | Интерактивен Explorer (12 таба, Claude AI, PRO режим) |
| [`calendar.html`](calendar.html) | Bitcoin × Прабългарски часовник-календар |
| [`stankov-stat-test.html`](stankov-stat-test.html) | Статистически тест на Теоремата на Станков |
| [`updates.html`](updates.html) | 2026 addenda hub: 42-дневна пирамида, Fermat PRO v3, AI bridge benchmark |
| [`pyramid-42-days.html`](pyramid-42-days.html) | Точна пирамидална идентичност: 7! x 6! seconds = 42 days |
| [`fermat-pro-demo-v3.html`](fermat-pro-demo-v3.html) | PoW/17-bit лаборатория с hit-log и CSV export |
| [`research/stankov-ai-bridge-results.html`](research/stankov-ai-bridge-results.html) | Контролиран NumPy benchmark на Stankov AI bridge |
| [`react-sources/parallelepiped-authentic.jsx`](react-sources/parallelepiped-authentic.jsx) | Автентичният React/Three.js източник за геометричната сглобка |

---

## 2026 Addenda

Новите файлове са добавени като отделен слой към проекта, за да се пази ясно разграничение между:

- **доказани точни идентичности**: `pyramid-42-days.html`;
- **Bitcoin-native визуализации**: `fermat-pro-demo-v3.html`, където водещите hex нули са третирани като PoW prefix;
- **емпирични експерименти**: `research/stankov-ai-bridge-results.html`, където AI bridge benchmark-ът е публикуван с консервативна интерпретация.
- **източници за одит**: `react-sources/`, където е запазен автентичният React файл зад `geometry.html`.

Важно уточнение за `0000`: четири водещи hex нули са 16 водещи нулеви bits и са смислени в Bitcoin, когато участват в условието `hash <= target`. Същата последователност вътре в hash-а трябва да се разглежда статистически, освен ако не е обвързана с target сравнение.

---

## 12 Открития

| # | Формула | Значение |
|---|---------|----------|
| 01 | `GCD(N,F) = GCD(r₁,N) = GCD(r₂,N) = 3` | Pair-flip инвариант |
| 02 | `65535 = 3×5×17×257 = 3×F₁×F₂×F₃` | 0xffff = три Ферма прости |
| 03 | `365 − 12×29.53 = 10.64д = 255ч = 0xFF` | Слънчево-лунна разлика = максимален байт |
| 04 | `Δ/2 − 11×600 ≈ B0→B1 (45 сек, 0.0098%)` | Genesis калибрация |
| 05 | `21 = floor(π) × denom(π≈22/7) = F(8)` | 21 произлиза от π и Луната |
| 06 | `p mod 21 = 1` (secp256k1) | 21-кратна симетрия в ℤₚ |
| 07 | `2016 × 2.5° = 5040° = 7! = 14 обороти` | Difficulty = факториел на лунната седмица |
| 08 | `26 × 2016 = 364 дни = 52×7` | Прабълг. идеална година = 26 Bitcoin периода |
| 09 | `285 = 235 + 50 = 3×5×19` | Genesis байтове = Метон + BTC награда |
| 10 | `F(4)=3, F(8)=21, F(12)=144` | Fibonacci структура на Bitcoin |
| 11 | `nₖ = −k − ½ + A·(−1)ᵏ·φ^(−2k)` | **Теоремата на Станков** |
| 12 | `a = year mod 19, c = year mod 7` | Великден Computus = Метон в закон |

---

## Теоремата на Станков (#11)

Корените на уравнението `Fibonacci(n) = 2^(2ⁿ) − 1` следват:

```
nₖ = −k − ½ + A·(−1)ᵏ·φ^(−2k) + o(φ^(−2k))

Decay rate:  φ² = φ+1 = 2.618...
Лимит:       ε_{k+1}/εₖ → −1/φ² = −0.38196601...
A ≈ −0.0746
```

Верифицирано с 50 корена при 120-цифрена точност (Mathematica 14.3).

---

## Хронология — 7514 години

```
5505 пр.Хр  →  Прабългарски календар  (364 = 52×7,  20160 = 10×2016)
2560 пр.Хр  →  Хеопсова пирамида      (h = 880/π,   cubit = π/6 m)
 432 пр.Хр  →  Метон                  (19 год = 235 лунни, ±125 мин)
 ~87 пр.Хр  →  Антикитера             (64/38 = 32/19, 19 в бронз)
 325 сл.Хр  →  Великден Computus      (year mod 19,  year mod 7)
2009 сл.Хр  →  Bitcoin Genesis        (285 = 3×5×19)
```

---

## Ключови числа

```
285  = 235 + 50 = 3×5×19    Genesis байтове
2016 = 2⁵×3²×7              Difficulty период
0xffff = 3×F₁×F₂×F₃         Difficulty мантиса
φ²   = φ+1 = 2.618...        Decay rate (Теорема на Станков)
p mod 21 = 1                 secp256k1 симетрия
```

---

*Stankov153@proton.me*

