# TyporaIframeSpoofing Vulnerability


## Vulnerability Overview

Dragging URLs from cross domain iframes deleted during the drag process may lead to user confusion and website spoofing attacks. This vulnerability affects Typora<=1.8.10. The html tag is 

````
<iframe src="https://www.bing.com">test</iframe>
````



## Vulnerability Reproduction

1. Download the lastest version of Typora from https://typora.io/.

   The version when I downloaded was `1.8.10`.

   ![(https://github.com/0x0fc/TyporaIframe/blob/main/images/iframe1.png)
](https://github.com/0x0fc/TyporaIframe/blob/main/images/iframe1.png)
2. Use Typora to open or edit a markdown file.

   For example, I created a file called “iframeTest.md” with typora.

   ![(https://github.com/0x0fc/TyporaIframe/blob/main/images/iframe2.png)](https://github.com/0x0fc/TyporaIframe/blob/main/images/iframe2.png)

3. Enter `<iframe src="https://www.bing.com">test</iframe>` to let Typora parse the html tags, resulting in the execution of malicious html.

   When just entering the embed tag:

   ![(https://github.com/0x0fc/TyporaIframe/blob/main/images/iframe3.png)](https://github.com/0x0fc/TyporaIframe/blob/main/images/iframe3.png)

   After Typora parses the iframe tag:

   ![(https://github.com/0x0fc/TyporaIframe/blob/main/images/iframe4.png)](https://github.com/0x0fc/TyporaIframe/blob/main/images/iframe4.png)
