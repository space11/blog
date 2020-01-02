---
title: How to use sed to find and replace text in files.
date: "2019-02-11T10:59:00"
author: "Borys"
---

### Replace string in text file using sed.

```sh
## find foo and replace with bar using sed
sed -i 's/foo/bar/g' inputFile.txt

## you can change the delimiter to keep syntax simple
sed -i 's+foo+bar+g' inputFile.txt
sed -i 's_word1_word2_g' inputFile.txt

## you can add I option to GNU sed to case insensitive search
sed -i 's/foo/bar/gI' inputFile.txt
sed -i 's_word1_word2_gI' inputFile.txt
```