# Micro CMS v1

<b>Notice: the key numbers mentioned may be variable.</b>

```
.
├── (homepage）
└── page/
    ├── 1 (Testing)
    ├── 2 (Markdown Test)
    ├── 3 (?)
    ├── ...(?)
    ├── 10 (?)
    ├── 11 (the first page you created)
    ├── create
    └── edit/
          ├── 1 (Testing)
          ├── 2 (Markdown Test)
          ├── 3 (?)
          ├── ...(?)
          ├── 10 (?)
          └── 11 (the first page you created)        
```
It's noticeable that the serial number 3-10 are skipped when we created new pages.
When it comes to /page/edit/7, the 1st flag can be found.

We can try XSS-injection by inputing scripts when creating new pages.
[1-xss](img/1-XSS.png)

[2-xss](img/2-XSS.png)
After submitting, the page/12 itself remains normal; however, when it comes to the homepage...
[3-xss](img/3-XSS.png)

Here the 2nd flag is!
When we check the source code of homepage and compares it with normal homepage, we'll know why.
[4-xss](img/4-XSS.png)
[5-xss](img/5-XSS.png)
