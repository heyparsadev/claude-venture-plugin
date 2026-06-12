# biz — Business Copilot Suite for Claude Code

سوئیت دستیار بیزینسی برای Claude Code — مارکت‌ریسرچ، تحلیل رقبا، کشف مشتری، سنجش Product-Market Fit، استراتژی Go-to-Market و مدل کسب‌وکار؛ همه به هم زنجیر شده از طریق یک workspace مشترک برای هر «ونچر» (ایده، محصول یا کلاینت).

A business copilot suite for Claude Code — market research, competitor analysis, customer discovery, PMF assessment, GTM strategy, and business modeling, all chained through a shared per-venture workspace.

## نصب / Install

```bash
claude plugin marketplace add /Users/parsa/agent
claude plugin install biz@parsa-plugins
```

بعد یک سشن جدید Claude Code باز کن (پلاگین‌ها اول سشن لود می‌شن).
Then start a new Claude Code session (plugins load at session start).

## شروع سریع / Quick start

```
/biz:start          ← داشبورد + راهنما: کجای مسیری و قدم بعدی چیه
/biz:new-venture    ← ثبت یک ایده/بیزینس/کلاینت جدید
```

یا فقط به زبان خودت حرف بزن — مثلاً «برای این ایده مارکت ریسرچ کن» یا «رقبای این محصول رو تحلیل کن» — اسکیل درست خودش فعال می‌شه.

Or just talk naturally — e.g. "do market research for this idea" — the right skill auto-activates.

## ماژول‌ها / Modules

| دستور | کار |
|---|---|
| `/biz:start` | ارکستراتور: داشبورد ونچرها، درخت تصمیم، راهنمای استفاده |
| `/biz:new-venture` | اینتیک ونچر جدید و ساخت workspace |
| `/biz:market-research` | سایزینگ بازار (TAM/SAM/SOM)، ترندها، سگمنت‌ها |
| `/biz:competitors` | تحلیل رقبا: ماتریس مقایسه، SWOT، battlecard |
| `/biz:customers` | کشف مشتری: گاید مصاحبه (Mom Test)، پرسونا، سنتز |
| `/biz:pmf` | سنجش Product-Market Fit: تست Sean Ellis، اسکورکارد |
| `/biz:gtm` | استراتژی Go-to-Market: پوزیشنینگ، کانال، قیمت، لانچ |
| `/biz:model` | Lean Canvas و اقتصاد واحد (CAC/LTV/Payback) |
| `/biz:review` | «جلسه هیئت‌مدیره»: بازبینی کل ونچر + توصیه |

راهنمای کامل فارسی: [biz/PLAYBOOK.fa.md](biz/PLAYBOOK.fa.md)

## ساختار خروجی‌ها / Output structure

```
ventures/<slug>/
├── VENTURE.md        ← پروفایل + وضعیت ماژول‌ها + یافته‌های کلیدی + لاگ تصمیم‌ها
├── 01-discovery/     ├── 02-market/      ├── 03-competitors/
├── 04-pmf/           ├── 05-gtm/         └── 06-model/
```

هر اسکیل اول `VENTURE.md` را می‌خواند و آخر کار آن را به‌روز می‌کند — خروجی هر ماژول ورودی ماژول بعدی است.
