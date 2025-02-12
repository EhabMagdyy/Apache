## Notes
> ### Make sure that apache2 is enabled & active
```bash
sudo systemctl status apache2
```

> ### To check syntax of apache2.conf file
```bash
sudo apachectl configtest
```

> ### After making change, run
```bash
sudo systemctl restart apache2
```

> ### Authenticatin: password and username (in var/www/html/)
```bash
sudo htpasswd -c .<passwdname> <username>
```

> ### Protection to "Project" Directory (apache2.conf)
```bash
<Directory /var/www/html/Project>
        AuthType Basic
        AuthName "Restricted web page"
        AuthUserFile "/var/www/html/.htpasswd"
        require valid-user 
</Directory>
```

---

## 1.Change Default file index.html -> default.html
```bash
# in apache2.conf
<Directory /var/www/html>
    DirectoryIndex default.html index.html index.php
</Directory>
```

```bash
localhost/ -> default.html
```

---

## 2.Redirect Example
> ### Page1.html will takes you to page2.html
```bash
localhost/Redirect/page1.html
```

---

## 3.Project Example
> ### Page1.html will takes you to page2.html
```bash
localhost/Project/
```
> ![Image](https://github.com/user-attachments/assets/f5a54ffa-a232-4035-adef-38c37f90bd66)
