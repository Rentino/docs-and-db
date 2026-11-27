# docs-and-db — مستندات و دادهٔ رنتینو

مخزن مستندات، نمودارها و دادهٔ مورد نیاز توسعهٔ پروژهٔ رنتینو.
مسئولیت این بخش با آرشیا احمدی و محمدرضا زارع است.

---

## فهرست

| فایل / پوشه | توضیح |
|---|---|
| [`TEST-REPORT.md`](./TEST-REPORT.md) | **گزارش جامع تست** — تست واحد، یکپارچه، عملکرد، و فهرست باگ‌های پیدا و رفع‌شده |
| [`docs/ARCHITECTURE.md`](./docs/ARCHITECTURE.md) | معماری کلی سیستم |
| [`docs/DOMAIN.md`](./docs/DOMAIN.md) | دامنهٔ کسب‌وکار و موجودیت‌ها |
| [`docs/PROJECT.md`](./docs/PROJECT.md) | تعریف پروژه و اهداف |
| [`docs/STATUS.md`](./docs/STATUS.md) | وضعیت پیشرفت |
| [`docs/CONVENTIONS.md`](./docs/CONVENTIONS.md) | قواعد کدنویسی و نام‌گذاری |
| [`docs/software-engineering/`](./docs/software-engineering/) | مجموعهٔ کامل مستندات مهندسی نرم‌افزار فاز ۱ (گزارش، اسلاید، MSP، پرسشنامه، ابزارهای ساخت) |

---

## مخازن مرتبط

| مخزن | نقش |
|---|---|
| [`Frontend-Rentino`](https://github.com/Rentino/Frontend-Rentino) | رابط کاربری Next.js 16 |
| [`Backend-Rentino`](https://github.com/Rentino/Backend-Rentino) | API با NestJS 11 + Prisma 6 + PostgreSQL 17 |
| `docs-and-db` | همین مخزن — مستندات و داده |

---

## شروع سریع

```bash
# دیتابیس
docker compose up -d          # در مخزن Backend-Rentino

# بک‌اند
cd Backend-Rentino
npx prisma migrate deploy
npx prisma db seed
npm run start:dev             # http://localhost:8000/api/v1

# فرانت‌اند
cd ../Frontend-Rentino
npm install
cp .env.example .env.local
npm run dev                   # http://localhost:3000
```

### حساب‌های نمایشی

رمز همهٔ حساب‌ها: `rentino1234`

| ایمیل | نقش |
|---|---|
| `admin@rentino.ir` | ادمین |
| `provider@rentino.ir` | تأمین‌کننده |
| `provider2@rentino.ir` | تأمین‌کننده |
| `customer@rentino.ir` | مشتری |
| `customer2@rentino.ir` | مشتری |

---

## وضعیت مستندات

- [x] گزارش تست و اعتبارسنجی
- [x] انتقال مستندات فاز ۱ از پوشهٔ محلی به این مخزن
- [ ] نمودار ER دیتابیس (پیشنهاد برای مرحلهٔ بعد)
- [ ] مستندات API به‌صورت فایل جداگانه (فعلاً Swagger زنده روی `/docs` کافی است)
