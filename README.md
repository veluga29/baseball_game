# baseball_game
야구경기 구현

Step-1 : 간단 야구 게임 구현
1. 스트라이크(s), 볼(b), 안타(hit), 아웃(o)을 세기 위해 변수를 설정하고 0으로 초기화했습니다.
2. 투구 결과가 총 4가지이므로 Math 함수의 랜덤 수(범위 : 0 < x < 0.9999...)에 4를 곱하여 나온 수를 내림하여 정수로 만들었고, 그 수를 result 배열에서 투구 결과 경우의 수를 호출하는 index로 활용하였습니다.
3. if 함수를 사용해 스트라이크, 볼, 안타, 아웃, 스트라이크를 통한 아웃, 볼을 통한 안타 등의 경우의 수를 나눴고, 그에 따라 s, b, hit, out 변수를 조정했습니다.
4. 각 경우의 수를 고려하여, if 함수를 이용해 출력의 경우의 수도 나눴습니다.
5. 전체적으로 경기를 진행하는 main 함수를 만들어, 위의 1번 2번 3번 4번을 묶었습니다. 마지막엔 out이 3개 일 때, 안타(hit)와 아웃(o)을 초기화도록 설정했습니다.

Step-2 : 팀 데이터 입력 및 시합 기능 구현
1. index 파일에 input 태그를 이용하여, 팀 데이터 저장을 위한 레이아웃을 만들었습니다. 아래 쪽에는 경기 진행, 데이터 입력, 데이터 출력 버튼을 각각 만들었습니다.
2. '타자 정보'와 '팀 정보'는 생성자 함수로 만들어 객체를 만들기 편하게 했습니다. 투수는 그냥 객체로 만들어 사용했습니다.
3. 1~9번 타자의 이름과 타율은 객체로 만들어 새로운 배열에 넣었습니다. 그 후, '팀 이름', '타자 정보'가 담긴 배열, '투수 정보' 객체 총 3가지가 담긴 '팀1', '팀2' 객체를 생성했습니다.
4. index 파일의 '데이터 입력' 버튼을 누르면, 위의 1, 2, 3 번이 한 번에 동작하고 데이터 저장완료 메시지가 뜨게끔 함수를 만들었습니다. 이 함수는 팀1과 팀2 정보를 배열로 담아 반환합니다.
5. 4번의 함수 return값을 변수에 저장해, 데이터 출력 함수에서 팀정보를 호출하는데 활용했습니다. 이를 통해, index 파일의 '데이터 출력' 버튼을 누르면 두 팀의 정보가 출력되게끔 구현했습니다.


(처음에 '게임진행', '팀데이터 저장', '팀데이터 출력' 페이지를 각각 파일로 나누어 진행했으나, 도중에 페이지끼리의 데이터 전달에 어려움을 느껴 한 파일로 통합했습니다. 2단계에서 스스로 맘에 안드는 부분들이 많지만, 할 수 있는만큼 구현하고 제출합니다.)