# npm vs yarn vs pnpm - Cheat Sheet

## مقدمه
سه ابزار محبوب برای مدیریت پکیج‌های جاوا اسکریپت هستند. هر کدام ویژگی‌های خاص خود را دارند و در سناریوهای مختلف مورد استفاده قرار می‌گیرند. **npm**، **yarn** و **pnpm**

---

## تفاوت ‌های اصلی
| ویژگی                      |                    npm |                 yarn |                pnpm |
|----------------------------|------------------------|----------------------|---------------------|
| **سرعت**                   |                  متوسط |      npm سریع ‌تر از |      بسیار سریع‌ تر |
| **استفاده از دیسک**        |                  بیشتر |                بیشتر |                کمتر |
| **حفظ یک پارچگی**          | `package-lock.json` با |      `yarn.lock`  با | `pnpm-lock.yaml` با |
| **`cache` مدیریت**         |             بهینه نیست |            بهینه شده |     بسیار بهینه‌ تر |
| **`node_modules`حجم**      |                   بزرگ |                 بزرگ |            کوچک ‌تر |
| **`monorepo` پشتیبانی از** |                   ضعیف | `workspaces` بله، با |           بسیار قوی |
| **حالت موازی نصب پکیج**    |                    خیر |                  بله |                 بله |
| **اجرای اسکریپت‌ها**       |              `npm run` |           `yarn run` |          `pnpm run` |
| **`PnP` پشتیبانی از**      |                    خیر |                  بله |                 بله |

---

### مدیریت پکیج ‌ها
| عملیات            |                          npm |                 yarn |                      pnpm |
|:------------------|-----------------------------:|---------------------:|--------------------------:|
| نصب تمام پکیج ‌ها |                `npm install` |       `yarn install` |            `pnpm install` |
| نصب یک پکیج       |            `npm install pkg` |       `yarn add pkg` |            `pnpm add pkg` |
| نصب dev پکیج      | `npm install pkg --save-dev` | `yarn add pkg --dev` | `pnpm add pkg --save-dev` |
| حذف پکیج          |          `npm uninstall pkg` |    `yarn remove pkg` |         `pnpm remove pkg` |
| آپدیت پکیج‌ها     |                 `npm update` |       `yarn upgrade` |             `pnpm update` |

---

### مدیریت کش
| عملیات     |                       npm |               yarn |               pnpm |
|:-----------|--------------------------:|-------------------:|-------------------:|
| پاکسازی کش | `npm cache clean --force` | `yarn cache clean` | `pnpm store prune` |

---

### بررسی امنیت و مشکلات پکیج ‌ها
| عملیات              |         npm |         yarn |         pnpm |
|:--------------------|------------:|-------------:|-------------:|
| بررسی مشکلات امنیتی | `npm audit` | `yarn audit` | `pnpm audit` |

---

### مدیریت نسخه ‌ها
| عملیات           |            npm |            yarn |            pnpm |
|:-----------------|---------------:|----------------:|----------------:|
| نمایش نسخه ابزار |       `npm -v` |       `yarn -v` |       `pnpm -v` |
| نمایش نسخه پکیج  | `npm list pkg` | `yarn list pkg` | `pnpm list pkg` |

---

### Monorepo استفاده در 
| عملیات                 |           npm |              yarn |                pnpm |
|:-----------------------|--------------:|------------------:|--------------------:|
| workspaces پشتیبانی از |   بله (محدود) |               بله | (yarn بهتر از ) بله |
| workspaces ایجاد       | `npm init -w` | `yarn workspaces` |      `pnpm init -w` |

---

## مقایسه دستورات مدیریتی
| دستور                  |                    npm |                     yarn |                 pnpm |
|:-----------------------|-----------------------:|-------------------------:|---------------------:|
| مقداردهی اولیه پکیج    |             `npm init` |              `yarn init` |          `pnpm init` |
| اجرای یک اسکریپت       |       `npm run script` |        `yarn run script` |    `pnpm run script` |
| اضافه کردن پکیج سراسری |   `npm install -g pkg` |    `yarn global add pkg` |    `pnpm add -g pkg` |
| حذف پکیج سراسری        | `npm uninstall -g pkg` | `yarn global remove pkg` | `pnpm remove -g pkg` |
