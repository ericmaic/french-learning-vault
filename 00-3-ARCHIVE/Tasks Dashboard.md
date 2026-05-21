# Tasks Completed

```dataviewjs
// 只统计这个文件夹下的任务
const folder = "00-1-SUMMARY/A-Daily"; // 改成你的 Daily 文件夹路径

let tasks = dv.pages(`"${folder}"`)
  .file.tasks
  .where(t => t.completed && t.completion);

// 按月份分组
let groups = tasks.groupBy(t => {
  const d = t.completion;
  return `${d.year}-${String(d.month).padStart(2, "0")}`;
});

// 按月份倒序显示
for (let group of groups.sort(g => g.key, "desc")) {
  dv.header(2, group.key);

  dv.taskList(
    group.rows.sort(t => t.completion, "desc"),
    false
  );
}
```


---
