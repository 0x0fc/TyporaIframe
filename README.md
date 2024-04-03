# TyporaIframeSpoofing Vulnerability

版本允许通过IFRAME元素向Messager组件注入HTML。

## Vulnerability Overview

Dragging URLs from cross domain iframes deleted during the drag process may lead to user confusion and website spoofing attacks. This vulnerability affects Typora<=1.8.10. The html tag is 

````
<iframe src="https://www.bing.com">test</iframe>
````



## Vulnerability Reproduction

1. Download the lastest version of Typora from https://typora.io/.

   The version when I downloaded was `1.8.10`.

   ![image-20240403212357118](./image/image-20240403212357118.png)

2. Use Typora to open or edit a markdown file.

   For example, I created a file called “iframeTest.md” with typora.

   ![image-20240403212654466](./image/image-20240403212654466.png)

1. Enter `<iframe src="https://www.bing.com">test</iframe>` to let Typora parse the html tags, resulting in the execution of malicious html.

   When just entering the embed tag:

   ![image-20240403212843513](./image/image-20240403212843513.png)

   After Typora parses the iframe tag:

   ![image-20240403212909845](./image/image-20240403212909845.png)
