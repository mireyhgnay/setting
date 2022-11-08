## grunt default 실행 시,  ‼️ grunt-cli 오류 발생

🔗 [https://alnair.tistory.com/44](https://alnair.tistory.com/44)

```bash
grunt-cli: The grunt command line interface (v1.3.1)

Fatal error: Unable to find local grunt.

If you're seeing this message, grunt hasn't been installed locally to

your project. For more information about installing and configuring grunt,

please see the Getting Started guide:

https://gruntjs.com/getting-started
```

**해결 방법** 

```bash
**npm install grunt --save-dev**
```