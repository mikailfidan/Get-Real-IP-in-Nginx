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
                set_real_ip_from ipv4;
                real_ip_header ClientSourceIP;
        }
