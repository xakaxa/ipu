~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
rm -rf *.md

mv nuclei /usr/bin/nuclei
chmod +x /usr/bin/nuclei
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
nuclei -l li.txt -t detect.yaml  -o re.txt -stats
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
nuclei -update-template-dir /dir/nuclei-templates -update-templates
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
https://gist.githubusercontent.com/ozuma/fb21ab0f7143579b1f2794f4af746fb2/raw/a4fa934311b8b9ed11fa6136d05565356601e991/blacklist.dat
masscan -Pn -sS -iL list.txt --rate 150000 -p1234 --open-only --excludefile block.txt --output-format list --output-file 1234.txt
36789.txt
awk '{ print $4 ":" $3 }' list.txt > 1.txt
wc -l 1.txt
rm -rf list.txt
mv 1.txt list.txt
curl bashupload.com -T list.txt
cat list.txt  | sed 's/.*/https\:\/\/&/' > list_h.txt
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
cat scan.txt | nuclei -stats -t cves -t exposures -t network -t default-logins -t vulnerabilities -t exposed-panels -t file -t iot  -bs 100 -c 50    -o scan.nuclei
cat scan2.txt | httpx -random-agent -nf -rl 5000 -t 1000 -p <ports> -stats  | nuclei -stats -t cves -t exposures -t network -t default-logins -t vulnerabilities -t exposed-panels -t file -t iot  -bs 100 -c 50    -o scan.nuclei
nuclei -l scan.txt -t /root/nuclei-templates/http/cves/2024/CVE-2024-123456.yaml -o results.txt -stats
grep -rl 'remote.*code.*execution' ~/nuclei-templates/ | xargs cp -t /root/NucleiRCE/
nuclei -l scan.txt -t /root/NucleiRCE/ -o results2.txt -stats
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
cat domains | /root/Downloads/nuclei -t tmpx -bs 1 -c 1 -nc -rate-limit 64 -timeout 7 -stats -retries 2 -H "User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:72.0) Gecko/20200101 Firefox/72.0"
cat domains | /root/Downloads/nuclei -t tmpx -bs 1 -c 1 -nc -rate-limit 64 -timeout 7 -stats -retries 2 -H "User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:72.0) Gecko/20200101 Firefox/72.0"
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
nuclei -w self-nuclei-templates/workflow/wordpress.yaml -u https://www.google.com:443 -rl 1000 -c 1000   -retries 1 -stats
nuclei -t self-nuclei-templates/wordpress/  -u https://www.google.com:443 -rl 1000 -c 1000   -retries 1 -stats
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-elog errors.txt
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
cat scan .txt | nuclei -stats -t cves -t exposures -t network -t default-logins -t vulnerabilities -t exposed-panels -t file -t iot -o scan.nuclei
cat scan .txt | nuclei -stats -t cves -t exposures -t network -t default-logins -t vulnerabilities -t exposed-panels -t file -t iot -o scan.nuclei
cat scan .txt | nuclei -stats -t cves -t exposures -t network -t default-logins -t vulnerabilities -t exposed-panels -t file -t iot -o scan.nuclei
nuclei -l alive.txt -stats -o res.txt -c 100  |& tee log.txt     
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
go run . -duc  -nh -retries 0 -rl 100 -bs 200 -target http://0.0.0.0:2379/debug_mode_nuclei_dump -t test.yaml -v
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
cat scan.txt | nuclei -stats -t cves -t exposures -t network -t default-logins -t vulnerabilities -t exposed-panels -t file -t iot  -bs 100 -c 50    -o scan.nuclei
cat scan2.txt | httpx -random-agent -nf -rl 5000 -t 1000 -p <ports> -stats  | nuclei -stats -t cves -t exposures -t network -t default-logins -t vulnerabilities -t exposed-panels -t file -t iot  -bs 100 -c 50    -o scan.nuclei
nuclei -l scan.txt -t /root/nuclei-templates/http/cves/2050/CVE.yaml -o results.txt -stats
grep -rl 'remote.*code.*execution' ~/nuclei-templates/ | xargs cp -t /root/NucleiRCE/
nuclei -l scan.txt -t /root/NucleiRCE/ -o results2.txt -stats
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
cat scan .txt | nuclei -stats -t cves -t exposures -t network -t default-logins -t vulnerabilities -t exposed-panels -t file -t iot -o scan.nuclei
nuclei -l /opt/assets/webs.txt -tags druid,springboot,nacos -timeout 10 -bs 100 -c 10 -rl 150 -mhe 10 -tlsi -o /opt/assets/nuclei-all.txt -stats
go run . -l /opt/assets/webs.txt -tags druid,springboot,nacos -timeout 10 -bs 100 -c 10 -rl 150 -mhe 10 -tlsi -o /opt/assets/nuclei-all.txt -stats
nuclei -sa -t $PWD/config/nuclei-templates -no-strict-syntax -severity critical,high,medium -type http,network,websocket,dns,ssl -report-config $PWD/config/nuclei_esConfig.yaml  -ztls -config-directory ${PWD}/config/nuclei -interactions-cache-size 5000 -interactions-eviction 60 -interactions-poll-duration 5 -interactions-cooldown-period 5 -max-host-error 5 -duc -json -o paypal_nuclei.json
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~













