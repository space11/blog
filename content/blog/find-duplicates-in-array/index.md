---
title: Find duplicates in array.
date: "2019-03-09T15:33:11"
author: "Borys"
---

### Chceck does array has duplicates, return: `true` or `false`
```JavaScript
function haseDuplicates(dataArray) {
    const entriesCount = {};
    const result = [];

    dataArray.forEach(item => {
      if (!entriesCount[item]) {
        entriesCount[item] = 0;
      }

      entriesCount[item] += 1;
    });

    const entries = Object.keys(entriesCount);

    entries.forEach(entry => {
      if (entriesCount[entry] >= 2) {
        result.push(entry);
      }
    });

    return result.length > 0;
}
```

### Find duplicates in an Array and return: `array` of duplicates - JavaScript
```JavaScript
function findDuplicates(dataArray) {
    const entriesCount = {};
    const result = [];

    dataArray.forEach(item => {
      if (!entriesCount[item]) {
        entriesCount[item] = 0;
      }

      entriesCount[item] += 1;
    });

    const entries = Object.keys(entriesCount);

    entries.forEach(entry => {
      if (entriesCount[entry] >= 2) {
        result.push(entry);
      }
    });

    return result;
}
```
