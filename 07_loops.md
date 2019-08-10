# ループ

## 準備

1. [Google Colaboratory](https://research.google.com/colaboratory/)で「Python 3の新しいノートブック」を作る．
1. ノートブックの名前を「07」に変える．

## 演習

**問題** 単純なループ

```python
for i in range(10):
  print("Hello, World!")
```

**問題** リストに対するループ

```python
fruits = ['Apple', 'Orange', 'Grape']
for f in fruits:
  print(f)
```

**問題** タプルとセットで上と同様のことを試せ。

**問題** 辞書に対するループ

```python
dic = {'A':100, 'B':200, 'C':300}
for k in dic:
  print(k)
```

**問題** コンテナの要素の変換（方針1：新しいコンテナを作る）

```python
fruits = ['Apple', 'Orange', 'Grape']

results = []
for i in fruits:
  results.append(i.upper())

print(results)
```

```python
fruits = ['Apple', 'Orange', 'Grape']

# 内包表記
results = [i.upper() for i in fruits]

print(results)
```

**問題** コンテナの要素の変換（方針2：既存のコンテナを書き換える）

```python
# 方法1（他の言語と同じ）
fruits = ['Apple', 'Orange', 'Grape']

for i in range(len(fruits)):
  fruits[i] = fruits[i].upper()

print(fruits)
```

```python
# ダメな例
fruits = ['Apple', 'Orange', 'Grape']

for i in fruits:
 i = i.upper()

print(fruits)
```

```python
# 方法2（Python固有の書き方）
fruits = ['Apple', 'Orange', 'Grape']

for i, f in enumerate(fruits):
  fruits[i] = f.upper()

print(fruits)
```

```python
# ダメな例
fruits = ['Apple', 'Orange', 'Grape']

for i, f in enumerate(fruits):
  f = f.upper()

print(fruits)
```

**問題** While

```python
i = 10

while i > 0:
  print(i)
  i -= 1

print('Happy New Year!')
```

**問題（レポート課題）** 上のコードをforを使って書き換えよ。ヒント：https://docs.python.org/ja/3/library/stdtypes.html#typesseq-range でrangeの使い方を確認する。

**問題** breakとcontinue

```python
for i in range(10):
  if i == 5:
    break
  print(i)
```

```python
for i in range(10):
  if i == 5:
    continue
  print(i)
```

**問題** 入れ子のループ

```python
for i in range(1, 3):
  print(i)
  for ch in ['a', 'b', 'c']:
    print(f'  {ch}')
```

**問題（レポート課題）** xとyについての方程式3x+5y=100の解をすべて求めよ．ただし，xとyは正の整数とする．
