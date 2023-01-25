<h2 align="center">Usage of Dirsearch</h2>

### Full URL & plain text output scan
    dirsearch --full-url --format plain -o scan.txt -u http://testphp.vulnweb.com

### Full url, plaintext output, custom wordlist
    dirsearch --full-url --format plain -o scan.txt -w /usr/share/wordlists/SecLists/Discovery/Web-Content/common.txt -u http://testphp.vulnweb.com

### Full url, plaintext output, wordlist, add extensions
    dirsearch --full-url --format plain -o scan.txt -e php,html,js -w /usr/share/wordlists/SecLists/Discovery/Web-Content/common.txt -u http://testphp.vulnweb.com

### Full url, plaintext output, wordlist, add extensions & exclude extension
    dirsearch --full-url --format plain -o scan.txt -e php,html,js -X xml -w /usr/share/wordlists/SecLists/Discovery/Web-Content/common.txt -u http://testphp.vulnweb.com

### above all + status code
    dirsearch --full-url --format plain -o scan.txt -e php,html,js -i 200,302 -w /usr/share/wordlists/SecLists/Discovery/Web-Content/common.txt -u http://testphp.vulnweb.com

### above all + Exclude Extensions
    dirsearch --full-url --format plain -o scan.txt -e php,html,js --exclude-extensions=xml,ico -i 200,301 -w /usr/share/wordlists/SecLists/Discovery/Web-Content/common.txt -u http://testphp.vulnweb.com