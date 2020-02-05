# 데이터 특징 노트
|변수명|내용|타입|특징|아이디어|
|------|---|---|---|---|
|fecha_dato|월별날짜데이터|object|2015.01.28~2016.05.28 매달 28일에 데이터가 기록됨(17개월) |연,월,일 분류|
|ncodpers|고객고유번호|int64|| id값으로 학습시 사용 x, unique개수 볼 필요 있음|
|ind_empleado|고용지표|object|99,9%가 N:not emplyee로 되어있음 |의미 없는 변수|
|pais_residencia|고객거주국가|object|99,5%가 ES로 기록되어 있음 |의미 없는 변수|
|sexo|
|age|고객성별|object -> int64| 범주형으로 되어있음, 23세가 가장 많음 |정수형으로 변환 필요
|fecha_alta|고객 첫 거래 날짜|object|날짜데이터| |
|ind_nuevo|
|antiguedad|거래 누적 기간(월)|object -> int64|-999999,NA 존재|수치형으로 취급 가능|
|indrel|
|ult_fec_cli_1t|중요고객 만료날짜|object|결측치가 많음||
|indrel_1mes|월초기준 고객등급 | object|'1'과 '1.0'이 다른값으로 존재| '1','1.0' 등을 같게 하고 P등급을 편의상 5로 변환|
|tiprel_1mes|
|indresi|
|indext| || 95%가 태어난 국적과 은행이 다름 | 5%의 개인화추천 가능?|
|conyuemp|은행 직원의 배우자 여부|object|결측치가 많음||
|canal_entrada|
|indfall| | | 99.7%의 고객이 살아있음 | 의미 없는 변수
|tipodom|
|cod_prov|
|nomprov|
|ind_actividad_cliente|
|renta|
|segmento|object|3개의 범주||
|ind_ahor_fin_ult1|
|ind_aval_fin_ult1|
|ind_cco_fin_ult1|
|ind_cder_fin_ult1|
|ind_cno_fin_ult1|
|ind_ctju_fin_ult1|
|ind_ctma_fin_ult1
|ind_ctop_fin_ult1|
|ind_ctpp_fin_ult1|
|ind_deco_fin_ult1|
|ind_deme_fin_ult1|
|ind_dela_fin_ult1|
|ind_ecue_fin_ult1|
|ind_fond_fin_ult1|
|ind_hip_fin_ult1|
|ind_plan_fin_ult1|
|ind_pres_fin_ult1|
|ind_reca_fin_ult1|
|ind_tjcr_fin_ult1|
|ind_valo_fin_ult1|
|ind_viv_fin_ult1|
|ind_nomina_ult1|
|ind_nom_pens_ult1|
|ind_recibo_ult1|


다음 프로젝트부터는 이 파일을 제일 먼저 만들어 놓고 진행하면서 채워나가야겠다. 한 군데에 모아 정리해놓는 게 좋은 방법인 것 같다.
