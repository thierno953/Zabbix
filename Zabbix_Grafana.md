# Installation de Grafana avec intégration Zabbix

```sh
# Install Grafana

sudo apt install -y apt-transport-https software-properties-common wget

sudo mkdir -p /etc/apt/keyrings/

wget -q -O - https://apt.grafana.com/gpg.key | gpg --dearmor | sudo tee /etc/apt/keyrings/grafana.gpg > /dev/null

echo "deb [signed-by=/etc/apt/keyrings/grafana.gpg] https://apt.grafana.com stable main" | sudo tee -a /etc/apt/sources.list.d/grafana.list

sudo apt update
sudo apt install -y grafana

sudo systemctl start grafana-server
sudo systemctl enable grafana-server

#  Install Zabbix Plugin

sudo grafana-cli plugins install alexanderzobnin-zabbix-app
sudo systemctl restart grafana-server

Grafana -> http://your-server-ip:3000

# API_URL

http://<IP_ZABBIX>/zabbix/api_jsonrpc.php
```

![grafana](/assets/grafana_01.png)

![grafana](/assets/grafana_02.png)

![grafana](/assets/grafana_03.png)

![grafana](/assets/grafana_04.png)

![grafana](/assets/grafana_05.png)

![grafana](/assets/grafana_06.png)

![grafana](/assets/grafana_07.png)

![grafana](/assets/grafana_08.png)

![grafana](/assets/grafana_09.png)

https://grafana.com/grafana/dashboards/5363-zabbix-full-server-status/

![grafana](/assets/grafana_10.png)

![grafana](/assets/grafana_11.png)

![grafana](/assets/grafana_12.png)

![grafana](/assets/grafana_13.png)

![grafana](/assets/grafana_14.png)

![grafana](/assets/grafana_15.png)

![grafana](/assets/grafana_16.png)
