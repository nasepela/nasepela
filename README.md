## Hi there 👋

<!--
**nasepela/nasepela** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
cd /var/www/
composer create-project laravel/laravel nasepela
sudo nano /etc/apache2/sites-available/nasepela.conf
<VirtualHost *:80>
    ServerName nasepela.com
    DocumentRoot /var/www/nasepela/public

    <Directory /var/www/nasepela>
        AllowOverride All
    </Directory>

    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
