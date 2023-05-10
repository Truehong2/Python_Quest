# Code Peer Review Templete
- 코더 : 신노아 , 정선종
- 리뷰어 : 박기용


# PRT(PeerReviewTemplate)
각 항목을 스스로 확인하고 체크하고 확인하여 작성한 코드에 적용하세요.
- [x] 1.코드가 정상적으로 동작하나요?
- [x] 2.문제를 제대로 이해했나요?
- [x] 3.함수가 작동하는 방식을 잘 설명했나요?
- [ ] 4.발생 가능한 에러를 찾아서 디버깅을 했나요?
- [ ] 5.코드를 더 개선시켰나요?

# 예시
1. 코드의 작동 방식을 주석으로 기록합니다.
2. 코드의 작동 방식에 대한 개선 방법을 주석으로 기록합니다.
3. 참고한 링크 및 ChatGPT 프롬프트 명령어가 있다면 주석으로 남겨주세요.
```python

# n-gram

# Open the text file 
# 파일 열기
with open('/content/06TheAvengers.txt', 'r') as file:
    text = file.read()

# Convert all text to lowercase 
# 소문자 제거 
text = text.lower()

# Remove all symbols #symbol
# for 문으로 text 단어에서 특수 문자만 제거 
symbols = ['!', '"', '#', '$', '%', '&', "'", '(', ')', '*', '+', ',', '-', '.', '/', ':', ';', '<', '=', '>', '?', '@', '[', '\', ']', '^', '_', '`', '{', '|', '}', '~', '\n', '\t']
for symbol in symbols:
    text = text.replace(symbol, '')

# Split text into bi-gram words 
# 인덱싱으로 두개의 문자씩 결합
words = text.split()
bigrams = [words[i] + ' ' + words[i+1] for i in range(len(words)-1)]

# Count the frequency of each bigram
# bigram 의 빈도를 계산 .
bigram_counts = {}
for bigram in bigrams:
    if bigram in bigram_counts:
        bigram_counts[bigram] += 1
    else:
        bigram_counts[bigram] = 1

# Find the most frequent bigram
# max 로 가장 많이 나온 단어 와 빈도 찾기
most_frequent_bigram = max(bigram_counts, key=bigram_counts.get)
most_frequent_count = bigram_counts[most_frequent_bigram]

# Print the most frequent bigram and its count
# 출력.
print(f"The most frequent pair of bigrams is '{most_frequent_bigram}' with a count of {most_frequent_count}.")
```

# 참고 링크 및 코드 개선 여부
```python
#더 많은 자료를 참고해보면 좋을 듯
#
#
#
```
