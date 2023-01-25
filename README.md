<h2 align="center">Usage of Dirsearch</h2>

### full URL & plain text output scan
    dirsearch --full-url --format plain -o scan.txt -u http://testphp.vulnweb.com

### full url, plaintext output, custom wordlist
    dirsearch --full-url --format plain -o scan.txt -w /usr/share/wordlists/SecLists/Discovery/Web-Content/common.txt -u http://testphp.vulnweb.com