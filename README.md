# venture — Business Copilot Suite for Claude Code

سوئیت دستیار بیزینسی برای Claude Code — مارکت‌ریسرچ، تحلیل رقبا، کشف مشتری، سنجش Product-Market Fit، استراتژی Go-to-Market و مدل کسب‌وکار؛ همه به هم زنجیر شده از طریق یک workspace مشترک برای هر «ونچر» (ایده، محصول یا کلاینت).

A business copilot suite for Claude Code — market research, competitor analysis, customer discovery, PMF assessment, GTM strategy, and business modeling, all chained through a shared per-venture workspace.

## نصب / Install

از داخل Claude Code (توصیه‌شده) / From inside Claude Code (recommended):

```
/plugin marketplace add heyparsadev/claude-venture-plugin
/plugin install venture@parsa-plugins
```

یا با CLI / Or via the CLI:

```bash
claude plugin marketplace add heyparsadev/claude-venture-plugin
claude plugin install venture@parsa-plugins
```

بعد یک سشن جدید Claude Code باز کن (پلاگین‌ها اول سشن لود می‌شن).
Then start a new Claude Code session (plugins load at session start).

## شروع سریع / Quick start

```
/venture:start          ← داشبورد + راهنما: کجای مسیری و قدم بعدی چیه
/venture:new-venture    ← ثبت یک ایده/بیزینس/کلاینت جدید
```

یا فقط به زبان خودت حرف بزن — مثلاً «برای این ایده مارکت ریسرچ کن» یا «رقبای این محصول رو تحلیل کن» — اسکیل درست خودش فعال می‌شه.

Or just talk naturally — e.g. "do market research for this idea" — the right skill auto-activates.

## ماژول‌ها / Modules

| دستور | کار |
|---|---|
| `/venture:start` | ارکستراتور: داشبورد ونچرها، درخت تصمیم، راهنمای استفاده |
| `/venture:new-venture` | اینتیک ونچر جدید و ساخت workspace |
| `/venture:market-research` | سایزینگ بازار (TAM/SAM/SOM)، ترندها، سگمنت‌ها |
| `/venture:competitors` | تحلیل رقبا: ماتریس مقایسه، SWOT، battlecard |
| `/venture:customers` | کشف مشتری: گاید مصاحبه (Mom Test)، پرسونا، سنتز |
| `/venture:pmf` | سنجش Product-Market Fit: تست Sean Ellis، اسکورکارد |
| `/venture:gtm` | استراتژی Go-to-Market: پوزیشنینگ، کانال، قیمت، لانچ |
| `/venture:model` | Lean Canvas و اقتصاد واحد (CAC/LTV/Payback) |
| `/venture:review` | «جلسه هیئت‌مدیره»: بازبینی کل ونچر + توصیه |

راهنمای کامل فارسی: [venture/PLAYBOOK.fa.md](venture/PLAYBOOK.fa.md)

## ساختار خروجی‌ها / Output structure

```
ventures/<slug>/
├── VENTURE.md        ← پروفایل + وضعیت ماژول‌ها + یافته‌های کلیدی + لاگ تصمیم‌ها
├── 01-discovery/     ├── 02-market/      ├── 03-competitors/
├── 04-pmf/           ├── 05-gtm/         └── 06-model/
```

هر اسکیل اول `VENTURE.md` را می‌خواند و آخر کار آن را به‌روز می‌کند — خروجی هر ماژول ورودی ماژول بعدی است.
