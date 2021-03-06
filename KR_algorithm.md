# algorithm

정렬 알고리즘 노트

정렬: 뭔가를 정리하는 것

<b><버블 정렬 (bubble sort)></b>

- 서로 인접한 두 원소를 검사하여 정렬하는 것
- 비효율적인 알고리즘
- 방법:
  1. 배열의 2개의 아이템을 선택하고, 비교하고, 왼쪽이 오른쪽보다 크다면 교환
  2. 오른쪽으로 이동해서 1번 프로세스를 반복
  3. 2번이 끝나면, 전부 정렬이 될때까지 싸이클을 반복
- 시간복잡도: O(n^2)<br />
  이유: 한 싸이클에 n-1번, 최악의 경우 (n-1)^2까지 비교하므로<br/> 
- 예시

![Bubble-sort-example-300px](https://user-images.githubusercontent.com/87036999/155900935-824308a5-4697-4267-8e52-0075f2be6341.gif)

<b><선택 정렬 (selection sort)></b>

- 가장 작은 것을 선택해서 제일 앞으로 보내는 것
- 비효율적인 알고리즘
- 방법:
  1. 배열의 전체 아이템중 가장 작은 아이템의 위치를 변수에 저장
  2. 가장 작은 숫자의 위치를 첫번째 아이템과 바꿈
  3. 정렬되지 않은 부분만 가지고 (2번에서 정렬된 아이템 빼고) 1, 2번을 반복
- 시간복잡도: O(n^2)
- 예시
  
![Selection-Sort-Gif](https://user-images.githubusercontent.com/87036999/155901039-09d48577-e02b-436d-96b8-7dc49976dea2.gif)

<b><삽입 정렬 (insertion sort)></b>

- 각 숫자를 적절한 위치에 상입하는 방법 (버정과 선정보단 빠름)
- 방법:
  1. 배열의 인덱스 1에 있는 아이템을 가지고 왼쪽의 것과 비교, 크다면 두고 작다면 바꿈
  2. 1번에서 선택한 아이템으로 바꿀 수 없을때까지 반복
  3. 1, 2번을 정렬될때까지 반복, 하지만 싸이클 후 인덱스를 1씩 늘림 (인덱스 2, 인덱스 3….)
- 시간복잡도: O(n^2)
- 거의 정렬된 상태에선 삽입 정렬이 어떤 알고리즘보다도 빠름
- 예시
  
![Insertion-sort-example-300px](https://user-images.githubusercontent.com/87036999/155901049-4d6b18e6-ce17-4f15-93fb-8cadb9aef206.gif)

<b><퀵 정렬 (quick sort)></b>
  
- 특정한 값을 기준으로 큰 숫자와 작은 숫자를 나누는 것
- 방법: 
  1. 피벗이라는 기준 값을 배열의 맨 첫(혹은 다른) 아이템으로 설정함
  2. 왼쪽에서 오른쪽으로 이동시키며 피벗보다 큰값, 오른쪽에서 왼쪽은 작은값을 선택
  3. 2번의 큰값과 작은값을 바꿔줌 (값이 엇갈리면 작은값과 피벗을바꾸고 그걸 피벗으로 바꿈)
- 시간복잡도: O(n * log(n)) → 최악엔 O(n^2)
- 예시
  
![Quicksort-example](https://user-images.githubusercontent.com/87036999/155901081-80b28267-6236-42be-ba09-89db39ac98e8.gif)

<b><병합 정렬 (merge sort)></b>
  
- 일단 반으로 나누고 나중에 합쳐서 정렬하는 것
- 방법:
  1. 배열을 계속 반으로 쪼개서 한 아이템으로 배열을 꾸리도록 부할시킴
  2. 2개씩 페어로 아이템을 비교하고 정렬되게 한 후 합침
  3. 2에서 합쳐진 집합들을 2개씩 페어로 다시 정렬되게 한 후 합침
  4. 정렬될때까지 같은 걸 반복
- 시간복잡도: O(n * log(n)) 보장됨
- 예시
  
![Merge-sort-example-300px](https://user-images.githubusercontent.com/87036999/155901101-29666b96-16d1-4f48-9491-e3ef06615a1d.gif)

<b><선형 검색 (linear search)></b>

- 방법: 배열의 1번째 아이템부터 끝까지 차례대로 특정값이 맞는지를 확인함
- 시간복잡도: O(n)
- 예시
  
![ucuj7xc3u0m69xeuglp0](https://user-images.githubusercontent.com/87036999/155901122-2a554d87-785e-4ca5-91ef-f13c7ac2dd31.gif)

<b><이진 검색 (binary search)></b>

- 제한: 정렬된 배열 (Sorted Array)에서만 사용 가능
- 반으로 가르는걸 binary라고 함
- 방법: 
  1. 배열의 정중앙에서 시작해서, 그 가운데 숫자가 찾고 싶은 값보다 큰지 작은지를 비교함
  2. 크면 아이템의 왼쪽으로, 작으면 아이템의 오른쪽으로 감
  3. 이동한 쪽에서 다시 1, 2번을 검색 될때까지 반복
- 시간복잡도: O(log(n))
- 예시
  
![ucuj7xc3u0m69xeuglp0](https://user-images.githubusercontent.com/87036999/155901207-77b2a556-af56-45dc-ad25-dc4d0d836db6.gif)
  
<b><재귀함수 (recursion function)></b>
  
- 종료 조건이 충족될 때까지 자기 자신을 호출하는 것
- 함수(메서드) 안에 자기 자신을 호출하는 것 
- 예시
  
![recursion1-4cf47bead28bba934db2a269fe65dcb7](https://user-images.githubusercontent.com/87036999/155901235-148a7e40-02af-461d-907d-791dc8bd18d7.gif)
