### using vim
vim 'filename'
I to insert
ESC to quit
```:w``` to write
```:wq``` to quit and write
```:qa!``` to forcequit without savings

cat 'filename'
to peek whats inside the file


dirs:
/etc/nginx/sites-enabled
/var/www/dir...

### default nginx script (static html) can also be found by typing "cat /etc/nginx/sites-enabled/default"
```
server {
       listen 80;
       listen [::]:80;

       listen 443;
       listen [::]:443;

       server_name cornelius.nottiketcom.xyz;

       root /var/www/cornelius.nottiketcom.xyz; # or any dir you want
       index index.html index.nginx-debian.html; # or whatever the filename is

       location / {
               try_files $uri $uri/ =404;
       }
}
```
