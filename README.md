# Jadlis-Advisor-Venture-Deals

Claude Code plugin — Venture deals advisor по методологии **Venture Deals** (Brad Feld, Jason Mendelson, 4th Ed. 2019).

## Что делает

8-mode dispatcher для венчурных сделок. Каждый mode активируется по ситуации пользователя:

| # | Mode | Ситуация |
|---|------|----------|
| 1 | Term Sheet | Получил термшит — разбор через линзу Economics vs Control |
| 2 | Fundraising | Готовится к раунду — pipeline, материалы, таргетинг VC |
| 3 | Negotiation | В переговорах — 6 стилей + контр-стратегии |
| 4 | Cap Table | Моделирует разводнение — option pool shuffle, price per share |
| 5 | Convertible Debt | Структурирует ноты/SAFE — 3 метода конвертации |
| 6 | VC Diligence | Оценивает VC-фонд — zombie detection, CVC flags |
| 7 | Deal Structure | LOI на приобретение — asset vs stock, escrow, earn-out |
| 8 | Legal Check | Аудит юридической гигиены — IP, 83(b), 409A |

## Установка

```bash
# Через маркетплейс
claude plugin install jadlis-advisor-venture-deals@jadlis-advisors

# Или напрямую
claude plugin install beCyborg/Jadlis-Advisor-Venture-Deals
```

## Использование

```
/jadlis-advisor-venture-deals:advisor
```

Advisor активируется только при явном вызове (`disable-model-invocation: true`).

## Что Claude НЕ умеет без этого advisor'а

- **Economics vs Control как парсинг-линза**: Claude трактует все clause термшита как равно важные; advisor делит на Economics (payout), Control (decisions) и noise
- **Liquidation preference decision matrix**: 3 варианта с формулами break-even точки; Claude не умеет считать когда capped participating лучше non-participating
- **Option pool shuffle**: конкретная механика снижения effective pre-money; Claude обычно пропускает что pool берётся из pre-money
- **3 метода конвертации нот**: Pre-Money / Percentage-Ownership / Dollars-Invested дают разные ownership; Claude не различает
- **6 стилей переговоров**: Bully / Nice Guy / Technocrat / Wimp / Curmudgeon / Smooth с контр-стратегиями вместо generic "будь кооперативным"
- **Zombie VC detection**: алгоритм из 4 шагов — fund vintage → commitment period → last new investment → direct questions
- **83(b) и 409A как процедурные дедлайны**: 30 дней (необратимо) / 12 месяцев (safe harbor); Claude не обрабатывает как критические deadlines
- **Red/Yellow/Green triage**: классификация каждого term sheet clause по степени важности для переговоров

## Источник

**Venture Deals: Be Smarter Than Your Lawyer and Venture Capitalist** — Brad Feld, Jason Mendelson (4th Edition, 2019). Практическое руководство по венчурным сделкам от managing directors Foundry Group, с более чем 30-летним опытом.

## Лицензия

Структура плагина и skill — MIT. Методология и фреймворки принадлежат авторам книги.
