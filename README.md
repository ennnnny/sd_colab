# **colab_stable_diffusion_webui**
[![](https://img.shields.io/static/v1?message=Open%20in%20Colab&logo=googlecolab&labelColor=5c5c5c&color=0f80c1&label=%20&style=flat)](https://colab.research.google.com/github/ennnnny/sd_colab/blob/self/230512.ipynb)

## 防掉线措施
有时候掉线是因为网络不稳定，有时候就是谷歌的验证机制了
听说可以通过自动点击来减少掉线频率，这时候可以利用javascript的语法，类似与不间断的点击得到以下代码
在Google colab的按F12，点击网页的控制台，粘贴如下代码：
```JS
function ConnectButton(){
  console.log("Connect pushed");
  document.querySelector("#top-toolbar > colab-connect-button").shadowRoot.querySelector("#connect").click()
}
setInterval(ConnectButton,60000);
```