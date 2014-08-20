ffmpeg + openresty(redis, lua, etc)
===========

## openresty

openresty

/usr/local/openresty にインストールされる

`/usr/local/openresty/nginx/` 以下にnginxに関わるのファイルが入っている。


## nginx.conf.template


### なぜ template

起動スクリプト`appinit` が実行されると

`nginx.conf.template` の `{{ XXX }}` とされた部分が

環境変数`XXX` の値と置き換わり nginx.conf として保存されるようになっている。 

### include

- http ディレクティブ外で `include /usr/local/openresty/nginx/conf/rtmp_conf/*.conf`
- http ディレクティブ内で `include /usr/local/openresty/nginx/conf/server_conf/*.conf`


