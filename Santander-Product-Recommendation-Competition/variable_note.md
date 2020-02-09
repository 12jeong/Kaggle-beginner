# 데이터 특징 노트
|변수명|내용|타입|특징|아이디어|
|------|---|---|---|---|
|fecha_dato|월별날짜데이터|object|2015.01.28~2016.05.28 매달 28일에 데이터가 기록됨(17개월), 2015.07부터 데이터 수 증가 |연,월,일 분류 |
|ncodpers|고객고유번호|int64|| id값으로 학습시 사용 x, unique개수 볼 필요 있음|
|ind_empleado|고용지표 A B F N|object|99,9%가 N:not emplyee로 되어있음 |의미 없는 변수|
|pais_residencia|고객거주국가|object|99,5%가 ES로 기록되어 있음 |의미 없는 변수|
|sexo|고객성별 H V |object|H<V||
|age|고객나이|object -> int64| 범주형으로 되어있음, 23세가 가장 많음 |정수형으로 변환 필요
|fecha_alta|고객 첫 거래 날짜|object|날짜데이터| |
|ind_nuevo|6개월 이내 신규고객인 경우 1 | float64 -> int64  || dummy |
|antiguedad|거래 누적 기간(월)|object -> int64|-999999,NA 존재|수치형으로 취급 가능|
|indrel|1중요고객 99이번달중요고객해지|float64-> int64|99의 비율이 낮음|dummy|
|ult_fec_cli_1t|중요고객 만료날짜|object|결측치가 많음||
|indrel_1mes|월초기준 고객등급 1 2 P 3 4| object-> int64|'1'과 '1.0'이 다른값으로 존재, 1값이 대부분| '1','1.0' 등을 같게 하고 P등급을 편의상 5로 변환|
|tiprel_1mes|월초 고객 관계 유형 A I P R |object| A,I가 대부분||
|indresi| 거주지역이 은행과 일치하면S/아니면N |object|약 99.5% 일치함(S)|dummy 의미 없는 변수|
|indext|태어난국적이 은행과 다르면S/같으면N |object| 95%가 태어난 국적과 은행이 다름 (N)| 5%의 개인화추천 가능? dummy|
|conyuemp|은행 직원의 배우자 여부 1|object|결측치가 많음|dummy|
|canal_entrada|고객유입채널|object|상위 3개~5개 정도||
|indfall| 고객사망여부 N/S| object | 99.7%의 고객이 살아있음(N) | dummy 의미 없는 변수
|tipodom| 주소유형|float64|Addres type. 1, primary address, 1밖에 없음|제거 변수|
|cod_prov| 지방고객주소|float64-> int64|nomprov와 관련||
|nomprov|지방명|object|MADRID가 가장 많음 (25%?)||
|ind_actividad_cliente| 활성고객여부 1 0 |float64-> int64||dummy|
|renta| 가계총수입 | float64-> int64|0>1||
|segmento|고객유형|object|3개의 범주, 02>03>01||
|ind_ahor_fin_ult1| |int64|1의 비율이 낮음|dummy|
|ind_aval_fin_ult1| |int64|1의 비율이 낮음|dummy|
|ind_cco_fin_ult1| |int64|0<1|dummy|
|ind_cder_fin_ult1| |int64|1의 비율이 낮음|dummy|
|ind_cno_fin_ult1| |int64||dummy|
|ind_ctju_fin_ult1| |int64||dummy|
|ind_ctma_fin_ult1| |int64|1의 비율이 낮음|dummy|
|ind_ctop_fin_ult1| |int64||dummy|
|ind_ctpp_fin_ult1| |int64||dummy|
|ind_deco_fin_ult1| |int64|1의 비율이 낮음|dummy|
|ind_deme_fin_ult1| |int64|1의 비율이 낮음|dummy|
|ind_dela_fin_ult1| |int64||dummy|
|ind_ecue_fin_ult1| |int64||dummy|
|ind_fond_fin_ult1| |int64||dummy|
|ind_hip_fin_ult1| |int64||dummy|
|ind_plan_fin_ult1| |int64||dummy|
|ind_pres_fin_ult1| |int64|1의 비율이 낮음|dummy|
|ind_reca_fin_ult1| |int64||dummy|
|ind_tjcr_fin_ult1| |int64||dummy|
|ind_valo_fin_ult1| |int64||dummy|
|ind_viv_fin_ult1| |int64|1의 비율이 낮음|dummy|
|ind_nomina_ult1| |float64-> int64||dummy|
|ind_nom_pens_ult1| |float64-> int64||dummy|
|ind_recibo_ult1| |int64||dummy|

- 책에서는 굳이 소수일 필요가 없는 변수에 대해서 정수로 변환하고 있다. (메모리 효율)
- 다음 프로젝트부터는 이 파일을 제일 먼저 만들어 놓고 진행하면서 채워나가야겠다. 한 군데에 모아 정리해놓는 게 좋은 방법인 것 같다.
