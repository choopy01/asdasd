$ProgressPreference = 'SilentlyContinue'
Invoke-WebRequest -Uri https://artifacts.elastic.co/downloads/beats/elastic-agent/elastic-agent-8.19.4-windows-x86_64.zip -OutFile elastic-agent-8.19.4-windows-x86_64.zip 
Expand-Archive .\elastic-agent-8.19.4-windows-x86_64.zip -DestinationPath .
cd elastic-agent-8.19.4-windows-x86_64
.\elastic-agent.exe install --url=https://192.168.87.27:8220 --enrollment-token=UUZWRG81a0JiOG93QWlIMlhvSEo6bHdZYlJjeGZKT295azBndXdGdGpzUQ==
