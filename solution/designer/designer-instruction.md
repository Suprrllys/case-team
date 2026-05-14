---
# ──────────────────────────────────────────────────────────────
# YAML-контракт презентации для Practicum Award 2026 (v3 — финальный)
# Номинация: Техно-продуктовый вклад
# Проект: «Команда ИИ-агентов для решения бизнес-кейсов»
# Mode: regular (PowerPoint через python-pptx)
#
# Главные изменения v3 vs v2:
# - Брендбук Яндекс Практикум (жёлтый + чёрный + YS Text)
# - AJTBD-иерархия уточнена из отзывов клиентов (Big Job «принять + защитить»)
# - D10 — монетизация подача А: «в стоимости подписки на нейросеть»
# - Убран весь внутренний сленг (Core Job / Micro Jobs / увольняем / снимаем барьеры)
# - Эталоны: «решения для Axenix (Cup Moscow 2024) и Askona (Inno Case Hack 2025)»
# - Slide 6 разбит на 2 (Экономика + Переход клиента)
# - Slide 9 слоган по формуле differentiation Замесина
# ──────────────────────────────────────────────────────────────

mode: regular

# ── МЕТА ──────────────────────────────────────────────────────
title: "Альтернатива стратегическому консалтингу через мультиагентную AI-команду"
subtitle: "Полный пакет материалов под защиту — за 4 часа, в стоимости подписки на нейросеть"
project: "Practicum Award 2026 · Техно-продуктовый вклад"
team: "Сергей Леонтьев · Product Manager"
date: ""
language: ru

# ── АУДИТОРИЯ И ФОРМАТ ────────────────────────────────────────
audience: "Жюри Practicum Award (CTO Практикума, Yandex AI Studio, LetAI, ФАНС, Замесин)"
goal: "Выход в финалисты + борьба за приз номинации или спецприз «Будущее за ним»"
key_takeaway: "Готовим полный пакет материалов решения бизнес-кейса под защиту перед стейкхолдерами — за 4 часа, в стоимости подписки на нейросеть"
tone: "Деловой, аналитический, методологически точный — без AI-обещаний и штампов"
time_limit_min: 10
aspect: "16:9"
size_px: [1920, 1080]

# ── БРЕНД ЯНДЕКС ПРАКТИКУМ ────────────────────────────────────
# Источник: брендбук Practicum (лендинг конкурса + общий брендинг Яндекс)
palette:
  primary:        "#FBCE07"   # Yandex Yellow — главный акцент (кнопки, hero-плашки, активные элементы)
  primary_dark:   "#000000"   # Yandex Black — фон hero-слайдов, контраст
  primary_soft:   "#FFF5CC"   # светлый жёлтый — карточки, заливка под графиками
  ink:            "#1A1A1A"   # основной текст
  ink_2:          "#666666"   # подзаголовки-выводы серым (Text-secondary)
  bg:             "#FFFFFF"   # фон контентных слайдов (чистый белый по бренду)
  accent_pos:     "#00C853"   # зелёный для положительных метрик (контраст к жёлтому)
  accent_warn:    "#FF6B00"   # оранжевый для предупреждений
  divider:        "#E5E5E5"   # тонкие разделители
fonts:
  display: "YS Display"       # для крупных заголовков (если недоступен → Inter Bold → Manrope Bold)
  body:    "YS Text"          # для основного текста (если недоступен → Inter → Manrope → Arial)
  mono:    "JetBrains Mono"   # для моноширинных блоков (схемы, код)
font_fallbacks:
  display: ["YS Display", "Inter", "Manrope", "Arial"]
  body:    ["YS Text", "Inter", "Manrope", "Arial"]
visual_style: |
  Брендинг Яндекс Практикум: чистый белый фон контентных слайдов, чёрный текст,
  жёлтый primary для акцентов (кнопки, плашки, активные табы навигации).
  Hero-слайды (Cover, Финал, разделители) — чёрный фон с жёлтыми акцентами и белой типографикой.
  Карточки на белом фоне — без рамок, мягкая тень, радиус 16-24 px.
  Иконки — линейные векторные в кружках primary_soft, монохром чёрные.

# ── ИСХОДНЫЕ МАТЕРИАЛЫ ────────────────────────────────────────
references:
  - "https://practicum.yandex.ru/practicum-award (лендинг конкурса — для брендбука)"
  - "case-output/analyst/practicum-award-context.md (research + матрица конкурентов)"
  - "case-output/analyst/jobs-and-segments-analysis.md (Mot-Moment + Big Job из отзывов)"
  - "case-output/financier/unit-economics.md (внутренняя экономика работы агентов)"
  - "case-output/marketer/positioning.md (финальные формулировки + слоганы)"
inputs:
  - "case-output/MANAGER-LOG.md"
  - "case-output/SLIDES-PLAN.md"

# ── ОГРАНИЧЕНИЯ ───────────────────────────────────────────────
constraints:
  - "не выдумывать числа — только из artifacts (financier, analyst)"
  - "каждая цифра прослеживаема к источнику в Decision Log"
  - "не больше 3 цветов в композиции (primary + bg + один акцент)"
  - "не больше 7±2 смысловых блоков на слайд"
  - "не больше 4 колонок в таблице"
  - "заголовок = ТЕЗИС, не тема"
  - "иконки только векторные; эмодзи запрещены"
  - "обязательный pre-flight overflow check"
  - "macOS PowerPoint blessing после генерации (открыть → Восстановить → Save As)"
  - "не использовать слова Core Job / Micro Jobs / увольняем / снимаем барьеры — внутренний сленг"
  - "эталоны: писать «решение для Axenix (Cup Moscow 2024)» и «решение для Askona (Inno Case Hack 2025)», без слова «финалист»"

# ── ВЫХОД ─────────────────────────────────────────────────────
output:
  filename: "practicum-award-2026-case-team.pptx"
  also_export: ["pdf"]

# ── ИСТОЧНИКИ ИСТИНЫ ──────────────────────────────────────────
sources_of_truth:
  regular_protocol: "~/Documents/Obsidian/base-of-knowledge/50 Дизайн/🎯 Универсальная инструкция презентации.md"
  aesthetic_reference: "~/Documents/Obsidian/base-of-knowledge/50 Дизайн/Inno-Case-Hack_2026_Monster-High_презентация-эталон.pdf"
  quality_skill: "~/Documents/Vibecoding-projects/.claude/skills/claude-design/"
---

## Slide 1 · Альтернатива стратегическому консалтингу через мультиагентную AI-команду {type:cover accent:dark}

**Полный пакет материалов под защиту — за 4 часа, в стоимости подписки на нейросеть.**

Сергей Леонтьев · Product Manager
Practicum Award 2026 · Техно-продуктовый вклад

## Slide 2 · Готовим полный пакет материалов решения бизнес-кейса под защиту перед стейкхолдерами — за стоимость подписки на нейросеть {type:exec-summary cols:2}

**За 4 часа вместо 5-6 дней, без дополнительной оплаты для пользователей Claude, с воспроизводимой методологией.**

**4 блока — всё решение одним слайдом:**

| Блок | Содержание |
|---|---|
| **Анализ** | 266 тыс компаний МСП в РФ принимают стратегические решения 2-6 раз в год; 5 текущих способов не дают сшитого пакета под защиту |
| **Концепция** | 5 Claude-агентов готовят  презентации, финмодели, аналитику и позиционирование. Решение go/no-go и защита перед людьми остаются за человеком |
| **Реализация** | 5 ролей · обучены на решениях для Axenix (Cup Moscow 2024) и Askona (Inno Case Hack 2025) · 26 методологических логик в каталоге команды ([открытый репозиторий](https://github.com/Suprrllys/case-team)) |
| **Эффект** | 4 часа вместо 5-6 дней · в стоимости подписки на нейросеть · устойчиво 84-98% экономии при ±20% к параметрам |

## Slide 3 · 266 тыс компаний МСП в РФ принимают стратегические решения 2-6 раз в год — и каждый раз должны защитить их перед инвестором, советом или партнёром {type:problem layout:split-chart}

**Из 9 проанализированных альтернатив ни одна не даёт сшитого пакета (research + стратегия + финмодель + презентация) под одной методологической логикой.**

**Сегмент:** Фаундер/CEO стартапа или Operations Director МСП в РФ; штат 5-50; принимает крупное стратегическое решение 2-6 раз в год. Полная карточка персоны — Приложение A1.

**Главная работа клиента:** принять обоснованное решение **и** провести его через стейкхолдеров (инвесторы / совет / партнёры / команда).

**Конкретные ситуации, когда возникает работа** (из отзывов клиентов на конкурентов):
- Питч инвестору в среду — встреча через 7 дней
- Совет директоров в пятницу — нужны цифры с источниками
- Конкурент сделал X — нужен стратегический ответ завтра
- Запуск нового продукта — go/no-go через 14 дней

**Что клиент нанимает сейчас и в чём минусы:**

| Альтернатива | Стоимость 1 кейса | Главный минус |
|---|---|---|
| Делать самому | 5-6 дней личного времени | Нехватка компетенций минимум в 1 из 5 ролей; история не сшивается |
| In-house команда из 5 | ~99 тыс ₽ + 700 тыс ₽/мес ФОТ | Неподъёмно для МСП |
| Big4-tier агентство | 350 тыс — 1.5 млн ₽ | Цена за «снижение риска через репутацию партнёра» |
| Фрилансеры с биржи (5 человек) | 50-150 тыс ₽ | Полный пакет не встречается — никто не сшивает в единую историю |
| ChatGPT / один AI-чат | подписка | Текст, не пакет; нет финмодели с формулами; каждая генерация дает разный результат |

**Объём рынка:** 266 тыс компаний МСП РФ / 18-80 млрд ₽ недополученного спроса в год.
Источники — Приложение A0.

## Slide 4 · 5 Claude-агентов готовят полный пакет — а решение и защита остаются за человеком {type:concept layout:hero accent:dark}

**Куратор смысла внутри команды + физические артефакты на выходе + дотренировка на двух реальных кейс-чемпионатах — этого нет ни у одного из 9 проанализированных конкурентов.**

**Что мы делаем полностью:**
- Презентация `.pptx` — с навигацией, pre-flight check, готова к показу
- Финмодель `.xlsx` — с формулами и sensitivity
- Аналитика — рынок, конкуренты, ЦА с источниками
- Концепция и позиционирование
- Decision Log — обоснование каждой развилки

**Что остаётся за человеком (граница ответственности):**
- Финальное go/no-go решение
- Защита перед инвестором / советом — живая коммуникация
- Операционное внедрение стратегии
- Договорённости с конкретными партнёрами

**4 архитектурных решения:**

1. **Менеджер-агент — куратор смысла внутри команды.** Решает, что класть на слайды; специалисты не пишут сразу в .pptx. Это ответ на 85% failure rate автономных агентов (Devin: 15% completion на сложных задачах — независимые тесты).
2. **На выходе — физические рабочие файлы**, не текст в чате. `.xlsx` с формулами, `.pptx` готов к показу, `.md` Decision Log с источниками.
3. **Дотренировка на двух реальных кейс-чемпионатах** — решение для Axenix на Cup Moscow 2024 и решение для Askona на Inno Case Hack 2025. Из них извлечено 26 методологических логик. Кроме того, тренировка методологией AJTBD и промптах Ивана Замесина
4. **Иерархия источников в каждом правиле агента:** эталон → бизнес-классика (Osterwalder, MoSCoW, AS-IS/TO-BE) → эвристика менеджера. Каждое правило ссылается на источник — это снижает галлюцинации.

## Slide 5 · 5 Claude-агентов, обученных на решениях для Axenix и Askona, с дисциплиной коммуникации через файлы {type:scheme}

**Архитектура устроена так, что специалисты не пишут друг другу — всё проходит через менеджера. Это снимает риск рассинхрона между маркетингом, финансами и аналитикой.**

**Схема взаимодействия (главный визуал слайда):**
```
                  ┌──────────────────┐
                  │  case-manager    │   ◄── куратор смысла
                  │  PM-оркестратор  │
                  └────┬─────────────┘
                       │ Agent tool (задача с контекстом)
                       ▼
        ┌──────────────┼──────────────┐
        ▼              ▼              ▼
   ┌─────────┐   ┌──────────┐   ┌──────────┐
   │analyst  │   │financier │   │marketer  │
   │research │   │финмодель │   │AJTBD     │
   └────┬────┘   └────┬─────┘   └─────┬────┘
        │ результат-.md в свою папку  │
        └──────────────┼──────────────┘
                       │ (между специалистами — через blockers/, всегда через менеджера)
                       ▼
                ┌──────────────┐
                │ case-designer│ ◄── конвертер формата
                │ YAML.md→.pptx│
                └──────────────┘
```

**5 ролей — что делает каждая:**

| Агент | Что делает | Главный метод |
|---|---|---|
| case-manager | Концепция, Decision Log, синтез | 6-шаговый алгоритм отбора инсайтов на слайды | Делегирование задач | Решение блокеров
| case-analyst | Research рынка, конкурентов, ЦА | Каталог исследовательских фреймворков + извлечение работ из отзывов |
| case-financier | Финмодель, NPV, sensitivity | Универсальная инструкция построения финмодели (5 блоков Input × 11 вертикалей) |
| case-marketer | AJTBD, позиционирование, каскад целей | Motivation-Moment персона + Value Exchange + Barrier-Concept Matching |
| case-designer | Конвертирует YAML.md → .pptx + полировка | python-pptx + 4 проверки качества (ai-slop, accessibility, ритм, polish) |

**Как тренировались:**
На решениях для Axenix (Cup Moscow 2024) и Askona (Inno Case Hack 2025) с кейс-чемпионатов. Решения разобраны на **26 методологических логик**; полная открытая методология и материалы — в [GitHub-репозитории `Suprrllys/case-team`](https://github.com/Suprrllys/case-team). Дотренировка на **рабочих артефактах** — черновики, Decision Log, отвергнутые идеи — не только на финальных результатах.

## Slide 6 · Для пользователя Claude — без дополнительной оплаты; внутри команды 1 кейс агентами стоит 11 тыс ₽ при 99 тыс ₽ in-house и 396 тыс ₽ через агентство {type:economics chart:bars}

**Категориальный сдвиг — стратегический пакет встроен в стоимость подписки на нейросеть, которая уже оплачена клиентом для других задач.**

**Главное для клиента (крупно):**
- **Дополнительный расход для пользователя Claude = 0 ₽** (подписка уже оплачена для других задач)
- **4 часа** реального времени работы вместо 5-6 дней команды
- Воспроизводимая методология — на каждую цифру есть источник

**Внутренняя экономика работы агентов (для прозрачности, не для цены клиенту):**

| Сравнение базы | Стоимость 1 кейса, ₽ |
|---|---|
| **Время менеджера** (3.5 ч × 1500 ₽) + Claude tokens | **~10 930** |
| In-house команда из 5 (90 чел.-ч × 1100 ₽/ч middle) | 99 000 |
| Big4-tier агентство (×4 multiplier) | 396 000 |

**Sensitivity — устойчивость экономии (±20% к параметрам):**
- Базовый: **89%** экономии vs in-house
- При junior-команде in-house (800 ₽/ч): **84%**
- При sourcing через Big4: **97-98%**
- При +20% к расходу токенов: **88%**

Якорь устойчив на всех границах разумного диапазона.

**Как пользоваться:**
- Установка `/case-team` одной командой в Claude Code ([открытый репозиторий `github.com/Suprrllys/case-team`](https://github.com/Suprrllys/case-team))
- Подписка Claude $20-100/мес уже оплачена для других задач — категориальный сдвиг, не цена сверху
- Полная бизнес-модель и монетизация автора — Приложение A9

## Slide 7 · Что меняется относительно существующих способов и что снижает порог входа {type:economics cols:2}

**Главный страх клиента — не «дорого», а «обнаружится фейк под вопросами стейкхолдера». Поэтому каждая цифра защищена источником.**

**Таблица 1 — Что меняется относительно существующих способов:**

| Способ сейчас | Что меняется с `/case-team` |
|---|---|
| **Делать самому** (5-6 дней) | 4 часа реального времени; качество в 5 ролях, недостижимое одному человеку |
| **In-house команда из 5** (99k ₽/кейс + 700k/мес ФОТ) | Не нужен 1-2-месячный найм; пакет за стоимость подписки на нейросеть |
| **Big4-tier агентство** (350k-1.5M ₽, 4-8 недель) | 4 часа вместо недель; снижение риска через прозрачность методологии вместо репутации партнёра |
| **Фрилансеры с биржи** (5 разных человек) | Куратор смысла внутри (менеджер-агент) — единая методология, согласованные артефакты |
| **ChatGPT / один AI-чат** | Получаешь `.xlsx` и `.pptx` с формулами, не текст в чате; на каждую цифру — источник |

**Таблица 2 — Низкий порог входа (4 барьера сняты, барьер цены снят полностью через подписку):**

| Барьер клиента | Как снят (измеримо) |
|---|---|
| **Технический** («настраивать MCP, subagents») | **1 команда** `/case-team` в Claude Code; **0 шагов** настройки multi-agent pipeline |
| **Доверия** («AI не справится со стратегией») | Дотренировка на **2 реальных кейс-чемпионатах**; **100% цифр** имеют URL-источник |
| **Формата** («получу ли то, что нужно показать стейкхолдеру») | Гарантированные **5 файлов** на выходе: `.xlsx` финмодель, `.pptx` презентация, `SOLUTION.md`, `MANAGER-LOG.md`, research |
| **Обучаемости** («надо изучать промпт-инжиниринг») | **0 команд** изучения промпт-инжиниринга; задача ставится естественным языком |

## Slide 8 · Один продуктовый менеджер плюс команда из 5 ИИ-агентов = эффективная единица решения бизнес-кейсов {type:team}

**Эта заявка собрана этой же командой `/case-team` за день до дедлайна подачи на конкурс — мета-доказательство тезиса.**

<!-- Дизайнеру: карточка участника с местом под фото слева (круг диаметр ~300px, photo=placeholder если файла нет — рендер инициалы СЛ на primary_soft фоне) + инфо справа -->

**Автор:**

```yaml
team:
  - name: "Сергей Леонтьев"
    photo: "assets/team/sergey.jpg"   # путь подставить перед сборкой; если нет — placeholder с инициалами «СЛ»
    role: "Менеджер по продукту"
    company: "ООО «Нинтегра»"
    university: "МАИ 2025, «Прикладная информатика»"
    achievements: "Победитель, призёр и участник 10+ кейс-чемпионатов по бизнес-анализу, стратегическому консалтингу, продуктовому управлению и маркетингу"
    methodology: "AJTBD + ИИ-агенты"
```

**Контакты:**
- suprrllysmanagement@mail.ru
- +7 (985) 176-06-58
- GitHub-репозиторий: [github.com/Suprrllys/case-team](https://github.com/Suprrllys/case-team)
- Видео-демо `/case-team` 5 мин: по запросу жюри

## Slide 9 · Полный пакет под защиту — в 8× быстрее, в стоимости подписки на нейросеть {type:final accent:dark}

**Готовим полный пакет материалов решения бизнес-кейса под защиту в 8× быстрее и без дополнительной оплаты для пользователей Claude — за счёт мультиагентной AI-команды в Claude Code.**

> Альтернатива стратегическому консалтингу через мультиагентную AI-команду

Сергей Леонтьев · Product Manager · Practicum Award 2026

---

<!--
ПРИЛОЖЕНИЯ ДЛЯ Q&A
══════════════════
Каждое приложение закрывает конкретный возможный вопрос жюри.
Показываются опционально — если жюри спросит. Не в основном нарративе.
Принцип (§3.4.2 case-manager): "если жюри не спросит — не показываем".
-->

## Appendix A0 · Источники {type:appendix}

**Все источники использованные при формировании решения — публичные URL, каждый проверяемый кликом.**

### Рынок консалтинга РФ
1. [TAdviser «Консалтинг (рынок России)»](https://www.tadviser.ru/index.php/Статья:Консалтинг_(рынок_России)) — общий объём 140 млрд ₽ в 2024 (+15% YoY)
2. [RAEX-RR рэнкинг стратегического консалтинга 2025](https://raex-rr.com/b2b/consulting/consulting_strategic_planning_and_organizational_development/2025/analytics/) — стратегический сегмент 14.8 млрд ₽ (+39%)
3. [RAEX-RR крупнейшие консалт-группы 2025](https://raex-rr.com/b2b/consulting/biggest_consulting_companies_and_groups/2025/) — Q1 2025 = 9.7 млрд ₽ (+9%)
4. [РБК Тренды «Тренды 2025 на рынке консалтинга»](https://trends.rbc.ru/trends/social/67c0c6279a7947193f435524) — управленческий 37 млрд ₽ (+19%) через Рексофт
5. [HSE Daily «Рынок управленческого консалтинга в 2023»](https://daily.hse.ru/post/novye-igroki-rynki-perspektivy-kak-vyglyadit-rynok-upravlencheskogo-konsaltinga-v-2023-godu)
6. [Fless.pro «Большая тройка в России после 2022»](https://fless.pro/big3-in-russia-after-2022-sbs-consulting)
7. [TAdviser «Яков и Партнёры (ранее McKinsey в России)»](https://www.tadviser.ru/index.php/Компания:Яков_и_Партнёры_(YnP,_ранее_McKinsey_в_России))
8. [KSK Group услуги стратегического консалтинга](https://kskgroup.ru/services/consulting/strategicheskiy-konsalting/) — нижний ценовой сегмент 350-550 тыс ₽
9. [Profi.ru стратегический консалтинг](https://profi.ru/buhgaltery_i_yuristy/strategicheskii-konsalting/price/)

### МСП в РФ (TAM)
10. [Ведомости 25.12.2025 «Число субъектов МСП»](https://www.vedomosti.ru/economics/articles/2025/12/25/1166484-chislo-subektov-msp-uvelichilos) — 6.835 млн МСП в янв 2026
11. [Единый реестр МСП ФНС](https://rmsp.nalog.ru/) — официальные данные
12. [Корпорация МСП «Численность обновила исторический максимум»](https://xn--90aifddrld7a.xn--p1ai/news/country/chislennost-msp-v-rossii-obnovila-istoricheskiy-maksimum-i-prevysila-6-8-mln-predpriyatiy/)
13. [Гарант «Количество малых и средних выросло»](https://www.garant.ru/news/1964227/)

### Ставки консультантов и фрилансеров РФ
14. [dreamjob.ru «Старший консультант»](https://dreamjob.ru/salary/starshiy-konsultant) — middle 150-280k ₽/мес
15. [Fless.pro «Зарплаты в Большой Тройке»](https://fless.pro/consulting-salaries-ru) — Associate 350-450k, Manager 500k
16. [vc.ru «Стратегический консалтинг»](https://vc.ru/hr/520245-strategicheskii-konsalting-na-blizhnem-vostoke-zarplaty-ot-120-tysyach-fantasticheskie-goroda-v-pustyne-i-metavselennaya)
17. [Gorodrabot.ru «Зарплата консультанта в Москве»](https://moskva.gorodrabot.ru/salaries/konsultant)
18. [Lidopad «Фрилансеры в России 2025»](https://lidopad.online/news/skolko-realno-zarabatyvayut-frilansery-v-rossii-statistika-i-prognoz-na-2026/) — средний доход 44k ₽/мес

### Multi-agent AI рынок и тренды
19. [Gartner «40% enterprise apps with AI agents by 2026»](https://www.gartner.com/en/newsroom/press-releases/2025-08-26-gartner-predicts-40-percent-of-enterprise-apps-will-feature-task-specific-ai-agents-by-2026-up-from-less-than-5-percent-in-2025)
20. [McKinsey MGI «$4.4 trillion AI value»](https://www.mckinsey.com/mgi/media-center/ai-could-increase-corporate-profits-by-4-trillion-a-year-according-to-new-research)
21. [McKinsey «State of AI» November 2025](https://www.mckinsey.com/capabilities/quantumblack/our-insights/the-state-of-ai)
22. [McKinsey «Economic potential of generative AI»](https://www.mckinsey.com/capabilities/tech-and-ai/our-insights/the-economic-potential-of-generative-ai-the-next-productivity-frontier)
23. [Markets&Markets «AI Agents Market 2025-2030»](https://www.marketsandmarkets.com/Market-Reports/ai-agents-market-15761548.html)
24. [Paul Okhrem «Enterprise AI Agents Statistics 2026»](https://paul-okhrem.com/enterprise-ai-agents-statistics-2026/) — $7.6→$10.8 млрд + 40% projects cancelled
25. [Joget «AI Agent Adoption 2026»](https://joget.com/ai-agent-adoption-in-2026-what-the-analysts-data-shows/)
26. [a16z «How 100 Enterprise CIOs Build Gen AI 2025»](https://a16z.com/ai-enterprise-2025/)
27. [a16z «Where Enterprises Adopt AI»](https://a16z.com/where-enterprises-are-actually-adopting-ai/)

### Конкуренты — международные multi-agent (цены и отзывы)
28. [Felloai «Manus AI Pricing 2026»](https://felloai.com/manus-ai-pricing/) — $0/$19/$39/$199
29. [RioTimes «Manus AI 14 Failures in Two Weeks»](https://www.riotimesonline.com/manus-a-i-review-14-failures-in-two-weeks-of-testing/)
30. [Trickle «Manus AI Review»](https://trickle.so/blog/manus-ai-review) — Reddit credit-burn case $2380
31. [Trustpilot Manus AI reviews](https://www.trustpilot.com/review/manus-ai.sbs)
32. [Lindy.ai Pricing](https://www.lindy.ai/pricing) — Free / Starter $19.99 / Pro $49.99
33. [CloudTalk «Lindy AI Pricing 2026»](https://www.cloudtalk.io/blog/lindy-ai-pricing/) — onboarding fee $1500 hidden
34. [CrewAI Pricing](https://crewai.com/pricing)
35. [ZenML «CrewAI Pricing Guide»](https://www.zenml.io/blog/crewai-pricing) — Enterprise $60-120k/год
36. [Microsoft Research «Magentic-One»](https://www.microsoft.com/en-us/research/articles/magentic-one-a-generalist-multi-agent-system-for-solving-complex-tasks/)
37. [WinBuzzer «AutoGen 0.4 + Magentic-One»](https://winbuzzer.com/2025/01/14/microsoft-releases-autogen-0-4-with-magentic-one-multi-ai-agent-framework-xcxwbn/)
38. [Devin Pricing](https://devin.ai/pricing/) — Core $20 / Team $500
39. [VentureBeat «Devin 2.0 Slashes Price to $20»](https://venturebeat.com/programming-development/devin-2-0-is-here-cognition-slashes-price-of-ai-software-engineer-to-20-per-month-from-500)
40. [OpenAIToolsHub «Devin AI Review: 13.86% SWE-Bench»](https://www.openaitoolshub.org/en/blog/devin-ai-review)
41. [SitePoint «Devin Aftermath: AI Engineers in Production»](https://www.sitepoint.com/devin-ai-engineers-production-realities/)

### Конкуренты — российские AI-платформы
42. [GigaChat Enterprise на Хабре](https://habr.com/ru/companies/sberbank/news/1005990/) — запуск март 2026
43. [vc.ru «Сбер GigaChat Enterprise»](https://vc.ru/typespace/2769088-sber-gigachat-enterprise-platforma-dlya-ii-agentov)
44. [GigaChat Business — Multi-Agent System](https://b2b.giga.chat/multi-agent-system)
45. [Yandex AI Studio главная](https://aistudio.yandex.ru/ru)
46. [Яндекс «AI Studio большое обновление»](https://yandex.ru/company/news/03-03-2026-01)
47. [Habr «Яндекс открыл рассуждающие ИИ-агенты»](https://habr.com/ru/amp/publications/1009872/)
48. [Just AI Agent Platform](https://agentplatform.just-ai.com/)
49. [Just AI «Сравнение российских AI-платформ 2026»](https://just-ai.com/blog/sravnenie-rossijskih-platform-dlya-sozdaniya-ai-agentov)

### Конкуренты — универсальные AI-чаты + презентации
50. [Claude for PowerPoint](https://claude.com/claude-for-powerpoint)
51. [Prezent.ai «Claude for PowerPoint: setup, limitations»](https://www.prezent.ai/blog/claude-for-powerpoint)
52. [MindStudio «Gamma vs ChatGPT vs Claude vs Google Slides»](https://www.mindstudio.ai/blog/gamma-vs-chatgpt-vs-claude-vs-google-slides-ai-presentation-tool-comparison)
53. [SlideSpeak «Create Presentations with Claude Design 2026»](https://slidespeak.co/blog/create-presentations-claude-design)

### Бенчмарки AI-экономии (для Slide 6 + A4)
54. [Klarna Press «AI assistant 2/3 customer service»](https://www.klarna.com/international/press/klarna-ai-assistant-handles-two-thirds-of-customer-service-chats-in-its-first-month/)
55. [OpenAI «Klarna AI does work of 700 agents»](https://openai.com/index/klarna/)
56. [CX Dive «Klarna AI slashing costs»](https://www.customerexperiencedive.com/news/klarna-ai-slash-customer-service-costs/748647/)
57. [Twig «Klarna AI Cut Resolution Time 82%»](https://www.twig.so/blog/how-klarna-is-revolutionizing-customer-support-with-ai)
58. [GitHub Blog «Quantifying GitHub Copilot Impact»](https://github.blog/news-insights/research/research-quantifying-github-copilots-impact-on-developer-productivity-and-happiness/) — +55% speed
59. [arXiv «AI on Developer Productivity: GitHub Copilot»](https://arxiv.org/abs/2302.06590) — peer-reviewed, P=0.0017
60. [Anthropic «How AI Is Transforming Work at Anthropic»](https://www.anthropic.com/research/how-ai-is-transforming-work-at-anthropic)
61. [Anthropic «Estimating productivity gains»](https://www.anthropic.com/research/estimating-productivity-gains) — ~80-81% task speedup
62. [HUB International «Anthropic Claude to 20 000+ Employees»](https://www.hubinternational.com/media-center/press-releases/2026/02/hub-international-brings-anthropics-claude-to-20000-employees/)

### Финмодель — стоимость API + курс ЦБ РФ
63. [Anthropic Pricing](https://platform.claude.com/docs/en/about-claude/pricing) — Opus 4.7 $5 input / $25 output на 1M токенов
64. [Finout «Anthropic API Pricing 2026»](https://www.finout.io/blog/anthropic-api-pricing)
65. [ЦБ РФ официальный курс](https://www.cbr.ru/) — USD/RUB 73.34 на 14 мая 2026
66. [Finance.mail.ru «Курс доллара на 14 мая 2026»](https://finance.mail.ru/article/oficialnyj-kurs-dollara-na-14-maya-2026-69208634/)

### Методологические источники
67. [Иван Замесин — публикации по AJTBD-консалтингу](https://zamesin.ru/) — Mot-Moment, extract-jobs-from-reviews, market-trends-research, competitor-research, differentiation-strategy
68. [Christensen «Competing Against Luck» (JTBD framework)](https://www.amazon.com/Competing-Against-Luck-Innovation-Customer/dp/0062435612)
69. [Osterwalder «Value Proposition Design»](https://www.strategyzer.com/library/value-proposition-design)
70. [Anthropic Claude Design — Claude.ai](https://claude.com)
71. [Practicum Award 2026 — лендинг конкурса](https://practicum.yandex.ru/practicum-award) — критерии оценки + жюри

---

## Appendix A1 · Сегмент клиента — фаундер МСП в стратегическом моменте (через работы AJTBD) {type:appendix}

**Кто (минимум характеристик):**
Founder/CEO стартапа (Series A-B) или Operations Director / Commercial Director МСП в РФ; штат компании 5-50 человек; оборот 10-500 млн ₽/год; города-миллионники.

### Иерархия работ

**Big Job (главная цель верхнего уровня):**
> Принять обоснованное стратегическое решение **и** провести его через стейкхолдеров (инвесторы / совет / партнёры / команда), чтобы развивать бизнес.

**Core Job** (выполняется `/case-team` полностью — точка покупки):
> Подготовить полный набор материалов решения бизнес-кейса под защиту.

**Small Jobs** (на том же уровне Core Job — НЕ выполняются `/case-team`, остаются за человеком):
- Принять финальное go/no-go решение
- Защитить решение лично перед стейкхолдерами (живая коммуникация)
- Внедрить стратегию операционно
- Договориться с конкретными партнёрами / нанять людей

### Контексты возникновения Core Job (триггеры из отзывов с дедлайнами)

| Триггер | Что именно происходит | Дедлайн |
|---|---|---|
| Питч инвестору в среду | Назначена встреча с фондом / частным инвестором / стратегическим партнёром | 7-14 дней |
| Совет директоров в пятницу | Регулярное заседание совета — нужны обоснованные цифры по KPI / квартальным результатам / новой инициативе | 3-10 дней |
| Конкурент сделал X | Внешний триггер: запуск продукта / снижение цен / заявление; команда требует стратегический ответ | 1-3 дня |
| Go/no-go нового продукта | Продуктовый комитет / партнёры требуют решения по запуску с обоснованием рынка / экономики / рисков | 7-21 день |

**Общее в триггерах:** во всех случаях есть **конкретный стейкхолдер и конкретный дедлайн**. Не абстрактное «нужна стратегия».

**Частотность Core Job:** 2-6 раз в год на одного фаундера (из анализа отзывов клиентов на конкурентов методом extract-jobs-from-reviews; [полный граф работ — в открытом репозитории](https://github.com/Suprrllys/case-team/blob/main/solution/analyst/jobs-and-segments-analysis.md)).

### Критерии успеха Core Job (измеримые, не абстрактные)

- **Скорость:** **4 часа** реального времени от запроса до готового пакета (vs 5-6 дней у команды из 5 человек)
- **Прослеживаемость:** **100% цифр** в финальных материалах имеют активную URL-ссылку на первичный источник
- **Защищаемость в Q&A:** на **каждую цифру** в основной презентации — кликабельная ссылка либо в slide, либо в приложении (правило «1 цифра = 1 источник»)
- **Воспроизводимость:** один запрос `/case-team` → структурно идентичный пакет из **5 файлов** (`.xlsx` финмодель, `.pptx` презентация, `SOLUTION.md`, `MANAGER-LOG.md`, research)
- **Низкий порог входа:** **1 команда** `/case-team` в Claude Code; **0 шагов** настройки MCP / subagents / pipeline

### Главная негативная эмоция до выполнения работы (из отзывов конкурентов)

**Страх «обнаружится фейк под вопросами стейкхолдера»** — не «дорого». Это объясняет, почему Big4 жив при 1-3 млн ₽ за один питч при наличии ChatGPT за подписку: клиенты Big4 покупают **защиту от позора через репутацию партнёра**, а не саму работу.

**Что меняет `/case-team`:** прозрачность методологии (каждая цифра прослеживается до источника в Decision Log) — функционально замещает «защиту через репутацию» для тех, кому Big4 недоступен.

### Где перехватить (точки контакта)

- Профессиональные Telegram-каналы по Product Management / стратегии
- Бизнес-школы и MBA-программы
- Конференции ProductSense / ProductCamp / EmergeConf
- Сарафан через комьюнити кейс-чемпионатов

---

## Appendix A2 · Конкуренты в multi-agent — матрица позиционирования {type:appendix}

**9 проанализированных конкурентов (по 3 слоям):**

**Прямые (multi-agent для бизнес-задач):**
- **Manus AI** — autonomous generalist; они = автономный generalist, мы = команда ролей с куратором смысла
- **Lindy** — операционная рутина; они = automation, мы = стратегические задачи
- **CrewAI / AutoGen** — конструкторы для разработчиков; они = инструменты сборки, мы = готовый продукт под класс задач

**Российские (operational, не strategic):**
- **GigaChat Enterprise** (Сбер) — для крупных корпов
- **Yandex AI Studio** — конструктор для разработчиков
- **Just AI Agent Platform** — Jay Knowledge Hub + Jay Flow

**Косвенные:**
- **Cognition Devin** — single-role vertical (SWE), 85% failure rate без супервизии — аргумент за нашу архитектуру «куратор смысла»
- **ChatGPT / Claude.ai** — главный когнитивный конкурент; наша работа начинается там, где ChatGPT не справляется с защитой
- **Big4-tier и «Яков и партнёры»** — нанимаются за защиту от позора, не за саму работу
- **Фрилансеры с биржи** — нет куратора смысла, никто не сшивает в питч-док

**Главный вывод:** мы занимаем **пустую клетку** в матрице позиционирования — готовый продукт под стратегический класс задач для одного человека без IT-ресурса. [Полная матрица 8 критериев × 9 конкурентов с обоснованиями](https://github.com/Suprrllys/case-team/blob/main/solution/analyst/practicum-award-context.md) — в открытом репозитории.

---

## Appendix A3 · Технологический стек {type:appendix}

| Компонент | Что | Обоснование выбора |
|---|---|---|
| **Модель** | Claude Opus 4.7 (1M context) | Длинный контекст для многошаговых кейсов с цепочкой источников; state-of-art reasoning |
| **Архитектура** | Claude Code subagents | Изолированные роли с собственными промптами, инструментами, папками |
| **Интеграции** | MCP-серверы (Notion, Google Drive), Web search / fetch | Доступ к внешним источникам без копирования вручную |
| **База знаний** | Локальные эталоны (Cup Moscow + Inno) + универсальные инструкции (финмодель, презентация) + каталог 18 типов слайдов + каталог исследовательских фреймворков | Дотренировка на реальных рабочих артефактах, не синтетике |
| **Методологии** | AJTBD-промпты Замесина (market-trends, competitor-research, differentiation-strategy, extract-jobs-from-reviews) интегрированы в `case-marketer` и `case-analyst` | Прямое использование методологии JTBD-консалтинга |
| **Дизайн-качество** | Скилл `claude-design` + 14 фазовых процедур (ai-slop, accessibility, hierarchy-rhythm, polish) | Контроль качества финального артефакта |
| **Сборка `.pptx`** | python-pptx + pre-flight overflow check + macOS PowerPoint blessing | Воспроизводимая программная сборка |

---

## Appendix A4 · Детальная финмодель и sensitivity {type:appendix}

**Реальные эмпирические данные пользователя (baseline):**
- Cup Moscow 2024 (Axenix): 5 человек × 140 чел.-часов на кейс
- Inno Case Hack 2025 (Askona): 5 человек × 40 чел.-часов на кейс
- Средний кейс: ~90 чел.-часов

**Ставки команды (средневзвешенная middle):**
- PM ~1190 ₽/час · Аналитик ~1070 ₽/час · Финансист ~1190 ₽/час · Маркетолог ~1010 ₽/час · Дизайнер ~950 ₽/час
- **Округлённая средневзвешенная:** 1100 ₽/час

**Стоимость 1 кейса (в человеческой команде):**
- In-house (90 ч × 1100 ₽): **99 000 ₽**
- Big4-tier (×4 multiplier): **396 000 ₽**

**Стоимость 1 кейса (с агентами, внутренний расход для прозрачности):**
- Время менеджера (3.5 ч × 1500 ₽): **5 250 ₽**
- Токены Claude (8M input + 1.5M output, $77.5 × 73.34 ₽/$): **5 680 ₽**
- **Итого:** ~**10 930 ₽**

**Sensitivity ±20% по 3 параметрам:** устойчиво в диапазоне **84-98%** экономии.

**Для клиента (D10 подача А):** **$0 дополнительно**, если есть Claude подписка ($20-100/мес уже оплачена для других задач).

Все источники цифр (Anthropic Pricing, ЦБ РФ, dreamjob.ru, fless.pro) — Приложение A0. [Полная финмодель с формулами и sensitivity](https://github.com/Suprrllys/case-team/blob/main/solution/financier/unit-economics.md) — в открытом репозитории.

---

## Appendix A5 · Каскад целей маркетинга (4 уровня) {type:appendix}

**Уровень 1 — Бизнес-цель:**
Выход в финалисты Practicum Award + борьба за приз номинации (500k ₽ + грант Yandex AI Studio) или спецприз «Будущее за ним» (150k ₽ для опыта до 2 лет).

**Уровень 2 — Маркетинговые цели (что должно произойти с восприятием жюри):**
- M1: Жюри запоминает проект как «новый класс инструмента», не «ещё одну multi-agent систему»
- M2: Жюри верит цифрам экономии (84-98%) и не задаёт риторическое «слишком красиво»
- M3: Жюри воспринимает заявку как методологически зрелую, не как пет-проект
- M4: Жюри ассоциирует автора с продуктовой и методологической культурой РФ
- M5: Жюри видит мета-демо как уникальный аргумент, не маркетинговый трюк

**Уровень 3 — Коммуникационные цели (какие сообщения донести):**
- C1 (Slide 2): «Всё решение за 30 секунд через 3 цифры»
- C2 (Slide 3): «5 текущих способов либо дороги, либо медленны, либо без артефактов»
- C3 (Slide 4): «5 ролей с куратором смысла, физические артефакты, эталоны»
- C4 (Slide 6): «Категориальный сдвиг — в стоимости подписки на нейросеть»
- C5 (Slide 7): «Главный страх клиента — не дорого, а фейк под вопросами»

**Уровень 4 — Метрики успеха (адаптация Reach / Frequency / SOV / Brand-lift под конкурс):**
- ME1: Все 8 членов жюри Техно-номинации читают заявку целиком (отсутствие отказа на скрининге)
- ME2: One-liner «в стоимости подписки на нейросеть» повторяется на 5 слайдах (Cover / Slide 2 / Slide 6 / Slide 9 / финал)
- ME3: Попадание в топ-10 финалистов
- ME4: Brand-lift — упоминание категории «multi-agent под бизнес-кейсы» в обратной связи жюри

---

## Appendix A6 · Дорожная карта Now / Next / Later {type:appendix}

**Now (готово):**
- 5 агентов с явными ролями и арсеналами методов
- 2 эталона дотренировки (Cup Moscow + Inno) → 26 методологических логик
- 2 режима handoff (premium HTML / regular .pptx)
- Скилл `/case-team` — одна команда установки
- Реальная подача в Practicum Award собрана этой же командой (мета-демо)

**Next (1-3 мес после конкурса):**
- Расширение [открытого репозитория `Suprrllys/case-team`](https://github.com/Suprrllys/case-team) — выложить агентов и skill целиком (сейчас опубликованы материалы заявки)
- Расширение эталонной базы (антикризис, M&A, креативный бренд, оптимизация процессов)
- 3-5 pilot-запусков с B2B-клиентами в обмен на кейс-стади

**Later (3-12 мес):**
- Полноценный B2B-go-to-market (стартапы + малый бизнес + корп. L&D)
- Edu-канал через бизнес-школы и кейс-чемпионаты
- Возможная PRO-надстройка на базе Anthropic API для масштабных запусков

---

## Appendix A7 · Методологические источники (иерархия) {type:appendix}

**1. Эталоны команды (главная эмпирическая база):**
- Cup Moscow 2024 (решение для Axenix, авиахаб Звартноц) — стратегический B2G кейс
- Inno Case Hack 2025 (решение для Askona, A-Sleep) — стартап-маркетинговый кейс
- Из них извлечено 26 методологических логик; [разбор и материалы — в открытом репозитории](https://github.com/Suprrllys/case-team)

**2. Бизнес-классика (общая методология):**
- AJTBD / Jobs To Be Done (Christensen, Moesta) — формат сегментации по работам
- Mot-Moment Persona — JTBD-консалтинг, методологически популяризирован в РФ Ваней Замесиным
- AJTBD-промпты Замесина (`market-trends-research`, `competitor-research`, `differentiation-strategy`, `extract-jobs-from-reviews`) — интегрированы в `case-marketer` и `case-analyst` как методологический стандарт
- Value Proposition Canvas (Osterwalder)
- MoSCoW / RICE / Weighted Scoring — приоритизация
- AS-IS / TO-BE — Lean / Six Sigma process improvement
- Theory of Change — impact-инвестирование
- Big4-tier consulting structure (presale + методология + ритейнеры)

**3. Эвристики автора:**
- Бюджет слайда (1 тезис + 3-7 буллетов + 1-3 цифры + 1 визуал)
- Правило 50:50 текст/визуал на контентных слайдах
- Pre-flight overflow check для python-pptx

**Принцип:** каждое правило агента в `/case-team` имеет явную ссылку на свой уровень источника. Это снижает галлюцинации в стратегических цифрах.

---

## Appendix A8 · 4 параллельных проверки качества дизайна {type:appendix}

Перед сдачей презентации `case-designer` запускает 4 параллельных под-скилла из `claude-design`:

| Проверка | Что ловит | Под-скилл |
|---|---|---|
| **AI-slop** | Шаблонные формулировки, generic-фразы, эмодзи как декор, градиенты везде | `ai-slop-check.md` |
| **Accessibility** | Контраст 4.5:1, читаемость заголовков, цвет как единственный носитель смысла | `accessibility-audit.md` |
| **Hierarchy / Rhythm** | Один visual anchor per slide, ≤7±2 блоков, нет полотен текста, ритм карточек | `hierarchy-rhythm-review.md` |
| **Polish** | Финальный гейт перед сдачей | `polish-pass.md` |

Дополнительно:
- **Pre-flight overflow check** — формула `font × line_spacing × n_lines / 72 ≤ container_h` для каждого textbox
- **macOS PowerPoint blessing** — после генерации открыть в PowerPoint, «Восстановить», Save As

---

## Appendix A9 · Бизнес-модель (открытая) {type:appendix}

**Что есть `/case-team`:**
- Open-source skill для Claude Code
- Устанавливается одной командой в свою Claude-среду
- Стоимость для пользователя — **$0 дополнительно**, если есть Claude подписка ($20-100/мес уже оплачена для других задач)

**Это НЕ:**
- ❌ SaaS-стартап (нет отдельной подписки на продукт)
- ❌ «Free pilot до взлёта цены» — реально бесплатный инструмент
- ❌ Закрытая корпоративная разработка — open-source MIT

**Монетизация автора:**
- Узнаваемость в продуктовом сообществе
- Возможные консультации
- Карьерные возможности

**В будущем (после интеграции Claude Design в десктоп-приложение Anthropic):**
- Premium-режим (HTML) тоже автоматизируется — не потребует ручного шага загрузки YAML в браузер
- Сохраняется open-source модель базовой команды
- PRO-надстройки — опционально
