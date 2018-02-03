## github demo
## oauth.html
https://gnjo.github.io/githubdemo/oauth.html

~~https://gnjo.github.io/githubdemo/old_oauth.html~~

## oauth にfetchを使うと色々な問題が発生する。
 - 1. 'mode': 'cors' ; が使えない。この場合は、access allow or no-corsと言われる。
 - 2. 'mode': 'no-cors'; で行うと認証は成功するが response.type = opaque となる。タイプが不透明になると、 .json()が使えない。
  - 但し、唯一、 .text()は リクエストヘッダに 'Content-Type':'text/plain' で動作するが、この場合 .text()は常に空を返す。
 
結論として、oauthにfetchを使うのは難しい。 githubならbasic認証であれば fetchを使える。
