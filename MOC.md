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

**根据 Daily 通过 Tracker 获取为：**

<% tp.file.cursor() %>

---


# B. Tasks and Review
---
![[Learning Tasks]]

---


# C. 快捷入口

- 通过 [[README]] 使用本仓库的所有工作流程与插件
- 通过 [[STATS.canvas]] 查看本仓库的数据


