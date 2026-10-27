---
theme: ./slidev-themes/hossam
title: R 데이터 분석 · 리스트(List)
layout: cover
---

# 리스트(List)

<p class="sub">R 데이터 분석 · 10강</p>

---

## #01. 리스트 만들기

리스트는 `list()`함수에 `key=value` 형식의 파라미터들을 나열하여 생성한다.

```r
x <- list(name='hello', age=19, height=175, weight=85)
x
```

<Output>

```text
$name     'hello'
$age      19
$height   175
$weight   85
```

</Output>

---

## #02. 리스트의 값에 접근하기

데이터에 접근시는 `변수명$key` 형식으로 접근

<Grid cols="2">
<div>

<div class="kicker">이름에 접근하기</div>

```r
x$name
```

<Output>

```text
'hello'
```

</Output>

</div>
<div>

<div class="kicker">나이에 접근하기</div>

```r
x$age
```

<Output>

```text
19
```

</Output>

</div>
</Grid>

---

## #03. 복합적인 구조의 리스트

벡터나 요인도 리스트의 원소가 될 수 있다.

<div class="kicker">계층적 리스트</div>

```r
y <- list(
        name='world',
        phone=c('010','1234','5678'),
        gender=factor('m', c('m','f')))
y
```

<Output>

```text
$name      'world'
$phone     '010' '1234' '5678'
$genderm   Levels:
           'm''f'
```

</Output>

---

### 개별 값에 접근하기

```r
print(y$name)
print(y$phone)
print(y$phone[2])
print(y$gender)
```

<Output>

```text
[1] "world"
[1] "010"  "1234" "5678"
[1] "1234"
[1] m
Levels: m f
```

</Output>
