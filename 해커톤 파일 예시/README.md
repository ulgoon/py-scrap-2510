# Web crawling Project

한국 프로스포츠 데이터 수집 프로젝트

## 주제

- K league data portal(https://data.kleague.com/)
- KBO(https://www.koreabaseball.com/Record/Crowd/GraphTeam.aspx)

데이터 수집

## 종류

- 경기데이터
    - 팀데이터
        - 시즌별 통산 승 무 패 득점 실점 카드 ..
    - 선수데이터(슈팅, 골, 기대득점, ..)
- 관중데이터
    - 구장별, 팀별 홈 원정 관중수
    - 해당 경기날 날씨(기상청 데이터 추가 스크래핑 필요)

## 방법

- kleague data portal은 동적사이트로 selenium을 이용하여 데이터에 접근
- 확보한 데이터의 정리는 pandas와 json 모듈로 진행

## 예시 데이터 형태

```python
data = {
    'football_data': {
        'team_stat': {},
        'player_stat': {},
        'crowd_stat': {
            'by_stadium': [],
            'by_team': [
                {
                    'team_name': 'Ulsan HD FC',
                    'played': 38
                    'home': 29219259,
                    'away': 82648,
                }
            ],
        },
    }
}
```

---

## 공공데이터가 필요할 경우

https://nia.or.kr/site/nia_kor/ex/bbs/View.do?cbIdx=99835&bcIdx=28652&parentSeq=28652