1, AWSのEC2にアクセスして、インスタンスの状態をRunningにする

2, ssh -i "ubuntu16.pem" ubuntu@ec2-13-230-150-249.ap-northeast-1.compute.amazonaws.comでアクセスする
   IPが変わるので、インスタンスのIPv4 パブリックを参照する

3, $ sudo vi /home/ubuntu/myblogapp2/myblogapp/myblogapp/settings.py
   $ sudo vi /etc/nginx/sites-available/myblogapp
   上記のファイルのIPを変更

4, $ sudo systemctl restart nginx
   $ sudo systemctl restart gunicorn
   常軌を実行

5, http://13.231.153.105/posts/にアクセスする。こちらもIPが変化しているので注意
