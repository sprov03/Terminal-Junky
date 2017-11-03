Terminal notes


    nohup sudo rsync -avr --stats -e "ssh -i $HOME/.ssh/id_rsa" myserveralias:/home/leadprop/public_html/leadpropeller/shared/public/sites /var/www/leadpropeller/storage/shared >> rsync-sites-output &
    nohup sudo rsync -avr --stats -e "ssh -i $HOME/.ssh/id_rsa" myserveralias:/home/leadprop/public/api/storage/public/previews /var/www/leadpropeller/storage/shared >> rsync-previews-output &
    

    sudo find /var/www/ -type d -exec chmod 0775 {} \;
   
    sudo find /var/www/ -type f -exec chmod 0764 {} \;
    
    sudo chown -R apache:www /var/www/
