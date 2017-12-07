# fav_spam_blocker
fav_spam_blocker_for_twitter

`usage: fav_spam_blocker.py [-h] --consumer-key CONSUMER_KEY --consumer-secret
                           CONSUMER_SECRET --token TOKEN --token-secret TOKEN_SECRET
                           --user-name USER_NAME [--num-digits NUM_DIGITS]
                          [--unlock]`

`optional arguments:
  -h, --help            show this help message and exit
  --consumer-key CONSUMER_KEY
  --consumer-secret CONSUMER_SECRET
  --token TOKEN
  --token-secret TOKEN_SECRET
  --user-name USER_NAME
  --num-digits NUM_DIGITS
  --unlock`
  
文字＋連番のツイッターアカウントをブロックします。スクリプト内でtweepyを使用していますので、インストールが必要です。

`pip3 install tweepy`

例えば

`python3 fav_spam_blocker.py --consumer-key CONSUMER_KEY 
                             --consumer-secret CONSUMER_SECRET 
                             --token TOKEN 
                             --token-secret TOKEN_SECRET
                             --user-name monarisa 
                             --num-digits 2`

を実行すると、@monarisa00 ~ @monarisa99 のツイッターアカウントを全てブロックします。num_digitsが数字の桁数を指します。--num-digits 3 であれば @monarisa000 ~ @monarisa999 のツイッターアカウントを全てブロックします。

ブロック解除するときは --unlock オプションをつけて

`python3 fav_spam_blocker.py --consumer-key CONSUMER_KEY 
                             --consumer-secret CONSUMER_SECRET 
                             --token TOKEN 
                             --token-secret TOKEN_SECRET
                             --user-name monarisa 
                             --num-digits 3
                             --unlock`

を実行します。


