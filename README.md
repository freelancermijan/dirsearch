<h2 align="center">Usage of Dirsearch</h2>

### Full URL & plain text output scan
    sudo dirsearch --full-url --format plain -o dirsearchScan.txt -u http://testphp.vulnweb.com

### Full url, plaintext output, custom wordlist
    sudo dirsearch --full-url --format plain -o dirsearchScan.txt -w /usr/share/wordlists/SecLists/Discovery/Web-Content/common.txt -u http://testphp.vulnweb.com

### Full url, plaintext output, wordlist, add extensions
    sudo dirsearch --full-url --format plain -o dirsearchScan.txt -e php,html,js -w /usr/share/wordlists/SecLists/Discovery/Web-Content/common.txt -u http://testphp.vulnweb.com

### Full url, plaintext output, wordlist, add extensions & exclude extension
    sudo dirsearch --full-url --format plain -o dirsearchScan.txt -e php,html,js -X xml -w /usr/share/wordlists/SecLists/Discovery/Web-Content/common.txt -u http://testphp.vulnweb.com

### above all + status code
    sudo dirsearch --full-url --format plain -o dirsearchScan.txt -e php,html,js -i 200,302 -w /usr/share/wordlists/SecLists/Discovery/Web-Content/common.txt -u http://testphp.vulnweb.com

### above all + Exclude Extensions
    sudo dirsearch --full-url --format plain -o dirsearchScan.txt -e php,html,js --exclude-extensions=xml,ico -i 200,301 -w /usr/share/wordlists/SecLists/Discovery/Web-Content/common.txt -u http://testphp.vulnweb.com

### Full url, output plzintext, include extension, exclude extension, status code, recursive mode
    sudo dirsearch --full-url --format plain -o scan.txt -e php,html,js --exclude-extensions=xml,ico -i 200,301 -r 3 -w /usr/share/wordlists/SecLists/Discovery/Web-Content/common.txt -u http://testphp.vulnweb.com

### Full url, output plzintext, include extension, exclude extension, status code, recursive mode+loop
    sudo dirsearch --full-url --format plain -o scan.txt -e php,html,js --exclude-extensions=xml,ico -i 200,301 -r --deep-recursive 3 -w /usr/share/wordlists/SecLists/Discovery/Web-Content/common.txt -u http://testphp.vulnweb.com

### Full url, output plzintext, include extension, exclude extension, status code, recursive mode+loop, threads
    sudo dirsearch --full-url --format plain -o scan.txt -e php,html,js --exclude-extensions=xml,ico -i 200,301 -r --deep-recursive 3 -t 20 -w /usr/share/wordlists/SecLists/Discovery/Web-Content/common.txt -u http://testphp.vulnweb.com