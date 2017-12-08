# fav_spam_blocker
fav_spam_blocker_for_twitter

Mac-OSXで動作確認済。python3スクリプトです。

使用にはCONSUMER_KEY、CONSUMER_SECRET、TOKEN、TOKEN_SECRETの取得が必要です。

https://apps.twitter.com/

上記リンクから登録し、各種KEYの取得が必要になります。参考リンク：http://phiary.me/twitter-api-key-get-how-to/

`usage: fav_spam_blocker.py [-h] --consumer-key CONSUMER_KEY --consumer-secret
                           CONSUMER_SECRET --token TOKEN --token-secret TOKEN_SECRET
                           --user-name USER_NAME [--num-digits NUM_DIGITS]
                          [--unlock]`

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
                             --num-digits 2
                             --unlock`

を実行します。


