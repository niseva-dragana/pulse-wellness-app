# Pulse — AI-Powered Youth Wellness Platform

> A personalized wellness check-in app for teenagers, powered by the Claude AI API and grounded in real HBSC (Health Behaviour in School-aged Children) international research data.

---

## 1. Problem

Adolescent mental health is declining globally. HBSC data shows 42% of teens report weekly high stress, only 12–28% meet daily activity guidelines, and average sleep at age 15 is 7.2 hours — well below the recommended 8–10. Accessible, engaging, and personalized wellness tools for this age group are virtually nonexistent.

## 2. Target Group

Teenagers aged 11–18, particularly those in secondary education. Secondary users include school counselors, teachers, and parents seeking insight into youth wellbeing.

## 3. How It Works

Pulse is a four-screen React web application:

- **Home** — Live HBSC statistics, trend charts, and entry point to the app
- **Daily Check-in** — A guided 4-step flow collecting mood, sleep, stress, social connection, and physical activity
- **AI Insights** — The check-in data is sent to the Claude API, which returns a personalized Wellness Score, empathetic headline, three research-backed insight cards, a daily micro-challenge, and an affirmation
- **Data Explorer** — Five interactive charts built on real HBSC data (life satisfaction, sleep gaps, stress sources, activity rates, mental health symptoms)

## 4. Expected Impact

- Builds emotional self-awareness and healthy habit formation in teenagers
- Reduces stigma around mental health through a non-clinical, engaging interface
- Educates users on real peer-health statistics through interactive data visualization
- Demonstrates responsible, human-centered AI use in a public health context

---

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | React 18 (JSX) |
| Charts | Recharts |
| Icons | Lucide React |
| AI | Anthropic Claude API (`claude-sonnet-4-20250514`) |
| Fonts | Google Fonts — Sora |
| Styling | Inline CSS + CSS-in-JS (no external CSS framework) |
| Deployment | Vercel (recommended) |
| Data | HBSC International Study (hbsc.org) |

---

## Getting Started

### Prerequisites

- Node.js v18+ — [nodejs.org](https://nodejs.org)
- An Anthropic API key — [console.anthropic.com](https://console.anthropic.com)

### Installation

```bash
npm create vite@latest pulse-app -- --template react
cd pulse-app
npm install recharts lucide-react
```

Replace `src/App.jsx` with `PulseApp.jsx`, then:

```bash
npm run dev
```

Open `http://localhost:5173`.

### API Key

In `PulseApp.jsx`, find the `callAI` function and add your key to the fetch headers:

```js
headers: {
  "Content-Type": "application/json",
  "x-api-key": "your-anthropic-api-key-here",
  "anthropic-version": "2023-06-01",
  "anthropic-dangerous-direct-browser-access": "true",
}
```

> Note: For production, move the API call to a backend or serverless function to keep your key secure.

### Deploy to Vercel

```bash
npm install -g vercel
npm run build
vercel --prod
```

Or connect your GitHub repo at [vercel.com](https://vercel.com) for automatic deployments on every push.

---

## Project Structure

```
pulse-app/
├── src/
│   └── App.jsx        # Full application (single-file component)
├── public/
├── index.html
├── package.json
└── vite.config.js
```

---

## Dependencies

```json
"recharts": "^2.x",
"lucide-react": "^0.383.0"
```

---

## License

MIT — free to use, modify, and distribute.

---
---

# Pulse — Платформа за добросостојба на млади, поддржана со вештачка интелигенција

> Апликација за персонализиран дневен wellness check-in наменета за тинејџери, поддржана од Claude AI API и базирана на реални податоци од меѓународната HBSC студија (Health Behaviour in School-aged Children).

---

## 1. Проблем

Менталното здравје на младите е во пад на глобално ниво. Според HBSC податоците, 42% од тинејџерите пријавуваат висок стрес на неделна основа, само 12–28% ги исполнуваат препораките за дневна физичка активност, а просечниот сон кај 15-годишниците изнесува 7,2 часа — далеку под препорачаните 8–10. Пристапни, ангажирачки и персонализирани алатки за оваа возрасна група практично не постојат.

## 2. Целна група

Млади на возраст 11–18 години, особено ученици во средно образование. Секундарни корисници се училишни психолози, наставници и родители кои сакаат подлабок увид во добросостојбата на своите ученици и деца.

## 3. Kako функционира апликацијата

Pulse е React веб-апликација со четири екрани:

- **Почетна страница** — Живи HBSC статистики, трендови и влез во апликацијата
- **Дневен Check-in** — Водена форма во 4 чекори: расположение, сон, стрес, социјална поврзаност и физичка активност
- **AI Увиди** — Податоците се испраќаат до Claude API, кој враќа персонализиран Wellness Score, емпатична порака, три увиди поткрепени со истражување, дневен микро-предизвик и афирмација
- **Истражување на податоци** — Пет интерактивни графикони базирани на реални HBSC наоди: задоволство со животот, разлика во спиење, извори на стрес, физичка активност и ментални симптоми

## 4. Очекуван Impact

- Градење на емоционална свесност и здрави навики кај младите
- Намалување на стигмата поврзана со менталното здравје преку пријатен, нео-клинички интерфејс
- Едукација на корисниците преку интерактивна визуелизација на реални истражувачки податоци
- Пример за одговорна и хуманоцентрична примена на вештачка интелигенција во јавното здравје

---

## Технолошки стек

| Слој | Технологија |
|---|---|
| Framework | React 18 (JSX) |
| Графикони | Recharts |
| Икони | Lucide React |
| AI | Anthropic Claude API (`claude-sonnet-4-20250514`) |
| Фонтови | Google Fonts — Sora |
| Стилизација | Inline CSS + CSS-in-JS (без надворешен CSS framework) |
| Деплојмент | Vercel (препорачано) |
| Податоци | HBSC International Study (hbsc.org) |

---

## Инсталација

### Предуслови

- Node.js v18+ — [nodejs.org](https://nodejs.org)
- Anthropic API клуч — [console.anthropic.com](https://console.anthropic.com)

### Чекори

```bash
npm create vite@latest pulse-app -- --template react
cd pulse-app
npm install recharts lucide-react
```

Замени го `src/App.jsx` со `PulseApp.jsx`, потоа:

```bash
npm run dev
```

Отвори `http://localhost:5173`.

### API Клуч

Во `PulseApp.jsx`, пронајди ја функцијата `callAI` и додај го клучот во headers:

```js
headers: {
  "Content-Type": "application/json",
  "x-api-key": "твојот-anthropic-api-клуч",
  "anthropic-version": "2023-06-01",
  "anthropic-dangerous-direct-browser-access": "true",
}
```

> Напомена: За продукција, API повикот треба да се премести на backend или serverless функција за да не се изложи клучот јавно.

### Деплојмент на Vercel

```bash
npm install -g vercel
npm run build
vercel --prod
```

Или поврзи го GitHub репозиториумот директно на [vercel.com](https://vercel.com) за автоматски деплојмент при секој push.

---

## Структура на проектот

```
pulse-app/
├── src/
│   └── App.jsx        # Целосна апликација (single-file компонента)
├── public/
├── index.html
├── package.json
└── vite.config.js
```

---

## Зависности

```json
"recharts": "^2.x",
"lucide-react": "^0.383.0"
```

---

## Лиценца

MIT — слободно за употреба, модификација и дистрибуција.
