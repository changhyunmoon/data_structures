# DATA_STRUCTURES
## SORT
종류 : selection sort, bubble sort(파생형 cocktail shaker sort), quick sort, insertion sort, shell sort, merge sort, heap sort, radix sort, tree sort, tim sort, block merge sort, intro sort, countion sort, bogo sort, stupid sort, sleep sort, gravity sort

### selection sort(선택 정렬)
제자리 정렬 알고리즘의 하나
입력 배열 이외에 다른 추가 메모리를 요구하지 않는 정렬 방법이다.

과정
1. 주어진 배열 중에서 최솟값을 찾는다.
2. 그 값을 맨 앞에 위치한 값과 교체한다(pass).
3. 맨 처음 위치를 뺀 나머지 리스트를 같은 방법으로 교체한다.
4. 하나의 원소만 남을 때까지 위의 1~3 과정을 반복한다.
  

### bubble sort(선택 정렬)
서로 인접한 두 원소를 검사하여 정렬하는 알고리즘

과정
1. 첫 번째 자료와 두 번째 자료를, 두 번째 자료와 세 번째 자료를, 세 번째와 네 번째를, … 이런 식으로 (마지막-1)번째 자료와 마지막 자료를 비교하여 교환하면서 자료를 정렬한다.
2. 1회전을 수행하고 나면 가장 큰 자료가 맨 뒤로 이동하므로 2회전에서는 맨 끝에 있는 자료는 정렬에서 제외되고, 2회전을 수행하고 나면 끝에서 두 번째 자료까지는 정렬에서 제외된다. 이렇게 정렬을 1회전 수행할 때마다 정렬에서 제외되는 데이터가 하나씩 늘어난다.

### cocktail shaker sort(캌테일 셰이커 정렬)
칵테일 정렬(cocktail sort), 셰이커 정렬(shaker sort), 양방향 버블 정렬(bidirectional bubble sort) 또는 양방향 거품 정렬

과정
1. 좌측 지점부터 우측 지점으로 비교 작업을 진행합니다. 교환할 자료가 있으면 교환하면서 우측 지점까지 진행합니다.
2. 마지막에 교환이 이루어진 곳을 우측 지점으로 설정합니다.
3. 이번에는 반대로 우측 지점부터 좌측 지점으로 비교 작업을 진행합니다. 교환할 자료가 있으면 교환 합니다.
4. 마지막에 교환이 이루어진 곳을 좌측 지점으로 지정합니다.
5. 좌측 지점과 우측 지점이 교차하지 않았다면 아직 정렬할 자료가 남아있으니 앞의 작업을 계속 반복합니다. 비교/교환 작업이 진행되면서 정렬 범위가 조금씩 좁아지게 되며 결국은 더이상 비교할 것이 없는 정렬 완료 상태가 됩니다.


### quick sort(퀵 정렬)

과정
1. 리스트 안에 있는 한 요소를 선택한다. 이렇게 고른 원소를 피벗(pivot) 이라고 한다.
2. 피벗을 기준으로 피벗보다 작은 요소들은 모두 피벗의 왼쪽으로 옮겨지고 피벗보다 큰 요소들은 모두 피벗의 오른쪽으로 옮겨진다. (피벗을 중심으로 왼쪽: 피벗보다 작은 요소들, 오른쪽: 피벗보다 큰 요소들)
3. 피벗을 제외한 왼쪽 리스트와 오른쪽 리스트를 다시 정렬한다.
    분할된 부분 리스트에 대하여 순환 호출 을 이용하여 정렬을 반복한다.
    부분 리스트에서도 다시 피벗을 정하고 피벗을 기준으로 2개의 부분 리스트로 나누는 과정을 반복한다.
4. 부분 리스트들이 더 이상 분할이 불가능할 때까지 반복한다. 리스트의 크기가 0이나 1이 될 때까지 반복한다.

### insertion sort(삽입 정렬)

과정
1. 삽입 정렬은 두 번째 자료부터 시작하여 그 앞(왼쪽)의 자료들과 비교하여 삽입할 위치를 지정한 후 자료를 뒤로 옮기고 지정한 자리에 자료를 삽입하여 정렬하는 알고리즘이다.
2. 즉, 두 번째 자료는 첫 번째 자료, 세 번째 자료는 두 번째와 첫 번째 자료, 네 번째 자료는 세 번째, 두 번째, 첫 번째 자료와 비교한 후 자료가 삽입될 위치를 찾는다. 자료가 삽입될 위치를 찾았다면 그 위치에 자료를 삽입하기 위해 자료를 한 칸씩 뒤로 이동시킨다.
3. 처음 Key 값은 두 번째 자료부터 시작한다.

### shell sort(셸 정렬)
삽입 정렬을 보완한 알고리즘이다.
삽입 정렬의 문제점인 요소를 삽입할 때 이웃한 위치로만 이동한다는 문제점이다.

과정
1. 먼저 정렬해야 할 리스트를 일정한 기준에 따라 분류
2. 연속적이지 않은 여러 개의 부분 리스트를 생성
3. 각 부분 리스트를 삽입 정렬을 이용하여 정렬
4. 모든 부분 리스트가 정렬되면 다시 전체 리스트를 더 적은 개수의 부분 리스트로 만든 후에 알고리즘을 반복
5. 위의 과정을 부분 리스트의 개수가 1이 될 때까지 반복

### merge sort(합병 정렬)

과정
1. 2개의 리스트의 값들을 처음부터 하나씩 비교하여 두 개의 리스트의 값 중에서 더 작은 값을 새로운 리스트(sorted)로 옮긴다.
2. 2개의 리스트의 값들을 처음부터 하나씩 비교하여 두 개의 리스트의 값 중에서 더 작은 값을 새로운 리스트(sorted)로 옮긴다.
3. 만약 둘 중에서 하나의 리스트가 먼저 끝나게 되면 나머지 리스트의 값들을 전부 새로운 리스트(sorted)로 복사한다.
4. 새로운 리스트(sorted)를 원래의 리스트(list)로 옮긴다.







