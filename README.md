# Exam Revision Planner 溫書計劃表

**Tell it your exam date and your weak topics — it schedules the weakest topics first, spread across the days left. Free, no login, no server, your data never leaves your device.**

**輸入考試日期同每科弱點,自動排每日溫邊課,最弱嘅排最先。免費、免登入、無伺服器,資料唔會離開你部機。**

## Try it

Open `index.html` in any browser (double-click works, no server needed).

## Use it in 2 minutes

1. Set the exam date, hours per day, and weekend hours per day.
2. Add each subject (with a weight 1–5: how much of the grade it is) and its topics; rate each topic 1 (weak) to 3 (solid).
3. Press **生成計劃 Generate plan** — weakest topics land on the earliest days, weak ones get a second review session, the last day is light review only.
4. Each day, tick topics off as you finish them. Progress is saved in this browser.
5. If the plan cannot fit, it warns you honestly ("too many topics for the days left — cut scope or add hours"). Export the plan as CSV or print it.

## 兩分鐘用法

1. 設定考試日期、平日每日時數、週末每日時數。
2. 加科目 (比重 1–5,佔分愈多愈高) 同課題,每課信心評 1 (唔識) 到 3 (識)。
3. 撳 **生成計劃**,最弱嘅課排最先,弱項會多一次重溫,考前最後一日只係輕溫習。
4. 每日做完就剔,進度儲喺呢部瀏覽器。
5. 排唔晒會出警告,話你知要減範圍定加時數。可以匯出 CSV 或者列印。

## What it does

- Day-by-day plan from today to the day before the exam; never more than the daily capacity (weekday and weekend hours differ).
- Order: lowest confidence first, then highest subject weight, then earliest subject.
- Weak (confidence 1) topics get a second review session a few days later; last day is review only.
- Tick-off boxes with a progress bar, saved in localStorage; regenerating keeps ticked topics ticked.
- Over-capacity warning with minutes per topic; CSV export and print.

## Honest limits — what it does NOT do

- **No content.** It does not teach the topics or write notes. It only schedules what you tell it to revise.
- **No guarantee.** Following the plan does not guarantee a grade. The confidence ratings are your own judgement.
- **No reminders or notifications.** It cannot ping you. Check the plan yourself each morning.
- **No server storage, no sharing, no login.** One device, one browser.

## Tests

`node tests/test_planner.js` — 16 checks: every topic appears at least once, weak topics twice, never exceeds daily capacity, last day review only, weakest-first, weight order, weekend capacity, over-capacity warning, CSV export, ES5-only scan, zero external resources.
