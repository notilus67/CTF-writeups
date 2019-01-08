# Micro CMS v1

<b>Notice: the key numbers mentioned may be variable.</b>

```
.
├── (mainpage）
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
When it comes to /page/edit/7, the first flag can be found.

We can try XSS-injection by inputing scripts when creating new pages.
