# Information Disclosure

## Explanation
Its all about sensitive data leaks like usernames or commercial data, or APIs keys … etc
https://portswigger.net/web-security/information-disclosure

- Try always cause an errors to see the stackTrace or frameworks versions

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

Where to find it?
- Backup files (zip, tar, tgz, sql, rar, tar.gz)
- Hidden files (.fileName)
- Source code repo (.git, .svn)
- Source code files (.old, .bak, .php~, .swp)
- JS files
- Search Public Github

## Tools
- Git: [DVCS-Pillage](https://github.com/evilpacket/DVCS-Pillage) dump source code from .git folder
- Sample report for which sensitive API key was disclosed: https://hackerone.com/reports/396467
- Tips and trick on searching companies public github repos: https://gist.github.com/EdOverflow/922549f610b258f459b219a32f92d10b
- Mazen Ahmed tool to clone public github projects of companies: https://github.com/mazen160/GithubCloner
- SVN extractor: https://github.com/anantshri/svn-extractor
- Bo0om file names list: https://github.com/Bo0oM/fuzz.txt
- Dirsearch: https://github.com/maurosoria/dirsearch
  
## Labs
- 
