# Get-Real-IP-in-Nginx
Getting real ip in nginx behind WAF

 location @localhost{
              
                proxy_set_header X-Real-IP $remote_addr;
                proxy_set_header Host $host;
                proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
                ...
                ...
                ...
                
                #Get Real IP
                set_real_ip_from 192.168.x.x;
                real_ip_header ClientSourceIP;
        }
