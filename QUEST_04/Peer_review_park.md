# Code Peer Review Templete

- 코더 : 신노아 , 정선종
- 리뷰어 : 박기용

---

# PRT(PeerReviewTemplate)

각 항목을 스스로 확인하고 체크하고 확인하여 작성한 코드에 적용하세요.

- [v] 코드가 정상적으로 동작하고 주어진 문제를 해결했나요?
- [ ] 주석을 보고 작성자의 코드가 이해되었나요?
- [ ] 코드가 에러를 유발할 가능성이 있나요?
- [v] 코드 작성자가 코드를 제대로 이해하고 작성했나요? (직접 인터뷰해보기)
- [v] 코드가 간결한가요?

---python

# 물고기 클래스 만들기
# 부모 클래스.
class Fish:
    def __init__(self, name, speed):
        self.name = name
        self.speed = speed
    def swim(self):
        return f"{self.name} is swimming at {self.speed} m/s"

# 제러레이터 함수 정의
def fmg(fish_list):
    for fish in fish_list:
        yield fish.swim()

# 물고기 객체의 이름과 속도를 가진 리스트 만들기

fish_list = [Fish("Nemo", 3), Fish("Dory", 5), Fish("Marlin", 7), Fish("Bubbles", 2), Fish("Gill", 4)]

# 제너레이터를 활용하여 물고기들의 움직임 출력
print("물고기들의 움직임 (Using generator):")
fish_generator = fmg(fish_list)
for movement in fish_generator:
    print(movement)


# 컴프리헨션을 활용하여 물고기들의 움직임 출력
print("\n물고기들의 움직임 (Using list comprehension):")
fish_movements = [fish.swim() for fish in fish_list]
for movement in fish_movements:
    print(movement)
---

# 참고 링크 및 코드 개선 여부

 !!! 고생 하셨습ㄴ디ㅏ. !!!!
 저도 부모 클래스에 출력값을 같이 작성 했으면 좋았을 법 했어요 . ㅎㅎㅎ 
```python
# 
#
#
```


