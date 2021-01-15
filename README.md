## ProbSpace スパムメール判別 2nd Place Solution  
https://prob.space/competitions/spam_mail  
## 解法  
### Model  
[トピック](https://prob.space/competitions/spam_mail/discussions/pop-ketle-Post29c55c7e659c8dc3ea45)で承認されたsimpletransformersのRoBERTaを使用しました  
詳細なパラメータや内容についてはコードをご覧ください　　
### Validation  
StratifiedKFold 7-Fold(3 random seed average)  
### Preprocessing  
cha_kabuさんの[baseline](https://prob.space/competitions/spam_mail/discussions/cha_kabu-Postd207047dddb824a851d4)とほとんど同じで、stopwordsやurlなどを削除しています  
### Pseudo Labeling
不均衡データでも高いf値が出ていたMultinomialNBモデルを使用しました   
### Postprocessing
テストデータのスパムメールの確率上位17000件をスパムメールとしました  
