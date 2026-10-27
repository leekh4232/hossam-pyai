---
theme: ./slidev-themes/hossam
title: R 데이터 분석 · 요인(Factor)
layout: cover
---

# 요인(Factor)

<p class="sub">R 데이터 분석 · 09강</p>

---

## #01. 요인(factor) 만들기

`factor`는 값 혹은 값에 대한 범주를 의미하는 벡터이다.

---

### 1) 순서 없는 범주

<Grid cols="2">
<div>

<div class="kicker">성별 표현하기</div>

- factor가 포함할 수 있는 값은 범주 벡터에 나열된 값 중 하나만 가능함.

```r
gender <- factor('m', c('m', 'f'))
print(gender)
```

<Output>

```text
[1] m
Levels: m f
```

</Output>

</div>
<div>

<div class="kicker">범주를 벗어난 경우</div>

- 범주를 벗어난 값을 지정할 경우 `<NA>`가 됨.

```r
gender <- factor('k', c('m', 'f'))
print(gender)
```

<Output>

```text
[1] <NA>
Levels: m f
```

</Output>

</div>
</Grid>

---

### 2) 백터나 행렬을 값으로 갖는 요인

예를 들어 설문조사를 한다고 할 때, 요인은 응답자가 답할 수 있는 답의 종류를 제한함.

<div class="kicker">좋아하는 계절을 모두 고르기</div>

여름,가을은 범주에 속해 있지만, Winter는 범주에 속한 값이 아니므로 NA가 됨.

```r
fav_season <- factor(c('여름','가을','Winter'), c('봄', '여름', '가을', '겨울'))
print(fav_season)
```

<Output>

```text
[1] 여름 가을 <NA>
Levels: 봄 여름 가을 겨울
```

</Output>

---

### 3) 순서 있는 범주 만들기

<div class="kicker">방법(1) - factor 함수에 ordered=TRUE 라는 옵션값을 추가.</div>

두 번째 파라미터로 지정된 백터의 순서대로 결정됨.

```r
result <- factor('good', c('bad', 'normal', 'good'), ordered=TRUE)
print(result)
```

<Output>

```text
[1] good
Levels: bad < normal < good
```

</Output>

---

### 3) 순서 있는 범주 만들기 (계속)

<div class="kicker">방법(2) - ordered 함수 사용</div>

`ordered()`함수의 두 번째 파라미터로 전달하는 백터가 값의 순서가 됨.

```r
grade <- ordered(c(1, 2), c(4, 3, 2, 1))
print(grade)
```

<Output>

```text
[1] 1 2
Levels: 4 < 3 < 2 < 1
```

</Output>

---
layout: section
---

# #02. 요인과 관련된 함수(명령어)

---

### 1) 범주의 수 조회하기

- `nlevels()` 함수는 파라미터로 전달된 범주의 항목 수를 반환함.
- 보기의 항목수를 조회하는 것으로 이해하자.

<div class="kicker">범주의 항목 수 조회</div>

```r
fav_season <- factor(c('여름','가을','Winter'), c('봄', '여름', '가을', '겨울'))
cnt <- nlevels(fav_season)
print(cnt)
```

<Output>

```text
4
```

</Output>

---

### 2) 범주의 항목

`levels()` 함수는 범주의 항목 자체를 반환함.

<div class="kicker">범주의 항목 조회</div>

```r
fav_season <- factor(c('여름','가을','Winter'), c('봄', '여름', '가을', '겨울'))
lvl <- levels(fav_season)
print(lvl)
```

<Output>

```text
"봄" "여름" "가을" "겨울"
```

</Output>

---

### 3) 범주 변경

- 범주의 항목을 의미하는 `levels(범주)`에 새로운 범주를 의미하는 백터를 주입하여 범주의 항목들을 변경
- 기존에 저장되어 있던 값은 새롭게 적용된 범주 항목에 대응되는 값으로 변경됨.

---

### 3) 범주 변경 (계속)

<div class="kicker">범주 항목 변경하기</div>

```r
fav_season <- factor('여름', c('봄', '여름', '가을', '겨울'))
print(fav_season)

# 보기 항목을 영문으로 변경
levels(fav_season) <- c('Spring', 'Summer', 'Fall', 'Winter')

# 기존에 저장되어 있던 여름은 새로운 범주에 대응되는 Summer로 변경된다.
print(fav_season)
```

<Output>

```text
[1] 여름
Levels: 봄 여름 가을 겨울
[1] Summer
Levels: Spring Summer Fall Winter
```

</Output>
