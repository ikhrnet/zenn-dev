---
title: "Bashで1年のすべての日付を出力する"
emoji: "🗓"
type: "tech"
topics: ["bash"]
published: true
---

`date` の `-d` オプションを使います。

```bash
new_years_day="2022-01-01"

for i in $(seq 0 364)
do
  date +%Y-%m-%d -d "$new_years_day + $i day"
done
```

365日が出力されます。

```txt
2022-01-01
2022-01-02
2022-01-03
[...]
2022-12-29
2022-12-30
2022-12-31
```

毎日出力されているファイルを、一括で処理する際に便利かと思います。
