# time-merge
👉 **[View on npm](https://www.npmjs.com/package/time-merge)**
A lightweight Node.js utility to merge overlapping or near-continuous time ranges based on a given threshold (in milliseconds).  
Useful for merging active time intervals, event logs, or any timestamp ranges.

---

## 📦 Installation

Install the package from npm:

```bash
npm install time-merge
```

## 📦 Usage

```bash
const { mergeTimeRanges } = require("time-merge");

const ranges = [
  [1000, 2000],
  [2500, 4000],
  [3900, 4100],
  [8000, 9000],
  [9050, 9500]
];

const threshold = 200;

const result = mergeTimeRanges(ranges, threshold);

console.log(result);

// ✅ Expected Output:
// [
//   [1000, 2000],
//   [2500, 4100],
//   [8000, 9500]
// ]
```
