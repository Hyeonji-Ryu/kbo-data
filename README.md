# What is kbo_data

kbo_data는 한국프로야구 경기정보를 스크래핑하는 파이썬 패키지입니다.  
kbo_data is a Python package that provides Korean professional baseball game information by scraping.

## Required

이 패키지를 사용하기 위해서는 chrome driver가 필요합니다.
chrome driver는 

## How to Use

1. 원하는 날짜의 경기 스케쥴을 다운로드 받습니다.

    ```python
    from kbo_data.get.schdule import get_schedule
    # 2021년 4월부터 2021년 5월까지의 KBO 경기 스케쥴을 가져옵니다.
    schedule = get_schedule("202104","202105",chrome_driver)
    # 2020년, 2021년 4월의 KBO 경기 스케쥴을 가져옵니다.    
    schedule  = get_schedule("202004","202104",chrome_driver, only_month=True)
    ```

2. 해당 스케쥴을 바탕으로 경기 정보를 가져옵니다.

```python
    from kbo_data.get.data import get_data
    # 2021년 4월부터 2021년 5월까지의 KBO 경기 스케쥴을 가져옵니다.
    data = get_data(schedule, chrome_driver)
    # 2020년, 2021년 4월의 KBO 경기 스케쥴을 가져옵니다.    
    data = get_schedule("202004","202104",chrome_driver, only_month=True)
```
