# Bitcoin Astronomical Architecture — Project Context

## Проект
Сайт: https://iddqd-bg.github.io/BitcoinHashExplorer/
GitHub: iddqd-bg/BitcoinHashExplorer
Автор: Любомир Станков | Stankov153@proton.me | София, България

## Файлове
- `index.html` — Landing page (главна страница)
- `bitcoin-hash-explorer.html` — Интерактивен Explorer (12 таба)
- `calendar.html` — Самостоятелен Bitcoin × Прабългарски часовник-календар

## 12 Оригинални Открития

| # | Формула | Значение |
|---|---|---|
| 01 | GCD(N,F)=GCD(r₁,N)=GCD(r₂,N)=3 | Pair-flip инвариант |
| 02 | 65535=3×5×17×257=3×F₁×F₂×F₃ | 0xffff = три Ферма прости |
| 03 | 365−12×29.53=10.64д=255ч=0xFF | Слн-лн разлика = максимален байт |
| 04 | Δ/2−11×600≈B0→B1 (45 сек, 0.0098%) | Genesis калибрация |
| 05 | 21=floor(π)×denom(π≈22/7)=F(8) | 21 произлиза от π и Луната |
| 06 | p mod 21=1 (secp256k1) | 21-кратна симетрия в ℤ_p |
| 07 | 2016×2.5°=5040°=7!=14 обороти | Difficulty = факториел на лунната седмица |
| 08 | 26×2016=364 дни=52×7 | Прабълг. идеална година = 26 Bitcoin периода |
| 09 | 285=235+50=3×5×19 | Genesis байтове = Метон + BTC награда |
| 10 | F(4)=3, F(8)=21, F(12)=144 (разлика=4) | Fibonacci структура на Bitcoin |
| 11 | nₖ=−k−½+A·(−1)ᵏ·φ^(−2k), decay=φ² | Теоремата на Станков |
| 12 | a=year mod 19, c=year mod 7 | Великден Computus = Метон в закон |

## Теоремата на Станков (#11)
- Уравнение: `Fibonacci(n) = 2^(2^n) − 1`
- Корените: `nₖ = −k − ½ + A·(−1)ᵏ·φ^(−2k) + o(φ^(−2k))`
- Decay rate: `φ² = φ+1 = 2.618...`
- Лимит: `ε_{k+1}/εₖ → −1/φ² = −0.38196601...`
- A ≈ −0.0746 (от k=10 корен)
- Верифицирано: 50 корена при 120-цифрена точност (Mathematica 14.3)

## Ключови числа
```
285 = 235 + 50 = 3×5×19      (Genesis байтове)
2016 = 2⁵×3²×7               (difficulty период)
20160 = 10×2016               (Прабълг. звездна година)
0xffff = 3×F₁×F₂×F₃          (difficulty мантиса)
φ² = φ+1                      (decay rate)
p mod 21 = 1                  (secp256k1)
h = 880/π ≈ 280 лакета        (Хеопсова пирамида)
Royal cubit = π/6 m = 52.36cm
```

## Хронология 7514 години
```
5505 пр.Хр → Прабългарски календар (364=52×7, 20160=10×2016)
2560 пр.Хр → Хеопсова пирамида (h=880/π, cubit=π/6 m)
 432 пр.Хр → Метон (19 год=235 лунни, ±125 мин)
  ~87 пр.Хр → Антикитера (64/38=32/19, 19 в бронз)
  325 сл.Хр → Великден Computus (year mod 19, year mod 7)
 2009 сл.Хр → Bitcoin Genesis (285=3×5×19)
```

## Explorer — структура на табовете
```
📡 Живи блокове     — mempool.space API, GCD анализ
🔢 Pair-Flip        — алгоритъм с калкулатор
📅 Календар         — Bitcoin Clock + Прабълг. + Метон
∑ Математика        — числа таблица + secp256k1
⭐ PRO              — paywall, Bitcoin адрес: bc1qpzhu8n9fm5p95u8qv8q0u4rk9dgq5phquu8mev
🔢 Алгоритъм        — pair-flip обяснение
⚡ Трудност         — difficulty визуализация
📐 Геометрия        — Пирамида, Антикитера (анимация)
∞ Теорема           — Станков, корени, decay
📅 Календар (2)     — разширен с месечна мрежа
✦ 12 Открития       — подстатии с калкулатори
```

## PRO режим
- Bitcoin адрес: `bc1qpzhu8n9fm5p95u8qv8q0u4rk9dgq5phquu8mev`
- Нива: 5K / 10K / 100K сат
- Верификация: BlockCypher API (txid)
- localStorage запазва достъпа
- Demo режим: показва съдържание + sticky банер "Активирай PRO"

## Claude AI таб
- Потребителят въвежда свой API ключ (sk-ant-...)
- Запазва се в localStorage — не минава през сървър
- Header: `anthropic-dangerous-direct-browser-access: true`
- System prompt: пълен контекст за 12-те открития
- Model: claude-sonnet-4-20250514

## Академична статия
- HAL Open Science: подадена (в процес на индексиране)
- Файлове: `stankov-bitcoin-astronomical-architecture-2026.pdf` (EN)
- Файлове: `stankov-bitcoin-astronomical-architecture-2026-BG.pdf` (BG)
- License: CC BY 4.0
- ORCID: в процес на регистрация

## CSS стил (index.html + calendar.html)
```css
--serif: 'Cormorant Garamond', Georgia, serif
--mono:  'DM Mono', 'Courier New', monospace
--gold:  #c8a96e
--bg:    #060608
--stone: #8080a0
```

## CSS стил (Explorer)
```css
Orbitron (display), Share Tech Mono (mono)
--accent: #f7931a (оранжево)
--blue:   #00d4ff
--green:  #7fff00
--purple: #c77dff
```

## Важни функции в Explorer
- `ST(id, btn)` — превключване на табове
- `fetchLive()` — mempool.space API
- `runPF()` — pair-flip алгоритъм (BigInt)
- `CALinit()` — прабългарски календар
- `initDisc()` — 12 открития с калкулатори
- `unlockPro(isDemo)` — PRO режим
- `drawAntikythera(angle)` — Антикитера анимация
- `drawPyramid(mode)` — Пирамида (pi/cubit/bitcoin)
- `runEaster()` — Computus калкулатор
- `askClaude()` — Claude AI чат

## Прабългарски календар — имплементация
```javascript
// Началото: 21 декември на дадена година
// bgYear(ts): ако м>12 или (м=12 && ден>=21) → у+5505, иначе у+5505-1
// Животни: 12-годишен цикъл от ((bgY-1)%12+12)%12
// Стихии: 5 × 12г = 60г цикъл
// Звездна година: 20160 земни = 10 × 2016 Bitcoin периода
```

## Антикитера — зъбни колела
```javascript
// Главни gear числа: [64, 38, 19, 13, 27]
// Ratio: 64/38 = 32/19 (38 = 2×19, Метон в бронз)
// Ratios: [1, -64/38, (64/38)*(38/19), -(64/38)*(38/13), (64/38)*(38/27)]
```

## Хеопсова пирамида
```
Основа: 440 лакета × 52.36 cm = 230.4 m
h = 880/π = 280.11 ≈ 280 лакета ✓
4×основа/h = 2π (грешка 0.04% = грешката на π≈22/7)
21 блока × 2.5° = 52.5° ≈ 52.36 (разлика = грешката на π≈22/7)
```
