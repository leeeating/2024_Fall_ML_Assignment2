data shape : (47127338, 92)

date_id : 0 - 1698
每個partition有170個date id

date id 0-249  drop : 00 01 02 03 04 21 26 27 31   

time_id : 0 - 967
前510個date id的time id只有到848，之後是到967

symbol_id : 0 - 38
每個日期分段會有不同數量的symbol

weight_id
同一天內的同一symbol id有相同的weight

feature 15在time id為24之前都為null
feature 17在time id為4之前都為null
feature_73, feature_74在time id為8 or 9之前都為null

插補feature 51, feature 54在dateid<=676, time id=369

feature     : null count    time_interval
39, 42      : 1555437       0-67(69, 70)
50, 53      : 1555432       0-67
41, 44      : 411736        0-17(18, 20)
52, 55      : 411732        0-17
73, 74      : 220124
32, 33, 58  : 217794
75, 76      : 35658         random 
77, 78      : 7885          random
45, 46      : 2850          
65, 66      : 2850



32, 58, 73, 74
75, 76

與date_id, symbol_id有關：feat 9, 10, 11, 20-30, weight_id


test data, 如果time_id == 0不會有lag資訊
for date in test_data['date_id'],unique():
    test_batch = (test_data['date_id] == 0)
    for time in test_batch['time_id'].unique()
        final batch = (test_batch['time_id'] == 0)
        


