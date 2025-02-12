### To check syntax of apache2.conf file:
```bash
sudo apachectl configtest
```

### After making change, run:
```bash
sudo systemctl restart apache2
```

## 1.Change Default file index.html -> default.html
```bash
# in apache2.conf
<Directory /var/www/html>
    DirectoryIndex default.html index.html index.php
</Directory>
```
