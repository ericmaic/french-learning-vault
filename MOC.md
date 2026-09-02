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
# 法语学习资源

## 法语发音

- [发音](https://www.bilibili.com/video/BV1Fz4y1a793/?spm_id_from=333.1387.favlist.content.click)

## 你好法语

- [水木法语](https://www.bilibili.com/cheese/play/ep20794?csource=common_hp_favorite_null&spm_id_from=333.1387.0.0)
- [瓦西胖达法语Youtube](https://www.youtube.com/@%E7%93%A6%E8%A5%BF%E8%83%96%E8%BE%BE%E6%B3%95%E8%AF%AD/videos)
- [瓦西胖达法语Blibili](https://www.bilibili.com/video/BV1W8411J7Rp?spm_id_from=333.788.videopod.episodes&vd_source=0c9dfe986e4a33075d217923fef01e52&p=11)
- [×Clara_法语了解一下](https://www.bilibili.com/video/BV1V7411E7Zg/?spm_id_from=333.788.recommend_more_video.2&trackid=web_related_0.router-related-2589621-n4rxt.1788161439193.503&vd_source=0c9dfe986e4a33075d217923fef01e52)
- [刘雯雯法语](https://www.youtube.com/results?search_query=%E4%BD%A0%E5%A5%BD%E6%B3%95%E8%AF%ADa1+%E5%88%98%E9%9B%AF%E9%9B%AF)
- [瓦西胖达法语 List](https://www.youtube.com/results?search_query=%E7%93%A6%E8%A5%BF%E8%83%96%E8%BE%BE%E6%B3%95%E8%AF%AD)
- [瓦西胖达法语 List2](https://www.youtube.com/@%E7%93%A6%E8%A5%BF%E8%83%96%E8%BE%BE%E6%B3%95%E8%AF%AD/videos)
- [瓦西胖达你好法语leson 3](https://www.youtube.com/watch?v=fUJ5T_otNhc)
- [【188集】你好！法语A1教材音频+文本，（Unité 0-9）完整版](https://www.bilibili.com/video/BV1DL411879a/?spm_id_from=333.337.search-card.all.click&vd_source=0c9dfe986e4a33075d217923fef01e52)

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

```dataviewjs
const folder = "00-1-SUMMARY/A-Daily"; // 改成你的 Daily 文件夹路径

const fields = [
  "你好法语 A 1",
  "你好法语 A 2",
  "你好法语 B 1",
  "你好法语 B 2"
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



