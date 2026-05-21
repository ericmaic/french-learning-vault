---
tags:
  - home
cssclasses:
TQ_short_mode:
TQ_show_task_count:
---
```dataviewjs
// --- 最终版代码 ---

const { DateTime } = dv.luxon;

const now = DateTime.now();
const startOfDay = now.startOf('day');
const passedMinutesInDay = now.diff(startOfDay, 'minutes').minutes;
const dayPercent = (passedMinutesInDay / (24 * 60)) * 100;

const startOfWeek = now.startOf('week');
const passedHoursInWeek = now.diff(startOfWeek, 'hours').hours;
const weekPercent = (passedHoursInWeek / (7 * 24)) * 100;

const monthPercent = (now.day / now.daysInMonth) * 100;

const passedDaysInYear = now.ordinal;
const totalDaysInYear = now.isInLeapYear ? 366 : 365;
const yearPercent = (passedDaysInYear / totalDaysInYear) * 100;

const progressBars = [
    { label: "今日进度", value: passedMinutesInDay, max: 24 * 60, percent: dayPercent },
    { label: "本周进度", value: passedHoursInWeek, max: 7 * 24, percent: weekPercent },
    { label: "本月进度", value: now.day, max: now.daysInMonth, percent: monthPercent },
    { label: "本年进度", value: passedDaysInYear, max: totalDaysInYear, percent: yearPercent }
];

function createProgressBar(data) {
    const container = dv.el("div", "");
    container.style.display = "flex";
    container.style.alignItems = "center";
    container.style.marginBottom = "8px";

    const label = dv.el("span", `${data.label}：`);
    label.style.minWidth = "75px";
    label.style.flexShrink = "0";

    const progress = dv.el("progress", "");
    progress.setAttribute("value", data.value);
    progress.setAttribute("max", data.max);
    progress.style.flexGrow = "1";
    progress.style.width = "100%";
    progress.style.height = "14px";

    const percentage = dv.el("span", ` ${data.percent.toFixed(2)}%`);
    percentage.style.marginLeft = "10px";

    container.append(label, progress, percentage);
    dv.paragraph(container);
}

progressBars.forEach(bar => createProgressBar(bar));
```
---

# A. 总学习时长

```dataviewjs
const folder = "00-1-SUMMARY/A-Daily"; // 改成你的 Daily 文件夹路径

const fields = [
  "Pronunciation",
  "Vocabulary",
  "Grammar",
  "Course",
  "Reading",
  "Listening",
  "Speaking",
  "Writing"
];

let totals = {};
for (let field of fields) {
  totals[field] = 0;
}

for (let page of dv.pages(`"${folder}"`)) {
  for (let field of fields) {
    let value = page[field];

    if (value) {
      let minutes = Number(String(value).replace(/[^\d.]/g, ""));
      if (!isNaN(minutes)) {
        totals[field] += minutes;
      }
    }
  }
}

dv.table(
  ["Category", "Total Minutes", "Hours"],
  fields.map(field => [
    field,
    totals[field],
    (totals[field] / 60).toFixed(2)
  ])
);

let grandTotal = Object.values(totals).reduce((a, b) => a + b, 0);

dv.paragraph(`**Total Study / Activity Time:** ${grandTotal} minutes = ${(grandTotal / 60).toFixed(2)} hours`);
```

---

# B. Tasks Dashboard

> [!Todo]
> ```dataview
> TASK
> FROM "00-1-SUMMARY/A-Daily"
> WHERE !completed
> SORT file.name DESC
> ```

---



