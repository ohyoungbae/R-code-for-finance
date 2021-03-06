# R-code-for-finance
R code for finance <br>
주식, 재무표, 데이터를 위해 만든 repo입니다. 

# 2018.12.08 UPDATE
1. 마감시황 업데이트 되었습니다
- 주말에 금요일 시황이 뜨지 않던 에러를 수정하였습니다.<br>

2. KRX종목테이블 항목이 추가되었습니다.
- 코스피,코스닥,코스넥 종목을 회사명,종목코드, 업종 등으로 나누도록 하였습니다.<br>
- 종목코드는 6자리를 따릅니다. 예) 005930<br>
- function 사용법은 아래 '코드이용방법'을 참고해 주시기 바랍니다.<br>

3. 기존에 KRX데이터 때문에 실행이 불가능 했던 코드들을 수정하였습니다.
- 재무제표 코드와 k-score 코드가 실행가능 한 상태로 되었습니다. <br>

4. 현재 홍콩주식은 사용이 불가한 상태입니다. 하루 빨리 수정하도록 하겠습니다.

# 2018.12.05 UPDATE
1. 마감시황 업데이트 되었습니다.
- DATE인식이 안되어서, 마감시황을 이용할 수 없다는 에러를 수정하였습니다.<br>
- 12월 5일 부시 전 대통령의 장례식으로 인한 갑작스러운 미국휴장에 코드가 시황을 인식하지 못하는 에러를 수정하였습니다.<br>
- 미국 뿐만 아니라 다른 나라 또한 예기치 못한 휴장을 방지하기 위해 코드를 수정하였습니다. 


# 코드 이용방법
- 마감시황은 현재 미국, 중국, 일본, 대만, 한국, WTI, 금/은 시황을 제공하며, 일 거래 그래프도 함께 제공됩니다. 마감시황에서 뜨는 plot과 가격, 가격변동(chg)은 실시간 value를 제공하며, 미국과 WTI를 제외한 나머지 시황은 오후5시에 제공됩니다.(사이트의 사정에 따라 시황이 뜨는 시간이 다를 수 있습니다.) <br>

- 홍콩주식과 중국주식은 홍콩재무제표, 중국재무제표를 나타냅니다. <br>

- 홍콩주식과 중국주식내 주식코드 테이블은 그냥 참고용이지, function과는 독립적이므로 원치 않으신 분들은 function만 import해도 됩니다. <br>

- 중국주식 이용방법 : cn_fs('코드번호') ex) cn_fs('000002') <br>

- 재무재표는 한국재무재표를 나타냅니다. 이용방법 kr_fs('기업명'), ex) kr_fs('삼성전자')<br>

- KRX종목 테이블 사용법 : 콘솔창에 krx_stock_table()을 치면 전 종목이 테이블 형태로 띄어 집니다. krx_stock_table(save_csv_file = TRUE)을 입력하실 경우, 전 종목이 띄어짐과 동시에 csv파일로 기본 디렉토리에 저장됩니다(파일명:KRX__테이블.csv)
krx_stock_table('kospi')를 입력하실 경우, kospi종목만, krx_stock_table('kosdaq')을 입력하실경우 kosdaq종목만, krx_stock_table('konex')를 입력하실 경우, konex종목만 띄우도록 수정하였습니다. 시장 명 뒤에 TRUE를 넣을 경우 csv파일로 저장됩니다, 예) krx_stock_table('kospi',TRUE)

- k-score는 알트만의 z-core를 본 떠 만든 한국형 모델 k-score입니다. 상장되어 있는 전 종목에 이 모델을 적용시키는 코드이며, 한눈에 기업의 부실정도를 측정가능하도록 하는 모델입니다.<br>
reference: <br>
[1] https://m.blog.naver.com/PostView.nhn?blogId=haan79&logNo=10158008764&proxyReferer=https%3A%2F%2Fwww.google.co.kr%2F<br>
[2] https://finata.blog.me/221191125946

- 한국주식 info는 한국 상장기업에 대한 기본 정보를 제공합니다. 코드이용방법 : kr_get_st('6자리코드') 예) kr_get_st('005930')<br>

